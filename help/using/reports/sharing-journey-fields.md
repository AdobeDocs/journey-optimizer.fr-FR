---
solution: Journey Optimizer
product: journey optimizer
title: Champs du parcours
description: Champs du parcours
feature: Journeys, Reporting
topic: Content Management
role: Developer, Admin
level: Experienced
exl-id: 177b4a97-c757-40ca-a190-fbd88169e5e2
source-git-commit: 6961a07e2874f9beb76a9beaebb29997d114d8e7
workflow-type: tm+mt
source-wordcount: '130'
ht-degree: 60%

---

# Champs du parcours {#sharing-journey-fields}

Ce groupe de champs est utilisé dans le schéma du **parcours** (en relation avec **journeyStepEvent**). Il contient les champs répertoriés ci-dessous.


>[!NOTE]
>
>Pour plus d’informations sur les attributs des propriétés de parcours, consultez [cette section](../building-journeys/expression/journey-properties.md#journey-properties-fields).


## journeyID {#journeyid-field}

Identifiant du parcours principal.

Type : chaîne

## journeyVersionID {#journeyversionid-field}

Identifiant de la version du parcours. Cet identifiant représente l’identité d’un parcours.

Type : chaîne

## name {#name-field}

Nom du parcours.

Type : chaîne

>[!NOTE]
>
>Le nom du parcours est utilisé pour lier les données d’exécution du parcours aux jeux de données de rapports. Si vous renommez un parcours, assurez-vous que le nouveau nom correspond au nom figurant dans votre jeu de données de rapports afin de créer des rapports précis. Une incohérence peut entraîner l’affichage inattendu des données de rapport. En savoir plus sur [résolution des problèmes liés aux données de rapports manquantes](../building-journeys/report-journey.md#troubleshooting-missing-data).

## description {#description-field}

Description du parcours.

Type : chaîne

## version {#version-field}

Version, représentée sous la forme `major`.`minor`

Type : chaîne
