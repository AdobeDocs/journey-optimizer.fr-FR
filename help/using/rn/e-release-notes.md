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
source-git-commit: 1b37da28e6dbb03c8c76dd9a6637dfd95447eb7e
workflow-type: tm+mt
source-wordcount: '371'
ht-degree: 24%

---

# Notes de mise à jour anticipées {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans les [notes de mise à jour](release-notes.md).

Les notes de mise à jour ci-dessous peuvent être modifiées sans avertissement préalable jusqu’à la date de disponibilité de la version. Les liens, les écrans et la documentation mise à jour sont publiés dans les [notes de mise à jour](release-notes.md), à la date de publication.

## Notes de mise à jour initiales d’octobre 2023 {#oct-rn-2023}

**Date de publication**: 25-26 octobre 2023

### Nouvelles fonctionnalités{#oct-2023-features}

Cette version apporte les nouvelles fonctionnalités répertoriées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Outils Sandbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’outil Sandbox vous permet de copier des objets sur plusieurs environnements de test en exploitant l’exportation et l’importation de packages. Un package peut se composer d’un ou de plusieurs objets. Tous les objets inclus dans un package doivent provenir du même environnement de test.</p>
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
<th><strong>MMS (Multimedia Message Service) en SMS (bêta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Avec le canal SMS, vous pouvez maintenant améliorer votre communication en envoyant des messages MMS (Multimedia Message Service), ce qui permet le partage d’images, de GIFs ou de vidéos avec vos clients. Notez que cette fonctionnalité est actuellement disponible en version bêta avec Sinch uniquement.</p>
<!--img src="assets/channel-reports.png"/-->
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>

### Améliorations {#oct-2023-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Audiences**

* Vous pouvez désormais cibler les audiences chargées à partir d’un fichier CSV dans les parcours et les campagnes.
* Vous pouvez désormais cibler les audiences créées par le biais de la composition de l’audience et utiliser les attributs d’enrichissement dans les Parcours.

>[!AVAILABILITY]
>
>Ces fonctionnalités sont actuellement disponibles en version bêta privée.

<!--
**Spam scoring for emails**

* When simulating an email content, a new option enables you to check how your content performs against inboxes spam filtering. This feature is currently proposed to a set of customers only (Limited Availability), and available for the Email channel.-->

**Alerte**

* Lorsqu’une erreur se produit dans l’une de vos campagnes, une icône d’avertissement s’affiche désormais dans la liste des campagnes avec l’état de la campagne.

**Campagnes**

* Vous pouvez désormais arrêter une campagne ponctuelle active, apporter des modifications et la reprendre. Cette amélioration est disponible en version bêta.

**Parcours**

* La durée maximale que vous pouvez définir dans n’importe quel temps d’attente est désormais de 29 jours au lieu de 30. Cela s’applique à :

   * la valeur **Durée** dans le champ [activité d’attente](../building-journeys/wait-activity.md)
   * la valeur **Période d’attente de rentrée** in [Propriétés du parcours](../building-journeys/journey-gs.md#entrance)
   * la valeur **Attendre** dans la définition du délai d’expiration de [general](../building-journeys/general-events.md#events-specific-time) et [réaction](../building-journeys/reaction-events.md) événements .

**Consentement dans la configuration du canal**

* Vous pouvez désormais sélectionner une action marketing au niveau de la surface du canal. Lorsqu’elles sont utilisées en surface, toutes les stratégies de consentement associées à cette action marketing sont exploitées afin de respecter les préférences de vos clients.

**Gestion des décisions**

* Plusieurs libellés relatifs à la limitation des offres dans l’interface de gestion des décisions ont été mis à jour.
