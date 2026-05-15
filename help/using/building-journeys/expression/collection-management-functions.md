---
solution: Journey Optimizer
product: journey optimizer
title: Fonctions de gestion des collections
description: En savoir plus sur les types de données dans les fonctions de gestion des collections
feature: Journeys
role: Developer
level: Experienced
keywords: requête, collections, fonctions, payload, parcours
exl-id: 09b38179-9ace-4921-985b-ddd17eb64681
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sNFI7l-UMGmRV2wRcvYa56tILLoWFxXeG3N5txgrUiw
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 545
ht-degree: 0%

---

# Fonctions de gestion des collections {#collection-management-functions}


## À propos des fonctions de collecte de requêtes

Le langage d’expression introduit également un ensemble de fonctions pour interroger des collections. Ces fonctions sont expliquées ci-dessous.

Dans les exemples suivants, nous utilisons un événement nommé « LobbyBeacon » contenant une collection de jetons de notification push. Les exemples de cette page utilisent la structure de payload d&#39;événement illustrée ci-dessous :

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

>[!NOTE]
>
>Dans les exemples ci-dessous, cette payload est référencée à l’aide de `@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens}` où « LobbyBeacon » est le nom de l’événement et le reste du chemin d’accès correspond à la structure affichée ci-dessus.

## La fonction all(`<condition>`)

La fonction **[!UICONTROL all]** permet de définir un filtre sur une collection donnée en utilisant une expression booléenne.

```json
<listExpression>.all(<condition>)
```

**Exemple conceptuel :** parmi tous les utilisateurs de l’application, vous pouvez obtenir ceux qui utilisent IOS 13 (expression booléenne « application utilisée == IOS 13 »). Le résultat de cette fonction est la liste filtrée contenant les éléments correspondant à l’expression booléenne (exemple : utilisateur de l’application 1, utilisateur de l’application 34, utilisateur de l’application 432).

Dans une activité Condition de Source de données , vous pouvez vérifier si le résultat de la fonction **[!UICONTROL all]** est nul ou non. Vous pouvez également combiner cette fonction **[!UICONTROL all]** avec d’autres fonctions telles que **[!UICONTROL count]**. Pour plus d’informations, voir [Activité de condition de Source de données](../conditions.md#data_source_condition).

**Exemples de code utilisant la payload LobbyBeacon :**

Les exemples ci-dessous utilisent la payload d’événement affichée en haut de cette page.


>[!CAUTION]
>
>L’utilisation d’événements d’expérience dans des expressions/conditions de parcours n’est pas prise en charge. Si votre cas d’utilisation nécessite l’utilisation d’événements d’expérience, envisagez d’autres méthodes. [ En savoir plus ](../exp-event-lookup.md)

### Exemple 1

Nous voulons vérifier si un utilisateur a installé une version spécifique d’une application. Pour ce faire, nous obtenons tous les jetons de notification push associés aux applications mobiles dont la version est égale à 1.0. Ensuite, nous exécutons une condition avec la fonction **[!UICONTROL count]** pour vérifier que la liste de jetons renvoyée contient au moins un élément.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all(currentEventField.application.version == "1.0").token}) > 0
```

Le résultat est vrai.

### Exemple 2

Ici, nous utilisons la fonction **[!UICONTROL count]** pour vérifier s’il existe des jetons de notification push dans la collection.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) > 0
```


Le résultat est vrai.


```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.token})
```

Le résultat de l’expression est **3**.


>[!NOTE]
>
>* Lorsque la condition de filtrage de la fonction **all()** est vide, le filtre renvoie tous les éléments de la liste. **Toutefois, pour compter le nombre d’éléments d’une collection, la fonction all n’est pas obligatoire.**
>
>* `currentEventField` n’est disponible que lors de la manipulation de collections d’événements, `currentDataPackField` lors de la manipulation de collections de sources de données et `currentActionField` lors de la manipulation de collections de réponses d’actions personnalisées.
>
>  Lors du traitement des collections avec `all`, `first` et `last`, nous effectuons une boucle sur chaque élément de la collection, un par un. `currentEventField`, `currentDataPackField` et `currentActionField` correspondent à l&#39;élément en boucle.


## Fonctions first(`<condition>`) et last(`<condition>`)

Les fonctions **[!UICONTROL first]** et **[!UICONTROL last]** permettent également de définir un filtre sur la collection en renvoyant le premier/dernier élément de la liste qui répond au filtre.

_`<listExpression>.first(<condition>)`_

_`<listExpression>.last(<condition>)`_

### Exemple 1

Cette expression renvoie le premier jeton de notification push associé aux applications mobiles dont la version est 1.0.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.first(currentEventField.application.version == "1.0").token}
```

Le résultat est `token_1`.

### Exemple 2

Cette expression renvoie le dernier jeton de notification push associé aux applications mobiles dont la version est 1.0.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.last(currentEventField.application.version == "1.0").token}
```

Le résultat est `token_2`.

## La fonction at(`<index>`)

La fonction **[!UICONTROL at]** permet de référencer un élément spécifique dans une collection en fonction d&#39;un index.
Index 0 est le premier index de la collection.

_`<listExpression>`.at(`<index>`)_

### Exemple

Cette expression renvoie le deuxième jeton de notification push de la liste.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}
```

Le résultat est `token_2`.