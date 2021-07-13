---
title: 'Source de données Adobe Experience Platform '
description: Découvrez comment configurer la source de données Adobe Experience Platform
feature: Sources de données
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 95%

---

# Source de données Adobe Experience Platform {#concept_zrb_nqt_52b}

La source de données Adobe Experience Platform définit la connexion au service de profil client en temps réel. Il s’agit d’une source de données intégrée et préconfigurée. Elle ne peut pas être supprimée. Cette source de données est conçue pour récupérer et utiliser des données du service de profil client en temps réel (par exemple, vérifier si la personne qui est entrée dans un parcours est de sexe féminin). Elle vous permet d’utiliser les données de profil et les données des événements d’expérience. Pour plus d’informations sur le service de profil client en temps réel, consultez la [documentation Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=fr){target=&quot;_blank&quot;}.

>[!NOTE]
>
>Vous pouvez récupérer les 1 000 derniers événements d’expérience créés il y a moins d’un an.

Pour autoriser la connexion au service de profil client en temps réel, nous devons utiliser une clé afin d’identifier une personne, ainsi qu’un espace de noms qui contextualise la clé. Par conséquent, vous ne pouvez utiliser cette source de données que si vos parcours commencent par un événement contenant une clé et un espace de noms. Voir [cette page](../building-journeys/journey.md).

Vous pouvez modifier le groupe de champs préconfiguré nommé « ProfileFieldGroup », en ajouter de nouveaux et supprimer ceux qui ne sont pas utilisés dans les parcours actifs ou dans un état de brouillon. Voir [cette page](../datasource/configure-data-sources.md#define-field-groups).

Les principales étapes nécessaires pour ajouter des groupes de champs à la source de données intégrée sont les suivantes :

1. Dans la liste des sources de données, sélectionnez la source de données Adobe Experience Platform intégrée.

   Le volet de configuration de la source de données s’ouvre alors dans la partie droite de l’écran.

   ![](../assets/journey23.png)

1. Cliquez sur **[!UICONTROL Ajouter un nouveau groupe de champs]** pour définir une nouvelle série de champs à récupérer. Voir [cette page](../datasource/configure-data-sources.md#define-field-groups).

   ![](../assets/journey24.png)

1. Sélectionnez un schéma dans la liste déroulante **[!UICONTROL Schéma]**. Ce champ répertorie les schémas de profil et d’événements d’expérience disponibles dans Adobe Experience Platform. La création du schéma n’est pas effectuée dans [!DNL Journey Optimizer], mais elle l’est dans Adobe Experience Platform.
1. Sélectionnez les champs que vous souhaitez utiliser.
1. Définissez la durée de mise en cache.
1. Cliquez sur **[!UICONTROL Enregistrer]**.

Lorsque vous placez le curseur sur le nom d’un groupe de champs, deux icônes s’affichent à droite. Elles vous permettent de supprimer et de dupliquer le groupe de champs. Notez que l’icône **[!UICONTROL Supprimer]** n’est disponible que si le groupe de champs n’est utilisé dans aucun parcours actif ou dans un état de brouillon (cette information est affichée dans le champ **[!UICONTROL Utilisé(e) dans]**).
