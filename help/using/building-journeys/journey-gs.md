---
solution: Journey Optimizer
product: journey optimizer
title: Créer votre premier parcours
description: Étapes clés de création de votre premier parcours avec Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: parcours, premier, commencer, démarrage rapide, audience, événement, action
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: 99099cb6b705cb5a7b97652154c42f0565fdfdb9
workflow-type: tm+mt
source-wordcount: '716'
ht-degree: 71%

---

# Créer votre premier parcours {#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="Créer des parcours"
>abstract="Utilisez **Adobe Journey Optimizer** pour créer des cas d’utilisation d’orchestration en temps réel à l’aide de données contextuelles stockées dans des événements ou des sources de données."

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Parcours"
>abstract="Concevoir des parcours clients pour offrir des expériences contextuelles personnalisées. Journey Optimizer vous permet de créer des cas d’utilisation d’orchestration en temps réel avec des données contextuelles stockées dans des événements ou des sources de données. L’onglet **Vue d’ensemble** affiche un tableau de bord avec les mesures clés liées à vos parcours : L’onglet **Parcourir** affiche la liste des parcours existants."


Adobe Journey Optimizer comprend une zone de travail d’orchestration omnicanal qui permet aux spécialistes du marketing d’harmoniser la portée marketing avec l’engagement client individuel. L’interface utilisateur vous permet de faire glisser facilement des activités de la palette vers la zone de travail pour créer votre parcours.

![](assets/journey38.png)

Suivez les étapes principales de création dʼun parcours décrites ci-après :

![](assets/journey-creation-process.png)

➡️ [Découvrir cette fonctionnalité en vidéo](#video)

L’interface utilisateur du parcours est présentée dans [cette page](journey-ui.md).


## Conditions préalables {#start-prerequisites}

Pour envoyer des messages avec des parcours, les prérequis suivants sont nécessaires :

1. **Configurer un événement** : si vous souhaitez déclencher vos parcours une fois qu&#39;un événement est reçu, vous devez configurer un événement. Vous devez définir les informations attendues et comment les traiter. Cette étape est effectuée par un **utilisateur technique**. [En savoir plus](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **Créer une audience** : votre parcours peut également écouter les audiences Adobe Experience Platform afin d’envoyer des messages par lots à un ensemble de profils spécifié. Pour cela, vous devez créer des audiences. [En savoir plus](../audience/about-audiences.md).

   ![](assets/segment2.png)

1. **Configurer la source de données** : vous devez définir une connexion à un système pour récupérer des informations supplémentaires qui seront utilisées pour vos parcours, par exemple dans vos conditions. Une source de données Adobe Experience Platform intégrée est également définie au moment de l&#39;approvisionnement. Cette étape n&#39;est pas obligatoire si vous n&#39;exploitez que les données des événements de votre parcours. Cette étape est effectuée par un **utilisateur technique**. [En savoir plus](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **Configurer une action** : si vous utilisez un système tiers pour envoyer vos messages, vous pouvez créer une action personnalisée. En savoir plus dans cette [section](../action/action.md). Cette étape est effectuée par un **utilisateur technique**. Si vous utilisez les fonctionnalités de message intégrées à Journey Optimizer, vous devez simplement ajouter une action de canal à votre parcours et concevoir votre contenu.

   ![](assets/custom2.png)



Les ingénieurs de données peuvent consulter [cette section](../configuration/about-data-sources-events-actions.md) pour en savoir plus sur la procédure de configuration des parcours, y compris les sources de données, les événements et les actions.


>[!NOTE]
>
>Les mécanismes de sécurisation et limitations des parcours sont détaillés sur [cette page](../start/guardrails.md).

## Création d’un parcours à plusieurs étapes {#jo-build}

Pour créer un parcours à plusieurs étapes, procédez comme suit :

1. Dans la section du menu Gestion des PARCOURS, cliquez sur **[!UICONTROL Parcours]**.

1. Cliquez sur le bouton **[!UICONTROL Créer un Parcours]** pour créer un parcours.

1. Modifiez le volet de configuration du parcours pour définir le nom du parcours et ses propriétés. Découvrez comment définir les propriétés de votre parcours dans [cette page](journey-properties.md).

   ![](assets/jo-properties.png)

Vous pouvez ensuite commencer à concevoir votre parcours.

## Concevoir le parcours {#jo-design}

Le concepteur de parcours omnicanaux dispose d’une interface intuitive par glisser-déposer, qui vous permet de créer des parcours à plusieurs étapes avec des audiences ciblées, des mises à jour basées sur des interactions client ou commerciale en temps réel et des messages omnicanaux.

![](assets/journey38.png)

1. Commencez par effectuer un glisser-déposer d’un événement ou d’une activité **Lecture d’audience** de la palette vers la zone de travail. Pour en savoir plus sur la conception d&#39;un parcours, consultez [cette section](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Faites glisser et déposez les étapes suivantes que l&#39;individu doit suivre. Par exemple, vous pouvez ajouter une condition suivie d’une action de canal. Pour en savoir plus sur les activités, consultez [cette section](about-journey-activities.md).

## Tester le parcours {#jo-test}

Une fois que vous avez créé votre parcours, vous pouvez le tester avant de le publier. Journey Optimizer propose un « mode test » pour afficher les profils de test lors de leur déplacement sur le parcours, détectant les erreurs potentielles avant l’activation. L’exécution de tests rapides vous permet de vérifier que les parcours fonctionnent correctement afin de pouvoir les publier en toute confiance.

En savoir plus dans cette [section](testing-the-journey.md)

## Publier le parcours {#jo-pub}

Vous devez publier un parcours pour l’activer et le rendre disponible pour que de nouveaux profils puissent y accéder. Avant de publier votre parcours, vérifiez qu’il est valide et qu’il ne comporte aucune erreur, Vous ne pouvez pas publier un parcours contenant des erreurs. En savoir plus sur la publication du parcours dans cette [section](publishing-the-journey.md).

![](assets/jo-journeyuc2_32bis.png)

Une fois publié, vous pouvez surveiller votre parcours à l’aide des outils de rapports dédiés afin de mesurer l’efficacité de votre parcours.

![](assets/jo-dynamic_report_journey_12.png)

En savoir plus sur les rapports de parcours dans cette [section](../reports/live-report.md).

Notez que vous pouvez dupliquer un parcours existant ou créer une nouvelle version d’un parcours. Découvrez comment dans [cette page](journey-ui.md)