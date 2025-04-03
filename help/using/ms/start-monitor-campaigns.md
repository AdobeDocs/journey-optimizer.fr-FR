---
solution: Journey Optimizer
product: journey optimizer
title: Démarrer et surveiller des campagnes à plusieurs étapes avec Adobe Journey Optimizer
description: Découvrez comment démarrer et surveiller des campagnes à plusieurs étapes avec Adobe Journey Optimizer.
hide: true
hidefromtoc: true
exl-id: 5fc2d1d6-75c3-4b45-bb2b-09982b9bd5ed
source-git-commit: 990d49202a790b5a117a7da665ed32f52f27b554
workflow-type: tm+mt
source-wordcount: '571'
ht-degree: 43%

---

# Démarrer et surveiller vos campagnes orchestrées {#start-monitor}

<!--
<audio controls><source src="../ms/assets/do-not-localize/sound.mp3" type="audio/mpeg">Your browser does not support the audio element.</audio> -->

>[!CONTEXTUALHELP]
>id="ajo_campaign_publication"
>title="Publier la campagne orchestrée"
>abstract="Pour démarrer votre campagne, vous devez la publier. Assurez-vous que tous les avertissements sont effacés avant la publication."


Une fois que vous avez créé et conçu les tâches à effectuer dans la zone de travail, vous pouvez les publier et contrôler leur exécution.

## Démarrer une campagne en plusieurs étapes {#start}

Pour démarrer une campagne à plusieurs étapes, accédez à l’onglet **[!UICONTROL À plusieurs étapes]** du menu **[!UICONTROL Campagne]** et sélectionnez la campagne à démarrer, puis cliquez sur le bouton **[!UICONTROL Démarrer]** dans le coin supérieur droit de la zone de travail.

Une fois la campagne à plusieurs étapes en cours d’exécution, chaque activité de la zone de travail est exécutée dans un ordre séquentiel, jusqu’à ce que la fin de la campagne à plusieurs étapes soit atteinte.

Vous pouvez suivre la progression des profils ciblés en temps réel à l’aide du flux visuel. Vous pouvez ainsi identifier rapidement le statut de chaque activité et le nombre de profils qu’elle contient.

![](assets/workflow-execution.png){zoomable="yes"}

## Transitions de campagne à plusieurs étapes {#transitions}

Dans les campagnes à plusieurs étapes, les données transportées d’une activité à une autre via des transitions sont stockées dans une table de travail temporaire. Ces données peuvent être affichées pour chaque transition. Pour cela, sélectionnez une transition pour ouvrir ses propriétés dans la partie droite de l’écran.

* Cliquez sur **[!UICONTROL Aperçu du schéma]** pour afficher le schéma de la table de travail.
* Cliquez sur **[!UICONTROL Aperçu des résultats]** pour visualiser les données véhiculées dans la transition sélectionnée.

![](assets/transition.png){zoomable="yes"}

## Surveiller l’exécution des activités {#activities}

Les indicateurs visuels situés dans le coin supérieur droit de chaque activité vous permettent de vérifier leur exécution :

| Indicateur visuel | Description |
|-----|------------|
| ![](assets/activity-status-pending.png){zoomable="yes"}{width="70%"} | L’activité est en cours d’exécution. |
| ![](assets/activity-status-orange.png){zoomable="yes"}{width="70%"} | L’activité nécessite votre attention. Vous devez, par exemple, confirmer l’envoi d’une diffusion ou prendre une mesure nécessaire. |
| ![](assets/activity-status-red.png){zoomable="yes"}{width="70%"} | L’activité a rencontré une erreur. Pour résoudre ce problème, ouvrez les journaux de campagne à plusieurs étapes pour plus d’informations. |
| ![](assets/activity-status-green.png){zoomable="yes"}{width="70%"} | L’activité a été exécutée correctement. |

## Surveiller les logs et les tâches {#logs-tasks}

La surveillance des logs et des tâches de workflows est une étape essentielle pour analyser vos campagnes à plusieurs étapes et vérifier qu&#39;elles s&#39;exécutent correctement. Les logs sont accessibles à partir de l’icône **[!UICONTROL Logs]**, située dans la barre d’outils d’actions et dans le volet des propriétés de chaque activité.

Le menu **[!UICONTROL Logs et tâches]** fournit un historique de l’exécution de la campagne à plusieurs étapes, enregistrant toutes les actions des utilisateurs et utilisatrices ainsi que les erreurs rencontrées.
![](assets/workflow-logs.png){zoomable="yes"}

Deux types d’informations sont disponibles :

* L’onglet **[!UICONTROL Log]** contient l’historique de l’exécution de toutes les activités de campagne à plusieurs étapes. Il répertorie par ordre chronologique les opérations réalisées et les erreurs d’exécution.
* L’onglet **[!UICONTROL Tâches]** permet de voir le séquencement de l’exécution des activités.

Sous les deux onglets, vous pouvez choisir les colonnes à afficher et leur ordre, appliquer des filtres et trouver rapidement des informations à l’aide du champ de recherche.

## Commandes d’exécution de campagne à plusieurs étapes {#execution-commands}

La barre d’actions située dans le coin supérieur droit propose des commandes qui vous permettent de gérer l’exécution de la campagne en plusieurs étapes. Vous pouvez effectuer les actions suivantes :

* **[!UICONTROL Démarrer]** / **[!UICONTROL Reprendre]** l&#39;exécution de la   Campagne à plusieurs étapes, qui adopte alors le statut En cours . Si la campagne à plusieurs étapes a été suspendue, elle reprend ; sinon, elle est lancée et les activités initiales sont alors activées.

* **[!UICONTROL Pause]** l’exécution de la campagne à plusieurs étapes, qui adopte alors le statut En pause. Aucune nouvelle activité ne sera activée jusqu’à la prochaine reprise, mais les opérations en cours ne sont pas suspendues.

* **[!UICONTROL Arrêter]** une campagne en cours d’exécution à plusieurs étapes, qui adopte alors le statut Terminé. Les opérations en cours sont interrompues si possible. Vous ne pouvez pas reprendre à partir de la campagne à plusieurs étapes à partir de l’endroit où elle a été arrêtée.
