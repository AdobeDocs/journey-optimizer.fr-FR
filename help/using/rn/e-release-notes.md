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
source-git-commit: 8dacf28f4c3217a57e648b3c80e1724d9794c9ea
workflow-type: tm+mt
source-wordcount: '699'
ht-degree: 35%

---

# Notes de mise à jour anticipées {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées à la fin de chaque mois dans les [notes de mise à jour](release-notes.md).

Les notes de mise à jour ci-dessous peuvent être modifiées sans avertissement préalable jusqu’à la date de disponibilité de la version. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les [notes de mise à jour](release-notes.md), à la date de publication.

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
<p>Ces éléments de décision sont intégrés de manière transparente à un large éventail de surfaces entrantes grâce au nouveau canal d’expérience basé sur le code, désormais accessible dans les campagnes Journey Optimizer. Les stratégies de décision de prise de décision d’expérience ne peuvent être utilisées que dans des campagnes d’expérience basées sur du code.</p>
<p>Cette prise de décision basée sur l’expérience n’est actuellement disponible que pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/gs-experience-decisioning.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


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
<p>Pour plus d’informations, consultez la <a href="../configuration/ip-warmup-gs.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Règles de fonctionnement - Version bêta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer des règles de limitation de fréquence granulaires et les appliquer à différents types de communications marketing par le biais d’ensembles de règles. </p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Prise en charge de plusieurs entités pour la recherche locale - Version bêta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>À déterminer</p>
</td>
</tr>
</tbody>
</table>


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

**Experience Decisioning**

De la version bêta à la version LA, les améliorations suivantes ont été ajoutées :

* **Prise de décision d’expérience + expériences basées sur le code (LA)**: vous pouvez désormais utiliser la fonction de prise de décision d’expérience pour utiliser des éléments de décision dans vos campagnes basées sur du code. Remarque : Le canal d’expérience basé sur le code et la prise de décision sur l’expérience ne sont pas disponibles pour les organisations qui ont acheté les offres complémentaires Adobe Healthcare Shield et Privacy and Security Shield. [En savoir plus](../code-based/get-started-code-based.md)
* Vous pouvez désormais exploiter les données contextuelles de Adobe Experience Platform dans vos règles de décision et vos formules de classement. [En savoir plus](../experience-decisioning/context-data.md)
* Une nouvelle autorisation « Gérer les décisions basées sur l’expérience » est désormais disponible pour la ressource Gestion des décisions. Il vous permet de gérer les droits liés à Experience Decisioning. [En savoir plus](../experience-decisioning/gs-experience-decisioning.md)
* Vous pouvez désormais ajouter plusieurs règles de limitation pour un élément de décision donné dans la prise de décision basée sur l’expérience. Cela vous permet d’augmenter le niveau de contrôle sur la manière dont les offres sont envoyées. [En savoir plus](../experience-decisioning/items.md#capping)
* Vous pouvez désormais créer des tableaux de bord de rapports personnalisés pour les campagnes Experience Decisioning à l’aide de [!DNL Customer Journey Analytics]. [En savoir plus](../experience-decisioning/cja-reporting.md)


**Offer Decisioning**

* **Prise en charge multi-règles** - Vous pouvez désormais ajouter jusqu’à 10 règles de limitation pour une offre donnée dans la gestion des décisions. Cela vous permet d’augmenter le niveau de contrôle sur la manière dont les offres sont envoyées.
* **Audits** - La variable **Journal des modifications** pour afficher toutes les modifications apportées à une offre ou à une décision qui a été supprimée. Les modifications liées aux offres et aux décisions sont désormais visibles dans le menu **Audits**.


**Canal e-mail**

* **List-unsubscribe** - Suite aux récentes annonces Gmail et Yahoo pour les expéditeurs en masse, Journey Optimizer prend en charge l’option &quot;post/1-click&quot; List-Unsubscribe.
* **Scoring des messages indésirables** - Vous pouvez désormais vérifier le score de spam de votre contenu dans un rapport de spam dédié. Grâce à SpamAssassin, Adobe Journey Optimizer peut désormais tester le contenu de vos emails et lui attribuer un score pour indiquer si les fournisseurs de FAI le considéreront comme un spam ou non. [En savoir plus](../content-management/spam-report.md)


**Audiences**

* L’utilisation d’audiences et d’attributs provenant de la composition de l’audience et du téléchargement personnalisé (fichier CSV) est désormais disponible avec Healthcare Shield ou Privacy and Security Shield.

**Personnalisation**

* **Table de recherche** - Vous pouvez désormais exploiter les données d’un jeu de données de recherche lorsqu’une relation a été définie à l’aide d’un attribut dans un tableau d’objets. Les valeurs de recherche seront disponibles en parcours (conditions, actions personnalisées, etc.) ni dans la personnalisation des messages.
* **Fragment d’expression** - Les fragments d’expression sont désormais disponibles pour le canal In-App.

**Parcours**

* **Stratégies de fusion** - Les stratégies de fusion peuvent désormais être configurées et utilisées dans vos parcours.
* **Prise en charge de mTLS** - Le protocole mTLS est désormais pris en charge dans les API Journey Optimizer et les actions personnalisées.
