---
product: journey optimizer
title: countOnlyNull
description: En savoir plus sur la fonction countOnlyNull
feature: Journeys
role: Developer
level: Experienced
keywords: countOnlyNull, fonction, expression, parcours
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: ht
source-wordcount: '56'
ht-degree: 100%

---

# countOnlyNull {#countOnlyNull}

Compte le nombre de valeurs « null » dans la liste.

Notez que le paramètre `<listObject>` n’est pas pris en charge dans cette fonction.

## Catégorie

Agrégation

## Syntaxe de la fonction

`countOnlyNull(<listAny>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| listToProcess | listString, listBoolean, listInteger, listDecimal, listDuration, listDateTime, listDateTimeOnly, listDateOnly |

## Signature et type renvoyé

`countOnlyNull(<listAny>)`

Renvoie un entier.

## Exemple

`countOnlyNull([10,2,10,null])`

Renvoie 1.
