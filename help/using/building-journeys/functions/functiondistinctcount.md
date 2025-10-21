---
product: journey optimizer
title: distinctCount
description: En savoir plus sur la fonction distinctCount
feature: Journeys
role: Developer
level: Experienced
keywords: distinctCount, fonction, expression, parcours
exl-id: 8796ba91-5c64-43c2-a444-27ac8b719c86
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 100%

---

# distinctCount{#distinctCount}

Compte le nombre de valeurs différentes en ignorant les valeurs « null ».

## Catégorie

Agrégation

## Syntaxe de la fonction

`distinctCount(<listAny>)`

## Paramètres

| Paramètre | Type | Description |
|-----------|------------------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly, or listObject | Liste à traiter. Pour listObject, il doit s’agir d’une référence de champ. |
| keyAttributeName | Chaîne | Ce paramètre est facultatif et uniquement pour listObject. Si le paramètre n’est pas fourni, un objet est considéré comme dupliqué si tous les attributs ont les mêmes valeurs. Dans le cas contraire, un objet est considéré comme dupliqué si l’attribut donné a la même valeur. |

## Signature et type renvoyé

`distinctCount(<listAny>)`

Renvoie un entier.

`distinctCount(<listObject>)`

`distinctCount(<listObject>,<string>)`

Renvoie une liste d’objets.


## Exemple

`distinctCount([10,2,10,null])`

Renvoie 2.

`distinctCount(@event{my_event.productListItems})`

Renvoie le nombre d’objets strictement distincts dans le tableau d’objets donné (type listObject).

`distinctCount(@event{my_event.productListItems}, "SKU")`

Renvoie le nombre d’objets ayant une valeur d’attribut {} « SKU » distincte.
