---
product: adobe campaign
title: intersect
description: En savoir plus sur la fonction intersect
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: e236efa9-91a8-4f08-94c6-45f1e060bb2f
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '79'
ht-degree: 100%

---

# intersection{#intersect}

Renvoie les valeurs communes dans les deux listes dʼentrée. Si lʼune des deux listes est nulle, elle renvoie une liste vide.

## Catégorie

Liste

## Syntaxe de la fonction

`intersect(<parameters>)`

## Paramètres

| Paramètre | Type |
|-----------|------------------|
| list 1 | list |
| list 2 | list |

## Signatures et types renvoyés

`intersect(listString,listString)` : listString
`intersect(listDecimal,listDecimal)` : listDecimal
`intersect(listInteger,listInteger)` : listInteger
`intersect(listDateTime,listDateTime)` : listDateTime
`intersect(listDateTimeOnly,listDateTimeOnly)` : listDateTimeOnly
`intersect(listDateOnly,listDateOnly)` : listDateOnly
`intersect(listDuration,listDuration)` : listDuration
`intersect(listBoolean,listBoolean)` : listBoolean

Renvoie une liste.

## Exemples

```json
intersect(
    ["sports", "news", "documentary"],
    ["sports", "movies", "documentary"]
)
```

Renvoie [« sports », « news »]

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "news", "documentary"]
)
```

Renvoie les éléments communs entre les attributs du profil et la liste de catégories donnée.

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @{myEvent.sport_interests}
)
```

Renvoie les éléments communs entre les attributs du profil et le champ dʼévénement donné.
