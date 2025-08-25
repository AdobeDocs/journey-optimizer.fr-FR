---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
topic: Content Management
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: c19c0df82ade193984710f6c2bdae6acd55a6fb5
workflow-type: tm+mt
source-wordcount: '1672'
ht-degree: 73%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations des fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour. [!DNL Adobe Journey Optimizer] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.


## Notes de mise à jour du 25 août {#25-8-rn}

**Date de publication** : 19 août 2025

### Nouvelles fonctionnalités {#Aug-25-8-features}

Les nouvelles fonctionnalités de cette version sont présentées ci-dessous.

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
<p><img src="assets/do-not-localize/PauseResume.gif"/></p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/journey-pause.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Vue Calendrier</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une vue Calendrier est désormais disponible dans les listes des parcours et des campagnes. Elle vous permet de visualiser toutes les activations de parcours et de campagnes dans les listes respectives.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements. Avec cette version en disponibilité générale, la fonctionnalité inclut les points suivants :</p>
<ul>
<li>Améliorations de la conception pour la navigation dans les dates</li>
<li>Possibilité de voir les brouillons de campagne si vous avez défini une date de début et une date de fin</li>
<li>Nouveau paramètre permettant de masquer et d’afficher les éléments de calendrier s’exécutant sur une longue période</li>
</ul>
<p><img src="assets/do-not-localize/calendar.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/journey-ui.md#calendar">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Dark mode in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>The Journey Optimizer Email Designer now offers the ability to switch to dark mode view, where you can additionally define specific custom settings that will display only for recipients reading their emails in dark mode.</p>
<p>Note the following:</p>
<ul>
<li>The dark mode final rendering may vary and depends on the recipient's email client.</li>
<li>Not all email clients support custom dark mode. Moreover, some email clients only apply their own default dark mode for all emails that are received. In both cases, the custom settings that you defined in the Email Designer cannot be rendered.</li>
</ul>
<P>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>For more information, refer to the <a href="../email/dark-mode.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Use Adobe Experience Platform data for personalization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Leverage data from [!DNL Adobe Experience Platform] in the personalization editor to personalize your content and decision attributes. In particular, this allows you to extend the definition of your attributes to additional data in datasets for bulk updates that change periodically without having to manually update the attributes one at a time.</p>
<p>With this release, the following enhancements have been introduced:</p>
<ul>
<li>Support of inbound channels,</li>
<li>The "datasetLookup" helper function can now be used within expression and visual fragments to personalize content using data from Adobe Experience Platform datasets,</li>
<li>An option in the dataset now allows you to enable datasets for lookup personalization, without having to perform an API call.</li>
</ul>
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p>For more information, refer to the <a href="../personalization/aep-data-perso.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Use Decisioning in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add Decision policies into email journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><img src="assets/do-not-localize/FILE.gif"/></p>
<p><For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Journey path optimization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Use the new Optimize node to target specific audiences or run A/B tests to determine the best path to meet your business-centric KPIs.</p>
<p>This tool allows you to test and vary, and customize communications, sequencing, and timing to best reach your customers.</p>
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p><img src="assets/do-not-localize/optimize.gif"/></p>
<p>For more information, refer to the detailed documentation</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Activité d’action dans les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer prend en charge une nouvelle activité d’action générique qui vous permet de configurer des actions uniques et des groupes d’actions entrantes multiples, ce qui simplifie la configuration des actions dans la zone de travail de parcours. Cette nouvelle fonctionnalité permet notamment les opérations suivantes :</p>
<ul>
<li>Configuration d’action native simplifiée dans la zone de travail de parcours</li>
<li>Capacité à créer des groupes d’actions entrants multiactions.</li>
<li>Possibilité d’ajouter une optimisation à toute action de canal intégrée</li>
<li>Possibilité d’ajouter des options d’expérimentation et multilingues à n’importe quelle action</li>
</ul>
<p>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour obtenir l’accès.</p>
<p><img src="assets/do-not-localize/action-activity.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/journey-action.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Pièces jointes PDF aux e-mails</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais joindre un fichier PDF statique à un e-mail envoyé avec Journey Optimizer.</p>
<ul>
<li>Vous pouvez envoyer jusqu’à 6 messages avec une pièce jointe PDF par profil et par an.</li>
<li>La taille maximale autorisée pour chaque fichier joint est de 5 Mo.</li>
<li>Pour augmenter la taille ou le volume, vous pouvez acheter un module complémentaire de pack de pièces jointes. Pour plus d’informations, contactez votre représentant ou représentante Adobe.</li>
</ul>
<p>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour obtenir l’accès.</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../email/pdf-attachments.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Landing page custom forms</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With [!DNL Journey Optimizer], you can now capture profile attributes though your landing pages.</p>
<p>Create, design and manage custom forms tailored to your needs based on a specific dataset. You can then leverage these forms in landing pages to add the profile attributes of your choice into the dataset defined for each form.</p>
<p>This capability is currently in beta version and only available to beta customers. To join the beta program, contact your Adobe representative.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Optimisation des campagnes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer vous fournit désormais les outils nécessaires pour diffuser du contenu personnalisé et optimisé à votre audience. Vous pouvez ainsi exécuter des expériences de contenu, créer un ciblage basé sur des règles et utiliser des combinaisons avancées des deux, afin d’optimiser l’efficacité de vos campagnes et de vos parcours.</p>
<p>Avec l’optimisation, vous pouvez réaliser les actions suivantes :</p>
<ul>
<li>Tester plusieurs variations de contenu pour identifier le message le plus efficace.</li>
<li>Diffuser du contenu personnalisé en fonction des attributs d’utilisation et des données contextuelles.</li>
<li>Combinez le ciblage et l’expérimentation pour des stratégies avancées.</li>
<li>Filtrer les utilisateurs et utilisatrices qui ne correspondent pas aux critères de variante.</li>
<li>Garantir des mécanismes de secours pour maintenir l’interaction client.</li>
</ul>
<P>Une fois le parcours ou la campagne actif, les profils sont évalués en fonction des critères définis. S’ils correspondent aux critères, ils sont diffusés avec l’expérience ou le contenu approprié.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>Précédemment publiée le 8 août dans les campagnes uniquement, cette capacité est désormais également disponible dans les parcours à partir du 22 août.</p>
<p>Pour plus d’informations, consultez la <a href="../campaigns/campaigns-message-optimization.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#Aug-25-8-improv}

