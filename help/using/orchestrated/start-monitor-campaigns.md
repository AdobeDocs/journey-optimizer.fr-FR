---
solution: Journey Optimizer
product: journey optimizer
title: Démarrer et surveiller les campagnes orchestrées avec Adobe Journey Optimizer
description: Découvrez comment démarrer et surveiller des campagnes orchestrées avec Adobe Journey Optimizer.
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: f8afef4729e50b7c9899bf7f2fe282347220dfac
workflow-type: tm+mt
source-wordcount: '780'
ht-degree: 35%

---

# Démarrer et surveiller vos campagnes orchestrées {#start-monitor}

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Publier une campagne orchestrée"
>abstract="Pour lancer votre campagne, vous devez la publier. Assurez-vous que tous les avertissements sont effacés avant la publication."

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>[Étapes de configuration](configuration-steps.md)<br/><br/>[Accédez aux campagnes orchestrées et gérez-les](access-manage-orchestrated-campaigns.md) | [Étapes clés de création de campagne orchestrée](gs-campaign-creation.md)<br/><br/>[Créez et planifiez la campagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrez les activités](orchestrate-activities.md)<br/><br/>[Envoyez des messages avec des campagnes orchestrées](send-messages.md)<br/><br/><b>[Lancez et surveillez la campagne](start-monitor-campaigns.md)</b><br/><br/>[Reporting](reporting-campaigns.md) | [Utiliser le créateur de règles](orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier des expressions](edit-expressions.md) | [Prise en main des activités](activities/about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Modifier la dimension](activities/change-dimension.md) - [Combiner](activities/combine.md) - [Deduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Fork](activities/fork.md) - [Reconciliation](activities/reconciliation.md) - [Split](activities/split.md) - [Wait](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

Une fois que vous avez créé et conçu les tâches à effectuer dans la zone de travail, vous pouvez les publier et contrôler leur exécution.

Vous pouvez également exécuter la campagne en mode test pour vérifier son exécution et le résultat des différentes activités.

## Tester et publier la campagne orchestrée {#test}

Journey Optimizer vous permet de tester vos campagnes orchestrées avant de les publier. Vous pouvez ainsi vérifier l’exécution et le résultat des différentes tâches composant la campagne, et cela n’a aucun impact fonctionnel : toutes les activités de la zone de travail sont exécutées, à l’exception des activités ayant un impact telles que **[!UICONTROL Sauvegarde d’audience]** et activités de canal.

Pour démarrer une campagne orchestrée en mode test, ouvrez la campagne orchestrée, puis cliquez sur le bouton **[!UICONTROL Démarrer]**.

![](assets/campaign-start.png){zoomable="yes"}

Une fois la campagne orchestrée en cours d’exécution, chaque activité de la zone de travail est exécutée dans un ordre séquentiel, jusqu’à ce que la fin de la campagne orchestrée soit atteinte.

Lorsque votre campagne est prête à être publiée, cliquez sur le bouton **[!UICONTROL Publier]**. Le flux visuel dans la zone de travail redémarre, ce qui vous permet d’afficher la progression des profils dans le diagramme.

## Flux visuel des campagnes orchestrées

Lorsqu’une campagne orchestrée est en cours d’exécution, en mode test ou de production, vous pouvez suivre la progression des profils ciblés par le biais des différentes tâches en temps réel à l’aide d’un flux visuel. Vous pouvez ainsi identifier rapidement le statut de chaque activité et le nombre de profils qu’elle contient.

![](assets/workflow-execution.png){zoomable="yes"}

Les données transportées d&#39;une activité à une autre via des transitions sont stockées dans une table de travail temporaire. Ces données peuvent être affichées pour chaque transition. Pour cela, sélectionnez une transition pour ouvrir ses propriétés dans la partie droite de l’écran.

* Cliquez sur **[!UICONTROL Aperçu du schéma]** pour afficher le schéma de la table de travail.
* Cliquez sur **[!UICONTROL Aperçu des résultats]** pour visualiser les données véhiculées dans la transition sélectionnée.

![](assets/transition.png){zoomable="yes"}

## Surveiller l’exécution de la campagne

### Surveiller l’exécution des activités {#activities}

Les indicateurs visuels présents dans chaque boîte d&#39;activité permettent de vérifier leur exécution :

| Indicateur visuel | Description |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | L’activité est en cours d’exécution. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | L’activité nécessite votre attention. Vous devez, par exemple, confirmer l’envoi d’une diffusion ou prendre une mesure nécessaire. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | L’activité a rencontré une erreur. Pour résoudre ce problème, ouvrez les journaux de campagne orchestrés pour plus d’informations. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | L’activité a été exécutée correctement. |

### Surveiller les logs et les tâches {#logs-tasks}

>[!CONTEXTUALHELP]
>id="ajo_campaign_logs"
>title="Logs et tâches"
>abstract="L’écran **Logs et tâches** fournit un historique de l’exécution de la campagne orchestrée : il consigne toutes les actions de l’utilisateur ou de l’utilisatrice, ainsi que les erreurs rencontrées."

La surveillance des logs et des tâches est une étape essentielle pour analyser vos campagnes orchestrées et vérifier qu’elles s’exécutent correctement. Les logs sont accessibles à partir de l’icône **[!UICONTROL Logs]**, située dans la barre d’outils d’actions et dans le volet des propriétés de chaque activité.

Le menu **[!UICONTROL Logs et tâches]** fournit un historique de l’exécution de la campagne orchestrée, enregistrant toutes les actions des utilisateurs et utilisatrices ainsi que les erreurs rencontrées.

![](assets/workflow-logs.png){zoomable="yes"}

Deux types d’informations sont disponibles :

* L’onglet **[!UICONTROL Log]** contient l’historique de l’exécution de toutes les activités de la campagne orchestrée. Il répertorie par ordre chronologique les opérations réalisées et les erreurs d’exécution.
* L’onglet **[!UICONTROL Tâches]** permet de voir le séquencement de l’exécution des activités.

Sous les deux onglets, vous pouvez choisir les colonnes à afficher et leur ordre, appliquer des filtres et trouver rapidement des informations à l’aide du champ de recherche.

## Commandes d’exécution de campagne orchestrées {#execution-commands}

La barre d’actions située dans le coin supérieur droit propose des commandes qui vous permettent de gérer l’exécution orchestrée de la campagne. Vous pouvez effectuer les actions suivantes :

* **[!UICONTROL Démarrer]** / **[!UICONTROL Reprendre]** l&#39;exécution de la   campagne orchestrée, qui adopte alors le statut En cours . Si la campagne orchestrée a été suspendue, elle est reprise, sinon elle est lancée et les activités initiales sont alors activées.

* **[!UICONTROL Pause]** l’exécution de la campagne orchestrée, qui adopte alors le statut En pause. Aucune nouvelle activité ne sera activée jusqu’à la prochaine reprise, mais les opérations en cours ne sont pas suspendues.

* **[!UICONTROL Arrêter]** une campagne orchestrée en cours d’exécution, qui adopte alors le statut Terminé. Les opérations en cours sont interrompues si possible. Vous ne pouvez pas reprendre à partir de la campagne orchestrée à l’endroit où elle a été arrêtée.
