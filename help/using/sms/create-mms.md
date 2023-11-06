---
solution: Journey Optimizer
product: journey optimizer
title: Créer un MMS
description: Découvrez comment créer un MMS dans Journey Optimizer.
feature: SMS
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 38defa47-9b33-43a3-9b3e-d3aa4cb2857f
source-git-commit: feae2cb9d0bed35f12eb117cf2969c9290ebc06f
workflow-type: tm+mt
source-wordcount: '1093'
ht-degree: 100%

---

# Créer un MMS {#create-mms}

## Conditions préalables{#sms-prerequisites}

Avant de créer votre SMS, vous devez d’abord configurer votre fournisseur de SMS avec Journey Optimizer. Procédez comme suit :

* Avant d’envoyer des SMS, vous devez intégrer les paramètres du fournisseur à Journey Optimizer.

+++ Découvrez comment créer des informations d’identification d’API MMS Sinch.

   1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** et sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]**. Cliquez sur le bouton **[!UICONTROL Créer des informations d’identification de l’API]**.

      ![](assets/sms_6.png)

   1. Configurez vos informations dʼidentification pour lʼAPI SMS :

   * Pour **[!DNL Sinch MMS]** :

      * **[!UICONTROL Nom]** : choisissez un nom pour vos informations d’identification d’API.

      * **[!UICONTROL ID de projet]**, **[!UICONTROL ID de l’application]** et **[!UICONTROL jeton API]** : dans le menu API de conversation, vous trouverez vos informations d’identification dans le menu Application.  [En savoir plus](https://docs.cc.sinch.com/cloud/service-configuration/en/oxy_ex-1/common/wln1620131604643.html).

     ![](assets/mms_provider.png)

   1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification API.

  Après avoir créé et configuré vos informations d’identification API, vous devez maintenant créer une surface de canal (c’est-à-dire un préréglage de message) pour les messages SMS.

+++

* Une fois cette opération terminée, vous devrez créer une surface SMS. Ces étapes doivent être exécutées par un Administrateur système Adobe Journey Optimizer.

+++ Découvrez comment créer votre surface de canal.

   1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** et sélectionnez **[!UICONTROL Branding]** > **[!UICONTROL Surfaces de canal]**. Cliquez sur le bouton **[!UICONTROL Créer une surface de canal]**.

      ![](assets/preset-create.png)

   1. Saisissez un nom et une description (facultatif) pour la surface, puis sélectionnez le canal SMS.

      ![](assets/sms-create-surface.png)

      >[!NOTE]
      >
      > Les noms doivent commencer par une lettre (A-Z). Ils ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser le trait de soulignement `_`, le point`.` et le trait d&#39;union `-`.

   1. Définissez les **paramètres SMS**.

      ![](assets/sms-surface-settings.png)

      Sélectionnez le **[!UICONTROL Type de SMS]** qui sera envoyé avec la surface : **[!UICONTROL Transactionnel]** ou **[!UICONTROL Marketing]**.

      * Choisissez **Marketing** pour les SMS promotionnels : ces messages nécessitent le consentement de l’utilisateur ou de l’utilisatrice.
      * Choisissez **Transactionnel** pour les messages non commerciaux tels que la confirmation de commande, les notifications de réinitialisation de mot de passe ou les informations de diffusion, par exemple.

      Lors de la création d’un SMS, vous devez choisir une surface de canal valide correspondant à la catégorie que vous avez sélectionnée pour votre message.

      >[!CAUTION]
      >
      >Les SMS **transactionnels** peuvent être envoyés aux profils qui se sont désabonnés des communications marketing. Ces messages ne peuvent être envoyés que dans des contextes spécifiques.

   1. Sélectionnez la **[!UICONTROL Configuration SMS]** à associer à la surface.

      Pour plus dʼinformations sur la configuration de votre environnement pour envoyer des messages SMS, consultez [cette section](#create-api).

   1. Saisissez le **[!UICONTROL Numéro dʼexpéditeur]** à utiliser lors de vos communications.

   1. Sélectionnez votre **[!UICONTROL Champ d’exécution SMS]** pour sélectionner l’**[!UICONTROL Attribut de profil]** associé aux numéros de téléphone des profils.

   1. Si vous souhaitez utiliser la fonction de raccourcissement des URL dans vos SMS, sélectionnez un élément de la liste **[!UICONTROL Sous-domaine]**.

      >[!NOTE]
      >
      >Avant de pouvoir sélectionner un sous-domaine, vous devez avoir configuré au moins un sous-domaine SMS. [Voici comment procéder.](sms-subdomains.md)

   1. Saisissez le **[!UICONTROL numéro d’opt-out]** que vous voulez utiliser pour cette surface. Lorsque les profils décident de ne plus recevoir de messages depuis ce numéro, vous pouvez toujours leur en envoyer à partir d’autres numéros que vous pouvez utiliser pour envoyer des SMS avec [!DNL Journey Optimizer].

      >[!NOTE]
      >
      >Dans [!DNL Journey Optimizer], la désinscription aux SMS n’est plus gérée au niveau du canal. Elle est désormais spécifique à un numéro.

   1. Une fois tous les paramètres configurés, cliquez sur **[!UICONTROL Envoyer]** pour confirmer. Vous pouvez également enregistrer la surface de canal en tant que brouillon et reprendre sa configuration ultérieurement.

      ![](assets/sms-submit-surface.png)

   1. Une fois la surface de canal créée, elle s&#39;affiche dans la liste avec le statut **[!UICONTROL Traitement]**.

      >[!NOTE]
      >
      >Si les vérifications ne réussissent pas, découvrez les raisons possibles de l’échec dans [cette section](#monitor-channel-surfaces).

   1. Une fois les vérifications effectuées, la surface de canal obtient le statut **[!UICONTROL Actif]**. Elle est prête à être utilisée pour diffuser des messages.

      ![](assets/preset-active.png)


## Créer un SMS {#create-sms-journey-campaign}

Accédez aux onglets ci-dessous pour savoir comment ajouter un SMS dans une campagne ou un parcours.

>[!BEGINTABS]

>[!TAB Ajouter un SMS à un parcours]

1. Ouvrez votre parcours, puis effectuez un glisser-déposer d’une activité SMS depuis la section **Actions** de la palette.

   ![](assets/sms_create_1.png)

1. Fournissez des informations de base sur votre message (libellé, description, catégorie), puis choisissez la surface de message à utiliser.

   ![](assets/sms_create_2.png)

   Pour plus d’informations sur la configuration de votre parcours, consultez cette [page](../building-journeys/journey-gs.md).

   Par défaut, le champ **[!UICONTROL Surface]** est prérempli avec la dernière surface utilisée par l’utilisateur ou l’utilisatrice pour ce canal.

Vous pouvez maintenant commencer à concevoir le contenu de votre SMS à partir du bouton **[!UICONTROL Modifier le contenu]**. [Définir le contenu de votre SMS](#sms-content)

>[!TAB Ajouter un SMS à une campagne]

1. Créez une campagne planifiée ou déclenchée par une API, sélectionnez **[!UICONTROL SMS]** comme action et choisissez la **[!UICONTROL surface d’application]** à utiliser. [En savoir plus sur la configuration des SMS](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. Cliquez sur **[!UICONTROL Créer]**.

1. Dans la section **[!UICONTROL Propriétés]**, modifiez le **[!UICONTROL Titre]** et la **[!UICONTROL Description]** de votre campagne.

   ![](assets/sms_create_4.png)

1. Cliquez sur le bouton **[!UICONTROL Sélectionner une audience]** pour définir l’audience à cibler à partir de la liste des audiences Adobe Experience Platform disponibles. [En savoir plus](../audience/about-audiences.md).

1. Dans le champ **[!UICONTROL Espace de noms d’identité]**, choisissez l’espace de noms à utiliser pour identifier les personnes à partir de l’audience sélectionnée. [En savoir plus](../event/about-creating.md#select-the-namespace).

   ![](assets/sms_create_5.png)

1. Cliquez sur **[!UICONTROL Créer une expérience]** pour commencer à configurer votre expérience de contenu et créer des traitements afin de mesurer leurs performances et d’identifier la meilleure option pour votre audience cible. [En savoir plus](../campaigns/content-experiment.md).

1. Dans la section **[!UICONTROL Tracking des actions]**, indiquez si vous souhaitez effectuer le tracking des clics sur les liens de votre SMS.

1. Les campagnes sont conçues pour être exécutées à une date spécifique ou à une fréquence récurrente. Découvrez comment configurer le **[!UICONTROL Planning]** de votre campagne dans [cette section](../campaigns/create-campaign.md#schedule).

1. Dans le menu **[!UICONTROL Déclencheurs d’action]**, choisissez la variable **[!UICONTROL Fréquence]** de votre SMS :

   * Une fois
   * Quotidien
   * Hebdomadaire
   * Mois

Vous pouvez maintenant commencer à concevoir le contenu de votre SMS à partir du bouton **[!UICONTROL Modifier le contenu]**. [Concevoir le contenu de votre SMS](#sms-content)

>[!ENDTABS]

## Définir le contenu de votre MMS{#mms-content}

1. Dans l’écran de configuration des parcours ou des campagnes, cliquez sur le bouton **[!UICONTROL Modifier le contenu]** pour configurer le contenu du SMS.

1. Cliquez sur le champ **[!UICONTROL Message]** pour ouvrir l’éditeur d’expression.

   ![](assets/sms-content.png)

1. Utilisez l’éditeur d’expression pour définir le contenu et ajouter du contenu dynamique. Vous pouvez utiliser n’importe quel attribut, comme le nom du profil ou la ville. En savoir plus sur la [personnalisation](../personalization/personalize.md) et le [contenu dynamique](../personalization/get-started-dynamic-content.md) dans l’éditeur d’expression.

1. Activez l’option MMS pour ajouter un média à votre contenu SMS.

   >[!NOTE]
   >
   > L’option MMS n’est disponible qu’avec Sinch. Vous devez créer des informations d’identification d’API spécifiques pour créer un MMS. [En savoir plus](sms-configuration.md#create-new-api)

   ![](assets/sms_create_6.png)

1. Ajoutez un **[!UICONTROL Titre]** à votre média.

1. Saisissez lʼURL de votre média dans le champ **[!UICONTROL Média]**.

   ![](assets/sms_create_7.png)

1. Cliquez sur **[!UICONTROL Enregistrer]** et vérifiez votre message dans l’aperçu. Choisissez l’option **[!UICONTROL Simuler le contenu]** pour prévisualiser vos URL raccourcies ou votre contenu personnalisé.

Vous pouvez maintenant tester et envoyer votre SMS à votre audience. [En savoir plus](send-sms.md).
Après leur envoi, vous pouvez mesurer l’impact de vos SMS dans les rapports Campaign ou Journey. Pour plus d’informations sur le reporting, consultez [cette section](../reports/campaign-global-report.md#sms-tab).

>[!NOTE]
>
>Conformément aux normes et réglementations du secteur, tous les messages SMS de marketing doivent contenir un moyen permettant aux destinataires de se désabonner facilement. Pour ce faire, les destinataires de SMS peuvent répondre avec des mots-clés d’accord préalable et de droit d’opposition. [Découvrir comment gérer un droit d’opposition](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

**Rubriques connexes**

* [Prévisualiser, tester et envoyer votre SMS](send-sms.md)
* [Configurer le canal SMS](sms-configuration.md)
* [Rapport SMS](../reports/journey-global-report.md#sms-global)
