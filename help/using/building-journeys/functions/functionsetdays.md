---
product: journey optimizer
title: setDays
description: En savoir plus sur la fonction setDays
feature: Journeys
role: Developer
level: Experienced
keywords: setDays, fonction, expression, parcours
exl-id: c2757e41-8206-44f7-9dbb-1fa79c0ba6e6
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: tm+mt
source-wordcount: '80'
ht-degree: 100%

---

# setDays {#setDays}

Définit le jour d’une date ou d’une date sans prise en compte du fuseau horaire. Par exemple, si vous voulez attendre jusqu’à un certain jour du mois, vous pouvez forcer le jour.

## Catégorie

Date

## Syntaxe de la fonction

`setDays(<parameter>)`

## Paramètres

| Paramètre | Type |
|--- |--- |
| date et heure | dateTime |
| date et heure sans prise en compte du fuseau horaire | dateTimeOnly |
|  jours | Entier |

## Signatures et type renvoyé

`setDays(<dateTime>,<days>)`

Renvoie une date et une heure.

`setDays(<dateTimeOnly>,<days>)`

Renvoie une date et une heure sans prendre en compte le fuseau horaire.

## Exemples

`setDays(toDateTime('2023-12-12T01:11:00Z'), 25)`

Renvoie 2023-12-25T01:11:00Z.

`setDays(toDateTimeOnly(@event{MyEvent.registrationDate}), 1)`
