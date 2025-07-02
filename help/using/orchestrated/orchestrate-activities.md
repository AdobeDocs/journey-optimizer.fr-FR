---
solution: Journey Optimizer
product: journey optimizer
title: Création de campagnes orchestrées avec Adobe Journey Optimizer
description: Découvrez comment créer des campagnes orchestrées avec Adobe Journey Optimizer
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: d8b83bc46526f721d4dfaf62cf8ba4cbf5a56ce7
workflow-type: tm+mt
source-wordcount: '893'
ht-degree: 24%

---

# Orchestrer des activités de campagne {#orchestrate}

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>[Étapes de configuration](configuration-steps.md)<br/><br/>[Accédez aux campagnes orchestrées et gérez-les](access-manage-orchestrated-campaigns.md) | [Étapes clés de création de campagne orchestrée](gs-campaign-creation.md)<br/><br/>[Créez et planifiez la campagne](create-orchestrated-campaign.md)<br/><br/><b>[Orchestrez les activités](orchestrate-activities.md)</b><br/><br/>[Lancez et surveillez la campagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Utiliser le créateur de règles](orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier des expressions](edit-expressions.md) | [Prise en main des activités](activities/about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Modifier la dimension](activities/change-dimension.md) - [Activités de canal](activities/channels.md) - [Combine](activities/combine.md) - [Deduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Fork](activities/fork.md) - [Reconciliation](activities/reconciliation.md) - [Split](activities/split.md) - [Wait](activities/wait.md) |

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

### Barre d’outils de la zone de travail {#toolbar}

La barre d’outils de la zone de travail propose des options permettant de manipuler facilement les activités et de naviguer dans la zone de travail :

![](assets/orchestrated-toolbar.png)

![Icône Mode de sélection multiple](assets/do-not-localize/canvas-multiple.svg) Sélectionnez plusieurs activités pour toutes les supprimer en même temps ou copiez-collez-les. [Découvrez comment copier-coller des activités](#copy)

![Icône Rotation](assets/do-not-localize/canvas-rotate.svg) basculez la zone de travail verticalement.

![Icône Ajuster à l’écran](assets/do-not-localize/canvas-fit.svg) Adaptez le niveau de zoom de la zone de travail à votre écran.

![Icône Zoom arrière](assets/do-not-localize/canvas-zoomout.svg) ![Icône Zoom avant](assets/do-not-localize/canvas-zoomin.svg) Zoom arrière ou dans la zone de travail.

![Icône Paramètres de campagne](assets/do-not-localize/canvas-map.svg) ouvre un instantané de la zone de travail indiquant que vous vous trouvez.

### Gérer des activités {#manage}

Lors de l’ajout d’activités, des boutons d’action sont disponibles dans le panneau des propriétés, vous permettant d’effectuer plusieurs opérations.

![](assets/activity-action.png)

![Icône Supprimer](assets/do-not-localize/activity-delete.svg) Supprimez l’activité de la zone de travail.

![Icône Désactiver](assets/do-not-localize/activity-disable.svg) ![Icône Activer](assets/do-not-localize/activity-enable.svg) Désactivez/activez l’activité. Lorsque la campagne orchestrée est exécutée, les activités désactivées et les activités suivantes sur le même chemin ne sont pas exécutées et la campagne orchestrée est arrêtée.

![Icône Pause](assets/do-not-localize/activity-pause.svg) ![Icône Reprendre](assets/do-not-localize/activity-resume.svg) Suspendre/Reprendre l’activité. Lorsque la campagne orchestrée est exécutée, elle se met en pause au niveau de l’activité en pause. La tâche correspondante, ainsi que toutes les suivantes dans le même chemin, ne sont pas exécutées.

![Icône Copier](assets/do-not-localize/activity-copy.svg) Copiez l’activité. [Découvrez comment copier-coller des activités](#copy)

![Icône Logs et tâches](assets/do-not-localize/activity-logs.svg) Accédez aux logs et tâches de l’activité.

Plusieurs activités de **Ciblage**, telles que **Combiner** ou **Déduplication**, vous permettent de traiter la population restante et de l’inclure dans une transition de sortie supplémentaire. Par exemple, si vous utilisez une activité **Partage**, le complémentaire est constitué de la population qui ne correspond à aucun des sous-ensembles définis précédemment. Pour utiliser cette fonctionnalité, activez l’option **[!UICONTROL Générer le complément]**.

### Activités de copier-coller {#copy}

Vous pouvez copier des activités et les coller dans n’importe quelle zone de travail de campagne orchestrée. La campagne de destination peut se trouver dans un autre onglet du navigateur.

* Pour copier une activité, cliquez sur le bouton ![Copier l’icône](assets/do-not-localize/activity-copy.svg) dans le volet des propriétés de l’activité.
* Pour copier plusieurs activités, cliquez sur l’icône ![Mode de sélection multiple](assets/do-not-localize/canvas-multiple.svg) dans la barre d’outils de la zone de travail.

| Copier une activité | Copie de plusieurs activités |
|  ---  |  ---  |
| ![](assets/orchestrated-copy-1.png){width="200" align="center" zoomable="yes"} | ![](assets/orchestrated-copy-2.png){width="200" align="center" zoomable="yes"} |

Pour coller les activités, cliquez sur le bouton **+** sur une transition et sélectionnez « Coller x activité ».

![](assets/orchestrated-copy-3.png){zoomable="yes"}{width="50%"}

## Exemple de diagramme {#example}

Voici un exemple de campagne orchestrée conçue pour envoyer un e-mail à tous les clients qui ont effectué un achat d’au moins 100 $, tout en excluant tous les clients qui ont moins de 50 points de fidélité.

![](assets/canvas-example-diagram.png){zoomable="yes"}

Dans le cadre de ce workflow, les activités suivantes ont été ajoutées :

* Une activité **[!UICONTROL Branchement]** divise la campagne orchestrée en trois chemins.
* Les activités **[!UICONTROL Créer une audience]** ciblent les trois ensembles de clients et clientes :

   * les clients et clientes disposant d’une adresse e-mail
   * Les clients qui ont effectué un achat d&#39;au moins 100 $,
   * Les clients qui ont moins de 50 points de fidélité.

* Une activité **[!UICONTROL Combiner]** regroupe les clients et clientes disposant d’une adresse e-mail et ceux et celles qui ont effectué un achat d’au moins 100 $,
* Une activité **[!UICONTROL Combiner]** exclut les clients et clientes disposant de moins de 50 points de fidélité,
* Une activité **[!UICONTROL Diffusion e-mail]** envoie un e-mail aux clients et clientes correspondants(e)s.

## Étapes suivantes {#next}

Une fois le diagramme de campagne orchestré conçu, vous pouvez l’exécuter et suivre l’avancement de ses différentes tâches. [Découvrez comment démarrer une campagne orchestrée et surveiller son exécution](start-monitor-campaigns.md)
