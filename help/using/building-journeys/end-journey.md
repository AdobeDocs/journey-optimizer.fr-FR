---
solution: Journey Optimizer
product: journey optimizer
title: Fin de parcours
description: Découvrez comment un parcours se termine dans Journey Optimizer.
feature: Journeys
role: User
level: Intermediate
keywords: rentrée, parcours, fin, dynamique, arrêt
exl-id: ea1ecbb0-12b5-44e8-8e11-6d3b8bff06aa
source-git-commit: a536336ec7b37ffa0cd860c2c7479c75365eff00
workflow-type: tm+mt
source-wordcount: '730'
ht-degree: 66%

---

# Terminer un parcours {#journey-ending}

Un parcours peut se terminer pour un individu dans deux contextes spécifiques :

* L’individu atteint à la dernière activité d’un chemin, puis passe à la [ balise de fin ](#end-tag).
* L’individu atteint une activité **Condition** (ou une activité **Attente** avec une condition) et ne répond à aucune des conditions.

L’individu peut alors entrer à nouveau dans le parcours si la rentrée est autorisée. Voir [cette page](../building-journeys/journey-properties.md#entrance)

Pour terminer un parcours actif, nous vous recommandons de le fermer. L’arrivée de nouveaux clients dans le parcours sera alors bloquée. Les profils qui ont déjà rejoint le parcours peuvent l’expérimenter jusqu’à la fin. Consultez [cette section](#close-journey)

Vous pouvez arrêter un parcours uniquement lorsqu’une urgence s’est produite et qu’il doit être mis fin immédiatement à tout traitement sur un parcours. Les personnes qui l’ont déjà rejoint sont toutes stoppées dans leur progression. Consultez [cette section](../building-journeys/journey.md#stop-journey)

>[!IMPORTANT]
>
>Vous ne pouvez pas redémarrer un parcours [fermé](#close-journey) ou [arrêté](#stop-journey).


## Balise parcours-end {#end-tag}

Lors de la création d’un parcours, une balise de fin s’affiche à la fin de chaque chemin. Ce nœud ne peut pas être ajouté par un utilisateur, ne peut pas être supprimé et seul son libellé peut être modifié. Il marque la fin de chaque chemin du parcours. Si le parcours comporte plusieurs chemins, il est conseillé d’ajouter un libellé à chaque fin pour faciliter la lecture des rapports. En savoir plus sur les [rapports de parcours ](../reports/live-report.md).

![](assets/journey-end.png)

## Fermeture d’un parcours {#close-journey}

Les raisons suivantes peuvent entraîner la fermeture d&#39;un parcours :

* Le parcours est fermé manuellement par le biais du bouton [**[!UICONTROL Fermer aux nouvelles entrées]**](#close-to-new-entrances).
* Un parcours basé sur un segment unique qui a terminé son exécution et a atteint la temporisation globale de 91 jours.
* Après la dernière occurrence d’un parcours récurrent basé sur une audience.

Le fait de fermer un parcours manuellement assure que les clients qui l’ont déjà rejoint puissent terminer leur chemin, mais que les nouveaux utilisateurs ne puissent pas le rejoindre. Lorsqu&#39;un parcours est fermé (pour l&#39;une des raisons ci-dessus), le statut **[!UICONTROL Fermé]** lui est attribué. Il n’est alors plus accessible aux nouveaux individus. Les profils déjà présents dans le parcours peuvent terminer le parcours normalement. Au-delà de la temporisation globale par défaut de 91 jours, le statut du parcours passe à **Terminé**.

Après la temporisation globale du parcours de **91 jours**, un parcours Lecture d’audience passe au statut **Terminé**. Ce comportement est défini sur 91 jours uniquement, car toutes les informations sur les profils entrés dans le parcours sont supprimées 91 jours après leur entrée. Les personnes toujours présentes dans le parcours sont automatiquement affectées. Ils quittent le parcours après la temporisation de 91 jours.  En savoir plus sur [la temporisation globale du parcours ](../building-journeys/journey-properties.md#global_timeout).

La version d&#39;un parcours fermé ne peut pas être redémarrée ni supprimée. Vous pouvez la dupliquer ou en créer une nouvelle version. Seuls les parcours terminés peuvent être supprimés.

### Fermer aux nouvelles entrées {#close-to-new-entrances}

Pour fermer un parcours dans la liste des parcours, cliquez sur le bouton **[!UICONTROL Points de suspension]** situé à droite du nom du parcours et sélectionnez **[!UICONTROL Fermer aux nouvelles entrées]**.

![](assets/journey-finish-quick-action.png)

Vous pouvez également réaliser les opérations suivantes :

1. Dans la liste **[!UICONTROL Parcours]**, cliquez sur le parcours que vous souhaitez fermer.
1. En haut à droite, cliquez sur la flèche vers le bas.

   ![](assets/finish_drop_down_list.png)

1. Cliquez sur **[!UICONTROL Fermer aux nouvelles entrées]** et confirmez dans la boîte de dialogue.

>[!TIP]
>
>Un parcours unique basé sur les segments conserve le statut **Actif** même après une seule exécution. Les profils ne reviendront pas une fois terminés, mais le statut du parcours reste **Actif** jusqu’à l’expiration du délai d’expiration global par défaut. Vous pouvez le fermer manuellement plus tôt à l’aide de l’option **Fermer aux nouvelles entrées**.


## Arrêt d’un parcours {#stop-journey}

Si nécessaire, il est possible d’arrêter la progression de tous les individus dans le parcours. L’arrêt du parcours entraîne la temporisation de tous les individus du parcours. Cependant, le fait d’arrêter un parcours suppose qu&#39;il soit mis un terme à la progression de toutes les personnes qui y participent. Le parcours est simplement mis à l&#39;arrêt. Si vous souhaitez terminer par un parcours, il est recommandé de [le fermer](#close-journey).

À l’arrêt, le statut du parcours est défini sur **[!UICONTROL Arrêté]**.

Vous pouvez arrêter un parcours, par exemple, si un spécialiste marketing se rend compte que le parcours cible une audience incorrecte ou si une action personnalisée censée diffuser des messages ne fonctionne pas correctement. Pour arrêter un parcours dans la liste des parcours, cliquez sur le bouton **[!UICONTROL Points de suspension]** situé à droite du nom du parcours et sélectionnez **[!UICONTROL Arrêter]**.

![](assets/journey-finish-quick-action.png)

Vous pouvez également réaliser les opérations suivantes :

1. Dans la liste **[!UICONTROL Parcours]**, cliquez sur le parcours que vous souhaitez arrêter.
1. En haut à droite, cliquez sur la flèche vers le bas.

   ![](assets/finish_drop_down_list2.png)

1. Cliquez sur **[!UICONTROL Arrêter]** et confirmez dans la boîte de dialogue.
