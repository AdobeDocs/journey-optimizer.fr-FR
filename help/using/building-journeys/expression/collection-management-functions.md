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
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: ht
source-wordcount: '481'
ht-degree: 100%

---

# Fonctions de gestion des collections {#collection-management-functions}


## À propos des fonctions d’interrogation de collections

Le langage d’expression s’accompagne également d’un ensemble de fonctions permettant d’interroger les collections. Ces fonctions sont expliquées ci-dessous.

Dans les exemples suivants, nous allons utiliser la payload d’événement contenant une collection :

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

## La fonction all(`<condition>`)

La fonction **[!UICONTROL all]** permet de définir un filtre sur une collection donnée en utilisant une expression booléenne.

```json
<listExpression>.all(<condition>)
```

Par exemple, parmi tous les personnes utilisant l’application, vous pouvez extraire celles qui utilisent IOS 13 (expression booléenne « app used == IOS 13 »). Le résultat de cette fonction est une liste filtrée contenant les éléments qui correspondent à l’expression booléenne (exemple : utilisateur 1 de l’application, utilisateur 34 de l’application, utilisateur 432 de l’application).

Dans une activité Condition de source de données, vous pouvez vérifier si le résultat de la fonction **[!UICONTROL all]** est nul ou non. Vous pouvez également combiner cette fonction **[!UICONTROL all]** à d’autres fonctions, telles que **[!UICONTROL count]**. Pour plus d’informations, voir [Activité Condition de source de données](../condition-activity.md#data_source_condition).


>[!CAUTION]
>
>L’utilisation d’événements d’expérience dans des expressions/conditions de parcours n’est pas prise en charge. Si votre cas d’utilisation nécessite l’utilisation d’événements d’expérience, envisagez d’utiliser d’autres méthodes. [En savoir plus](../exp-event-lookup.md)

### Exemple 1

Nous voulons vérifier si un utilisateur ou une utilisatrice a installé une version spécifique d’une application. Pour ce faire, nous récupérons tous les jetons de notification push associés aux applications mobiles dont la version est égale à 1.0. Ensuite, nous exécutons une condition avec la fonction **[!UICONTROL count]** pour vérifier que la liste de jetons renvoyée contient au moins un élément. 

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all(currentEventField.application.version == "1.0").token}) > 0
```

Le résultat est true.

### Exemple 2

Ici, nous utilisons la fonction **[!UICONTROL count]** pour vérifier s’il existe des jetons de notification push dans la collection.

```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.all().token}) > 0
```


Le résultat est true.


```json
count(@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.token})
```

Le résultat de l’expression est **3**.


>[!NOTE]
>
>* Lorsque la condition de filtrage de la fonction **all()** est vide, le filtre renvoie tous les éléments de la liste. **Cependant, pour comptabiliser le nombre d’éléments d’une collection, la fonction all n’est pas obligatoire.**
>
>* `currentEventField` n’est disponible que lors de la manipulation de collections d’événements, `currentDataPackField` lors de la manipulation de collections de sources de données et `currentActionField` lors de la manipulation de collections de réponses d’actions personnalisées.
>
>  Lors du traitement de collections avec `all`, `first` et `last`, une boucle est exécutée sur chaque élément de la collection, un par un. `currentEventField`, `currentDataPackField` et `currentActionField` correspondent à l’élément exécuté en boucle.


## Fonctions first(`<condition>`) et last(`<condition>`)

Les fonctions **[!UICONTROL first]** et **[!UICONTROL last]** activent également la définition d’un filtre sur la collection, tout en renvoyant le premier/dernier élément de la liste qui correspond au filtre.

_`<listExpression>.first(<condition>)`_

_`<listExpression>.last(<condition>)`_

### Exemple 1

Cette expression renvoie le premier jeton de notification push associé aux applications mobiles dont la version est égale à 1.0. 


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.first(currentEventField.application.version == "1.0").token}
```

Le résultat est `token_1`.

### Exemple 2

Cette expression renvoie le dernier jeton de notification push associé aux applications mobiles dont la version est égale à 1.0. 


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.last(currentEventField.application.version == "1.0").token}
```

Le résultat est `token_2`.

## La fonction at(`<index>`)

La fonction **[!UICONTROL at]** vous permet de référencer un élément spécifique d’une collection conformément à un index.
L’index 0 est le premier de la collection.

_`<listExpression>`.at(`<index>`)_

### Exemple

Cette expression renvoie le deuxième jeton de notification push de la liste.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}
```

Le résultat est `token_2`.