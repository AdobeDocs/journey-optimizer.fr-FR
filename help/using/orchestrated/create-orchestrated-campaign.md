---
solution: Journey Optimizer
product: journey optimizer
title: Création et planification de campagnes orchestrées avec Journey Optimizer
description: Découvrez comment créer et planifier une campagne orchestrée avec Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 13da680d-fef8-4749-9190-8ca3d77b060a
source-git-commit: 6439be00315dfde7ab385d7f848b7031d95060f4
workflow-type: tm+mt
source-wordcount: '1125'
ht-degree: 17%

---


# Créer et planifier une campagne orchestrée {#create-first-campaign}

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>[Étapes de configuration](configuration-steps.md)<br/><br/>[Accédez aux campagnes orchestrées et gérez-les](access-manage-orchestrated-campaigns.md) | [Étapes clés de création de campagne orchestrée](gs-campaign-creation.md)<br/><br/>[Créez et planifiez la campagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrez les activités](orchestrate-activities.md)<br/><br/><b>[Lancez et surveillez la campagne](start-monitor-campaigns.md)</b><br/><br/>[Reporting](reporting-campaigns.md) | [Utiliser le créateur de règles](orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier les expressions](edit-expressions.md)<br/><br/>[Reciblage](retarget.md) | [Prise en main des activités](activities/about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Modifier la dimension](activities/change-dimension.md) - [Activités de canal](activities/channels.md) - [Combine](activities/combine.md) - [Deduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Fork](activities/fork.md) - [Reconciliation](activities/reconciliation.md) - [Enregistrer l’audience](save-audience.md) - [Split](activities/split.md) - [Wait](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Créez une campagne orchestrée dans [!DNL Adobe Journey Optimizer] et configurez son planning d’exécution pour contrôler le moment de son lancement et sa fréquence d’exécution. Choisissez de lancer la campagne immédiatement, à une date et une heure spécifiques ou de manière récurrente à l’aide d’options de planification flexibles telles que les fréquences quotidiennes, hebdomadaires ou mensuelles.

## Créer la campagne {#create}

>[!CONTEXTUALHELP]
>id="ajo_campaign_creation_workflow"
>title="Liste de campagnes orchestrées"
>abstract="L’onglet **Orchestration** répertorie toutes les campagnes orchestrées. Cliquez sur le nom d’une campagne orchestrée pour la modifier. Cliquez sur le bouton **Créer une campagne orchestrée** pour ajouter une nouvelle campagne orchestrée."

Pour créer une campagne orchestrée, procédez comme suit :

1. Dans le menu **[!UICONTROL Campagnes]**, sélectionnez l’onglet **[!UICONTROL Orchestration]**, puis cliquez sur **[!UICONTROL Créer une campagne]**.

   ![](assets/inventory-create.png)

1. Saisissez un nom et une description pour la campagne.

1. *(facultatif)* utilisez le champ **[!UICONTROL Balises]** pour affecter des balises unifiées Adobe Experience Platform à votre campagne. Vous pouvez ainsi facilement les classer et améliorer la recherche à partir de la liste des campagnes orchestrées. [Découvrez comment utiliser les balises](../start/search-filter-categorize.md#tags).

1. Cliquez sur **[!UICONTROL Créer]**.

Votre campagne orchestrée est maintenant créée et apparaît dans la liste des campagnes orchestrées. Vous pouvez mettre à jour ces propriétés à tout moment en cliquant sur l’icône ![icône des paramètres de campagne](assets/do-not-localize/campaign-settings.svg) dans la zone de travail de campagne.

## Planifier la campagne {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_scheduler"
>title="Planificateur"
>abstract="En tant que responsable de campagne, vous pouvez planifier des campagnes pour les lancer automatiquement à des heures spécifiques, ce qui permet d’obtenir un minutage précis et des données de ciblage exactes pour les communications marketing."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_validity"
>title="Validité du planificateur"
>abstract="Vous pouvez définir une période de validité pour le planificateur. Elle peut être permanente (par défaut) ou valide jusqu’à une date spécifique."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_options"
>title="Options du planificateur"
>abstract="Définissez la fréquence du planificateur. Il peut être exécuté à un moment précis, ou encore une ou plusieurs fois par jour, semaine ou mois."

Par défaut, les campagnes orchestrées démarrent lorsqu’elles sont activées manuellement et se terminent lorsque leurs activités associées ont été exécutées. Si vous préférez retarder l’exécution ou exécuter la campagne de manière récurrente, vous pouvez définir un planning pour la campagne.

Tenez compte des bonnes pratiques suivantes lors de la planification de campagnes orchestrées afin de garantir des performances optimales et un comportement attendu :

* Ne planifiez pas l’exécution d’une campagne orchestrée à une fréquence supérieure à toutes les 15 minutes, car cela peut nuire aux performances générales du système et créer des blocs dans la base de données.
* Si vous souhaitez envoyer un message ponctuel dans votre campagne orchestrée, vous pouvez le définir pour qu’il s’exécute **Une fois**.
* Si vous souhaitez envoyer un message récurrent dans votre campagne orchestrée, vous devez utiliser une option **Planification** et définir la fréquence d&#39;exécution. L’activité de diffusion récurrente ne permet pas de définir de planning.

Pour configurer le planning de la campagne, procédez comme suit :

1. Ouvrez la campagne et cliquez sur le bouton **[!UICONTROL Dès que possible]**.

   ![](assets/create-schedule.png)

1. Sélectionnez une fréquence d&#39;exécution pour la campagne, puis configurez les options disponibles. Les paramètres varient en fonction de la fréquence sélectionnée :

   +++Une fois

   Exécuter la campagne une seule fois à une date et une heure spécifiées.

   * **[!UICONTROL Date]** : sélectionnez la date à laquelle la campagne doit être exécutée.
   * **[!UICONTROL Heure]** : sélectionnez l’heure spécifique à laquelle la campagne doit être exécutée.

   +++

   +++Quotidien

   Exécuter la campagne tous les jours ou les jours sélectionnés.

   * **[!UICONTROL Périodicité quotidienne]** : sélectionnez la fréquence d’exécution de la campagne :
      * **[!UICONTROL Tous les jours]** : exécute la campagne tous les jours de la semaine, y compris les week-ends.
      * **[!UICONTROL En semaine]** : exécute la campagne uniquement du lundi au vendredi.
      * **[!UICONTROL Sur une période spécifique]** : exécute la campagne quotidiennement au cours d’une période définie (par exemple, du 1er au 15 juillet). La campagne ne s’exécutera pas en dehors de cette plage.
      * **[!UICONTROL Jours sélectionnés de la semaine]** : exécute la campagne uniquement les jours spécifiés de la semaine (par exemple, lundi, mercredi, vendredi).

   * **[!UICONTROL Heure de début]** : définissez l’heure à laquelle la campagne doit s’exécuter chaque jour.

   +++

   +++Plusieurs fois par jour

   Exécuter la campagne plusieurs fois au cours de la même journée. Vous pouvez choisir des heures spécifiques ou définir une fréquence périodique.

   * **[!UICONTROL Heures sélectionnées]** : sélectionnez les heures spécifiques auxquelles la campagne doit s’exécuter et configurez sa périodicité quotidienne (à exécuter tous les jours de la semaine ou certains jours).
   * **[!UICONTROL Périodique]** : choisissez d’exécuter la campagne toutes les n minutes ou toutes les heures. Vous pouvez également définir la période au cours de laquelle les exécutions sont autorisées.

   +++

   +++Hebdomadaire

   Exécutez la campagne une fois par semaine, avec des options pour des jours spécifiques.

   * **[!UICONTROL Fréquence]** : choisissez la fréquence d’exécution de la campagne (par exemple, toutes les semaines, toutes les 2 semaines).
   * **[!UICONTROL Date de début]** : sélectionnez la date à laquelle la périodicité doit commencer.
   * **[!UICONTROL Périodicité quotidienne]** : sélectionnez les jours de la semaine où l’exécution doit avoir lieu (par exemple, tous les lundis et jeudis).
   * **[!UICONTROL Heure de début]** : définissez l’heure à laquelle la campagne doit s’exécuter les jours sélectionnés.

   +++

   +++Mensuel

   Exécutez la campagne sur une base mensuelle, avec des options pour des jours spécifiques.

   * **[!UICONTROL Récurrence mensuelle]** : indiquez si la campagne s’exécute tous les mois ou uniquement pendant des mois spécifiques.
   * **[!UICONTROL Récurrence quotidienne]** :
      * **[!UICONTROL Tous les jours]** : exécute la campagne tous les jours du mois, y compris les week-ends.
      * **[!UICONTROL Dernier jour du mois]** : exécute la campagne uniquement le dernier jour calendaire de chaque mois (par exemple, le 31 janvier et les 28 et 29 février).
      * **[!UICONTROL Jour spécifique du mois (par exemple, le 15)]** : exécute la campagne un jour spécifié (par exemple, le 15 de chaque mois).
      * **[!UICONTROL Premier/dernier ou énième jour de la semaine]** (par exemple, premier lundi) :      Exécute la campagne un jour de la semaine spécifié (par exemple, le 15 de chaque semaine).
      * **[!UICONTROL Jours sélectionnés de la semaine]** : exécute la campagne un jour spécifié.

   * **[!UICONTROL Heure de début]** : définissez l’heure d’exécution de la campagne.

   +++

1. Utilisez le paramètre **[!UICONTROL Période de validité]** pour définir des dates de début et de fin spécifiques et limiter ainsi l’exécution de la campagne à une période limitée.

1. Pour les plannings de périodicité, cliquez sur le bouton **[!UICONTROL Prévisualiser les heures de lancement]** pour prévisualiser les dates et heures exactes d’exécution à venir en fonction de la configuration actuelle. Cela permet de valider le planning avant l’activation et de s’assurer que la campagne s’exécutera comme prévu.

>[!NOTE]
>
>Lors de la planification de campagnes dans [!DNL Adobe Journey Optimizer], assurez-vous que la date/l’heure de début correspond à la première diffusion souhaitée. Pour les campagnes récurrentes, si l’heure planifiée initiale est déjà dépassée, les campagnes sont reportées au prochain créneau horaire disponible en fonction de leurs règles de périodicité.

Dans l’exemple suivant, l’activité est configurée de sorte que la campagne orchestrée s’exécute deux fois par jour à 9 h et à 12 h, tous les jours de la semaine du 1er octobre 2025 au 1er janvier 2026.

![Planificateur configuré pour exécuter la campagne deux fois par jour à 9 h et 12 h](assets/scheduler-sample.png){width="50%" align="left"}

## Étapes suivantes {#next}

Une fois les paramètres et le planning de votre campagne configurés, vous pouvez commencer à orchestrer les différentes tâches qu’elle effectuera. [Découvrez comment orchestrer des activités de campagne](../orchestrated/orchestrate-activities.md)
