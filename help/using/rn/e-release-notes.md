---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
description: Notes de mise à jour de Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: c75664f9b4d58fff1b073c385bcb839e9c11c8ec
workflow-type: tm+mt
source-wordcount: '740'
ht-degree: 18%

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
<th><strong>API de modèles de contenu</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer et gérer des modèles de contenu Adobe Journey Optimizer à l’aide d’API dédiées, ce qui vous permet d’intégrer facilement votre système de contenu existant.</p>
<!--<p>For more information, refer to the <a href="../start/search-filter-categorize.md#tags">detailed documentation</a>.</p>-->
</td>
</tr>
</tbody>
</table>


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
<p>Vous pouvez désormais ajouter des messages de courrier dans vos campagnes. Le canal Courrier est un canal off-line qui vous permet de personnaliser et de générer les fichiers requis par les opérateurs de services postaux pour envoyer du courrier à vos clients.</p>
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
<p>Outre les campagnes et les parcours, vous pouvez désormais attribuer des balises unifiées Adobe Experience Platform à vos landing pages, modèles de contenu, fragments et listes d’abonnements. Vous pouvez ainsi facilement les classer et améliorer la recherche et la navigation dans toutes les listes. </p>
<img src="assets/do-not-localize/campaigns-tag.gif"/>
<p>Pour plus d’informations, consultez la <a href="../start/search-filter-categorize.md#tags">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


### Améliorations {#july-2023-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Parcours**

<!--* You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.-->
* Introduction d’un nouveau type d’alerte système. Vous pouvez désormais être averti en cas d’échec d’une action personnalisée.


**Campagnes**

* Les événements contextuels liés aux campagnes sont désormais disponibles dans le menu &quot;Attributs contextuels&quot; de l’éditeur de personnalisation.


**Audiences**

Des améliorations ont été apportées au sélecteur d’audiences dans les parcours ou les campagnes, avec l’ajout de nouvelles colonnes indiquant l’origine et la fréquence de mise à jour des audiences.

Avec la publication du portail de composition de l’audience, Adobe Experience Platform et Adobe Journey Optimizer ont mis à jour l’utilisation des &quot;audiences&quot; et des &quot;segments&quot; dans le système et la documentation.

* Audience : ensemble de personnes, de comptes, de foyers ou d’autres entités qui partagent des caractéristiques et des comportements communs.
* Définition d’un segment : règles utilisées pour décrire les caractéristiques ou le comportement clés d’une audience cible dans Adobe Experience Platform. Ce terme était auparavant appelé « segment ».

Par conséquent, dans Adobe Journey Optimizer et l’interface utilisateur d&#39;Adobe Experience Platform, « Segments » est remplacé par « Audiences » pour refléter ce nouveau chemin de création et de gestion d’audience.

**API**

Authentification des API Adobe Journey Optimizer : la méthode JWT pour générer des jetons d’accès a été abandonnée. Toutes les nouvelles intégrations doivent être créées à l’aide de la méthode d’authentification OAuth serveur à serveur. Adobe vous recommande également de migrer vos intégrations existantes vers la méthode OAuth. [En savoir plus](https://developer.adobe.com/journey-optimizer-apis/references/authentication/).


**Autres modifications**

Les jeux de données Journey Optimizer exportés vers les destinations de stockage dans le cloud sont désormais disponibles pour tous les clients. Cette fonctionnalité vous permet d’établir une connexion en direct avec les emplacements de stockage dans le cloud afin d’exporter le contenu de vos jeux de données. [En savoir plus](../data/export-datasets.md).

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version bêta et peut être modifiée.</p>