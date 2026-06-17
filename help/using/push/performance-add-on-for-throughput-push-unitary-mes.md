---
solution: Journey Optimizer
product: journey optimizer
title: Module complémentaire Performances pour le débit - (push) unitaire - Diffusion des messages
description: Découvrez comment configurer et utiliser le module complémentaire Performances pour débit - (push) unitaire - Diffusion des messages dans Adobe Journey Optimizer.
feature: Push
topic: Content Management
role: User
level: Intermediate
exl-id: 2d0677ad-41c8-4299-a7c8-0e4f8a1716f7
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: c96d2aa5-76a2-443d-8d23-5de95577c909
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b6b77c26-2a48-4a62-9ceb-5ae67f4dfde5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
source-git-commit: 4aebdb06094628cfe7393c7f7b41e5fe0ee9df13
workflow-type: tm+mt
source-wordcount: 252
ht-degree: 4%

---


# Module complémentaire Performances pour le débit - (push) unitaire - Diffusion des messages {#performance-add-on-for-throughput-push-unitary-mes}

>[!AVAILABILITY]
>
>Cette fonctionnalité est disponible depuis **AJO26.7** (2026-07-27).

## Vue d’ensemble {#overview}

Adobe Journey Optimizer présente le **module complémentaire de performance pour débit - (push) unitaire - Diffusion des messages**, qui permet aux entreprises de fournir des expériences client plus pertinentes et personnalisées sur les canaux push.

Cette page explique comment configurer et utiliser cette fonctionnalité dans vos campagnes et parcours.

## Conditions préalables {#prerequisites}

Avant de commencer :

* Vous avez accès à Adobe Journey Optimizer avec les autorisations **push** requises.
* Une surface de canal push est configurée. Voir [Configuration du canal push](../configuration/channel-surfaces.md).

## Fonctionnement {#how-it-works}

Module complémentaire Performances pour le débit - (push) unitaire - La diffusion des messages s’intègre directement au moteur d’exécution d’AJO. Lorsqu’un profil atteint une action push dans un parcours ou une campagne, la fonctionnalité applique les paramètres configurés au moment de l’envoi.

Fonctionnalités principales :

* **Personnalisation au niveau du profil** — Les paramètres s’adaptent par destinataire à l’aide d’attributs de profil et de contexte.
* **Prise en charge des Parcours et des campagnes** — fonctionne à la fois dans des parcours orchestrés et dans des campagnes ponctuelles.
* **Mesures en temps réel** — les résultats apparaissent dans les [rapports push](../reports/push-report.md).

## Configurer le module complémentaire de performance pour le débit {#configure}

1. Dans le menu de gauche d’AJO, accédez à **Canaux** > **Configurations push**.
1. Sélectionnez ou créez une configuration de canal.
1. Dans la section **Module complémentaire de performance pour**, activez la fonctionnalité.
1. Définissez les paramètres requis.
1. Cliquez sur **Enregistrer**.

>[!NOTE]
>
>Les modifications de configuration s’appliquent aux nouvelles exécutions de parcours. Les parcours en cours ne sont pas affectés.

## Rubriques connexes {#related-topics}

* [Prise en main des notifications push](get-started-push.md)
* [Créer une notification push](create-push.md)
* [Notes De Mise À Jour D’AJO 26.7](../rn/release-notes.md)
