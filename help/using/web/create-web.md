---
title: Créer des expériences web
description: Découvrez comment créer une page web et modifier son contenu dans Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: e28c038b-49ed-4685-bfe6-514116eb0711
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 100%

---

# Créer des expériences web {#create-web}

>[!AVAILABILITY]
>
>La fonctionnalité de canal web est actuellement disponible en version bêta pour certains utilisateurs uniquement.

[!DNL Journey Optimizer] vous permet de personnaliser l’expérience web que vous diffusez à vos clients par le biais de campagnes web entrantes.

>[!CAUTION]
>
>Dans [!DNL Journey Optimizer], vous ne pouvez actuellement créer des expériences web qu’en utilisant des **campagnes**.

## Conditions préalables {#prerequesites}

Pour créer et accéder à des pages web dans l’interface utilisateur [!DNL Journey Optimizer], remplissez les conditions préalables suivantes :

* Pour ajouter des modifications à votre site web, vous devez mettre en œuvre le [SDK Web Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=fr){target=&quot;_blank&quot;} sur votre site web.

* Pour accéder au concepteur web [!DNL Journey Optimizer], vous devez télécharger l’extension de navigateur [Adobe Experience Cloud Visual Editing Helper ](https://chrome.google.com/webstore/detail/adobe-experience-cloud-vi/kgmjjkfjacffaebgpkpcllakjifppnca){target=&quot;_blank&quot;} sur Chrome. [En savoir plus](visual-editing-helper.md)

>[!CAUTION]
>
>Google Chrome est actuellement le seul navigateur qui prend en charge la création de pages web dans [!DNL Journey Optimizer].

Pour que l’expérience web soit correctement diffusée, les paramètres suivants doivent être définis :

* Dans la [Collection de données Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/overview.html?lang=fr){target=&quot;_blank&quot;}, assurez-vous qu’un train de données est défini, de telle sorte que sous le service **[!UICONTROL Adobe Experience Platform]**, les deux options suivantes soient activées : **[!UICONTROL Segmentation Edge]** et **[!UICONTROL Adobe Journey Optimizer]**.

   Cela permet de s’assurer que les événements entrants Journey Optimizer sont correctement gérés par Adobe Experience Platform Edge. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=fr){target=&quot;_blank&quot;}

   ![](assets/web-aep-datastream-ajo.png)

   >[!NOTE]
   >
   >L’option **[!UICONTROL Adobe Journey Optimizer]** ne peut être activée que lorsque l’option **[!UICONTROL Segmentation Edge]** est déjà activée.

* Dans [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=fr){target=&quot;_blank&quot;}, assurez-vous d’avoir une stratégie de fusion avec l’option **[!UICONTROL Stratégie de fusion Active-On-Edge]** activée. Pour ce faire, sélectionnez une stratégie sous le menu Experience Platform **[!UICONTROL Client]** > **[!UICONTROL Profils]** > **[!UICONTROL Stratégies de fusion]**. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=fr#configure){target=&quot;_blank&quot;}

   Cette stratégie de fusion est utilisée par les canaux entrants [!DNL Journey Optimizer] pour activer et publier correctement les campagnes entrantes sur l’Edge. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/profile/merge-policies/ui-guide.html?lang=fr){target=&quot;_blank&quot;}

   ![](assets/web-aep-merge-policy.png)

## Créer une campagne web {#create-web-campaign}

Pour commencer à créer votre expérience web par le biais d’une campagne, suivez les étapes ci-dessous.

1. Créer une campagne. [En savoir plus](../campaigns/create-campaign.md)

1. Sélectionnez l’action **[!UICONTROL Web]**.

   ![](assets/web-create-campaign.png)

1. Définissez une surface web.

   >[!NOTE]
   >
   >Une surface web est une propriété web identifiée par une URL où le contenu sera diffusé. Elle peut correspondre à l’URL d’une ou de plusieurs pages, ce qui vous permet de diffuser des modifications sur une ou plusieurs pages web.

   Vous pouvez saisir une **[!UICONTROL URL de la page]** si vous souhaitez appliquer les modifications à une seule page uniquement.

   ![](assets/web-campaign-surface.png)

1. Vous pouvez également créer une **[!UICONTROL Règle de correspondance de pages]** pour cibler plusieurs URL correspondant à la même règle ; par exemple, si vous souhaitez appliquer les modifications à une bannière principale sur l’ensemble d’un site web ou ajouter une image principale qui s’affiche sur toutes les pages de produits d’un site web.

   Pour ce faire, sélectionnez **[!UICONTROL Règle de correspondance de pages]** et cliquez sur **[!UICONTROL Créer une règle]**.

   ![](assets/web-campaign-matching-rule.png)

1. Définissez vos critères pour les champs **[!UICONTROL Domaine]** et **[!UICONTROL Page]**.

   Par exemple, si vous souhaitez modifier des éléments qui s’affichent sur toutes les pages de produits pour femmes de votre site web Luma, sélectionnez **[!UICONTROL Domaine]** > **[!UICONTROL Commence par]** > `luma` et **[!UICONTROL Page]** > **[!UICONTROL Contient]** > `women`.

   ![](assets/web-pages-matching-rule.png)

1. Enregistrez vos modifications. La règle s’affiche dans l’écran **[!UICONTROL Créer une campagne]**.

   ![](assets/web-pages-matching-rule-example.png)

