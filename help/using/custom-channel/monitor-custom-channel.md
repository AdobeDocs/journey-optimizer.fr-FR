---
title: Gestion et surveillance des canaux personnalisés
description: Découvrez comment gérer le cycle de vie des canaux personnalisés et des configurations de canal, et surveiller les performances des diffusions par le biais des rapports Adobe Journey Optimizer.
feature: Channel Configuration
topic: Content Management
role: User
level: Beginner
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '948'
ht-degree: 6%

---


# Surveillance des canaux personnalisés {#monitor-custom-channel}

Une fois qu’un canal personnalisé est créé et activé, vous pouvez [gérer son cycle de vie](create-custom-channel.md#access-channel-builder) et surveiller les performances des diffusions via l’interface [!DNL Journey Optimizer].

## Utilisation des rapports de campagne et de parcours {#reporting}

[!DNL Journey Optimizer] fournit des rapports prêts à l’emploi pour les canaux personnalisés.

Les mesures suivantes sont disponibles pour les canaux personnalisés dans les rapports en direct (24 h) et globaux (CJA).<!--TBC and add or replace with CJA link when available-->

| Mesure | Description |
|--------|-------------|
| **Tentatives de diffusion** | Nombre total de messages envoyés au point d’entrée externe. |
| **Diffusions réussies** | Messages pour lesquels le point d’entrée a renvoyé une réponse HTTP 2xx. |
| **Profils ciblés** | Nombre de profils uniques atteints. |
| **Clics** | Nombre de clics sur les liens suivis dans la payload. Nécessite un sous-domaine délégué pour les canaux personnalisés. |
| **Erreurs/Échecs** | Nombre de tentatives de diffusion ayant échoué, avec répartition par raison d’erreur. |

En savoir plus sur les [rapports dynamiques](../reports/live-report.md) et [rapports globaux](../reports/report-gs-cja.md). Pour plus d’informations sur les fonctionnalités de reporting, consultez [cette documentation](../reports/report-cja-manage.md).

<!--
### Journey reports {#journey-reports}

To view delivery data for a custom channel action in a journey:

1. Open the journey from the **[!UICONTROL Journeys]** list.
1. Click **[!UICONTROL View report]** in the top-right area.
   * **[!UICONTROL Live report]** – Data for the last 24 hours.
   * **[!UICONTROL All time]** – Full lifetime data via Customer Journey Analytics (CJA).

### Campaign reports {#campaign-reports}

To view delivery data for a custom channel campaign:

1. Open the campaign from the **[!UICONTROL Campaigns]** list.
1. Click **[!UICONTROL Reports]** in the top-right area.

The campaign report includes execution count, successful deliveries, errors, and click data (if link tracking is enabled).
-->

## Surveiller les performances de diffusion {#monitoring}

Outre les rapports de campagne et de parcours, [!DNL Journey Optimizer] fournit un tableau de bord personnalisé dédié à la surveillance des canaux. Pour y accéder, sélectionnez **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Créateur de canaux]** > **[!UICONTROL Surveillance des canaux personnalisés]**.

![Tableau de bord de surveillance des canaux personnalisés](assets/custom_channel_monitoring_dashboard.png){width="100%"}

Ce tableau de bord vous permet de surveiller la fiabilité et les performances des appels API que [!DNL Journey Optimizer] effectuez à vos points d’entrée externes lors de la diffusion de messages de canal personnalisés. Utilisez-le pour repérer rapidement les problèmes d’intégration, de latence et de limitation.

Le tableau de bord **[!UICONTROL Surveillance des canaux personnalisés]** fonctionne comme d’autres rapports à tout moment dans [!DNL Journey Optimizer]. Vous pouvez sélectionner une période, filtrer par canal ou point d’entrée et analyser en profondeur pour afficher les campagnes et les parcours qui reposent sur chaque canal personnalisé. [En savoir plus](../reports/report-cja-manage.md)

### Mesures de canal personnalisées {#monitoring-kpis}

