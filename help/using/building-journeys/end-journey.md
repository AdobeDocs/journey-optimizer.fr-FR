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
source-git-commit: e435a4bf9d284845f27021b3d36c555def749fbe
workflow-type: tm+mt
source-wordcount: '756'
ht-degree: 50%

---

# Terminer un parcours {#journey-ending}

## Comment se termine un parcours en direct

Les parcours sont fermés lorsque le délai d’expiration du parcours global est atteint ou après la dernière occurrence d’un parcours récurrent basé sur l’audience. [Découvrez comment les parcours sont clôturés](#close-journey).

Si vous devez mettre fin à un parcours en direct, nous vous recommandons de [le fermer](#close-to-new-entrances) manuellement. L&#39;arrivée de nouveaux clients sur le parcours est alors bloquée. Les profils qui ont déjà rejoint le parcours peuvent l’expérimenter jusqu’à la fin.

Vous pouvez également [arrêter un parcours ](#stop-journey), uniquement en cas d’urgence et si tout le traitement du parcours doit être arrêté immédiatement. Les personnes qui sont déjà entrées dans un parcours sont toutes stoppées dans leur progression.

>[!IMPORTANT]
>
>* Vous ne pouvez pas redémarrer ou supprimer un parcours [fermé](#close-journey) ou [arrêté](#stop-journey). Vous pouvez la dupliquer ou en créer une nouvelle version.
>
>* Seuls les parcours terminés peuvent être supprimés.

## Comment les profils terminent un parcours

Un parcours se termine pour un individu dans deux contextes spécifiques :

* L’individu atteint à la dernière activité d’un chemin, puis passe à la [ balise de fin ](#end-tag).
* L’individu atteint une activité **Condition** (ou une activité **Attente** avec une condition) et ne répond à aucune des conditions.

L’individu peut alors entrer à nouveau dans le parcours si la rentrée est autorisée. [En savoir plus sur la gestion des entrées/rentrées](../building-journeys/journey-properties.md#entrance)

## Balise parcours-end {#end-tag}

Lors de la création d’un parcours, une balise de fin s’affiche à la fin de chaque chemin. Ce nœud ne peut pas être ajouté par un utilisateur, ne peut pas être supprimé et seul son libellé peut être modifié. Il marque la fin de chaque chemin du parcours.

Si le parcours comporte plusieurs chemins, il est conseillé d’ajouter un libellé à chaque fin pour faciliter la lecture des rapports. En savoir plus sur les [rapports de parcours ](../reports/live-report.md).

![](assets/journey-end.png)

## Fermeture d’un parcours {#close-journey}

Les raisons suivantes peuvent entraîner la fermeture d&#39;un parcours :

* Un parcours basé sur un segment unique qui a terminé son exécution et a atteint la temporisation globale de 91 jours.
* Après la dernière occurrence d’un parcours récurrent basé sur une audience.
* Le parcours est fermé manuellement par le biais du bouton [**[!UICONTROL Fermer aux nouvelles entrées]**](#close-to-new-entrances).

Après la temporisation globale du parcours de **91 jours**, un parcours Lecture d’audience passe au statut **Terminé**. Ce comportement est défini sur 91 jours uniquement, car toutes les informations sur les profils entrés dans le parcours sont supprimées 91 jours après leur entrée. Les personnes toujours présentes dans le parcours sont automatiquement affectées. Ils quittent le parcours après la temporisation de 91 jours.  En savoir plus sur [la temporisation globale du parcours ](../building-journeys/journey-properties.md#global_timeout).

>[!TIP]
>
>Un parcours unique basé sur les segments conserve le statut **Actif** même après une seule exécution. Les profils ne peuvent pas réintégrer une fois l’opération terminée, mais le statut du parcours reste **Actif** jusqu’à l’expiration du délai d’expiration global par défaut. Vous pouvez le fermer manuellement plus tôt à l’aide de l’option **Fermer aux nouvelles entrées**.

### Fermer aux nouvelles entrées {#close-to-new-entrances}

Le fait de fermer un parcours manuellement assure que les clients qui l’ont déjà rejoint puissent terminer leur chemin, mais que les nouveaux utilisateurs ne puissent pas le rejoindre. Lorsqu&#39;un parcours est fermé (pour l&#39;une des raisons ci-dessus), le statut **[!UICONTROL Fermé]** lui est attribué. Il n’est alors plus accessible aux nouveaux individus. Les profils déjà présents dans le parcours peuvent terminer le parcours normalement. Au-delà de la temporisation globale par défaut de 91 jours, le statut du parcours passe à **Terminé**.

Pour fermer un parcours dans la liste des parcours, cliquez sur le bouton **[!UICONTROL Points de suspension]** situé à droite du nom du parcours et sélectionnez **[!UICONTROL Fermer aux nouvelles entrées]**.

![](assets/journey-finish-quick-action.png)

Vous pouvez également réaliser les opérations suivantes :

1. Dans la liste **[!UICONTROL Parcours]**, cliquez sur le parcours que vous souhaitez fermer.
1. En haut à droite, cliquez sur la flèche vers le bas.

   ![](assets/finish_drop_down_list.png){width="50%" align="left" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Fermer aux nouvelles entrées]** et confirmez dans la boîte de dialogue.




## Arrêt d’un parcours {#stop-journey}

Si nécessaire, il est possible d’arrêter la progression de tous les individus dans le parcours. L’arrêt du parcours entraîne la temporisation de tous les individus du parcours. Cependant, le fait d’arrêter un parcours suppose qu&#39;il soit mis un terme à la progression de toutes les personnes qui y participent. Le parcours est simplement mis à l&#39;arrêt. Si vous souhaitez terminer par un parcours, il est recommandé de [le fermer](#close-journey).


Vous pouvez arrêter un parcours, par exemple, si un spécialiste marketing se rend compte que le parcours cible une audience incorrecte ou si une action personnalisée censée diffuser des messages ne fonctionne pas correctement. Pour arrêter un parcours dans la liste des parcours, cliquez sur le bouton **[!UICONTROL Points de suspension]** situé à droite du nom du parcours et sélectionnez **[!UICONTROL Arrêter]**.

![](assets/journey-finish-quick-action.png)

Vous pouvez également réaliser les opérations suivantes :

1. Dans la liste **[!UICONTROL Parcours]**, cliquez sur le parcours que vous souhaitez arrêter.
1. En haut à droite, cliquez sur la flèche vers le bas.

   ![](assets/finish_drop_down_list2.png){width="50%" align="left" zoomable="yes"}

1. Cliquez sur **[!UICONTROL Arrêter]** et confirmez dans la boîte de dialogue.

À l’arrêt, le statut du parcours est défini sur **[!UICONTROL Arrêté]**.
