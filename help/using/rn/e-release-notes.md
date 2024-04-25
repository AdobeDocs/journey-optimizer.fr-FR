---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
description: Notes de mise à jour anticipées de Journey Optimizer
feature: Release Notes
topic: Content Management
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
hide: true
hidefromtoc: true
source-git-commit: 882af161383a54a1f9b09d2a8d0cab84abbf7dcd
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 44%

---

# Notes de mise à jour anticipées {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées à la fin de chaque mois dans les [notes de mise à jour](release-notes.md).

Les notes de mise à jour ci-dessous peuvent être modifiées sans avertissement préalable jusqu’à la date de disponibilité de la version. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les [notes de mise à jour](release-notes.md), à la date de publication.

## Notes de mise à jour d’avril 2024 (nouveau) {#e-2024}

**Date de publication** : mercredi 30 avril 2024

### Nouvelle fonctionnalité {#e-features}

Cette version apporte les nouvelles fonctionnalités présentées ci-dessous.

<!--table>
<thead>
<tr>
<th><strong>Business rules - Private Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>It is now possible to create and apply rule sets to your marketing communications.  </p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Prise de décision d’expérience - Disponibilité limitée</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Experience Decisioning simplifie la personnalisation en offrant un catalogue centralisé d’offres marketing connues sous le nom d’« éléments de décision » et un moteur de décision sophistiqué. Ce moteur tire parti des règles et des critères de classement pour sélectionner et présenter les éléments de décision les plus pertinents à chaque individu.</p>
<p>Ces éléments de décision sont intégrés de manière transparente à un large éventail de surfaces entrantes grâce au nouveau canal d’expérience basé sur le code, désormais accessible dans les campagnes Journey Optimizer. Les stratégies de décision de prise de décision d’expérience ne peuvent être utilisées que dans des campagnes d’expérience basées sur du code.</p>
<p>Actuellement, la prise de décision d’expérience n’est disponible que pour un ensemble d’organisations (disponibilité limitée). Pour y accéder, contactez votre représentant Adobe.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Personalization - Local Lookups - Multi-Entity Support - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>TBD</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>MMS (Multimedia Message Service) avec Infobip</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Avec le canal SMS, vous pouvez maintenant améliorer votre communication en envoyant des MMS, ce qui permet le partage d’images, de GIF ou de vidéos avec vos clientes et clients. Cette fonctionnalité, auparavant uniquement disponible avec Sinch, est désormais également disponible avec Infobip.</p>
<img src="assets/do-not-localize/mms.gif"/>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>AI Assistant - Experience Variant Generation - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with the AI assistant. You can now use the AI assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow - LA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now easily perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Email Surface Personalization - Private beta </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define dynamic subdomains and personalized header parameters when creating email channel surfaces, for increased flexibility and control over your email settings.</p>
</td>
</tr>
</tbody>
</table-->

### Améliorations {#e-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

<!--
* **Experience Decisioning + Code-based experiences (LA)**: You can now leverage the Experience decisioning feature to use decision items in your code-based campaigns. Note: The Code-based experience channel and Experience decisioning are not available for organizations that have purchased the Adobe Healthcare Shield and Privacy and Security Shield add-on offerings.
-->
<!--
* **Expression Fragments supported for Web and In-App**: Expression fragments are now available for the Web and In-app channels. 
-->


<!--
* **DULE for AJO Channel Surface**: It is now possible to apply a label on certain profile attributes to restrict their usage inside a channel surface through marketing actions.
-->


<!--
* **List-Unsubscribe updates**: Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. 
-->

**Gestion des décisions**

* La variable **Journal des modifications** pour afficher toutes les modifications apportées à une offre ou à une décision qui a été supprimée. Les modifications liées aux offres et aux décisions sont désormais visibles dans la variable **Audits** .

**Prise de décision d’expérience**

De la version bêta à la version LA, les améliorations suivantes ont été ajoutées :

* Vous pouvez désormais exploiter les données contextuelles de Adobe Experience Platform dans vos règles de décision à l’aide de la variable **Données contextuelles** .
* Une nouvelle autorisation &quot;Gérer les décisions d’expérience&quot; est désormais disponible pour la ressource Gestion des décisions. Il vous permet de gérer les droits liés à Experience Decisioning.
* Vous pouvez désormais ajouter plusieurs règles de limitation pour une seule offre. Cela vous permet d’augmenter le niveau de contrôle sur la manière dont les offres sont envoyées.
* Vous pouvez désormais ajouter plusieurs règles de limitation pour un élément de décision donné dans Experience Decisioning. Cela vous permet d’augmenter le niveau de contrôle sur la manière dont les offres sont envoyées.
* Vous pouvez désormais créer des tableaux de bord de rapports personnalisés pour les campagnes Experience Decisioning à l’aide de [!DNL Customer Journey Analytics].

**Parcours**

* **Amélioration du concepteur de Parcours**

   * L’interface utilisateur de la zone de travail améliorée offre une expérience utilisateur plus intuitive et efficace.
   * Les activités sont plus claires et présentent plus d’informations sur le canevas de parcours avec moins de clics.

* **Nouveaux rapports en direct**: les rapports parcours des dernières 24 heures sont désormais accessibles directement dans la zone de travail du Parcours.

**Configuration**

* Vous pouvez désormais sélectionner une action marketing au niveau de la surface de canal. Lorsqu’elles sont utilisées en surface, toutes les stratégies de consentement associées à cette action marketing sont utilisées afin de respecter les préférences de vos clientes et clients.
* L’utilisation du contrôle d’accès au niveau de l’objet est désormais disponible pour les surfaces de canal.

