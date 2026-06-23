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
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1000
ht-degree: 51%

---

# Fonctions de gestion des collections {#collection-management-functions}


## À propos des fonctions d’interrogation de collections

Le langage d’expression s’accompagne également d’un ensemble de fonctions permettant d’interroger les collections. Ces fonctions sont expliquées ci-dessous.

Dans les exemples suivants, nous utilisons un événement nommé « LobbyBeacon » contenant une collection de jetons de notification push. Les exemples de cette page utilisent la structure de payload d’événement illustrée ci-dessous :

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
>Dans les exemples ci-dessous, cette payload est référencée à l’aide de `@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens}` où « LobbyBeacon » est le nom de l’événement et le reste du chemin d’accès correspond à la structure affichée ci-dessus.

## La fonction all(`<condition>`)

La fonction **[!UICONTROL all]** permet de définir un filtre sur une collection donnée en utilisant une expression booléenne.

```json
<listExpression>.all(<condition>)
```

**Exemple conceptuel :** parmi toutes les personnes utilisant l’application, vous pouvez extraire celles qui utilisent IOS 13 (expression booléenne « app used == IOS 13 »). Le résultat de cette fonction est une liste filtrée contenant les éléments qui correspondent à l’expression booléenne (exemple : utilisateur 1 de l’application, utilisateur 34 de l’application, utilisateur 432 de l’application).

Dans une activité Condition de source de données, vous pouvez vérifier si le résultat de la fonction **[!UICONTROL all]** est nul ou non. Vous pouvez également combiner cette fonction **[!UICONTROL all]** à d’autres fonctions, telles que **[!UICONTROL count]**. Pour plus d’informations, voir [Activité Condition de source de données](../conditions.md#data_source_condition).

**Exemples de code utilisant la payload LobbyBeacon :**

Les exemples ci-dessous utilisent la payload d’événement affichée en haut de cette page.


>[!CAUTION]
>
>L’utilisation d’événements d’expérience dans des expressions/conditions de parcours n’est pas prise en charge. Si votre cas d’utilisation nécessite l’utilisation d’événements d’expérience, envisagez d’utiliser d’autres méthodes. [En savoir plus](../exp-event-lookup.md)

### Exemple 1

Nous voulons vérifier si un utilisateur ou une utilisatrice a installé une version spécifique d’une application. Pour ce faire, nous récupérons tous les jetons de notification push associés aux applications mobiles dont la version est 1.0. Ensuite, nous exécutons une condition avec la fonction **[!UICONTROL count]** pour vérifier que la liste de jetons renvoyée contient au moins un élément.

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

La fonction **[!UICONTROL at]** permet de référencer un élément spécifique dans une collection en fonction d&#39;un index.
Index 0 est le premier index de la collection.

_`<listExpression>`.at(`<index>`)_

### Exemple

Cette expression renvoie le deuxième jeton de notification push de la liste.


```json
@event{LobbyBeacon._experience.campaign.message.profile.pushNotificationTokens.at(1).token}
```

Le résultat est `token_2`.

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page présente les fonctions de gestion des collections `all()`, `first()`, `last()` et `at()` utilisées dans l’éditeur d’expression avancé de Parcours, illustré par des exemples de payload de jeton de notification push.

**Intentions:**

* Filtrer une collection de champs d’événement ou de source de données à l’aide d’une condition booléenne avec `all(<condition>)`
* Comptabiliser les éléments de collection filtrés ou non filtrés à l’aide de `count()` combinés avec des fonctions de collection
* Récupérez le premier ou le dernier élément correspondant d’une collection à l’aide de `first()` ou `last()`
* Accéder à un élément de collection à un index spécifique basé sur zéro à l’aide de `at(<index>)`
* Identifiez la variable de boucle (`currentEventField`, `currentDataPackField`, `currentActionField`) qui s’applique à chaque contexte de collection

**Glossaire:**

* **all(condition)** : filtre une collection et renvoie tous les éléments correspondant à l’expression booléenne donnée *(spécifique au produit)*
* **first(condition)** : renvoie le premier élément (le plus récent pour les événements d&#39;expérience) d&#39;une collection correspondant à la condition *(spécifique au produit)*
* **last(condition)** : renvoie le dernier élément (le plus ancien pour les événements d’expérience) d’une collection correspondant à la condition *(spécifique au produit)*
* **at(index)** : renvoie l’élément à l’index zéro spécifié d’une collection *(spécifique au produit)*
* **currentEventField** : variable de boucle disponible uniquement lors de l’itération sur des collections d’événements *(spécifiques au produit)*
* **currentDataPackField** : variable de boucle disponible uniquement lors de l’itération sur des collections de sources de données *(spécifiques au produit)*
* **currentActionField** : variable de boucle disponible uniquement lors de l’itération sur des collections de réponses d’action personnalisée *(spécifiques au produit)*

**Mécanismes de sécurisation :**

* L’utilisation d’événements d’expérience dans des expressions/conditions de parcours n’est pas prise en charge. Envisagez d’autres méthodes telles que les attributs calculés
* `currentEventField`, `currentDataPackField` et `currentActionField` ne sont disponibles qu’à l’intérieur de leurs contextes de collection respectifs
* La fonction `all` n’est pas nécessaire pour compter les éléments de collection ; `count()` peut être appliquée directement au chemin du champ
* Lorsque `all()` est appelé avec une condition vide, tous les éléments de la collection sont renvoyés

**Terminologie:**

* Nom canonique : Fonctions de gestion des collections — Acronyme : none — variantes : fonctions de collection, fonctions de collection de requêtes
* Synonymes : « all() » = « fonction de filtre de collection » ; « at() » = « accesseur d’index »
* Ne pas confondre : `first()` (événement d’expérience le plus récent) ≠ premier élément inséré dans les listes générales

**FAQ:**

* **Q : Quelle est la différence entre `all()` avec une condition vide et `all()` avec une condition ?** — Un `all()` vide renvoie chaque élément ; un `all()` basé sur des conditions renvoie uniquement les éléments correspondant à cette expression booléenne.
* **Q : Comment compter les jetons de notification push sans utiliser `all()` ?** — Appelez `count()` directement sur le chemin du champ de jeton, par exemple `count(@event{LobbyBeacon...pushNotificationTokens.token})`.
* **Q : Quelle variable dois-je utiliser pour référencer l’élément actif lors de la boucle sur une collection de source de données ?** — Utilisez des `currentDataPackField` dans `all()`, `first()` ou `last()` sur les collections de sources de données.
* **Q : Comment puis-je obtenir le deuxième élément d&#39;une collection ?** — Utilisez `at(1)` car index 0 est le premier élément.
* **Q : Pourquoi renvoie-`last()` l’événement d’expérience le plus ancien ?** — Les événements d’expérience sont stockés dans l’ordre chronologique inverse, de sorte que la dernière position de la collection correspond à l’événement le plus ancien.

+++
