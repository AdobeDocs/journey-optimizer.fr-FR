---
solution: Journey Optimizer
product: journey optimizer
title: Fonctions de gestion des collections
description: En savoir plus sur les types de données dans les fonctions de gestion des collections
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 09b38179-9ace-4921-985b-ddd17eb64681
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '603'
ht-degree: 0%

---

# Fonctions de gestion des collections {#collection-management-functions}

Le langage d’expression introduit également un ensemble de fonctions pour interroger les collections.

Ces fonctions sont expliquées ci-dessous. Dans les exemples suivants, nous allons utiliser la payload d’événement contenant une collection :

```json
                { 
   "_experience":{ 
      "campaign":{ 
         "message":{ 
            "profile":{ 
               "pushNotificationTokens":[ 
                  { 
                     "token":"token_1",
                     "application":{ 
                        "_id":"APP1",
                        "name":"MarltonMobileApp",
                        "version":"1.0"
                     }
                  },
                  { 
                     "token":"token_2",
                     "application":{ 
                        "_id":"APP2",
                        "name":"MarketplaceApp",
                        "version":"1.0"
                     }
                  },
                  { 
                     "token":"token_3",
                     "application":{ 
                        "_id":"APP3",
                        "name":"VendorApp",
                        "version":"2.0"
                     }
                  }
               ]
            }
         }
      }
   },
   "timestamp":"1536160728"
}
```

**La fonction &quot;all(`<condition>`)&quot;**

Le **[!UICONTROL all]** active la définition d’un filtre sur une collection donnée en utilisant une expression booléenne.

```json
<listExpression>.all(<condition>)
```

Par exemple, parmi tous les utilisateurs de l’application, vous pouvez obtenir ceux qui utilisent IOS 13 (expression booléenne &quot;app used == IOS 13&quot;). Le résultat de cette fonction est la liste filtrée contenant les éléments correspondant à l’expression booléenne (exemple : utilisateur 1 de l’application, utilisateur 34 de l’application, utilisateur 432 de l’application).

