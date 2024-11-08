---
solution: Journey Optimizer
product: journey optimizer
title: Rapport de campagne
description: Découvrez comment utiliser les données d’expérimentation du rapport de campagne.
feature: Reporting
topic: Content Management
role: User
level: Intermediate
source-git-commit: 47482adb84e05fe41eb1c50479a8b50e00469ec4
workflow-type: ht
source-wordcount: '279'
ht-degree: 100%

---

# Rapport d’expérimentation de campagne {#campaign-global-report-cja-experimentation}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment_click"
>title="Mesure de succès"
>abstract="Valeur totale de la mesure de succès, précédemment sélectionnée lors de la création de vos expériences, divisée par le nombre de profils."

## Expérimentation {#experimentation}

L’onglet **[!UICONTROL Expérimentation]** fournit des informations clés sur les performances de chaque variante et identifie la variante la plus réussie.

Notez que la définition de la meilleure performance peut prendre un certain temps. Si votre expérience échoue, elle est définie sur **Non concluant**.

![](assets/cja-experimentation-1.png)

### KPI d’expérimentation {#experimentation-kpis}

![](assets/cja-experimentation-kpis.png)

Les indicateurs clés de performance (KPI) d’**[!UICONTROL expérimentation]** fonctionnent comme un tableau de bord global, fournissant une analyse des mesures essentielles associées à votre expérimentation.

+++ En savoir plus sur les mesures des KPI d’expérimentation

* **[!UICONTROL Effet élévateur]** : mesure de l’amélioration en pourcentage du taux de conversion d’un traitement donné par rapport à la ligne de base.

* **[!UICONTROL Confiance]** : preuves qu’un traitement donné est le même que le traitement de la ligne de base. [En savoir plus](../content-management/experiment-calculations.md#understand-confidence)

+++

### Variante par clics entrants {#variant-inbound}

![](assets/cja-experimentation-variants.png)

Le widget **[!UICONTROL Variante par clics entrants]** décrit les performances de chaque variante.
Pour un examen approfondi de ces résultats et de leur interprétation, reportez-vous à [cette page](../content-management/get-started-experiment.md#interpret-results).

+++ En savoir plus sur les mesures de variante par clics entrants

* **[!UICONTROL Personnes]** : nombre de profils qui sont qualifiés en tant que profils cibles pour vos messages.

* **[!UICONTROL Clics entrants]** : nombre total de clics sur les canaux sortants.

* **[!UICONTROL Taux de conversion]** : valeur totale de la mesure de succès, précédemment sélectionnée lors de la création de vos expériences, divisée par le nombre de profils.

* **[!UICONTROL Effet élévateur]** : mesure de l’amélioration en pourcentage du taux de conversion d’un traitement donné par rapport à la ligne de base.

* **[!UICONTROL Confiance]** : preuves qu’un traitement donné est le même que le traitement de la ligne de base. [En savoir plus](../content-management/experiment-calculations.md#understand-confidence)

<!--
* **[!UICONTROL Confidence Upper bound]**:

* **[!UICONTROL Confidence Lower bound]**:
-->
+++

### Taux de conversion des clics entrants {#conversion-rate}

![](assets/cja-experimentation-conversion.png)

Le graphe **[!UICONTROL Intervalle de confiance]** mesure l’incertitude quant à l’amélioration. Il indique la différence de performance en pourcentage entre la ligne de base et le traitement le plus performant. [En savoir plus](../content-management/experiment-calculations.md#confidence-intervals).
