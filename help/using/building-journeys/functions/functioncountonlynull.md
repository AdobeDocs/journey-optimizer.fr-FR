---
product: journey optimizer
title: countOnlyNull
description: En savoir plus sur la fonction countOnlyNull
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: countOnlyNull, fonction, expression, parcours
exl-id: d06fc594-33dd-48ce-8c62-2f2892a867da
source-git-commit: 1d30c6ae49fd0cac0559eb42a629b59708157f7d
workflow-type: ht
source-wordcount: '52'
ht-degree: 100%

---

# countOnlyNull {#countOnlyNull}

Compte le nombre de valeurs « null » dans la liste.

## Catégorie

Agrégation

## Syntaxe de la fonction

`countOnlyNull(<listAny>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| Liste | listString |
| Liste | listBoolean |
| Liste | listInteger |
| Liste | listDecimal |
| Liste | listDuration |
| Liste | listDateTime |
| Liste | listDateTimeOnly |
| Liste | listDateOnly |

## Signature et type renvoyé

`countOnlyNull(<listAny>)`

Renvoie un entier.

## Exemple

`countOnlyNull([10,2,10,null])`

Renvoie 1.
