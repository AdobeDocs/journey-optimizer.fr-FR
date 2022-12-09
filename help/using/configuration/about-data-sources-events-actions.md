---
solution: Journey Optimizer
product: journey optimizer
title: Configuration des parcours
description: Découvrez comment configurer les sources de données, les événements et les actions
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: c144d44f-031f-4ca2-800e-d3878af400a5
source-git-commit: f04454860ebe597d3306e62b58de5f32e08342ee
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 0%

---

# Configuration des parcours {#configure-journeys}

>[!CONTEXTUALHELP]
>id="ajo_journey_configuration_dashboard"
>title="A propos de la configuration d’un parcours"
>abstract="Pour envoyer des messages avec des parcours, vous devez configurer les sources de données, les événements et les actions. Les sources de données vous permettent de définir une connexion à un système afin de récupérer des informations supplémentaires qui seront utilisées dans vos parcours, par exemple dans vos conditions. Les événements vous permettent de déclencher vos parcours lorsqu’un événement est reçu. Les actions personnalisées vous permettent de vous connecter à un système tiers pour envoyer vos messages. Si vous utilisez les fonctionnalités de message intégré de Journey Optimizer, il n’est pas nécessaire de configurer une action."

Pour envoyer des messages avec des parcours, vous devez configurer **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** et **[!UICONTROL Actions]**.

![](assets/admin-menu.png)

## Sources de données {#data-sources}

La configuration de la source de données vous permet de définir une connexion à un système afin de récupérer des informations supplémentaires qui seront utilisées dans vos parcours. [En savoir plus](../../using/datasource/about-data-sources.md)

## Événements {#events}

Les événements vous permettent de déclencher unitairement vos parcours pour envoyer des messages, en temps réel, à l’individu qui participe au parcours.

Dans la configuration des événements, vous configurez les événements prévus dans les parcours. Les données des événements entrants sont normalisées conformément au modèle de données d’expérience Adobe (XDM). Les événements proviennent des API d’ingestion en flux continu pour les événements authentifiés et non authentifiés (tels que les événements du SDK Adobe Mobile). [En savoir plus](../../using/event/about-events.md)

## Actions {#actions}

Les fonctionnalités de message Journey Optimizer sont intégrées : il vous suffit d’ajouter une activité d’action de canal à votre parcours. Si vous utilisez un système tiers pour envoyer vos messages, vous pouvez créer une action personnalisée. [En savoir plus](../../using/action/action.md)

## Parcourir les champs Adobe Experience Platform {#friendly-names-display}

Lors de la définition [payload d’événement](../event/about-creating.md#define-the-payload-fields), [payload du groupe de champs](../datasource/configure-data-sources.md#define-field-groups) et de sélectionner les champs du [éditeur d&#39;expression](../building-journeys/expression/expressionadvanced.md), le nom d’affichage s’affiche en plus du nom du champ. Ces informations sont récupérées à partir de la définition de schéma dans le modèle de données d’expérience.

Si des descripteurs tels que &quot;xdm:alternateDisplayInfo&quot; sont fournis lors de la configuration des schémas, les noms conviviaux remplacent les noms d’affichage. Elle est particulièrement utile lorsque vous utilisez des &quot;eVars&quot; et des champs génériques. Vous pouvez configurer des descripteurs de nom conviviaux via un appel API. Pour plus d’informations, voir [Guide de développement du registre des schémas](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html){target=&quot;_blank&quot;}.

![](assets/xdm-from-descriptors.png)

Si un nom convivial est disponible, le champ s’affiche sous la forme `<friendly-name>(<name>)`. Si aucun nom convivial n’est disponible, le nom d’affichage s’affiche, par exemple `<display-name>(<name>)`. Si aucun d’eux n’est défini, seul le nom technique du champ s’affiche. `<name>`.

>[!NOTE]
>
>Les noms conviviaux ne sont pas récupérés lorsque vous sélectionnez des champs à partir d’une union de schémas.
