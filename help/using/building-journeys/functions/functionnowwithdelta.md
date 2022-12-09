---
product: journey optimizer
title: nowWithDelta
description: En savoir plus sur la fonction nowWithDelta
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: cb1eb221-8532-4637-ac6c-8e058463ac94
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '110'
ht-degree: 0%

---

# nowWithDelta {#nowWithDelta}

Renvoie la date et l’heure actuelles, y compris un décalage. Si un identifiant de fuseau horaire est spécifié, le décalage de fuseau horaire est appliqué. Pour plus d’informations sur les types de données, reportez-vous à la section [cette page](../expression/data-types.md).

## Catégorie

Date

## Syntaxe de la fonction

`nowWithDelta(<parameters>)`

## Paramètres

| Paramètre | Description |
|--- |--- |
| delta | valeur entière positive ou négative |
| partie date | années, mois, jours, heures, minutes ou secondes sous forme de chaîne |
| identifiant de fuseau horaire | représentation sous forme de chaîne de la valeur du fuseau horaire. Pour plus d’informations, voir [Types de données](../expression/data-types.md). L’identifiant de fuseau horaire doit être une constante sous forme de chaîne. Il ne peut pas s’agir d’une référence de champ ou d’une expression. |

## Signatures et type renvoyé

`nowWithDelta(<delta>,<date part>`

`nowWithDelta(<delta>,<date part>,"<timeZone id>")`

Renvoie une valeur dateTime.

## Exemples

`nowWithDelta(-2, "hours")`

`nowWithDelta(-2, "hours", "Europe/Paris")`

Renvoie une valeur dateTime il y a exactement 2 heures.
