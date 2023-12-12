---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
description: Notes de mise à jour anticipées de Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 004eb41b084f32993ec437f589e4e3d2cf7500d3
workflow-type: tm+mt
source-wordcount: '356'
ht-degree: 100%

---

# Notes de mise à jour anticipées {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans les [notes de mise à jour](release-notes.md).

Les notes de mise à jour ci-dessous peuvent être modifiées sans avertissement préalable jusqu’à la date de disponibilité de la version. Les liens, les écrans et la documentation mise à jour sont publiés dans les [notes de mise à jour](release-notes.md), à la date de publication.

## Notes de mise à jour anticipées d’octobre 2023 {#oct-rn-2023}

**Date de publication** : 25-26 octobre 2023

### Nouvelles fonctionnalités{#oct-2023-features}

Cette version apporte les nouvelles fonctionnalités répertoriées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Outil Sandbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’outil Sandbox vous permet de copier des objets sur plusieurs sandbox en exploitant l’export et l’import de packages. Un package peut se composer d’un ou de plusieurs objets. Tous les objets inclus dans un package doivent provenir du même sandbox.</p>
<!--img src="../data/assets/dataset-export-setup.png"-->
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>Composed audiences in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use audiences created in composition workflows in your journeys to target customers. Once an audience composition is published, and the audience saved, use a Read Audience activity to select this new audience in your journey canvas.</p>
<img src="assets/channel-reports.png"/>
<p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table -->

<table>
<thead>
<tr>
<th><strong>MMS (Multimedia Message Service, service de messagerie multimédia) dans les SMS (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Avec le canal SMS, vous pouvez maintenant améliorer votre communication en envoyant des MMS, ce qui permet le partage d’images, de GIF ou de vidéos avec vos clientes et clients. Notez que cette fonctionnalité est actuellement disponible en version Beta avec Sinch uniquement.</p>
<!--img src="assets/channel-reports.png"/-->
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>

### Améliorations {#oct-2023-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Audiences**

* Vous pouvez désormais cibler les audiences chargées à partir d’un fichier CSV dans les parcours et les campagnes.
* Vous pouvez désormais cibler les audiences créées par le biais de la composition de l’audience et utiliser les attributs d’enrichissement dans les parcours.

>[!AVAILABILITY]
>
>Ces fonctionnalités sont actuellement disponibles en version Private Beta.

<!--
**Spam scoring for emails**

* When simulating an email content, a new option enables you to check how your content performs against inboxes spam filtering. This feature is currently proposed to a set of customers only (Limited Availability), and available for the Email channel.-->

**Campagnes**

<!--* You can now stop a live one-time campaign, make modifications and resume it again. This improvement is available in Beta.-->
* Lorsqu’une erreur se produit dans l’une de vos campagnes, une icône d’avertissement s’affiche désormais dans la liste des campagnes avec le statut de la campagne.

**Parcours**

* La durée maximale que vous pouvez définir dans n’importe quel temps d’attente est désormais de 29 jours au lieu de 30. Cela s’applique aux éléments suivants :

   * Le champ **Durée** dans l’[activité d’attente](../building-journeys/wait-activity.md).
   * La **période d’attente de reprise** dans les [propriétés du parcours](../building-journeys/journey-gs.md#entrance).
   * Le champ **Attendre pendant** dans la définition de la temporisation des événements [généraux](../building-journeys/general-events.md#events-specific-time) et de [réaction](../building-journeys/reaction-events.md).

**Consentement dans la configuration des canaux**

* Vous pouvez désormais sélectionner une action marketing au niveau de la surface de canal. Lorsqu’elles sont utilisées en surface, toutes les stratégies de consentement associées à cette action marketing sont utilisées afin de respecter les préférences de vos clientes et clients.

**Gestion des décisions**

* Plusieurs libellés relatifs à la limitation des offres dans l’interface de gestion des décisions ont été mis à jour.
