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

Journey Optimizer propose désormais un **modèle de parcours simplifié** qui vise à améliorer l’expérience utilisateur et les processus internes. À compter de la version d’avril, vous pouvez bénéficier des fonctionnalités suivantes :

* Une **toile de parcours repensée** conçue pour une expérience utilisateur modernisée
* Interface utilisateur **rapports en direct** directement disponible dans la zone de travail du parcours

>[!NOTE]
>
>N’oubliez pas que le déploiement de cette fonctionnalité sera progressif. Il se peut que les modifications ne s’affichent pas immédiatement.

## Mises à jour sur le modèle de parcours

Le nouveau modèle de parcours cohabitera avec le modèle existant, ce qui signifie que des parcours utiliseront **deux modèles différents** :

* Modèle hérité
* Le nouveau modèle

Tous les parcours du modèle hérité y resteront. Vous pourrez toujours les modifier, les tester ou les publier. Toute nouvelle version créée à partir d’un parcours sur le modèle hérité y restera également. Il n&#39;y a **aucun changement fonctionnel** autour de ces parcours.

Comme vous le voyez dans la capture d’écran ci-dessous, les nœuds ont une forme arrondie, ce qui correspond à l’ancienne interface utilisateur pour les parcours du modèle hérité.

![](assets/new-canvas.png)

Cependant, lorsque vous **créez un nouveau parcours** ou **dupliquez un modèle existant**, celui-ci sera sur le nouveau modèle. Les parcours de l’ancien modèle seront toujours pris en charge jusqu’à ce qu’une majorité de clients passent au nouveau modèle.

Il existe une limite au nouveau modèle de parcours ; il **sera pas possible de copier et coller des activités du modèle hérité dans le nouveau modèle et vice versa**. Si vous souhaitez le faire, nous vous conseillons de dupliquer votre ancien parcours pour le passer au nouveau, puis de copier vos activités.

Dans la capture d’écran ci-dessous, vous pouvez voir l’interface utilisateur repensée pour la zone de travail du parcours (disponible uniquement avec le nouveau modèle) :

![](assets/new-canvas2.png)

**À partir de maintenant, toute nouvelle fonctionnalité ajoutée au concepteur de parcours (y compris les rapports en direct) ne sera disponible que pour les parcours sur le nouveau modèle.**

## Amélioration de la conception de la zone de travail de parcours

Avec le nouveau modèle de parcours, nous introduisons une interface utilisateur de zone de travail de parcours **** nouvelle et améliorée, qui s’intègre de manière transparente dans l’écosystème des solutions et applications Adobe Experience Cloud, pour une expérience utilisateur intuitive et efficace. Tout parcours du nouveau modèle sera sur cette nouvelle conception.

![](assets/new-canvas3.gif)

Les activités seront désormais représentées par des cases carrées avec les fonctionnalités suivantes :

* La première ligne représentant le type d’activité qui sera souvent remplacée par davantage d’informations contextuelles (dans Lecture d’audiences, elle contiendra le nom de l’audience sélectionnée) ou par un libellé personnalisé si vous en définissez un.
* Deuxième ligne représentant toujours le type d’activité.

![](assets/new-canvas4.png)

Cette nouvelle interface utilisateur améliore la lisibilité de la zone de travail du parcours en fournissant des libellés et des types d’activité **plus clairs**.

Il permet également à l’équipe produit d’ajouter plus d’informations sur la zone de travail avec moins de clics. Un exemple d’« informations supplémentaires » serait l’inclusion de rapports dynamiques dans la zone de travail du parcours, où vous pouvez voir les profils qui rejoignent et quittent vos activités en raison d’erreurs.

![](assets/new-canvas5.png)

## Rapports dynamiques dans la zone de travail du parcours

Outre l’amélioration de la disposition de la zone de travail de parcours, une nouvelle fonctionnalité a été introduite pour permettre aux utilisateurs d’afficher les mesures de rapports en temps réel des **dernières 24 heures**, appelées rapports en direct, directement dans la zone de travail de parcours.

Pour chaque activité de chaque parcours actif utilisant le nouveau modèle, vous avez accès aux éléments suivants :


* Nombre de profils participant à cette activité.
* Nombre de profils ayant quitté cette activité en raison d’une erreur.

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
