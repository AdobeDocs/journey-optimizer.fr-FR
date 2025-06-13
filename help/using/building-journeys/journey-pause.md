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
source-git-commit: adff7581d72947273675ab9b7bc36702d76d3792
workflow-type: tm+mt
source-wordcount: '2004'
ht-degree: 1%

---

# Mettre en pause un parcours {#journey-pause}

>[!CONTEXTUALHELP]
>id="ajo_journey_pause"
>title="Mettre le parcours en pause"
>abstract="Mettre en pause un parcours dynamique pour empêcher l’entrée de nouveaux profils. Choisissez de supprimer les profils actuellement dans le parcours ou de les conserver en place. S’ils sont conservés, ils reprendront l’exécution à l’activité d’action suivante une fois le parcours redémarré. Parfait pour les mises à jour ou les arrêts d&#39;urgence sans perdre la progression."

Vous pouvez suspendre vos parcours dynamiques, effectuer toutes les modifications nécessaires et les reprendre à tout moment.<!--You can choose whether the journey is resumed at the end of the pause period, or whether it stops completely. --> Pendant la pause, vous pouvez [appliquer des filtres globaux](#journey-global-filters) pour exclure des profils en fonction de leurs attributs. Le parcours est automatiquement repris à l’issue de la période de pause. Vous pouvez également [reprendre manuellement](#journey-resume-steps).

>[!AVAILABILITY]
>
>Cette fonctionnalité n’est disponible que pour un ensemble d’organisations (disponibilité limitée) et sera déployée à l’échelle mondiale dans une prochaine version.


## Avantages clés {#journey-pause-benefits}

Les parcours de pause et de reprise offrent aux utilisateurs et aux utilisatrices du parcours davantage de contrôle et de flexibilité en permettant de suspendre temporairement les parcours en direct sans perturber l’expérience client. En pause, aucune communication n’est envoyée et les profils restent suspendus jusqu’à la reprise du parcours.

Cette fonctionnalité réduit le risque d’envoi de messages inattendus lors d’erreurs ou de mises à jour (par exemple : modification du contenu du message), prend en charge une gestion du parcours plus sûre et accroît la confiance des utilisateurs et utilisatrices. La visibilité des parcours en pause et de leur statut directement dans l’interface utilisateur améliore la transparence et l’agilité opérationnelle.

>[!CAUTION]
>
>* Les autorisations de pause et de reprise des parcours sont limitées aux utilisateurs disposant de l’autorisation de haut niveau **[!DNL Publish journeys]**. Pour en savoir plus sur la gestion des droits d’accès des utilisateurs et des utilisatrices [!DNL Journey Optimizer], consultez [cette section](../administration/permissions-overview.md).
>
>* Avant de commencer à utiliser la fonctionnalité de pause/reprise, [lisez les mécanismes de sécurisation et limites](#journey-pause-guardrails).


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

![Mettre en pause en bloc deux parcours actifs de la barre inférieure](assets/bulk-pause-journeys.png)

### Comportement dans les parcours en pause

Lorsqu’un parcours est en pause, les nouvelles entrées sont toujours ignorées, quel que soit le mode de conservation/d’exclusion.

La gestion des profils lorsqu&#39;un parcours est en pause dépend de l&#39;activité. Les comportements sont détaillés ci-dessous. Pour une compréhension complète, consultez également cet [exemple de bout en bout](#journey-pause-sample).

| Activité parcours | Gestion des profils |
|-------------------------|--------------------------------------------------|
| [Qualification de l’audience](audience-qualification-events.md) | Dans le 1er nœud : ignoré <br> dans les autres nœuds : même comportement que dans un parcours en direct, cependant, si la qualification de l’audience se fait après une activité d’action et que l’utilisateur ou l’utilisatrice est mis en pause sur cette action, la qualification de l’audience est ignorée. |
| [Événement unitaire](general-events.md) | Dans le 1er nœud : ignoré <br>Dans les autres nœuds : même comportement que dans un parcours en direct, cependant, si l’événement se produit après une activité d’action et que l’utilisateur ou l’utilisatrice est mis en pause sur cette action, l’événement est ignoré. |
| [Lecture d’audience](read-audience.md) | Même comportement que dans un parcours en direct, avec quelques spécificités :<br>1.  Si l’action <strong>Pause</strong> a été activée après le démarrage de l’activité <strong>Lecture d’audience</strong>, les profils entrés dans le parcours continueront (jusqu’à l’activité <strong>Action</strong> suivante). Comme le parcours lit les audiences à une certaine vitesse, si l’audience complète n’est pas encore entrée, les profils restants dans la file d’attente seront ignorés.   <br>2. Pour les exécutions uniques : nous n’affichons aucune erreur à l’heure de reprise si la date planifiée était antérieure à la date de reprise. Cet échéancier serait ignoré. <br>3. Pour les parcours incrémentiels : <br>- Si une pause se produit avant la première occurrence, l’audience complète est lue lors de la reprise. <br>- Si une pause se produit, par exemple, le 4e jour d’une périodicité quotidienne et que le parcours reste en pause jusqu’au 9e jour, tous les profils entrés du 4e au 9e jour seront inclus lors de la reprise |
| [Réaction](reaction-events.md) | Même comportement que dans un parcours en direct, cependant, si la réaction se produit après une activité d’action et que l’utilisateur est en pause sur cette action, l’événement sera ignoré. |
| [Attente](wait-activity.md) | Même comportement que dans un parcours dynamique |
| [Condition](condition-activity.md) | Même comportement que dans un parcours dynamique |
| Décision de contenu | Les profils sont garés ou ignorés en fonction de ce que l’utilisateur a choisi lorsque le parcours a été suspendu |
| [Action de canal](journeys-message.md) | Les profils sont garés ou ignorés en fonction de ce que l’utilisateur a choisi lorsque le parcours a été suspendu |
| [Action personnalisée](../action/action.md) | Les profils sont garés ou ignorés en fonction de ce que l’utilisateur a choisi lorsque le parcours a été suspendu |
| [Mettre à jour le profil](update-profiles.md) et [Saut](jump.md) | Même comportement que dans un parcours dynamique |
| [Source de données externes](../datasource/external-data-sources.md) | Même comportement que dans un parcours dynamique |
| [Critères de sortie](journey-properties.md#exit-criteria) | Même comportement que dans un parcours dynamique |

## Reprise d’un parcours en pause {#journey-resume-steps}

>[!CONTEXTUALHELP]
>id="ajo_journey_resume"
>title="Reprendre le parcours"
>abstract="Reprenez un parcours en pause pour permettre aux nouveaux profils de rejoindre à nouveau le parcours. Si les profils étaient en attente pendant la pause, ils continueront leur parcours. Idéal pour redémarrer les parcours en toute sécurité après des mises à jour ou des pauses."

Les parcours en pause sont automatiquement repris à l’issue d’une période de pause maximale de 14 jours. Ils peuvent être repris manuellement à tout moment. La reprise d’un parcours en pause permet à de nouveaux profils de saisir à nouveau. Si les profils étaient en attente pendant la pause, ils continueront leur parcours. Idéal pour redémarrer les parcours en toute sécurité après des mises à jour ou des pauses.

Pour reprendre un parcours en pause et recommencer à écouter les événements de parcours, procédez comme suit :

1. Ouvrez le parcours que vous souhaitez reprendre.
1. Cliquez sur le bouton **...Plus** dans la section supérieure droite de la zone de travail du parcours, puis sélectionnez **Reprendre**.

   Le parcours passe à l’état **Reprise**. Lorsque le parcours reprend, de nouvelles entrées démarrent dans la minute qui suit. La reprise des profils qui étaient conservés peut prendre un certain temps.  Comme tous les profils doivent reprendre pour que le parcours soit à nouveau **actif**, la transition du statut **Reprise** au statut **actif** peut prendre un certain temps.

1. Cliquez sur le bouton **Reprendre** pour confirmer.


Dans la liste de vos parcours, vous pouvez reprendre un ou plusieurs parcours **en pause**. Pour reprendre un groupe de parcours (_reprise en bloc_), sélectionnez-les et cliquez sur le bouton **Reprendre** situé dans la barre bleue en bas de l’écran. Notez que le bouton **Reprendre** n’est disponible que lorsque les parcours **En pause** sont sélectionnés.


## Application d’un filtre global aux profils d’un parcours en pause  {#journey-global-filters}

Lorsqu’un parcours est en pause, vous pouvez l’appliquer en fonction des attributs de profil. Ce filtre permet d’exclure les profils qui correspondent à l’expression définie au moment de la reprise. Une fois le filtre global défini, il s’applique aux nœuds d’action, même pour les nouvelles entrées de profil. Les profils correspondant aux critères et les nouveaux profils qui tentent d’y accéder seront exclus du parcours **sur le nœud d’action suivant** qu’ils rencontrent.

Par exemple, pour exclure tous les clients français d’un parcours en pause, procédez comme suit :

1. Accédez au parcours en pause que vous souhaitez modifier.

1. Cliquez sur l’icône **Critères de sortie et filtre global**.

   ![Ajouter un filtre global à un parcours en pause](assets/add-global-filter.png)

1. Dans les paramètres **Critères de sortie et filtre global**, cliquez sur **Ajouter un filtre global** pour définir un filtre en fonction des attributs de profil.

1. Définissez l’expression pour exclure les profils dont l’attribut de pays est égal à France.

   ![Ajouter un filtre global à un parcours en pause](assets/add-country-filter.png)

1. Enregistrez votre filtre et cliquez sur le bouton **Mettre à jour le parcours** pour appliquer vos modifications.

1. [Reprendre le parcours ](#journey-resume-steps).

   Au moment de la reprise, tous les profils dont l’attribut de pays est défini sur France seront automatiquement exclus du parcours au niveau du nœud d’action suivant. Tous les nouveaux profils dont l’attribut de pays est défini sur France qui tentent d’entrer dans le parcours sont bloqués au nœud d’action suivant.

N’oubliez pas que les exclusions de profil pour les profils actuellement dans le parcours et pour les nouveaux profils ne se produiront que lorsqu’ils atteignent un nœud d’action.

>[!CAUTION]
>
>* Vous ne pouvez définir qu **un seul** global par parcours.
>
>* Vous pouvez uniquement créer, mettre à jour ou supprimer un filtre global dans les parcours **En pause**.

## Mécanismes de sécurisation et limitations {#journey-pause-guardrails}

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
* Dans les parcours en pause, les alertes ne se déclenchent pas pour les alertes de segments par lots.
* Il n’existe aucun journal d’audit dans le système lorsque l’état de pause du parcours est arrêté après 14 jours.
* Certains profils ignorés peuvent être visibles dans l’événement d’étape de Parcours, mais pas dans les rapports. Par exemple : ignorez les événements métier pour Lecture d’audience, les traitements Lecture d’audience sont abandonnés en raison d’un parcours en pause, les événements ignorés lorsque l’activité d’événement se trouvait après une action en attente du profil.
  <!--* There is a guardrail (at an org level) on the max number of profiles that can be held in paused journeys. This guardrail is per org, and is visible in the journey inventory on a new bar (only visible when there are paused journeys).-->

## Exemple complet {#journey-pause-sample}

Prenons l’exemple du parcours ci-dessous :

![Exemple de parcours ](assets/pause-journey-sample.png)

Lorsque vous suspendez ce parcours, vous indiquez si les profils sont **Ignorés** ou **Bloqués**, puis la gestion des profils est la suivante :

1. Activité **AddToCart** : toutes les nouvelles entrées de profil sont bloquées. Si un profil est déjà entré dans le parcours avant une pause, il passera au nœud d’action suivant.
1. Activité **Attente** : les profils continuent à attendre normalement sur le nœud et le quitteront, même si le parcours est en pause.
1. **Condition** : les profils continuent de remplir des conditions et de se déplacer vers la branche de droite, en fonction de l’expression définie sur la condition.
1. Activités **Push**/**Email** : lors d&#39;un parcours en pause, les profils commencent à attendre ou sont ignorés (selon le choix effectué par l&#39;utilisateur au moment de la pause) sur le nœud d&#39;action suivant. Les profils vont donc commencer à attendre ou seront ignorés.
1. **Événements** après les nœuds d’action : si un profil est en attente sur un nœud d’action et qu’un événement se produit après, si cet événement est déclenché, le profil est ignoré.

Selon ce comportement, vous pouvez voir le nombre de profils augmenter sur le parcours en pause, principalement dans les activités avant les actions. Par exemple, dans cet exemple, l’Attente est ignorée, ce qui augmente le nombre de profils qui passent par l’activité Condition .

Lorsque vous reprenez ce parcours :

1. Les entrées du parcours débutent dans une minute
1. Les profils qui étaient en attente dans le parcours des activités d’action sont repris à un taux de 5 000 tps. Ils vont alors entrer l’action qu’ils attendaient et continuer le parcours.
