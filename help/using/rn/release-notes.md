---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
topic: Content Management
description: Notes de mise à jour de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 0e5d1e7a7520579b1fae7898f67cb10ee3915e1c
workflow-type: tm+mt
source-wordcount: '1152'
ht-degree: 74%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour.

[!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous à la [newsletter trimestrielle d’Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} dès aujourd’hui, et recevez les dernières mises à jour produits, les articles les plus intéressants, des cas pratiques, des conseils et bien plus encore, directement dans votre boîte de réception, tous les trimestres.


## Notes de mise à jour initiales de juin 2024 {#24-6-2024}

**Les notes de mise à jour anticipées ci-dessous peuvent être modifiées sans préavis jusqu’à la date de publication.**.

**Date de publication**: 18-19 juin 2024

### Nouvelles fonctionnalités {#june-24-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Workflow de maintenance d’IP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Si vous envoyez des emails sur une toute nouvelle adresse IP, vous pouvez désormais facilement exécuter des workflows de chauffage des adresses IP directement à partir de l’interface utilisateur. Adobe Journey Optimizer offre un moyen standardisé et efficace d’affiner vos adresses IP en respectant les bonnes pratiques de délivrabilité optimale.</p>
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
<th><strong>Assistant IA dans Adobe Journey Optimizer</strong><br/></th>
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
<th><strong>Reporting with Customer Journey Analytics (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer reporting is now fully integrated with Customer Journey Analytics capabilities, standardizing reporting across both platforms and improving data consistency and reliability. This seamless integration between Journey Optimizer and Customer Journey Analytics provides a clearer view of performance metrics, enabling users to make more informed decisions.</p>
</td>
</tr>
</tbody>
</table-->


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
<p>Multilingual content is currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
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
<p>Experimentation in journeys is currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
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

### Améliorations {#june24-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.


**Gestion des décisions**

* **Prise en charge de plusieurs règles dans la gestion des décisions** - Vous pouvez désormais ajouter jusqu’à 10 règles de limitation pour une offre donnée dans la gestion des décisions. Cela vous permet d’augmenter le niveau de contrôle sur la manière dont les offres sont envoyées. [En savoir plus](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

<!--**Content fragments**

* Fragments can now be edited, and changes can be propagated across all live journeys and campaigns where they are used.
* New statuses for content fragments have been introduced: **Draft**, **Live**, **Publishing**, and **Archived**. 
* To use a fragment in a journey or campaign, it must now be in the **Live** status. A new step has been added to the fragment creation process, allowing the fragment to be published and made available for use in journeys and campaigns. Note that fragment publishing requires a new permission.
   
   **CAUTION** - Since **Draft** and **Live** statuses have been introduced with Journey Optimizer June release, all fragments created before this release have the **Draft** status, even if they are used in a journey or campaign. Learn how to update your existing fragments in this section.-->

**Parcours**

* Le délai d’attente global par parcours a été augmenté de 30 à 90 jours.
* Adobe Journey Optimizer prend désormais en charge les demandes de suppression/accès des informations personnelles ainsi que les demandes de gestion du cycle de vie des données.
* Vous pouvez désormais redimensionner les colonnes de l’inventaire des parcours.
* **Éditeur d’expression avancé dans la configuration des événements** est désormais GA : vous pouvez désormais utiliser l’éditeur d’expression avancé lors de la configuration d’un événement, ce qui vous permet de définir des expressions plus complexes ou d’utiliser des fonctions dans la condition d’identifiant d’événement. Cette fonctionnalité est disponible en disponibilité limitée pour certains clients. <!--[Read more](../event/about-creating.md)-->
* **Stratégies de fusion** sont désormais GA : les stratégies de fusion utilisées par un Parcours sont désormais visibles et cohérentes dans tout le parcours. Cette fonctionnalité est disponible en disponibilité limitée pour certains clients. <!--[Read more](../building-journeys/journey-gs.md#merge-policies)-->



**Campagnes**

* Lors de la création d’une campagne dans Adobe Journey Optimizer, vous pouvez désormais choisir le type de campagne (planifiée ou déclenchée) dans un nouveau modal.

<!--**Email channel**

* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)-->


**Canal SMS**

* Vous pouvez désormais ajouter des codes courts uniques pour chaque environnement de test avec une seule configuration d’API, ce qui rend le processus plus efficace et plus simple.
  <!--* You can now modify existing SMS configurations.-->

**Canal in-app**

* **Fragment d’expression** - Les fragments d’expression sont désormais disponibles pour le **Canal in-app**. <!--[Read more](../personalization/use-expression-fragments.md)-->


* Vous pouvez désormais utiliser le module externe Edge Delivery pour obtenir les informations nécessaires pour comprendre et résoudre les problèmes liés à vos implémentations entrantes.



## Notes de mise à jour de mai 2024 {#may-2024}

**Date de publication** : 21-22 mai 2024

### Nouvelles fonctionnalités {#e-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Décisions pour les expériences  - Disponibilité limitée</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Décisions pour les expériences simplifie la personnalisation en offrant un catalogue centralisé d’offres marketing connues sous le nom d’« éléments de décision » et un moteur de décision sophistiqué. Ce moteur tire parti des règles et des critères de classement pour sélectionner et présenter les éléments de décision les plus pertinents à chaque individu.</p>
<p>Ces éléments de décision sont intégrés de manière transparente à un large éventail de surfaces entrantes grâce au nouveau canal d’expérience basé sur le code, désormais accessible dans les campagnes Journey Optimizer. Les politiques de décisions pour les expériences ne peuvent être utilisées que dans des campagnes d’expérience basées sur du code.</p>
<p>Ces décisions pour les expériences ne sont actuellement disponibles que pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/gs-experience-decisioning.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Personnalisation de la surface des e-mails - Disponibilité limitée</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais définir des sous-domaines dynamiques et des paramètres d’en-tête personnalisés lors de la création de surfaces de canal e-mail pour une meilleure flexibilité et un meilleur contrôle de vos paramètres d’e-mail.</p>
<p>La personnalisation de la surface des e-mails n’est actuellement disponible que pour un ensemble donné d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Pour plus d’informations, consultez la <a href="../email/surface-personalization.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>If you are sending email on a brand new IP address, you can now easily perform IP warmup workflows directly from the user interface. Adobe Journey Optimizer offers a standardized and efficient way to warm up your IP adresses that follows the best practices for optimal deliverability.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Business rules - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create granular frequency capping rules, and apply them to different types of marketing communications through rule sets. This new capability lets you control how often your audiences receive a message by setting cross-channel rules, that automatically exclude over-solicited profiles from messages and actions.</p>
<p>Business rules capability is currently available as a beta. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p>
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

**Décisions pour les expériences** (Disponibilité limitée)

De la version bêta à cette version, les améliorations suivantes ont été ajoutées :

* **Décisions pour les expériences + expériences basées sur le code** : vous pouvez désormais tirer profit de la fonctionnalité de prise de décision basée sur l’expérience pour utiliser des éléments de décision dans vos campagnes basées sur du code. Note : le canal Expérience basée sur le code et les décisions pour les expériences ne sont pas disponibles pour les organisations qui ont acheté les offres complémentaires Healthcare Shield et Privacy and Security Shield d’Adobe. [En savoir plus](../code-based/get-started-code-based.md)
* **Données contextuelles** : vous pouvez désormais exploiter les données contextuelles d’Adobe Experience Platform dans vos règles de décision et formules de classement. [En savoir plus](../experience-decisioning/context-data.md)
* **Nouvelle autorisation** : une nouvelle autorisation « Gérer les décisions basées sur l’expérience » est désormais disponible pour la ressource Gestion des décisions. Elle vous permet de gérer les droits liés aux décisions pour les expériences. [En savoir plus](../experience-decisioning/gs-experience-decisioning.md)
* **Règles de limitation** : vous pouvez désormais ajouter plusieurs règles de limitation pour un élément de décision donné dans les décisions pour les expériences. Cela vous permet d’augmenter le niveau de contrôle sur la manière dont les offres sont envoyées. [En savoir plus](../experience-decisioning/items.md#capping)
* **Rapports** : vous pouvez désormais créer des tableaux de bord de rapports personnalisés pour les campagnes de décisions pour les expériences à l’aide de [!DNL Customer Journey Analytics]. [En savoir plus](../experience-decisioning/cja-reporting.md)


<!--**Decision Management**

* **Multi-rule support** - You can now add up to 10 capping rules for a given offer in Decision Management. This allows you to increase the level of control over the way offers are sent.
* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->


**Canal e-mail**

<!--
* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)
-->

* **Notation de spam** (version bêta) : vous pouvez désormais vérifier la notation de spam de votre contenu dans un rapport de spam dédié. Grâce à SpamAssassin, Adobe Journey Optimizer peut désormais tester le contenu de vos e-mails et lui attribuer un score pour indiquer si les FAI ou les fournisseurs de messagerie le considèrent comme un spam ou non. [En savoir plus](../content-management/spam-report.md)

  >[!AVAILABILITY]
  >
  >Cette fonctionnalité est actuellement en version bêta et disponible uniquement pour les clientes et clients bêta. Pour rejoindre le programme bêta, contactez votre représentant ou représentante Adobe.

<!--
**Audiences**

* The use of audiences and attributes from audience composition and custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.-->

<!--**Personalization**

* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

**Parcours**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **Prise en charge de mTLS** : l’authentification mTLS est désormais prise en charge dans les actions personnalisées. Aucune configuration supplémentaire n’est requise dans l’action ou le parcours personnalisé pour activer mTLS. L’activation se produit automatiquement lorsqu’un point d’entrée compatible mTLS est détecté. [En savoir plus](../action/about-custom-action-configuration.md#mtls-protocol-support)
* **Tables de recherche dans les événements** :vous pouvez désormais exploiter les données d’un jeu de données de recherche lorsqu’une relation a été définie à l’aide d’un attribut dans un tableau d’objets. Les valeurs de recherche seront disponibles dans les parcours (conditions, actions personnalisées, etc.) et dans la personnalisation des messages. [En savoir plus](../event/experience-event-schema.md#relationships_limitations)
* **Éditeur d’expression avancé dans la configuration des événements** (LA) : vous pouvez désormais utiliser l’éditeur d’expression avancé lors de la configuration d’un événement, ce qui vous permet de définir des expressions plus complexes ou d’utiliser des fonctions dans la condition d’identifiant d’événement. Cette fonctionnalité est publiée en disponibilité limitée pour certaines clientes et certains clients uniquement. [En savoir plus](../event/about-creating.md)
* **Politiques de fusion** (LA) : les politiques de fusion utilisées par un parcours sont désormais visibles et cohérentes dans l’ensemble du parcours. Cette fonctionnalité est publiée en disponibilité limitée pour certaines clientes et certains clients uniquement. [En savoir plus](../building-journeys/journey-gs.md#merge-policies)

**Mondialisation**

Dans le cadre de nos efforts continus pour offrir une expérience utilisateur et utilisatrice unifiée, nous harmonisons la terminologie utilisée dans les produits et applications Adobe Experience Cloud. Cela concerne le terme allemand « Titel » qui est remplacé par « Label » lorsqu’il se rapporte au nom d’un objet. Les modifications seront progressivement déployées dans l’interface utilisateur et dans la documentation.



