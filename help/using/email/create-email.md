---
solution: Journey Optimizer
product: journey optimizer
title: Créer un e-mail
description: Découvrez comment créer un e-mail dans Journey Optimizer.
feature: Email
topic: Content Management
role: User
level: Beginner
keywords: créer, e-mail, commencer, parcours, campagne
exl-id: c77dc420-a375-4376-ad86-ac740e214c3c
source-git-commit: 97fa287d94efb7fb95817fc15268e736517cb629
workflow-type: tm+mt
source-wordcount: '1187'
ht-degree: 82%

---

# Créer un e-mail {#create-email}

>[!CONTEXTUALHELP]
>id="ajo_message_email"
>title="Création d&#39;un e-mail"
>abstract="Définissez l’objet de l’e-mail et ouvrez le Concepteur d’e-mail pour créer le contenu de l’e-mail."

## Ajouter une action d’e-mail {#email-action}

Pour créer un e-mail dans [!DNL Journey Optimizer], ajoutez une action d’**[!UICONTROL e-mail]** à un parcours ou à une campagne. Suivez ensuite les étapes ci-dessous, en fonction de votre cas.

>[!BEGINTABS]

>[!TAB Ajouter un e-mail à un parcours]

1. Ouvrez votre parcours, puis effectuez un glisser-déposer d’une activité **[!UICONTROL Action]** depuis la section **[!UICONTROL Actions]** de la palette. En savoir plus sur l’activité [Action](../building-journeys/journey-action.md).

   >[!IMPORTANT]
   >
   >Tous les canaux natifs étant désormais accessibles par le biais de l’activité Action , les activités de canal natives héritées seront abandonnées avec la version de mars. Les parcours existants qui incluent des actions héritées continueront à fonctionner en l’état. Aucune migration n’est requise.

1. Sélectionnez **[!UICONTROL E-mail]** comme type d’action.

   ![](assets/email_journey.png)

1. Saisissez un **[!UICONTROL Libellé]** pour identifier votre action dans la zone de travail du parcours.

1. Cliquez sur le bouton **[!UICONTROL Configurer l’action]**.

1. Vous accédez à l’onglet **[!UICONTROL Actions]**. À partir de là, sélectionnez ou créez la configuration d’e-mail à utiliser. [En savoir plus](email-settings.md)

   ![](assets/email-action-config.png)

1. En outre :

   * Vous pouvez appliquer des règles de limitation à votre action e-mail en sélectionnant un jeu de règles dans la liste déroulante **[!UICONTROL Règles métier]**. [En savoir plus](../conflict-prioritization/channel-capping.md)

   * Vous pouvez utiliser l’option **[!DNL Send time optimization]** pour prévoir le meilleur moment pour envoyer le message afin d’optimiser l’engagement en fonction des taux historiques d’ouverture et de clic. [Voici comment procéder](../building-journeys/send-time-optimization.md)

