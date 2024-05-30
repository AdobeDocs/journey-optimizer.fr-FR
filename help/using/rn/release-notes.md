---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
topic: Content Management
description: Notes de mise à jour de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 40e4aaa93400daf52c96aa5ac2de17151cdbb07f
workflow-type: tm+mt
source-wordcount: '768'
ht-degree: 93%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour.

[!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous à la [newsletter trimestrielle d’Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} dès aujourd’hui, et recevez les dernières mises à jour produits, les articles les plus intéressants, des cas pratiques, des conseils et bien plus encore, directement dans votre boîte de réception, tous les trimestres.


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
<th><strong>Personnalisation de la surface des emails - Disponibilité limitée</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais définir des sous-domaines dynamiques et des paramètres d’en-tête personnalisés lors de la création de surfaces de canal de courrier électronique pour une flexibilité accrue et un contrôle accru de vos paramètres de courrier électronique.</p>
<p>La personnalisation de la surface des emails n’est actuellement disponible que pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
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
  >Cette fonctionnalité est actuellement en version bêta et disponible uniquement pour les clientes et clients bêta. Pour rejoindre le programme bêta, contactez votre représentant Adobe.

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



