---
solution: Journey Optimizer
product: journey optimizer
title: Suspendre un parcours
description: Découvrez comment mettre en pause et reprendre un parcours actif.
feature: Journeys
role: User
level: Intermediate
keywords: publication, parcours, actif, validité, vérification
exl-id: a2892f0a-5407-497c-97af-927de81055ac
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/gIj6jGScvIDgAJxb3B4wiuqP6BKZS0tvCeqC6wRo5IQ
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4ebid: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2: id: b32bb433-f8c6-4931-8e52-e657230a3bf2id: d8353d85-5da7-453d-bd68-40ad33fa0ab7id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b4dd41a7-ccf8-4e9d-918e-acaab534a307id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: 0bbbbf94550d4cb762ecca300932620c8d3da50e
workflow-type: tm+mt
source-wordcount: 3545
ht-degree: 67%

---

# Suspendre un parcours {#journey-pause}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment suspendre et reprendre un parcours en direct pour apporter des modifications en toute sécurité ou arrêter les envois, arrêter ou fermer un parcours en pause sans le reprendre au préalable et appliquer les critères de sortie d’attribut de profil pendant la pause.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_pause"
>title="Mettre votre parcours en pause"
>abstract="La mise en pause d’un parcours dynamique empêcher l’intégration de nouveaux profils. Les profils actuellement dans le parcours peuvent être supprimés ou conservés. S’ils sont conservés, ils reprendront l’exécution à l’activité d’action suivante une fois le parcours redémarré. Idéal pour les mises à jour ou les arrêts d’urgence, sans perte de la progression."