Les améliorations de cette version sont présentées ci-dessous.

* **Administration**

   * **Alertes de surveillance de la configuration des canaux** - Vous pouvez désormais vous abonner pour recevoir des alertes système, par e-mail ou dans le centre de notifications Journey Optimizer, au cas où <!--a channel configuration failure happens or if -->un enregistrement DNS est manquant. [En savoir plus](../reports/alerts.md#alert-dns-record-missing)

* **Campagnes**

   * **Contrôle des taux dans les campagnes sortantes** - Vous pouvez désormais activer le contrôle des taux pour les campagnes sortantes (e-mail, SMS, notifications push), ce qui vous permet d’éviter la surcharge des systèmes en aval, tels que les pages de destination ou les plateformes d’assistance clientèle. [En savoir plus](../campaigns/campaign-schedule.md#rate-control)

   * **Planification de campagnes d’action** : les planificateurs de campagnes quotidiens, hebdomadaires et mensuels ont été mis à jour afin d’assurer un contrôle plus détaillé des planifications récurrentes :

      * **Périodicité hebdomadaire** : vous pouvez désormais choisir de répéter la campagne toutes les semaines ou toutes les deux semaines, et sélectionner le ou les jours de la semaine où elle doit s’exécuter.

      * **Récurrence mensuelle** : vous pouvez désormais choisir de répéter la campagne tous les mois ou tous les deux mois, et sélectionner le jour du mois où elle doit s’exécuter.

      * **Plannings quotidiens, hebdomadaires ou mensuels** : vous pouvez indiquer si le planning récurrent doit s’arrêter à une date spécifique ou après un certain nombre d’occurrences.

   * **Campagnes d’action transactionnelles planifiées** : les campagnes d’action transactionnelles planifiées sont désormais disponibles pour l’envoi de communications transactionnelles par lots, basées sur l’audience, via des canaux e-mail, SMS et push.

* **Canal - Cartes de contenu**

   * **Modèles de disposition de carte de contenu** - Le canal de carte de contenu fournit désormais des dispositions de message prêtes à l’emploi qui rationaliseront votre expérience de création. Cette version comprend des modèles de disposition Petite image, Grande image et Image uniquement.

* **Canal - Push**

   * **Date d’expiration des notifications push** : vous pouvez désormais spécifier une date d’expiration pour chaque notification push. Cela empêche l’envoi de messages urgents (comme les soldes du Black Friday) après une certaine date, évitant ainsi une mauvaise expérience pour vos clientes et clients.

* **Canal - SMS**

   * **Opt-out en logique floue** : lorsqu’elle est activée, l’option **Opt-out en logique floue** détecte les messages entrants qui ressemblent fortement aux mots-clés d’opt-out définis (par exemple, « CANCIL ») et envoie automatiquement une réponse de confirmation pour vérifier l’intention de désabonnement de l’utilisateur ou l’utilisatrice. Si l’utilisateur confirme via l’invite définie, il est désabonné. [En savoir plus](../sms/sms-configuration-sinch.md)

     >[!NOTE]
     >
     >**Opt-out flou** est disponible uniquement avec Sinch et Infobip.

   * **Vérifier la connexion SMS** - Vous pouvez désormais facilement tester et vérifier vos informations d’identification d’API SMS dans Adobe Journey Optimizer en envoyant un exemple de message à un appareil désigné. [En savoir plus](../sms/sms-configuration-sinch.md)

* **Configuration**

  &lt;!—* **Prise en charge des domaines dynamiques** - Journey Optimizer prend désormais en charge la personnalisation complète/de base des URL pour les domaines prédéfinis acceptés par Adobe. Cette fonctionnalité est disponible en disponibilité limitée pour un ensemble de clients et clientes. [En savoir plus](../personalization/personalization-build-expressions.md#where)—Mise à jour le 21 août : En attente de l&#39;eng. pour confirmer le déploiement sur prod.—>

   * **Prise en charge des attributs personnalisés avec l’URL de désabonnement en un clic** : a-vec Journey Optimizer, si vous gérez le consentement en dehors d’Adobe, vous pouvez définir un point d’entrée personnalisé externe en définissant votre propre lien de désabonnement en un clic dans la configuration de l’e-mail. Lorsque les personnes destinataires cliquent sur le lien de désabonnement, Journey Optimizer ajoute certains paramètres par défaut, spécifiques au profil, à l’événement de mise à jour du consentement.

     Pour personnaliser davantage votre lien de désabonnement en un clic, vous pouvez maintenant définir des attributs personnalisés qui seront également ajoutés à l’événement de consentement. [En savoir plus](../email/list-unsubscribe.md#custom-attributes)

* **Jeux de données**

   * **Référentiel d’objets Experience Decisioning - Éléments d’offre personnalisés** - Le jeu de données d’exportation intégré capture désormais tous les attributs de l’offre et le statut du cycle de vie, ce qui permet une personnalisation et un reporting complets. [En savoir plus](../data/export-datasets.md)

   * Ajout de la vérification des versions via le champ `etag` pour améliorer la cohérence et suivre les modifications afin d’offrir des articles plus facilement.

* **Prise de décision**

   * **Joindre des fragments aux éléments de décision** - Journey Optimizer permet désormais de joindre des fragments aux éléments de décision qui peuvent être utilisés dans les campagnes d’expérience basées sur le code par le biais de politiques de décision. Cette fonctionnalité est disponible en disponibilité limitée pour un ensemble de clients et clientes. [En savoir plus](../experience-decisioning/create-decision.md#fragments)

* **Parcours**

   * **Opérations de parcours en masse** : dans la liste de vos parcours, vous pouvez désormais sélectionner plusieurs éléments. Une fois la sélection réalisée, vous pouvez suspendre ou reprendre jusqu’à 10 parcours à la fois.

   * **Prise en charge de la redirection (302) dans les actions personnalisées** : les actions personnalisées peuvent désormais gérer les redirections HTTP 302 requête par requête. Cela permet aux parcours de s’intégrer aux API qui redirigent les requêtes vers des URL localisées ou spécifiques à une région. Les redirections sont suivies automatiquement, ce qui garantit que le contenu diffusé est correct, sans configuration supplémentaire.

   * **Plusieurs actions entrantes dans les parcours** - Pour simplifier votre orchestration des parcours, vous pouvez désormais définir plusieurs actions entrantes dans un seul parcours. Précédemment disponible dans les campagnes, cette fonctionnalité vous permet de diffuser simultanément plusieurs expériences basées sur du code, des messages in-app, des cartes de contenu ou des actions web à différents emplacements, chaque action contenant un contenu spécifique. [En savoir plus](../building-journeys/journey-action.md#multi-action)

## Orchestration de campagne

**Date de disponibilité** : 4 août 2025

Journey Optimizer comprend désormais l’**orchestration des campagnes**, une nouvelle fonctionnalité spécialement conçue pour les campagnes par lots lancées par la marque. Cette version présente une zone de travail d’orchestration de campagne et une modélisation des données améliorée, qui fonctionnent ensemble pour permettre aux spécialistes marketing de planifier, de cibler et de diffuser des campagnes cross-canal personnalisées.

>[!IMPORTANT]
>
>Pour accéder à l’orchestration de campagne, votre licence doit inclure le package **Journey Optimizer - Campagnes et parcours** ou **Journey Optimizer - Campagnes**. Contactez votre représentant ou représentante Adobe pour confirmer votre licence et effectuer une mise à jour si nécessaire.

![GIF de l’orchestration de campagne](assets/do-not-localize/release.gif)

Elle comprend des [jeux de données et des schémas relationnels](#oc-relational) et une [zone de travail de campagne](#oc-canvas). Ensemble, ces deux innovations ouvrent la voie à un nouveau standard d’orchestration des campagnes par lots dans Journey Optimizer. Les fonctionnalités principales sont répertoriées ci-dessous.

### Fonctionnalités principales {#oc-capabilities}

* **Workflows à plusieurs étapes**

  Pilotez des campagnes par lots multicanaux sophistiquées avec la nouvelle zone de travail personnalisée pour l’orchestration de campagne.

* **Audiences à la demande**

  Segmentez les audiences à la demande pour une activation immédiate.

* **Segmentation d’entités multiples**

  Créez des audiences à l’aide du contexte commercial (dimensions autres que les personnes), par exemple les produits, les magasins, les renouvellements, les réservations, etc.

* **Visibilité avant envoi**

  Examinez, affiner et optimiser les audiences et les campagnes avant le lancement et pendant l’exécution des campagnes.

### Zone de travail de campagne {#oc-canvas}

Une toute nouvelle interface d’orchestration visuelle, conçue spécialement pour les campagnes par lots. Cette zone de travail permet d’effectuer les opérations suivantes :

* Planification visuelle des flux de campagnes multicanaux et à plusieurs étapes

* Prise en charge des audiences à la demande créées à partir de requêtes relationnelles

* Partage d’audience, attentes et logique conditionnelle avancés

* Nombre précis de pré-envois après l’application de règles et de filtres métier

### Jeux de données et schémas relationnels {#oc-relational}

Adobe Journey Optimizer prend désormais en charge les entités relationnelles (produits, magasins, réservations, contrats, etc.) liées à des profils basés sur des personnes. Cela permet la segmentation et la personnalisation sur des structures de données multidimensionnelles, en activant des cas d’utilisation tels que :

* Un message par réservation, abonnement ou contrat

* Segmentation basée sur les attributs d’entité associés (par exemple, catégorie de produits ou emplacement de magasin)

* Adressabilité améliorée (par exemple, envoi à tous les contacts connus liés à une entité)

### Importance de ces éléments

Cette version donne aux spécialistes marketing un contrôle total sur le marketing par lots initié par la marque et basé sur l’audience, en combinant la modélisation flexible des données avec une expérience d’orchestration personnalisée. Elle est spécialement conçue pour l’orchestration de campagne par lots à partir de parcours en temps réel, tout en offrant une personnalisation et une évolutivité avancées.

### En savoir plus

Pour en savoir plus, consultez la [documentation sur l’orchestration de campagne](../orchestrated/gs-orchestrated-campaigns.md).


