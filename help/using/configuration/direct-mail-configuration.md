---
title: Configuration du courrier
description: Découvrez comment configurer le canal courrier dans Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: ef66b30870fabf882bd368294e8a3b388d7ec182
workflow-type: tm+mt
source-wordcount: '825'
ht-degree: 1%

---

# Configuration du courrier {#direct-mail-configuration}

[!DNL Journey Optimizer] vous permet de personnaliser et de générer les fichiers requis par les opérateurs de services postaux pour envoyer du courrier à vos clients.

Lorsque vous préparez une diffusion courrier, [!DNL Journey Optimizer] génère un fichier contenant tous les profils ciblés et les coordonnées de contact sélectionnées (adresse postale, par exemple). Vous pourrez alors envoyer ce fichier à votre opérateur de services postaux qui prendra en charge l&#39;envoi réel.

Pour envoyer un courrier, vous devez créer un fichier et le charger sur un serveur. Avant de pouvoir le faire, vous devez créer une [configuration du routage des fichiers](#file-routing-configuration) et un [surface courrier](#direct-mail-surface) qui fera référence à la configuration de routage des fichiers.

## Configuration du routage des fichiers {#file-routing-configuration}

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details"
>title="Définition des paramètres de la configuration de routage des fichiers"
>abstract="Lors de la création du courrier, vous allez générer le fichier contenant toutes les informations de profil requises. Ce fichier doit être exporté et téléchargé sur un serveur afin que votre opérateur de services postaux puisse accéder à ce fichier et l&#39;utiliser pour diffuser du courrier."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_details_header"
>title="Définition des paramètres de la configuration de routage des fichiers"
>abstract="Vous devez définir l&#39;endroit où le fichier sera exporté et téléchargé pour que votre opérateur de services postaux puisse l&#39;utiliser."

>[!CONTEXTUALHELP]
>id="ajo_dm_select_file_routing"
>title="Configuration du routage des fichiers"
>abstract="Sélectionnez la configuration de routage des fichiers de votre choix, qui définit l&#39;endroit où le fichier sera exporté et téléchargé pour que votre opérateur de services postaux l&#39;utilise."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_type"
>title="Sélectionnez le type de serveur pour votre routage de fichiers."
>abstract="Sélectionnez le serveur à utiliser pour le téléchargement et le stockage des fichiers de courrier. Actuellement, seuls Amazon S3 et SFTP sont pris en charge."

>[!CONTEXTUALHELP]
>id="ajo_dm_file_routing_aws_region"
>title="Choisissez la région AWS"
>abstract="Sélectionnez la région géographique dans laquelle vous souhaitez exporter et charger vos fichiers de courrier. Pour une utilisation optimale, il est recommandé de choisir la région la plus proche pour héberger votre infrastructure cloud."

1. Accédez au **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Configuration du routage des fichiers]** > **[!UICONTROL Routage de fichier]** , puis cliquez sur **[!UICONTROL Création d’une configuration de routage]**.

   ![](assets/file-routing-config-button.png)

1. Attribuez un nom à votre configuration.

1. Sélectionner la configuration **[!UICONTROL Type de serveur]**, c’est-à-dire le serveur que vous souhaitez utiliser pour charger et stocker les fichiers de courrier.

   ![](assets/file-routing-config-type.png)

   >[!NOTE]
   >
   >Actuellement, seuls Amazon S3 et SFTP sont disponibles.

   Lors de la création du courrier, vous allez générer le fichier contenant toutes les informations de profil requises. Ce fichier doit être exporté et téléchargé sur un serveur afin que votre opérateur de services postaux puisse accéder à ce fichier et l&#39;utiliser pour diffuser du courrier.

1. Renseignez les détails et les informations d’identification spécifiques au type de configuration sélectionné, telles que l’adresse du serveur, la clé d’accès, etc.

   ![](assets/file-routing-config-sftp-details.png)