Vous pouvez suspendre vos parcours en direct, effectuer toutes les modifications nécessaires et les reprendre à tout moment.<!--You can choose whether the journey is resumed at the end of the pause period, or whether it stops completely. --> Pendant la pause, vous pouvez [appliquer des critères de sortie d’attribut de profil](#journey-exit-criteria) pour exclure des profils en fonction de leurs attributs. Le parcours est automatiquement repris à l’issue de la période de pause. Vous pouvez également [le reprendre manuellement](#journey-resume-steps) ou [arrêter le parcours ](#stop-close-paused) à partir de l’état **En pause** sans le reprendre au préalable.

## Avantages clés {#journey-pause-benefits}

La mise en pause et la reprise des parcours offrent aux responsables de parcours davantage de contrôle et de flexibilité en permettant de suspendre temporairement les parcours actifs sans perturber l’expérience client. Lorsque le parcours est suspendu, aucune communication n’est envoyée et les profils restent suspendus jusqu’à la reprise du parcours.

Cette fonctionnalité réduit le risque d’envoi de messages indésirables lors d’erreurs ou de mises à jour (par exemple, une modification du contenu du message), offre une gestion des parcours plus sûre et renforce la confiance du ou de la responsable de parcours. L’affichage des parcours en pause et de leur statut directement dans l’interface d’utilisation améliore la transparence et l’agilité opérationnelle.

>[!CAUTION]
>
>* Les autorisations de mise en pause et de reprise des parcours sont limitées aux utilisateurs et aux utilisatrices qui disposent de l’autorisation de haut niveau **[!DNL Publish journeys]**. Pour en savoir plus sur la gestion des droits d’accès des utilisateurs et des utilisatrices [!DNL Journey Optimizer], consultez [cette section](../administration/permissions-overview.md).
>
>* Avant de commencer à utiliser la fonctionnalité de mise en pause/reprise, [lisez la section sur les Mécanismes de sécurisation et les limitations](#journey-pause-guardrails).


## Mise en pause d’un parcours {#journey-pause-steps}

Vous pouvez mettre en pause n’importe quel parcours **actif**.

Pour mettre en pause votre parcours, procédez comme suit :

1. Ouvrez le parcours que vous souhaitez mettre en pause.
1. Cliquez sur le bouton **...Plus** situé en haut à droite de la zone de travail du parcours, puis sélectionnez **Mettre en pause**.

   ![Bouton Mettre en pause le parcours](assets/pause-journey-button.png)

1. Sélectionnez les options de gestion des profils qui se trouvent actuellement dans le parcours.

   ![Options de mise en pause de parcours](assets/pause-confirm.png){width="50%"}

   Vous pouvez :

   * **Mettre en pause les profils** - Les profils attendront le nœud **Action** suivant pour reprendre le parcours.
   * **Ignorer les profils** - Les profils seront exclus du parcours lors du nœud **Action** suivant.

   Lorsque vous suspendez un parcours, il est supposé que vous prévoyez de le reprendre à un moment donné. Cependant, un parcours ne peut pas rester en pause indéfiniment. Pour éviter cela, vous pouvez définir la durée pendant laquelle le parcours doit rester en pause (entre 1 et 14 jours). Le parcours reprend automatiquement après le nombre de jours sélectionné.

1. Cliquez sur le bouton **Mettre en pause** pour confirmer l’opération.

Le nombre maximal de profils pouvant être conservés dans des parcours mis en pause pour votre organisation est visible dans l’inventaire des parcours. Il n’est visible que lorsqu’au moins un parcours est en pause. Cet indicateur affiche également le nombre total de parcours mis en pause. Il est réactualisé toutes les 30 minutes. En savoir plus dans la section [Mécanismes de sécurisation et limitations](#guardrails-and-limitations).

![Nombre de parcours mis en pause et de profils actuellement en pause](assets/profiles-in-paused-journeys.png){width="50%"}

Dans la liste de vos parcours, vous pouvez mettre en pause un ou plusieurs parcours **actifs**. Pour mettre en pause un groupe de parcours (_pause par lots_), sélectionnez-les dans la liste et cliquez sur le bouton **Mettre en pause** dans la barre bleue en bas de l’écran. Le bouton **Mettre en pause** n’est disponible que lorsque des parcours **actifs** sont sélectionnés.

![Mettre en pause deux parcours actifs en même temps à partir de la barre inférieure](assets/bulk-pause-journeys.png)

## Logique d’exécution des parcours mis en pause {#journey-pause-exec}

Lorsqu’un parcours est en pause, les nouvelles entrées sont toujours supprimées, quel que soit le mode choisi (mettre en pause/ignorer).

Lorsqu’un parcours est en pause, la gestion des profils et l’exécution des activités dépendent de l’activité. Les comportements sont détaillés ci-dessous. Afin de comprendre pleinement ces principes, consultez également cet [exemple de bout en bout](#journey-pause-sample).


| Activité de parcours | Lorsque le parcours est en pause |
|-------------------------|--------------------------------------------------|
| [Qualification d’audience](audience-qualification-events.md) | <ul> <li>Lors du premier nœud de la zone de travail : toute qualification de profil pour l’audience est ignorée. </li><li>Dans les autres nœuds : même comportement que dans un parcours actif, mais si la qualification de l’audience se situe après une activité <strong>Action</strong> et que l’utilisateur ou l’utilisatrice est mis en pause lors de cette action, la qualification de l’audience est ignorée. </li></ul> |
| [Événement unitaire](general-events.md) | <ul> <li>Lors du premier nœud de la zone de travail : l’événement est ignoré.</li><li>Dans les autres nœuds : même comportement que dans un parcours actif. Cependant, si l’événement se situe après une activité <strong>Action</strong> et que l’utilisateur ou l’utilisatrice est mis en pause lors de cette action, l’événement est ignoré. </li></ul> |
| [Lecture d’audience](read-audience.md) | Même comportement que dans un parcours actif, avec quelques spécificités : <ol> <li> Si le bouton <strong>Mettre en pause</strong> a été utilisé après le démarrage de l’activité <strong>Lecture d’audience</strong>, les profils déjà entrés dans le parcours le poursuivront (jusqu’à l’activité <strong>Action</strong> suivante). Étant donné que le parcours lit les audiences à une certaine vitesse, si l’audience entière n’est pas encore entrée, les profils restants dans la file d’attente seront ignorés.</li><li> Pour les exécutions uniques : aucune erreur ne s’affichera au moment de la reprise si la date planifiée est antérieure à la date de reprise. Cette planification sera ignorée.</li><li>Pour les parcours incrémentiels : <ul><li>Si une pause se produit avant la première occurrence, l’audience complète sera lue lors de la reprise. </li><li>Si une pause se produit, par exemple, le 4e jour d’une périodicité quotidienne et que le parcours reste en pause jusqu’au 9e jour, alors, lors de la reprise, tous les profils qui sont entrés entre le 4e et le 9e jour seront inclus.  </li></ul></ol> |
| [Réaction](reaction-events.md) | Même comportement que dans un parcours actif. Cependant, si la réaction se situe après une activité <strong>Action</strong> et que l’utilisateur ou l’utilisatrice est mis en pause lors de cette action, l’événement de réaction est ignoré. |
| [Attente](wait-activity.md) | Même comportement que dans un parcours actif. |
| [Optimiser](optimize.md) | Même comportement que dans un parcours actif. |
| [Décision de contenu](content-decision.md) | Les profils sont conservés ou ignorés en fonction de ce que l’utilisateur ou l’utilisatrice a choisi lorsque le parcours a été suspendu. |
| [Action de canal](journey-action.md) | Les profils sont conservés ou ignorés en fonction de ce que l’utilisateur ou l’utilisatrice a choisi lorsque le parcours a été suspendu. |
| [Action personnalisée](../action/action.md) | Les profils sont conservés ou ignorés en fonction de ce que l’utilisateur ou l’utilisatrice a choisi lorsque le parcours a été suspendu. |
| [Mettre à jour le profil](update-profiles.md) et [Sauter](jump.md) | Les profils sont conservés ou ignorés en fonction de ce que l’utilisateur ou l’utilisatrice a choisi lorsque le parcours a été suspendu. |
| [Source de données externe](../datasource/external-data-sources.md) | Même comportement que dans un parcours actif. |
| [Critères de sortie](journey-properties.md#exit-criteria) | Même comportement que dans un parcours actif. |


Découvrez comment résoudre les problèmes liés aux rejets dans [cette section](#discards-troubleshoot).

## Reprise d’un parcours en pause {#journey-resume-steps}

>[!CONTEXTUALHELP]
>id="ajo_journey_resume"
>title="Reprendre votre parcours"
>abstract="La reprise d’un parcours en pause permet à de nouveaux profils de réintégrer le parcours. Si les profils étaient en attente pendant la pause, ils continueront leur parcours. Idéal pour redémarrer des parcours en toute sécurité après des mises à jour ou des pauses."

Les parcours en pause sont automatiquement repris à l’issue d’une période de pause maximale de 14 jours. Ils peuvent être repris manuellement à tout moment. Reprenez un parcours en pause pour permettre à de nouveaux profils de rejoindre à nouveau le parcours. Si des profils étaient en attente pendant la pause, ils continueront leur parcours. Idéal pour redémarrer des parcours en toute sécurité après des mises à jour ou des pauses.

Pour reprendre un parcours en pause et recommencer à écouter les événements de parcours, procédez comme suit :

1. Ouvrez le parcours que vous souhaitez reprendre.
1. Cliquez sur le bouton **...Plus** situé en haut à droite de la zone de travail du parcours, puis sélectionnez **Reprendre**.

   Le statut du parcours devient **Reprise en cours**. Lorsque le parcours reprend, les nouvelles entrées démarrent en moins d’une minute. La reprise des profils qui ont été mis en pause peut prendre un certain temps : les profils sont repris à un taux de 5 000 tps.  Étant donné que tous les profils doivent reprendre pour que le parcours soit à nouveau **actif**, la transition du statut **reprise en cours** au statut **actif** peut prendre un certain temps.

1. Cliquez sur le bouton **Reprendre** pour confirmer l’opération.


Dans la liste de vos parcours, vous pouvez reprendre un ou plusieurs parcours **en pause**. Pour reprendre un groupe de parcours (_reprise par lots_), sélectionnez-les et cliquez sur le bouton **Reprendre** situé dans la barre bleue en bas de l’écran. Notez que le bouton **Reprendre** n’est disponible que lorsque des parcours **en pause** sont sélectionnés.

## Arrêter un parcours en pause {#stop-close-paused}

Si vous décidez de ne pas reprendre un parcours en pause, vous pouvez le terminer à partir de l’état **En pause**. Cela met immédiatement fin à tout traitement de parcours et arrête chaque profil restant dans le parcours. [En savoir plus sur l’arrêt d’un parcours ](end-journey.md#stop-journey).

Pour arrêter un parcours en pause dans la zone de travail du parcours, procédez comme suit :

1. Ouvrez le parcours **En pause** que vous souhaitez arrêter ou fermer.
1. Cliquez sur le bouton **...Plus** dans la section supérieure droite de la zone de travail du parcours.
1. Sélectionnez **[!UICONTROL Arrêter]**, puis confirmez dans la boîte de dialogue.

Dans la liste de vos parcours, vous pouvez également cliquer sur le bouton **[!UICONTROL Points de suspension]** à droite du nom du parcours en pause et sélectionner **[!UICONTROL Arrêter]**.

>[!IMPORTANT]
>
>Vous ne pouvez pas redémarrer ou supprimer un parcours [fermé](end-journey.md#close-journey) ou [arrêté](end-journey.md#stop-journey). Vous pouvez [le dupliquer](journey-ui.md#duplicate-a-journey) ou en [créer une nouvelle version](publish-journey.md#journey-versions).
>
>L’arrêt d’un parcours nécessite l’autorisation **[!DNL Manage journeys]** . Si le parcours comprend des campagnes intégrées ou des nœuds de messagerie, les utilisateurs doivent également disposer des autorisations **Campagnes > Publier les campagnes**. [En savoir plus sur les autorisations Stop](end-journey.md#stop-journey).

## Afficher le moment où un parcours a été suspendu ou repris {#view-pause-resume-info}

Pour savoir quand un parcours a été suspendu ou repris pour la dernière fois, et par qui, ouvrez le parcours et accédez à ses **propriétés** (cliquez sur l’icône en forme de crayon en regard du nom du parcours). Utilisez le bouton **Copier les détails techniques** pour copier les informations techniques qui incluent :

* Date et heure de la dernière pause et de la reprise
* Le nom d’affichage et l’identifiant de l’utilisateur qui a effectué la dernière pause et la dernière reprise
* Paramètres du parcours en pause (comportement de pause, durée maximale de pause, état de reprise automatique, identifiant de pause)

Ces informations sont utiles pour le dépannage, le contrôle ou le partage avec l’assistance. Pour obtenir la liste complète des champs copiés, voir [ Accès aux propriétés d’un parcours ](journey-properties.md#access-properties).

## Appliquer un critère de sortie dans un parcours mis en pause {#journey-exit-criteria}

Lorsqu’un parcours est mis en pause, vous pouvez appliquer un critère de sortie basé sur des attributs de profil. Ce filtre permet d’exclure au moment de la reprise les profils qui correspondent à une expression définie. Après la définition des critères de sortie basés sur des attributs de profil, ceux-ci sont appliqués sur les nœuds d’action, même pour les nouvelles entrées de profils. Les profils existants correspondant aux critères et les nouveaux profils entrant dans le parcours seront exclus du parcours **sur le nœud d’action suivant** qu’ils rencontrent.

Par exemple, pour exclure toutes les clientes et tous les clients français d’un parcours en pause, procédez comme suit :

1. Accédez au parcours en pause que vous souhaitez modifier.

1. Cliquez sur l’icône **Critères de sortie**.

   ![Ajouter un critère de sortie d’attribut de profil à un parcours mis en pause](assets/add-exit-criteria.png)

1. Dans les paramètres **Critères de sortie**, cliquez sur **Ajouter des critères de sortie** pour définir un filtre en fonction des attributs de profil.

1. Définissez l’expression pour exclure les profils dont l’attribut de pays est égal à « France ».

   ![Ajouter un critère de sortie d’attribut de profil à un parcours mis en pause](assets/add-country-filter.png)

1. Enregistrez votre filtre et cliquez sur le bouton **Mettre à jour le parcours** pour appliquer vos modifications.

1. [Reprenez le parcours](#journey-resume-steps).

   Au moment de la reprise, tous les profils dont l’attribut de pays est défini sur France seront automatiquement exclus du parcours au niveau du nœud d’action suivant. Tous les nouveaux profils dont l’attribut de pays est défini sur France qui tenteront d’entrer dans le parcours seront bloqués au nœud d’action suivant.

N’oubliez pas que les exclusions de profils, pour les profils actuellement dans le parcours et pour les nouveaux profils, ne se produiront que **lorsqu’ils atteindront un nœud d’action**.

>[!CAUTION]
>
>* Vous ne pouvez définir qu’**un** seul critère de sortie basé sur un attribut de profil pour chaque parcours.
>
>* Vous pouvez uniquement créer, mettre à jour ou supprimer un critère de sortie basé sur un attribut de profil dans les parcours **mis en pause**.
>
>* Pour en savoir plus sur les critères de sortie basés sur des attributs de profil, consultez [cette section](journey-properties.md#profile-exit-criteria).

## Mécanismes de sécurisation et limitations {#journey-pause-guardrails}

* Une version de parcours peut être suspendue pendant **14 jours au maximum** avec un maximum de **10 millions de profils** autorisés dans les parcours en pause dans l’ensemble de votre organisation.
Cette limite tient compte du nombre total de profils conservés sur tous les parcours en pause, et non de profils distincts. Par exemple, si les mêmes profils de 5 millions sont conservés dans deux parcours en pause, la limite de 10 millions est atteinte.
Cette limite est vérifiée toutes les 30 minutes. Cela signifie que vous pouvez temporairement dépasser le seuil de 10 millions, mais une fois que le système le détecte, tous les profils supplémentaires sont automatiquement ignorés.

  Si vous reprenez les parcours pour ramener le nombre de profils conservés en dessous de la limite, le parcours reprend immédiatement, mais la mise à jour du nombre de profils peut prendre jusqu’à 30 minutes. Pendant ce temps, le système peut toujours considérer ces profils comme étant en pause.

* Pour les parcours qui incluent des [activités entrantes](../channels/gs-channels.md#inbound-channels) (par exemple, in-app, web, etc.), la suspension du parcours n’interrompt pas les communications qui ont déjà été déclenchées. Si un profil s’est qualifié pour une activité entrante avant la suspension, le message correspondant sera toujours diffusé. Pour arrêter complètement toutes les communications entrantes, vous devez arrêter le parcours.
* Les parcours en pause sont comptabilisés dans le quota des parcours actifs.
* Les profils qui sont entrés dans le parcours mais ignorés pendant la pause sont toujours comptabilisés comme des profils engageables.
* Les parcours en pause sont pris en compte dans toutes les règles métier, de la même manière que s’ils étaient actifs.
* Le délai d’expiration global des parcours s’applique toujours aux parcours en pause. Par exemple, si un profil se trouve dans un parcours pendant 90 jours et que ce parcours est mis en pause, ce profil quittera toujours le parcours le 91e jour.
* Les profils sont **supprimés** dans un parcours en pause lorsqu’ils atteignent une activité d’action. S’ils restent en attente pendant la mise en pause d’un parcours et quittent cette attente après la reprise du parcours, ils poursuivront le parcours et ne seront pas ignorés. [Voir l’exemple de bout en bout](#journey-pause-sample)
* Même après la pause, à mesure que les événements continuent d’être traités, ces événements sont comptabilisés dans le quota d’événements de parcours par seconde. Si celui-ci est dépassé, une limitation est appliquée pour les événements unitaires.
* Lorsque les profils sont mis en pause dans un parcours en pause, les attributs de profil sont actualisés au moment de la reprise.
* Les conditions sont toujours exécutées dans des parcours en pause. Ainsi, si un parcours a été mis en pause en raison de problèmes de qualité des données, toute condition préalable à un nœud d’action peut être évaluée avec des données incorrectes.
* Pour les parcours de **lecture d’audience** basés sur une audience incrémentale, la durée de pause est prise en compte. Ce n’est pas le cas pour la qualification d’audience ou les parcours basés sur un événement : si une qualification d’audience ou un événement est reçu pendant une pause et qu’il s’agit de la première activité du parcours, ces événements sont ignorés.
* Si des profils sont mis en pause dans un parcours et que ce parcours reprend automatiquement au bout de quelques jours, ces profils continuent le parcours et ne sont pas supprimés. Si vous voulez les supprimer, vous devez arrêter le parcours.
* Dans les parcours mis en pause, les alertes ne se déclenchent pas pour les [alertes de segment par lot](../reports/alerts.md#alert-read-audiences).
* Il n’existe aucun journal d’audit dans le système lorsque l’état de mise en pause du parcours est arrêté après 14 jours.
* Certains profils ignorés peuvent être visibles dans l’événement d’étape du parcours, mais pas dans les rapports. Par exemple :
   * Ignorer les événements métier pour **Lecture d’audience**
   * Les tâches de **Lecture d’audience** sont abandonnées en raison d’un parcours en pause
   * Événements ignorés lorsque l’activité **Événement** se situe après une activité d’action où le profil est en attente



## Exemple de bout en bout {#journey-pause-sample}

Prenons l’exemple du parcours ci-dessous :

![Exemple de parcours](assets/pause-journey-sample.png){zoomable="yes"}

Lorsque vous mettez en pause ce parcours, vous choisissez si les profils sont **Supprimés** ou **Conservés** et ensuite, la gestion des profils est la suivante :

1. Activité **AddToCart** : toutes les nouvelles entrées de profils sont bloquées. Si un profil est déjà entré dans le parcours avant une pause, il poursuit le parcours jusqu’au nœud d’action suivant.
1. Activité **Attente** : les profils continuent à attendre normalement sur le nœud et le quitteront, même si le parcours est en pause.
1. **Condition** : les profils continuent de passer par les conditions et se dirigent vers la bonne branche, en fonction de l’expression définie sur la condition.
1. Activités **Push**/**E-mail** : lorsqu’un parcours est suspendu, les profils commencent à attendre ou sont ignorés (selon le choix effectué par l’utilisateur ou l’utilisatrice au moment de la suspension) sur le nœud d’action suivant. Les profils vont donc commencer à attendre ou seront ignorés.
1. **Événements** après les nœuds **Action** : si un profil est en attente sur un nœud **Action** et qu’une activité **Événement** suit, si cet événement est déclenché, il est ignoré.

Selon ce comportement, vous pouvez voir le nombre de profils augmenter sur le parcours en pause, principalement dans les activités précédant les activités **Action**. Dans cet exemple, l’activité **Attente** est toujours activée, ce qui augmente le nombre de profils qui passent par l’activité **Condition** lorsqu’ils la quittent.

Lorsque vous reprenez ce parcours :

1. Les entrées du parcours débutent en l’espace d’une minute.
1. Les profils qui étaient en attente dans le parcours sur les activités **Action** sont rétablis à un taux de 5 000 tps. Ils peuvent alors entrer dans l’activité **Action** pour laquelle ils attendaient et continuer le parcours.

## Résoudre les problèmes liés aux rejets de profils dans les parcours en pause {#discards-troubleshoot}

Vous pouvez utiliser le [[!DNL Adobe Experience Platform] Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html?lang=fr){target="_blank"} pour interroger les événements d’étape, ce qui peut fournir plus d’informations sur les abandons de profil, selon le moment où ils se sont produits.

* Pour les rejets qui se produisent avant que le profil ne rejoigne le parcours, utilisez le code suivant :

  ```sql
  SELECT
  TIMESTAMP,
  _experience.journeyOrchestration.profile.ID,
  to_json(_experience.journeyOrchestration)
  FROM
  journey_step_events
  WHERE
  _experience.journeyOrchestration.serviceEvents.dispatcher.eventType = 'PAUSED_JOURNEY_VERSION'
  AND _experience.journeyOrchestration.journey.versionID=<jvId>  
  ```

  Il permet de répertorier les rejets qui se sont produits au niveau du point d’entrée du parcours :

   1. Lorsqu’un parcours d’audience est en cours d’exécution et que le premier nœud est toujours en cours de traitement, si le parcours est mis en pause, tous les profils non traités sont ignorés.

   1. Lorsqu’un nouvel événement unitaire arrive vers le nœud de départ (pour déclencher une entrée) lorsque le parcours est en pause, l’événement est ignoré.

* Pour les rejets qui se produisent lorsque le profil est déjà dans le parcours, utilisez le code suivant :

  ```sql
  SELECT
  TIMESTAMP,
  _experience.journeyOrchestration.profile.ID,
  to_json(_experience.journeyOrchestration)
  FROM
  journey_step_events
  WHERE
  _experience.journeyOrchestration.serviceEvents.stateMachine.eventType = 'JOURNEY_IN_PAUSED_STATE'
  AND _experience.journeyOrchestration.journey.versionID=<jvId> 
  ```

  Cette commande liste les rejets qui se produisent lorsque les profils se trouvent dans un parcours :

   1. Si le parcours est mis en pause avec l’option Ignorer activée et qu’un profil a rejoint le parcours avant la mise en pause, ce profil sera ignoré lorsqu’il atteindra le nœud d’action suivant.

   1. Si le parcours a été mis en pause avec l’option Conserver sélectionnée, mais que des profils ont été ignorés en raison d’un dépassement du quota de 10 millions, ces profils seront toujours ignorés lorsqu’ils atteindront le nœud d’action suivant.

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page explique comment suspendre et reprendre un parcours dynamique dans Adobe Journey Optimizer, y compris le comportement de blocage ou d’abandon de profil pendant la pause, comment appliquer des critères de sortie d’attribut de profil en pause et comment résoudre les abandons de profil à l’aide de Query Service.

**Intentions:**
* Mettre en pause un parcours dynamique pour empêcher de nouvelles entrées de profil et conserver ou ignorer les profils en cours au nœud d’action suivant
* Reprendre un parcours en pause manuellement ou savoir quand il reprend automatiquement après la période de pause maximale
* Appliquez un critère de sortie d’attribut de profil pour exclure des profils spécifiques (par exemple, par pays) lorsqu’un parcours est en pause
* Suspension en bloc ou reprise en bloc de plusieurs parcours actifs de la liste d’inventaire des parcours
* Résolution des problèmes liés aux abandons de profil dans un parcours en pause à l’aide des requêtes d’événement d’étape de Adobe Experience Platform Query Service
* Afficher le journal d’audit indiquant qui a suspendu ou repris un parcours et quand

**Glossaire:**
* **Pause (parcours)** : état qui suspend temporairement un parcours actif, ce qui empêche les nouvelles entrées et interrompt la progression du profil au nœud d’action suivant ; aucune communication n’est envoyée pendant la suspension *(spécifique au produit)*
* **Mode de suspension** : une option de pause qui fait attendre les profils en cours au nœud d’action suivant jusqu’à ce que le parcours reprenne en *(spécifique au produit)*
* **Mode de rejet** : option de pause qui quitte les profils en cours du parcours lorsqu’ils atteignent le nœud d’action suivant *(spécifique au produit)*
* **Critère de sortie basé sur les attributs de profil** : application d’un parcours en pause qui exclut les profils correspondant à une expression définie au niveau du nœud d’action suivant lors de la reprise *(spécifique au produit)*
* **Mise en pause en bloc/reprise en bloc** : la possibilité de suspendre ou de reprendre plusieurs parcours actifs ou en pause simultanément à partir de la liste d’inventaire des parcours *(spécifique au produit)*

**Mécanismes de sécurisation :**
* Seuls les utilisateurs disposant de l’autorisation **Publier les parcours** peuvent suspendre et reprendre les parcours. L’arrêt d’un parcours en pause nécessite **Gérer les parcours** (et **Campagnes > Publier les campagnes** si des campagnes intégrées ou des nœuds de messagerie sont présents)
* La durée de pause peut être configurée de 1 à 14 jours, après quoi le parcours reprend automatiquement
* Les profils conservés pendant la pause reprennent à 5 000 TPS au maximum ; le parcours reste dans l’état Reprise jusqu’à ce que tous les profils conservés aient repris
* Un maximum de 10 millions de profils peuvent être conservés sur tous les parcours en pause d’une organisation. Les profils en trop sont automatiquement ignorés
* Un seul critère de sortie basé sur les attributs de profil peut être défini par parcours
* Les critères de sortie basés sur les attributs de profil peuvent uniquement être créés, mis à jour ou supprimés lorsque le parcours est en pause
* Les parcours en pause sont comptabilisés dans le quota de parcours actifs
* Le délai d’expiration global du parcours (91 jours) s’applique toujours pendant une pause
* Les communications d’activité entrantes déjà déclenchées avant la pause continuent d’être diffusées ; pour les arrêter, le parcours doit être complètement arrêté
* Les alertes pour le segment par lot ne se déclenchent pas dans les parcours en pause
* Les nouvelles entrées sont toujours ignorées lorsqu’un parcours est en pause, quel que soit le mode de conservation ou d’exclusion

**Terminologie:**
* Nom canonique : Suspendre un parcours — Acronyme : aucun — variantes : Suspendre le parcours, Suspendre/Reprendre
* Synonymes : « Conserver » = « Profils de parc » ; « Ignorer » = « Profils de sortie »
* Ne pas confondre : « Pause » ≠ « Arrêter » — La pause est temporaire et permet la reprise ; l’option Arrêter quitte immédiatement tous les profils et ne peut pas être annulée en direct
* Ne les confondez pas : « Pause » ≠ « Fermer aux nouvelles entrées » — Fermer aux nouvelles entrées permet aux profils existants de se terminer mais ne les suspend pas ; Mettre en pause suspend tous les profils en cours au nœud d’action suivant

**FAQ:**
* **Q : Qu’advient-il des profils déjà présents dans un parcours lorsqu’il est en pause ?** — Selon l’option sélectionnée au moment de la pause, les profils sont conservés (en attente au nœud d’action suivant) ou ignorés (sortis du parcours au nœud d’action suivant).
* **Q : Combien de temps un parcours peut-il rester en pause ?** — Entre 1 et 14 jours (choisi au moment de la pause) ; il reprend ensuite automatiquement.
* **Q : Puis-je exclure certains profils lorsqu’un parcours est en pause ?** — Oui ; appliquez un critère de sortie basé sur les attributs de profil (un par parcours) pendant que le parcours est en pause pour exclure les profils correspondants au nœud d’action suivant lors de la reprise.
* **Q : La mise en pause d’un parcours s’arrête-t-elle dans l’application ou les messages web déjà déclenchés ?** — Non ; les communications entrantes déjà déclenchées avant que la pause ne se poursuive. Pour arrêter toutes les communications entrantes, vous devez arrêter entièrement le parcours.
* **Q : Comment puis-je savoir quels profils ont été ignorés lors d’une pause ?** — Interroger le jeu de données `journey_step_events` dans Adobe Experience Platform Query Service à l’aide des filtres de type d’événement `PAUSED_JOURNEY_VERSION` ou `JOURNEY_IN_PAUSED_STATE` avec l’ID de version par parcours.

+++
