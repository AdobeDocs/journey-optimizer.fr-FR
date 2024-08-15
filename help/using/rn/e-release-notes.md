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
source-git-commit: 128a56b543f470bf967fd195fde73ff7b32b2a17
workflow-type: tm+mt
source-wordcount: '633'
ht-degree: 34%

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
<th><strong>Configuration de canal guidée</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La configuration guidée du canal vous permet d’automatiser les étapes de configuration du canal mobile dans une expérience unifiée afin de commencer plus rapidement avec Journey Optimizer. Cette configuration facilite la configuration rapide des canaux marketing, en s’assurant que toutes les ressources requises sont facilement disponibles dans Experience Platform, Journey Optimizer et Data Collection. Cela permet à votre équipe marketing de commencer immédiatement la création de campagne et de parcours.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Cartes de contenu</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La carte de contenu est une nouvelle fonctionnalité de messagerie numérique de Adobe Journey Optimizer qui fournit du contenu personnalisé et attrayant directement dans les applications mobiles et les sites web. Contrairement aux notifications push traditionnelles, les cartes de contenu s’intègrent de manière transparente à l’interface utilisateur, offrant des mises à jour persistantes et non intrusives qui améliorent l’interaction et l’expérience utilisateur.</p>
<p>Grâce à cette fonctionnalité, les marketeurs peuvent présenter du contenu multimédia pertinent aux utilisateurs, augmenter l’engagement des utilisateurs et veiller à ce que les messages importants soient affichés sans interrompre le parcours de l’utilisateur.</p>
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


<table>
<thead>
<tr>
<th><strong>Action personnalisée Marketo Engage</strong><br/></th>
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
<th><strong>Variables dans les fragments de contenu</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les fragments peuvent désormais utiliser des variables d’entrée, à la fois dans les <a href="../personalization/use-expression-fragments.md">fragments d’expression</a> et les <a href="../email/use-visual-fragments.md">fragments visuels</a>. Vous pouvez utiliser ces variables pour personnaliser le contenu et les paramètres de vos messages, dans vos campagnes et parcours.</p>
</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Workflow de préchauffage d’adresses IP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Date de disponibilité : 13 août</p>
<p>Si vous envoyez des e-mails sur une toute nouvelle adresse IP, vous pouvez désormais facilement exécuter des workflows de préchauffage d’adresses IP directement à partir de l’interface d’utilisation. Adobe Journey Optimizer offre un moyen standardisé et efficace de préchauffer vos adresses IP en respectant les bonnes pratiques de délivrabilité optimale.</p>
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
* Lors de la création de vos parcours, les alertes s’affichent désormais dans une liste déroulante, afin de s’aligner sur les alertes de campagne et d’offrir une expérience utilisateur cohérente. [En savoir plus](../building-journeys/troubleshooting.md#checking-for-errors-before-testing)
* Les options de zoom de la barre d’outils de parcours ont été améliorées : le pourcentage de zoom est désormais visible et vous pouvez désormais facilement réinitialiser la valeur de zoom sur 100 %.

**Audiences**

* L’utilisation d’audiences issues d’un chargement personnalisé (fichier CSV) est désormais disponible avec Privacy and Security Shield.
* Lors du ciblage d’une audience de téléchargement personnalisée (fichier CSV), vous pouvez désormais utiliser les attributs du fichier dans vos campagnes et parcours. Ces attributs sont disponibles dans l’éditeur de personnalisation, pour personnaliser vos messages et dans l’éditeur d’expression avancé de parcours.

<!--
**Push channel**

* You can now add your mobile application push credentials inside Adobe Journey Optimizer channel configuration settings. Creating an App surface in Adobe Experience Platform Data Collection is no longer required.-->

<!--* The `event-id` condition is now automatically filled during test mode. -->

<!--**SMS channel**

* You can now modify existing SMS configurations.-->

<!--
**In-app channel**

* Expression fragments are now available for the In-app channel.-->
