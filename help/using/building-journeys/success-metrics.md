---
solution: Journey Optimizer
product: journey optimizer
title: Publier le parcours
description: Découvrez comment créer des rapports sur la mesure de parcours de votre choix.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: publication, parcours, dynamique, validité, vérifier
hide: true
hidefromtoc: true
source-git-commit: 3d0cda6f206799b7a96b60ee43a1ad3f9f0600cf
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 12%

---

# Configurer et suivre votre mesure de parcours {#success-metrics}

Grâce aux mesures en parcours, vous pouvez mesurer efficacement l’impact de vos activités en suivant leurs performances par rapport à des mesures prédéfinies.
En suivant ces mesures, vous pouvez évaluer les performances de votre parcours, identifier les points à améliorer et prendre des décisions éclairées pour améliorer l’engagement des clients.

## Conditions préalables {#prerequisites}

Avant d’utiliser votre mesure de parcours, vous devez ajouter un jeu de données qui inclut le `Commerce Details` [groupe de champs](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=fr#field-group){target="_blank"}.

## Mesures disponibles {#metrics}

La liste des mesures varie en fonction des [groupes de champs](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=fr#field-group){target="_blank"} inclus dans votre jeu de données.

Si votre jeu de données n’est pas configuré, seules les mesures suivantes seront disponibles : **[!UICONTROL Taux de clics]**, **[!UICONTROL Clic unique]**, **[!UICONTROL Taux de clics]** et **[!UICONTROL Taux d’ouverture]**.

Notez qu’avec une licence Customer Journey Analytics, vous pouvez créer des mesures de succès personnalisées. [En savoir plus](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-components/cja-calcmetrics/cm-workflow/participation-metric)


| Mesures | Groupe de champs associé |
|-|-|
| Clics | Aucun groupe de champs requis |
| Clics uniques | Aucun groupe de champs requis |
| Taux de clics (CTR) | Aucun groupe de champs requis |
| Taux d’ouverture de clics publicitaires (CTOR) | Aucun groupe de champs requis |
| Pages vues | Groupe de champs Web |
| Lancements d’application | Groupe de champs mobiles |
| Premiers lancements d’application | Groupe de champs mobiles |
| Installations de l’application | Groupe de champs mobiles |
| Mises à niveau de l’application | Groupe de champs mobiles |
| Achats | Groupe de champs Détails Commerce |
| Passages en caisse | Groupe de champs Détails Commerce |
| Ajouts au panier | Groupe de champs Détails Commerce |
| Ouvertures de panier | Groupe de champs Détails Commerce |
| Consultations du panier | Groupe de champs Détails Commerce |
| Suppressions de panier | Groupe de champs Détails Commerce |
| Consultations produits | Groupe de champs Détails Commerce |
| Enregistrer pour plus tard | Groupe de champs Détails Commerce |

## Attribution {#attribution}

Chaque mesure est fournie avec une attribution définie qui détermine les points de contact ou interactions qui ont contribué à un résultat spécifique.

* **Attribution des mesures avec la licence Journey Optimizer** :

  Avec la licence Journey Optimizer uniquement, l’intervalle de recherche en amont disponible maximal pour toute mesure sélectionnée est défini sur 7 jours. Pour ces mesures, le modèle d’attribution est défini par défaut sur **Dernière touche**, c’est-à-dire l’interaction la plus récente avant la conversion.

  Par exemple, vous pouvez suivre si un achat a été effectué après qu’un client a interagi avec votre parcours au cours des 7 derniers jours.

* **Attribution des mesures avec la licence Customer Journey Analytics** :

  Avec les licences Journey Optimizer et Customer Journey Analytics, vous pouvez créer des mesures personnalisées avec des paramètres d’attribution spécifiques ou modifier les attributions des mesures intégrées.

  En savoir plus sur les [Modèles d’attribution](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-dataviews/component-settings/attribution#attribution-models)

## Attribuer votre mesure de Parcours {#assign}

Pour commencer à effectuer le suivi de votre mesure de parcours, procédez comme suit :

1. Dans le menu **[!UICONTROL Parcours]**, cliquez sur **[!UICONTROL Créer un Parcours]**.

1. Modifiez le volet de configuration du parcours pour attribuer un nom au parcours et définir ses propriétés. Découvrez comment définir les propriétés de votre parcours dans [cette page](../building-journeys/journey-properties.md).

1. Choisissez vos **[!UICONTROL mesures de Parcours]** qui seront utilisées pour mesurer l’efficacité de votre parcours.

   Notez que les mesures s’appliquent au parcours lui-même et à tous les éléments du parcours.

   ![](assets/success_metric.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

1. Concevez votre parcours avec les **[!UICONTROL activités]** nécessaires.

1. Testez et publiez votre parcours.

1. Ouvrez votre rapport de parcours pour suivre les performances de la mesure de succès qui vous a été attribuée.

   La mesure que vous avez choisie s’affiche dans le tableau KPI et statistiques des Parcours du rapport.

   ![](assets/success_metric_2.png)