1. Sélectionnez le bouton **[!UICONTROL Modifier le contenu]** et créez votre contenu selon vos besoins à l’aide du Designer d’e-mail. [En savoir plus](#define-email-content)

1. Revenez à la zone de travail parcours. Si nécessaire, complétez votre flux de parcours en faisant glisser et en déposant des actions ou des événements supplémentaires. [En savoir plus](../building-journeys/about-journey-activities.md)

Pour plus d’informations sur la création, la configuration et la publication d’un parcours, consultez [cette page](../building-journeys/journey-gs.md).

>[!TAB Ajouter un e-mail à une campagne]

1. [Créez une campagne](../campaigns/create-campaign.md), puis sélectionnez **[!UICONTROL E-mail]** comme action.

1. Suivez les étapes de création d’une campagne par e-mail, telles que les propriétés de la campagne, l’[audience](../audience/about-audiences.md) et le [planning](../campaigns/campaign-schedule.md).

   ![](assets/email_campaign_steps.png)

1. Sélectionnez l’action **[!UICONTROL E-mail]**.

1. Sélectionnez ou créez la configuration du canal e-mail. [En savoir plus](email-settings.md)

   ![](assets/email_campaign.png)

<!--
From the **[!UICONTROL Action]** section, specify if you want to track how your recipients react to your delivery: you can track email opens, and/or clicks on links and buttons in your email.

![](assets/email_campaign_tracking.png)
-->
Pour plus d’informations sur la création, la configuration et l’activation d’une campagne, consultez [cette page](../campaigns/get-started-with-campaigns.md).

>[!ENDTABS]

## Définir le contenu de votre e-mail {#define-email-content}

<!-- update the quarry component with right ID value-->

>[!CONTEXTUALHELP]
>id="test_id"
>title="Configurer le contenu des e-mails"
>abstract="Créez le contenu de votre e-mail. Définissez son objet, puis utilisez le concepteur d’e-mails pour créer et personnaliser le corps de l’e-mail."

Après avoir ajouté l’action E-mail à votre parcours ou à votre campagne, vous devez définir le contenu de l’e-mail, y compris l’objet, les informations sur l’expéditeur ou l’expéditrice et le corps de l’e-mail à l’aide du concepteur d’e-mail. Procédez comme suit :

1. Dans l’écran de configuration des parcours ou des campagnes, cliquez sur le bouton **[!UICONTROL Modifier le contenu]** pour configurer le contenu de l’e-mail. [En savoir plus](get-started-email-design.md)

   ![](assets/email_campaign_edit_content.png)

1. Activez le bouton **[!UICONTROL Activer la prise de décision]** si vous souhaitez ajouter des politiques de décision dans votre e-mail.

   Les politiques de décision sont des conteneurs pour vos offres qui tirent profit du moteur de prise de décision afin de renvoyer dynamiquement le meilleur contenu à diffuser pour chaque membre de l’audience. [Découvrez comment ajouter une politique de décision dans un e-mail](../experience-decisioning/create-decision.md#create-decision).

   ![](assets/../../experience-decisioning/assets/decision-policy-enable.png)

   >[!AVAILABILITY]
   >
   >Pour l’instant, la création de politique de décision dans les e-mails est proposée en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en obtenir l’accès.

1. Dans la section **[!UICONTROL En-tête]**, vérifiez les champs **[!UICONTROL Nom de l’expéditeur ou de l’expéditrice]**, **[!UICONTROL E-mail de l’expéditeur ou de l’expéditrice]** et **[!UICONTROL Cci]**. Ils sont configurés dans la configuration du canal e-mail que vous avez sélectionnée. [En savoir plus](email-settings.md) <!--check if same for journey-->

   ![](assets/email_designer_edit_content_header.png)

1. Ajoutez un objet pour votre message. Pour configurer et personnaliser l’objet à l’aide de l’éditeur de personnalisation, cliquez sur l’icône **[!UICONTROL Ouvrir la boîte de dialogue de personnalisation]**. [En savoir plus](../personalization/personalization-build-expressions.md)

   >[!NOTE]
   >
   >La ligne d’objet est obligatoire. Elle ne doit pas inclure de sauts de ligne.

1. Cliquez sur le bouton **[!UICONTROL Modifier le corps de l’e-mail]** pour accéder au Concepteur d’e-mail et commencer à créer votre contenu. [En savoir plus](get-started-email-design.md)

   ![](assets/email_designer_edit_email_body.png)

1. Si vous êtes dans une campagne, vous pouvez également cliquer sur le bouton **[!UICONTROL Éditeur de code]** pour coder votre propre contenu en HTML brut à l’aide de la fenêtre pop-up qui s’affiche.

   ![](assets/email_designer_edit_code_editor.png)

   >[!NOTE]
   >
   >Si vous avez déjà créé ou importé du contenu par l’intermédiaire du concepteur d’e-mail, ce contenu s’affiche par HTML.

## Vérifier les alertes {#check-email-alerts}

Lorsque vous concevez vos messages, des alertes s’affichent dans l’interface (en haut à droite de l’écran) lorsque des paramètres clés sont manquants.

![](assets/email_journey_alerts_details.png)

>[!NOTE]
>
>Si ce bouton ne s’affiche pas, aucune alerte n’a été détectée.

Les paramètres et les éléments vérifiés par le système sont répertoriés ci-dessous. Vous trouverez également des informations sur la façon d’adapter votre configuration pour résoudre les problèmes correspondants.

Deux types d’alertes peuvent avoir lieu :

* Les **avertissements** se rapportent aux recommandations et aux bonnes pratiques telles que :

   * **[!UICONTROL Le lien d’opt-out ne figure pas dans le corps de l’e-mail]** : il est recommandé d’ajouter un lien d’exclusion dans le corps de votre e-mail. Découvrez comment configurer ce lien dans [cette section](../privacy/opt-out.md#opt-out-decision-management).

     >[!NOTE]
     >
     >Les e-mails de type marketing doivent inclure un lien de désinscription, qui n’est pas obligatoire pour les messages transactionnels. La catégorie du message (**[!UICONTROL Marketing]** ou **[!UICONTROL Transactionnel]**) est définie au niveau de la [configuration des canaux](email-settings.md#email-type) et au moment de la [création du message](#create-email-journey-campaign) d’un parcours ou d’une campagne.

   * **[!UICONTROL Version texte du contenu HTML vide]** : n’oubliez pas de définir une version texte du corps de votre e-mail, car elle sera utilisée lorsque le contenu HTML ne peut pas être affiché Découvrez comment créer cette version texte dans [cette section](text-version-email.md).

   * **[!UICONTROL Lien vide figurant dans le corps de l’email]** : vérifiez que tous les liens de votre email sont corrects. Découvrez comment gérer le contenu et les liens dans [cette section](content-from-scratch.md).

   * **[!UICONTROL La taille de l’email dépasse la limite de 100 Ko]** : pour une diffusion optimale, veillez à ce que la taille de votre email ne dépasse pas 100 Ko. Découvrez comment modifier le contenu des emails dans [cette section](content-from-scratch.md).

* Les **erreurs** vous empêchent de tester ou d’activer le parcours ou la campagne tant qu’elles ne sont pas corrigées, telles que :

   * **[!UICONTROL L’objet est manquant.]** : l’objet de l’e-mail est obligatoire. Découvrez comment définir et personnaliser ce champ dans [cette section](create-email.md).

  <!--HTML is empty when Amp HTML is present-->

   * **[!UICONTROL La version e-mail du message est vide.]** : cette erreur s’affiche lorsque le contenu de l’e-mail n’a pas été configuré. Découvrez comment concevoir le contenu des e-mails dans [cette section](get-started-email-design.md).

   * **[!UICONTROL La configuration n’existe pas]** : vous ne pouvez pas utiliser votre message si la configuration que vous avez sélectionnée est supprimée après la création du message. Si cette erreur se produit, sélectionnez une autre configuration dans les **[!UICONTROL Propriétés]** du message. En savoir plus sur les configurations des canaux dans [cette section](../configuration/channel-surfaces.md).

>[!CAUTION]
>
>Pour pouvoir tester ou activer le parcours/la campagne à l’aide de l’e-mail, vous devez résoudre toutes les alertes d’**erreurs**.

## Vérifier et envoyer votre e-mail

Une fois le contenu de votre message défini, vous pouvez utiliser des profils de test pour le prévisualiser, envoyer des BAT et contrôler son rendu pour les clients de bureau, mobiles et web populaires. Si vous avez inséré du contenu personnalisé, vous pouvez vérifier l’affichage de celui-ci dans le message à l’aide des données de profil de test.

Vous pouvez également valider la qualité de votre contenu pour en évaluer la lisibilité, l’efficacité et la cohésion. [En savoir plus sur la validation de la qualité du contenu](../content-management/brands-score.md#validate-quality)

>[!NOTE]
>
>En plus des profils de test, [!DNL Journey optimizer] vous permet également de tester différentes variantes de votre contenu en le prévisualisant et en envoyant des BAT à l’aide d’exemples de données d’entrée chargés à partir d’un fichier CSV/JSON ou ajoutés manuellement. [Découvrez comment simuler des variations de contenu.](../test-approve/simulate-sample-input.md)

Pour ce faire, cliquez sur **[!UICONTROL Simuler du contenu]**, puis ajoutez un profil de test pour vérifier votre message à l’aide des données de profil de test.

![](assets/email_designer_edit_simulate.png)

Vous trouverez des informations détaillées sur la sélection des profils de test et la prévisualisation de votre contenu dans la section [Gestion de contenu](../content-management/preview-test.md).

Une fois votre e-mail prêt, effectuez la configuration de votre [parcours](../building-journeys/journey-gs.md) ou [campagne](../campaigns/create-campaign.md) et activez-le pour envoyer le message.

>[!NOTE]
>
>Pour suivre le comportement de vos destinataires par le biais d’ouvertures d’e-mails et/ou d’interactions avec des e-mail,s assurez-vous que les options dédiées dans la section **[!UICONTROL Tracking]** sont activées dans l’[activité E-mail](../building-journeys/journey-action.md) du parcours ou dans la [campagne](../campaigns/create-campaign.md) par e-mail.<!--to move?-->

<!--

## Define your email content {#email-content}

Use [!DNL Journey Optimizer] Email Designer to [design your email from scratch](../email/content-from-scratch.md). If you have an existing content, you can [import it in the Email Designer](../email/existing-content.md), or [code your own content](../email/code-content.md) in [!DNL Journey Optimizer]. 

[!DNL Journey Optimizer] comes with a set of [built-in templates](email-templates.md) to help you start. Any email can also be saved as a template.

Use [!DNL Journey Optimizer] personalization editor to personalize your messages with profiles' data. For more on personalization, refer to [this section](../personalization/personalize.md).

Adapt the content of your messages to the targeted profiles by using [!DNL Journey Optimizer] dynamic content capabilities. [Get started with dynamic content](../personalization/get-started-dynamic-content.md)

## Email tracking {#email-tracking}

If you want to track the behavior of your recipients through openings and/or clicks on links, enable the following options: **[!UICONTROL Email opens]** and **[!UICONTROL Click on email]**. 

Learn more about tracking in [this section](message-tracking.md).

## Validate your email content {#email-content-validate}

Control the rendering of your email, and check personalization settings with test profiles, using the preview section on the left-hand side. For more on this, refer to [this section](preview.md).

![](assets/messages-simple-preview.png)

You must also check alerts in the upper section of the editor.  Some of them are simple warnings, but others can prevent you from using the message. 

-->

