---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
description: Notes de mise à jour anticipées de Journey Optimizer
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 100%

---

# Notes de mise à jour anticipées {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans les [notes de mise à jour](release-notes.md).

Les notes de mise à jour ci-dessous peuvent être modifiées sans avertissement préalable jusqu’à la date de disponibilité de la version. Les liens, les écrans et la documentation mise à jour sont publiés dans les [notes de mise à jour](release-notes.md), à la date de publication.

## Notes de mise à jour de septembre 2023 (nouveau) {#sept-rn-2023}

**Date de publication** : 26-27 septembre 2023

### Nouvelles fonctionnalités{#sept-2023-features}

Cette version apporte les nouvelles fonctionnalités répertoriées ci-dessous.


<table>
<thead>
<tr>
<th><strong>Rapports consolidés sur le canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La fonction de rapports sur le canal offre aux analystes et aux spécialistes du marketing un aperçu complet du trafic et de l’engagement au niveau du canal. Pour accéder au menu « Rapport », vous devez disposer de l’autorisation « Afficher les rapports du canal ».</p>
<img src="assets/channel-reports.png"/>
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Destinations d’export des jeux de données (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’export des jeux de données Journey Optimizer vers les destinations d’espace de stockage sont désormais disponibles pour tous. Cette fonctionnalité vous permet d’établir une connexion active aux emplacements d’espace de stockage pour exporter le contenu de vos jeux de données.</p>
<img src="../data/assets/dataset-export-setup.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Stockage des informations d’identification de l’application mobile par sandbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Cette nouvelle fonctionnalité vous permet de gérer et d’associer facilement des informations d’identification push à une sandbox dédiée dans les surfaces d’application.</p>
<p>Pour plus d’informations, consultez la <a href="../in-app/inapp-configuration.md">documentation détaillée</a>.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Attributs calculés</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les attributs calculés permettent de résumer facilement les données d’événement dans les attributs de profil par le biais d’une interface utilisateur intuitive pour une segmentation, une personnalisation et une activation optimisées basées sur le comportement. Grâce à cette fonctionnalité, vous pouvez créer des attributs calculés en libre-service, les gérer et les utiliser dans la segmentation, les destinations de profil client en temps réel ou Journey Optimizer.<br/><br/>
En outre, les attributs calculés simplifient la segmentation et les workflows de parcours pour vous aider à diffuser facilement des expériences pertinentes. Pour en savoir plus, consultez la <a href="https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html?lang=fr">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/computed-attributes.gif">
</tr>
</tbody>
</table>


### Améliorations {#sept-2023-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

<!--**Audiences**

* You can now target audiences uploaded from a CSV file into journeys and campaigns.
* You can now target audiences resulting from composition workflows into journeys. -->

**Personnalisation**

* Outre les fragments visuels, il est désormais possible de créer, d’enregistrer et de réutiliser des fragments d’expression à partir de l’interface de Journey Optimizer via l’éditeur d’expression. Les fragments d’expression remplacent les expressions enregistrées précédemment.

**Alerte**

* Introduction d’un nouveau type d’alerte système. Vous pouvez désormais recevoir une notification en cas d’échec d’une lecture d’audience.

**Canal web**

* Les applications monopage (SPA) peuvent désormais être créées dans l’éditeur visuel du concepteur web, ce qui vous permet de sélectionner les vues spécifiques auxquelles vous souhaitez appliquer les modifications de vos pages web. Une vue peut être définie pour un site entier ou un groupe d’éléments visuels sur un site, tels que la page d’accueil, l’ensemble du site de produits ou les préférences de livraison, encadrés sur toutes les pages de passage en caisse. Pour créer et exécuter des campagnes web Adobe Journey Optimizer sur des applications monopage, une configuration unique du développeur est nécessaire pour définir les vues dans l’implémentation du SDK web Adobe Experience Platform.

* Lors de la modification d’une page à l’aide du concepteur web, vous pouvez désormais ajouter de nouvelles modifications à votre contenu directement à partir du volet **Modifications**, sans avoir à sélectionner un composant et à le modifier dans l’interface du concepteur.
* Lors de la configuration de sous-domaines web, vous avez désormais la possibilité d’ajouter votre propre sous-domaine, en plus d’utiliser un sous-domaine déjà délégué à Adobe.

**Parcours**

* La prise en charge des réponses d’action personnalisée est désormais disponible pour tous. Vous pouvez désormais utiliser les réponses d’appel API dans des actions personnalisées et orchestrer votre parcours en fonction de ces réponses. En outre, un nouveau mécanisme de sécurisation a été ajouté pour limiter toutes les actions personnalisées à 5 000 appels/s par point d’entrée.
* Lors de la duplication d’un parcours, vous pouvez désormais définir le nom de la copie de parcours.

<!--
* The maximum duration that you can define in the Wait activity is now 29 days instead of 30.
-->

**Canal e-mail**

Une nouvelle option de configuration de la surface de l’email permet de choisir d’envoyer des messages transactionnels aux profils même si leurs adresses e-mail se trouvent dans la liste de suppression d’Adobe Journey Optimizer.

**Canal SMS**

Deux nouveaux champs, **Message d’opt-in** et **Message d’aide**, ont été ajoutés à l’écran de configuration de l’API, ce qui permet aux utilisateurs de personnaliser les réponses pour les mots-clés entrants. Notez que ceci est uniquement disponible pour le fournisseur SMS Sinch.

**Reporting**

Vous pouvez désormais exporter des rapports Journey Optimizer en tant que fichier CSV. [En savoir plus](../reports/global-report.md#export-reports)

<!--**Decision management**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    -->