Dans une activité Condition de source de données , vous pouvez vérifier si le résultat de la variable **[!UICONTROL all]** est nulle ou non. Vous pouvez également combiner les **[!UICONTROL all]** avec d’autres fonctions, telles que **[!UICONTROL count]**. Pour plus d’informations, voir [Activité Condition de source de données](../condition-activity.md#data_source_condition).

**Exemple 1 :**

Nous voulons vérifier si un utilisateur a installé une version spécifique d’une application. Pour ce faire, nous obtenons tous les jetons de notification push associés aux applications mobiles dont la version est égale à 1.0. Ensuite, nous exécutons une condition avec la variable **[!UICONTROL count]** pour vérifier que la liste de jetons renvoyée contient au moins un élément .

```json
count(@{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all(currentEventField.application.version == "1.0").token}) > 0
```

Le résultat est vrai.

**Exemple 2 :**

Ici, nous utilisons la méthode **[!UICONTROL count]** pour vérifier si la collection contient des jetons de notification push.

```json
count(@{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) > 0
```

Le résultat sera vrai.

<!--Alternatively, you can check if there is no token in the collection:

   ```json
   count(@{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) == 0
   ```

The result will be false.

Here we use the count function in a condition to count the number of push notification tokens in the event.

`count(@{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token})`

The result is true.

Note that when the condition in the **all()** function is empty, the filter will return all the elements in the list. Hence, the expression above is equivalent to:

`count(@{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.application.name})`

In both cases, the result of the expression is **3**.

A query of experience events recorded on the Adobe Experience Platform may or may not include the current event that triggered the current Journey. This will depend on the relative processing time with which [!DNL Journey Orchestration] sees an event and started evaluating conditions, versus the time it takes for that event to be ingested into the Adobe Experience Platform. For example, when using the .all() syntax to query experience events from the Adobe Experience Platform, we recommend enforcing the exclusion of the current event (by requiring an
earlier timestamp) in order to only consider prior events.-->

>[!NOTE]
>
>Lorsque la condition de filtrage dans la variable **all()** est vide, le filtre renvoie tous les éléments de la liste. **Toutefois, pour comptabiliser le nombre d’éléments d’une collection, la fonction all n’est pas obligatoire.**


```json
count(@{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.token})
```

Le résultat de l’expression est **3**.

**Exemple 3 :**

Nous vérifions ici si une personne n’a reçu aucune communication au cours des dernières 24 heures. Nous filtrons la collection d’événements d’expérience récupérés à partir de la source de données Experience Platform, à l’aide de deux expressions basées sur deux éléments de la collection. En particulier, l’horodatage de l’événement est comparé à la valeur dateTime renvoyée par la variable **[!UICONTROL nowWithDelta]** fonction .

```json
count(#{ExperiencePlatform.MarltonExperience.experienceevent.all(
   currentDataPackField.directMarketing.sends.value > 0 and
   currentDataPackField.timestamp > nowWithDelta(-1, "days")).timestamp}) == 0
```

Le résultat sera true si aucun événement d’expérience ne correspond aux deux conditions.

**Exemple 4 :**

Ici, nous voulons vérifier si une personne a lancé une application au moins une fois au cours des 7 derniers jours, afin, par exemple, de déclencher une notification push l’invitant à démarrer un tutoriel.

```json
count(
 #{ExperiencePlatform.AnalyticsData.experienceevent.all(
 nowWithDelta(-7,"days") <= currentDataPackField.timestamp
 and currentDataPackField.application.firstLaunches.value > 0
)._id}) > 0
```

<!--**"All + Count" example 4:** here we use the count function in a boolean expression to see if there is push notification tokens in the collection.

`count(@{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().application.name}) > 0`

The result will be:

`true`

Alternatively, you can check if there is NO token in the collection:

`count(@{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().application.name}) =0`

The result will be:

`false`-->

>[!NOTE]
>
>**[!UICONTROL currentEventField]** n’est disponible que lors de la manipulation de collections d’événements et **currentDataPackField**
>lors de la manipulation de collections de sources de données. Lors du traitement de collections avec **[!UICONTROL all]**, **[!UICONTROL first]** et **[!UICONTROL last]**, we
>sur chaque élément de la collection, un par un. **[!UICONTROL currentEventField]** et **currentDataPackField**
>correspondent à l’élément en boucle.

**Les fonctions &quot;first(`<condition>`)&quot; et &quot;last(`<condition>`)&quot;**

Le **[!UICONTROL first]** et **[!UICONTROL last]** Les fonctions activent également la définition d’un filtre sur la collection tout en renvoyant le premier/dernier élément de la liste qui correspond au filtre.

_`<listExpression>.first(<condition>)`_

_`<listExpression>.last(<condition>)`_

**Exemple 1 :**

Cette expression renvoie le premier jeton de notification push associé aux applications mobiles dont la version est égale à 1.0.

```json
@{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.first(currentEventField.application.version == "1.0").token
```

Le résultat est &quot;token_1&quot;.

**Exemple 2 :**

Cette expression renvoie le dernier jeton de notification push associé aux applications mobiles dont la version est égale à 1.0.

```json
@{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.last(currentEventField.application.version == "1.0").token}
```

Le résultat est &quot;token_2&quot;.

>[!NOTE]
>
>Les événements d’expérience sont récupérés à partir d’Adobe Experience Platform sous la forme d’une collection dans l’ordre chronologique inverse. Par conséquent :
>
>* **[!UICONTROL first]** renvoie l’événement le plus récent.
>* **[!UICONTROL last]** renvoie l’événement le plus ancien.


**Exemple 3 :**

Nous vérifions si le premier événement Adobe Analytics (le plus récent) avec une valeur non nulle pour l’ID DMA a une valeur égale à 602.

```json
#{ExperiencePlatform.AnalyticsProd_EvarsProps.experienceevent.first(
currentDataPackField.placeContext.geo.dmaID > 0).placeContext.geo.dmaID} == 602
```

**La fonction &quot;at(`<index>`)&quot;**

Le **[!UICONTROL at]** vous permet de référencer un élément spécifique d’une collection selon un index.
L’index 0 est le premier de la collection.

_`<listExpression>`.at(`<index>`)_

**Exemple :**

Cette expression renvoie le deuxième jeton de notification push de la liste.

```json
@{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}
```

Le résultat est &quot;token_2&quot;.

**Autres exemples**

```json
#{ExperiencePlatform.ExperienceEventFieldGroup.experienceevent. all(currentDataPackField._aepgdcdevenablement2.purchase_event.receipt_nbr == "10-337-4016"). 
_aepgdcdevenablement2.purchase_event.productListItems. all(currentDataPackField.SKU == "AB17 1234 1775 19DT B4DR 8HDK 762").name}
```

```json
 #{ExperiencePlatform.ExperienceEventFieldGroup.experienceevent.last(
currentDataPackField.eventType == "commerce.productListAdds").productListItems.last(currentDataPackField.priceTotal >= 150).name}
```
