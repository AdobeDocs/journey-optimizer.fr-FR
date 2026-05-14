---
solution: Journey Optimizer
product: journey optimizer
title: Configurer des parcours
description: Découvrez comment configurer les sources de données, les événements et les actions
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: configuration, parcours, tableau de bord, sources de données, événements, actions
exl-id: c144d44f-031f-4ca2-800e-d3878af400a5
TQID: https://experienceleague.adobe.com/e-4vo3PypkPPOl5pIKWJ1Ecmflj3-CTIAtEV8fjMdk4
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: c2062154-398f-466d-bbc2-4e0d0c3f37a9
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: dd51b532-b93f-4bcf-8dbf-0d007f593aca
  - id: efb19423-4da4-4fd1-88d8-5ee8c71ae766
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 539
ht-degree: 100%

---

# Commencer la configuration des parcours {#configure-journeys}

>[!CONTEXTUALHELP]
>id="ajo_journey_configuration_dashboard"
>title="À propos de la configuration de parcours"
>abstract="Pour envoyer des messages avec des parcours, vous devez configurer des sources de données, des événements et des actions. Les sources de données vous permettent d’établir une connexion avec un système pour récupérer des informations supplémentaires qui seront utilisées pour vos parcours, par exemple dans vos conditions. Les événements vous permettent de déclencher vos parcours lorsqu’un événement est reçu. Les actions personnalisées permettent de se connecter facilement à un système tiers pour envoyer vos messages. Si vous utilisez les fonctionnalités de messagerie intégrées de Journey Optimizer, il n’est pas nécessaire de configurer une action."

Pour envoyer des messages avec des parcours, vous devez configurer des **[!UICONTROL sources de données]**, des **[!UICONTROL événements]** et des **[!UICONTROL actions]**. Les sources de données vous permettent d’établir une connexion avec un système pour récupérer des informations supplémentaires qui seront utilisées pour vos parcours, par exemple dans vos conditions. Les événements vous permettent de déclencher vos parcours lorsqu’un événement est reçu. Les actions personnalisées permettent de se connecter facilement à un système tiers pour envoyer vos messages. Si vous utilisez les fonctionnalités de messagerie intégrées de Journey Optimizer, il n’est pas nécessaire de configurer une action.


![](assets/admin-menu.png)

Vous pouvez également configurer des connexions à des systèmes externes par le biais de sources de données et d’actions personnalisées. Vous pouvez ainsi, par exemple, enrichir vos parcours de données provenant d’un système de réservation externe ou envoyer des messages à l’aide d&#39;un système tiers tel qu’Epsilon ou Facebook. Découvrez comment [intégrer Journey Optimizer à des systèmes externes](external-systems.md).

## Sources de données {#data-sources}

La configuration des sources de données vous permet de définir une connexion à un système afin de récupérer des informations supplémentaires qui seront utilisées dans vos parcours. [En savoir plus](../../using/datasource/about-data-sources.md)

## Événements {#events}

Les événements vous permettent de déclencher vos parcours de manière unitaire pour envoyer des messages, en temps réel, à l’individu progressant dans le parcours.

Dans la configuration des événements, vous configurez les événements attendus dans les parcours. Les données des événements entrants sont normalisées conformément au modèle de données d’expérience Adobe (XDM). Les événements authentifiés et non authentifiés proviennent des API Streaming Ingestion (comme les événements du kit de développement Adobe Mobile SDK). [En savoir plus](../../using/event/about-events.md)

## Actions {#actions}

Les fonctionnalités de message Journey Optimizer sont intégrées : il vous suffit d’ajouter une activité d’action de canal à votre parcours. Si vous utilisez un système tiers pour envoyer vos messages, vous pouvez créer une action personnalisée. [En savoir plus](../../using/action/action.md)

## Parcourir à travers les champs Adobe Experience Platform {#friendly-names-display}

Lors de la définition de la [payload d&#39;événement](../event/about-creating.md#define-the-payload-fields), de la [payload du groupe de champs](../datasource/configure-data-sources.md#define-field-groups) et de la sélection de champs dans l&#39;[éditeur d&#39;expression](../building-journeys/expression/expressionadvanced.md), le nom d&#39;affichage s&#39;affiche en plus du nom du champ. Ces informations sont récupérées à partir de la définition du schéma dans le modèle de données d&#39;expérience.

Si des descripteurs tels que « xdm:alternateDisplayInfo » sont fournis lors de la configuration des schémas, les noms conviviaux remplacent les noms d’affichage. Cela est particulièrement utile lorsque vous utilisez des « eVars » et des champs génériques. Vous pouvez configurer des descripteurs de noms conviviaux via un appel API. Pour plus d&#39;informations, consultez le [guide sur le registre de schéma destiné aux développeurs](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=fr){target="_blank"}.

![](assets/xdm-from-descriptors.png)

Si un nom convivial est disponible, le champ s&#39;affiche sous la forme `<friendly-name>(<name>)`. Si aucun nom convivial n&#39;est disponible, le nom d&#39;affichage s&#39;affiche, par exemple `<display-name>(<name>)`. Si aucun d&#39;eux n&#39;est défini, seul le nom technique du champ s&#39;affiche `<name>`.

>[!NOTE]
>
>Les noms conviviaux ne sont pas récupérés lorsque vous sélectionnez des champs dans une union de schémas.
