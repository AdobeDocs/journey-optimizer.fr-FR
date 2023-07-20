---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
description: Notes de mise à jour de Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: b677776becaabc15c85be0a5a46b741cebb9d87b
workflow-type: tm+mt
source-wordcount: '626'
ht-degree: 23%

---

# Notes de mise à jour anticipées {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans la variable [notes de mise à jour](release-notes.md).

Les notes de mise à jour anticipées ci-dessous peuvent être modifiées sans préavis jusqu’à la date de disponibilité de la version. Les liens, les écrans et la documentation mise à jour sont publiés dans la section [notes de mise à jour](release-notes.md), à la date de publication.


## Notes de mise à jour initiales de juillet 2023 {#july-rn-2023}

**Date de publication**: 26-27 juillet

### Nouvelles fonctionnalités{#july-2023-features}

Cette version apporte les nouvelles fonctionnalités répertoriées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Composition de l’audience</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer des workflows de composition afin de combiner les audiences Adobe Experience Platform existantes dans un canevas visuel et d’exploiter diverses activités (fractionner, enrichir...) pour créer de nouvelles audiences. Les audiences nouvellement créées sont réenregistrées dans Adobe Experience Platform avec les audiences existantes et peuvent être exploitées dans les campagnes Journey Optimizer pour cibler les clients.</p>
<img src="../audience/assets/audiences-publish.png"/>
<p>Pour plus d’informations, consultez la <a href="../audience/get-started-audience-orchestration.md">documentation détaillée</a>.</p>
<p>La composition de l’audience est entièrement intégrée au nouveau menu "Audiences" de Adobe Experience Platform qui sert de portail centralisé vers les audiences. Vous pouvez désormais utiliser une page de navigation qui comprend un nouveau tableau de bord avec des tendances et des chevauchements de segments afin de trouver de nouvelles informations et d’explorer les outils de l’organisation pour le suivi et le balisage. Cette expérience s’accompagne de contrôles de gouvernance pour l’étiquetage normalisé des audiences ainsi que de fonctionnalités de gestion du cycle de vie des audiences afin de gérer les workflows d’activation. Grâce à cette nouvelle expérience de gestion, vous pouvez désormais gérer facilement et en toute sécurité les audiences à partir d’un seul emplacement. Pour plus d’informations, reportez-vous à la section <a href="https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=fr" target="_blank">Documentation Adobe Experience Platform</a>.</p></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Canal courrier</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais ajouter des messages postaux dans vos campagnes et parcours. Le canal Courrier est un canal off-line qui vous permet de personnaliser et de générer les fichiers requis par les opérateurs de services postaux pour envoyer du courrier à vos clients.</p>
<p>Lors de la préparation d'une diffusion courrier, Journey Optimizer génère un fichier comprenant tous les profils ciblés et les coordonnées de contact sélectionnées (adresse postale, par exemple). Vous pourrez alors envoyer ce fichier à votre opérateur de services postaux qui prendra en charge l'envoi réel.</p>
<img src="../direct-mail/assets/direct-mail-properties.png">
<p>Pour plus d’informations, consultez la <a href="../direct-mail/create-direct-mail.md">documentation détaillée</a>.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Convertir le contenu de votre HTML pour le Concepteur d'email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais importer et convertir n’importe quel contenu de HTML dans l’éditeur d’email de Journey Optimizer. Les blocs de contenu sont automatiquement identifiés et disponibles dans le Concepteur d'email : utilisez ses puissantes fonctionnalités de conception pour la mettre à jour et la personnaliser !</p>
<img src="../email/assets/html-imported_2.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Utilisation des balises dans Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais attribuer des balises Adobe Experience Platform unifiées à vos landing pages, modèles, fragments de contenu et listes d’abonnements, en plus des campagnes et des parcours. Vous pouvez ainsi facilement les classer et améliorer la recherche et la navigation dans toutes les listes. Cette fonctionnalité est actuellement disponible en version GA (Général disponible).</p>
<img src="assets/do-not-localize/campaigns-tag.gif"/>
<p>Pour plus d’informations, consultez la <a href="../start/search-filter-categorize.md#tags">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


### Améliorations {#july-2023-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Audiences**

Des améliorations ont été apportées au sélecteur d’audiences dans les parcours ou les campagnes, avec l’ajout de nouvelles colonnes indiquant l’origine et la fréquence de mise à jour des audiences.

Avec la publication du portail de composition de l’audience, Adobe Experience Platform et Adobe Journey Optimizer ont mis à jour l’utilisation des &quot;audiences&quot; et des &quot;segments&quot; dans le système et la documentation.

* Audience : ensemble de personnes, de comptes, de foyers ou d’autres entités qui partagent des caractéristiques et des comportements communs.
* Définition d’un segment : règles utilisées pour décrire les caractéristiques ou le comportement clés d’une audience cible dans Adobe Experience Platform. Ce terme était auparavant appelé « segment ».

Par conséquent, dans Adobe Journey Optimizer et l’interface utilisateur d&#39;Adobe Experience Platform, « Segments » est remplacé par « Audiences » pour refléter ce nouveau chemin de création et de gestion d’audience.


**Parcours**

* Vous pouvez désormais utiliser les réponses d’appel API dans des actions personnalisées et orchestrer votre parcours en fonction de ces réponses.


**Campagnes**

* Les événements contextuels liés aux campagnes sont désormais disponibles dans le menu &quot;Attributs contextuels&quot; de l’éditeur de personnalisation.

