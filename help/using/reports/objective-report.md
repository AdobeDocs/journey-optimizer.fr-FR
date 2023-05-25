---
solution: Journey Optimizer
product: journey optimizer
title: Rapport global de campagne
description: Découvrez comment utiliser les données du rapport global de campagne
feature: Reporting
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 6b8983d3f3fa989bd7190fc6a8b51fa8989b2293
workflow-type: tm+mt
source-wordcount: '479'
ht-degree: 71%

---

# Rapport global de campagne {#objective-report}

Rapport global de campagne est accessible directement à partir de votre campagne à l’aide de la fonction **[!UICONTROL Afficher le rapport]** bouton .

Le **[!UICONTROL Rapport global]** de campagne est divisé en différents widgets présentant le succès et les erreurs de votre campagne. Chaque widget peut être redimensionné et supprimé si nécessaire. Pour plus d&#39;informations à ce propos, consultez cette [section](../reports/global-report.md#modify-dashboard).

Pour obtenir la liste détaillée de chaque mesure disponible dans Adobe Journey Optimizer, reportez-vous à [cette page](global-report.md#list-of-components-global.md).

## Onglet Campagne {#campaign-global-objectives}

### Diffusion {#delivery-global-objectives}

![](assets/campaign_report_global_1.png)

Le widget **[!UICONTROL Statistiques de la campagne]** présente les principales informations relatives à votre Campagne :

* **[!UICONTROL Profils entrés]** : nombre de profils ayant commencé le parcours.

* **[!UICONTROL Actions réalisées]** : nombre total de fois uniques où une action dans le parcours a été réalisée.

* **[!UICONTROL Échec des actions en %]** : nombre total de fois uniques où une action a échoué dans le parcours par rapport au nombre total de fois uniques où une action a été réalisée.

### Rapport d’objectifs {#objective-global}

>[!AVAILABILITY]
>
>Le **Rapport Objectifs** Cette fonctionnalité est actuellement disponible uniquement pour un ensemble d’organisations (disponibilité limitée). Pour en savoir plus, contactez votre représentant Adobe.

![](assets/performance_report.gif)

Le **[!UICONTROL Objectifs]** vous permet d’affiner davantage les rapports de vos diffusions en ciblant une mesure spécifique.

Les **[!UICONTROL objectifs]** répertoriés sont liés aux **[!UICONTROL Jeux de données]** définissant une connexion à un système afin de récupérer des informations supplémentaires. Une liste d’**[!UICONTROL objectifs]** intégrés est disponible, mais vous pouvez l’accroître en ajoutant un nouveau **[!UICONTROL Jeu de données]**. Pour la procédure détaillée, consultez cette [section](../campaigns/reporting-configuration.md).

Après avoir sélectionné les objectifs que vous souhaitez cibler, les deux widgets **[!UICONTROL Présentation des performances]** et **[!UICONTROL Objectif de la campagne]** fournissent un résumé détaillé des performances de votre diffusion.

Avec le widget **[!UICONTROL Objectif de la campagne]**, vous pouvez également choisir de comparer votre objectif principal à une autre mesure.

### Rapport d’expérience {#experimentation-global-objectives}

![](assets/experimentation_report_3.png)

Le **[!UICONTROL Expérience]** fournit des informations clés sur les performances de chaque variante et identifie la variante la plus réussie.

Notez que la définition de meilleure performance peut prendre un certain temps, elle sera représentée par cette icône ![](assets/experimentation_report_1.png).

+++En savoir plus sur les différents widgets et mesures disponibles pour le rapport d’expérience.

Le widget **[!UICONTROL Résultat de l’expérience]** décrit les performances de chaque variante. Vous pouvez modifier votre ligne de base en sélectionnant l’un des traitements du menu déroulant **[!UICONTROL Ligne de base]**. Le meilleur traitement sera signalé par une icône en forme d’étoile.

Le tableau présente les mesures suivantes :

* **[!UICONTROL Effet élévateur sur la ligne de base]**: Mesure de l’amélioration en pourcentage du taux de conversion d’un traitement donné par rapport à la ligne de base.

* **[!UICONTROL Confiance]** : preuves qu’un traitement donné est le même que le traitement de la ligne de base. [En savoir plus](../campaigns/experiment-calculations.md#understand-confidence)

* **[!UICONTROL Clics sortants uniques]** : nombre total de clics sur les canaux sortants.

* **[!UICONTROL Profils]** : nombre de profils ciblés pour ce traitement.

* **[!UICONTROL Clics/profils sortants uniques]**: Valeur totale de la mesure de succès, précédemment sélectionnée lors de la création de vos expériences, divisée par le nombre de profils.

Le **[!UICONTROL Intervalle de confiance]** Le graphique mesure l’incertitude quant à l’amélioration. Il détaille la différence en pourcentage de performance entre la ligne de base et le traitement le plus performant. [En savoir plus](../campaigns/experiment-calculations.md#confidence-intervals).
+++

Pour un examen approfondi de ces résultats et de leur interprétation, reportez-vous à [cette page](../campaigns/get-started-experiment.md#interpret-results).

