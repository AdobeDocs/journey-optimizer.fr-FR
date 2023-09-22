---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
description: Notes de mise à jour anticipées de Journey Optimizer
hide: true
hidefromtoc: true
source-git-commit: c9be63086b63fb5f4d6094d8bc7690464cf6b768
workflow-type: tm+mt
source-wordcount: '556'
ht-degree: 22%

---

# Notes de mise à jour anticipées {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans les [notes de mise à jour](release-notes.md).

Les notes de mise à jour ci-dessous peuvent être modifiées sans avertissement préalable jusqu’à la date de disponibilité de la version. Les liens, les écrans et la documentation mise à jour sont publiés dans les [notes de mise à jour](release-notes.md), à la date de publication.

## Notes de mise à jour initiales de septembre 2023 {#sept-rn-2023}

**Date de publication**: 26-27 septembre 2023

### Nouvelles fonctionnalités{#sept-2023-features}

Cette version apporte les nouvelles fonctionnalités répertoriées ci-dessous.


<table>
<thead>
<tr>
<th><strong>Rapports Canal consolidé</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La fonction Rapport Canal offre aux analystes et aux spécialistes du marketing un aperçu complet des mesures de trafic et d’engagement au niveau du canal. Pour accéder au menu "Rapport", vous devez disposer de l’autorisation "Afficher les rapports Canal".</p>
<img src="assets/channel-reports.png"/>
<!--p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p-->
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Destinations d’exportation de jeux de données (GA)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’exportation des jeux de données Journey Optimizer vers des destinations de stockage dans le cloud est désormais disponible en général. Cette fonctionnalité vous permet d’établir une connexion active aux emplacements d’espace de stockage pour exporter le contenu de vos jeux de données.</p>
<img src="../data/assets/dataset-export-setup.png">
<!--p>For more information, refer to the <a href="../audience/get-started-audience-orchestration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Stockage des informations d’identification de l’application mobile par environnement de test</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Cette nouvelle fonctionnalité vous permet de gérer et d’associer facilement des informations d’identification push à un environnement de test dédié dans les interfaces d’application.</p>
<p>Pour plus d’informations, consultez la <a href="../in-app/inapp-configuration.md">documentation détaillée</a>.</p>
</tr>
</tbody>
</table>

### Améliorations {#sept-2023-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

<!--**Audiences**

* You can now target audiences uploaded from a CSV file into journeys and campaigns.
* You can now target audiences resulting from composition workflows into journeys. -->

**Personnalisation**

* Outre les fragments visuels, il est désormais possible de créer, enregistrer et réutiliser des fragments d’expression à partir de l’interface de Journey Optimizer via l’éditeur d’expression. Les fragments d’expression remplacent les expressions enregistrées précédemment.
* Vous pouvez désormais utiliser des attributs calculés Adobe Experience Platform pour la personnalisation dans Journey Optimizer. Les attributs calculés sont des valeurs agrégées qui sont calculées selon les jeux de données d’événements d’expérience activés pour le profil ingérés dans Adobe Experience Platform.

**Alerte**

* Deux nouveaux types d’alertes système ont été introduits. Vous pouvez désormais être averti lorsqu’une action personnalisée ou un segment de lecture échoue.

**Canal web**

* Les applications d’une seule page (SPA) peuvent désormais être créées dans l’éditeur visuel web. Vous pouvez maintenant sélectionner les vues spécifiques auxquelles vous souhaitez appliquer les modifications de vos pages web. Une vue peut être définie comme un site entier ou un groupe d’éléments visuels sur un site, tels que la page d’accueil, l’ensemble du site de produits ou les préférences de livraison, encadrés sur toutes les pages de passage en caisse. Une configuration unique pour les développeurs est nécessaire pour définir les vues dans l’implémentation du SDK Web de Adobe Experience Platform. Cela permet aux marketeurs de créer et d’exécuter des campagnes Web Adobe Journey Optimizer sur SPA.

* Lors de la modification d’une page à l’aide du concepteur web, vous pouvez désormais ajouter de nouvelles modifications à votre contenu directement à partir du volet Modifications , sans avoir à sélectionner un composant et à le modifier dans l’interface du concepteur.
* Lors de la configuration de sous-domaines web, vous avez désormais la possibilité d’ajouter votre propre sous-domaine, en plus d’utiliser un sous-domaine déjà délégué à Adobe.

**Parcours**

* Les fonctionnalités de réponse d’action personnalisée sont désormais GA. Cela vous permet d’exploiter les réponses d’appel API dans des actions personnalisées et d’orchestrer votre parcours en fonction de ces réponses. En outre, une nouvelle barrière de sécurité a été ajoutée pour limiter toutes les actions douanières à 5 000 appels/s par point de terminaison.
* Lors de la duplication d’un parcours, vous pouvez désormais définir le nom de la copie de parcours.
* La durée maximale que vous pouvez définir dans l’activité Attente est désormais de 29 jours au lieu de 30.

**Canal e-mail**

Une nouvelle option de configuration de la surface de l&#39;email permet de choisir d&#39;envoyer des messages transactionnels aux profils même si leurs adresses email se trouvent dans la liste de suppression de Adobe Journey Optimizer.

<!--**Decision management**

Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.    -->