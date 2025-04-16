---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser des activités de campagne orchestrées
description: Découvrez comment orchestrer des activités de campagne.
hide: true
hidefromtoc: true
exl-id: 02f986b2-8200-4e0e-8918-44e528a6a3ec
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 55%

---

# À propos des activités de campagne orchestrées {#ms-campaign-activities}

Les activités de campagne orchestrées sont regroupées en trois catégories. Selon le contexte, les activités disponibles peuvent différer.

Toutes les activités sont présentées dans les sections ci-dessous :

* [Activités de ciblage et de gestion des données](#targeting)
* [Activités de canal](#channel)
* [Activités de contrôle de flux](#flow-control)

![](../assets/workflow-activities.png)

## Activités de ciblage {#targeting}

Ces activités sont spécifiques au ciblage. Elles permettent de construire une ou plusieurs cibles en définissant une audience, puis en partageant ou en combinant ces audiences à l’aide des opérations d’intersection, d’union ou d’exclusion.

* [Créer une audience](build-audience.md) : définissez votre population cible. Vous pouvez sélectionner une audience existante ou utiliser le concepteur de requête pour définir votre propre requête.
* [Modifier la dimension](change-dimension.md) : modifiez la dimension de ciblage au fur et à mesure que vous créez votre campagne orchestrée.
* [Combiner](combine.md) : effectuez une segmentation sur votre population entrante. Vous pouvez utiliser une union, une intersection ou une exclusion.
* [Déduplication](deduplication.md) : supprimez les doublons dans le ou les résultats des activités entrantes.
* [Enrichissement](enrichment.md) : définissez des données supplémentaires à traiter dans votre campagne orchestrée. Avec cette activité, vous pouvez utiliser la transition entrante et configurer l’activité pour ajouter des données supplémentaires à la transition sortante.
* [Réconciliation](reconciliation.md) : permet de définir le lien entre les données des données Journey Optimizer et les données d&#39;une table de travail, par exemple les données chargées depuis un fichier externe.
* [Sauvegarde d&#39;audience](save-audience.md) : mettez à jour une audience existante ou créez une audience à partir de la population calculée en amont dans une campagne orchestrée.
* [Partage](split.md) : segmentez la population entrante en plusieurs sous-ensembles.

## Activités de gestion des données {#data}

Ces activités sont spécifiques à la manipulation et à l’enrichissement des données de population.

* [Chargement de fichier](load-file.md) : utilisez des profils et des données stockés dans un fichier externe.
* [Mise à jour des données](update-data.md) : effectuez des mises à jour en masse des champs de la base de données. Plusieurs options vous permettent de personnaliser la mise à jour des données.

## Activités de canal {#channel}

Adobe Journey Optimizer vous permet d’automatiser et d’exécuter des campagnes marketing sur plusieurs canaux. Vous pouvez combiner des activités de canal dans la zone de travail afin de créer une campagne orchestrée cross-canal pouvant déclencher des actions en fonction du comportement du client ou de la cliente. Les activités **Canal** suivantes sont disponibles : e-mail, SMS, notifications push Android et iOS. [Découvrez comment configurer une diffusion dans le contexte d&#39;une campagne orchestrée](channels.md).

## Activités de contrôle de flux {#flow-control}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_end"
>title="Activité de fin"
>abstract="L’activité **Fin** vous permet de marquer graphiquement la fin d’une campagne orchestrée. Cette activité n’a aucun impact fonctionnel et est donc facultative."

Les activités suivantes sont spécifiques à l&#39;organisation et à l&#39;exécution de campagnes orchestrées. Leur principale tâche est de coordonner les autres activités :

* [Rendez-vous](and-join.md) : synchronisez plusieurs branches d’exécution d’une campagne orchestrée.
* **Fin** : marquez graphiquement la fin d’une campagne orchestrée. Cette activité n’a aucun impact fonctionnel et est donc facultative.
* [Branchement](fork.md) : créez des transitions sortantes afin de lancer plusieurs activités en parallèle.
* [Planificateur](scheduler.md) : planifiez le démarrage de la campagne orchestrée.
* [Test](test.md) : activez des transitions en fonction de conditions spécifiées.
* [Attente](wait.md) : interrompt momentanément l’exécution d’une partie d’une campagne orchestrée.