La section **[!UICONTROL Mesures de canal personnalisé]** fournit une vue consolidée de l’intégrité opérationnelle et de la fiabilité de vos appels de canal personnalisé.

![Mesures de canal personnalisées](assets/custom_channel_metrics.png){width="100%"}

+++ En savoir plus sur les mesures de canal personnalisé

* **[!UICONTROL Appels réussis]** : nombre total d’appels HTTP ayant renvoyé une réponse valide sans erreur.

* **[!UICONTROL Erreurs 4xx/5xx]** : nombre d’appels ayant échoué en raison d’erreurs côté client (4xx) ou côté serveur (5xx), mettant en évidence des problèmes de configuration ou des échecs de point d’entrée.

* **[!UICONTROL Appels de dépassement de délai]** : nombre d’appels ayant échoué, car ils ont dépassé le temps de réponse maximal. Cela permet de faire apparaître des problèmes de latence ou de performances avec les points d’entrée externes.

* **[!UICONTROL Échecs de pré-appel]** : nombre d’envois de canal personnalisé ayant échoué avant que l’appel HTTP ne soit effectué vers le point d’entrée externe. Ces défaillances se produisent dans la couche d’infrastructure de [!DNL Journey Optimizer], et non dans votre système externe. Il existe trois catégories :

  | Catégorie | Description |
  |----------|-------------|
  | **Échecs d’authentification** (`AUTH_*`) | [!DNL Journey Optimizer] n’a pas pu obtenir ou actualiser le jeton OAuth ou les informations d’identification nécessaires pour appeler le point d’entrée. Vérifiez que les informations d’identification de l’API liées à la configuration du canal sont valides et n’ont pas expiré. |
  | **Erreurs de génération de requête** (`REQUEST_GENERATION_ERROR`) | [!DNL Journey Optimizer] n’a pas pu créer de requête HTTP valide, par exemple, parce qu’un modèle d’URL n’a pas pu être résolu ou qu’un champ de personnalisation obligatoire était manquant. |
  | **Erreurs d’analyse HTTP** (`HTTP_PARSE_ERROR`) | [!DNL Journey Optimizer] a reçu une réponse du point d’entrée mais n’a pas pu l’analyser dans une structure utilisable. |

  >[!TIP]
  >
  >Les échecs de pré-appel indiquent un problème du côté [!DNL Journey Optimizer] ou dans la configuration du canal, plutôt qu’un problème avec votre point d’entrée externe. Commencez la résolution des problèmes en examinant vos informations d’identification API et les champs de payload obligatoires.

* **[!UICONTROL Latence moyenne]** : temps de réponse moyen de bout en bout (en millisecondes) pour tous les appels HTTP, y compris les appels réussis, les erreurs et les délais d’expiration.

<!--
* **[!UICONTROL Capped calls]**: Number of calls that were blocked due to capping limits, ensuring downstream systems are not overloaded.

* **[!UICONTROL Average RPS]**: Number of requests per second processed by the custom channel over the selected time range.

* **[!UICONTROL Average successful latency]**: Average end-to-end response time (in milliseconds) for successful calls only, excluding failed requests and timeouts.

* **[!UICONTROL Average queue time]**: Average time (in milliseconds) calls spent waiting in the execution queue before being sent. This only applies to throttled endpoints, where [!DNL Journey Optimizer] queues calls when the throughput limit is reached.
-->

+++

### Résultats des canaux personnalisés au fil du temps {#outcomes-overtime}

![Résultats de canal personnalisés au fil du temps](assets/custom_channel_metrics.png){width="100%"}

Le graphique **[!UICONTROL Résultats des canaux personnalisés au fil du temps]** affiche la tendance des KPI des appels HTTP sur la période sélectionnée. La granularité de la série temporelle dépend de la période sélectionnée :

* Pour un rapport sur 7 jours, chaque point de données affiche les KPI pour un jour.
* Pour une période d’un jour, le graphique affiche les indicateurs de performance clés par heure.
* Pour une période d’une heure, le graphique affiche les KPI par minute.

