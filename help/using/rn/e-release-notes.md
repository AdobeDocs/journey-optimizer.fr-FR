---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
description: Notes de mise à jour anticipées de Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 4dc269b0671b99eaddeebf358ebe4e45f5c4c721
workflow-type: tm+mt
source-wordcount: '455'
ht-degree: 31%

---

# Notes de mise à jour anticipées {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées à la fin de chaque mois dans les [notes de mise à jour](release-notes.md).

**Les notes de mise à jour anticipées ci-dessous peuvent être modifiées sans avertissement préalable jusqu’à la date de disponibilité de la version**. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les [notes de mise à jour](release-notes.md) à la date de publication.

## Notes de mise à jour anticipées de juillet 2024 {#e-2024}

**Date de publication** : 30-31 juillet 2024

### Nouvelles fonctionnalités {#e-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Workflow de nettoyage d’IP (GA)</strong><br/></th>
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
<th><strong>Canal SMS avec n'importe quel fournisseur</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais configurer d’autres fournisseurs de SMS dans Journey Optimizer, en plus des fournisseurs par défaut, Sinch, Infobip et Twilio.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
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
<p>Vous pouvez désormais intégrer Adobe Journey Optimizer à Adobe Marketo Engage pour créer vos cas d’utilisation B2B. Depuis un parcours, une nouvelle action personnalisée vous permet d’ingérer des données dans Marketo.</p>
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
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
<!--p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p-->
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

* (Disponibilité : 8 juillet) Vous pouvez désormais utiliser l’éditeur d’expression avancé lors de la configuration d’un événement, ce qui vous permet de définir des expressions plus complexes ou d’utiliser des fonctions dans la condition d’identifiant d’événement. [En savoir plus](../event/about-creating.md#adv-exp-editor)

* La condition `event-id` est désormais automatiquement remplie en mode test.

**Canal SMS**

* Vous pouvez maintenant modifier les configurations SMS existantes.

**Canal in-app**

* Les fragments d’expression sont désormais disponibles pour le canal In-App.

**Canal push**

* Vous pouvez maintenant ajouter vos informations d’identification push d’application mobile dans les paramètres de configuration du canal Adobe Journey Optimizer. La création d’une surface d’application dans la collecte de données Adobe Experience Platform n’est plus nécessaire.

**Audiences**

* L’utilisation d’audiences et d’attributs provenant de la composition de l’audience et du téléchargement personnalisé (fichier CSV) est désormais disponible avec Healthcare Shield ou Privacy and Security Shield.