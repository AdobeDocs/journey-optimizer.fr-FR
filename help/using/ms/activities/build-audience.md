---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Créer une audience
description: Découvrez comment utiliser l’activité Créer une audience dans une campagne à plusieurs étapes
hide: true
hidefromtoc: true
source-git-commit: 00f843300a9cfe798ea4d3a92fbe89ba80e70bc5
workflow-type: tm+mt
source-wordcount: '368'
ht-degree: 61%

---

# Créer une audience {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="Activité Créer une audience"
>abstract="L’activité **Créer une audience** vous permet de définir l’audience qui va rejoindre la campagne à plusieurs étapes. Lors de l’envoi de messages dans le cadre d’une campagne à plusieurs étapes, l’audience du message n’est pas définie dans l’activité de canal, mais dans l’activité **Créer une audience**."

L’activité **Créer une audience** est une activité de **ciblage**. Cette activité permet de définir l’audience qui va entrer dans la campagne à plusieurs étapes. Lors de l’envoi de messages dans le cadre d’une campagne à plusieurs étapes, l’audience du message n’est pas définie dans l’activité de canal, mais dans l’activité **Créer une audience**.

Pour définir la population de l’audience, vous pouvez :

* sélectionner une audience Adobe Experience Platform ;
* Créez une audience à l’aide du concepteur de requête en définissant et en combinant des critères de filtrage.

>[!NOTE]
>
>Les audiences chargées à partir d’un fichier ne peuvent pas être ciblées à l’aide d’une activité Créer une audience. Pour cela, vous devez utiliser une activité **Chargement de fichier** suivie d&#39;une activité **Réconciliation**.

<!--
The **Build audience** activity can be placed at the beginning of the workflow or after any other activity. Any activity can be placed after the **Build audience**.
-->

## Configurer l’activité Créer une audience {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="Audience"
>abstract="Sélectionnez votre audience de la même manière que vous utilisez une audience lors de la conception d’une nouvelle diffusion."

Pour configurer l’activité **Créer une audience**, procédez comme suit :

![](../assets/workflow-audience.png)

1. Ajoutez une activité **Créer une audience**.
1. Définissez un libellé.
1. Définissez le type d’audience : **Créer votre audience** ou **Lecture d’audience**.
1. Configurez votre audience en suivant les étapes présentées dans les onglets ci-dessous.

>[!BEGINTABS]

>[!TAB Créer votre propre (requête)]

Pour créer votre propre requête, procédez comme suit :

1. Sélectionnez **Créer la vôtre (requête)**.
1. Choisissez la **dimension de ciblage**. La dimension de ciblage permet de définir la population ciblée par l’opération : personnes destinataires, personnes bénéficiaires d’un contrat, opérateurs et opératrices, personnes abonnées, etc. Par défaut, la cible est sélectionnée parmi les destinataires.
1. Cliquez sur **Continuer**.
1. Utilisez le modéliseur de requête pour définir votre requête, de la même manière que vous créez une audience lors de la conception d’un e-mail.

>[!TAB Lecture d’audience]

Pour sélectionner une audience existante, procédez comme suit :

1. Sélectionnez **Lecture d’audience**.
1. Cliquez sur **Continuer**.
1. Sélectionnez votre audience de la même manière que vous utilisez une audience lors de la conception d’une nouvelle diffusion.

>[!ENDTABS]

## Exemples{#build-audience-examples}

Voici un exemple de campagne à plusieurs étapes avec deux activités **Créer une audience**. La première cible l’audience des joueurs et joueuses de poker, suivie d’une diffusion e-mail. La seconde cible l’audience des clientes et clients VIP, suivie d’une diffusion SMS.

![](../assets/workflow-audience-example.png)
