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
source-git-commit: 628d49ee45ce161fc5e213bda60cb44d41223369
workflow-type: tm+mt
source-wordcount: '844'
ht-degree: 26%

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
<p>Vous pouvez désormais créer des règles de limitation de fréquence granulaires et les appliquer à différents types de communications marketing par le biais d’ensembles de règles. Grâce à cette nouvelle fonctionnalité, vous pouvez contrôler la fréquence à laquelle vos audiences reçoivent un message en définissant des règles cross-canal, qui excluent automatiquement les profils sur-sollicités des messages et actions.</p>
<p>La fonctionnalité de règles de fonctionnement est actuellement disponible en version bêta publique.</p>
<p>Pour plus d’informations, consultez la <a href="../configuration/business-rules.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Données de personnalisation étendues - Version bêta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais rechercher et récupérer des valeurs de données dans des jeux de données Adobe Experience Platform et utiliser ces valeurs pour créer des conditions dans Adobe Journey Optimizer. Vous pouvez exploiter les données d’un jeu de données de recherche lorsqu’une relation a été définie à l’aide d’un attribut dans un tableau d’objets. Vous pouvez spécifier des jeux de données non activés pour le profil pour la recherche. Une fois activé, vous pouvez utiliser un attribut de profil comme clé de jointure au jeu de données spécifié pour récupérer d’autres données à des fins de personnalisation.</p>
<p>Cette fonctionnalité est actuellement disponible en version bêta publique.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#e-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Experience Decisioning**

Les améliorations suivantes ont été ajoutées depuis la version bêta vers cette version :

* **Prise de décision d’expérience + expériences basées sur le code (LA)** - Vous pouvez désormais tirer parti de la fonction de prise de décision d’expérience pour utiliser des éléments de décision dans vos campagnes basées sur du code. Remarque : Le canal d’expérience basé sur le code et la prise de décision sur l’expérience ne sont pas disponibles pour les organisations qui ont acheté les offres complémentaires Adobe Healthcare Shield et Privacy and Security Shield. [En savoir plus](../code-based/get-started-code-based.md)
* **Données contextuelles** - Vous pouvez désormais exploiter les données contextuelles de Adobe Experience Platform dans vos règles de décision et vos formules de classement. [En savoir plus](../experience-decisioning/context-data.md)
* **Nouvelle autorisation** - Une nouvelle autorisation &quot;Gérer les décisions d’expérience&quot; est désormais disponible pour la ressource Gestion des décisions. Il vous permet de gérer les droits liés à Experience Decisioning. [En savoir plus](../experience-decisioning/gs-experience-decisioning.md)
* **Règles de limitation** - Vous pouvez désormais ajouter plusieurs règles de limitation pour un élément de décision donné dans Experience Decisioning. Cela vous permet d’augmenter le niveau de contrôle sur la manière dont les offres sont envoyées. [En savoir plus](../experience-decisioning/items.md#capping)
* **Reporting** - Vous pouvez désormais créer des tableaux de bord de rapports personnalisés pour les campagnes Experience Decisioning à l’aide de [!DNL Customer Journey Analytics]. [En savoir plus](../experience-decisioning/cja-reporting.md).


**Gestion des décisions**

* **Prise en charge multi-règles** - Vous pouvez désormais ajouter jusqu’à 10 règles de limitation pour une offre donnée dans la gestion des décisions. Cela vous permet d’augmenter le niveau de contrôle sur la manière dont les offres sont envoyées.
* **Audits** - La variable **Journal des modifications** pour afficher toutes les modifications apportées à une offre ou à une décision qui a été supprimée. Les modifications liées aux offres et aux décisions sont désormais visibles dans le menu **Audits**.


**Canal e-mail**

* **List-unsubscribe** - Suite aux récentes annonces Gmail et Yahoo pour les expéditeurs en masse, Journey Optimizer prend en charge l’option &quot;post/1-click&quot; List-Unsubscribe.
* **Scoring des messages indésirables** (Version bêta) - Vous pouvez désormais vérifier le score de spam de votre contenu dans un rapport de spam dédié. Grâce à SpamAssassin, Adobe Journey Optimizer peut désormais tester le contenu de vos emails et lui attribuer un score pour indiquer si les fournisseurs de FAI le considéreront comme un spam ou non. [En savoir plus](../content-management/spam-report.md)


**Audiences**

* L’utilisation d’audiences et d’attributs provenant de la composition de l’audience et du téléchargement personnalisé (fichier CSV) est désormais disponible avec Healthcare Shield ou Privacy and Security Shield.

**Personnalisation**

* **Fragment d’expression** - Les fragments d’expression sont désormais disponibles pour le **Canal in-app**. [En savoir plus](../personalization/use-expression-fragments.md)

**Parcours**

* **Stratégies de fusion** (Disponibilité limitée) : les stratégies de fusion utilisées par un parcours sont désormais visibles et cohérentes dans tout le parcours.
* **Prise en charge de mTLS** - Le protocole mTLS est désormais pris en charge dans les API Journey Optimizer et les actions personnalisées.
* **Tables de recherche dans les événements** - Vous pouvez désormais exploiter les données d’un jeu de données de recherche lorsqu’une relation a été définie à l’aide d’un attribut dans un tableau d’objets. Les valeurs de recherche seront disponibles en parcours (conditions, actions personnalisées, etc.) ni dans la personnalisation des messages.
