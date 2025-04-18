---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Enregistrer l’audience
description: Découvrez comment utiliser l’activité Branchement dans une campagne orchestrée
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 84e34d21-dca1-4203-8539-f2b20e461936
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 67%

---

# Enregistrer l’audience {#save-audience}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_save_audience"
>title="Enregistrer une audience"
>abstract="Utilisez cette activité pour mettre à jour une audience existante ou créer une nouvelle audience à partir de la population calculée en amont dans la campagne orchestrée. Les audiences créées sont ajoutées à la liste des audiences et sont disponibles dans le menu **Audiences**."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_saveaudience_outbound"
>title="Générer une transition sortante"
>abstract="Utilisez cette option pour ajouter une transition après l’activité **Enregistrer l’audience**."

L’activité **Enregistrer l’audience** est une activité de **ciblage**. Cette activité permet de mettre à jour une audience existante ou de créer une nouvelle audience à partir de la population calculée en amont dans une campagne orchestrée. Les audiences créées sont ajoutées à la liste des audiences de l’application, disponible via le menu **Audiences**.

Cette activité est essentiellement utilisée afin de conserver des groupes de population calculés dans la même campagne orchestrée, en les convertissant en audiences réutilisables. Connectez-la à d’autres activités de ciblage telles que **Créer une audience** ou **Combiner**.

## Configurer l’activité Enregistrer l’audience{#save-audience-configuration}

Pour configurer l’activité **Enregistrer l’audience**, procédez comme suit :

![](../assets/workflow-save-audience.png)

1. Ajoutez une activité **Enregistrer l’audience** à votre campagne orchestrée.

1. Dans le menu déroulant **Mode**, sélectionnez l’action à réaliser :

   * **Créer ou mettre à jour une audience existante** : définissez un **libellé d’audience**. Si l’audience existe déjà, elle est mise à jour, sinon une nouvelle audience est créée.

   * **Mettre à jour une audience existante** : sélectionnez l’**Audience** à mettre à jour parmi la liste des audiences existantes.

1. Sélectionnez le **mode de mise à jour** qui s’appliquera aux audiences existantes :

   * **Remplacer le contenu de l’audience par de nouvelles données** : tout le contenu de l’audience est remplacé. Les anciennes données sont perdues. Seules les données issues de la transition entrante de l’activité d’enregistrement d’audience sont conservées. Cette option écrase le type et la dimension de ciblage de l’audience mise à jour.

   * **Compléter l’audience avec les nouvelles données** : l’ancien contenu de l’audience est conservé et les données sont complétées avec celles issues de la transition entrante de l’activité d’enregistrement d’audience.

1. Cochez l’option **Générer une transition sortante** si vous souhaitez ajouter une transition après l’activité **Enregistrer l’audience**.

Le contenu de l’audience enregistrée est ensuite disponible dans la vue détaillée de l’audience, accessible depuis le menu **Audiences**. Les colonnes disponibles à partir de cette vue correspondent aux colonnes de la transition entrante de l&#39;activité **Sauvegarde d&#39;audience** de la campagne orchestrée.


## Exemple{#save-audience-example}

L’exemple suivant illustre une mise à jour simple de l’audience à partir du ciblage. Un planificateur est ajouté pour exécuter la campagne orchestrée une fois par mois. Une requête récupère tous les profils abonnés aux différentes applications disponibles. L’activité **Enregistrer l’audience** met à jour l’audience en supprimant les profils qui se sont désabonnés du service depuis la dernière exécution de campagne orchestrée et en ajoutant les profils nouvellement abonnés.
