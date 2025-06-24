---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
topic: Content Management
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 7e378cbda6ee2379a8bd795588c328cb14107aa4
workflow-type: tm+mt
source-wordcount: '1179'
ht-degree: 72%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations des fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour. [!DNL Adobe Journey Optimizer] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.


## Notes de mise à jour du 25 juin {#25-6-rn}

<!--
**Early release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.-->

**Date de publication** : 18 juin 2025

<!--See also [Adobe Experience Platform Pre Release Notes](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

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
<p>Pour plus d’informations, consultez la <a href="../sms/sms-configuration.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Champs de formulaire dans le contenu d’expérience basée sur du code</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais définir des champs modifiables spécifiques dans les modèles de contenu JSON ou HTML qui permettent aux personnes sans connaissances techniques de modifier facilement le contenu d’une vue de formulaire dans la création de canal d’expérience basée sur du code, sans avoir à manipuler de code.<br />En outre, lors de la définition des modèles de contenu d’expérience basés sur du code, vous pouvez désormais insérer des politiques de décision dans le modèle, ce qui favorise la réutilisation et facilite l’utilisation.</p>
<img src="assets/do-not-localize/form-fields.gif">
<p>Pour plus d’informations, consultez la <a href="../code-based/code-based-form-fields.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Custom delegation method for subdomains</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In addition to the full delegation and the CNAME method, a new subdomain configuration method is now available: the Custom delegation method, which enables you to fully own controlling and maintaining all aspects of DNS that are required for delivering, rendering and tracking messages.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Activité Décision de contenu dans les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais inclure des offres personnalisées dans vos parcours par le biais d’une activité de décision de contenu dédiée dans la zone de travail de parcours et les utiliser dans des activités de parcours, y compris des conditions et des actions personnalisées.</p>
<img src="assets/do-not-localize/content-decision.gif">
<p>Cette fonctionnalité n’est disponible que pour un ensemble d’organisations (disponibilité limitée) et sera proposée à tous les utilisateurs et utilisatrices dans une prochaine version.</p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/content-decision.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

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
<img src="assets/do-not-localize/DryRun.gif">
<p>Cette fonctionnalité n’est disponible que pour un ensemble d’organisations (disponibilité limitée) et sera proposée à tous les utilisateurs et utilisatrices dans une prochaine version.</p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/journey-dry-run.md">documentation détaillée</a>.</p>

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
<img src="assets/do-not-localize/PauseResume.gif">
<p>Cette fonctionnalité n’est disponible que pour un ensemble d’organisations (disponibilité limitée) et sera proposée à tous les utilisateurs et utilisatrices dans une prochaine version.</p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/journey-pause.md">documentation détaillée</a>.</p>
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


<table>
<thead>
<tr>
<th><strong>jeux de données Adobe Experience Platform dans la prise de décision (version bêta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Auparavant disponibles pour la personnalisation, les jeux de données Adobe Experience Platform peuvent désormais être utilisés pour la prise de décision. Cela vous permet d’étendre la définition de vos attributs de décision aux données supplémentaires des jeux de données pour les mises à jour en bloc qui changent régulièrement sans avoir à mettre à jour manuellement les attributs un par un. Par exemple, la disponibilité, les temps d’attente, etc.</p>
<p>Cette fonctionnalité est actuellement disponible en version Beta publique pour l’ensemble des clientes et clients. Veuillez contacter votre représentant de compte si vous souhaitez accéder à cette fonctionnalité</p>
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/aep-data-exd.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 20 juin 2025</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#25-06-improv}

Les améliorations de cette version sont présentées ci-dessous.

* **Jeux de règles de canal**

   * **Fenêtre de durée personnalisée** pour la limitation : un nouveau champ **Toutes les** est désormais disponible dans l’écran de configuration des jeux de règles de canal, ce qui vous permet d’appliquer des règles de limitation de la fréquence sur plusieurs jours, semaines ou mois, selon la durée spécifiée.

   * **Fréquence de limitation de la réinitialisation toutes les heures** - Vous pouvez désormais appliquer une limitation toutes les heures pour les ensembles de règles de canal. Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Contactez l’assistance clientèle pour l’activer.

   * **Durée quotidienne** - Auparavant disponible en disponibilité limitée, le capping de la fréquence « quotidienne » dans les ensembles de règles de canal est désormais disponible pour tous les clients.

  Pour plus d’informations, consultez la [documentation détaillée](../conflict-prioritization/channel-capping.md).

* **Expériences basées sur du code**

   * L’ajout d’une politique de décision est désormais disponible dans des modèles de contenu d’expérience basés sur du code, où elle peut être utilisée pour tirer parti des offres dans les champs de formulaire modifiables. [En savoir plus](../code-based/code-based-form-fields.md)

   * À partir du parcours d’expérience basé sur le code ou de l’écran d’édition de la campagne, vous pouvez désormais ajouter directement une politique de décision, sans ouvrir l’éditeur de personnalisation. [En savoir plus](../code-based/create-code-based.md#edit-code)

* **Prise en charge des CSS personnalisés dans le concepteur d’e-mail**

  Journey Optimizer vous permet désormais d’ajouter un CSS personnalisé au contenu de votre e-mail directement dans le Designer d’e-mail. [En savoir plus](../email/custom-css.md)

* **Nouvelle navigation à onglets pour les campagnes**

  Un nouveau modèle de navigation permet un accès plus rapide à la création de contenu et prend en charge une extension supplémentaire des paramètres dans les campagnes. [En savoir plus](../campaigns/create-campaign.md)

* **Prise de décision**

   * **Copie de sandbox et prise de décision** (date de disponibilité : 3 juin 2025) - Les objets Decisioning peuvent désormais être copiés entre des sandbox, ce qui simplifie les workflows de test et de déploiement. [En savoir plus](../configuration/copy-objects-to-sandbox.md#decisioning)

   * **Prise en charge des attributs d’élément de décision pour les règles de prise de décision** (date de disponibilité : 4 juin 2025) - Vous pouvez désormais tirer parti des attributs d’élément de décision pour créer des règles de prise de décision. [En savoir plus](../experience-decisioning/rules.md#create)

* **Mise à jour de l’API d’exécution de message interactif** - Date de disponibilité : 6 juin 2025

  L’API d’exécution de message interactif vous permet désormais de supprimer le planning d’exécution des campagnes à venir. [En savoir plus](https://developer.adobe.com/journey-optimizer-apis/references/messaging/){target="_blank"}
