---
solution: Journey Optimizer
product: journey optimizer
title: Création d’un SMS
description: Découvrez comment créer un message SMS dans Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 81ab92022329788c1feea24c7a621ef154d33422
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 86%

---

# Création d’un SMS {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Création d’un SMS"
>abstract="Ajoutez votre SMS et commencez à le personnaliser à l&#39;aide de l&#39;éditeur d&#39;expression."

## Ajouter un SMS {#create-sms-journey-campaign}

Accédez aux onglets ci-dessous pour savoir comment ajouter un SMS dans une campagne ou dans un parcours.

>[!BEGINTABS]

>[!TAB Ajouter un SMS à un parcours]

1. Ouvrez votre parcours, puis effectuez un glisser-déposer d’une activité SMS à partir du **Actions** de la palette.

   ![](assets/sms_create_1.png)

1. Fournissez des informations de base sur votre message (libellé, description, catégorie), puis choisissez la surface de message à utiliser.

   ![](assets/sms_create_2.png)

   Pour plus d’informations sur la configuration de votre parcours, consultez cette [page](../building-journeys/journey-gs.md).

Vous pouvez maintenant commencer à concevoir le contenu de votre SMS à partir du bouton **[!UICONTROL Modifier le contenu]**. [Définir le contenu de votre SMS](#sms-content)

>[!TAB Ajouter un SMS à une campagne]

1. Créez une campagne planifiée ou déclenchée par une API, sélectionnez **[!UICONTROL SMS]** comme action et choisissez la **[!UICONTROL surface d’application]** à utiliser. [En savoir plus sur la configuration des SMS](sms-configuration.md).

   ![](assets/sms_create_3.png)

1. Cliquez sur **[!UICONTROL Créer]**.

1. Dans la section **[!UICONTROL Propriétés]**, modifiez le **[!UICONTROL Titre]** et la **[!UICONTROL Description]** de votre campagne.

   ![](assets/sms_create_4.png)

1. Dans la section **[!UICONTROL Tracking des actions]**, indiquez si vous souhaitez effectuer le tracking des clics sur les liens de votre SMS.

1. Cliquez sur le bouton **[!UICONTROL Sélectionner une audience]** pour définir l’audience à cibler à partir de la liste des segments Adobe Experience Platform disponibles. [En savoir plus](../segment/about-segments.md).

1. Dans le champ **[!UICONTROL Espace de noms d’identité]**, choisissez l’espace de noms à utiliser pour identifier les personnes à partir du segment sélectionné. [En savoir plus](../event/about-creating.md#select-the-namespace).

   ![](assets/sms_create_5.png)

1. Les campagnes sont conçues pour être exécutées à une date spécifique ou à une fréquence récurrente. Découvrez comment configurer le **[!UICONTROL Planning]** de votre campagne dans [cette section](../campaigns/create-campaign.md#schedule).

1. Dans le menu **[!UICONTROL Déclencheurs d’action]**, choisissez la variable **[!UICONTROL Fréquence]** de votre SMS :

   * Une fois
   * Quotidien
   * Hebdomadaire
   * Mois

Vous pouvez maintenant commencer à concevoir le contenu de votre SMS à partir du bouton **[!UICONTROL Modifier le contenu]**. [Concevoir le contenu de votre SMS](#sms-content)

>[!ENDTABS]


## Définir le contenu de votre SMS{#sms-content}

1. Dans l’écran de configuration des parcours ou des campagnes, cliquez sur le bouton **[!UICONTROL Modifier le contenu]** pour configurer le contenu du SMS.

1. Cliquez sur le champ **[!UICONTROL Message]** pour ouvrir l’éditeur d’expression.

   ![](assets/sms-content.png)

1. Utilisez l’éditeur d’expression pour définir le contenu et ajouter du contenu dynamique. Vous pouvez utiliser n’importe quel attribut, comme le nom du profil ou la ville. En savoir plus sur la [personnalisation](../personalization/personalize.md) et le [contenu dynamique](../personalization/get-started-dynamic-content.md) dans l’éditeur d’expression.

1. Cliquez sur **[!UICONTROL Enregistrer]** et vérifiez votre message dans l’aperçu. [En savoir plus](send-sms.md)

   ![](assets/sms-content-preview.png)

>[!NOTE]
>
>Conformément aux normes et réglementations du secteur, tous les messages SMS de marketing doivent contenir un moyen permettant aux destinataires de se désabonner facilement. Pour ce faire, les destinataires de SMS peuvent répondre avec des mots-clés d’accord préalable et de droit d’opposition. [Découvrir comment gérer un droit d’opposition](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

**Rubriques connexes**

* [Configurer le canal SMS](sms-configuration.md)
* [Rapport SMS](../reports/journey-global-report.md#sms-global)
* [Ajouter un message dans un parcours](../building-journeys/journeys-message.md)
* [Ajouter un message dans une campagne](../campaigns/create-campaign.md)
