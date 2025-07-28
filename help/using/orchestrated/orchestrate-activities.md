---
solution: Journey Optimizer
product: journey optimizer
title: Créer des campagnes orchestrées avec Adobe Journey Optimizer
description: Découvrez comment créer des campagnes orchestrées à l’aide d’Adobe Journey Optimizer.
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: d1d64125-cf00-49c2-a71d-1494ede16f61
source-git-commit: 855c45b5baec50865ac645eae707d5f1a5052b9b
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 86%

---

# Activités de campagne orchestrée {#orchestrate}

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>Création et gestion de schémas et de jeux de données relationnels :</br> <ul><li>[Prise en main des schémas et des jeux de données](gs-schemas.md)</li><li>[Schéma manuel](manual-schema.md)</li><li>[Schéma de chargement de fichier](file-upload-schema.md)</li><li>[ Ingérer des données ](ingest-data.md)</li></ul>[Accéder aux campagnes orchestrées et les gérer](access-manage-orchestrated-campaigns.md)<br/><br/>[Étapes clés pour créer une campagne orchestrée](gs-campaign-creation.md) | [Créer et planifier la campagne](create-orchestrated-campaign.md)<br/><br/><b>[Orchestrer les activités](orchestrate-activities.md)</b><br/><br/>[Démarrer et surveiller la campagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Utiliser le créateur de règles](orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier les expressions](edit-expressions.md)<br/><br/>[Reciblage](retarget.md) | [Commencer avec les activités](activities/about-activities.md)<br/><br/>Activités :<br/>[Rendez-vous](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Changement de dimension](activities/change-dimension.md) - [Activités de canal](activities/channels.md) - [Combiner](activities/combine.md) - [Déduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Branchement](activities/fork.md) - [Réconciliation](activities/reconciliation.md) - [Enregistrer l’audience](activities/save-audience.md) - [Partage](activities/split.md) - [Attente](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Le contenu de cette page n’est pas définitif et peut être modifié.

>[!ENDSHADEBOX]

Une fois que vous avez [créé une campagne orchestrée](gs-campaign-creation.md), vous pouvez commencer à orchestrer les différentes tâches qu’elle exécutera. Pour ce faire, une zone de travail visuelle dédiée vous permet de créer un diagramme de votre campagne orchestrée. Dans ce diagramme, vous pouvez ajouter différentes activités et les enchaîner dans un ordre séquentiel.

## Ajouter des activités {#add}

À ce stade de la configuration, le diagramme comporte une icône de démarrage, qui représente le début de votre campagne orchestrée. Pour ajouter votre première activité, cliquez sur le bouton **+** associé à l’icône de démarrage.

La liste des activités pouvant être ajoutées au diagramme s’affiche. Les activités disponibles dépendent de votre position dans le diagramme de la campagne orchestrée. Par exemple, lorsque vous ajoutez votre première activité pour démarrer votre campagne orchestrée en ciblant une audience, fractionner le chemin de campagne orchestrée ou définir une activité **Attente** pour retarder l’exécution de la campagne. D’autres choix s’offrent à vous après une activité **Créer une audience** : vous pouvez affiner votre cible avec des activités de ciblage, envoyer une diffusion à votre audience avec des activités de canal ou organiser le processus de la campagne orchestrée avec des activités de contrôle de flux.

![](assets/orchestrated-start.png){zoomable="yes"}

Une fois qu’une activité a été ajoutée au diagramme, un volet s’affiche à droite, permettant de définir des paramètres spécifiques. Des informations détaillées sur la configuration de chacune des activités sont disponibles dans [cette section](activities/about-activities.md).

![](assets/orchestrated-configure-activities.png){zoomable="yes"}

Répétez ce processus pour ajouter autant d’activités que vous le souhaitez en fonction des tâches que votre campagne orchestrée doit exécuter. Vous pouvez également insérer une nouvelle activité entre deux activités. Pour ce faire, cliquez sur le bouton **+** sur la transition entre les activités, puis sélectionnez l’activité souhaitée et configurez-la dans le volet de droite.

Vous avez la possibilité de personnaliser le nom des transitions entre chaque activité. Pour ce faire, sélectionnez la transition et modifiez son libellé dans le volet de droite.

![](assets/canvas-transition.png)

### Barre d’outils de la zone de travail {#toolbar}

La barre d’outils de la zone de travail propose des options permettant de manipuler facilement les activités et de naviguer dans la zone de travail :

![](assets/orchestrated-toolbar.png)

![Multiple selection mode icon](assets/do-not-localize/canvas-multiple.svg) : sélectionnez plusieurs activités pour les supprimer toutes en même temps ou pour les copier et les coller. [Découvrez comment copier et coller les activités.](#copy)

![Rotate icon](assets/do-not-localize/canvas-rotate.svg) : faites pivoter la zone de travail verticalement.

![Fit to screen icon](assets/do-not-localize/canvas-fit.svg) : adaptez l’échelle de la zone de travail à votre écran.

![Zoom out icon](assets/do-not-localize/canvas-zoomout.svg)/![Zoom in  icon](assets/do-not-localize/canvas-zoomin.svg) : effectuez un zoom arrière ou avant dans la zone de travail.

![Campaign settings icon](assets/do-not-localize/canvas-map.svg) : ouvre un instantané de la zone de travail indiquant où vous vous trouvez.

### Gérer des activités {#manage}

Lors de l’ajout d’activités, des boutons d’action sont disponibles dans le panneau des propriétés, vous permettant d’effectuer plusieurs opérations.

![](assets/activity-action.png)

![Delete icon](assets/do-not-localize/activity-delete.svg) : supprimez l’activité à partir de la zone de travail.

![Disable icon](assets/do-not-localize/activity-disable.svg) ![Enable icon](assets/do-not-localize/activity-enable.svg) : désactivez/activez l’activité. Lorsque la campagne orchestrée est exécutée, les activités désactivées et les activités qui suivent sur le même chemin ne sont pas exécutées et la campagne orchestrée est arrêtée.

![Pause icon](assets/do-not-localize/activity-pause.svg) ![Resume icon](assets/do-not-localize/activity-resume.svg) : suspendez/reprenez l’activité. Lorsque la campagne orchestrée est exécutée, elle s’arrête quand l’activité est en pause. La tâche correspondante, ainsi que toutes les suivantes dans le même chemin, ne sont pas exécutées.

Vous pouvez utiliser n’importe quelle activité de la zone de travail comme point d’arrêt pour suspendre l’exécution de la campagne. Cela signifie que la campagne sera exécutée uniquement jusqu’à cette activité, puis que l’exécution sera suspendue. Pendant la suspension de l’exécution, le moteur de segmentation conserve les données temporaires à votre disposition pour la prévisualisation. Vous pouvez sélectionner la transition entrante juste avant l’activité en pause pour afficher les données transportées. En savoir plus sur cette section : [Surveillance visuelle du flux](../orchestrated/start-monitor-campaigns.md#flow).

![Copy icon](assets/do-not-localize/activity-copy.svg) : copiez l’activité. [Découvrez comment copier et coller les activités.](#copy)

![Logs and tasks icon](assets/do-not-localize/activity-logs.svg) : accédez aux journaux et tâches de l’activité.

Plusieurs activités de **Ciblage**, telles que **Combiner** ou **Déduplication**, vous permettent de traiter la population restante et de l’inclure dans une transition de sortie supplémentaire. Par exemple, si vous utilisez une activité **Partage**, le complément est constitué de la population qui ne correspond à aucun des sous-ensembles définis précédemment. Pour utiliser cette fonctionnalité, activez l’option **[!UICONTROL Générer le complément]**.

### Activités de copier-coller {#copy}

Vous pouvez copier des activités et les coller dans n’importe quelle zone de travail de la campagne orchestrée. La campagne de destination peut se trouver dans un autre onglet du navigateur.

* Pour copier une activité, cliquez sur le bouton ![Copy icon](assets/do-not-localize/activity-copy.svg) dans le volet des propriétés de l’activité.
* Pour copier plusieurs activités, cliquez sur l’icône ![Multiple selection mode icon](assets/do-not-localize/canvas-multiple.svg) dans la barre d’outils de la zone de travail.

| Copier une activité | Copier plusieurs activités |
|  ---  |  ---  |
| ![](assets/orchestrated-copy-1.png){width="200" align="center" zoomable="yes"} | ![](assets/orchestrated-copy-2.png){width="200" align="center" zoomable="yes"} |

Pour coller les activités, cliquez sur le bouton **+** sur une transition et sélectionnez « Coller l’activité X ».

![](assets/orchestrated-copy-3.png){zoomable="yes"}{width="50%"}

## Exemple de diagramme {#example}

Voici un exemple de campagne orchestrée conçue pour envoyer un e-mail aux clientes et clients qui ont effectué un achat d’au moins 100 $, tout en excluant celles et ceux qui ont moins de 50 points de fidélité.

![](assets/canvas-example-diagram.png){zoomable="yes"}

Dans le cadre de ce workflow, les activités suivantes ont été ajoutées :

* Une activité **[!UICONTROL Branchement]** divise la campagne orchestrée en trois chemins.
* Les activités **[!UICONTROL Créer une audience]** ciblent les trois ensembles de clientes et clients :

   * les clients et clientes disposant d’une adresse e-mail
   * Les clientes et clients qui ont effectué un achat d’au moins 100 $
   * Les clientes et clients qui ont moins de 50 points de fidélité

* Une activité **[!UICONTROL Combiner]** regroupe les clientes et clients disposant d’une adresse e-mail et celles et ceux qui ont effectué un achat d’au moins 100 $.
* Une activité **[!UICONTROL Combiner]** exclut les clientes et clients disposant de moins de 50 points de fidélité.
* Une activité **[!UICONTROL Diffusion e-mail]** envoie un e-mail aux clientes et clients correspondants.

## Étapes suivantes {#next}

Une fois le diagramme de la campagne orchestrée conçu, vous pouvez exécuter la campagne orchestrée et suivre la progression des différentes tâches. [Découvrez comment démarrer une campagne orchestrée et surveiller son exécution](start-monitor-campaigns.md).
