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
TQID: https://experienceleague.adobe.com/dpQ6PEm-afX4PZuWSPrpAWDH7yBhUKZHZRF134VehAg
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a9f73820-6899-47c2-a597-3fec28ab756a
  - id: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2:
  - id: d145add9-d5b9-481b-aa8a-e15e6bb7f813
  - id: a7289281-9ae4-47b1-b8cf-4028b98af776
  - id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 130
ht-degree: 100%

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

## nom {#name-field}

Nom du parcours.

Type : Chaîne

>[!NOTE]
>
>Le nom du parcours est utilisé pour lier les données d’exécution du parcours aux jeux de données de rapports. Si vous renommez un parcours, veillez à ce que le nouveau nom corresponde au nom figurant dans votre jeu de données de rapports afin de garantir l’exactitude des rapports. Une incohérence peut empêcher les données de rapport de s’afficher comme prévu. En savoir plus sur la [résolution des problèmes liés aux données de rapports manquantes](../building-journeys/report-journey.md#troubleshooting-missing-data).

## description {#description-field}

Description du parcours.

Type : chaîne

## version {#version-field}

Version, représentée sous la forme `major`.`minor`

Type : chaîne
