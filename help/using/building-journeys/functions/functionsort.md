---
product: journey optimizer
title: sort
description: En savoir plus sur la fonction sort
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: sort, fonction, expression, parcours
exl-id: 607e1424-4165-48ae-b896-cce2d18f7dcc
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: ht
source-wordcount: '152'
ht-degree: 100%

---

# sort {#sort}

Trie une liste de valeurs ou d’objets dans l’ordre naturel.

>[!NOTE]
>
>Si la liste cible est un listObject, cette fonction ne peut être utilisée que dans les expressions d’action personnalisées.

## Catégorie

Liste

## Syntaxe de la fonction

`sort(<parameters>)`

## Paramètres

| Paramètre | Type | Description |
|-----------|------------------|------------------|
| listToSort | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly, or listObject | Liste à trier. Pour listObject, il doit s’agir d’une référence de champ. |
| keyAttributeName | chaîne | Ce paramètre est uniquement destiné à listObject. Le nom de lʼattribut dans les objets de la liste donnée, utilisé comme clé pour le tri. |
| sortingOrder | booléen | ascendant (true) ou descendant (false) |

## Signature et type renvoyé

`sort(<listInteger>,<boolean>)`

Renvoie une liste de nombres entiers.

`sort(<listDecimal>,<boolean>)`

Renvoie une liste de nombres décimaux.

`sort(<listString>,<boolean>)`

Renvoie une liste de chaînes.

`sort(<listDateTimeOnly>,<boolean>)`

Renvoie une liste de dates et heures sans tenir compte du fuseau horaire.

`sort(<listDateTime>,<boolean>)`

Renvoie une liste de dates et heures.

`sort(<listDateOnly>,<boolean>)`

Renvoie une liste de dates.

`sort(<listBoolean>,<boolean>)`

Renvoie une liste de valeurs booléennes.

`sort(<listObject>,<string>,<boolean>)`

Renvoie une liste d’objets.

## Exemple

`sort(["A", "C", "B"], true)`

Renvoie `["A","B","C"]`.

`sort([1, 3, 2], false)`

Renvoie `[3, 2, 1]`.

