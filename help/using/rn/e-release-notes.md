---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
description: Notes de mise à jour anticipées de Journey Optimizer
feature: Release Notes
topic: Content Management
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 9fdaff7a4364bb7ecfeec27446ed8f4b4ce34488
workflow-type: tm+mt
source-wordcount: '306'
ht-degree: 52%

---

# Notes de mise à jour anticipées {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées à la fin de chaque mois dans les [notes de mise à jour](release-notes.md).

**Les notes de mise à jour anticipées ci-dessous peuvent être modifiées sans avertissement préalable jusqu’à la date de disponibilité de la version**. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les [notes de mise à jour](release-notes.md) à la date de publication.

## Notes de mise à jour anticipées d’août 2024 {#e-2024}

**Date de publication** : 20-21 août 2024

### Nouvelles fonctionnalités {#e-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Action personnalisée Marketo Engage</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais intégrer Adobe Journey Optimizer à Adobe Marketo Engage pour créer vos cas d’utilisation B2B. Depuis un parcours, une nouvelle action personnalisée vous permet d’ingérer des données dans Marketo.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Amélioration des configurations de canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les fonctionnalités actuelles de surface de canal ont été améliorées pour une approche cohérente sur tous les canaux. Vous pouvez maintenant définir, gérer et réutiliser ces configurations pour l’un de vos canaux.</p>
<p><ul>
<li>Les surfaces de canal sont désormais renommées <strong>Configurations de canal</strong></li>
<li>L’inventaire des configurations de canal vous permet désormais de créer des configurations de canal réutilisables pour tous les canaux, y compris désormais les canaux web, les messages in-app ou l’expérience basée sur le code.</li>
<li>Le contrôle d’accès au niveau de l’objet (OLAC) est désormais disponible pour chaque configuration de canal, ce qui vous permet de décider lequel de vos utilisateurs est autorisé à créer ou à utiliser des configurations spécifiques.</li>
<li>Pour certains canaux, vous pouvez créer des configurations de canal qui ciblent plusieurs plateformes. Il peut s’agir, par exemple, d’une configuration de canal de messagerie in-app pouvant cibler une page web, une application iOS et une application Android.</li>
</ul></p>
<p>Pour plus d’informations, consultez la <a href="../configuration/ip-warmup-gs.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Améliorations {#e-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Parcours**

* Dans l’activité **Condition**, par défaut, la condition Heure est désormais définie par heure, de 00:00 à 12:00. [En savoir plus](../building-journeys/condition-activity.md#time_condition)

**Audiences**

* L’utilisation d’audiences issues d’un chargement personnalisé (fichier CSV) est désormais disponible avec Privacy and Security Shield.

<!--
**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.-->

<!--* The `event-id` condition is now automatically filled during test mode. -->

<!--**SMS channel**

* You can now modify existing SMS configurations.-->

<!--
**In-app channel**

* Expression fragments are now available for the In-app channel.-->
