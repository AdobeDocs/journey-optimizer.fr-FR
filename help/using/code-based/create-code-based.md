---
title: Créer des expériences basées sur le code
description: Découvrez comment créer des expériences basées sur le code dans Journey Optimizer.
feature: Offers
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
badge: label="Version Beta"
exl-id: 25c2c448-9380-47b0-97c5-16d9afb794c5
source-git-commit: b00a4e174e978121687428147b5b3861077c5182
workflow-type: tm+mt
source-wordcount: '1009'
ht-degree: 99%

---

# Créer des expériences basées sur le code {#create-code-based}

>[!BEGINSHADEBOX]

Ce guide couvre les sujets suivants :

* [Prise en main du canal basé sur le code](get-started-code-based.md)
* [Conditions préalables basées sur le code](code-based-prerequisites.md)
* [Exemples de mises en œuvre basées sur le code](code-based-implementation-samples.md)
* **[Créer des expériences basées sur le code](create-code-based.md)**

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>La fonctionnalité de canal d’expérience basée sur le code est actuellement disponible en version bêta pour certains utilisateurs ou utilisatrices uniquement. Pour rejoindre le programme Beta, contactez l’assistance clientèle d’Adobe.

## Créer une campagne basée sur le code {#create-code-based-campaign}

Pour commencer à créer votre expérience basée sur le code par le biais d’une campagne, suivez les étapes ci-dessous.

>[!CAUTION]
>
>Dans [!DNL Journey Optimizer], vous ne pouvez actuellement créer des expériences basées sur le code qu’en utilisant des **campagnes**.

1. Création d’une campagne. [En savoir plus](../campaigns/create-campaign.md)

1. Sélectionnez l’action **[!UICONTROL Expérience basée sur le code (Beta)]**.

