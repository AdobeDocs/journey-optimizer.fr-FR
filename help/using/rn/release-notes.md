---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 9dedefb30a6c61965595a102c2d02207ae620285
workflow-type: tm+mt
source-wordcount: '2015'
ht-degree: 28%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] suit un modèle de diffusion continue, ce qui permet à Adobe de diffuser régulièrement de nouvelles fonctionnalités, de nouvelles améliorations et de nouveaux correctifs. Cette approche permet un déploiement évolutif et échelonné des fonctionnalités afin d’assurer les performances et la stabilité dans tous les environnements.

En raison de ce modèle, les notes de mise à jour sont mises à jour entre les versions mensuelles. Pour plus d’informations sur le cycle de publication et les phases de disponibilité, consultez le [cycle de publication de Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Notes de mise à jour préliminaires du 26 janvier {#latest-rn}

**Date de publication** : mercredi 27 janvier 2026

**Les notes de version préliminaire ci-dessous peuvent être modifiées sans préavis jusqu’à la date de publication**. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les notes de mise à jour, à la date de publication.

Voir également les [Notes de mise à jour préliminaires d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

### Nouvelles fonctionnalités {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>Activité d’action dans les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer prend en charge une nouvelle <strong>activité d’action</strong> générique qui vous permet de configurer des actions uniques et des <strong>groupes d’actions entrants à actions multiples</strong>, ce qui permet d’optimiser la configuration des actions dans la zone de travail du parcours. Cette nouvelle fonctionnalité permet notamment les opérations suivantes :</p>
<ul>
<li>Configuration d’action native simplifiée dans la zone de travail de parcours</li>
<li>Création de groupes d’actions entrantes multi-actions</li>
<li>Ajout d’une optimisation à toute action de canal intégrée</li>
<li>Possibilité d’ajouter des options d’expérimentation et multilingues à n’importe quelle action</li>
</ul>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
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
<p>Renseignez davantage insight sur l’intégrité et les performances de vos points d’entrée d’action personnalisés grâce à un nouveau <strong>tableau de bord de surveillance</strong> et à des données d’événement d’étape de parcours enrichies. Effectuez le suivi des appels réussis, des erreurs, du débit, des temps de réponse et des temps d’attente de la file d’attente pour comprendre rapidement quand, où et pourquoi des anomalies se produisent.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Heures creuses/exclusions basées sur l’heure</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les heures calmes vous permettent de définir des <strong>exclusions temporelles</strong> pour les canaux e-mail, SMS, notification push et WhatsApp. Ils garantissent qu’aucun message n’est envoyé pendant des périodes spécifiques, ce qui vous aide à respecter les préférences des clients et les exigences de conformité. Vous pouvez appliquer des heures creuses par le biais d’<strong>ensembles de règles</strong> qui peuvent être affectés à des actions individuelles dans des campagnes ou des parcours pour un contrôle précis.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements. Avec cette version de disponibilité générale, la fonctionnalité permet désormais au client de mettre en file d’attente une action de campagne jusqu’à la fin des heures creuses et de prévisualiser la règle des heures creuses activée.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal Courrier dans parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Auparavant limité aux campagnes, le canal <strong>publipostage direct</strong> est désormais disponible sur la zone de travail de parcours <strong></strong>, ce qui vous permet d’incorporer le publipostage direct dans vos parcours. Le publipostage direct peut désormais être utilisé dans les scénarios de lot et de parcours 1:1, avec la prise en charge de la configuration de l’extraction de fichiers et des paramètres de fréquence basés sur le temps.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
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
<p>Adobe Journey Optimizer prend désormais en charge les <strong>notifications push web</strong>, ce qui étend le canal push au-delà des applications mobiles. Vous pouvez diffuser facilement des notifications aux navigateurs mobiles et de bureau, ce qui vous permet d’atteindre les clients directement sur leurs appareils sans avoir besoin d’une application. Cette amélioration permet d’interagir avec les utilisateurs et utilisatrices à l’aide de messages personnalisés et opportuns en temps réel, en exploitant les mêmes workflows de création et les mêmes fonctionnalités de ciblage que ceux déjà disponibles pour les notifications push mobiles.</p>
<p>Publiée précédemment en version Beta, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).</p>
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
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Exportation de messages</strong><br/></th>
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
<p>Les enregistrements sont conservés dans le jeu de données d’exportation de messages AJO pendant 7 jours calendaires <strong> à compter de l’ingestion</strong>. Pendant cette période de conservation, vous pouvez exporter les données vers votre propre espace de stockage via les destinations Experience Platform. La fonctionnalité est activée au niveau de la configuration des canaux, ce qui vous permet de contrôler de manière granulaire les messages exportés.</p>
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
<p>Un nouvel ensemble d’<strong>API d’outils de migration</strong> est disponible pour migrer les entités de gestion des offres vers Experience Decisioning. Cet outil permet une migration transparente entre les sandbox avec des fonctionnalités de résolution de dépendance et de restauration.</p>
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
<p>L’agent de création de parcours permet aux utilisateurs de Journey Optimizer de créer et de configurer des parcours marketing à l’aide d’une interface en langage naturel. Avec l’agent de création de Parcours, les utilisateurs et utilisatrices peuvent rapidement créer des parcours en décrivant leurs besoins dans des invites conversationnelles. L’agent simplifie la création de parcours, ce qui permet aux spécialistes du marketing de se concentrer sur la stratégie plutôt que sur la configuration technique.</p>
<p><a href="https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent#journey-create-agent-skill-overview-and-user-guide" target="_blank">En savoir plus</a></p>
<p>Date de disponibilité : mardi 12 janvier 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nouvelle API pour récupérer les campagnes d’action</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une nouvelle API <strong>Journey Optimizer</strong> est désormais disponible, ce qui vous permet de récupérer et d’inspecter par programmation les données liées à la campagne, telles que les détails, les versions et les configurations.</p>
<p>Pour plus d’informations, consultez la <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">documentation détaillée</a>.</p>
<p>Date de disponibilité : mardi 24 novembre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nouvelles alertes de parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Trois nouvelles alertes de parcours <strong></strong> sont désormais disponibles pour vous aider à surveiller et à suivre les événements de cycle de vie des parcours et les performances des actions personnalisées :</p>
<ul>
<li><strong>Parcours publié</strong> : recevez des notifications lorsqu’un parcours est publié par un utilisateur ou une utilisatrice dans la zone de travail du parcours.</li>
<li><strong>Parcours terminé</strong> : recevez des alertes lorsqu’un parcours est terminé, avec des définitions spécifiques en fonction du type de parcours (Lecture d’audience ou Déclenché par un événement).</li>
<li><strong>Limitation d’action personnalisée déclenchée</strong> : recevez une notification lorsque la limitation est activée sur un point d’entrée d’action personnalisée.</li>
</ul>
<p>Il est possible de s’abonner à ces alertes au niveau de l’organisation ou pour des parcours spécifiques.</p>
<p>Pour plus d’informations, consultez la <a href="../reports/alerts.md#journey-alerts">documentation détaillée</a>.</p>
<p>Date de disponibilité : jeudi 5 novembre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Thèmes dans le concepteur d’e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais appliquer rapidement des <strong>thèmes préapprouvés</strong> pour garantir la cohérence de la marque dans tous les e-mails, accélérer le processus de création de votre campagne et produire indépendamment des e-mails de haute qualité tout en réduisant la dépendance aux équipes de conception.</p>
<p>Publiée auparavant en version bêta, cette fonctionnalité est désormais disponible pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Pour plus d’informations, consultez la <a href="../email/apply-email-themes.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : jeudi 5 novembre 2025</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#jan-26-01-improv}

Les améliorations de cette version sont présentées ci-dessous.

#### AI

* **Contrôles de qualité du contenu de l’assistant d’IA** - En plus de l’alignement de la marque, vous pouvez désormais évaluer la <strong>qualité du contenu</strong> globale pour identifier les problèmes potentiels de lisibilité, de cohésion et d’efficacité, indépendamment des directives de votre marque. Ces contrôles automatisés permettent d&#39;identifier les messages peu clairs, le ton incohérent ou les lacunes structurelles.

* **Mettre à jour les marques avec un nouvel onglet de couleur** - Les directives relatives à la marque permettent de s’assurer que votre marque est présentée de manière cohérente à tous les points de contact. La nouvelle <strong>section Couleurs</strong> définit les normes du système de couleurs de votre marque et décrit comment les couleurs sont sélectionnées, organisées et appliquées à travers les expériences. Il garantit une utilisation cohérente des couleurs primaires, secondaires, d’accentuation et neutres pour prendre en charge une identité de marque cohérente, accessible et reconnaissable.

#### Canaux

* **Webhooks SMS** - Les Webhooks sont désormais pris en charge sur tous les fournisseurs SMS. Vous pouvez configurer chaque webhook en fonction de son objectif, des webhooks entrants pour capturer les messages entrants et des webhooks de commentaires pour recevoir les accusés de réception de diffusion, les mises à jour de statut et d&#39;autres événements liés aux messages.

#### Campagnes

* **Planification de l’opération à l’aide du fuseau horaire du profil** - La planification des opérations peut désormais utiliser le <strong>fuseau horaire</strong> de chaque profil pour diffuser les messages à l’heure locale prévue.

  **Remarque** : cette amélioration est disponible uniquement pour un ensemble d’organisations (disponibilité limitée).


#### Experience Decisioning

* **Joindre des fragments aux éléments de décision** - Journey Optimizer permet désormais de joindre des <strong>fragments</strong> aux éléments de décision qui peuvent être utilisés dans les campagnes d’expérience basées sur le code par le biais de politiques de décision.

  **Remarque** : publiée précédemment en disponibilité limitée, cette amélioration est désormais disponible dans tous les environnements (disponibilité générale).

#### Parcours

* **Tirer parti d’une payload de réponse d’erreur dans des actions personnalisées de parcours** - Vous pouvez désormais définir une <strong>payload de réponse d’erreur</strong> facultative pour les actions personnalisées. Lorsqu’un appel échoue, la payload d’erreur est exposée dans le contexte du parcours et est disponible dans la branche temporisation/erreur pour prendre en charge une logique de secours plus riche et le débogage.

* **Combiner des actions de message natives et Adobe Campaign** - Journey Optimizer vous permet désormais de combiner des actions de message Adobe Campaign v7/v8 avec des actions de canal natives dans le même parcours.

* **Validation de la taille de la payload du Parcours dans parcours** - Journey Optimizer valide désormais les tailles de payload du parcours pour garantir des performances optimales et la stabilité du système. Lors de la création ou de la publication de parcours, vous recevez des avertissements et des erreurs clairs si les tailles de payload approchent ou dépassent les limites recommandées, ainsi que des conseils pratiques pour optimiser votre configuration de parcours. Cette validation proactive vous permet d’identifier rapidement les problèmes potentiels et de maintenir les performances du parcours.

* **Plusieurs actions entrantes dans les parcours** - Pour simplifier votre orchestration des parcours, vous pouvez désormais définir <strong>plusieurs actions entrantes</strong> dans un seul parcours. Précédemment disponible dans les campagnes, cette fonctionnalité vous permet de diffuser simultanément plusieurs expériences basées sur du code, des messages in-app, des cartes de contenu ou des actions web à différents emplacements, chaque action contenant un contenu spécifique.

  **Remarque** : publiée précédemment en disponibilité limitée, cette amélioration est désormais disponible dans tous les environnements (disponibilité générale).

#### Campagnes orchestrées

* **Sélectionner des attributs et copier les valeurs de distribution** - Vous pouvez désormais sélectionner ou copier des valeurs directement à partir de la vue de distribution des valeurs dans les campagnes orchestrées.

* **Héritage des libellés d’utilisation des données pour les audiences** - Les libellés appliqués dans Adobe Experience Platform sont désormais automatiquement transférés lors de l’enregistrement des audiences dans les campagnes orchestrées, ce qui réduit le balisage DULE manuel.

* **Filtres de reciblage prédéfinis** - Pour prendre en charge un reciblage plus facile pour les cas d’utilisation de campagnes orchestrées, cette version introduit de nouveaux <strong>filtres de commentaires sur les campagnes</strong>. Ces filtres vous permettent de cibler directement les audiences en fonction de l’engagement du message, par exemple envoyé, ouvert uniquement, ouvert ou sur lequel vous avez cliqué, ou ouvert et cliqué, et de sélectionner la campagne spécifique ou la campagne en transition à recibler.

* **Filtres prédéfinis avec paramètres** - Vous pouvez désormais créer des <strong>filtres avec paramètres</strong> dans les campagnes orchestrées pour des règles réutilisables et modifiables.

* **Confirmation des messages avant l’envoi** - Une <strong>étape de confirmation</strong> est désormais activée par défaut avant l’envoi de campagnes orchestrées afin de réduire les envois accidentels.

* **Prise en charge des métadonnées générées par l’utilisateur** - La fonction d’assistance <strong>executionMetadata</strong> est désormais disponible dans l’éditeur de personnalisation pour les campagnes orchestrées. Vous pouvez ainsi joindre des informations contextuelles à toute action native et les stocker dans un jeu de données pour les exporter vers des systèmes externes.

* **Bouton Redémarrer** - Les campagnes orchestrées comprennent désormais un <strong>bouton de redémarrage</strong> afin que vous puissiez rapidement relancer les exécutions, si nécessaire, avant de publier la campagne.

* **Prise en charge du contrôle des taux** - Les campagnes orchestrées prennent désormais en charge <strong>contrôle des taux</strong> pour vous aider à rythmer les diffusions et à vous aligner sur les contraintes de volume.

#### Autorisations

* **Empêcher l’approbation automatique pour les parcours et les campagnes** - Ajout d’une option lors de la création ou de la définition de la stratégie d’approbation pour empêcher les créateurs de Parcours/campagnes de valider leurs propres objets.

## Bientôt disponible {#jan-26-01-coming-soon}

La publication des fonctionnalités et améliorations suivantes est prévue dans les prochains jours. **Les informations peuvent faire l’objet de modifications**. Les liens, les écrans et la documentation mis à jour seront partagés une fois que ces mises à jour seront en production.

<table>
<thead>
<tr>
<th><strong>Génération de contenu dans Journey Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Optimisé par Adobe Experience Platform Agent Orchestrator, <strong>Journey Agent</strong> est disponible dans Journey Optimizer et vous permet d’analyser les parcours par le biais d’une interface en langage naturel. Vous pouvez désormais également générer et gérer du contenu spécifique à un canal directement dans Journey Agent, ce qui permet de créer du contenu pour des canaux tels que les e-mails et les notifications push, d’appliquer et de prévisualiser des modèles, d’affiner le ton et le style via des invites et d’ouvrir le contenu dans Content Designer pour le modifier en contexte.</p>
<p>Date de disponibilité : mardi 2 février 2026</p>
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
<p>Vous pouvez désormais personnaliser et optimiser le contenu de vos messages push avec <strong>Decisioning</strong>. Utilisez des <strong>scores de priorité</strong>, des formules ou des modèles d’IA pour afficher le meilleur contenu à l’intention de vos clients.</p>
<p>Date de disponibilité : mercredi 3 février 2026</p>
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
<p>Vous pouvez désormais ajouter des politiques de décision dans les parcours et campagnes SMS. Les politiques de décision sont des conteneurs pour vos offres qui tirent profit du moteur de prise de décision afin d’effectuer un rendu dynamique du meilleur contenu à diffuser, pour chaque membre de l’audience.</p>
<p>Cette fonctionnalité est disponible en disponibilité limitée pour un ensemble d’organisations.</p>
<p>Date de disponibilité : mercredi 3 février 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Activité Décision de contenu</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais inclure des <strong>offres personnalisées</strong> dans vos parcours par le biais d’une activité de décision de contenu dédiée dans la zone de travail de parcours, et les utiliser dans des activités de parcours, y compris des conditions et des actions personnalisées.</p>
<p>Cette fonctionnalité sera disponible dans tous les environnements (disponibilité générale).</p>
<p>Date de disponibilité : mercredi 3 février 2026</p>
</td>
</tr>
</tbody>
</table>
