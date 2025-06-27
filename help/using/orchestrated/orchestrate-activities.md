---
solution: Journey Optimizer
product: journey optimizer
title: Création de campagnes orchestrées avec Adobe Journey Optimizer
description: Découvrez comment créer des campagnes orchestrées avec Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: 2604fa59a8fa6393580180afa6da264319636e68
workflow-type: tm+mt
source-wordcount: '737'
ht-degree: 28%

---

# Orchestrer des activités de campagne {#orchestrate}

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>[Étapes de configuration](configuration-steps.md)<br/><br/>[Accédez aux campagnes orchestrées et gérez-les](access-manage-orchestrated-campaigns.md) | [Étapes clés de création de campagne orchestrée](gs-campaign-creation.md)<br/><br/>[Créez et planifiez la campagne](create-orchestrated-campaign.md)<br/><br/><b>[Orchestrez les activités](orchestrate-activities.md)</b><br/><br/>[Envoyez des messages avec des campagnes orchestrées](send-messages.md)<br/><br/>[Lancez et surveillez la campagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Utiliser le créateur de règles](orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier des expressions](edit-expressions.md) | [Prise en main des activités](activities/about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Modifier la dimension](activities/change-dimension.md) - [Combiner](activities/combine.md) - [Deduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Fork](activities/fork.md) - [Reconciliation](activities/reconciliation.md) - [Split](activities/split.md) - [Wait](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Une fois que vous avez [créé une campagne orchestrée](gs-campaign-creation.md), vous pouvez commencer à orchestrer les différentes tâches qu’elle exécutera. Pour ce faire, une zone de travail visuelle vous permet de créer un diagramme de campagne orchestré. Dans ce diagramme, vous pouvez ajouter différentes activités et les enchaîner dans un ordre séquentiel.

## Ajouter des activités {#add}

À ce stade de la configuration, le diagramme comporte une icône de démarrage, qui représente le début de votre campagne orchestrée. Pour ajouter votre première activité, cliquez sur le bouton **+** associé à l’icône de démarrage.

La liste des activités pouvant être ajoutées au diagramme s’affiche. Les activités disponibles dépendent de votre position dans le diagramme de campagne orchestré. Par exemple, lorsque vous ajoutez votre première activité, vous pouvez démarrer votre campagne orchestrée en ciblant une audience, en fractionnant le chemin de campagne orchestré ou en définissant une activité **Attente** pour retarder l’exécution de la campagne orchestrée. D’un autre côté, après une activité **Créer une audience**, vous pouvez affiner votre cible avec des activités de ciblage, envoyer une diffusion à votre audience avec des activités de canal ou organiser le processus de campagne orchestré avec des activités de contrôle de flux.

![](assets/orchestrated-start.png){zoomable="yes"}

Une fois qu’une activité a été ajoutée au diagramme, un volet s’affiche à droite. Il vous permet de la configurer avec des paramètres spécifiques. Des informations détaillées sur la configuration de chacune des activités sont disponibles dans [cette section](activities/about-activities.md).

![](assets/orchestrated-configure-activities.png){zoomable="yes"}

Répétez ce processus pour ajouter autant d’activités que vous le souhaitez en fonction des tâches que votre campagne orchestrée doit effectuer. Vous pouvez également insérer une nouvelle activité entre deux activités. Pour ce faire, cliquez sur le bouton **+** sur la transition entre les activités, puis sélectionnez l’activité souhaitée et configurez-la dans le volet de droite.

Vous pouvez personnaliser le nom des transitions entre chaque activité. Pour ce faire, sélectionnez la transition et modifiez son libellé dans le volet de droite.

![](assets/canvas-transition.png)

## Barre d’outils de la zone de travail {#toolbar}

La barre d’outils de la zone de travail propose des options permettant de manipuler facilement les activités et de naviguer dans la zone de travail :

![](assets/orchestrated-toolbar.png)

![Icône Mode de sélection multiple](assets/do-not-localize/canvas-multiple.svg) Sélectionnez plusieurs activités pour toutes les supprimer en même temps ou copiez-collez-les. [Découvrez comment copier-coller des activités](#copy)

![Icône Rotation](assets/do-not-localize/canvas-rotate.svg) basculez la zone de travail verticalement.

![Icône Ajuster à l’écran](assets/do-not-localize/canvas-fit.svg) Adaptez le niveau de zoom de la zone de travail à votre écran.

![Icône Zoom arrière](assets/do-not-localize/canvas-zoomout.svg) ![Icône Zoom avant](assets/do-not-localize/canvas-zoomin.svg) Zoom arrière ou dans la zone de travail.

![Icône Paramètres de campagne](assets/do-not-localize/canvas-map.svg) ouvre un instantané de la zone de travail indiquant que vous vous trouvez.

## Gérer des activités {#manage}

Lors de l’ajout d’activités, des boutons d’action sont disponibles dans le panneau des propriétés, vous permettant d’effectuer plusieurs opérations.

![](assets/activity-action.png)

![Icône Supprimer](assets/do-not-localize/activity-delete.svg) Supprimez l’activité de la zone de travail.

![Icône Désactiver](assets/do-not-localize/activity-disable.svg) ![Icône Activer](assets/do-not-localize/activity-enable.svg) Désactivez/activez l’activité. Lorsque la campagne orchestrée est exécutée, les activités désactivées et les activités suivantes sur le même chemin ne sont pas exécutées et la campagne orchestrée est arrêtée.

![Icône Pause](assets/do-not-localize/activity-pause.svg) ![Icône Reprendre](assets/do-not-localize/activity-resume.svg) Suspendre/Reprendre l’activité. Lorsque la campagne orchestrée est exécutée, elle se met en pause au niveau de l’activité en pause. La tâche correspondante, ainsi que toutes les suivantes dans le même chemin, ne sont pas exécutées.

![Icône Copier](assets/do-not-localize/activity-copy.svg) Copiez l’activité. [Découvrez comment copier-coller des activités](#copy)

![Icône Logs et tâches](assets/do-not-localize/activity-logs.svg) Accédez aux logs et tâches de l’activité.

Plusieurs activités de **Ciblage**, telles que **Combiner** ou **Déduplication**, vous permettent de traiter la population restante et de l’inclure dans une transition de sortie supplémentaire. Par exemple, si vous utilisez une activité **Partage**, le complémentaire est constitué de la population qui ne correspond à aucun des sous-ensembles définis précédemment. Pour utiliser cette fonctionnalité, activez l’option **[!UICONTROL Générer le complément]**.

## Déplacer ou copier des activités {#move-copy}

### Activités de copier-coller {#copy}

Vous pouvez copier des activités et les coller dans n’importe quelle zone de travail de campagne orchestrée. La campagne de destination peut se trouver dans un autre onglet du navigateur.

* Pour copier une activité, cliquez sur le bouton ![Copier l’icône](assets/do-not-localize/activity-copy.svg) dans le volet des propriétés de l’activité.
* Pour copier plusieurs activités, cliquez sur l’icône ![Mode de sélection multiple](assets/do-not-localize/canvas-multiple.svg) dans la barre d’outils de la zone de travail.

| Copier une activité | Copie de plusieurs activités |
|  ---  |  ---  |
| ![](assets/orchestrated-copy-1.png){width="200" align="center" zoomable="yes"} | ![](assets/orchestrated-copy-2.png){width="200" align="center" zoomable="yes"} |

Pour coller les activités, cliquez sur le bouton **+** sur une transition et sélectionnez « Coller x activité ».

![](assets/orchestrated-copy-3.png){zoomable="yes"}{width="50%"}

<!--## Example {#example}

Here is an orchestrated campaign example designed to send an email to all customers (other than VIP customers) with an email who are interested in coffee machines.

![](assets/workflow-example.png){zoomable="yes"}{zoomable="yes"}

To achieve this, activities below have been added:

* A **[!UICONTROL Fork]** activity that divides the orchestrated campaign into three paths (one for each set of customer),
* **[!UICONTROL Build audience]** activities to target the three sets of customers:

    * Customers with an email,
    * Customers belonging to the pre-existing "Interrested in Coffee Machine(s)" audience,
    * Customers belonging to the pre-existing "VIP ro reward" audience.

* A **[!UICONTROL Combine]** activity that groups together customers with an email and those interested in coffee machines,
* A **[!UICONTROL Combine]** activity that excludes VIP customers,
* An **[!UICONTROL Email delivery]** activity that sends an email to the resulting customers. 

Once you have completed the orchestrated campaign, add en **[!UICONTROL End]** activity at the end of the diagram. This activity allow you to visually mark the end of a workflow and has no functional impact.

After successfully designing the orchestrated campaign diagram, you can execute the orchestrated campaign and track the progress of its various tasks. [Learn how to start an orchestrated campaign and monitor its execution](start-monitor-campaigns.md)-->
