---
product: journey optimizer
title: count
description: En savoir plus sur la fonction count
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: count, fonction, expression, parcours
exl-id: 6980c1ec-3afd-4fc9-ae10-76bcf7364a04
source-git-commit: 2f47209ad2a5e5b5d26f01949f5e9ade63c2581f
workflow-type: tm+mt
source-wordcount: '90'
ht-degree: 100%

---

# count {#count}

Compte les éléments de la liste sans tenir compte des valeurs « null ».

## Catégorie

Agrégation

## Syntaxe de la fonction

`count(<listAny>)`

`count(<listObject>)`

## Paramètres

| Paramètre | Type | Description |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly, or listObject | Liste à traiter. Pour listObject, il doit s’agir d’une référence de champ. Un listObject ne peut pas contenir d’objet null. |

## Signatures et type renvoyé

`count(<listAny>)`

Renvoie un entier.

## Exemple

`count([10,2,10,null])`

Renvoie 3.

`count(@event{my_event.productListItems})`

Renvoie le nombre d’objets dans le tableau d’objets donné (type listObject). Remarque : un objet listObject ne peut pas contenir d’objet null.
