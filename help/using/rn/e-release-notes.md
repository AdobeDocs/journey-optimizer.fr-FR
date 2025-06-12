---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour anticipées
description: Notes de mise à jour anticipées de Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 8dae895f33d8e95424bc96c8050b8f52d7c02b50
workflow-type: tm+mt
source-wordcount: '998'
ht-degree: 35%

---

# Notes de mise à jour anticipées {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées à la fin de chaque mois dans les [notes de mise à jour](release-notes.md).

**Les notes de mise à jour anticipées ci-dessous peuvent être modifiées sans avertissement préalable jusqu’à la date de disponibilité de la version**. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les [notes de mise à jour](release-notes.md) à la date de publication.


## Notes de mise à jour anticipées du 25 juin {#25-6-rn}


**Les notes de mise à jour anticipée ci-dessous peuvent être modifiées sans avertissement préalable jusqu’à la date de disponibilité de la version**. Les liens, les copies d’écran et la documentation mise à jour sont publiés à la date de publication.

**Date de publication** : jeudi 18 juin 2025


### Nouvelles fonctionnalités {#25-06-features}

Les nouvelles fonctionnalités de cette version sont présentées ci-dessous.




<table>
<thead>
<tr>
<th><strong>Messagerie RCS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La messagerie RCS (Rich Communication Services) est désormais prise en charge dans Journey Optimizer, ce qui permet d’utiliser les fonctionnalités de messagerie améliorées suivantes, sous réserve de la prise en charge de l’opérateur :</p>
<ul>
<li>Prise en charge des expéditeurs marqués et vérifiés : envoyez des messages à l’aide de profils métier vérifiés avec des éléments de branding (logo, nom de l’expéditeur, etc.).</li>
<li>Informations sur la diffusion des messages : recevez des rapports de diffusion détaillés comprenant les mises à jour de l’état des messages (par exemple, envoyé, diffusé, lu).</li>
<li>Suivi des liens : incorporez et suivez les URL dans les messages RCS pour l’analyse de l’engagement.</li>
<li>Secours aux SMS : secours automatique aux SMS lorsque l’appareil du profil ne prend pas en charge RCS ou est temporairement inatteignable via RCS.</li>
<li>Composition de base du message : envoyez des messages RCS textuels avec des médias facultatifs et des éléments riches, en fonction de la prise en charge du fournisseur.</li>
</ul>
<!--p>For more information, refer to the <a href="../sms/sms-configuration.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>True Multi-Tenant Unitary Delivery</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>No description provided.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Champs de formulaire dans le contenu d’expérience basé sur le code</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais définir des champs modifiables spécifiques dans les modèles de contenu JSON ou HTML qui permettent aux utilisateurs non techniques de modifier facilement le contenu des expériences basées sur le code sans avoir à manipuler le code.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Méthode de délégation personnalisée pour les sous-domaines</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Outre la délégation complète et la méthode CNAME, une nouvelle méthode de configuration de sous-domaine est désormais disponible : la méthode de délégation personnalisée, qui vous permet de posséder entièrement le contrôle et la maintenance de tous les aspects du DNS nécessaires à la diffusion, au rendu et au suivi des messages.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Activité Prise de décision de contenu dans les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais inclure des offres personnalisées dans vos parcours par le biais d’une activité de prise de décision de contenu dédiée dans la zone de travail de parcours et les utiliser dans des activités de parcours, y compris des conditions et des actions personnalisées.</p>
<p>Cette fonctionnalité n’est disponible que pour un ensemble d’organisations (disponibilité limitée) et sera déployée à l’échelle mondiale dans une prochaine version.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Experience Decisioning in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>No description provided.</p>
</td>
</tr>
</tbody>
</table-->



