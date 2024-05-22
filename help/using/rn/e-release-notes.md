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
source-git-commit: ae9a315f6c9d2c2408788a7e4b32cdbd516f41d6
workflow-type: tm+mt
source-wordcount: '656'
ht-degree: 40%

---

# Notes de mise à jour anticipées {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées à la fin de chaque mois dans les [notes de mise à jour](release-notes.md).

**Les notes de mise à jour anticipées ci-dessous peuvent être modifiées sans préavis jusqu’à la date de publication.**. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les [notes de mise à jour](release-notes.md), à la date de publication.

## Notes de mise à jour initiales de mai 2024 {#e-2024}

**Date de publication**: 21-22 mai 2024

### Nouvelles fonctionnalités {#e-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous.


<table>
<thead>
<tr>
<th><strong>Prise de décision basée sur l’expérience - Disponibilité limitée</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Experience Decisioning simplifie la personnalisation en offrant un catalogue centralisé d’offres marketing connues sous le nom d’« éléments de décision » et un moteur de décision sophistiqué. Ce moteur tire parti des règles et des critères de classement pour sélectionner et présenter les éléments de décision les plus pertinents à chaque individu.</p>
<p>Ces éléments de décision sont intégrés de manière transparente à un large éventail de surfaces entrantes grâce au nouveau canal d’expérience basé sur le code, désormais accessible dans les campagnes Journey Optimizer. Les politiques de décision de prise de décision basée sur l’expérience ne peuvent être utilisées que dans des campagnes d’expérience basées sur du code.</p>
<p>Cette prise de décision basée sur l’expérience n’est actuellement disponible que pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/gs-experience-decisioning.md">documentation détaillée</a>.</p>
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

**Experience Decisioning** (Disponibilité limitée)

Les améliorations suivantes ont été ajoutées depuis la version bêta vers cette version :

* **Experience Decisioning + expériences basées sur le code** - Vous pouvez désormais tirer parti de la fonction de prise de décision d’expérience pour utiliser des éléments de décision dans vos campagnes basées sur du code. Note : le canal Expérience basée sur le code et la prise de décision basée sur l’expérience ne sont pas disponibles pour les organisations qui ont acheté les offres complémentaires Healthcare Shield et Privacy and Security Shield d’Adobe. [En savoir plus](../code-based/get-started-code-based.md)
* **Données contextuelles** - Vous pouvez désormais exploiter les données contextuelles de Adobe Experience Platform dans vos règles de décision et vos formules de classement. [En savoir plus](../experience-decisioning/context-data.md)
* **Nouvelle autorisation** - Une nouvelle autorisation &quot;Gérer les décisions d’expérience&quot; est désormais disponible pour la ressource Gestion des décisions. Elle vous permet de gérer les droits liés à la prise de décision basée sur l’expérience. [En savoir plus](../experience-decisioning/gs-experience-decisioning.md)
* **Règles de limitation** - Vous pouvez désormais ajouter plusieurs règles de limitation pour un élément de décision donné dans Experience Decisioning. Cela vous permet d’augmenter le niveau de contrôle sur la manière dont les offres sont envoyées. [En savoir plus](../experience-decisioning/items.md#capping)
* **Reporting** - Vous pouvez désormais créer des tableaux de bord de rapports personnalisés pour les campagnes Experience Decisioning à l’aide de [!DNL Customer Journey Analytics]. [En savoir plus](../experience-decisioning/cja-reporting.md)


<!--**Decision Management**

* **Multi-rule support** - You can now add up to 10 capping rules for a given offer in Decision Management. This allows you to increase the level of control over the way offers are sent.
* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->


**Canal e-mail**

<!--
* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)
-->

* **Scoring des messages indésirables** (Version bêta) - Vous pouvez désormais vérifier le score de spam de votre contenu dans un rapport de spam dédié. Grâce à SpamAssassin, Adobe Journey Optimizer peut désormais tester le contenu de vos emails et lui attribuer un score pour indiquer si les FAI ou les fournisseurs de messagerie le considèrent comme un spam ou non. [En savoir plus](../content-management/spam-report.md)

  >[!AVAILABILITY]
  >
  >Cette fonctionnalité est actuellement en version bêta et disponible uniquement pour les clients bêta. Pour rejoindre le programme Beta, contactez l’assistance clientèle d’Adobe.

<!--
**Audiences**

* The use of audiences and attributes from audience composition and custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.-->

<!--**Personalization**

* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

**Parcours**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **Prise en charge de mTLS** - L’authentification mTLS est désormais prise en charge dans les actions personnalisées. Aucune configuration supplémentaire n’est requise dans l’action ou le parcours personnalisé pour activer mTLS ; elle se produit automatiquement lorsqu’un point d’entrée compatible mTLS est détecté. [En savoir plus](../action/about-custom-action-configuration.md#mtls-protocol-support)
* **Tables de recherche dans les événements** - Vous pouvez désormais exploiter les données d’un jeu de données de recherche lorsqu’une relation a été définie à l’aide d’un attribut dans un tableau d’objets. Les valeurs de recherche seront disponibles en parcours (conditions, actions personnalisées, etc.) et personnalisation des messages. [En savoir plus](../event/experience-event-schema.md#relationships_limitations)
* **Éditeur d’expression avancé dans la configuration des événements** (LA) - Vous pouvez désormais utiliser l’éditeur d’expression avancé lors de la configuration d’un événement, ce qui vous permet de définir des expressions plus complexes ou d’utiliser des fonctions dans la condition d’identifiant d’événement. Cette fonctionnalité est disponible en disponibilité limitée pour certains clients. [En savoir plus](../event/about-creating.md)
* **Stratégies de fusion** (LA) - Les stratégies de fusion utilisées par un Parcours sont désormais visibles et cohérentes dans tout le parcours. Cette fonctionnalité est disponible en disponibilité limitée pour certains clients. [En savoir plus](../building-journeys/journey-gs.md#merge-policies)

**Mondialisation**

Dans le cadre de nos efforts continus pour offrir une expérience utilisateur unifiée, nous harmonisons la terminologie utilisée dans les produits et applications Adobe Experience Cloud. Cela affecte le terme allemand &quot;Titre&quot; qui est remplacé par &quot;Libellé&quot; lorsqu’il se rapporte au nom d’un objet. Les modifications seront progressivement déployées dans l’interface utilisateur et dans la documentation.



