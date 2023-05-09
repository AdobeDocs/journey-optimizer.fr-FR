---
solution: Journey Optimizer
product: journey optimizer
title: Conception d'e-mails
description: Découvrez comment concevoir vos e-mails
feature: Overview
topic: Content Management
role: User
level: Intermediate
keywords: e-mail, conception, stock, ressources
exl-id: e4f91870-f06a-4cd3-98b7-4c413233e310
source-git-commit: 3a9b11b1a4d2159261586394f1595e52c8b749e7
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 100%

---

# Prise en main de la conception d’e-mails {#get-started-content-design}

Vous pouvez importer du contenu existant dans [!DNL Journey Optimizer] ou tirer parti des fonctionnalités de conception de contenu :

* Tirez parti des **fonctionnalités de conception d’e-mail** [!DNL Journey Optimizer] pour créer ou importer des e-mails réactifs. [En savoir plus](content-from-scratch.md)

* Utiliser **Adobe Experience Manager Assets Essentials** pour enrichir vos e-mails, créer et gérer votre propre base de données de ressources. [En savoir plus](assets-essentials.md)

* Rechercher des **photos Adobe Stock** pour créer votre contenu et améliorer votre conception d’e-mail. [En savoir plus](stock.md)

* Améliorez l’expérience des clients en créant des messages dynamiques personnalisés en fonction de leurs attributs de profil. En savoir plus sur [Personnalisation](../personalization/personalize.md) et [Contenu dynamique](../personalization/get-started-dynamic-content.md).

➡️ [Découvrez cette fonctionnalité en vidéo](#video)

## Bonnes pratiques en matière de conception d’e-mail {#best-practices}

Lors de l’envoi d’e-mails, n’oubliez pas que les destinataires peuvent les transférer, ce qui peut parfois entraîner des problèmes de rendu. Ceci est particulièrement vrai lors de l’utilisation de classes CSS qui peuvent ne pas être prises en charge par le fournisseur de messagerie utilisé pour le transfert, notamment si vous utilisez la classe « CSS is-desktop-hidden » pour masquer une image sur les périphériques mobiles.

Pour minimiser ces problèmes de rendu, nous vous recommandons de garder votre structure de conception d’e-mail aussi simple que possible. Essayez d’utiliser une conception unique qui fonctionne aussi bien pour les ordinateurs de bureau et les appareils mobiles, et évitez d’utiliser des classes CSS complexes ou d’autres éléments de conception qui ne sont pas entièrement pris en charge par tous les clients de messagerie. En suivant ces bonnes pratiques, vous aurez l’assurance que vos e-mails sont correctement rendus, quelle que soit la manière dont ils sont affichés ou transférés par les destinataires.

## Étapes clés de création de contenu d’e-mail {#key-steps}

Une fois que vous avez [ajouté un e-mail](create-email.md) dans un parcours ou une campagne, vous pouvez commencer à créer le contenu de votre e-mail.

1. Dans l’écran de configuration des parcours ou des campagnes, parcourez l’écran **[!UICONTROL Modifier le contenu]** pour accéder au Concepteur d’e-mail. [En savoir plus](create-email.md#define-email-content)

   ![](assets/email_designer_edit_email_body.png)

1. Dans la page d’accueil du Concepteur d’e-mail, choisissez la manière de concevoir votre e-mail à l’aide des options suivantes :

   * **Concevez vos e-mails en partant de zéro** dans l’interface du Concepteur d’e-mail et tirez parti des images provenant d’[Adobe Experience Manager Assets Essentials](assets-essentials.md). Découvrez comment concevoir le contenu des e-mails dans [cette section](content-from-scratch.md).

   * **Codez ou collez du code HTML brut** directement dans le concepteur d’email. Découvrez comment coder votre propre contenu dans [cette section](code-content.md).

      >[!NOTE]
      >
      >Dans une campagne, vous pouvez également sélectionner le bouton **[!UICONTROL Éditeur de code]** à partir de l’écran **[!UICONTROL Modifier le contenu]** écran. [En savoir plus](create-email.md#define-email-content)

   * **Importez du contenu HTML existant** à partir d’un fichier ou d’un dossier .zip. Découvrez comment importer un contenu d’e-mail dans [cette section](existing-content.md).

   * **Sélectionnez un contenu existant** à partir d’une liste de modèles intégrés ou personnalisés. Découvrez comment utiliser des modèles d’e-mail dans [cette section](email-templates.md).

   ![](assets/email_designer_create_options.png)

1. Une fois que le contenu de votre e-mail a été défini et personnalisé, vous pouvez exporter votre contenu pour le valider ou pour l’utiliser ultérieurement. Cliquez sur **[!UICONTROL Exporter le HTML]** pour enregistrer sur votre ordinateur un fichier zip qui contiendra votre HTML et vos ressources.

   ![](assets/email_designer_export.png)

## Vidéo pratique {#video}

Découvrez comment créer du contenu d&#39;e-mail avec l&#39;éditeur de messages.

>[!VIDEO](https://video.tv.adobe.com/v/334150?quality=12)