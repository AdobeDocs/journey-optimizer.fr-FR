---
solution: Journey Optimizer
product: journey optimizer
title: À propos des sources de données
description: Découvrez comment configurer une source de données
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '309'
ht-degree: 0%

---

# À propos des sources de données {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="À propos des sources de données"
>abstract="La configuration de la source de données est toujours effectuée par un utilisateur technique. La configuration de la source de données vous permet de définir une connexion à un système afin de récupérer des informations supplémentaires qui seront utilisées dans vos parcours, par exemple : définition de condition, données de paramètre et de personnalisation dans les actions, définition d’attente personnalisée, définition de fuseau horaire."

La configuration de la source de données vous permet de définir une connexion à un système afin de récupérer des informations supplémentaires qui seront utilisées dans vos parcours, par exemple :

* [définition de condition](../building-journeys/condition-activity.md)
* données de paramètre et de personnalisation dans [actions](../action/action.md)
* [Définition d’une attente personnalisée](../building-journeys/wait-activity.md#custom)
* [Définition d’un fuseau horaire](../building-journeys/timezone-management.md)

➡️ [Découvrez cette fonctionnalité en vidéo](#video)

Cette configuration n’est pas requise si vos parcours utilisent uniquement des données locales provenant d’une payload d’événement. Par exemple, si votre parcours est composé d’un événement suivi d’une activité d’action de canal qui utilise uniquement les données de l’événement, il n’est pas nécessaire de configurer une source de données.

Il existe deux types de sources de données :

* La source de données Adobe Experience Platform préconfigurée qui définit la connexion au service de profil client en temps réel. Il s’agit d’une source de données intégrée. Voir [cette page](../datasource/adobe-experience-platform-data-source.md).
* Les sources de données externes qui vous permettent de définir une connexion à des systèmes externes. Ce sont celles que vous pouvez créer. Voir [cette page](../datasource/external-data-sources.md).

Pour chaque source de données, vous définissez les informations à récupérer à l’aide de groupes de champs. Les groupes de champs sont des ensembles de champs qui peuvent être récupérés à partir d’une source de données. Voir [cette page](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>Les relations de schéma ne sont pas prises en charge pour les sources de données.

Pour plus d’informations sur la configuration d’une source de données Adobe Experience Platform et d’une source de données externe, ainsi que sur la recherche et l’utilisation des données dans un parcours, regardez cette section [tutoriel vidéo](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html){target=&quot;_blank&quot;}.

## Vidéo pratique {#video}

Découvrez ce qu’est une source de données et comment configurer Experience Platform et des sources de données externes.

>[!VIDEO](https://video.tv.adobe.com/v/334256?quality=12)

