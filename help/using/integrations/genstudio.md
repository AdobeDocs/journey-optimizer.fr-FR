---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main de l’intégration de GenStudio dans Journey Optimizer
description: Découvrez comment utiliser GenStudio dans Journey Optimizer
feature: Content Assistant, Integrations
topic: Content Management, Artificial Intelligence
role: User
level: Beginner, Intermediate
source-git-commit: b24e50f698567e1f45318d942dff87febba179c9
workflow-type: tm+mt
source-wordcount: '623'
ht-degree: 2%

---

# Prise en main de l’intégration de GenStudio {#gs-genstudio}

>[!CONTEXTUALHELP]
>id="ajo_genstudio_button"
>title="Utiliser un modèle créé avec GenStudio"
>abstract="Grâce à l’intégration transparente à Adobe GenStudio for Performance Marketing, vous pouvez facilement importer un modèle GenStudio amélioré par la technologie Adobe AI."

>[!AVAILABILITY]
>
>L’intégration de GenStudio dans [!DNL Adobe Journey Optimizer] n’est actuellement pas disponible pour être utilisée avec les offres complémentaires **Healthcare Shield** ou **Privacy and Security Shield**.
>
>L’intégration de GenStudio est disponible uniquement pour le canal e-mail.

[Adobe GenStudio for Performance Marketing](https://business.adobe.com/fr/products/genstudio-for-performance-marketing.html){target="_blank"} est une application générée, basée sur l’IA, qui permet aux équipes marketing de créer leurs propres annonces et e-mails afin de générer des campagnes marketing personnalisées et percutantes, conformes à vos normes de marque et à vos politiques d’entreprise. En utilisant la technologie d’IA d’Adobe, il fournit une suite complète d’outils qui simplifient les complexités de la création et de la gestion de contenu afin que les créatifs puissent se concentrer sur l’innovation.

En savoir plus sur les [!DNL GenStudio for Performance Marketing] dans la [documentation](https://experienceleague.adobe.com/fr/docs/genstudio-for-performance-marketing/user-guide/home){target="_blank"} dédiée.

>[!INFO]
>
>Pour en savoir plus, consultez cette [présentation](https://business.adobe.com/products/genstudio-for-performance-marketing.html#watch-overview){target="_blank"} et une [démonstration](https://business.adobe.com/products/genstudio-for-performance-marketing.html#demo){target="_blank"} de [!DNL Adobe GenStudio for Performance Marketing].

<!--To access the GenStudio integration in [!DNL Adobe Journey Optimizer] feature, users need to be granted the **xxx** permission. [Learn more](../administration/permissions.md)

>[!IMPORTANT]
>
>* Before starting using this capability, read out related [Guardrails and Limitations](#generative-guardrails).-->

Pour améliorer l’efficacité marketing et maintenir la cohérence de la marque, vous pouvez intégrer facilement les expériences [!DNL **GenStudio for Performance Marketing**] avec [!DNL **Adobe Journey Optimizer**]. Vous pouvez ainsi tirer parti de la création de contenu optimisée par l’IA de [!DNL GenStudio], ainsi que des fonctionnalités d’orchestration avancées de [!DNL Journey Optimizer].

<!--![](../rn/assets/do-not-localize/genstudio.gif)-->

<!--Guardrails and limitations {#genstudio-guardrails}

General guidelines for using the GenStudio integration in [!DNL Adobe Journey Optimizer] for email generation are listed below:

See if guidelines/limitations such as the ones listed [here](gs-generative.md#generative-guardrails) for the AI Assistant can apply.

The following limitations apply to GenStudio integration in [!DNL Adobe Journey Optimizer]:-->

## Tirer parti des fonctionnalités de GenStudio dans Journey Optimizer {#use-genstudio}

L’intégration [!DNL GenStudio for Performance Marketing] et [!DNL Journey Optimizer] vous permet de faire en sorte que les professionnels du marketing de votre entreprise travaillent mieux ensemble pour rationaliser les processus.

Par exemple, un spécialiste du marketing technique, qui utilise [!DNL Journey Optimizer] pour développer et automatiser des campagnes par e-mail, peut collaborer avec un spécialiste du marketing de performance qui crée du contenu à l’aide de [!DNL GenStudio].

Grâce à cette intégration, les deux peuvent travailler ensemble pour intégrer facilement du contenu de marque provenant de [!DNL GenStudio] dans [!DNL Journey Optimizer], fournissant des e-mails attrayants qui ciblent des segments de clients spécifiques et stimulent les ventes.

### Exporter un modèle HTML de Journey Optimizer vers GenStudio {#export-from-ajo-to-genstudio}

Tout d’abord, vous pouvez exporter un modèle HTML [!DNL Journey Optimizer], y compris les directives de votre marque vers [!DNL GenStudio for Performance Marketing]. Suivez les étapes ci-dessous.

1. Dans [!DNL Journey Optimizer], accédez au contenu de votre e-mail dans un parcours ou une campagne. [Voici comment procéder](../email/get-started-email-design.md#key-steps)

1. Dans le Designer d’e-mail, sélectionnez **[!UICONTROL Exporter HTML]** à partir du bouton **[!UICONTROL Plus]**.

   ![](assets/genstudio-export-template.png){zoomable="yes"}

1. Chargez ce modèle exporté HTML dans [!DNL GenStudio for Performance Marketing]. <!--Make sure you detect the fields that the generative AI uses to insert content in order to create an actionable template.-->

   >[!NOTE]
   >
   >Découvrez comment télécharger un modèle HTML dans [!DNL GenStudio] dans la section dédiée au [Guide de l’utilisateur d’Adobe GenStudio for Performance Marketing](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/content/templates/use-templates#templates-from-ajo-and-marketo){target="_blank"}.

1. Dans GenStudio, utilisez ce modèle pour créer plusieurs variations d’e-mail avec des invites d’IA et les enregistrer.

   >[!NOTE]
   >
   >Découvrez comment créer des expériences e-mail dans la [section](https://experienceleague.adobe.com/en/docs/genstudio-for-performance-marketing/user-guide/create/create-email-experience){target="_blank"} dédiée à GenStudio.

### Utilisation des expériences GenStudio dans Journey Optimizer {#leverage-genstudio-experiences}

Pour tirer parti des variations d’e-mail [!DNL GenStudio] que vous venez de créer en les important dans [!DNL Journey Optimizer], procédez comme suit.

1. Dans [!DNL Journey Optimizer], [ajoutez un e-mail](../email/create-email.md) à une campagne.

1. Dans l’écran de configuration de la campagne, parcourez l’écran [Modifier le contenu](../email/create-email.md#define-email-content) et cliquez sur **[!UICONTROL Modifier le corps de l’e-mail]** pour ouvrir le Designer d’e-mail. [Voici comment procéder](../email/get-started-email-design.md#key-steps)

1. Sur la page d&#39;accueil d&#39;Email Designer, sélectionnez **[!UICONTROL Importer HTML]** et cliquez sur le bouton **[!UICONTROL Adobe GenStudio for Performance Marketing]**.

   ![](assets/genstudio-pem-import-email.png){zoomable="yes"}

1. Parcourez les expériences GenStudio pour commencer à créer votre contenu. Vous pouvez filtrer les expériences selon plusieurs critères tels que les produits, les rôles, les marques ou même les couleurs.

   <!--![](assets/genstudio-filter-experiences.png){zoomable="yes"}-->

1. Sélectionnez une expérience et cliquez sur **[!UICONTROL Utiliser]**.

   ![](assets/genstudio-use-experience.png){zoomable="yes"}

1. Sélectionnez le dossier dans lequel vous souhaitez importer l’expérience GenStudio.

   ![](assets/genstudio-choose-destination.png){zoomable="yes"}

1. Le contenu sélectionné s’affiche dans le Designer d’e-mail.

   ![](assets/genstudio-email-content.png){zoomable="yes"}

   >[!NOTE]
   >
   >Les expériences GenStudio [créées à partir d’un modèle [!DNL Journey Optimizer]  ](#export-from-ajo-to-genstudio) sont importées directement dans le Designer d’e-mail. Les expériences GenStudio créées sans modèle de [!DNL Journey Optimizer] sont importées en [mode de compatibilité](../email/existing-content.md).

   Utilisez les [outils d’édition de contenu d’e-mail](../email/content-from-scratch.md) et [champs de personnalisation](../personalization/personalize.md) pour modifier votre e-mail selon vos besoins. Enregistrez votre contenu.

1. Revenez à la page de résumé de la campagne, puis cliquez sur **[!UICONTROL Créer une expérience]** pour utiliser l’expérimentation. [Découvrez comment créer une expérience de contenu](../content-management/content-experiment.md)

   <!--![](assets/genstudio-create-experiment.png){zoomable="yes"}-->

1. Créez plusieurs traitements et répétez les étapes ci-dessus pour importer et exploiter rapidement les autres variations d’expérience d’e-mail que vous avez créées dans [!DNL GenStudio].

   ![](assets/genstudio-define-treatments.png){zoomable="yes"}

1. Enregistrez vos modifications et [activez](../campaigns/review-activate-campaign.md) la campagne.

Après avoir exécuté l’expérience, suivez les performances de vos traitements de campagne avec le [rapport de campagne d’expérimentation](../reports/campaign-global-report-cja-experimentation.md). Vous pouvez ensuite interpréter les résultats de votre expérience. [Voici comment procéder](../content-management/get-started-experiment.md#interpret-results)