---
solution: Journey Optimizer
product: journey optimizer
title: Mettre en pause un parcours
description: Découvrez comment suspendre et reprendre un parcours en direct
feature: Journeys
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Disponibilité limitée" type="Informative"
keywords: publication, parcours, actif, validité, vérifier
source-git-commit: 2d7067782d6adc7fe5c458a575729d2293af2aaf
workflow-type: tm+mt
source-wordcount: '1196'
ht-degree: 3%

---

# Mettre en pause un parcours {#journey-pause}

>[!CONTEXTUALHELP]
>id="ajo_journey_pause"
>title="Mettre le parcours en pause"
>abstract="Mettre en pause un parcours dynamique pour empêcher l’entrée de nouveaux profils. Choisissez de supprimer les profils actuellement dans le parcours ou de les conserver en place. S’ils sont conservés, ils reprendront l’exécution à l’activité d’action suivante une fois le parcours redémarré. Parfait pour les mises à jour ou les arrêts d&#39;urgence sans perdre la progression."

Vous pouvez suspendre vos parcours dynamiques, effectuer toutes les modifications nécessaires et les reprendre à tout moment.<!--You can choose whether the journey is resumed at the end of the pause period, or whether it stops completely. --> Pendant la pause, vous pouvez [appliquer des filtres globaux](#journey-global-filters) pour exclure des profils en fonction de leurs attributs. Le parcours est automatiquement repris à l’issue de la période de pause. Vous pouvez également [reprendre manuellement](#journey-resume-steps).

>[!AVAILABILITY]
>
>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.


## Avantages clés {#journey-dry-run-benefits}

Les parcours de pause et de reprise offrent aux utilisateurs et aux utilisatrices du parcours davantage de contrôle et de flexibilité en permettant de suspendre temporairement les parcours en direct sans perturber l’expérience client. En pause, aucune communication n’est envoyée et les profils restent suspendus jusqu’à la reprise du parcours.

Cette fonctionnalité réduit le risque d’envoi de messages inattendus lors d’erreurs ou de mises à jour (par exemple : modification du contenu du message), prend en charge une gestion du parcours plus sûre et accroît la confiance des utilisateurs et utilisatrices. La visibilité des parcours en pause et de leur statut directement dans l’interface utilisateur améliore la transparence et l’agilité opérationnelle.

>[!CAUTION]
>
>Les autorisations de pause et de reprise des parcours sont limitées aux utilisateurs disposant de l’autorisation de haut niveau **[!DNL Publish journeys]**. Pour en savoir plus sur la gestion des droits d’accès des utilisateurs et des utilisatrices [!DNL Journey Optimizer], consultez [cette section](../administration/permissions-overview.md).

## Mécanismes de sécurisation et recommandations

* Une version de parcours peut être suspendue pendant 14 jours au maximum.
* Les parcours en pause sont pris en compte dans toutes les règles métier, de la même manière que s’ils étaient actifs.
* Les profils sont « ignorés » dans un parcours en pause lorsqu’ils atteignent une activité d’action. S’ils restent en attente pendant la mise en pause d’un parcours et quittent cette attente après sa reprise, ils poursuivront le parcours et ne seront pas ignorés.
* Même après la pause, à mesure que les événements continuent d’être traités, ces événements sont comptabilisés dans le nombre d’événements de Parcours par seconde, quota au-delà duquel la limitation est prise en compte pour l’unité.
* Les profils entrés sur le parcours mais ignorés pendant la pause seraient toujours comptabilisés comme des profils engageables.
* Lorsque les profils se maintiennent dans un parcours en pause, les attributs de profil sont actualisés au moment de la reprise
* Les conditions sont toujours exécutées dans des parcours en pause. Ainsi, si un parcours a été suspendu en raison de problèmes de qualité des données, toute condition préalable à un nœud d’action peut être évaluée avec des données incorrectes.
* Pour le parcours d’audience de lecture incrémentielle, la durée de pause est prise en compte. Par exemple, pour un parcours quotidien, s’il a été mis en pause le 2 et a repris le 5 du mois, alors l’exécution le 6 prendra tous les profils qualifiés du 1 au 6. Ce n’est pas le cas pour la qualification d’audience ou les parcours basés sur un événement (si une qualification d’audience ou un événement sont reçus pendant une pause, ces événements sont ignorés).
* Les parcours en pause sont comptabilisés dans le quota de parcours vivants.
* Le délai d’expiration global du parcours s’applique toujours aux parcours en pause. Par exemple, si un profil a été dans un parcours pendant 90 jours et que le parcours est suspendu, ce profil quittera toujours le parcours le 91 e jour.
* Si des profils sont conservés dans un parcours et que ce parcours reprend automatiquement au bout de quelques jours, les profils continuent le parcours et ne sont pas supprimés. Si vous voulez les laisser tomber, vous devez arrêter le parcours.
  <!--* There is a guardrail (at an org level) on the max number of profiles that can be held in paused journeys. This guardrail is per org, and is visible in the journey inventory on a new bar (only visible when there are paused journeys).-->

## Mise en pause d’un parcours {#journey-pause-steps}

Vous pouvez suspendre n’importe quel parcours **en ligne**.

Pour suspendre le parcours, procédez comme suit :

1. Ouvrez le parcours à mettre en pause.
1. Cliquez sur le bouton **...Plus** dans la section supérieure droite de la zone de travail du parcours, puis sélectionnez **Pause**.

   ![Bouton Mettre en pause le parcours ](assets/pause-journey-button.png){width="80%" align="left"}

1. Sélectionnez le mode de gestion des profils qui se trouvent actuellement dans le parcours.

   ![Options de parcours de pause](assets/pause-confirm.png){width="50%" align="left"}

   Vous pouvez effectuer les actions suivantes :

   * **En attente** profils - Les profils attendront que le parcours soit repris
   * **Ignorer** profils - Les profils seront exclus du parcours sur le nœud d’action suivant

1. Cliquez sur le bouton **Pause** pour confirmer.

Dans la liste de vos parcours, vous pouvez mettre en pause un ou plusieurs parcours **en ligne**. Pour suspendre un groupe de parcours (_pause en bloc_), sélectionnez-les dans la liste et cliquez sur le bouton **Pause** dans la barre bleue en bas de l’écran. Le bouton **Pause** n’est disponible que lorsque des parcours **en direct** sont sélectionnés.

![Mettre en pause en bloc deux parcours actifs de la barre inférieure](assets/bulk-pause-journeys.png){width="80%" align="left"}


## Reprise d’un parcours en pause {#journey-resume-steps}

>[!CONTEXTUALHELP]
>id="ajo_journey_pause"
>title="Reprendre le parcours"
>abstract="Reprenez un parcours en pause pour permettre aux nouveaux profils de rejoindre à nouveau le parcours. Si les profils étaient en attente pendant la pause, ils continueront leur parcours. Idéal pour redémarrer les parcours en toute sécurité après des mises à jour ou des pauses."

Les parcours en pause sont automatiquement repris à l’issue d’une période de pause maximale de 14 jours. Ils peuvent être repris manuellement à tout moment. La reprise d’un parcours en pause permet à de nouveaux profils de saisir à nouveau. Si les profils étaient en attente pendant la pause, ils continueront leur parcours. Idéal pour redémarrer les parcours en toute sécurité après des mises à jour ou des pauses.

Pour reprendre un parcours en pause et recommencer à écouter les événements de parcours, procédez comme suit :

1. Ouvrez le parcours que vous souhaitez reprendre.
1. Cliquez sur le bouton **...Plus** dans la section supérieure droite de la zone de travail du parcours, puis sélectionnez **Reprendre**.

   Le parcours passe à l’état **Reprise**. Le passage du statut **Reprise** au statut **Actif** peut prendre un certain temps : tous les profils doivent être repris pour que le parcours soit à nouveau **Actif**.

1. Cliquez sur le bouton **Reprendre** pour confirmer.


Dans la liste de vos parcours, vous pouvez reprendre un ou plusieurs parcours **en pause**. Pour reprendre un groupe de parcours (_reprise en bloc_), sélectionnez-les et cliquez sur le bouton **Reprendre** situé dans la barre bleue en bas de l’écran. Notez que le bouton **Reprendre** n’est disponible que lorsque les parcours **En pause** sont sélectionnés.


## Application d’un filtre global aux profils d’un parcours en pause  {#journey-global-filters}

Lorsqu’un parcours est en pause, vous pouvez l’appliquer en fonction des attributs de profil. Ce filtre permet d’exclure les profils qui correspondent à l’expression définie au moment de la reprise. Les profils correspondant aux critères qui se trouvent actuellement dans le parcours le quitteront et les nouveaux profils qui tenteront d’y accéder seront bloqués.

Par exemple, pour exclure tous les clients français des communications marketing vers la France, procédez comme suit :

1. Accédez au parcours en pause que vous souhaitez modifier.

1. Cliquez sur l’icône **Critères de sortie et filtre global**.

   ![Ajouter un filtre global à un parcours en pause](assets/add-global-filter.png){width="50%" align="left"}

1. Dans les paramètres **Critères de sortie et filtre global**, définissez un filtre en fonction des attributs de profil.

1. Définissez l’expression pour exclure les profils dont l’attribut de pays est égal à France.

   ![Ajouter un filtre global à un parcours en pause](assets/add-country-filter.png){width="50%" align="left"}

1. Enregistrez votre filtre et cliquez sur le bouton **Mettre à jour le parcours** pour appliquer vos modifications.

1. [Reprendre le parcours ](#journey-resume-steps).

   Au moment de la reprise, tous les profils dont l’attribut de pays est défini sur France seront automatiquement exclus du parcours. Tous les nouveaux profils dont l’attribut de pays est défini sur France qui tentent d’entrer sur le parcours seront bloqués.

N’oubliez pas que les exclusions de profil pour les profils actuellement dans le parcours et pour les nouveaux profils ne se produiront que lorsqu’ils atteignent un nœud d’action.

>[!CAUTION]
>
>* Vous ne pouvez définir qu **un seul** global par parcours.
>
>* Vous pouvez uniquement créer, mettre à jour ou supprimer un filtre global dans les parcours **En pause**.