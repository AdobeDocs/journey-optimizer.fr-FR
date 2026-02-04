---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 9ac3eaba0b4c6536c1c447df825eb5f5c0afc900
workflow-type: tm+mt
source-wordcount: '1710'
ht-degree: 87%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] suit un modèle de diffusion continue, ce qui permet à Adobe de diffuser régulièrement de nouvelles fonctionnalités, de nouvelles améliorations et de nouveaux correctifs. Cette approche permet un déploiement évolutif et échelonné des fonctionnalités afin d’assurer les performances et la stabilité dans tous les environnements.

En raison de ce modèle, les notes de mise à jour sont mises à jour entre les versions mensuelles. Pour plus d’informations sur le cycle de publication et les phases de disponibilité, consultez le [cycle de publication de Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Notes de mise à jour de janvier 2026 {#latest-rn}

<!--**Release date**: January 27-28, 2026-->

Les sections [Fonctionnalités](#jan-26-01-features) et [Améliorations](#jan-26-01-improv) couvrent les fonctionnalités déjà disponibles, tandis que [Bientôt disponible](#jan-26-01-coming-soon) répertorie les éléments planifiés pour une date de disponibilité ultérieure.

<!-- **The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date. 

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### Nouvelles fonctionnalités {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>API d’outils de migration en libre-service</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les <strong>API d’outils de migration</strong> sont désormais disponibles pour migrer par programme les entités de gestion des décisions vers la prise de décision, et comprennent les fonctionnalités suivantes :</p>
<ul>
<li>Des portées de migration flexibles (sandbox, offre ou niveau de décision)</li>
<li>L’analyse et la validation automatisées des dépendances</li>
<li>La prise en charge de la restauration pour les migrations terminées</li>
<li>Des rapports de migration détaillés avec les mappages d’objet</li>
</ul>
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/decisioning-migration-api.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 3 février 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Surveillance des actions personnalisées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Obtenez une meilleure visibilité de l’intégrité et des performances de vos <strong>points d’entrée d’action personnalisée</strong> grâce à un nouveau tableau de bord de surveillance et à des données d’événement d’étape de parcours enrichies. Effectuez le suivi des appels réussis, des erreurs, du débit, des temps de réponse et des temps d’attente de la file d’attente pour comprendre rapidement quand, où et pourquoi des anomalies se produisent.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<p>Pour plus d’informations, consultez la <a href="../action/reporting.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 3 février 2026</p>
</td>
</tr>
</tbody>
</table>
<table>

<thead>
<tr>
<th><strong>Prise en charge de la prise de décision dans le canal SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais personnaliser et optimiser le contenu de vos <strong>SMS</strong> avec <strong>Decisioning</strong>. Utilisez des scores de priorité, des formules ou des modèles d’IA pour afficher le meilleur contenu à vos clientes et clients.</p>
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/create-decision.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 2 février 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Prise en charge de la prise de décision dans le canal push</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais personnaliser et optimiser le contenu de vos <strong>notifications push</strong> avec <strong>Decisioning</strong>. Utilisez des scores de priorité, des formules ou des modèles d’IA pour afficher le meilleur contenu à vos clientes et clients.</p>
<p>Experience Decisioning avec les notifications push nécessite une version spécifique de Mobile SDK. Avant d’implémenter cette fonctionnalité, consultez les <a href="https://developer.adobe.com/client-sdks/home/release-notes/" target="_blank">notes de mise à jour</a> pour identifier la version requise et vous assurer que vous avez effectué la mise à niveau en conséquence. Vous pouvez également afficher toutes les versions de SDK disponibles pour votre plateforme dans <a href="https://developer.adobe.com/client-sdks/home/current-sdk-versions/" target="_blank">cette section</a>.</p>
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/create-decision.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 30 janvier 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal Courrier dans les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Auparavant limité aux campagnes, le canal <strong>Courrier</strong> est désormais disponible sur la zone de travail de parcours, ce qui vous permet d’incorporer le courrier dans vos parcours. Le courrier peut désormais être utilisé dans les <strong>scénarios de parcours par lots et individuels</strong>, avec la prise en charge de la configuration de l’extraction de fichiers et des paramètres de fréquence basés sur le temps.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<p><img src="assets/do-not-localize/dm-journey.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../direct-mail/get-started-direct-mail.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : vendredi 29 janvier 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Heures creuses (exclusions basées sur les heures)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les <strong>heures creuses</strong> vous permettent de définir des exclusions basées sur les heures pour les canaux E-mail, SMS, Notification push et WhatsApp. EIles garantissent qu’aucun message n’est envoyé pendant des périodes spécifiques, ce qui vous aide à respecter les préférences de la clientèle et les exigences de conformité. Vous pouvez appliquer des heures creuses par le biais d’<strong>ensembles de règles</strong> qui peuvent être affectés à des actions individuelles dans des campagnes ou des parcours pour un contrôle précis.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements. Avec cette version en disponibilité générale, la fonctionnalité permet désormais à la clientèle de mettre en file d’attente une action de campagne jusqu’à la fin des heures creuses et de prévisualiser la règle des heures creuses activée.</p>
<p><img src="assets/do-not-localize/quiet-hour-ga.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../conflict-prioritization/quiet-hours.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : vendredi 29 janvier 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Exporter des messages</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une nouvelle fonctionnalité d’<strong>export des messages</strong> est désormais disponible pour les canaux e-mail et SMS. Cette fonctionnalité vous permet d’exporter automatiquement le contenu des messages envoyés vers un jeu de données Experience Platform dédié, ce qui vous permet d’effectuer les opérations suivantes :</p>
<ul>
<li>Respecter les exigences réglementaires (telles que la loi HIPAA)</li>
<li>Archiver les messages pour les réclamations juridiques et les demandes de renseignements de l’assistance clientèle</li>
<li>Conserver des copies du contenu personnalisé envoyé aux individus</li>
</ul>
<p>Les enregistrements sont conservés dans le jeu de données d’export des messages AJO pendant 7 jours calendaires à compter de l’ingestion. Pendant cette période de conservation, vous pouvez les exporter vers votre propre espace de stockage via les destinations Experience Platform. La fonctionnalité est activée au niveau de la configuration des canaux, ce qui vous permet de <strong>contrôler de façon précise</strong> les messages exportés.</p>
<p>Cette fonctionnalité n’est disponible que pour les canaux e-mail et SMS, pour les organisations qui ont acheté l’offre complémentaire d’export des messages. Pour plus d’informations, contactez votre représentant ou représentante Adobe.</p>
<p><img src="assets/do-not-localize/message-export.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../configuration/message-export.md#message-export">documentation détaillée</a>.</p>
<p>Date de disponibilité : 28 janvier 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal courrier dans les campagnes orchestrées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le canal courrier est désormais disponible dans les campagnes orchestrées. L’<strong>activité Courrier</strong> facilite l’envoi de courrier depuis votre campagne orchestrée pour les messages ponctuels et récurrents. Elle permet d’automatiser le processus de génération du <strong>fichier d’extraction</strong> requis par les prestataires de services postaux. Vous pouvez combiner des activités de canal dans la zone de travail de campagne orchestrée afin de créer des campagnes cross-canal pouvant déclencher des actions en fonction du comportement de la clientèle et des données.</p>
<p><img src="assets/do-not-localize/dm-oc.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../orchestrated/activities/channels.md#channel">documentation détaillée</a>.</p>
<p>Date de disponibilité : 28 janvier 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Agent Journey : création d’un parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’agent Journey offre désormais des fonctionnalités de création qui permettent aux utilisateurs et utilisatrices de Journey Optimizer de créer et de configurer des parcours marketing par le biais d’une <strong>interface en langage naturel </strong>. Grâce à ces nouvelles compétences, les utilisateurs et utilisatrices peuvent rapidement créer des parcours en décrivant simplement leurs besoins dans des <strong>prompts conversationnels</strong>. Cette innovation simplifie le processus de création de parcours, ce qui permet aux spécialistes marketing de se concentrer sur la stratégie plutôt que sur la configuration technique.</p>
<p>Pour plus d’informations, consultez la <a href="../start/ai-features.md#journey-agent">documentation détaillée</a>.</p>
<p>Date de disponibilité : 12 janvier 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API de récupération de campagne d’action</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une nouvelle API Journey Optimizer est désormais disponible. Celle-ci vous permet de récupérer et d’inspecter par programme les <strong>données liées à la campagne</strong>, telles que les détails, les versions et les configurations.</p>
<p>Pour plus d’informations, consultez la <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/" target="_blank">documentation détaillée</a>.</p>
<p>Date de disponibilité : 24 novembre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Thèmes du Concepteur d’e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais appliquer rapidement des <strong>thèmes préapprouvés</strong> pour garantir la <strong>cohérence de la marque</strong> dans tous les e-mails, accélérer le processus de création de vos campagnes et produire de manière autonome des e-mails de grande qualité tout en réduisant la dépendance à l’égard des équipes de conception.</p>
<p><img src="assets/do-not-localize/themes.gif"/></p>
<p>Publiée auparavant en version bêta, cette fonctionnalité est désormais disponible pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Pour plus d’informations, consultez la <a href="../email/apply-email-themes.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 5 novembre 2025</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#jan-26-01-improv}

#### IA

* **Contrôles de qualité du contenu de l’assistant IA** : en plus de l’alignement sur la marque, vous pouvez désormais évaluer la <strong>qualité du contenu</strong> globale pour identifier les problèmes potentiels de <strong>lisibilité</strong>, de cohésion et d’efficacité, indépendamment des directives de votre marque. Ces contrôles automatisés permettent d’identifier les messages peu clairs, le ton incohérent ou les lacunes structurelles. [En savoir plus](../content-management/brands-score.md#validate-quality).

  [Découvrez cette fonctionnalité en vidéo](https://video.tv.adobe.com/v/3470548/?captions=fre_fr&learn=on).

#### Parcours

* **Combiner des actions de message natives et Adobe Campaign** : Journey Optimizer vous permet désormais de combiner des actions de message <strong>Adobe Campaign v7/v8</strong> avec des <strong>actions de canal natives</strong> dans le même parcours. [En savoir plus](../building-journeys/using-adobe-campaign-v7-v8.md)

  Date de disponibilité : mercredi 27 janvier 2026.

* **Payload de réponse d’erreur d’action personnalisée** : vous pouvez désormais définir une <strong>payload de réponse d’erreur</strong> facultative pour les actions personnalisées. Lorsqu’un appel échoue, la payload d’erreur est exposée dans le contexte du parcours (sous le nœud errorResponse de l’action) et est disponible dans la branche <strong>temporisation/erreur</strong>, avec `jo_status_code`, afin de permettre une logique de secours plus riche et le débogage. [En savoir plus](../action/about-custom-action-configuration.md#define-the-message-parameters)

  Date de disponibilité : mercredi 27 janvier 2026.

* **Validation de la taille de la payload du parcours dans les parcours** : Journey Optimizer valide désormais les <strong>tailles de la payload</strong> pour garantir des performances optimales et la stabilité du système. Lors de la création ou de la publication de parcours, vous recevez <strong>des avertissements et des erreurs</strong> clairs si les tailles de payload approchent ou dépassent les limites recommandées, ainsi que des conseils pratiques pour optimiser votre configuration de parcours. Cette validation proactive vous permet d’identifier rapidement les problèmes potentiels et de maintenir les performances du parcours. [En savoir plus](../start/guardrails.md#journey-payload-size)

  Date de disponibilité : mercredi 27 janvier 2026.


* **Alertes de parcours** : de nouvelles <strong>alertes préconfigurées</strong> sont disponibles pour les parcours.
   * <strong>Taux de rejet de profil dépassé</strong> : ratio de rejets de profil par rapport aux profils ayant rejoint le parcours au cours des 5 dernières minutes et ayant dépassé le seuil.
   * <strong>Taux d’erreur d’action personnalisée dépassé</strong> : ratio des erreurs d’action personnalisée par rapport aux appels HTTP réussis au cours des 5 dernières minutes et ayant dépassé le seuil.
   * <strong>Taux d’erreur de profil dépassé</strong> : ratio de profils erronés par rapport aux profils ayant rejoint le parcours au cours des 5 dernières minutes et ayant dépassé le seuil.

  Pour plus d’informations, consultez la [documentation détaillée](../reports/alerts.md).

  Date de disponibilité : 14 octobre 2025

#### Campagnes orchestrées

* **Héritage des libellés d’utilisation des données pour les audiences** : les libellés appliqués dans Adobe Experience Platform sont désormais automatiquement transférés lors de l’enregistrement des <strong>audiences</strong> dans les campagnes orchestrées, ce qui réduit le <strong>balisage DULE</strong> manuel. [En savoir plus](../orchestrated/activities/save-audience.md)

* **Filtres prédéfinis avec paramètres** : vous pouvez désormais créer des <strong>filtres prédéfinis</strong> avec <strong>paramètres</strong> dans les campagnes orchestrées pour des règles réutilisables et modifiables. [En savoir plus](../orchestrated/predefined-filters.md)

* **Sélectionner des attributs et copier les valeurs de distribution** : vous pouvez désormais <strong>sélectionner ou copier des valeurs</strong> directement à partir de la vue de <strong>distribution des valeurs</strong> dans les campagnes orchestrées. [En savoir plus](../orchestrated/build-query.md)

* **Confirmation des messages avant l’envoi** : une <strong>étape de confirmation</strong> est désormais activée par défaut avant l’envoi de campagnes orchestrées afin de réduire les envois accidentels. [En savoir plus](../orchestrated/activities/channels.md#confirm-message-sending)

* **Filtres de reciblage prédéfinis** : pour prendre en charge un reciblage plus facile pour les cas d’utilisation de campagnes orchestrées, cette version introduit de nouveaux <strong>filtres de commentaires sur les campagnes</strong>. Ces filtres vous permettent de cibler directement des audiences en fonction de l’<strong>interaction avec les messages</strong>, par exemple, envoyés, ouverts uniquement, ouverts ou ayant fait l’objet d’un clic ou ouverts et ayant fait l’objet d’un clic, puis de sélectionner la campagne spécifique ou la campagne en transition à recibler. [En savoir plus](../orchestrated/retarget.md)

* **Prise en charge du contrôle du débit** : les campagnes orchestrées prennent désormais en charge le <strong>contrôle du débit</strong> afin de vous permettre de réguler les diffusions et de respecter les <strong>contraintes de volume</strong>. [En savoir plus](../orchestrated/activities/channels.md#rate-control)

* **Bouton de redémarrage** : les campagnes orchestrées comprennent désormais un <strong>bouton de redémarrage</strong> afin que vous puissiez rapidement <strong>relancer les exécutions</strong> si nécessaire avant de publier la campagne. [En savoir plus](../orchestrated/start-monitor-campaigns.md)

* **Prise en charge des métadonnées générées par l’utilisateur ou l’utilisatrice** : la <strong>fonction d’assistance executionMetadata</strong> est désormais disponible dans l’éditeur de personnalisation pour les campagnes orchestrées. Vous pouvez ainsi joindre des informations contextuelles à toute action native et les stocker dans un jeu de données pour les exporter vers des systèmes externes. [En savoir plus](../personalization/functions/helpers.md#execution-metadata)

  Date de disponibilité : mercredi 27 janvier 2026.

* **Rétablir le statut de brouillon des campagnes actives** - Vous pouvez désormais rétablir le statut de brouillon des campagnes orchestrées actives lorsqu’elles rencontrent des erreurs d’exécution ou lorsque vous devez modifier les campagnes planifiées avant qu’elles ne commencent à s’exécuter. Cette option est disponible jusqu&#39;à l&#39;envoi du premier message. [En savoir plus](../orchestrated/start-monitor-campaigns.md#back-to-draft)

#### Campagnes

* **Planification de l’opération à l’aide du fuseau horaire du profil** - La planification des opérations peut désormais utiliser le <strong>fuseau horaire</strong> de chaque profil pour diffuser les messages à l’heure locale prévue. [En savoir plus](../campaigns/campaign-schedule.md)

  **Remarque** : cette amélioration ne sera disponible que pour un ensemble d’organisations (disponibilité limitée).

  Date de disponibilité : mercredi 27 janvier 2026.

#### Autorisations

* **Empêcher l’approbation automatique pour les parcours et les campagnes** : ajout d’une option lors de la création ou de la définition de la <strong>politique d’approbation</strong> pour empêcher les créateurs et créatrices de parcours ou de campagnes d’<strong>approuver leurs propres objets</strong>. [En savoir plus](../test-approve/approval-policies.md)

  Date de disponibilité : mercredi 27 janvier 2026.

#### SMS

* **Webhooks SMS** - Les Webhooks sont désormais pris en charge sur tous les fournisseurs SMS. Vous pouvez configurer chaque webhook en fonction de son objectif, des webhooks entrants pour capturer les messages entrants et des webhooks de commentaires pour recevoir les accusés de réception de diffusion, les mises à jour de statut et d&#39;autres événements liés aux messages. [En savoir plus](../sms/sms-webhook.md)

  Date de disponibilité : mardi 2 février 2026.

<!--
## Coming soon {#jan-26-01-coming-soon}

In the next few days, the following capabilities and enhancements are scheduled for release. **Information is subject to change**. Updated links, screens, and documentation will be shared once these updates are live in production.

### Features

<table>
<thead>
<tr>
<th><strong>Content decision activity</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Content decision activity</strong> is now available in the journey canvas for integrating <strong>personalized offers</strong> directly into your customer journeys. This activity enables you to deliver decision-based content and reference those offers throughout your journey - in conditions for creating eligibility-based branching, in custom actions for passing offer data to external systems, and in other activities for building fully personalized customer experiences.</p>
<p>This capability will be available to all environments (General Availability).</p>
<p>Availability date: February 11, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Web Push notifications channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports <strong>Web Push notifications</strong>, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both <strong>mobile and desktop browsers</strong>, enabling you to reach customers directly on their devices without requiring an app. This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same authoring workflows and targeting capabilities already available for mobile push.</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>Previously released in Beta, this capability will be available to all environments (General Availability).</p>
<p>Availability date: February 11, 2026</p>
</td>
</tr>
</tbody>
</table>

### Improvements


* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach <strong>fragments</strong> to <strong>decision items</strong> which can be leveraged in code-based experience campaigns through decision policies.

  Availability date: February 11, 2026.

-->