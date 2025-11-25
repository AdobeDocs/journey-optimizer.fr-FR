---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec les sources de données
description: Découvrez comment commencer avec les sources de données.
feature: Journeys, Data Sources
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: données, source, parcours, plateforme
exl-id: e0cb261f-7cf7-42de-8e56-576492e3b5cc
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: ht
source-wordcount: '343'
ht-degree: 100%

---

# Commencer avec les sources de données {#about-data-sources}

>[!CONTEXTUALHELP]
>id="ajo_journey_data_source_list"
>title="À propos des sources de données"
>abstract="La configuration d’une source de données est toujours effectuée par un utilisateur technique. Elle vous permet de définir une connexion à un système afin de récupérer des informations supplémentaires qui seront utilisées dans vos parcours. Par exemple : définition de conditions, données de paramètres et de personnalisation dans les actions, définition d’attente personnalisée, définition de fuseau horaire."

Elle vous permet de définir une connexion à un système afin de récupérer des informations supplémentaires qui seront utilisées dans vos parcours. Par exemple :

* [Définition d’une condition](../building-journeys/condition-activity.md)
* Données de paramètre et de personnalisation dans les [actions](../action/action.md)
* [Définition d’une attente personnalisée](../building-journeys/wait-activity.md#custom)
* [Définition d’un fuseau horaire](../building-journeys/timezone-management.md)

➡️ [Découvrez cette fonctionnalité en vidéo.](#video)

Cette configuration n’est pas requise si vos parcours utilisent uniquement les données locales provenant d’une payload d’événement. Par exemple, si votre parcours comprend un événement suivi d’une activité d’action de canal qui utilise uniquement les données de l’événement, il n’est pas nécessaire de configurer une source de données.

Il existe deux types de sources de données :

* La source de données Adobe Experience Platform **préconfigurée** qui définit la connexion au service de profil client en temps réel. Il s’agit d’une source de données intégrée. Voir [cette page](../datasource/adobe-experience-platform-data-source.md).
* Les sources de données **externes** qui vous permettent de définir une connexion à des systèmes externes. Il s’agit des sources de données que vous pouvez créer. Voir [cette page](../datasource/external-data-sources.md).

>[!NOTE]
>
>Les réponses étant désormais prises en charge, vous devez utiliser des actions personnalisées au lieu de sources de données pour les cas d’utilisation de sources de données externes. Pour plus d’informations sur les réponses, voir [cette section](../action/action-response.md)

Pour chaque source de données, vous définissez les informations à récupérer à l’aide de groupes de champs. Les groupes de champs sont des ensembles de champs qui peuvent être récupérés à partir d’une source de données. Voir [cette page](../datasource/configure-data-sources.md#define-field-groups).

>[!NOTE]
>
>Les relations de schémas ne sont pas prises en charge pour les sources de données.

Pour plus d’informations sur la configuration d’une source de données Adobe Experience Platform et d’une source de données externe, ainsi que sur la recherche et l’utilisation des données dans un parcours, regardez ce [tutoriel vidéo](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/journey-configuration/configure-data-sources.html?lang=fr){target="_blank"}.

## Vidéo pratique {#video}

Comprenez ce qu&#39;est une source de données. Découvrez également comment configurer des sources de données Experience Platform et externes.

>[!VIDEO](https://video.tv.adobe.com/v/3416634?captions=fre_fr&quality=12)

