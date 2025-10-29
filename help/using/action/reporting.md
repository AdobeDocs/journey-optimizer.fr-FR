---
solution: Journey Optimizer
product: journey optimizer
title: Rapport de parcours
description: Découvrez comment utiliser les données du rapport de parcours.
feature: Reporting, Journeys
topic: Content Management
role: User
level: Intermediate
badge: label="Disponibilité limitée" type="Informative"
source-git-commit: b93d2288156713ac7479eef491f6104df1955a18
workflow-type: tm+mt
source-wordcount: '431'
ht-degree: 3%

---

# Surveillance des actions personnalisées {#reporting}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_custom_actions_monitor"
>title="Surveillance des actions personnalisées"
>abstract="La page de création de rapports **[!UICONTROL Action personnalisée]** vous permet de suivre les performances et la fiabilité des appels API que vos parcours effectuent à des systèmes tiers."

>[!AVAILABILITY]
>
>La création de rapports d’actions personnalisées n’est actuellement disponible que pour un ensemble d’organisations (disponibilité limitée).

La page de création de rapports **[!UICONTROL Action personnalisée]** vous permet de surveiller la fiabilité et les performances des appels API effectués depuis vos parcours vers des systèmes tiers. Ces rapports vous aident à identifier rapidement les problèmes d’intégration, les goulets d’étranglement de latence ou les limites de limitation/plafonnement qui peuvent avoir un impact sur la diffusion.

La page de création de rapports d’action personnalisée fonctionne comme d’autres rapports à tout moment dans Journey Optimizer. Pour plus d’informations sur les fonctionnalités des tableaux de bord, consultez [cette documentation](../reports/report-cja-manage.md).

Pour accéder à la page de création de rapports **[!UICONTROL Action personnalisée]**, cliquez sur ![](assets/do-not-localize/Smock_Monitoring_18_N.svg) sur la page d’accueil **[!UICONTROL Actions]**.

![](assets/monitor-1.png)

➡️ [En savoir plus sur la configuration des actions personnalisées](../action/about-custom-action-configuration.md)

## KPI {#kpis}

![](assets/monitor-2.png)

Les indicateurs clés de performance **[!UICONTROL action personnalisée]** servent de tableau de bord centralisé, fournissant une vue consolidée de l’intégrité opérationnelle et de la fiabilité de vos appels d’action personnalisée. Ces mesures vous permettent d’évaluer les performances, d’identifier les goulets d’étranglement et d’assurer des intégrations stables avec des systèmes externes.

+++ En savoir plus sur les KPI des actions personnalisées

* **[!UICONTROL Appels réussis]** : nombre total d&#39;appels HTTP ayant renvoyé une réponse valide sans erreur.

* **[!UICONTROL erreurs 4xx/5xx]** : nombre d’appels ayant échoué en raison d’erreurs côté client (4xx) ou côté serveur (5xx), mettant en évidence des problèmes de configuration ou des échecs de point d’entrée.

* **[!UICONTROL Délais d’expiration]** : nombre d’appels ayant échoué, car ils ont dépassé le temps de réponse maximal. Cela permet de faire apparaître des problèmes de latence ou de performances avec les points d’entrée externes.

* **[!UICONTROL Appels limités]** : nombre d’appels bloqués en raison des limites de limitation, ce qui permet de s’assurer que les systèmes en aval ne sont pas surchargés.

* **[!UICONTROL RPS moyenne]** : nombre de demandes par seconde traitées par l’action personnalisée sur la période sélectionnée.

+++

## Appels au fil du temps {#calls}

![](assets/monitor-3.png)

Le graphique **[!UICONTROL Appels au fil du temps]** affiche la tendance des KPI des appels HTTP sur la période sélectionnée pour le rapport. La granularité de la série temporelle dépend de la période sélectionnée. Par exemple :

* Pour un rapport sur 7 jours, chaque point de données affiche les KPI pour un jour.
* Si vous sélectionnez une période d’un jour, le graphique affiche les KPI par heure.
* Si vous sélectionnez une période d’une heure, le graphique affiche les KPI par minute.

➡️[Voir la section KPI pour une description des mesures d’appel HTTP](#kpis)

## Répartition des appels {#breakdown}

![](assets/monitor-4.png)

Le tableau **[!UICONTROL Répartition des appels]** fournit une répartition hiérarchique des mesures d’appels HTTP, des mesures globales par point d’entrée au niveau supérieur aux mesures par action personnalisée à l’aide de chaque point d’entrée jusqu’aux parcours qui en dépendent au niveau inférieur.

➡️[Voir la section KPI pour une description des mesures d’appel HTTP](#kpis)