### Latence dans le temps {#latency-overtime}

![Latence de canal personnalisé au fil du temps](assets/custom_channel_latency.png){width="100%"}

Le graphique **[!UICONTROL Latence au fil du temps]** permet de visualiser la tendance des mesures de latence sur la période sélectionnée. Cette vue de série temporelle vous permet de suivre les modèles de performances, d’identifier les périodes de latence de pointe et de surveiller l’impact des optimisations ou des modifications du système au fil du temps.

### Répartition du résultat du canal personnalisé {#outcome-breakdown}

![Répartition des résultats du canal personnalisé](assets/custom_channel_latency.png){width="100%"}

Le tableau **[!UICONTROL Répartition des résultats du canal personnalisé]** fournit une répartition hiérarchique des mesures d’appel HTTP, depuis les mesures globales par point d’entrée au niveau supérieur, jusqu’aux mesures par canal personnalisé utilisant ce point d’entrée, en passant par les campagnes et les parcours qui reposent sur ces mesures au niveau inférieur.

### Répartition de la latence {#latency-breakdown}

Le tableau **[!UICONTROL Répartition de la latence]** fournit une répartition détaillée des mesures de latence sur vos canaux personnalisés. Cette vue vous permet d’identifier les points d’entrée ou canaux spécifiques qui rencontrent des problèmes de performances, ce qui vous permet d’identifier et de résoudre les goulots d’étranglement de latence de manière efficace.

### Insight Builder {#insight-builder}

Utilisez **[!UICONTROL Insight Builder]** pour créer des visualisations et des tableaux de bord personnalisés en fonction des mesures de canal personnalisées. Cet outil vous permet de combiner plusieurs indicateurs de performance clés, d’appliquer des filtres et de créer des vues personnalisées qui correspondent à vos besoins de surveillance et de création de rapports. [En savoir plus](../reports/report-cja-manage.md#insight-builder)

## Dépannage {#troubleshooting}

Si vous rencontrez des problèmes avec votre canal personnalisé, le tableau suivant répertorie les symptômes courants, les causes possibles et les résolutions recommandées.

| Symptôme | Cause possible | Résolution |
|---------|----------------|------------|
| **Erreurs HTTP 401/403** | Échec de l&#39;authentification — informations d&#39;identification expirées ou incorrectes. | Mettez à jour les informations d’identification dans **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Informations d’identification d’API]**. |
| **Erreurs HTTP 429** | Le point d’entrée externe limite les requêtes provenant de [!DNL Journey Optimizer]. | Passez en revue les limites de taux de votre point d’entrée. Réduisez le paramètre de limitation dans la configuration de la stratégie du créateur de canaux. |
| **Erreurs HTTP 5xx** | Le système externe est hors service ou renvoie des erreurs de serveur. | Vérifiez le tableau de bord d’intégrité de votre système externe. Configurez les chemins d’erreur sur l’activité d’action de parcours pour gérer les échecs transitoires de manière appropriée. |
| **Jetons de personnalisation non résolus** | L’expression fait référence à un attribut qui n’est pas présent sur le profil. | Vérifiez que le chemin d’accès de l’attribut XDM est correct. Ajoutez une valeur de secours par défaut : `{{profile.person.name.firstName \| default("Valued Customer")}}`. |
| **Erreur de validation du champ obligatoire** | Un champ de payload obligatoire n’a aucune valeur au moment de la création. | Assurez-vous que tous les champs obligatoires sont renseignés dans l’éditeur de contenu. Vous pouvez également supprimer la contrainte requise dans le Créateur de canaux si le champ est vraiment facultatif. |

<!--
## Related resources {#related}

* [Get started with custom channels](get-started-custom-channel.md)
* [Configure a custom channel](custom-channel-configuration.md)
* [Global report overview](../reports/report-gs-cja.md)
* [Journey live report](../reports/live-report.md
-->