1. Saisissez la surface de l’expérience basée sur le code. [En savoir plus](#surface-definition)

   ![](assets/code-based-campaign-surface.png)

   >[!CAUTION]
   >
   >Assurez-vous que l’URI de surface utilisé dans votre campagne basée sur le code correspond à celui utilisé dans votre propre mise en œuvre. Sinon, les modifications ne seront pas diffusées.

1. Sélectionnez **[!UICONTROL Créer]**.

1. Suivez les étapes de création d’une campagne , telles que les propriétés de la campagne, l’[audience](../audience/about-audiences.md) et le [planning](../campaigns/create-campaign.md#schedule).

   >[!NOTE]
   >
   >Pour plus d’informations sur la configuration d’une campagne, consultez cette [page](../campaigns/get-started-with-campaigns.md).

1. Modifiez le contenu selon vos besoins à l’aide de l’éditeur d’expression. [En savoir plus](#edit-code)

   ![](assets/code-based-campaign-edit-content.png)

## Modifier le contenu du code {#edit-code}

>[!CONTEXTUALHELP]
>id="ajo_code_based_experience"
>title="Utiliser l’éditeur d’expression"
>abstract="Insérez et modifiez le code que vous souhaitez diffuser dans le cadre de cette action d’expérience basée sur le code."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/personalized-dynamic-content/personalization/expression-editor/personalization-build-expressions.html" text="Commencer avec l’éditeur d’expression"

1. Dans l’écran de modification de la campagne, sélectionnez **[!UICONTROL Modifier le code]**.

   ![](assets/code-based-campaign-edit-code.png)

1. L’[éditeur d’expression](../personalization/personalization-build-expressions.md) s’ouvre. Il s’agit d’une interface de création d’expérience non visuelle qui vous permet de créer votre code.

1. Vous pouvez passer du mode de création HTML au mode JSON, et inversement.

   >[!CAUTION]
   >
   >Si vous changez de mode de création, vous perdrez l’ensemble de votre code actuel. Veillez donc à changer de mode avant de commencer la création.

1. Saisissez votre code selon vos besoins. Vous pouvez utiliser l’éditeur d’expression [!DNL Journey Optimizer] avec toutes ses fonctionnalités de personnalisation et de création. [En savoir plus](../personalization/personalization-build-expressions.md)

   ![](assets/code-based-campaign-code-editor.png)

1. Dans les campagnes basées sur le code, vous pouvez utiliser la fonctionnalité de décision d’expérience. Sélectionnez l’icône **[!UICONTROL Décisions]** dans la barre de gauche, puis cliquez sur **[!UICONTROL Créer une décision]**. [En savoir plus](../experience-decisioning/create-decision.md)

   ![](assets/code-based-campaign-create-decision.png)

   >[!NOTE]
   >
   >La fonctionnalité de décision basée sur l’expérience est actuellement disponible en version Beta pour certains utilisateurs et utilisatrices.

1. Cliquez sur **[!UICONTROL Enregistrer et fermer]** pour confirmer vos modifications.

Désormais, dès que votre développeur ou développeuse lance un appel d’API ou de SDK pour récupérer du contenu pour la surface sélectionnée, les modifications sont appliquées à votre page web ou application.

## Tester la campagne basée sur le code {#test-code-based-campaign}

>[!CONTEXTUALHELP]
>id="ajo_code_based_preview"
>title="Prévisualiser votre expérience basée sur le code"
>abstract="Effectuez une simulation de ce à quoi ressemblera votre expérience basée sur le code."

Pour afficher un aperçu de votre expérience basée sur le code qui a été modifiée, suivez les étapes ci-dessous.

>[!CAUTION]
>
>Vous devez disposer de profils de test pour simuler les offres qui leur seront diffusées. Découvrez comment [créer des profils de test](../audience/creating-test-profiles.md).

1. Dans l’écran de modification du contenu ou l’éditeur d’expression, sélectionnez **[!UICONTROL Simuler le contenu]**.

   ![](assets/code-based-campaign-simulate.png)

1. Cliquez sur **[!UICONTROL Gérer les profils de test]** pour sélectionner un ou plusieurs profils de test.

1. Un aperçu de votre expérience basée sur le code qui a été modifiée s’affiche.

<!--
    ![](assets/code-based-designer-preview.png)

    You can also open it in the default browser, or copy the test URI to paste it in any browser. This allows you to share the link with your team and stakeholders who will be able to preview the new web experience in any browser before the campaign goes live.

    When copying the test URI, the content displayed is the one personalized for the test profile used when the content simulation was generated in [!DNL Journey Optimizer].-->

## Activer la campagne basée sur le code {#activate-code-based-campaign}

Une fois que vous avez défini votre campagne basée sur le code et modifié votre contenu selon vos besoins à l’aide de l’[éditeur basé sur le code](#edit-code), vous pouvez la vérifier et l’activer. Suivez les étapes ci-dessous.

>[!NOTE]
>
>Vous pouvez également prévisualiser le contenu de votre campagne avant de l’activer. [En savoir plus](#test-code-based-campaign)

1. Dans votre campagne basée sur le code, sélectionnez **[!UICONTROL Examiner pour activer]**.

   ![](assets/code-based-campaign-review.png)

1. Vérifiez et modifiez si nécessaire le contenu, les propriétés, la surface, l’audience et le planning.

1. Sélectionnez **[!UICONTROL Activer]**.

   ![](assets/code-based-campaign-activate.png)

   >[!NOTE]
   >
   >Lorsque vous cliquez sur **[!UICONTROL Activer]**, les modifications des campagnes basées sur le code peuvent prendre jusqu’à 1 minute pour être prises en compte à votre emplacement.

Votre campagne basée sur le code passe au statut **[!UICONTROL Actif]** et est maintenant visible pour l’audience sélectionnée. Chaque destinataire de votre campagne peut voir vos modifications.

>[!NOTE]
>
>Si vous avez défini un planning pour votre campagne basée sur le code, celle-ci conserve le statut **[!UICONTROL Planifié]** jusqu’à ce que la date et l’heure de début soient atteintes.
>
>Si vous activez une campagne basée sur le code ayant un impact sur les mêmes emplacements qu’une autre campagne déjà active, toutes les modifications seront appliquées à vos emplacements.

En savoir plus sur l’activation des campagnes dans [cette section](../campaigns/review-activate-campaign.md).

## Arrêter une campagne basée sur le code {#stop-code-based-campaign}

Lorsqu’une campagne basée sur le code est active, vous pouvez l’arrêter afin d’empêcher votre audience de voir vos modifications. Suivez les étapes ci-dessous.

1. Sélectionnez une campagne active dans la liste.

1. Dans le menu supérieur, sélectionnez **[!UICONTROL Arrêter la campagne]**.

   ![](assets/code-based-campaign-stop.png)

1. Les modifications que vous avez ajoutées ne seront plus visibles pour l’audience que vous avez définie.

>[!NOTE]
>
>Une fois une campagne basée sur le code arrêtée, vous ne pouvez plus la modifier ni l’activer. Vous pouvez uniquement la dupliquer et activer la campagne dupliquée.

## Rapports de campagne basée sur le code

Vous pouvez accéder aux rapports de campagne basée sur le code à partir de l’écran récapitulatif de la campagne.

Les rapports globaux portent sur les événements qui se sont produits il y a au moins deux heures et couvrent les événements sur une période sélectionnée. En comparaison, les rapports dynamiques portent sur les événements qui se sont produits au cours des dernières 24 heures, avec un intervalle de temps minimal de deux minutes à compter de l’occurrence de l’événement.

### Rapport dynamique basé sur le code {#live-report-code-based}

Dans votre **[!UICONTROL rapport dynamique]** de campagne, l’onglet **[!UICONTROL Expérience basée sur le code]** présente les informations principales relatives à vos applications et à vos pages web. [En savoir plus sur les rapports dynamiques](../reports/campaign-live-report.md)

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport d’expérience basée sur le code.

Les KPI de **[!UICONTROL performances d’expérience basée sur le code]** détaillent les informations principales relatives à l’engagement de vos visiteurs et visiteuses avec vos expériences basées sur le code, telles que :

* **[!UICONTROL Impressions]** : nombre total d’expériences diffusées à tous les utilisateurs et utilisatrices.

* **[!UICONTROL Interactions]** : nombre total d’engagements en lien avec votre application ou page web. Cela inclut toutes les actions entreprises par les personnes, telles que les clics ou toute autre interaction.

Le graphe **[!UICONTROL Résumé de l’expérience basée sur le code]** présente l’évolution de vos expériences web (impressions, impressions et interactions uniques) pour les dernières 24 heures.

<!--The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your app/pages.-->
+++

### Rapport global basé sur le code {#global-report-code-based}

Pour accéder directement au rapport global de campagne basée sur le code à partir de votre campagne, cliquez sur le bouton **[!UICONTROL Afficher le rapport]**. [En savoir plus sur le rapport global](../reports/campaign-global-report.md)

Depuis votre **[!UICONTROL rapport global]** de campagne, l’onglet **[!UICONTROL Expérience basée sur le code]** présente les informations principales relatives à vos applications ou vos pages web.

![](assets/code-based-campaign-global-report.png)

<!--image-->

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport d’expérience basée sur le code.

Les KPI de **[!UICONTROL performances d’expérience basée sur le code]** détaillent les informations principales relatives à l’engagement de vos visiteurs et visiteuses avec vos expériences, telles que :

* **[!UICONTROL Impressions uniques]** : nombre d’utilisateurs et d’utilisatrices uniques auxquels l’expérience a été diffusée.

* **[!UICONTROL Impressions]** : nombre total d’expériences diffusées à tous les utilisateurs et utilisatrices.

* **[!UICONTROL Interactions]** : pourcentage d’engagements avec votre application/page. Cela inclut toutes les actions entreprises par les personnes, telles que les clics ou toute autre interaction.

Le graphe **[!UICONTROL Résumé de l’expérience basée sur le code]** présente l’évolution de vos expériences web (impressions uniques, impressions et interactions) pour la période concernée.

<!--The **[!UICONTROL Interactions by element]** table details the main information relative to your visitors' engagement with the various elements on your apps/pages.-->
+++

<!--
## How-to video{#video}

The video below shows how to create a code-based campaign, configure its properties, review, and publish it.

>[!VIDEO]()

-->
