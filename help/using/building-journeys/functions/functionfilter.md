---
product: journey optimizer
title: filter
description: En savoir plus sur la fonction filter
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 05e3d2ba-1a27-4f27-88cc-3d83eb3b14af
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: ht
source-wordcount: '109'
ht-degree: 100%

---

# filter{#filter}

Renvoie une valeur listObject avec les objets dont lʼattribut clé correspond à lʼune des valeurs clés données.

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