<table>
<thead>
<tr>
<th><strong>Parcours de l’essai</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’essai de parcours est un mode de publication de parcours spécial dans Adobe Journey Optimizer qui permet aux praticiens du parcours de tester un parcours à l’aide de données de production réelles sans contacter de vrais clients ou mettre à jour les informations de profil. Cette fonctionnalité permet aux utilisateurs et utilisatrices du parcours d’avoir confiance dans leur conception de parcours et leur ciblage d’audience avant de le publier en direct.</p>
<p>Cette fonctionnalité n’est disponible que pour un ensemble d’organisations (disponibilité limitée) et sera déployée à l’échelle mondiale dans une prochaine version.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Suspendre et reprendre les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez maintenant suspendre et reprendre vos parcours. Cette fonctionnalité offre aux professionnels du parcours un meilleur contrôle et une plus grande flexibilité en permettant de suspendre temporairement les parcours en direct sans interrompre l’expérience client. En pause, aucune communication n’est envoyée et les profils restent suspendus jusqu’à la reprise du parcours.</p>
<p>Vous pouvez suspendre et reprendre un seul parcours ou effectuer des opérations de pause et de reprise en bloc sur un groupe de parcours.</p>
<p>En outre, vous pouvez appliquer des filtres globaux aux parcours en pause afin d’exclure les profils en fonction de leurs attributs.</p>
<p>Cette fonctionnalité n’est disponible que pour un ensemble d’organisations (disponibilité limitée) et sera déployée à l’échelle mondiale dans une prochaine version.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mettre à l’échelle le gagnant de l’expérimentation</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le gagnant de l’expérience vous permet de déployer automatiquement ou manuellement la variation gagnante d’une expérience sur l’ensemble de votre audience. Cette fonctionnalité vous permet d’optimiser la portée et l’efficacité d’un système performant identifié, sans surveillance manuelle constante.</p>
<p>Pour plus d’informations, consultez la <a href="../content-management/content-experiment.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 2 juin 2025</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Conflit et hiérarchisation</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dans Journey Optimizer, la gestion du volume et du calendrier des campagnes et des parcours est essentielle pour éviter de submerger les clientes et clients avec un trop grand nombre d’interactions. Journey Optimizer propose désormais plusieurs outils de gestion des conflits et de hiérarchisation, auparavant réservés aux organisations à accès limité (LA), qui sont désormais accessibles au public (GA).</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements. Les améliorations suivantes ont été apportées à cette version à disponibilité générale :</p>
<ul>
<li>Prise en charge étendue : les outils de gestion des conflits prennent désormais en charge les Parcours unitaires et les Parcours de qualification d’audience, en plus des parcours Lecture d’audience.</li>
<li>Amélioration de la résolution des problèmes : deux nouveaux champs d’événement d’étape sont désormais disponibles dans Query Service, ce qui vous permet d’analyser pourquoi un profil a été rejeté d’un parcours ou d’une campagne.</li>
<li>Amélioration des rapports : les rapports indiquent désormais quelle règle spécifique a exclu un profil d’un parcours ou d’une campagne, ce qui offre une plus grande transparence et des informations exploitables.</li></ul>
<img src="assets/do-not-localize/gif-conflict.gif">
<p>Pour plus d’informations, consultez la <a href="../conflict-prioritization/gs-conflict-prioritization.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 3 juin 2025</p>
</td>
</tr>
</tbody>
</table>


### Améliorations {#25-06-improv}

Les améliorations de cette version sont présentées ci-dessous.

* **Jeux de règles de canal**

   * **Fenêtre de durée personnalisée** pour la limitation - Un nouveau champ **Nombre de répétitions** est désormais disponible dans l’écran de configuration des jeux de règles de canal. Il vous permet d’appliquer des règles de limitation de fréquence sur plusieurs jours, semaines ou mois, selon la durée spécifiée.

   * **Durée horaire** - Vous pouvez désormais appliquer une limitation toutes les heures pour les ensembles de règles de canal.

* **Expériences basées sur le code**

  Les politiques de décision sont désormais disponibles dans les modèles de contenu d’expérience basés sur du code et dans le rail de droite de l’éditeur de code.

* **Concepteur d’e-mail**

   * **Prise en charge d’un CSS personnalisé** - Journey Optimizer vous permet désormais d’ajouter un CSS personnalisé au contenu de votre e-mail directement dans le Concepteur d’e-mail.
   * **Prise en charge du mode sombre** - Le Concepteur d’e-mail Journey Optimizer offre désormais la possibilité de passer en mode sombre où vous pouvez définir des paramètres spécifiques.


* **Decisioning** - Date de disponibilité : 3 juin 2025

  Les objets de prise de décision peuvent désormais être copiés entre les sandbox, ce qui simplifie les workflows de test et de déploiement. [En savoir plus](../configuration/copy-objects-to-sandbox.md#decisioning)

* **Prise en charge des attributs d’élément de décision pour les règles de prise de décision** - Date de disponibilité : 4 juin 2025

  Vous pouvez désormais tirer parti des attributs d’élément de décision pour créer des règles de prise de décision. [En savoir plus](../experience-decisioning/rules.md#create)

* **Mise à jour de l’API d’exécution de message interactif** - Date de disponibilité : 6 juin 2025

  L’API d’exécution de message interactif vous permet désormais de supprimer le planning d’exécution des campagnes à venir. [En savoir plus](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}