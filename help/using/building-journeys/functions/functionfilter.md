---
product: journey optimizer
title: filter
description: En savoir plus sur la fonction filter
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: filtre, fonction, expression, parcours
exl-id: 05e3d2ba-1a27-4f27-88cc-3d83eb3b14af
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 96%

---

# filter{#filter}

Renvoie une valeur listObject avec les objets dont lʼattribut clé correspond à lʼune des valeurs clés données.

>[!NOTE]
>
>Si la liste cible est un listObject, cette fonction ne peut être utilisée que dans les expressions d’action personnalisées.

## Catégorie

Liste

## Syntaxe de la fonction

`filter(<parameters>)`

## Paramètres

| Paramètre | Type | Description |
|-----------|------------------|------------------|
| listToFilter | listObject | liste dʼobjects à filtrer. Il doit être une référence de champ. |
| keyAttributeName | chaîne | nom de lʼattribut dans les objets de la liste donnée, utilisé comme clé pour le filtrage |
| keyValueList | list | tableau de valeurs clés pour le filtrage |

## Signatures et types renvoyés

`filter(listObject, string, listString)`

`filter(listObject, string, listInteger)`

`filter(listObject, string, listDecimal)`

`filter(listObject, string, listDateTime)`

`filter(listObject, string, listDateTimeOnly)`

`filter(listObject, string, listDateOnly)`

`filter(listObject, string, listDuration)`

`filter(listObject, string, listBoolean)`

Renvoie une valeur listObject.

## Exemples

Voici un exemple dʼune payload transmise dans un événement entrant « myevent » :

```json
"productListItems": [{
   "id": "product1",
   "name": "the product 1",
   "price": 20
},{
   "id": "product2",
   "name": "the product 2",
   "price": 30
},{
   "id": "product3",
   "name": "the product 3",
   "price": 50
}]
```

Vous pouvez utiliser lʼexpression suivante :

```json
filter(
 @{myevent.productListItems},
 "id", 
 ["product2", "product3", "product4"]
)
```

Renvoie une valeur listObject contenant les deux objets avec « product2 » et « product3 » comme id.
