---
solution: Journey Optimizer
product: journey optimizer
title: Création d’un SMS
description: Découvrez comment créer un message SMS dans Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: 1f88626a-b491-4b36-8e3f-57f2b7567dd0
source-git-commit: 03c714833930511fa734662b637d2416728073c2
workflow-type: tm+mt
source-wordcount: '646'
ht-degree: 97%

---

# Création d’un SMS {#create-sms}

>[!CONTEXTUALHELP]
>id="ajo_message_sms"
>title="Créer un SMS"
>abstract="Ajoutez votre SMS et commencez à le personnaliser à l’aide de l’éditeur d’expression."

## Ajouter un SMS {#create-sms-journey-campaign}

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

## Définir le contenu de votre SMS{#sms-content}

>[!CONTEXTUALHELP]
>id="ajo_message_sms_content"
>title="Définir le contenu de votre SMS"
>abstract="Personnalisez et personnalisez vos SMS à l&#39;aide de l&#39;éditeur d&#39;expression pour définir le contenu et incorporer des éléments dynamiques."

1. Dans l’écran de configuration des parcours ou des campagnes, cliquez sur le bouton **[!UICONTROL Modifier le contenu]** pour configurer le contenu du SMS.

1. Cliquez sur le champ **[!UICONTROL Message]** pour ouvrir l’éditeur d’expression.

   ![](assets/sms-content.png)

1. Utilisez l’éditeur d’expression pour définir le contenu et ajouter du contenu dynamique. Vous pouvez utiliser n’importe quel attribut, comme le nom du profil ou la ville. En savoir plus sur la [personnalisation](../personalization/personalize.md) et le [contenu dynamique](../personalization/get-started-dynamic-content.md) dans l’éditeur d’expression.

1. Une fois le contenu défini, ajoutez les URL de suivi à votre message. Pour ce faire, accédez au menu **[!UICONTROL Fonctions d’assistance]** et sélectionnez **[!UICONTROL Helpers]**.

   Notez que pour utiliser la fonction de raccourcissement des URL, vous devez d’abord configurer un sous-domaine, qui sera ensuite lié à votre surface. [En savoir plus](sms-subdomains.md).

   >[!CAUTION]
   >
   > Pour accéder aux sous-domaines SMS et les modifier, vous devez disposer de l’autorisation **[!UICONTROL Gestion des sous-domaines SMS]** dans le sandbox de production.

   ![](assets/sms_tracking_1.png)

1. Dans le menu **[!UICONTROL Fonctions d’assistance]**, cliquez sur **[!UICONTROL Fonction URL]**, puis sélectionnez **[!UICONTROL Ajouter une URL]**.

   ![](assets/sms_tracking_2.png)

1. Dans le champ `originalUrl`, collez l’URL à raccourcir.

1. Cliquez sur **[!UICONTROL Enregistrer]** et vérifiez votre message dans l’aperçu. Choisissez l’option **[!UICONTROL Simuler le contenu]** pour prévisualiser vos URL raccourcies ou votre contenu personnalisé.

   ![](assets/sms-content-preview.png)

Vous pouvez maintenant tester et envoyer votre SMS à votre audience. [En savoir plus](send-sms.md).
Après leur envoi, vous pouvez mesurer l’impact de vos SMS dans les rapports Campaign ou Journey. Pour plus d’informations sur le reporting, consultez [cette section](../reports/campaign-global-report.md#sms-tab).

>[!NOTE]
>
>Conformément aux normes et réglementations du secteur, tous les messages SMS de marketing doivent contenir un moyen permettant aux destinataires de se désabonner facilement. Pour ce faire, les destinataires de SMS peuvent répondre avec des mots-clés d’accord préalable et de droit d’opposition. [Découvrir comment gérer un droit d’opposition](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

**Rubriques connexes**

* [Prévisualiser, tester et envoyer votre SMS](send-sms.md)
* [Configurer le canal SMS](sms-configuration.md)
* [Rapport SMS](../reports/journey-global-report.md#sms-global)
* [Ajouter un message dans un parcours](../building-journeys/journeys-message.md)
* [Ajouter un message dans une campagne](../campaigns/create-campaign.md)
