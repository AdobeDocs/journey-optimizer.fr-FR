---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main des jeux de données
description: Découvrez comment utiliser les jeux de données Adobe Experience Platform dans Adobe Journey Optimizer
role: User
level: Beginner
exl-id: dcdd3c81-0f00-4259-a8a5-9062a4c40b6f
source-git-commit: 7e27f5502d64d0c91de2c67e4011e650e77c6a92
workflow-type: tm+mt
source-wordcount: '776'
ht-degree: 0%

---

# Prise en main des jeux de données {#datasets-gs}

Toutes les données ingérées dans Adobe Experience Platform sont conservées sous forme de jeux de données dans le lac de données. Un jeu de données est une structure de stockage et de gestion pour une collecte de données, généralement sous la forme d’un tableau, qui contient un schéma (des colonnes) et des champs (des lignes).

## Accès aux jeux de données{#access-datasets}

Le **Jeux de données** espace de travail dans [!DNL Adobe Journey Optimizer] l’interface utilisateur vous permet d’explorer les données et de créer des jeux de données.

Sélectionner **Jeux de données** dans le volet de navigation de gauche pour ouvrir le tableau de bord Jeux de données .

![](assets/datasets-home.png)

Ajouter des données à [!DNL Adobe Experience Platform] est la base de la création d’un profil. Vous pourrez ensuite exploiter les profils dans [!DNL Adobe Journey Optimizer]. Commencez par définir des schémas, utilisez les outils ETL pour préparer et normaliser vos données, puis créez des jeux de données basés sur vos schémas.

Sélectionnez la **Parcourir** pour afficher la liste de tous les jeux de données disponibles pour votre organisation. Des détails s’affichent pour chaque jeu de données répertorié, notamment son nom, le schéma auquel le jeu de données adhère et l’état de l’exécution d’ingestion la plus récente.

Par défaut, seuls les jeux de données que vous avez ingérés s’affichent. Si vous souhaitez afficher les jeux de données générés par le système, activez la variable **Affichage des jeux de données système** bascule à partir du filtre.

![](assets/ajo-system-datasets.png)

Sélectionnez le nom d’un jeu de données pour accéder à son écran Activité du jeu de données et afficher les détails du jeu de données que vous avez sélectionné. L’onglet Activité comprend un graphique qui visualise le taux de messages en cours de consommation ainsi qu’une liste des lots réussis et en échec.

Voici les différents jeux de données disponibles :

**Reporting**

* _Reporting - Jeu de données d’événement de retour de message_: Logs de diffusion des messages. Informations sur toutes les diffusions de messages de Journey Optimizer à des fins de création de rapports et de segments. Les commentaires des FAI par e-mail sur les bounces sont également enregistrés dans ce jeu de données.
* _Reporting - Jeu de données d’événement de suivi de messagerie_: Logs d’interaction pour le canal Email qui est utilisé à des fins de création de rapports et de segments. Informations stockées : informations sur les actions effectuées par l’utilisateur final dans un email (ouvertures, clics, etc.).
* _Reporting - Jeu de données d’événement de suivi push_: Logs d’interaction pour le canal Push utilisés à des fins de création de rapports et de segments. Informations stockées : informations sur les actions effectuées par l’utilisateur final dans les notifications push.
* _Reporting - Événement d’étape du parcours_: Capture tous les événements d’expérience d’étape du parcours générés par Journey Optimizer pour qu’ils soient utilisés par des services tels que la création de rapports. Également essentiel pour la création de rapports dans Customer Journey Analytics pour l’analyse YoY. Associé à des métadonnées de parcours.
* _Création de rapports - Parcours_: Jeu de données de métadonnées contenant des informations sur chaque étape d’un parcours.
* _Reporting - Cci_: Jeu de données d’événement de retour qui stocke les logs de diffusion pour les emails en Cci. À utiliser à des fins de création de rapports.

**Consentement**

* _Jeu de données du service de consentement_: stocke les informations de consentement d’un profil.

**Intelligent Services**

* _Scores d’optimisation du temps d’envoi / Scores d’engagement_: Scores de sortie de l’IA dédiée au parcours.

## Aperçu des jeux de données{#preview-datasets}

Dans l’écran Activité du jeu de données , sélectionnez **Prévisualisation d’un jeu de données** près du coin supérieur droit de l’écran pour prévisualiser le lot le plus récent ayant réussi dans ce jeu de données. Lorsqu’un jeu de données est vide, le lien de prévisualisation est désactivé.

![](assets/dataset-preview.png)

## Création de jeux de données{#create-datasets}

Pour créer un jeu de données, commencez par sélectionner **Création d’un jeu de données** dans le tableau de bord Jeux de données .

Vous pouvez :

* Créez un jeu de données à partir d’un schéma. [En savoir plus dans cette documentation](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#schema){target=&quot;_blank&quot;}
* Créez un jeu de données à partir d’un fichier CSV. [En savoir plus dans cette documentation](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/map-a-csv-file.html){target=&quot;_blank&quot;}

Regardez cette vidéo pour savoir comment créer un jeu de données, le mapper à un schéma, y ajouter des données et confirmer que les données ont été ingérées.

>[!VIDEO](https://video.tv.adobe.com/v/334293?quality=12)

## Gouvernance des données

Dans un jeu de données, parcourez la variable **Gouvernance des données** pour vérifier les libellés au niveau du jeu de données et du champ. La gouvernance des données classe les données en fonction du type de stratégies qui s’applique.

L’une des principales fonctionnalités de [!DNL Adobe Experience Platform] est de rassembler des données issues de plusieurs systèmes d’entreprise afin de permettre aux marketeurs de mieux identifier, comprendre et impliquer les clients. Ces données peuvent être soumises à des restrictions d’utilisation définies par votre organisation ou par des réglementations légales. Il est donc important de s’assurer que vos opérations de données sont conformes aux politiques d’utilisation des données.

[!DNL Adobe Experience Platform Data Governance] vous permet de gérer les données client et de garantir la conformité aux réglementations, aux restrictions et aux politiques applicables à l’utilisation des données. Il joue un rôle clé dans Experience Platform à différents niveaux, notamment le catalogage, la traçabilité des données, l’étiquetage de l’utilisation des données, les stratégies d’utilisation des données et le contrôle de l’utilisation des données pour les actions marketing.

En savoir plus sur la gouvernance des données et les libellés d’utilisation des données dans la section [Documentation sur la gouvernance des données](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/user-guide.html){target=&quot;_blank&quot;}

## Exemples et cas pratiques{#uc-datasets}

Découvrez comment créer un schéma, un jeu de données et ingérer des données pour ajouter des profils de test dans Adobe Journey Optimizer dans [cet exemple de bout en bout](../segment/creating-test-profiles.md)

En savoir plus sur la création de jeux de données dans [Documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target=&quot;_blank&quot;}.

Découvrez comment utiliser l’interface utilisateur des jeux de données dans le [Présentation de Data Ingestion](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html){target=&quot;_blank&quot;}.

Une liste de cas d’utilisation avec des exemples de requête est disponible [here](../data/datasets-query-examples.md).

**Voir aussi**

* [Présentation de l’ingestion par flux](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html){target=&quot;_blank&quot;}
* [Ingestion de données dans Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/tutorials/ingest-batch-data.html){target=&quot;_blank&quot;}
