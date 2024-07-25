---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
description: Notes de mise à jour anticipées de Journey Optimizer
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: ad4599874cb04b58d26a93197485818f4db1ecc4
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 76%

---

# Notes de mise à jour anticipées {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées à la fin de chaque mois dans les [notes de mise à jour](release-notes.md).

**Les notes de mise à jour anticipées ci-dessous peuvent être modifiées sans avertissement préalable jusqu’à la date de disponibilité de la version**. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les [notes de mise à jour](release-notes.md) à la date de publication.

## Notes de mise à jour anticipées de juillet 2024 {#e-2024}

**Date de version** : 30-31 juillet 2024

### Nouvelles fonctionnalités {#e-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Workflow de préchauffage d’adresses IP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Si vous envoyez des e-mails sur une toute nouvelle adresse IP, vous pouvez désormais facilement exécuter des workflows de préchauffage d’adresses IP directement à partir de l’interface d’utilisation. Adobe Journey Optimizer offre un moyen standardisé et efficace de préchauffer vos adresses IP en respectant les bonnes pratiques de délivrabilité optimale.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Canal SMS avec n’importe quel fournisseur (version bêta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais configurer d’autres fournisseurs de SMS dans Journey Optimizer, en plus des fournisseurs par défaut Sinch, Infobip et Twilio.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Composition d’audience fédérée (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La composition d’audiences fédérées est désormais disponible dans Adobe Journey Optimizer. Il permet aux entreprises de composer des données pour une meilleure utilisation dans divers cas d’utilisation. Grâce à cette nouvelle approche, en tant qu’utilisateur Adobe Real-Time Customer Data Platform et/ou Adobe Journey Optimizer, vous pouvez fédérer les jeux de données directement à partir de votre entrepôt de données existant pour créer et enrichir les audiences et attributs Adobe Experience Platform dans un seul système.</p>
<!--p>For more information, refer to the <a href="https://experienceleague.adobe.com/en/docs/federated-audience-composition/using/home"  target="_blank">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Marketo Engage custom action</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now integrate Adobe Journey Optimizer with Adobe Marketo Engage to build your B2B use cases. From a journey, a new custom action allows you to ingest data into Marketo.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Improved channel configurations</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The current channel surface capabilities have been enhanced for a consistent approach across all channels. You can now define, manage, and reuse these configurations for any of your channels.</p>
<p><ul>
<li>Channel surfaces are now renamed to <strong>Channel configurations</strong></li>
<li>From the Channel configurations inventory you can now create reusable channel configurations for all channels, including now Web, In-app messaging, or Code-based experience</li>
<li>Object level access control (OLAC) is now available for each channel configuration, allowing you to decide which of your users are allowed to create or use specific configurations</li>
<li>For some channels, you can create channel configurations that target multiple platforms. An example here would be an In-app messaging channel configuration that can target a web page, an iOS app and an Android app.</li>
</ul></p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


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

* (Disponible le 8 juillet) Vous pouvez désormais utiliser l’éditeur d’expression avancé lors de la configuration d’un événement, ce qui vous permet de définir des expressions plus complexes ou d’utiliser des fonctions dans la condition d’identifiant d’événement. [En savoir plus](../event/about-creating.md#adv-exp-editor)

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
