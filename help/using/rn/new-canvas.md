---
solution: Journey Optimizer
product: journey optimizer
title: Nouvelle interface de parcours
feature: Release Notes
topic: Content Management
description: Nouvelle interface de parcours
hide: true
hidefromtoc: true
exl-id: 03828fca-dde7-4b3b-b890-2c007d1245cc
source-git-commit: 17dc12f66a740b1ebea360aa20453d9b750d3e5c
workflow-type: tm+mt
source-wordcount: '541'
ht-degree: 1%

---

# Bienvenue dans le concepteur de Parcours amélioré {#new-canvas}

>[!CONTEXTUALHELP]
>id="ajo_new_canvas"
>title="Nouveautés"
>abstract="Nouvelle zone de travail"

Bienvenue dans le meilleur concepteur de parcours !

Nous avons développé une **modèle de parcours simplifié** qui vise à améliorer les processus internes. Bien que ce nouveau modèle soit une amélioration principale, notre équipe a profité de l’occasion pour ajouter des fonctionnalités visibles et bénéfiques pour les utilisateurs de Journey Optimizer :

* A **canevas de parcours reconçu** Conçu pour une expérience d’interface utilisateur modernisée
* A **création de rapports en direct** Interface utilisateur directement disponible dans le canevas de parcours

>[!AVAILABILITY]
>
>Gardez à l’esprit que le déploiement de cette fonctionnalité sera progressif. Il se peut que vous ne voyiez pas les modifications immédiatement.

## Mises à jour du modèle de parcours

Le nouveau modèle de parcours sera associé au modèle existant, ce qui signifie qu’il y aura des parcours utilisant **deux modèles différents**:

* L’ancienne, appelée &quot;v1&quot;
* Et le nouveau, appelé &quot;v2&quot;

Tous les parcours de la version 1 restent dans la version 1. Vous pourrez toujours les modifier, les tester ou les publier. Toute nouvelle version créée à partir d’une version 1 restera également dans la version 1. Il y a **aucune modification fonctionnelle** environ 1 parcours.

Comme vous pouvez le voir dans la capture d’écran ci-dessous, les noeuds sont en forme ronde, qui est l’ancienne interface utilisateur pour les parcours sur le modèle v1.

![](assets/new-canvas.png)

Cependant, lorsque vous **Création d’un parcours** ou **dupliquer un existant**, il s’agira d’un parcours v2.  Nous prévoyons de continuer à prendre en charge les parcours v1 jusqu’à ce qu’une majorité de clients soient transférés vers la version v2.

Il y a une limitation au nouveau modèle de parcours : il sera **impossible de copier et coller des activités d’un parcours v1 vers une v2 et vice versa.**. Si vous souhaitez effectuer cette opération, nous vous conseillons de dupliquer votre parcours v1 pour en faire un v2, puis de copier vos activités.

Dans la capture d’écran ci-dessous, vous pouvez voir l’interface utilisateur repensée pour le canevas de parcours (disponible uniquement avec le modèle v2) :

![](assets/new-canvas2.png)

**À partir de maintenant, toute nouvelle fonctionnalité ajoutée au concepteur de parcours (y compris les rapports en direct) ne sera disponible que pour les parcours v2.**

## Amélioration de la conception du canevas de parcours

Avec le nouveau modèle de parcours, nous introduisons un nouveau modèle amélioré. **Interface utilisateur du canevas de parcours**, qui s’intègre parfaitement dans l’écosystème d’applications et de solutions Adobe Experience Cloud, ce qui permet une expérience utilisateur intuitive et efficace. Tout parcours de la pile v2 se trouve sur cette nouvelle conception.

![](assets/new-canvas3.gif)

Les activités seront désormais représentées par des cases carrées avec les fonctionnalités suivantes :

* La première ligne représentant le type d’activité qui sera souvent remplacée par des informations plus contextuelles (par exemple : sur Lecture d’audience, elle contiendra le nom de l’audience sélectionnée) ou par un libellé personnalisé si vous en définissez une.
* La deuxième ligne représente toujours le type d’activité.

![](assets/new-canvas4.png)

Cette nouvelle interface utilisateur améliore la lisibilité du canevas de parcours en fournissant des **libellés et types d’activité plus clairs**.

Elle permet également à l’équipe produit d’ajouter plus d’informations sur la zone de travail avec moins de clics. Un exemple d’&quot;informations supplémentaires&quot; est l’inclusion des rapports en direct dans le canevas de parcours, où vous pouvez voir les profils entrant et sortant de vos activités en raison d’erreurs.

![](assets/new-canvas5.png)


## Création de rapports en direct dans le canevas de parcours

En plus de la nouvelle conception de la toile de parcours, nous vous proposons la possibilité de voir, **sur chaque activité**, le nombre de profils ayant participé à cette activité et le nombre ayant quitté l&#39;activité en raison d&#39;une erreur :

<!--
**last 24 hours reporting metrics** (called "live reporting") directly in the journey canvas.

![](assets/new-canvas6.png)

With every live journey on the new model, you will be able to see two types of "last 24 hours" reporting information:

* On a **new insert**, you will see:
    * The number of profiles that have been exported for audience-triggered journeys. You will see the number of profiles available in the last export job alongside the time when that export has been made.
    * The number of profiles who exited the journey
    * The percentage of errors
    ![](assets/new-canvas7.png)

* **On each activity**, you will see the number of profiles who entered that activity and the number who exited because of an error:
-->

![](assets/new-canvas8.png)

L’interface utilisateur est automatiquement actualisée toutes les minutes.

<!--
Please note that you may see differences between the number of exported profiles and the number of profiles flowing through the journey. The exported profiles count only provides information about the last export job being made while the number of profiles entering an activity only contains profiles who did it in the last 24 hours. This can especially be visible on recurring daily journeys as there could be a data overlap between two days.
-->