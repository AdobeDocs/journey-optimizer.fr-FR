---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour 2026
description: Notes de mise à jour de 2026 pour Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 65ca94cf-8e17-4a25-90f3-238083f81477
source-git-commit: b6b74e357029f4924f9699c05af3a0fcd7fcefd6
workflow-type: tm+mt
source-wordcount: '2573'
ht-degree: 64%

---

# Notes de mise à jour 2026 {#release-notes-2026}

Cette page répertorie toutes les fonctionnalités et améliorations pour [!DNL Journey Optimizer] publiées en 2026.



## Notes de mise à jour de février 2026 {#feb-26-01-rn}

### Nouvelles fonctionnalités {#feb-26-01-features}


<table>
<thead>
<tr>
<th><strong>arbitrage de parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais utiliser des <strong>formules de classement</strong> pour améliorer automatiquement les scores de priorité des parcours en fonction des attributs de profil client et des facteurs contextuels, afin que les clients puissent accéder aux parcours les plus pertinents.</p>
<p><img src="assets/do-not-localize/journey-arbitration-formulas.gif"/></p>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Pour plus d’informations, consultez la <a href="../conflict-prioritization/journey-ranking-formulas.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : mercredi 24 février 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Activité d’action dans les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer prend en charge une nouvelle <strong>activité d’action</strong> générique qui vous permet de configurer des actions uniques et des groupes d’actions entrants multi-actions, ce qui permet une configuration d’action rationalisée dans la zone de travail de parcours. Cette nouvelle fonctionnalité permet notamment les opérations suivantes :</p>
<ul>
<li>Configuration d’action native simplifiée dans la zone de travail de parcours</li>
<li>Création de groupes d’actions entrantes multi-actions</li>
<li>Ajout d’une optimisation à toute action de canal intégrée</li>
<li>Possibilité d’ajouter des options d’expérimentation et multilingues à n’importe quelle action.</li>
</ul>
<p><img src="assets/do-not-localize/action-activity.gif"/></p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/journey-action.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : samedi 20 février 2026</p>
<p><strong>Remarque :</strong> tous les canaux natifs sont désormais accessibles via l'activité parcours d'action . Les activités de canal natives héritées seront abandonnées avec la version de mars. Les parcours existants qui incluent des actions héritées continueront à fonctionner en l’état. Aucune migration n’est requise.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Vague d’envoi des messages sortants</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais planifier la diffusion des messages des campagnes ou des parcours Journey Optimizer par lots contrôlés dans le temps.</p>
<p>L’envoi de vagues offre les avantages suivants :</p>
<ul>
<li>Meilleure délivrabilité : la diffusion des envois au fil du temps contribue à maintenir une bonne réputation des expéditeurs et réduit le risque d'être marqué comme spam.</li>
<li>Contrôle de la charge - Évitez de surcharger les systèmes en aval (par exemple les centres d’appels, les pages de destination) en limitant le nombre de messages diffusés en même temps.</li>
<li>Cas d’utilisation importants et sensibles au facteur temps : adaptés aux audiences importantes ou lorsque vous devez contrôler le timing (par exemple, capacité du centre d’appel, montée en réputation ou offres limitées dans le temps).</li>
</ul>
<p><img src="assets/do-not-localize/waves.gif"/></p>
<p>Dans les <strong>campagnes</strong>, cette fonctionnalité est disponible dans tous les environnements (Disponibilité générale). Pour plus d’informations, consultez la <a href="../campaigns/send-using-waves.md">documentation détaillée</a>.</p>

<p>Dans <strong></strong>, cette fonctionnalité n’est disponible que pour un ensemble d’organisations (disponibilité limitée). Pour y accéder, contactez votre représentant ou représentante Adobe. Pour plus d’informations, consultez la <a href="../building-journeys/send-using-waves.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : vendredi 19 février 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Migration des sous-domaines vers la délégation personnalisée</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais migrer les sous-domaines à l’aide du mode de délégation CNAME vers la délégation personnalisée directement à partir de l’interface, afin de pouvoir respecter des politiques de sécurité plus strictes conformément aux directives de votre entreprise sans recréer de configurations de canal.</p>
<p><img src="assets/do-not-localize/subdomain-migration.gif"/></p>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Pour plus d’informations, consultez la <a href="../configuration/custom-subdomain-migration.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : vendredi 19 février 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de notifications push web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer prend désormais en charge les <strong>notifications push web</strong>, ce qui étend le canal push au-delà des applications mobiles. Vous pouvez facilement diffuser des notifications vers les <strong>navigateurs mobiles et de bureau</strong>, ce qui vous permet d’atteindre les clientes et clients directement sur leurs appareils sans avoir besoin d’une application. Cette amélioration permet d’interagir avec les utilisateurs et utilisatrices à l’aide de messages personnalisés et opportuns en temps réel, en utilisant les mêmes workflows de création et les mêmes fonctionnalités de ciblage que ceux déjà disponibles pour les notifications push mobiles.</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>Publiée précédemment dans Beta, cette fonctionnalité sera disponible pour tous les environnements (disponibilité générale).</p>
<p>Pour plus d’informations, consultez la <a href="../push/push-configuration-web.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : samedi 13 février 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Activité de décision de contenu</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une nouvelle <strong>activité de décision de contenu</strong> est désormais disponible dans la zone de travail du parcours pour intégrer des offres personnalisées directement dans vos parcours clients. Cette activité vous permet de diffuser du contenu basé sur des décisions et de référencer ces offres dans l’ensemble de votre parcours, dans des conditions de création d’embranchements basés sur l’éligibilité, dans des actions personnalisées pour transmettre des données d’offre à des systèmes externes et dans d’autres activités pour créer des expériences client entièrement personnalisées.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/content-decision.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : mercredi 10 février 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API d’outils de migration en libre-service</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les API d’outils de migration sont désormais disponibles pour migrer par programmation des entités <strong>Gestion des décisions</strong> vers <strong>Prise de décision</strong>, avec les fonctionnalités suivantes :</p>
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
<p>Renseignez davantage insight sur l’intégrité et les performances de vos points d’entrée d’action personnalisés grâce à un nouveau tableau de bord de surveillance et à des données d’événement d’étape de parcours enrichies. Effectuez le suivi des appels réussis, des erreurs, du débit, des temps de réponse et des temps d’attente de la file d’attente pour comprendre rapidement quand, où et pourquoi des anomalies se produisent.</p>
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
<p>Vous pouvez désormais personnaliser et optimiser le contenu de vos SMS avec Decisioning. Utilisez des scores de priorité, des formules ou des modèles d’IA pour afficher le meilleur contenu à vos clientes et clients.</p>
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/create-decision.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 2 février 2026</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#feb-26-01-improv}

