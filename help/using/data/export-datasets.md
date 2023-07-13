---
solution: Journey Optimizer
product: journey optimizer
title: Exporter des jeux de données vers des emplacements d’espace de stockage
description: Découvrez comment exporter vos jeux de données à l’aide des destinations d’espace de stockage d’Adobe Experience Platform.
role: User
level: Beginner
badge: label="Version bêta" type="Informative"
keywords: platform, lac de données, créer, lac, jeux de données, profil
exl-id: 66b5c691-ddc4-4e9b-9386-2ce6c307451c
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '579'
ht-degree: 93%

---

# Exporter des jeux de données vers des emplacements d’espace de stockage {#export-datasets}

>[!AVAILABILITY]
>
>La fonction d’exportation des jeux de données est actuellement en version bêta et disponible pour tous les utilisateurs et utilisatrices d’Adobe Journey Optimizer. Contactez votre représentant ou représentante Adobe pour obtenir l’accès aux destinations si vous n’y avez pas déjà accès.

Journey Optimizer vous permet d’établir une connexion active aux emplacements d’espace de stockage pour exporter le contenu de vos jeux de données.

En exportant régulièrement vos données, vous pouvez vous assurer d’avoir un enregistrement complet et à jour de vos interactions client, utiliser ces informations à des fins de création de rapports ou d’analyse et maintenir la conformité aux exigences légales.

## Destinations d’espace de stockage disponibles {#destinations}

Vous pouvez exporter des jeux de données vers 6 destinations d’espace de stockage accessibles à partir du menu **[!UICONTROL Destinations]**, dans l’onglet **[!UICONTROL Catalogue]**.

![](assets/dataset-export-setup.png)

>[!AVAILABILITY]
>
>Ces destinations sont toutes disponibles en version bêta et peuvent faire l’objet de modifications.

Des informations détaillées sur chaque destination sont disponibles dans la documentation Adobe Experience Platform :

* [Amazon S3](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/amazon-s3.html?lang=fr)
* [Azure Blob](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/azure-blob.html?lang=fr)
* [Azure Data Lake Gen2](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/adls-gen2.html?lang=fr)
* [Zone d’atterrissage des données](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/data-landing-zone.html?lang=fr)
* [Google Cloud Storage](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/google-cloud-storage.html?lang=fr)
* [SFTP](https://experienceleague.adobe.com/docs/experience-platform/destinations/catalog/cloud-storage/sftp.html?lang=fr)

## Conditions préalables {#prerequisites}

Vérifiez les conditions préalables suivantes avant de commencer à exporter vos jeux de données :

* Pour exporter des jeux de données, vous avez besoin des [autorisations de contrôle d’accès](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=fr#permissions) **Gérer les destinations**, **Afficher les destinations**, **Activer des destinations**, et **Gérer et activer des destinations de jeu de données**. Lisez la [présentation du contrôle d’accès](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/overview.html?lang=fr) ou contactez votre administrateur de produit pour obtenir les autorisations requises.

* Cette fonctionnalité prend uniquement en charge l’exportation des données de première génération, c’est-à-dire les données brutes définies dans la [description du produit Real-time Customer Data Platform](https://helpx.adobe.com/fr/legal/product-descriptions/real-time-customer-data-platform-b2c-edition-prime-and-ultimate-packages.html). Assurez-vous que le jeu de données que vous souhaitez exporter ne contient pas de données de deuxième génération.

## Étapes principales pour exporter des jeux de données {#main-steps}

Les principales étapes pour exporter un jeu de données vers un emplacement d’espace de stockage sont les suivantes :

![](assets/dataset-export-process.png)

Des informations détaillées sur chaque étape sont disponibles dans la documentation Adobe Experience Platform : [Exporter des jeux de données vers des destinations d’espace de stockage](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=fr).

1. **Configurez votre destination d’espace de stockage**. Si ce n’est pas déjà fait, connectez-vous à une destination d’espace de stockage à partir du catalogue des destinations. [Découvrez comment créer une connexion de destination](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/connect-destination.html?lang=fr#setup).

   <!--![](assets/dataset-export-setup.png)-->

1. **Sélectionnez la destination d’espace de stockage** où vous souhaitez exporter vos jeux de données. Dans le catalogue des destinations, cliquez sur le bouton **[!UICONTROL Exporter les jeux de données]** sur la vignette souhaitée et sélectionnez la connexion à utiliser.

   <!--![](assets/dataset-export-destination.png)-->

   >[!NOTE]
   >
   >Si vous utilisez Adobe Journey Optimizer avec des profils client en temps réel, les cartes de destination affichent un bouton &quot;Activer&quot;, ce qui vous permet à la fois d’exporter des jeux de données et d’activer des audiences pour cette destination, en fonction des autorisations que vous avez activées.

1. **Sélectionnez le ou les jeux de données** que vous souhaitez exporter vers la destination sélectionnée.

   <!--![](assets/dataset-export-dataset-selection.png)-->

1. **Planifiez l’exportation** de votre jeu de données. Indiquez à quel moment l’exportation doit commencer et à quelle fréquence elle doit se produire.

   <!--![](assets/dataset-export-schedule.png)-->

1. **Examinez et confirmez l’exportation** en vérifiant le résumé qui s’affiche à la fin de la configuration.

   <!--![](assets/dataset-export-review.png)-->

Une fois l’exportation terminée, le contenu de votre jeu de données est déposé dans votre emplacement d’espace de stockage selon le planning que vous avez configuré. [Découvrez comment vérifier la réussite de l’exportation d’un jeu de données](https://experienceleague.adobe.com/docs/experience-platform/destinations/ui/activate/export-datasets.html?lang=fr#verify).
