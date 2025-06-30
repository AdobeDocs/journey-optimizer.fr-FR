---
solution: Journey Optimizer
product: journey optimizer
title: Démarrer et surveiller les campagnes orchestrées avec Adobe Journey Optimizer
description: Découvrez comment démarrer et surveiller des campagnes orchestrées avec Adobe Journey Optimizer.
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: 02270bddf988e8a722e78d0b63fe157c74b586e4
workflow-type: tm+mt
source-wordcount: '694'
ht-degree: 18%

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

## Tester votre campagne avant la publication {#test}

Journey Optimizer vous permet de tester les campagnes orchestrées avant leur mise en ligne. En mode test, toutes les activités de la zone de travail sont exécutées, à l’exception des activités **[!UICONTROL Sauvegarde d’audience]** et des activités de canal. Il n’y a aucun impact fonctionnel sur vos données ou votre audience.

Pour tester une campagne :

1. Ouvrez la campagne orchestrée.
2. Cliquez sur **[!UICONTROL Démarrer]**.

![](assets/campaign-start.png){zoomable="yes"}

Chaque activité de la campagne est exécutée de manière séquentielle jusqu’à ce que la fin du diagramme soit atteinte. Lors de l’exécution du test, vous pouvez gérer la campagne à l’aide de la barre d’actions de la zone de travail. Plusieurs possibilités sʼoffrent alors à vous :

* **Arrêter** l’exécution à tout moment.
* **Démarrez** l’exécution à nouveau.
* **Reprendre** l’exécution si elle a été précédemment suspendue en raison d’un problème.

Si une erreur ou un avertissement se produit lors de l’exécution, vous êtes averti(e) via l’icône **[!UICONTROL Alertes]** / **[!UICONTROL Avertissement]** dans la barre d’outils de la zone de travail.

![](assets/campaign-warning.png){zoomable="yes"}

Vous pouvez également identifier rapidement les activités ayant échoué à l’aide des [indicateurs visuels de statut](#activities) affichés directement sur chaque activité. Pour obtenir un dépannage détaillé, ouvrez les [journaux de la campagne](#logs-tasks) qui fournissent des informations détaillées sur l’erreur et son contexte.

## Publication de la campagne {#publish}

Une fois votre campagne testée et prête, cliquez sur **[!UICONTROL Publier]** pour la rendre active.

![](assets/campaign-publish.png){zoomable="yes"}

Le flux visuel redémarre et les profils réels commencent à circuler dans le parcours en temps réel.

## Surveiller l’exécution des campagnes {#monitor}

### Surveillance visuelle du flux {#flow}

Lors de l’exécution (en mode test ou actif), le flux visuel montre comment les profils se déplacent dans le parcours en temps réel. Le nombre de profils qui passent d’une tâche à l’autre s’affiche.

![](assets/workflow-execution.png){zoomable="yes"}

1. Sélectionnez une transition.
1. Dans le panneau de droite :
&#x200B;- Cliquez sur **[!UICONTROL Aperçu du schéma]** pour afficher le schéma de la table de travail.
&#x200B;- Cliquez sur **[!UICONTROL Prévisualiser les résultats]** pour afficher les données transportées.

![](assets/transition.png){zoomable="yes"}

Les données transportées d&#39;une activité à une autre via des transitions sont stockées dans une table de travail temporaire. Ces données peuvent être affichées pour chaque transition. Pour examiner les données transmises entre les activités :

1. Sélectionnez une transition.
1. Dans le volet des propriétés, cliquez sur **[!UICONTROL Aperçu du schéma]** pour afficher le schéma de la table de travail. Sélectionnez **[!UICONTROL Prévisualiser les résultats]** pour afficher les données transportées.

![](assets/transition.png){zoomable="yes"}

### Indicateurs d’exécution d’activité {#activities}

Les indicateurs visuels de statut vous aident à comprendre les performances de chaque activité :

| Indicateur visuel | Description |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | L’activité est en cours d’exécution. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | L’activité nécessite votre attention. Vous devez, par exemple, confirmer l’envoi d’une diffusion ou prendre une mesure nécessaire. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | L’activité a rencontré une erreur. Pour résoudre ce problème, ouvrez les journaux de campagne orchestrés pour plus d’informations. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | L’activité a été exécutée correctement. |

### Logs et tâches {#logs-tasks}

>[!CONTEXTUALHELP]
>id="ajo_campaign_logs"
>title="Logs et tâches"
>abstract="L’écran **Logs et tâches** fournit un historique de l’exécution de la campagne orchestrée, enregistrant toutes les actions des utilisateurs et utilisatrices ainsi que les erreurs rencontrées."

La surveillance des logs et des tâches est une étape essentielle pour analyser vos campagnes orchestrées et vérifier qu’elles s’exécutent correctement. Les journaux et les tâches sont accessibles à partir du bouton **[!UICONTROL Journaux]** disponible en mode test et actif dans la barre d’outils de la zone de travail ou dans le volet des propriétés de chaque activité.

L’écran **[!UICONTROL Logs et tâches]** fournit un historique complet de l’exécution de votre campagne, enregistrant toutes les actions des utilisateurs et les erreurs rencontrées.

![](assets/workflow-logs.png){zoomable="yes"}

Deux types d’informations sont disponibles :

* L’onglet **[!UICONTROL Log]** contient l’historique chronologique de toutes les opérations et erreurs.
* L’onglet **[!UICONTROL Tâches]** détaille la séquence d’exécution étape par étape des activités.

Sous les deux onglets, vous pouvez choisir les colonnes à afficher et leur ordre, appliquer des filtres et trouver rapidement des informations à l’aide du champ de recherche.
