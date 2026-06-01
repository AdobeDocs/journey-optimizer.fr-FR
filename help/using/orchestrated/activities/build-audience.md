---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Créer une audience
description: Découvrez comment utiliser l’activité Créer une audience dans une campagne orchestrée.
exl-id: 3959b5fa-0c47-42a5-828f-4d7ca9b7e72d
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/9hEr5kAHco1iq8arv-FddaG3vm54CS-cPFUA63soeAg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29c
subfeature_v2: id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 18f6b23dbbe53e486e5af76ef7cc61fa1784475d
workflow-type: tm+mt
source-wordcount: 338
ht-degree: 78%

---

# Créer une audience {#build-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience"
>title="Activité Créer une audience"
>abstract="L’activité **Créer une audience** vous permet de définir l’audience qui va entrer dans la campagne orchestrée. Lors de l’envoi de messages dans le cadre d’une campagne orchestrée, l’audience du message n’est pas définie dans l’activité de canal, mais dans l’activité **Créer une audience**."

En tant que spécialiste marketing, vous pouvez créer des segments d’audience complexes par le biais d’une interface intuitive, ce qui vous permet de cibler les utilisateurs et les utilisatrices en fonction d’un large éventail de critères et de comportements, afin d’adapter plus efficacement vos campagnes.

Pour ce faire, utilisez l’activité de ciblage **[!UICONTROL Créer une audience]**. Cette activité définit l’audience qui entre dans la campagne orchestrée. Lors de l’envoi de messages dans le cadre d’une campagne orchestrée, l’audience est définie dans l’activité **[!UICONTROL Créer une audience]** et non dans la campagne orchestrée.

## Configurer l’activité Créer une audience {#build-audience-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_build_audience_audienceselector"
>title="Audience"
>abstract="Sélectionnez votre audience de la même manière que vous utilisez une audience lors de la conception d’une nouvelle diffusion."

Pour configurer l’activité **[!UICONTROL Créer une audience]**, procédez comme suit :

1. Ajoutez une activité **[!UICONTROL Créer une audience]**.

   ![](../assets/build-audience.png)

1. Définissez un **[!UICONTROL libellé]**.

1. Configurez votre audience en suivant les étapes présentées dans les onglets ci-dessous.

1. Choisissez la **[!UICONTROL dimension de ciblage]**. La dimension de ciblage permet de définir la population ciblée par l’opération : destinataires, bénéficiaires d’un contrat, opérateur ou opératrice, abonnées et abonnés, etc. Par défaut, la cible est sélectionnée parmi les destinataires.

1. Cliquez sur **[!UICONTROL Continuer]**.

1. Utilisez le créateur de règles pour définir votre requête. [En savoir plus sur le créateur de règles dans cette section](../orchestrated-rule-builder.md)

1. Indiquez si une transition sortante doit être générée lorsque l’audience est vide.

## Exemples{#build-audience-examples}

Voici un exemple de campagne orchestrée comportant deux activités **[!UICONTROL Créer une audience]**. La première cible les profils qui ont des articles dans leur panier, avec une diffusion par e-mail. La seconde cible les profils qui ont une liste de souhaits, avec une diffusion par SMS.

![](../assets/build-audience-2.png)

Dans l’exemple ci-dessous, l’activité **[!UICONTROL Créer une audience]** utilise le créateur de règles pour filtrer les profils en fonction de leur formule d’abonnement. Une condition est définie sur l’attribut `plan` pour inclure uniquement les profils où `plan = "basic"`, ce qui limite l’audience aux abonnés de niveau de base avant de les transmettre à l’activité suivante.

![](../assets/build-audience-plan.png){width="50%" align="left"}
