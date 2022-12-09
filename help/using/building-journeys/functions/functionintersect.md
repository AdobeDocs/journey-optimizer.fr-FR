---
product: journey optimizer
title: intersection
description: En savoir plus sur la fonction intersecte
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: e236efa9-91a8-4f08-94c6-45f1e060bb2f
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '81'
ht-degree: 0%

---

# intersection{#intersect}

Renvoie les valeurs communes des deux listes de saisie. Si l’une des deux listes est nulle, renvoie une liste vide.

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

`intersect(listString,listString)`: listString
`intersect(listDecimal,listDecimal)`: listDecimal
`intersect(listInteger,listInteger)`: listInteger
`intersect(listDateTime,listDateTime)`: listDateTime
`intersect(listDateTimeOnly,listDateTimeOnly)`: listDateTimeOnly
`intersect(listDateOnly,listDateOnly)`: listDateOnly
`intersect(listDuration,listDuration)`: listDuration
`intersect(listBoolean,listBoolean)`: listBoolean

Renvoie une liste.

## Exemples

```json
intersect(
    ["sports", "news", "documentary"],
    ["sports", "movies", "documentary"]
)
```

Renvoie [&quot;sports&quot;, &quot;news&quot;]

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
    ["sports", "news", "documentary"]
)
```

Renvoie les éléments communs entre les attributs de profil et une liste donnée de catégories.

```json
intersect(
    #{ExperienceDataPlatform.profile.interests},
        @{myEvent.sport_interests}
)
```

Renvoie les éléments communs entre les attributs de profil et le champ d’événement donné.
