---
solution: Journey Optimizer
product: journey optimizer
title: Source de données Adobe Experience Platform
description: Découvrez comment configurer la source de données Adobe Experience Platform
feature: Journeys, Data Sources
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: intégré, source, données, platform, intégration
exl-id: 9083e355-15e3-4d1f-91ae-03095e08ad16
source-git-commit: f5ea4455fc0a8ed9e2819a260a8691fc1237844c
workflow-type: tm+mt
source-wordcount: '422'
ht-degree: 63%

---

# Source de données Adobe Experience Platform {#adobe-experience-platform-data-source}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_built_in"
>title="Source de données Adobe Experience Platform"
>abstract="La source de données Adobe Experience Platform définit la connexion au profil client en temps réel d’Adobe. Cette source de données est intégrée et préconfigurée et ne peut pas être supprimée. Elle est conçue pour récupérer et utiliser des données du service de profil client en temps réel (par exemple, vérifier si la personne qui est entrée dans un parcours est de sexe féminin). Elle vous permet d’utiliser les données de profil et les données des événements d’expérience."

La source de données Adobe Experience Platform définit la connexion au profil client en temps réel d’Adobe. Cette source de données est intégrée et préconfigurée et ne peut pas être supprimée. Cette source de données est conçue pour récupérer et utiliser des données du service de profil client en temps réel (par exemple, vérifier si la personne qui est entrée dans un parcours est de sexe féminin). Elle vous permet d&#39;utiliser les données de profil et les données des événements d&#39;expérience. Pour plus d’informations sur le profil client en temps réel d’Adobe, consultez la documentation de [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=fr){target="_blank"}.

Pour autoriser la connexion au service de profil client en temps réel, nous devons utiliser une clé afin d’identifier une personne, ainsi qu’un espace de noms qui contextualise la clé. Par conséquent, vous ne pouvez utiliser cette source de données que si vos parcours commencent par un événement contenant une clé et un espace de noms. [En savoir plus](../building-journeys/journey.md).

Vous pouvez modifier le groupe de champs préconfiguré nommé « ProfileFieldGroup », en ajouter de nouveaux et supprimer ceux qui ne sont pas utilisés dans les parcours actifs ou dans un état de brouillon. [En savoir plus](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>Vous pouvez récupérer les 1 000 derniers événements d’expérience créés il y a moins d’un an.

Les étapes principales pour ajouter des groupes de champs à la source de données intégrée sont présentées ci-dessous :

1. Dans la liste des sources de données, sélectionnez la source de données intégrée **Adobe Experience Platform**.

   Le volet de configuration de la source de données s’ouvre alors dans la partie droite de l’écran.

   ![](assets/journey23.png)

1. Sélectionnez **[!UICONTROL Ajouter un nouveau groupe de champs]** pour définir une [nouvelle série de champs à récupérer](../datasource/configure-data-sources.md#define-field-groups).

   ![](assets/journey24.png)

1. Sélectionnez un schéma dans la liste déroulante **[!UICONTROL Schéma]**. Ce champ répertorie les schémas **Profil** et **Événements d’expérience** disponibles dans Adobe Experience Platform. La création du schéma est effectuée dans Adobe Experience Platform, mais pas dans Adobe Journey Optimizer.
1. Sélectionnez les champs à utiliser et enregistrez vos modifications.


>[!TIP]
>
>Pointez sur le nom d’un groupe de champs pour afficher deux icônes à droite. Utilisez-les pour **Dupliquer** ou **Supprimer** le groupe de champs. Notez que l’icône **[!UICONTROL Supprimer]** n’est disponible que si le groupe de champs n’est utilisé dans aucun parcours **En ligne**, **Brouillon** ou **Terminé**. Reportez-vous au champ **[!UICONTROL Utilisé dans]** pour vérifier si c’est le cas.
