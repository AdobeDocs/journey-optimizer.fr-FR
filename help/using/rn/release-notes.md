---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 2dd468a97b8cb696d4ad7f1d0de2aceb15da29df
workflow-type: tm+mt
source-wordcount: '1839'
ht-degree: 21%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] suit un modèle de diffusion continue, ce qui permet à Adobe de diffuser régulièrement de nouvelles fonctionnalités, de nouvelles améliorations et de nouveaux correctifs. Cette approche permet un déploiement évolutif et échelonné des fonctionnalités afin d’assurer les performances et la stabilité dans tous les environnements.

En raison de ce modèle, les notes de mise à jour sont mises à jour entre les versions mensuelles. Pour plus d’informations sur le cycle de publication et les phases de disponibilité, consultez le [cycle de publication de Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Notes de mise à jour de janvier 2026 {#latest-rn}

**Date de publication** : 27-28 janvier 2026

Les sections [Fonctionnalités](#jan-26-01-features) et [Améliorations](#jan-26-01-improv) couvrent les fonctionnalités déjà disponibles, tandis que [Bientôt disponible](#jan-26-01-coming-soon) répertorie les éléments planifiés pour une date de disponibilité ultérieure.

<!-- **The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date. 

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

### Nouvelles fonctionnalités {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>Canal de notifications push web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer prend désormais en charge les <strong>notifications push web</strong>, ce qui étend le canal push au-delà des applications mobiles. Vous pouvez diffuser facilement des notifications aux <strong>navigateurs mobiles et de bureau</strong>, ce qui vous permet d’atteindre les clients directement sur leurs appareils sans avoir besoin d’une application. Cette amélioration permet d’interagir avec les utilisateurs et utilisatrices à l’aide de messages personnalisés et opportuns en temps réel, en exploitant les mêmes workflows de création et les mêmes fonctionnalités de ciblage que ceux déjà disponibles pour les notifications push mobiles.</p>
<p><img src="assets/do-not-localize/web-push.gif"/></p>
<p>Publiée précédemment en version Beta, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).</p>
<p>Pour plus d’informations, consultez la <a href="../push/push-configuration-web.md">documentation détaillée</a>.</p>
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
<p>Le canal Courrier est désormais disponible dans les campagnes orchestrées. L’activité <strong>Publipostage direct</strong> facilite l’envoi de publipostage direct dans votre campagne orchestrée, pour les messages ponctuels et récurrents. Il permet d’automatiser le processus de génération du fichier <strong>extraction</strong> requis par les fournisseurs de publipostage direct. Vous pouvez combiner des activités de canal dans la zone de travail de campagne orchestrée afin de créer des campagnes cross-canal pouvant déclencher des actions en fonction du comportement de la clientèle et des données.</p>
<p><img src="assets/do-not-localize/dm-oc.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../orchestrated/activities/channels.md#channel">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent - Création d’un Parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Agent offre désormais des fonctionnalités de création qui permettent aux utilisateurs de Journey Optimizer de créer et de configurer des parcours marketing par le biais d’une <strong> interface en langage naturel </strong>. Grâce à ces nouvelles compétences, les praticiens peuvent rapidement créer des parcours en décrivant simplement leurs besoins dans <strong>invites conversationnelles</strong>. Cette innovation simplifie le processus de création de parcours, ce qui permet aux spécialistes marketing de se concentrer sur la stratégie plutôt que sur la configuration technique.</p>
<p>Pour plus d’informations, consultez la <a href="../start/ai-features.md#journey-agent">documentation détaillée</a>.</p>
<p>Date de disponibilité : mardi 12 janvier 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API d’extraction de campagne d’action</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une nouvelle API Journey Optimizer est désormais disponible, ce qui vous permet d’extraire et d’inspecter par programmation les données <strong>liées à la campagne</strong> telles que les détails, les versions et les configurations.</p>
<p>Pour plus d’informations, consultez la <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/" target="_blank">documentation détaillée</a>.</p>
<p>Date de disponibilité : mardi 24 novembre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Thèmes Designer des emails</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais appliquer rapidement des <strong>thèmes préapprouvés</strong> pour garantir la <strong>cohérence de la marque</strong> à tous les e-mails, accélérer le processus de création de votre campagne et produire indépendamment des e-mails de haute qualité tout en réduisant la dépendance aux équipes de conception.</p>
<p><img src="assets/do-not-localize/themes.gif"/></p>
<p>Publiée auparavant en version bêta, cette fonctionnalité est désormais disponible pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Pour plus d’informations, consultez la <a href="../email/apply-email-themes.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : jeudi 5 novembre 2025</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#jan-26-01-improv}

#### AI

* **Contrôles de qualité du contenu de l’assistant d’IA** - En plus de l’alignement de la marque, vous pouvez désormais évaluer l’ensemble <strong>qualité du contenu</strong> pour identifier les problèmes potentiels de <strong>lisibilité</strong>, de cohésion et d’efficacité, indépendamment des directives de votre marque. Ces contrôles automatisés permettent d&#39;identifier les messages peu clairs, le ton incohérent ou les lacunes structurelles. [En savoir plus](../content-management/brands-score.md#validate-quality). [Découvrez cette fonctionnalité en vidéo](https://video.tv.adobe.com/v/3470544/?learn=on).

#### Experience Decisioning

* **Joindre des fragments aux éléments de décision** - Journey Optimizer permet désormais de joindre des <strong>fragments</strong> aux <strong>éléments de décision</strong> qui peuvent être utilisés dans les campagnes d’expérience basées sur le code par le biais de politiques de décision. [En savoir plus](../experience-decisioning/items.md)

  **Remarque** : publiée précédemment en disponibilité limitée, cette amélioration est désormais disponible dans tous les environnements (disponibilité générale).

#### Parcours

* **Combiner des actions de message natives et Adobe Campaign** - Journey Optimizer vous permet désormais de combiner des actions de message <strong>Adobe Campaign v7/v8</strong> avec des actions de canal <strong>natives</strong> dans le même parcours. [En savoir plus](../building-journeys/using-adobe-campaign-v7-v8.md)

* **Payload de réponse d’erreur d’action personnalisée** - Vous pouvez désormais définir une <strong>payload de réponse d’erreur</strong> facultative pour les actions personnalisées. Lorsqu’un appel échoue, la payload d’erreur est exposée dans le contexte du parcours (sous le nœud errorResponse de l’action) et est disponible dans la branche <strong>timeout/error</strong>, avec `jo_status_code`, pour prendre en charge une logique de secours plus riche et le débogage. [En savoir plus](../action/action-response.md)

* **Validation de la taille de la payload du Parcours dans parcours** - Journey Optimizer valide désormais <strong>tailles de la payload</strong> pour garantir des performances optimales et la stabilité du système. Lors de la création ou de la publication de parcours, vous recevez des <strong>avertissements et erreurs</strong> clairs si les tailles de payload approchent ou dépassent les limites recommandées, ainsi que des conseils pratiques pour optimiser votre configuration de parcours. Cette validation proactive vous permet d’identifier rapidement les problèmes potentiels et de maintenir les performances du parcours. [En savoir plus](../start/guardrails.md#journey-payload-size)

* **Alertes de Parcours** - De nouvelles <strong>alertes préconfigurées</strong> sont disponibles pour les parcours.
   * <strong>Taux de rejet du profil dépassé</strong> - Ratio des rejets de profil par rapport aux profils entrés au cours des 5 dernières minutes ayant dépassé le seuil
   * <strong>Taux d’erreurs d’action personnalisée dépassé</strong> - Rapport entre les erreurs d’action personnalisée et les appels HTTP réussis au cours des 5 dernières minutes dépassé le seuil
   * <strong>Taux d’erreur de profil dépassé</strong> - Ratio de profils en erreur par rapport aux profils entrés au cours des 5 dernières minutes qui a dépassé le seuil

  Pour plus d’informations, consultez la [documentation détaillée](../reports/alerts.md).

  Date de disponibilité : 14 octobre 2025.

#### Campagnes orchestrées

* **Héritage des libellés d’utilisation des données pour les audiences** - Les libellés appliqués dans Adobe Experience Platform sont désormais automatiquement transférés lors de l’enregistrement des <strong>audiences</strong> dans les campagnes orchestrées, ce qui réduit le <strong>balisage DULE</strong> manuel. [En savoir plus](../orchestrated/activities/save-audience.md)

* **Filtres prédéfinis avec paramètres** - Vous pouvez désormais créer des <strong>filtres prédéfinis</strong> avec <strong>paramètres</strong> dans les campagnes orchestrées pour des règles réutilisables et modifiables. [En savoir plus](../orchestrated/predefined-filters.md)

* **Sélectionner des attributs et copier les valeurs de distribution** - Vous pouvez désormais <strong>sélectionner ou copier des valeurs</strong> directement à partir de la vue <strong>distribution des valeurs</strong> dans les campagnes orchestrées. [En savoir plus](../orchestrated/build-query.md)

* **Confirmation des messages avant l’envoi** - Une <strong>étape de confirmation</strong> est désormais activée par défaut avant l’envoi de campagnes orchestrées afin de réduire les envois accidentels. [En savoir plus](../orchestrated/activities/channels.md#confirm-message-sending)

* **Filtres de reciblage prédéfinis** - Pour prendre en charge un reciblage plus facile pour les cas d’utilisation de campagnes orchestrées, cette version introduit de nouveaux <strong>filtres de commentaires sur les campagnes</strong>. Ces filtres vous permettent de cibler directement des audiences en fonction de l’engagement du message <strong>message</strong>, par exemple, envoyé, ouvert uniquement, ouvert ou sur lequel l’utilisateur a cliqué ou ouvert et sur lequel il a cliqué, puis de sélectionner la campagne spécifique ou la campagne en transition que vous souhaitez recibler. [En savoir plus](../orchestrated/retarget.md)

* **Prise en charge du contrôle des taux** - Les campagnes orchestrées prennent désormais en charge <strong>contrôle des taux</strong> pour vous aider à rythmer les diffusions et à vous aligner sur les <strong>contraintes de volume</strong>. [En savoir plus](../orchestrated/activities/channels.md#rate-control)

* **Bouton Redémarrer** - Les campagnes orchestrées comprennent désormais un <strong>bouton de redémarrage</strong> afin que vous puissiez rapidement <strong>relancer les exécutions</strong> si nécessaire avant de publier la campagne. [En savoir plus](../orchestrated/start-monitor-campaigns.md)

* **Prise en charge des métadonnées générées par l’utilisateur** - La fonction d’assistance <strong>executionMetadata</strong> est désormais disponible dans l’éditeur de personnalisation pour les campagnes orchestrées. Vous pouvez ainsi joindre des informations contextuelles à toute action native et les stocker dans un jeu de données pour les exporter vers des systèmes externes. [En savoir plus](../personalization/functions/helpers.md#execution-metadata)

#### Autorisations

* **Empêcher l’approbation automatique pour les parcours et les campagnes** - Ajout d’une option lors de la création ou de la définition de la <strong>Politique d’approbation</strong> pour empêcher les créateurs de parcours ou de campagnes de <strong>approuver leurs propres objets</strong>. [En savoir plus](../test-approve/approval-policies.md)

## Bientôt disponible {#jan-26-01-coming-soon}

La publication des fonctionnalités et améliorations suivantes est prévue dans les prochains jours. **Les informations peuvent faire l’objet de modifications**. Les liens, les écrans et la documentation mis à jour seront partagés une fois que ces mises à jour seront en production.

### Fonctionnalités

<table>
<thead>
<tr>
<th><strong>Export de message</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une nouvelle fonctionnalité <strong>Exportation des messages</strong> est désormais disponible pour les canaux e-mail et SMS. Cette fonctionnalité vous permet d'exporter automatiquement le contenu des messages envoyés vers un jeu de données Experience Platform dédié, ce qui vous permet d'effectuer les opérations suivantes :</p>
<ul>
<li>Respect des exigences réglementaires (telles que la loi HIPAA)</li>
<li>Archiver les messages pour les réclamations juridiques et les demandes de renseignements de l'assistance clientèle</li>
<li>Conserver des copies du contenu personnalisé envoyé aux individus</li>
</ul>
<p>Les enregistrements sont conservés dans le jeu de données d’exportation de messages AJO pendant 7 jours calendaires à compter de l’ingestion. Pendant cette période de conservation, vous pouvez exporter les données vers votre propre espace de stockage via les destinations Experience Platform. La fonctionnalité est activée au niveau de la configuration du canal, ce qui vous permet <strong>un contrôle granulaire</strong> sur les messages exportés.</p>
<p>Cette fonctionnalité est disponible uniquement pour les canaux e-mail et SMS, pour les organisations qui ont acheté l’offre de module complémentaire Exportation de messages . Pour en savoir plus, contactez votre représentant Adobe.</p>
<p>Date de disponibilité : jeudi 28 janvier 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal courrier dans parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Auparavant limité aux campagnes, le canal <strong>Publipostage direct</strong> est désormais disponible sur la zone de travail du parcours, ce qui vous permet d’incorporer le publipostage direct dans vos parcours. Le publipostage direct peut désormais être utilisé dans les scénarios <strong>par lots et de parcours 1:1</strong>, avec la prise en charge de la configuration de l’extraction de fichiers et des paramètres de fréquence temporels.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité sera disponible pour tous les environnements (disponibilité générale).</p>
<p>Date de disponibilité : jeudi 28 janvier 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Heures calmes (exclusions temporelles)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les <strong>heures de silence</strong> vous permettent de définir des exclusions temporelles pour les canaux E-mail, SMS, Notification push et WhatsApp. Ils garantissent qu’aucun message n’est envoyé pendant des périodes spécifiques, ce qui vous aide à respecter les préférences des clients et les exigences de conformité. Vous pouvez appliquer des heures creuses par le biais d’<strong>ensembles de règles</strong> qui peuvent être affectés à des actions individuelles dans des campagnes ou des parcours pour un contrôle précis.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements. Avec cette version de disponibilité générale, la fonctionnalité permet désormais au client de mettre en file d’attente une action de campagne jusqu’à la fin des heures creuses et de prévisualiser la règle des heures creuses activée.</p>
<p>Date de disponibilité : jeudi 28 janvier 2026</p>
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
<p>Les <strong>API d’outil de migration</strong> sont désormais disponibles pour migrer par programmation les entités de gestion des décisions vers la prise de décision, et comprennent :</p>
<ul>
<li>Portées de migration flexibles (sandbox, offre ou niveau de décision)</li>
<li>Analyse et validation automatisées des dépendances</li>
<li>Prise en charge de la restauration pour les migrations terminées</li>
<li>Rapports de migration détaillés avec les mappages d’objet</li>
</ul>
<p>Date de disponibilité : jeudi 28 janvier 2026</p>
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
<p>Renseignez davantage insight sur l’intégrité et les performances de vos points d’entrée d’action personnalisés <strong>custom action</strong> avec un nouveau tableau de bord de surveillance et des données d’événement d’étape de parcours enrichies. Effectuez le suivi des appels réussis, des erreurs, du débit, des temps de réponse et des temps d’attente de la file d’attente pour comprendre rapidement quand, où et pourquoi des anomalies se produisent.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<p>Date de disponibilité : jeudi 28 janvier 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Prise en charge de la prise de décision dans les canaux push et SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais personnaliser et optimiser le contenu de vos messages <strong>push et SMS</strong> avec <strong>Decisioning</strong>. Utilisez des scores de priorité, des formules ou des modèles d’IA pour afficher le meilleur contenu à vos clients.</p>
<p>Date de disponibilité : mercredi 3 février 2026</p>
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
<p>Une nouvelle <strong>activité de décision de contenu</strong> est désormais disponible dans la zone de travail du parcours pour intégrer <strong>offres personnalisées</strong> directement dans vos parcours clients. Cette activité vous permet de diffuser du contenu basé sur des décisions et de référencer ces offres dans l’ensemble de votre parcours, dans des conditions de création d’embranchements basés sur l’éligibilité, dans des actions personnalisées pour transmettre des données d’offre à des systèmes externes et dans d’autres activités pour créer des expériences client entièrement personnalisées.</p>
<p>Cette fonctionnalité sera disponible dans tous les environnements (disponibilité générale).</p>
<p>Date de disponibilité : mercredi 3 février 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Génération de contenu dans Journey Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Optimisé par Adobe Experience Platform Agent Orchestrator, <strong>Journey Agent</strong> est disponible dans Journey Optimizer et vous permet d’analyser les parcours par le biais d’une interface en langage naturel. Vous pouvez désormais également <strong>générer et gérer du contenu</strong> directement dans Journey Agent, créer du contenu pour des canaux tels que les e-mails et les notifications push, appliquer et prévisualiser des modèles, affiner le ton et le style à l’aide d’invites et ouvrir le contenu dans Content Designer pour une modification contextuelle.</p>
<p>Date de disponibilité : mardi 2 février 2026</p>
</td>
</tr>
</tbody>
</table>

### Améliorations

* **Planification de l’opération à l’aide du fuseau horaire du profil** - La planification des opérations peut désormais utiliser le <strong>fuseau horaire</strong> de chaque profil pour diffuser les messages à l’heure locale prévue.

  **Remarque** : cette amélioration ne sera disponible que pour un ensemble d’organisations (disponibilité limitée).

  Date de disponibilité : 28 janvier 2026.

* **Webhooks SMS** - <strong>Webhooks</strong> sont désormais pris en charge sur tous les fournisseurs de SMS. Vous pouvez configurer chaque webhook en fonction de son objectif, des webhooks entrants pour capturer les messages entrants et des webhooks de commentaires pour recevoir les accusés de réception de diffusion, les mises à jour de statut et d&#39;autres événements liés aux messages.

  Date de disponibilité : 28 janvier 2026.