1. Une fois la surface web définie, sélectionnez **[!UICONTROL Créer]**. Vous pouvez maintenant configurer les propriétés et les paramètres de votre campagne.

## Configurer la campagne web {#configure-web-campaign}

1. Dans l’onglet **[!UICONTROL Propriétés]**, vous pouvez modifier le nom de la campagne et ajouter une description si nécessaire.

   ![](assets/web-campaign-properties.png)

1. Pour attribuer des libellés d’utilisation des données personnalisés ou de base à la campagne web, sélectionnez l’option **[!UICONTROL Gérer l’accès]** en haut de l’écran. [En savoir plus sur le contrôle d’accès au niveau de l’objet (OLAC)](../administration/object-based-access.md)

1. Vous pouvez sélectionner **[!UICONTROL Expérience de contenu]** pour tester les traitements de contenu avec des parties de l’audience, afin de déterminer le traitement le plus performant par rapport à une mesure spécifique. [En savoir plus](../campaigns/content-experiment.md)

   >[!AVAILABILITY]
   >
   >La fonctionnalité **Expérience de contenu** est actuellement disponible uniquement pour un ensemble d’organisations (disponibilité limitée). Pour en savoir plus, contactez votre représentant Adobe.

1. Dans l’onglet **[!UICONTROL Action]** de l’opération, sélectionnez **[!UICONTROL Modifier le contenu]** pour commencer à créer votre campagne web. [En savoir plus](author-web.md)

   ![](assets/web-edit-content.png)

1. Dans l’onglet **[!UICONTROL Audience]**, définissez qui pourra voir votre campagne web. Par défaut, la campagne web sera visible par tous les visiteurs.

   ![](assets/web-campaign-audience.png)

   Vous pouvez également sélectionner une audience spécifique. Cliquez sur le bouton **[!UICONTROL Sélectionner une audience]** pour afficher la liste des segments Adobe Experience Platform disponibles. [En savoir plus sur les segments](../segment/about-segments.md)

   >[!NOTE]
   >
   >Pour les campagnes déclenchées par API, l’audience doit être définie via un appel API. [En savoir plus](../campaigns/api-triggered-campaigns.md)

   ![](assets/web-campaign-select-audience.png)

1. Dans le champ **[!UICONTROL Espace de noms d’identité]**, choisissez l’espace de noms à utiliser pour identifier les personnes à partir du segment sélectionné. [En savoir plus sur les espaces de noms](../event/about-creating.md#select-the-namespace)

1. Définissez un **[!UICONTROL Planning]** pour votre campagne web. [En savoir plus](../campaigns/create-campaign.md#schedule)

   ![](assets/web-campaign-schedule.png)

   Par défaut, elle commence lorsqu’elle est activée manuellement et se termine lorsqu’elle est arrêtée manuellement, mais vous pouvez également définir des dates et heures spécifiques pour que vos modifications soient visibles.

   ![](assets/web-campaign-schedule-start.png)

## Activation de la campagne web {#activate-web-campaign}

Une fois que vous avez défini vos [paramètres de campagne web](#configure-web-campaign) et que vous avez modifié votre contenu selon vos besoins à l’aide du [concepteur web](author-web.md), vous pouvez examiner et activer votre campagne web. Suivez les étapes ci-dessous.

>[!NOTE]
>
>Vous pouvez également prévisualiser le contenu de votre campagne web avant de l’activer. [En savoir plus](author-web.md#test-web-campaign)

1. Dans votre campagne web, sélectionnez **[!UICONTROL Examiner pour activer]**.

   ![](assets/web-campaign-review.png)

1. Examinez et modifiez si nécessaire le contenu, les propriétés, la surface, l’audience et le planning.

1. Sélectionnez **[!UICONTROL Activer]**.

   ![](assets/web-campaign-activate.png)

   >[!NOTE]
   >
   >Après avoir cliqué sur **[!UICONTROL Activer]**, les modifications des campagnes web peuvent prendre jusqu’à 15 minutes pour être disponibles en direct sur votre site web.

Votre campagne web passe au statut **[!UICONTROL Actif]** et est maintenant visible pour l’audience sélectionnée. Chaque destinataire de votre campagne peut voir les modifications que vous avez ajoutées à votre site web à l’aide du concepteur web [!DNL Journey Optimizer].

>[!NOTE]
>
>Si vous avez défini un planning pour votre campagne web, celle-ci conserve le statut **[!UICONTROL Planifié]** jusqu’à ce que la date et l’heure de début soient atteintes.
>
>Si vous activez une campagne web ayant un impact sur les mêmes pages qu’une autre campagne déjà active, toutes les modifications seront appliquées à vos pages web.

En savoir plus sur l’activation des campagnes dans [cette section](../campaigns/review-activate-campaign.md).

## Arrêt d’une campagne web {#stop-web-campaign}

Lorsqu’une campagne web est active, vous pouvez l’arrêter afin d’empêcher votre audience de voir vos modifications. Suivez les étapes ci-dessous.

1. Sélectionnez une campagne active dans la liste.

1. Dans le menu supérieur, sélectionnez **[!UICONTROL Arrêter la campagne]**.

   ![](assets/web-campaign-stop.png)

1. Les modifications que vous avez ajoutées ne seront plus visibles pour l’audience que vous avez définie.

>[!NOTE]
>
>Une fois une campagne web arrêtée, vous ne pouvez plus la modifier ni l’activer. Vous pouvez uniquement la dupliquer et activer la campagne dupliquée.
