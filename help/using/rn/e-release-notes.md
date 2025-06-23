---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour anticipées
description: Notes de mise à jour anticipées de Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 20f5dc6eab5695b485f4569ad098922a130d4b56
workflow-type: ht
source-wordcount: '1022'
ht-degree: 100%

---

# Notes de mise à jour anticipées {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées à la fin de chaque mois dans les [notes de mise à jour](release-notes.md).

**Les notes de mise à jour anticipées ci-dessous peuvent être modifiées sans avertissement préalable jusqu’à la date de disponibilité de la version**. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les [notes de mise à jour](release-notes.md) à la date de publication.


## Notes de mise à jour anticipées de juin 2025 {#25-6-rn}


**Les notes de mise à jour anticipée ci-dessous peuvent être modifiées sans avertissement préalable jusqu’à la date de disponibilité de la version**. Les liens, les copies d’écran et la documentation mise à jour sont publiés à la date de publication.

**Date de publication** : 18 juin 2025


### Nouvelles fonctionnalités {#25-06-features}

Les nouvelles fonctionnalités de cette version sont présentées ci-dessous.




<table>
<thead>
<tr>
<th><strong>Services de messagerie RCS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les services de messagerie RCS (Rich Communication Services) sont désormais pris en charge dans Journey Optimizer, ce qui permet d’utiliser les fonctionnalités de messagerie améliorées suivantes, sous réserve de la prise en charge par le fournisseur et l’opérateur :</p>
<ul>
<li>Prise en charge des expéditeurs de marque vérifiés : envoyez des messages à l’aide de profils métier vérifiés avec des éléments de branding (logo, nom de l’expéditeur, etc.).</li>
<li>Informations sur la diffusion des messages : recevez des rapports de diffusion détaillés comprenant les mises à jour du statut des messages (par exemple, envoyé, diffusé, lu).</li>
<li>Suivi des liens : incorporez et suivez les URL dans les messages RCS pour l’analyse de l’engagement.</li>
<li>Basculement vers les SMS : basculement automatique vers les SMS lorsque l’appareil du profil ne prend pas en charge RCS ou est temporairement inatteignable via RCS.</li>
<li>Composition de base du message : envoyez des messages RCS textuels avec des médias facultatifs et des éléments enrichis, en fonction de la prise en charge du fournisseur.</li>
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
<th><strong>Champs de formulaire dans le contenu d’expérience basée sur du code</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais définir des champs modifiables spécifiques dans les modèles de contenu JSON ou HTML qui permettent aux personnes sans connaissances techniques de modifier facilement le contenu d’une vue de formulaire dans la création de canal d’expérience basée sur du code, sans avoir à manipuler de code.<br />De plus, lors de la définition des modèles de contenu d’expérience basés sur du code, vous pouvez désormais insérer des politiques de décision dans le modèle, ce qui favorise la réutilisation et facilite l’utilisation.</p>
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
<p>Outre la délégation complète et la méthode CNAME, une nouvelle méthode de configuration de sous-domaine est désormais disponible : la méthode de délégation personnalisée. Elle vous permet de contrôler et de gérer totalement l’ensemble des aspects du DNS nécessaires à la diffusion, au rendu et au suivi des messages.</p>
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
<p>Vous pouvez désormais inclure des offres personnalisées dans vos parcours par le biais d’une activité Prise de décision de contenu dédiée dans la zone de travail du parcours et les utiliser dans des activités de parcours, y compris des conditions et des actions personnalisées.</p>
<p>Cette fonctionnalité n’est disponible que pour un ensemble d’organisations (disponibilité limitée) et sera proposée à tous les utilisateurs et utilisatrices dans une prochaine version.</p>
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
<th><strong>Essai de parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’essai de parcours est un mode de publication de parcours spécial dans Adobe Journey Optimizer qui permet aux concepteurs et conceptrices de tester un parcours à l’aide de données de production réelles sans contacter les clients et clientes ni modifier les informations de profil. Cette fonctionnalité permet aux concepteurs et conceptrices du parcours de valider leur conception et leur ciblage d’audience avant de publier le parcours.</p>
<p>Cette fonctionnalité n’est disponible que pour un ensemble d’organisations (disponibilité limitée) et sera proposée à tous les utilisateurs et utilisatrices dans une prochaine version.</p>
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
<p>Vous pouvez maintenant suspendre et reprendre les parcours. Cette fonctionnalité offre aux concepteurs et conceptrices du parcours un meilleur contrôle et une plus grande flexibilité en leur permettant de suspendre temporairement les parcours actifs sans perturber l’expérience client. Lorsque le parcours est suspendu, aucune communication n’est envoyée et les profils restent suspendus jusqu’à la reprise du parcours.</p>
<p>Vous pouvez suspendre et reprendre un seul parcours ou un groupe de parcours par le biais d’opérations en bloc.</p>
<p>En outre, vous pouvez appliquer des filtres globaux aux parcours suspendus afin d’exclure les profils en fonction de leurs attributs.</p>
<p>Cette fonctionnalité n’est disponible que pour un ensemble d’organisations (disponibilité limitée) et sera proposée à tous les utilisateurs et utilisatrices dans une prochaine version.</p>
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
<p>Mettre à l’échelle le gagnant de l’expérimentation vous permet de déployer automatiquement ou manuellement la variation gagnante d’une expérience sur l’ensemble de votre audience. Cette fonctionnalité vous permet d’optimiser la portée et l’efficacité d’un système performant identifié, sans surveillance manuelle constante.</p>
<p>Pour plus d’informations, consultez la <a href="../content-management/content-experiment.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 2 juin 2025</p></td>
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
<p>Date de disponibilité : 3 juin 2025</p>
</td>
</tr>
</tbody>
</table>