Les améliorations de cette version sont présentées ci-dessous.

#### Configuration

* **Utilisation des événements d’expérience dans les expressions de parcours** - À compter du 1er avril 2026, l’utilisation des attributs d’événement d’expérience dans les expressions de parcours ne sera plus prise en charge pour les organisations qui n’ont pas utilisé cette fonctionnalité au cours des 90 derniers jours. Cette fonctionnalité n’est déjà plus disponible pour les nouvelles organisations clientes depuis le 8 juillet 2025. Pour obtenir des alternatives, consultez [Recherche d’événement d’expérience dans les parcours &#x200B;](../building-journeys/exp-event-lookup.md).

#### Gestion de contenu

<!--
* **Update brands with new color tab** - Brand guidelines help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors</strong> section defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity. [Read more](../content-management/brands.md)
-->

* **Utiliser des thèmes pour convertir des images en modèles d’e-mail** - Lors de la conversion d’une image en modèle d’e-mail dans Journey Optimizer, vous pouvez désormais utiliser un thème comme entrée afin que l’HTML générée suive les paramètres de votre marque. Les styles tels que la couleur d’arrière-plan, la couleur du bouton, les polices, l’espacement des lignes, les marges et la marge intérieure sont appliqués automatiquement, ce qui réduit le travail de conception manuel et fournit un modèle prêt à l’emploi avec un minimum de modifications. [En savoir plus](../content-management/image-to-html.md)

  Date de disponibilité : 17 février 2026.

<!--* **Text mode for fragments** - You can now create and manage text versions of your fragments, supporting workflows that rely on plain text content and providing the same flexibility as in email content. [Read more](../content-management/create-fragments.md)-->

#### Concepteur d’e-mail

* **Retrait de texte** - Vous pouvez désormais appliquer un retrait de gauche personnalisable à la première ligne des paragraphes des composants de texte directement à partir du panneau des propriétés. <!--The new **Indentation** control lets you define indentation in pixels or percentage via a numeric input or slider, with live preview on the canvas. --> Cela améliore la lisibilité du contenu de forme longue tel que les éditoriaux et les articles. [En savoir plus](../email/get-started-email-style.md)

  Date de disponibilité : 18 février 2026.

#### Prise de décision

* **Prise en charge entrante d’Edge pour l’utilisation des données Adobe Experience Platform dans la prise de décision** - L’utilisation des données Adobe Experience Platform dans la prise de décision prend désormais en charge les cas d’utilisation entrants Edge, en plus des e-mails et des actions personnalisées dans les parcours. [En savoir plus](../experience-decisioning/aep-data-exd.md)

  Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.

* **Aperçu de la prise de décision dans le canal d’expérience basé sur le code** - Vous pouvez désormais prévisualiser les éléments de décision lors de la configuration de la prise de décision avec le canal d’expérience basé sur le code. L’aperçu est disponible directement dans l’interface de création avant la mise en ligne. [En savoir plus](../code-based/test-code-based.md#preview-code-based)

  Date de disponibilité : jeudi 18 février 2026

* **Joindre des fragments aux éléments de décision** : Journey Optimizer permet désormais de joindre des fragments aux éléments de décision qui peuvent être utilisés dans les campagnes d’expérience basées sur du code par le biais de politiques de décision. [En savoir plus](../experience-decisioning/fragments-decision-policies.md)

  Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).

  Date de disponibilité : 12 février 2026.

#### Personnalisation

* **Assistant d’exécution des métadonnées** - La fonction d’assistance `executionMetadata` est désormais disponible pour tous les clients Journey Optimizer. Utilisez-le pour ajouter de manière dynamique des informations contextuelles à toute action native et pour les capturer dans un jeu de données en vue de les exporter vers des systèmes externes. [En savoir plus](../personalization/functions/helpers.md#execution-metadata)

  Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).

  Date de disponibilité : 20 février 2026.

#### SMS

* **Webhooks SMS** - Les Webhooks sont désormais pris en charge sur tous les fournisseurs SMS. Vous pouvez configurer chaque webhook en fonction de son objectif : webhooks entrants pour capturer les messages entrants et webhooks Retours pour recevoir les accusés de réception de diffusion, les mises à jour de statut et d&#39;autres événements liés aux messages. [En savoir plus](../sms/sms-webhook.md)

  Date de disponibilité : 2 février 2026.



## Notes de mise à jour de janvier 2026 {#jan-26-rn}

<!--**Release date**: January 27-28, 2026-->

### Nouvelles fonctionnalités {#jan-26-01-features}


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