1. Si vous avez sélectionné **[!UICONTROL Amazon S3]**, vous pouvez choisir la région AWS dans laquelle vous souhaitez exporter et charger vos fichiers de courrier.

   ![](assets/file-routing-config-aws-region.png)

   >[!NOTE]
   >
   >Les régions d’AWS sont des zones géographiques distinctes réparties dans le monde et utilisées par AWS pour héberger son infrastructure. Pour une utilisation optimale, il est recommandé de choisir la région la plus proche pour héberger votre infrastructure cloud.

1. Sélectionnez **[!UICONTROL Envoyer]**. La configuration de routage des fichiers est créée avec l’événement **[!UICONTROL Principal]** statut. Il est maintenant prêt à être utilisé dans une surface de courrier pour diffuser du courrier à partir de [!DNL Journey Optimizer].

   >[!NOTE]
   >
   >Vous pouvez également sélectionner **[!UICONTROL Enregistrer en tant que brouillon]** pour créer la configuration de routage des fichiers, mais vous ne pourrez pas la sélectionner en surface tant qu&#39;elle n&#39;est pas **[!UICONTROL Principal]**.

## Créer une surface de courrier {#direct-mail-surface}

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_settings"
>title="Définition des paramètres du courrier"
>abstract="Une surface de courrier contient les paramètres liés au formatage du fichier contenant les données de profil pour le courrier. Vous devez également définir l’endroit où le fichier sera exporté en sélectionnant la configuration de routage du fichier."

<!--
>[!CONTEXTUALHELP]
>id="ajo_dm_surface_sort"
>title="Define the sort order"
>abstract="If you select this option, the sort will be by profile ID, ascending or descending. If you unselect it, the sorting configuration defined when creating the direct mail message within a journey or a campaign."-->

>[!CONTEXTUALHELP]
>id="ajo_dm_surface_split"
>title="Définition du seuil de partage de fichiers"
>abstract="Vous devez définir le nombre maximal d’enregistrements pour chaque fichier contenant les données de profil. Une fois le seuil spécifié atteint, un autre fichier sera créé pour les enregistrements restants."

Une fois le routage des fichiers configuré, vous devez créer une surface de canal pour pouvoir diffuser du courrier à partir de [!DNL Journey Optimizer]. Dans chaque surface, vous devez sélectionner une configuration de routage de fichiers.

1. Création d’une surface de canal. [En savoir plus](channel-surfaces.md)

1. Sélectionnez la **[!UICONTROL Canal Courrier]** canal.

   ![](assets/surface-direct-mail-channel.png)

1. Définissez les paramètres du courrier dans la section dédiée de la configuration de la surface du canal.

   ![](assets/surface-direct-mail-settings.png)

1. Sélectionnez le format du fichier : **[!UICONTROL CSV]** ou **[!UICONTROL Texte délimité]**.

1. Dans le **[!UICONTROL Insertion]** , vous pouvez choisir de supprimer automatiquement les lignes en double.

1. Définissez le nombre maximum d&#39;enregistrements (c&#39;est-à-dire des lignes) pour chaque fichier contenant les données de profil. Une fois le seuil spécifié atteint, un autre fichier sera créé pour les enregistrements restants.

   ![](assets/surface-direct-mail-split.png)

   Par exemple, si le fichier contient 100 000 enregistrements et que la limite de seuil est fixée à 60 000, les enregistrements seront divisés en deux fichiers. Le premier fichier contiendra 60 000 lignes et le second les 40 000 lignes restantes.

   >[!NOTE]
   >
   >Vous pouvez définir un nombre compris entre 1 et 200 000 enregistrements, ce qui signifie que chaque fichier doit contenir au moins 1 ligne et pas plus de 200 000 lignes.

1. Enfin, sélectionnez l’option **[!UICONTROL Configuration du routage des fichiers]** parmi celles que vous avez créées. Cela définit l’endroit où le fichier sera exporté et téléchargé pour que votre opérateur de services postaux l’utilise.

   >[!CAUTION]
   >
   >Si vous n&#39;avez configuré aucune option de routage de fichier, vous ne pourrez pas créer de surface de courrier. [En savoir plus](#file-routing-configuration)

   ![](assets/surface-direct-mail-file-routing.png)