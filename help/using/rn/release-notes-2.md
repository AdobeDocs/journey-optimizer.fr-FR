---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notes de mise à jour d’Adobe Journey Optimizer
hide: true
source-git-commit: 8ab2054698179fb23abf1c16915fe166afaf1e3f
workflow-type: tm+mt
source-wordcount: '2735'
ht-degree: 19%

---


<!-- DRAFT — Topic-based layout exploration. All content is identical to release-notes.md (May '26). The only change is the grouping axis: topic > type. -->

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations des fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] suit un modèle de diffusion continue, ce qui permet à Adobe de proposer régulièrement de nouvelles fonctionnalités, de nouvelles améliorations et de nouveaux correctifs. Cette approche permet un déploiement évolutif et échelonné des fonctionnalités afin d’assurer les performances et la stabilité dans tous les environnements. En raison de ce modèle, les notes de mise à jour sont mises à jour entre les versions mensuelles. Pour plus d’informations sur le cycle de publication et les phases de disponibilité, consultez le [cycle de publication de Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

>[!NOTE]
>
>Les fonctionnalités répertoriées dans ces notes de mise à jour incluent une **date de disponibilité** indiquant le moment auquel chaque modification devient accessible dans votre environnement. Les entrées marquées **Bientôt disponible** devraient sortir dans les prochains jours. Les informations sont sujettes à changement.

## Notes de mise à jour du 26 mai {#may-26-rn}

### Parcours {#may-26-journeys}

Les fonctionnalités et améliorations suivantes ont été ajoutées aux parcours dans cette version. D’autres modifications sont également prévues pour ce mois-ci. Consultez la section [Bientôt disponible](#may-26-journeys-coming-soon) ci-dessous.

<table>
<thead>
<tr>
<th><strong>Fragments de parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer <strong>fragments de Parcours </strong> dans Adobe Journey Optimizer. Les fragments de parcours sont des ensembles réutilisables de nœuds de parcours que vous pouvez créer une fois et déposer dans n’importe quel parcours de votre sandbox. Qu’il s’agisse d’une vérification d’éligibilité, d’une logique de routage de canal préférée ou d’une séquence de bienvenue, les fragments aident les équipes à se déplacer plus rapidement et à rester cohérentes, sans avoir à reconstruire la même logique à chaque fois.</p>
<p>Une fois créés, les fragments sont stockés dans un <strong>inventaire des fragments</strong> dédié et peuvent être insérés dans n’importe quel parcours à l’aide de l’activité <strong>Fragments de Parcours </strong>.</p>
<!--<p><img src="assets/do-not-localize/journey-fragments.gif"></p>-->
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/journey-fragments.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 13 mai 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Simulation de parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais définir votre parcours sur <strong>Simulation</strong>. Ce mode permet de valider la logique à l’aide d’<strong>utilisateurs simulés</strong>. Il s’agit de profils temporaires créés spécifiquement pour la simulation, qui vous permettent de tester librement sans avoir à gérer de profils de test persistants dans Adobe Experience Platform.</p>
<p>Cette fonctionnalité est actuellement en disponibilité limitée pour l’ensemble des clients et clientes, avec des fonctions essentielles.</p>
<p><img src="assets/do-not-localize/simulate-user.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/simulate-journey.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 5 mai 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Optimisation des chemins de parcours - Ciblage (disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Utilisez le nouveau nœud <strong>Optimiser</strong> pour cibler des audiences spécifiques afin de déterminer le meilleur moyen d’atteindre vos indicateurs de performance clés orientés métier.</p>
<p>Cet outil vous permet de développer des campagnes marketing plus efficaces, plus susceptibles de résonner au niveau 1:1, d’améliorer les efforts de personnalisation marketing pour les clients et d’améliorer les KPI d’engagement client essentiels, tels que les conversions et les recettes.</p>
<p>Auparavant disponible en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements.</p>
<p>Date de disponibilité : 21 mai 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Arbitrage de parcours - formules de classement (Disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais utiliser des formules pour augmenter automatiquement les scores de priorité des parcours en fonction des attributs de profil client et de facteurs contextuels, afin que les clients puissent accéder aux parcours les plus pertinents.</p>
<p>Auparavant disponible en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements.</p>
<p>Date de disponibilité : 21 mai 2026</p>
</td>
</tr>
</tbody>
</table>

#### Bientôt disponible {#may-26-journeys-coming-soon}

Les fonctionnalités de parcours ci-dessous devraient être publiées à la fin du mois. Les informations sont sujettes à changement.

<table>
<thead>
<tr>
<th><strong>Assistant AI pour les expressions de Parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’assistant AI fonctionne désormais dans l’éditeur d’expression avancé de parcours pour convertir les invites en langage naturel en expressions valides et en logique conditionnelle. Décrivez l’expression que vous souhaitez créer et l’assistant AI génère un code prêt à l’emploi que vous pouvez appliquer immédiatement ou affiner à l’aide d’invites de relance.</p>
<p>Cette fonctionnalité est disponible pour tous les clients sous la forme d’un Beta public.</p>
<!--<p><img src="assets/do-not-localize/expression-assistant.gif"></p>-->
<p>Date de disponibilité : 22 mai 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Simulation de parcours (disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Publiée précédemment en disponibilité limitée, la simulation de Parcours est désormais disponible pour tous les environnements. Avec cette version de disponibilité générale, vous pouvez désormais utiliser Journey Agent pour générer des utilisateurs et des événements simulés directement dans le menu Simulation .</p>
<p>Date de disponibilité : 1 juin 2026</p>
</td>
</tr>
</tbody>
</table>

* **Saisie automatique pour les parcours de lecture d’audience non récurrents** - Les parcours non récurrents **lecture d’audience** passent désormais automatiquement au statut **Arrêté** une fois le dernier profil actif quitté. Auparavant, ces parcours restaient **en ligne** jusqu’à l’expiration du délai d’expiration global de 91 jours, même lorsqu’aucun profil n’y circulait plus. Grâce à cette amélioration, le statut du parcours reflète le statut d’exécution réel dès qu’il est terminé, ce qui permet de conserver un inventaire précis de vos parcours sans intervention manuelle.

  Notez que ce comportement ne s’applique pas aux parcours qui incluent des nœuds provoquant des périodes d’attente, tels que les nœuds d’attente, les nœuds de réaction ou les transitions déclenchées par un événement. Ces parcours restent soumis à la temporisation globale standard de 91 jours.

  Date de disponibilité : 21 mai 2026

* **Authentification personnalisée basée sur un certificat dans les actions personnalisées** - Les actions personnalisées prennent désormais en charge l’authentification personnalisée basée sur un certificat. En ajoutant `subType: "certificateCredential"` à une configuration d’autorisation personnalisée, Journey Optimizer utilise un certificat géré Adobe pour signer une assertion client JWT et l’échanger contre un jeton d’accès (aucun secret client requis). Conçu pour les API d’entreprise qui appliquent la vérification d’identité avec certificat, comme l’Azure Entra ID.

  Date de disponibilité : 21 mai 2026

* **Personnalisation en boucle des données relationnelles** - L’éditeur de personnalisation prend désormais en charge un bloc Boucle qui effectue une itération sur les collections relationnelles, telles que les commandes, les comptes ou les réservations, et effectue le rendu d’un bloc de contenu par enregistrement dans un seul e-mail ou SMS. Les collections sont configurées par le biais du sélecteur de données à l’aide de jetons de personnalisation, sans écriture d’expression requise.

  Date de disponibilité : 1 juin 2026

* **Prise en charge des identifiants supplémentaires pour les audiences externes** - Les identifiants supplémentaires dans les parcours sont désormais pris en charge pour les audiences externes, y compris les audiences importées d’un fichier CSV et les audiences créées avec la composition d’audience fédérée. Vous pouvez désigner n’importe quel attribut de non-identité ou attribut d’identité de non-personne de l’audience comme ID supplémentaire. Aucun étiquetage de schéma n’est requis.

  Date de disponibilité : 1 juin 2026

### Campagnes orchestrées {#may-26-oc}

Les fonctionnalités et améliorations suivantes ont été ajoutées aux campagnes orchestrées dans cette version. D’autres modifications sont également prévues pour ce mois-ci. Consultez la section [Bientôt disponible](#may-26-oc-coming-soon) ci-dessous.

<table>
<thead>
<tr>
<th><strong>Campagnes orchestrées en chaîne</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les campagnes orchestrées peuvent désormais être liées en déclenchant une campagne orchestrée directement à partir de l’activité <strong>Fin</strong> d’une autre campagne orchestrée.</p>
<p>Cela permet de diviser une logique d’orchestration complexe en flux plus petits et réutilisables qui peuvent être appelés à partir de plusieurs campagnes parentes plutôt que reconstruits à chaque fois. La payload transmise au moment de l’exécution est disponible pour la segmentation et la personnalisation dans la campagne en aval. De ce fait, chaque campagne liée peut se comporter en fonction du contexte qu’elle reçoit.</p>
<p><img src="assets/do-not-localize/oc-trigger.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../orchestrated/trigger-orchestrated-campaign.md#signal-end">documentation détaillée</a>.</p>
<p>Date de disponibilité : 20 mai 2026</p>
</td>
</tr>
</tbody>
</table>

* **Ajouter des liens dans l’activité Enrichissement** - La fonctionnalité Ajouter un lien est désormais disponible dans l’activité Enrichissement pour les campagnes orchestrées. Vous pouvez ainsi créer une relation directe entre les données de votre table de travail et vos tables de base de données existantes.

  Date de disponibilité : 20 mai 2026

#### Bientôt disponible {#may-26-oc-coming-soon}

La fonctionnalité de campagne orchestrée suivante devrait sortir plus tard ce mois-ci. Les informations sont sujettes à changement.

<table>
<thead>
<tr>
<th><strong>Ciblage basé sur des fichiers pour les campagnes orchestrées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les campagnes orchestrées prennent désormais en charge le chargement d’un fichier CSV ou TXT directement dans la zone de travail de campagne en tant qu’audience de ciblage, sans avoir à ingérer le fichier dans Adobe Experience Platform au préalable. Les données du fichier sont utilisées au moment de l’exécution et ne sont pas conservées en tant que jeu de données Adobe Experience Platform. Lors de la configuration de fichiers, vous pouvez définir des mappages de colonnes, des types de données, une gestion des NULL et des politiques d’erreur par colonne. Cela prend en charge les campagnes de listes de partenaires ou d’envois ad hoc pour lesquelles la création d’un pipeline d’ingestion complet n’est pas pratique.</p>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Date de disponibilité : 1 juin 2026</p>
</td>
</tr>
</tbody>
</table>

### Campagnes {#may-26-campaigns}

Les améliorations de campagne suivantes devraient être publiées plus tard dans le mois. Consultez la section [Bientôt disponible](#may-26-campaigns-coming-soon) ci-dessous.

#### Bientôt disponible {#may-26-campaigns-coming-soon}

Les améliorations suivantes de la campagne devraient être publiées à la fin du mois. Les informations sont sujettes à changement.

* **Alertes client pour les événements de cycle de vie de campagne** - Les nouvelles alertes système vous informent désormais des événements de cycle de vie clés pour les campagnes déclenchées par action et par API. S’abonner au niveau du sandbox.

  Date de disponibilité : 1 juin 2026

* **Remplacer le champ d’exécution par défaut dans les campagnes** - Auparavant disponible au niveau du parcours, vous pouvez désormais remplacer le champ d’exécution par défaut défini globalement pour vos diffusions e-mail, SMS et WhatsApp dans les paramètres de la campagne.

  Date de disponibilité : 1 juin 2026

### Prise de décision {#may-26-decisioning}

Les fonctionnalités et améliorations suivantes ont été ajoutées à Decisioning dans cette version. D’autres modifications sont également prévues pour ce mois-ci. Consultez la section [Bientôt disponible](#may-26-decisioning-coming-soon) ci-dessous.

<table>
<thead>
<tr>
<th><strong>Règles de prise de décision et optimisation de l’IA dédiée aux formules de classement</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] utilise désormais l’IA pour détecter les règles de prise de décision et les formules de classement qui peuvent être simplifiées. Dans l’inventaire, un indicateur rouge s’affiche sur toute règle pour laquelle l’IA a identifié une opportunité d’optimisation. Cliquez sur l’indicateur pour afficher l’expression d’origine avec la version suggérée par l’IA. À partir de là, vous pouvez télécharger un fichier pour examiner la manière dont les profils simulés sont évalués par chaque version et confirmer qu’ils se comportent de manière identique, puis remplacer l’expression par l’expression optimisée.</p>
<p><img src="assets/do-not-localize/rule-ai.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../start/ai-features.md#decisioning-optimization">documentation détaillée</a>.</p>
<p>Date de disponibilité : 5 mai 2026</p>
</td>
</tr>
</tbody>
</table>

* **API de workflow de migration Decisioning** - Le contrat d’API pour la création d’analyses des dépendances et de workflows de migration a été mis à jour : transmettez **`request-level`** en tant que **paramètre de requête** sur l’URL de la requête (`sandbox`, `offer` ou `decision`). Le niveau de requête ne doit plus être envoyé dans le corps JSON. [En savoir plus](../experience-decisioning/decisioning-migration-api.md)

  Date de disponibilité : 6 mai 2026

* **Fragments de contenu Adobe Experience Manager dans Decisioning** - Vous pouvez désormais mapper les fragments de contenu Adobe Experience Manager aux éléments de décision dans Decisioning et les exploiter dans les politiques de décision pour diffuser le fragment approprié au bon client au bon moment. [En savoir plus](../integrations/aem-fragments.md#aem-decisioning)

  Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.

  Date de disponibilité : 20 mai 2026

#### Bientôt disponible {#may-26-decisioning-coming-soon}

La fonctionnalité de prise de décision suivante devrait être publiée à la fin du mois. Les informations sont sujettes à changement.

<table>
<thead>
<tr>
<th><strong>Prise en charge de la prise de décision dans le canal Courrier</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais ajouter des politiques de décision dans les parcours et campagnes de publipostage direct. Les politiques de décision sont des conteneurs pour vos offres qui s’appuient sur le moteur de prise de décision pour renvoyer de manière dynamique le meilleur contenu pour chaque membre de l’audience. La prise de décision par publipostage direct prend également en charge les cas d’utilisation de prise de décision par lots, ce qui vous permet d’exporter les éléments d’offre correspondants pour chaque profil dans une audience Adobe Experience Platform donnée.</p>
<!--<p><img src="assets/do-not-localize/exd-dm.gif"></p>-->
<p>Date de disponibilité : 1 juin 2026</p>
</td>
</tr>
</tbody>
</table>

### Canal E-mail {#may-26-email}

Les fonctionnalités et améliorations suivantes ont été ajoutées au canal e-mail dans cette version. D’autres modifications sont également prévues pour ce mois-ci. Consultez la section [Bientôt disponible](#may-26-email-coming-soon) ci-dessous.

<table>
<thead>
<tr>
<th><strong>Liens profonds dans le Concepteur d’e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il est désormais possible d’ajouter des liens profonds au contenu de votre e-mail par le biais d’une option dans le Concepteur d’e-mail. Cela permet aux utilisateurs et utilisatrices d’accéder directement au contenu in-app approprié au lieu d’être redirigés vers des navigateurs ou des boutiques d’applications, en préservant le contexte et l’engagement.</p>
<p><img src="assets/do-not-localize/deeplinks.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../email/deeplinks.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 12 mai 2026</p>
</td>
</tr>
</tbody>
</table>

#### Bientôt disponible {#may-26-email-coming-soon}

Les améliorations suivantes du canal e-mail devraient être publiées à la fin du mois. Les informations sont sujettes à changement.

* **Personnaliser les détails de l’expéditeur de l’e-mail par destinataire et campagne** - Les campagnes orchestrées prennent désormais en charge la personnalisation des champs d’en-tête des e-mails, notamment le nom de l’expéditeur, l’adresse de l’expéditeur et la réponse, à l’aide d’attributs de profil ou de données relationnelles. Cela permet aux détails de l’expéditeur de refléter le conseiller, l’emplacement ou la filiale approprié(e) pour chaque destinataire, plutôt que de router tous les envois via une seule adresse d’entreprise.

  Les valeurs d’en-tête peuvent être définies au niveau du canal et remplacées par campagne à l’aide de données contextuelles pour un contrôle plus précis.

  Date de disponibilité : 1 juin 2026

* **Texte enrichi dans les champs de fragment modifiables** - Vous pouvez désormais ajouter du texte enrichi aux fragments personnalisables utilisés dans le contenu de votre e-mail. Par exemple, lorsque vous utilisez le composant Texte comme champ modifiable dans le Designer d’e-mail, vous pouvez directement mettre en forme le contenu (en gras et en italique, par exemple) et insérer des liens hypertexte.

  Date de disponibilité : 1 juin 2026

* **Limiter la rupture d’héritage dans les fragments** - Lors de la création ou de la modification d’un fragment, vous pouvez désormais choisir s’il peut être modifié lorsqu’il est utilisé dans des e-mails. Le verrouillage d’un fragment garantit qu’il reste synchronisé partout où il apparaît, empêchant les modifications locales qui pourraient enfreindre les normes de la marque ou les exigences de conformité. Ce paramètre peut être mis à jour ultérieurement et s’appliquer aux utilisations futures.

  Date de disponibilité : 1 juin 2026

### Messagerie mobile (SMS, MMS et RCS) {#may-26-mobile}

Les fonctionnalités et améliorations suivantes ont été ajoutées à la messagerie mobile dans cette version.

<table>
<thead>
<tr>
<th><strong>Nouveau canal de message mobile et messagerie RCS améliorée</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les SMS, MMS et RCS sont désormais regroupés dans une seule action <strong>Message mobile</strong> dans Adobe Journey Optimizer, ce qui facilite la gestion de tous les types de messages mobiles à partir d’un seul emplacement. Dans le cadre de cette mise à jour, vous pouvez désormais créer des messages RCS de médias riches, y compris des images, des carrousels et des actions suggérées, directement dans Journey Optimizer grâce à une nouvelle expérience de création native.</p>
<p>Pour plus d’informations, consultez la <a href="../mobile/get-started-mobile.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 20 mai 2026</p>
</td>
</tr>
</tbody>
</table>

* **Nombre de caractères** - Vous pouvez désormais utiliser le nombre de caractères pour surveiller la longueur de vos SMS en temps réel. Cela vous permet de savoir quand un message sera partagé en plusieurs segments afin de mieux gérer la mise en forme et d’éviter une hausse imprévue des coûts d’envoi. [En savoir plus](../mobile/create-mobile-message.md)

* **SMS entrant vers un jeu de données personnalisé** : dans **Informations d’identification de l’API SMS**, acheminez **SMS entrant** vers un **jeu de données d’événement d’expérience personnalisé et activé pour le profil** que vous sélectionnez au lieu du jeu de données de tracking par défaut uniquement. [En savoir plus](../mobile/mobile-webhook.md)

* **Amélioration de l’interface des webhooks** : lors de la configuration des webhooks SMS, l’interface d’utilisation comprend désormais un guide de configuration intégré avec des exemples pratiques, ce qui facilite l’alignement des payloads des fournisseurs et la résolution des problèmes sans quitter le flux de configuration. [En savoir plus](../mobile/mobile-webhook.md)

### Canal WhatsApp {#may-26-whatsapp}

Les améliorations suivantes ont été ajoutées au canal WhatsApp dans cette version.

* **Prise en charge et suivi des boutons WhatsApp** - Les modèles WhatsApp prennent désormais en charge **Réponse rapide**, **Call to action - URL** et **Call to action - téléphone**, **Copier le code** n’est pas pris en charge. Journey Optimizer envoie les boutons pris en charge et suit les interactions avec les autres rapports de canal.

* **Données contextuelles du canal WhatsApp** - Journey Optimizer capture désormais les données d’interaction supplémentaires renvoyées par le canal WhatsApp et les stocke dans le **Jeu de données AJO EmailTrackingExperienceEvent** sous le groupe de champs `whatsAppChannelContext`.

  +++ Champs capturés pour la création d’audiences WhatsApp et l’analyse de l’engagement

   * **`messageType`** - Type de message WhatsApp (par exemple `templateBased`, `response`)
   * **`inboundMessage`** - contenu de réponse entrante (par exemple `stop`, `start`, `subscribe`)
   * **`inboundNumber`** - ID de l’expéditeur où le message entrant a été reçu
   * **`channelType`** - Catégorie de canal (`Utility`, `Marketing` ou `Promotional`)
   * **`profileNumber`** - Numéro de téléphone à partir duquel le message entrant a été reçu
   * **`origTimestamp`** - Horodatage d&#39;origine de Meta / WhatsApp
   * **`status`** - Statut de la diffusion, y compris les commentaires normalisés du fournisseur (`sent`, `delivered`, `bounce`, `error`, `delay`, `duplicate`, `denylist`, `exclude` ou `unknown`) et le message brut de statut du fournisseur
   * **`reactionEvent`** - Contenu de la réponse de l’utilisateur : émoticône pour les réactions ou texte du message pour les réponses à un message spécifique
   * **`reactionMessageID`** - ID du message d’origine auquel une réponse est apportée
   * **`reactionActionName`** - Type d’action de réponse (`react`, `unreact` ou `reply`)
   * **`interactiveSelectedTitle`** - Titre sélectionné par l&#39;utilisateur dans un message interactif WhatsApp
   * **`interactiveType`** - Type de message interactif (`list reply`, `button reply` ou `button`)
   * **`interactiveSelectedDescription`** - Description de l&#39;option interactive WhatsApp sélectionnée
   * **`interactiveSelectedID`** - Identifiant de l&#39;option sélectionnée sur WhatsApp

  +++

### Contenu et intégrations {#may-26-content}

Les fonctionnalités et améliorations suivantes ont été ajoutées à la gestion de contenu et aux intégrations dans cette version.

<table>
<thead>
<tr>
<th><strong>Sélecteur du gestionnaire de contenu</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer utilise désormais le <strong>sélecteur de grille de contenu</strong>, une boîte de dialogue modale unifiée permettant de sélectionner à la fois le Experience Manager Assets et les fragments de contenu. Le nouveau sélecteur comprend :</p>
<ul>
<li><strong>Navigation, recherche et filtrage</strong> sur toutes les ressources et tous les fragments.</li>
<li><strong>Recherche sémantique IA</strong> : décrivez ce dont vous avez besoin en langage clair et simple, par exemple « du café dans les montagnes », pour faire apparaître des ressources contextuellement pertinentes en fonction du sens et du contenu, et pas seulement des correspondances textuelles. Les requêtes multilingues sont également prises en charge.</li>
<li><strong>Chargement de résumé</strong> : chargez un résumé marketing pour faire apparaître automatiquement les ressources qui s’alignent sur le contexte de votre campagne en fonction de son contenu et des exigences.</li>
<li><strong>Rendus Dynamic Media</strong> : sélectionnez et appliquez des rendus d’image pour les ressources dynamiques sans quitter le sélecteur.</li>
</ul>
<p>Pour plus d’informations, consultez la <a href="../integrations/aem-content-advisor.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 19 mai 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Intégrations (disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La fonctionnalité <b>Intégrations</b> vous permet de connecter des sources de données tierces directement à Adobe Journey Optimizer. En simplifiant la manière d’extraire des données externes et du <b>contenu composable</b>, cette fonctionnalité facilite la diffusion de messages dynamiques personnalisés sur tous vos canaux.</p>
<p>Publiée précédemment dans Beta, cette fonctionnalité est désormais disponible pour tous les environnements.</p>
<p>Pour plus d’informations, consultez la <a href="../integrations/integrations.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 4 mai 2026</p>
</td>
</tr>
</tbody>
</table>

* **Accès aux référentiels interorganisations dans le sélecteur Assets** - Vous pouvez désormais sélectionner facilement des ressources à partir de référentiels dans plusieurs organisations directement dans le sélecteur de ressources Adobe Experience Manager.

### Administration {#may-26-admin}

Les améliorations d’administration suivantes devraient être publiées plus tard dans le mois. Consultez la section [Bientôt disponible](#may-26-admin-coming-soon) ci-dessous.

#### Bientôt disponible {#may-26-admin-coming-soon}

Les améliorations d’administration suivantes devraient être publiées à la fin du mois. Les informations sont sujettes à changement.

* **Dossiers pour les parcours et les campagnes** - Vous pouvez désormais organiser vos parcours et campagnes dans des dossiers pour améliorer la navigation et la gestion dans l’interface.

  Date de disponibilité : 21 mai 2026

* **Jeu de données d’événement de retour de message passant à l’ingestion par lots** - Le `AJO Message Feedback Event Dataset` passe de la diffusion en continu au mode d’ingestion par lots. Cette modification garantit que l’ingestion de données ne dépasse pas les limites d’ingestion en flux continu. Si vous utilisez ce jeu de données dans des rapports Customer Journey Analytics ou si vous exécutez des requêtes sur celui-ci, attendez-vous à une augmentation de la latence des données allant jusqu’à 2 heures.

  Date de disponibilité : 1 juin 2026
