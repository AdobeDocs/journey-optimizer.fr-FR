---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour préliminaires pour Journey Optimizer
description: Notes de mise à jour préliminaires pour Adobe Journey Optimizer
feature: Release Notes
hide: true
hidefromtoc: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: 86bd616a9331c5225c78ccf52c5d26a063fa8654
workflow-type: tm+mt
source-wordcount: '2080'
ht-degree: 31%

---

# Notes de version préliminaire {#e-release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations des fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées à la fin de chaque mois dans les [notes de mise à jour](release-notes.md).


## Notes de pré-version du 26 janvier &#39;26 {#jan-26-01-rn}

**Les notes de version préliminaire ci-dessous peuvent être modifiées sans préavis jusqu’à la date de publication**. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les notes de mise à jour, à la date de publication.

Voir également les [Notes de mise à jour préliminaires d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Date de publication** : mardi 26 janvier 2026

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
<p>Journey Optimizer prend en charge une nouvelle activité d’action générique <strong>qui vous permet de configurer à la fois des actions uniques et </strong>des groupes<strong> d’actions entrantes multi-actions, ce qui permet une configuration d’action rationalisée dans le canevas du parcours.</strong> Cette nouvelle fonctionnalité permet notamment les opérations suivantes :</p>
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
<p>Obtenez des informations plus approfondies sur l’intégrité et les performances de vos points de terminaison d’action personnalisés avec un nouveau <strong>tableau de bord</strong> de surveillance et des données enrichies d’événements d’étape de parcours. Suivez les appels réussis, les erreurs, le débit, les temps de réponse et les temps d’attente des files d’attente pour comprendre rapidement quand, où et pourquoi les anomalies se produisent.</p>
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
<p>Les heures calmes vous permettent de définir <strong>des exclusions basées sur le temps pour les</strong> canaux Email, SMS, Push et WhatsApp. Ils garantissent qu’aucun message n’est envoyé pendant des périodes spécifiques, ce qui vous aide à respecter les préférences des clients et les exigences de conformité. Vous pouvez appliquer des heures creuses par le biais d’<strong>ensembles de règles</strong> qui peuvent être affectés à des actions individuelles dans des campagnes ou des parcours pour un contrôle précis.</p>
<p>Auparavant disponible en disponibilité limitée, cette fonctionnalité est désormais disponible pour tous les environnements. Avec cette version de disponibilité générale, la fonctionnalité inclut désormais la possibilité pour le client de mettre en file d’attente une action de campagne jusqu’à la fin des heures de silence, et la possibilité de prévisualiser la règle des heures de silence activée.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal courrier dans les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Auparavant limité aux campagnes, le <strong>canal</strong> Courrier est désormais disponible sur le canevas<strong> du parcours, ce qui vous permet d’intégrer le </strong>publipostage dans vos parcours. Direct Mail peut désormais être utilisé dans les scénarios de parcours par lots et 1:1, avec la prise en charge de la configuration de l’extraction de fichiers et des paramètres de fréquence basés sur le temps.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal de notifications push Web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer prend désormais en charge <strong>les notifications</strong> push Web, étendant ainsi le canal push au-delà du mobile. Vous pouvez envoyer des notifications de manière transparente aux navigateurs mobiles et de bureau, ce qui vous permet d’atteindre les clients directement sur leurs appareils sans avoir besoin d’une application. Cette amélioration permet d’interagir avec les utilisateurs et utilisatrices à l’aide de messages personnalisés et opportuns en temps réel, en exploitant les mêmes workflows de création et les mêmes fonctionnalités de ciblage que ceux déjà disponibles pour les notifications push mobiles.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Messagerie de base RCS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Avec la nouvelle <strong>offre complémentaire RCS Basic</strong> , vous pouvez désormais diffuser la messagerie RCS (Rich Communication Services) de base dans Journey Optimizer, activant les fonctionnalités de messagerie améliorées suivantes sous réserve de la prise en charge du fournisseur et de l’opérateur :</p>
<ul>
<li>Prise en charge des expéditeurs de marque vérifiés : envoyez des messages à l’aide de profils métier vérifiés avec des éléments de branding (logo, nom de l’expéditeur, etc.).</li>
<li>Informations sur la diffusion des messages : recevez des rapports de diffusion détaillés comprenant les mises à jour du statut des messages (par exemple, envoyé, diffusé, lu).</li>
<li>Suivi des liens : incorporez et suivez les URL dans les messages RCS pour l’analyse de l’engagement.</li>
<li>Basculement vers les SMS : basculement automatique vers les SMS lorsque l’appareil du profil ne prend pas en charge RCS ou est temporairement inatteignable via RCS.</li>
<li>Composition de message de base : envoyez des messages RCS textuels de base.</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Aide à la décision dans les canaux Push et SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais ajouter <strong>des stratégies</strong> de décision aux campagnes push et SMS. Les politiques de décision sont des conteneurs pour vos offres qui tirent profit du moteur de prise de décision afin d’effectuer un rendu dynamique du meilleur contenu à diffuser, pour chaque membre de l’audience.</p>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
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
<p>Le canal Courrier est désormais disponible dans les campagnes orchestrées. L’activité <strong></strong> Courrier facilite publipostage’envoi au sein de votre campagne orchestrée, pour les messages ponctuels et récurrents. Il sert à automatiser le processus de génération <strong>du fichier</strong> d’extraction requis par publipostage fournisseurs. Vous pouvez combiner des activités de canal dans la zone de travail de campagne orchestrée afin de créer des campagnes cross-canal pouvant déclencher des actions en fonction du comportement de la clientèle et des données.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Formulaires personnalisés de la page de destination</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Avec Journey Optimizer, vous pouvez désormais capturer <strong>les attributs</strong> de profil via vos pages d’entrée. Créez, concevez et gérez des <strong>formulaires</strong> personnalisés adaptés à vos besoins en fonction d’un jeu de données spécifique. Vous pouvez ensuite utiliser ces formulaires dans les pages de destination pour ajouter les attributs de profil de votre choix au jeu de données défini pour chaque formulaire.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nouveaux connecteurs source pour les applications de programmes de fidélité</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De nouveaux <strong>connecteurs de</strong> sources sont désormais disponibles en Adobe Experience Platform pour les applications de fidélité Talon.One, Capillary et Kobie. Ces connecteurs vous permettent de diffuser facilement des données de fidélité dans Adobe Experience Platform et d’exploiter ces données dans Journey Optimizer.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Export d’un message</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il est désormais possible d’exporter <strong>les diffusions</strong> envoyées dans un jeu de données spécifique, à des fins d’archivage et de conformité. Cette capacité est disponible non seulement pour les e-mails, mais aussi pour d’autres canaux tels que les SMS. La durée de conservation des données pour le jeu de données d’exportation de messages est maintenant <strong>de 7 jours</strong>.</p>
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
<p>Une nouvelle <strong>API</strong> Journey Optimizer est désormais disponible, vous permettant de récupérer et d’inspecter par programmation les données relatives à la campagne, telles que les détails, les versions et les configurations.</p>
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
<p>Trois nouvelles <strong>alertes</strong> de parcours sont désormais disponibles pour vous aider à surveiller et suivre les événements du cycle de vie du parcours et les performances des actions personnalisées :</p>
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
<p>Vous pouvez désormais appliquer rapidement des <strong>thèmes</strong> pré-approuvés pour assurer la cohérence de la marque dans tous les e-mails, accélérer votre processus de création de campagnes et produire indépendamment des e-mails de haute qualité tout en réduisant la dépendance vis-à-vis des équipes de conception.</p>
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

#### IA

* **Assistant IA Contrôles** de qualité du contenu - En plus de l’alignement de la marque, vous pouvez désormais évaluer la qualité<strong> globale </strong>du contenu pour découvrir les problèmes potentiels de lisibilité, de cohésion et d’efficacité, indépendamment des directives de votre marque. Ces contrôles automatisés aident à identifier les messages peu clairs, les tonalités incohérentes ou les lacunes structurelles.
* **Mettez à jour les marques avec le nouvel onglet** de couleur - Les directives de marque garantissent que votre marque est présentée de manière cohérente sur tous les points de contact. La nouvelle <strong>section</strong> Couleurs définit les normes pour le système de couleurs de votre marque, décrivant comment les couleurs sont sélectionnées, organisées et appliquées dans toutes les expériences. Il garantit une utilisation cohérente des couleurs primaires, secondaires, accentuées et neutres pour soutenir une identité de marque cohérente, accessible et reconnaissable.

#### Campagnes

* **Planifiez Campaign à l’aide du fuseau** horaire du profil - Campaign La planification peut désormais utiliser le fuseau<strong> horaire de </strong>chaque profil pour remettre les messages à l’heure locale prévue.

  **Remarque** : Cette amélioration n’est disponible que pour un ensemble d’organisations (disponibilité limitée).

#### Canaux

* **Webhooks SMS : Phase II** - Description à fournir.

* **Offre** de revente WhatsApp - Description à fournir.

#### Concepteur d’e-mail

* **Corrections en place dans le Concepteur** d’e-mails - <strong>Les suggestions</strong> automatiques de contenu basées sur l’IA sont désormais disponibles dans le Concepteur d’e-mails lorsque des violations sont détectées lors de la validation du contenu. Si le contenu est signalé comme étant mal aligné avec les directives de la marque ou ne répond pas aux critères de qualité, le système génère de manière proactive des alternatives corrigées qui peuvent être examinées et appliquées en ligne, améliorant ainsi la conformité et accélérant la production.

#### Décision concernant l’expérience

* **Arbitrage** de parcours : vous pouvez désormais utiliser <strong>des formules et des modèles</strong> d’IA pour augmenter automatiquement les scores de priorité des parcours en fonction des attributs du profil client et des facteurs contextuels, garantissant ainsi que les clients entrent dans les parcours les plus pertinents.

  **Remarque** : Cette amélioration n’est disponible que pour un ensemble d’organisations (disponibilité limitée).

* **exd Sandbox Tool Documentation - Mise à jour** - Description à fournir.

* **API** d’outils de migration en libre-service : un nouvel ensemble d’API<strong> d’outils de migration est disponible pour migrer les entités de gestion des </strong>offres vers Experience Decisioning. Les outils permettent une migration transparente entre les environnements de test avec des capacités de résolution de dépendance et de restauration.

* **Joindre des fragments aux éléments** de décision - Journey Optimizer offre désormais la possibilité d’attacher <strong>des fragments</strong> aux éléments de décision qui peuvent être exploités dans des campagnes d’expérience basées sur du code via des stratégies de décision.

  **Remarque** : Auparavant disponible en disponibilité limitée, cette amélioration est désormais disponible pour tous les environnements (disponibilité générale).

#### Parcours

* **Utilisation d’une charge utile de réponse d’échec dans le parcours Actions** personnalisées : vous pouvez désormais définir une charge<strong> utile de réponse d’erreur facultative </strong>pour les actions personnalisées. Lorsqu’un appel échoue, la charge utile d’erreur est exposée dans le contexte du parcours et est disponible dans la branche expiration/erreur pour prendre en charge une logique de secours et un débogage plus riches.

* **Combiner des actions** de message natives et Adobe Campaign - Journey Optimizer vous permet désormais de combiner Adobe Campaign actions de message v7/v8 avec des actions de canal natives dans le même parcours.

* **Validation de la taille de la charge utile du parcours - Journey Optimizer fournit désormais une** validation<strong> de la taille de la charge utile pour garantir des performances optimales</strong> et la stabilité du système. Lors de la création ou de la publication de parcours, vous recevez des avertissements clairs et des erreurs si la taille des charges utiles approche ou dépasse les limites recommandées, ainsi que des conseils pratiques pour optimiser la configuration de votre parcours. Cette validation proactive vous aide à identifier rapidement les problèmes potentiels et à maintenir les performances du parcours.

* **Actions entrantes multiples dans les parcours : pour simplifier l’orchestration de votre parcours, vous pouvez désormais définir** plusieurs actions<strong> entrantes</strong> dans un seul parcours. Auparavant disponible dans les campagnes, cette fonctionnalité vous permet de diffuser plusieurs expériences basées sur du code, messages in-app, cartes de contenu ou actions web à différents emplacements en même temps, chaque action contenant un contenu spécifique.

  **Remarque** : Auparavant disponible en disponibilité limitée, cette amélioration est désormais disponible pour tous les environnements (disponibilité générale).

#### Campagnes orchestrées

* **Sélectionner les attributs et copier les valeurs** de distribution : vous pouvez désormais sélectionner ou copier des valeurs directement à partir de la vue Distribution de valeurs dans les campagnes orchestrées.

* **Héritage des étiquettes d’utilisation des données pour les audiences** : <strong>les étiquettes</strong> d’utilisation des données appliquées dans Adobe Experience Platform sont désormais automatiquement reportées lors de l’enregistrement des audiences dans des campagnes orchestrées, ce qui réduit le balisage DULE manuel.

* **Filtres de reciblage prédéfinis** : pour faciliter le reciblage des cas d’utilisation de campagnes orchestrées, cette version introduit de nouveaux <strong>filtres de reciblage</strong>. Ces filtres vous permettent de cibler directement les audiences en fonction de l’engagement des messages, tels que envoyé, ouvert uniquement, ouvert ou cliqué, ou ouvert et cliqué, et de sélectionner la campagne spécifique ou la campagne de transition que vous souhaitez recibler.

* **Filtres prédéfinis avec paramètres** - Vous pouvez désormais créer des <strong>filtres avec des paramètres</strong> dans des campagnes orchestrées pour des règles réutilisables et modifiables.

* **Confirmation du message avant l’envoi** - Une <strong>étape</strong> de confirmation est désormais activée par défaut avant l’envoi de campagnes orchestrées afin de réduire les envois accidentels.

* **Prise en charge** des métadonnées générées par l’utilisateur : la <strong>fonction</strong> d’assistance executionMetadata est désormais disponible dans l’éditeur de personnalisation pour les campagnes orchestrées, ce qui vous permet d’associer des informations contextuelles à n’importe quelle action native et de les stocker dans un jeu de données pour les exporter vers des systèmes externes.

* **Bouton** Redémarrer - Les campagnes orchestrées incluent désormais un <strong>bouton</strong> de redémarrage qui vous permet de relancer rapidement les exécutions en cas de besoin avant de publier la campagne.

* **Prise en charge** du contrôle de débit : les campagnes orchestrées prennent désormais en charge <strong>le contrôle</strong> des taux pour vous aider à accélérer les livraisons et à vous aligner sur les contraintes de volume.

#### Autorisations

* **Empêcher l’auto-approbation des parcours et des campagnes** : vous pouvez désormais exiger que les créateurs ne puissent pas approuver leurs propres parcours ou campagnes, ce qui améliore la <strong>séparation des tâches</strong> dans les workflows d’approbation.

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
<p>Optimisé par Adobe Experience Platform Agent Orchestrator, <strong>Journey Agent</strong> est disponible dans Journey Optimizer et vous permet d’analyser les parcours via une interface en langage naturel. Vous pouvez désormais générer et gérer du contenu spécifique à un canal directement dans Journey Agent, créer du contenu pour des canaux tels que les e-mails et les notifications push, appliquer et prévisualiser des modèles, affiner le ton et le style à l’aide d’invites et ouvrir du contenu dans Content Designer pour une modification contextuelle.</p>
<p>Date de disponibilité : mardi 2 février 2026</p>
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
<p>Vous pouvez désormais inclure <strong>des offres</strong> personnalisées dans vos parcours via une activité de décision de contenu dédiée dans le canevas de parcours et les utiliser dans les activités de parcours, y compris les conditions et les actions personnalisées.</p>
<p>Date de disponibilité : mardi 2 février 2026</p>
</td>
</tr>
</tbody>
</table>
