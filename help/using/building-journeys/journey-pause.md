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
source-git-commit: cd85b58350b4f8829aa1bc925c151be9b061b170
workflow-type: tm+mt
source-wordcount: '704'
ht-degree: 6%

---

# Mettre en pause un parcours {#journey-pause}

Vous pouvez suspendre vos parcours dynamiques, effectuer toutes les modifications nécessaires et les reprendre à tout moment. Un parcours peut être suspendu pendant 14 jours au maximum. Vous pouvez choisir de reprendre le parcours à l’issue de la période de pause ou de l’arrêter complètement.


>[!AVAILABILITY]
>
>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.


## Avantages clés {#journey-dry-run-benefits}

Les parcours en pause et de reprise offrent aux marketeurs un meilleur contrôle et une plus grande flexibilité en permettant de suspendre temporairement les parcours en direct sans perturber l&#39;expérience client. En pause, aucune communication n’est envoyée et les profils restent suspendus jusqu’à la reprise du parcours.

Cette fonctionnalité réduit le risque d’envoi de messages inattendus lors d’erreurs ou de mises à jour (par exemple : modification du contenu du message), prend en charge une gestion du parcours plus sûre et accroît la confiance des utilisateurs et utilisatrices. La visibilité des parcours en pause et de leur statut directement dans l’interface utilisateur améliore la transparence et l’agilité opérationnelle.

>[!CAUTION]
>
>Les autorisations de pause et de reprise des parcours sont limitées aux utilisateurs disposant de l’autorisation de haut niveau **[!DNL Publish journeys]**. Pour en savoir plus sur la gestion des droits d’accès des utilisateurs et des utilisatrices [!DNL Journey Optimizer], consultez [cette section](../administration/permissions-overview.md).

## Mécanismes de sécurisation et recommandations

* Une version de parcours peut être suspendue pendant 14 jours au maximum.
* Les parcours en pause sont pris en compte dans toutes les règles métier, de la même manière que s’ils étaient actifs.
* Les profils sont « ignorés » dans un parcours en pause lorsqu’ils atteignent une activité d’action. S’ils restent en attente pendant la mise en pause d’un parcours et quittent cette attente lors de la reprise du parcours, ils continueront ce dernier et ne seront pas ignorés.
* Même après la pause, au fur et à mesure que les événements continuent à être traités, ces événements sont comptabilisés dans le quota de 5 ktps, après quoi la limitation est prise en compte pour l’unité.
* Les profils entrés sur le parcours mais ignorés pendant la pause seraient toujours comptabilisés comme des profils engageables.
* Lorsque les profils se maintiennent dans un parcours en pause, les attributs de profil sont actualisés au moment de la reprise
* Les conditions sont toujours exécutées dans des parcours en pause. Ainsi, si un parcours a été suspendu en raison de problèmes de qualité des données, toute condition préalable à un nœud d’action peut être évaluée avec des données incorrectes.
* Pour le parcours d’audience de lecture incrémentielle, la durée de pause est prise en compte. Par exemple, pour un parcours quotidien, s’il a été mis en pause le 2 et a repris le 5 du mois, alors l’exécution le 6 prendra tous les profils qualifiés du 1 au 6. Ce n’est pas le cas pour la qualification d’audience ou les parcours basés sur un événement (si une qualification d’audience ou un événement sont reçus pendant une pause, ces événements sont ignorés).
* Les parcours en pause sont comptabilisés dans le quota de parcours vivants.
* Le délai d’expiration global du parcours s’applique toujours aux parcours en pause. Par exemple, si un profil a été dans un parcours pendant 90 jours et que le parcours est suspendu, ce profil quittera toujours le parcours le 91 e jour.
* Un nouveau statut de parcours **Reprise** est disponible lorsqu’un parcours est repris. Il recommence à écouter les événements de parcours lorsque vous cliquez sur le bouton **Reprendre**.  La reprise des profils dans le parcours présente quelques retards. Lorsque le parcours passe de **Reprise** à **En direct**, cela signifie que tous les profils ont été repris. La **reprise** peut donc prendre un certain temps.
* Si des profils sont conservés dans un parcours et que ce parcours reprend automatiquement au bout de XX jours, les profils continuent le parcours et ne sont pas supprimés. Si vous souhaitez les supprimer, vous devez reprendre manuellement le parcours.
  <!--* There is a guardrail (at an org level) on the max number of profiles that can be held in paused journeys. This guardrail is per org, and is visible in the journey inventory on a new bar (only visible when there are paused journeys).-->

## Mise en pause d’un parcours {#journey-pause-steps}

Vous pouvez suspendre n’importe quel parcours en direct.

Pour suspendre le parcours, procédez comme suit :

1. Ouvrez le parcours à mettre en pause.
1. Cliquez sur le bouton **...Plus** dans la section supérieure droite de la zone de travail du parcours, puis sélectionnez **Pause**.

   ![Bouton Mettre en pause le parcours ](assets/pause-journey-button.png)

1. Sélectionnez le mode de gestion des profils qui se trouvent actuellement dans le parcours.

   ![Options de parcours de pause](assets/pause-confirm.png){width="50%" align="left"}

   Vous pouvez effectuer les actions suivantes :

   * Conserver les profils
   * Ignorer les profils

1. Cliquez sur le bouton **Pause** pour confirmer.

Un parcours peut être suspendu pendant 14 jours au maximum.

## Reprise d’un parcours en pause {#journey-resume-steps}

Les parcours en pause peuvent être repris manuellement à tout moment.

Pour reprendre un parcours, procédez comme suit :

1. Ouvrez le parcours que vous souhaitez reprendre.
1. Cliquez sur le bouton **...Plus** dans la section supérieure droite de la zone de travail du parcours, puis sélectionnez **Reprendre**.




