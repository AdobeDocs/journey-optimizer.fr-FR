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
source-git-commit: 6c4e0418776622467e7f5b7bb3d9332d965becf1
workflow-type: ht
source-wordcount: '434'
ht-degree: 100%

---

# Notes de mise à jour anticipées {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées à la fin de chaque mois dans les [notes de mise à jour](release-notes.md).

**Les notes de mise à jour anticipées ci-dessous peuvent être modifiées sans avertissement préalable jusqu’à la date de disponibilité de la version**. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les [notes de mise à jour](release-notes.md) à la date de publication.

## Notes de mise à jour anticipées de juin 2024 {#e-2024}

**Date de publication** : 18-19 juin 2024

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


<!--<table>
<thead>
<tr>
<th><strong>Content Fragments customization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define specific fields in a fragment that can be edited when the fragment is added to a campaign or journey. This allows for the adjustment of content portions at the time of use, providing flexibility to override default values with context-specific details.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->


<table>
<thead>
<tr>
<th><strong>Assistant IA dans Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’assistant IA est une fonctionnalité de l’interface d’utilisation qui vous permet de parcourir et de comprendre les concepts Adobe et d’obtenir des informations opérationnelles sur votre environnement spécifique. Il est disponible dans plusieurs produits Adobe Experience Cloud, y compris Adobe Journey Optimizer.</p>
<p>Pour plus d’informations, consultez la <a href="../start/ai-assistant.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>





<!--table>
<thead>
<tr>
<th><strong>Multilingual messages in journeys and campaigns  (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now effortlessly create content in multiple languages within a single campaign or journey. With this feature, you can switch between languages when editing your campaign or your journey, streamlining the entire editing process and improving your capability to efficiently manage multilingual content.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Experimentation in journeys (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Already available in campaigns, Adobe Journey Optimizer now supports experiments in journeys. Experiments are randomized trials, which in the context of online testing, means that you expose some randomly selected users to a given variation of a message, and another randomly selected set of users to some other variation or treatment. After exposure, you can then measure the outcome metrics you are interested in, such as opens of emails, subscriptions, or purchases.</p>
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


**Gestion des décisions**

* **Prise en charge de plusieurs règles dans la gestion des décisions** : vous pouvez désormais ajouter jusqu’à 10 règles de limitation pour une offre donnée dans la gestion des décisions. Cela vous permet d’augmenter le niveau de contrôle sur la manière dont les offres sont envoyées. [En savoir plus](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

<!--**Content fragments**

* Fragments can now be edited, and changes can be propagated across all live journeys and campaigns where they are used.
* New statuses for content fragments have been introduced: **Draft**, **Live**, **Publishing**, and **Archived**. 
* To use a fragment in a journey or campaign, it must now be in the **Live** status. A new step has been added to the fragment creation process, allowing the fragment to be published and made available for use in journeys and campaigns. Note that fragment publishing requires a new permission.
   
   **CAUTION** - Since **Draft** and **Live** statuses have been introduced with Journey Optimizer June release, all fragments created before this release have the **Draft** status, even if they are used in a journey or campaign. Learn how to update your existing fragments in this section.-->

**Parcours**

* Le délai d’expiration global de parcours est passé de 30 à 91 jours.
* Adobe Journey Optimizer prend désormais en charge les demandes de suppression/d’accès pour les informations personnelles ainsi que les demandes de gestion du cycle de vie des données.
* Vous pouvez désormais redimensionner les colonnes de l’inventaire des parcours.
* **L’éditeur d’expression avancé dans la configuration des événements** est maintenant disponible de manière générale : vous pouvez désormais utiliser l’éditeur d’expression avancé lors de la configuration d’un événement, ce qui vous permet de définir des expressions plus complexes ou d’utiliser des fonctions dans la condition d’ID d’événement. Cette fonctionnalité est publiée en disponibilité limitée pour certaines clientes et certains clients uniquement. <!--[Read more](../event/about-creating.md)-->
* **Les politiques de fusion** sont maintenant disponibles de manière générale : les politiques de fusion utilisées par un parcours sont désormais visibles et cohérentes dans l’ensemble du parcours. Cette fonctionnalité est publiée en disponibilité limitée pour certaines clientes et certains clients uniquement. <!--[Read more](../building-journeys/journey-gs.md#merge-policies)-->



**Campagnes**

* Lors de la création d’une campagne dans Adobe Journey Optimizer, vous pouvez désormais choisir le type de campagne (planifiée ou déclenchée) dans une nouvelle boîte de dialogue modale.

<!--**Email channel**

* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)-->


**Canal SMS**

* Vous pouvez désormais ajouter des codes courts uniques pour chaque sandbox avec une seule configuration d’API, ce qui rend le processus plus efficace et plus simple.
  <!--* You can now modify existing SMS configurations.-->

**Canal in-app**

* **Fragment d’expression** : les fragments d’expression sont désormais disponibles pour le **Canal in-app**. <!--[Read more](../personalization/use-expression-fragments.md)-->


* Vous pouvez désormais utiliser le plug-in Edge Delivery pour obtenir les informations nécessaires pour comprendre et résoudre les problèmes liés à vos implémentations entrantes.
