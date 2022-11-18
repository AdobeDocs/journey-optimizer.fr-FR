---
title: Créer un message de publipostage direct
description: Découvrez comment créer un message de publipostage direct dans Journey Optimizer.
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 6b438268-d983-4ab8-9276-c4b7de74e6bd
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '478'
ht-degree: 100%

---

# Créer un message de publipostage direct {#create-direct}

>[!CONTEXTUALHELP]
>id="ajo_direct_mail"
>title="Création de publipostage direct"
>abstract="Créez des messages de publipostage direct dans des campagnes planifiées et concevez les fichiers d’extraction requis par les fournisseurs de publipostage direct pour envoyer du courrier à votre clientèle."

Le publipostage direct est un canal hors ligne qui vous permet de personnaliser et de générer les fichiers d’extraction requis par les fournisseurs de publipostage direct pour envoyer du courrier à votre clientèle.

Lorsque vous créez un publipostage direct, Journey Optimizer génère un fichier contenant tous les profils ciblés et les données sélectionnées (adresse postale, attributs de profil, par exemple). Votre fournisseur de publipostage direct pourra alors récupérer ce fichier et s’occupera de l’envoi réel.

Les messages de publipostage direct ne peuvent être créés que dans le cadre de campagnes planifiées. Ils ne sont pas disponibles pour une utilisation dans des campagnes déclenchées par l’API ou dans des parcours.

>[!IMPORTANT]
>
>Avant d’envoyer un message de publipostage direct, assurez-vous d’avoir configuré les éléments suivants :
>
>1. Une [configuration du routage des fichiers](../configuration/direct-mail-configuration.md#file-routing-configuration) qui spécifie le serveur sur lequel le fichier d’extraction doit être téléchargé et stocké,
>1. Une [surface de message de publipostage direct](../configuration/direct-mail-configuration.md#direct-mail-surface) qui fera référence à la configuration du routage des fichiers.


## Création de votre message de publipostage direct {#create}

Les étapes de création et d’envoi d’un message de publipostage direct sont les suivantes :

1. Créez une campagne planifiée, puis sélectionnez **[!UICONTROL Publipostage direct]** comme action et choisissez la surface du canal à utiliser. [Découvrez comment créer une surface de publipostage direct.](../configuration/direct-mail-configuration.md#direct-mail-surface)

   ![](assets/direct-mail-campaign.png)

1. Cliquez sur **[!UICONTROL Créer]**, puis définissez des informations de base sur votre campagne (nom, description). [Découvrez comment configurer une campagne.](../campaigns/create-campaign.md)

   ![](assets/direct-mail-edit.png)

1. Cliquez sur le bouton **[!UICONTROL Modifier le contenu]** pour configurer le fichier d’extraction à envoyer à votre fournisseur de publipostage direct.

1. Définissez le nom du fichier d’extraction dans le champ **[!UICONTROL Nom de fichier]**.

   Il peut parfois s’avérer nécessaire d’ajouter des informations au début ou à la fin du fichier d’extraction. Pour ce faire, utilisez le champ **[!UICONTROL Notes]**, puis indiquez si vous souhaitez inclure la note en tant qu’en-tête ou pied de page.

   <!--Click on the button to the right of the Output file field and enter the desired label. You can use personalization fields, content blocks and dynamic text (see Defining content). For example, you can complete the label with the delivery ID or the extraction date.-->

   ![](assets/direct-mail-properties.png)

1. Utilisez la zone de gauche pour définir les informations à afficher en colonnes dans le fichier d’extraction :

   1. Cliquez sur le bouton **[!UICONTROL Ajouter]** pour ajouter une nouvelle colonne, puis sélectionnez-la dans la liste.

   1. Dans la section **[!UICONTROL Formatage]**, indiquez un libellé pour la colonne, puis définissez les attributs de profil à afficher à l’aide de l’[Éditeur d’expression](../personalization/personalization-build-expressions.md).

      ![](assets/direct-mail-content.png)

   1. Pour trier le fichier d’extraction à l’aide de la colonne sélectionnée, activez l’option **[!UICONTROL Trier par]**. L’icône **[!UICONTROL Trier par]** s’affiche alors à côté du libellé de la colonne dans la structure du fichier.

1. Répétez ces étapes pour ajouter autant de colonnes que nécessaire pour créer votre fichier d’extraction. Vous pouvez ajouter jusqu’à 50 colonnes.

   ![](assets/direct-mail-complete.png)

   Vous pouvez supprimer une colonne à tout moment en la sélectionnant et en cliquant sur le bouton **[!UICONTROL Supprimer]** à partir de la section **[!UICONTROL Formatage]**.

1. Une fois le contenu du publipostage direct défini, terminez la configuration de votre campagne.

   Lorsque la campagne démarrera, le fichier d’extraction sera automatiquement généré et exporté vers le serveur spécifié dans votre [configuration du routage des fichiers](../configuration/direct-mail-configuration.md).
