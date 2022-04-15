---
title: Prise en main des jeux de données
description: Découvrez comment utiliser des jeux de données Adobe Experience Platform dans Adobe Journey Optimizer
role: User
level: Beginner
exl-id: dcdd3c81-0f00-4259-a8a5-9062a4c40b6f
source-git-commit: 9ebcfd6c41c17fe3be0423822209443fc55244a7
workflow-type: tm+mt
source-wordcount: '430'
ht-degree: 55%

---

# Prise en main des jeux de données {#datasets-gs}

Toutes les données correctement ingérées par Adobe Experience Platform sont conservées sous forme de jeux de données dans le lac de données. Un jeu de données est une structure de stockage et de gestion pour la collecte de données, généralement sous la forme d&#39;un tableau, qui contient un schéma (des colonnes) et des champs (des lignes).

## Accès aux jeux de données{#access-datasets}

Le **Jeux de données** espace de travail dans [!DNL Adobe Journey Optimizer] l’interface utilisateur vous permet d’explorer les données et de créer des jeux de données.

Sélectionner **Jeux de données** dans le volet de navigation de gauche pour ouvrir le tableau de bord Jeux de données .

![](assets/datasets-home.png)

L’ajout de données à Adobe Experience Platform est la base de la création d’un profil. Vous pouvez ensuite exploiter les profils dans [!DNL Adobe Journey Optimizer]. Commencez par définir des schémas, utilisez les outils ETL pour préparer et normaliser vos données, puis créez des jeux de données basés sur vos schémas.

Sélectionnez la **Parcourir** pour afficher la liste de tous les jeux de données disponibles pour votre organisation. Des détails s’affichent pour chaque jeu de données répertorié, notamment son nom, le schéma auquel le jeu de données adhère et l’état de l’exécution d’ingestion la plus récente.

Par défaut, seuls les jeux de données que vous avez ingérés s’affichent. Si vous souhaitez afficher les jeux de données générés par le système, activez la variable **Affichage des jeux de données système** bascule à partir du filtre.

![](assets/ajo-system-datasets.png)

Sélectionnez le nom d’un jeu de données pour accéder à son écran Activité du jeu de données et afficher les détails du jeu de données que vous avez sélectionné. L’onglet activité contient un graphique qui permet de visualiser le taux de messages consommé ainsi qu’une liste des lots réussis et en échec.

## Création de jeux de données{#create-datasets}

Pour créer un jeu de données, commencez par sélectionner **Création d’un jeu de données** dans le tableau de bord Jeux de données .

Vous pouvez :

* Créer un jeu de données à partir d’un schéma. [En savoir plus dans cette documentation](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#schema){target=&quot;_blank&quot;}
* Créer un jeu de données à partir d’un fichier CSV. [En savoir plus dans cette documentation](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html?lang=fr){target=&quot;_blank&quot;}


Regardez cette vidéo pour savoir comment créer un jeu de données, le mapper à un schéma, y ajouter des données et confirmer que les données ont été ingérées.

>[!VIDEO](https://video.tv.adobe.com/v/334293?quality=12)


Découvrez comment créer un schéma, un jeu de données et ingérer des données pour ajouter des profils de test dans Adobe Journey Optimizer dans [cet exemple de bout en bout](../segment/creating-test-profiles.md)

En savoir plus sur la création de jeux de données dans [Documentation Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=fr){target=&quot;_blank&quot;}.

Découvrez comment utiliser l’interface utilisateur des jeux de données dans la [documentation de présentation de l’ingestion des données](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=fr){target=&quot;_blank&quot;}.


**Voir également**

* [Création d’un schéma, d’un jeu de données et ingestion des données pour ajouter des profils de test dans Journey Optimizer](../segment/creating-test-profiles.md)
* [Présentation de l’ingestion par flux](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=fr){target=&quot;_blank&quot;}
* [Ingestion de données dans Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html?lang=fr){target=&quot;_blank&quot;}