### Améliorations {#25-06-improv}

Les améliorations de cette version sont présentées ci-dessous.

* **Jeux de règles de canal**

   * **Fenêtre de durée personnalisée** pour le capping - Un nouveau champ **Nombre de répétitions** est désormais disponible sur l’écran de configuration des jeux de règles de canal. Il vous permet d’appliquer des règles de capping de fréquence sur plusieurs jours, semaines ou mois, selon la durée spécifiée.

   * **Durée en heures** - Vous pouvez désormais appliquer un capping à l’heure pour les jeux de règles de canal.

* **Expériences basées sur du code**

   * L’ajout d’une politique de décision est désormais disponible dans les modèles de contenu d’expérience basés sur du code.

   * À partir du parcours d’expérience basé sur du code ou de l’écran de modification de la campagne, vous pouvez désormais ajouter directement une politique de décision, sans ouvrir l’éditeur de personnalisation.

* **Prise en charge des CSS personnalisés dans le concepteur d’e-mail**

  Journey Optimizer vous permet désormais d’ajouter un CSS personnalisé au contenu de votre e-mail directement dans le concepteur d’e-mail.

* **Nouvelle navigation à onglets pour les campagnes**

  Le nouveau modèle de navigation permet un accès plus rapide à la création de contenu et prend en charge une extension supplémentaire des paramètres dans les campagnes.

* **Prise de décision** - Date de disponibilité : 3 juin 2025

  Les objets de prise de décision peuvent désormais être copiés entre les sandbox, ce qui simplifie les workflows de test et de déploiement. [En savoir plus](../configuration/copy-objects-to-sandbox.md#decisioning)

* **Prise en charge des attributs d’élément de décision pour les règles de prise de décision** - Date de disponibilité : 4 juin 2025

  Vous pouvez désormais tirer parti des attributs d’élément de décision pour créer des règles de prise de décision. [En savoir plus](../experience-decisioning/rules.md#create)

* **Mise à jour de l’API d’exécution de message interactif** - Date de disponibilité : 6 juin 2025

  L’API d’exécution de message interactif vous permet désormais de supprimer le planning d’exécution des campagnes à venir. [En savoir plus](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}