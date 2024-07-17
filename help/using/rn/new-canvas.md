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
source-git-commit: 6b9044117dcdd7554dea0c5f791a6dcfb0218010
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 2%

---

# Bienvenue dans le concepteur de parcours amélioré {#new-canvas}

Journey Optimizer propose désormais un **modèle de parcours simplifié** visant à améliorer l’expérience utilisateur et les processus internes. À compter de la version d’avril, vous pouvez bénéficier des fonctionnalités suivantes :

* Un **canevas de parcours reconçu** conçu pour une expérience d’interface utilisateur modernisée
* Une interface utilisateur de **création de rapports en direct** directement disponible dans la zone de travail du parcours

>[!NOTE]
>
>Gardez à l’esprit que le déploiement de cette fonctionnalité sera progressif. Il se peut que vous ne voyiez pas les modifications immédiatement.

## Mises à jour du modèle de parcours

Le nouveau modèle de parcours sera en ligne avec le modèle existant, ce qui signifie qu’il y aura des parcours utilisant **deux modèles différents** :

* Le modèle hérité
* Le nouveau modèle

Tous les parcours du modèle hérité y resteront. Vous pourrez toujours les modifier, les tester ou les publier. Toute nouvelle version créée à partir d’un parcours sur le modèle hérité y restera également. Il n’existe **aucune modification fonctionnelle** autour de ces parcours.

Comme vous pouvez le voir dans la capture d’écran ci-dessous, les noeuds sont en forme ronde, qui est l’ancienne interface utilisateur pour les parcours sur le modèle hérité.

![](assets/new-canvas.png)

Cependant, lorsque vous **créez un parcours** ou **dupliquez un  existant**, il se trouve sur le nouveau modèle. Les parcours sur le modèle hérité seront toujours pris en charge jusqu’à ce qu’une majorité de clients soient transférés vers le nouveau modèle.

Le nouveau modèle de parcours présente une limitation. Il ne sera **pas possible de copier et coller des activités du modèle hérité vers le nouveau modèle, et inversement**. Si vous souhaitez effectuer cette opération, nous vous conseillons de dupliquer votre parcours hérité pour le changer en nouveau modèle, puis de copier vos activités.

Dans la capture d’écran ci-dessous, vous pouvez voir l’interface utilisateur repensée pour le canevas de parcours (disponible uniquement avec le nouveau modèle) :

![](assets/new-canvas2.png)

**Toute nouvelle fonctionnalité ajoutée au concepteur de parcours (y compris les rapports en direct) ne sera disponible que pour les parcours sur le nouveau modèle à partir de ce moment.**

## Amélioration de la conception du canevas de parcours

Avec le nouveau modèle de parcours, nous proposons une **interface utilisateur de canevas de parcours** nouvelle et améliorée, qui s’intègre parfaitement à l’écosystème d’applications et de solutions Adobe Experience Cloud, ce qui permet une expérience utilisateur intuitive et efficace. Tout parcours dans le nouveau modèle sera sur cette nouvelle conception.

![](assets/new-canvas3.gif)

Les activités seront désormais représentées par des cases carrées avec les fonctionnalités suivantes :

* La première ligne représentant le type d’activité qui sera souvent remplacée par des informations plus contextuelles (dans Lecture d’audience, elle contiendra le nom de l’audience sélectionnée) ou par un libellé personnalisé si vous en définissez une.
* La deuxième ligne représente toujours le type d’activité.

![](assets/new-canvas4.png)

Cette nouvelle interface utilisateur améliore la lisibilité du canevas de parcours en fournissant des **libellés et types d’activité plus clairs**.

Elle permet également à l’équipe produit d’ajouter plus d’informations sur la zone de travail avec moins de clics. Un exemple d’&quot;informations supplémentaires&quot; est l’inclusion des rapports en direct dans le canevas de parcours, où vous pouvez voir les profils entrant et sortant de vos activités en raison d’erreurs.

![](assets/new-canvas5.png)

## Création de rapports en direct dans le canevas de parcours

Outre la disposition améliorée du canevas de parcours, une nouvelle fonctionnalité est introduite pour permettre aux utilisateurs d’afficher les mesures de création de rapports en temps réel à partir de **les dernières 24 heures**, appelées rapports en direct, directement dans la zone de travail du parcours.

Pour chaque activité au sein de chaque parcours actif utilisant le nouveau modèle, vous avez accès aux éléments suivants :


* Nombre de profils entrant dans cette activité.
* Nombre de profils sortant de cette activité en raison d’une erreur.

![](assets/new-canvas6bis.png)

<!--`
With every live journey on the new model, you will be able to see two types of "last 24 hours" reporting information:

* On a **new insert**, you will see:
    * The number of profiles that have been exported for audience-triggered journeys. You will see the number of profiles available in the last export job alongside the time when that export has been made.
    * The number of profiles who exited the journey
    * The percentage of errors
    ![](assets/new-canvas7.png)
* **On each activity**, you will see the number of profiles who entered that activity and the number who exited because of an error:
    ![](assets/new-canvas8.png)
-->
<!--
Please note that you may see differences between the number of exported profiles and the number of profiles flowing through the journey. The exported profiles count only provides information about the last export job being made while the number of profiles entering an activity only contains profiles who did it in the last 24 hours. This can especially be visible on recurring daily journeys as there could be a data overlap between two days.
-->
