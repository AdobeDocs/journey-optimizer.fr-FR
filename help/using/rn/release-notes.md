---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
topic: Content Management
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d2c6c2cabc40d896fa3bf2bd401fe1c15e7c8054
workflow-type: tm+mt
source-wordcount: '1843'
ht-degree: 41%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations des fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour. [!DNL Adobe Journey Optimizer] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Notes de mise à jour de septembre 2025 {#25-9-rn}

**Date de publication** : 23-24 septembre 2025

### Nouvelles fonctionnalités {#sept-25-9-features}

<!-- table>
<thead>
<tr>
<th><strong>Public API to retrieve journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new Journey Optimizer API is now available to retrieve journeys and their associated objects such as campaigns and surfaces.</p>
<p>For more information, refer to the <a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">detailed documentation</a></p>
<p>Availability date: Sept 25, 2025</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Journey Optimizer Experimentation Accelerator</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer Experimentation Accelerator est un produit IA conçu pour faire passer votre expérimentation au niveau supérieur. Conçu pour les utilisateurs de Adobe Journey Optimizer et d’Adobe Target, il unifie la gestion des expériences, fournit des informations et des opportunités optimisées par l’IA et introduit un nouvel agent d’expérimentation.</p>
<p>Vous pouvez vous attendre à :</p>
<ul>
<li><strong>Inventaire d’expériences unifié :</strong> permet d’afficher, de filtrer et de gérer rapidement toutes les expériences de Adobe Journey Optimizer et d’Adobe Target dans un espace de travail unique.</li>
<li><strong>Informations et opportunités de l’expérience AI :</strong> allez au-delà des lectures statistiques avec des informations et des recommandations pilotées par GenAI. Chaque expérience fait désormais apparaître des opportunités exploitables, accompagnées d’une justification, afin que les équipes puissent décider en toute confiance de la suite des tests.</li>
<li><strong> Prise en charge du bandit manchot (MAB) dans Journey Optimizer :</strong> optimisez l’impact tout en réduisant le trafic gaspillé grâce aux expériences de bandit manchot. Au lieu de répartir les audiences de manière égale, MAB affecte automatiquement davantage de visiteurs aux variations les plus performantes en temps réel afin que vous puissiez offrir de meilleures expériences à davantage de clients tout en apprenant ce qui fonctionne.</li></ul>
<p><img src="assets/do-not-localize/experimentation-accelerator.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../content-management/experiment-accelerator.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 23 septembre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent est là !</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Optimisé par <a href="https://experienceleague.adobe.com/fr/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator" target="_blank">Adobe Experience Platform Agent Orchestrator</a>, Journey Agent est disponible dans Journey Optimizer. Il permet d’analyser les parcours par le biais d’une interface en langage naturel. L’agent détectera les conflits d’audience ou planifiera des conflits et des abandons de profils dans un parcours pour vous aider à prendre des mesures afin de les résoudre. Vous pourrez bientôt créer des parcours avec le soutien d’un agent.</p>
<p>Pour plus d’informations, consultez la <a href="https://experienceleague.adobe.com/fr/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze" target="_blank">documentation détaillée</a>.</p>
<p>Date de disponibilité : 24 septembre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mode sombre dans le Concepteur d’e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le Concepteur d’e-mail de Journey Optimizer permet désormais de passer en mode sombre, pour que vous puissiez notamment définir des paramètres personnalisés spécifiques qui s’afficheront uniquement pour les destinataires qui lisent leurs e-mails en mode sombre.</p>
<p>Prenez note des points suivants :</p>
<ul>
<li>Le rendu final du mode sombre dépend du client de messagerie de la personne destinataire.</li>
<li>Les clients de messagerie ne prennent pas tous en charge le mode sombre personnalisé. De plus, certains clients de messagerie appliquent uniquement leur propre mode sombre par défaut pour tous les e-mails reçus. Dans les deux cas, le rendu des paramètres personnalisés que vous avez définis dans le Concepteur d’e-mail ne pourra pas être affiché.</li>
</ul>
<p><img src="assets/do-not-localize/dark-mode.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../email/dark-mode.md">documentation détaillée</a>.</p>
 <p>Date de disponibilité : 16 septembre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Optimisation des chemins de parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Utilisez le nouveau nœud Optimiser pour cibler des audiences spécifiques ou exécuter des tests A/B afin de déterminer le meilleur moyen d’atteindre vos indicateurs de performance clés orientés métier.</p>
<p>Cet outil vous permet de tester, varier et personnaliser les communications, le séquencement et les délais afin d’atteindre avec précision votre clientèle.</p>
<p>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en obtenir l’accès.</p>
<p><img src="assets/do-not-localize/optimize.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/optimize.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 4 septembre 2025</p>
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
<p>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en obtenir l’accès.</p>
<p><img src="assets/do-not-localize/custom-delegation.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../configuration/delegate-custom-subdomain.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 4 septembre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utilisation des données Adobe Experience Platform pour la personnalisation et la prise de décision</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Publiée précédemment en version bêta publique, cette fonctionnalité est désormais disponible pour tous les environnements. Les améliorations suivantes ont été apportées à cette version :</p>
<ul><li>Prise en charge de la personnalisation de la recherche de jeux de données dans les canaux entrants.</li>
<li>La fonction d’assistance « datasetLookup » peut désormais être utilisée dans les fragments d’expression. Pour l’instant, cette fonctionnalité est disponible pour un nombre limité de clientes et clients. Pour en bénéficier, contactez votre représentant ou représentante Adobe.</li>
<li>Une option de l’interface de gestion des jeux de données permet désormais d’activer les jeux de données basés sur des enregistrements pour la personnalisation de la recherche, sans avoir à effectuer d’appel API.</li>
<li>Surveillance améliorée pour suivre le statut d’ingestion des données et déterminer le moment auquel les jeux de données sont prêts pour la recherche.</li>
<li>Mise à jour des instructions d’utilisation et des mécanismes de sécurisation pour garantir des performances et une fiabilité optimales.</li>
<li>Les jeux de données Adobe Experience Platform peuvent désormais être utilisés dans les règles de limitation de prise de décision.</li></ul></p>
<p>Pour plus d’informations, consultez la <a href="../data/lookup-aep-data.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 1er septembre 2025</p>
</td>
</tr>
</tbody>
</table>


### Améliorations {#sept-25-9-improvements}

* **Prise en charge du Webhook pour les campagnes déclenchées par l’API**\
  Les campagnes déclenchées par API prennent désormais en charge les Webhooks. Configurez une URL webhook pour recevoir des mises à jour en temps réel de l’état de chaque message, ce qui améliore l’observabilité et permet une surveillance et une automatisation transparentes. [En savoir plus](../configuration/feedback-webhooks.md)

  Date de disponibilité : 29 septembre 2025

* **Prise en charge de mTLS pour le canal SMS**
Lors de la configuration d’un fournisseur de SMS personnalisé, vous avez désormais la possibilité d’activer l’authentification mutuelle TLS (mTLS), qui nécessite que le client et le serveur confirment l’identité de l’un et l’autre avant qu’une connexion sécurisée ne soit établie. [En savoir plus](../sms/sms-configuration-custom.md) - Date de disponibilité : 23 septembre 2025

* **Schémas basés sur des modèles**\
  Les schémas basés sur des modèles peuvent désormais être utilisés par pour prendre en charge vos besoins de modélisation relationnelle dans les campagnes orchestrées. [En savoir plus](../orchestrated/gs-schemas.md) - Date de disponibilité : 23 septembre 2025

* **Prise en charge de la recherche de jeux de données dans parcours**\
  Une nouvelle activité dans les parcours, **Recherche de jeu de données**, vous permet de récupérer dynamiquement les données des jeux de données d’enregistrement Adobe Experience Platform au moment de l’exécution. Grâce à cette fonctionnalité, vous pouvez accéder à des données qui peuvent ne pas se trouver dans la payload de profil ou d’événement, en veillant à ce que vos interactions client soient à la fois pertinentes et opportunes. [En savoir plus](../building-journeys/dataset-lookup.md) - Date de disponibilité : 23 septembre 2025

  Cette activité est disponible uniquement pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.

* **Prise en charge de la redirection dans les actions personnalisées de Parcours**\
  Les redirections (302) sont désormais prises en charge dans les actions personnalisées de Parcours. - Date de disponibilité : 23 septembre 2025

* **Alertes de surveillance de la configuration des canaux** : vous pouvez désormais vous abonner pour recevoir des alertes système, soit par e-mail, soit dans le centre de notifications Journey Optimizer, en cas d’erreur de configuration du canal e-mail utilisant le type de délégation de sous-domaine personnalisé. [En savoir plus](../reports/alerts.md#alert-channel-config-failure) - Date de disponibilité : 23 septembre 2025

* **Demandes de désabonnement en un clic** - Nous avons introduit des améliorations qui renforcent encore la gestion des demandes de désabonnement en un clic configurées sous Gestion Adobe, en assurant un traitement fiable et cohérent. - Date de disponibilité : 23 septembre 2025

* **Les paramètres de corps JSON imbriqués sont désormais pris en charge dans l’authentification personnalisée**\
  Lors de la configuration de l’authentification personnalisée pour une action personnalisée, les objets JSON imbriqués (par exemple, les sous-objets dans `bodyParams`) sont désormais pris en charge. [En savoir plus](../datasource/external-data-sources.md#custom-authentication-mode) - Date de disponibilité : 18 septembre 2025

* **Fréquence du capping redéfini à l’heure** : vous pouvez désormais appliquer un capping de la fréquence à l’heure pour les jeux de règles de canal. Auparavant disponible en disponibilité limitée, cette fonctionnalité est désormais disponible pour tous les environnements et vous permet de choisir une heure (auparavant 3 heures). [En savoir plus](../conflict-prioritization/channel-capping.md) - Date de disponibilité : 17 septembre 2025

* **Simulation des variations de contenu pour tous les canaux entrants**\
  Auparavant uniquement disponible pour les canaux E-mail, SMS et Notification push, la simulation de variations de contenu s’applique désormais également à tous les canaux entrants. [En savoir plus](../test-approve/simulate-sample-input.md) - Date de disponibilité : 17 septembre 2025

* **Expression pour les règles de limitation de prise de décision** : vous pouvez désormais créer vos propres expressions pour définir le seuil d’une règle de limitation pour un élément de décision. [En savoir plus](../experience-decisioning/items.md#capping) - Date de disponibilité : 16 septembre 2025

* **Prise en charge des domaines dynamiques** : Journey Optimizer prend désormais en charge la personnalisation complète/de base des URL pour les domaines prédéfinis acceptés par Adobe. [En savoir plus](../personalization/personalization-build-expressions.md#where) - Date de disponibilité : 12 septembre 2025

  Cette fonctionnalité est disponible en disponibilité limitée pour un ensemble de clients et clientes.

* **Webhooks** - Cette version introduit les améliorations suivantes pour les Webhooks lors de la configuration d’un fournisseur de SMS personnalisé :

   * Vous pouvez maintenant définir l’objectif de votre webhook, soit Entrant, soit Commentaires, en fonction du type de données que vous souhaitez capturer. [En savoir plus](../sms/sms-configuration-custom.md#webhook) - Date de disponibilité : 23 septembre 2025

   * L’interface de configuration des mots-clés a été améliorée afin de faciliter la configuration. [En savoir plus](../sms/sms-configuration-custom.md#webhook) - Date de disponibilité : 23 septembre 2025

* **SMS**

   * Lors de la configuration d’un fournisseur de SMS personnalisé, vous pouvez désormais définir un mot-clé **Default** utilisé lorsqu’un SMS entrant contient un mot-clé non reconnu. Vous pouvez également créer des mots-clés **personnalisés** pour des actions spécifiques. [En savoir plus](../sms/sms-configuration-custom.md) - Date de disponibilité : 23 septembre 2025

   * Vous pouvez désormais accéder aux réponses par mots-clés entrants non définies qui sont envoyées par l’intermédiaire d’un SMS, y compris les fautes de frappe, les mots ou les phrases qui ne sont pas explicitement définis dans la configuration. Elles sont stockées pendant 13 mois dans le jeu de données **Événement d&#39;expérience de tracking d&#39;e-mail AJO**, sous **InboundMessage**. Disponible uniquement avec Sinch, Infobip et le fournisseur de SMS personnalisé. - Date de disponibilité : 23 septembre 2025

<!--
* **Approval policy permissions**
  Added an option when creating or setting Approval Policy to prevent Journey/Campaign creators from approving their own objects. [Read more](../test-approve/approval-policies.md) - Availability date: Sept 23, 2025 
-->

### Bientôt disponible {#sept-25-9-soon}

La publication des fonctionnalités et améliorations suivantes est prévue dans les prochains jours. **Les informations peuvent faire l’objet de modifications**. Les liens, écrans et documentation mis à jour seront partagés une fois que ces mises à jour seront en production.

<table>
<thead>
<tr>
<th><strong>Nouveau canal de notifications push web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer prend désormais en charge les notifications push web, étendant le canal push au-delà des applications mobiles. Vous pouvez diffuser facilement des notifications aux navigateurs mobiles et de bureau, ce qui vous permet d’atteindre les clients directement sur leurs appareils sans avoir besoin d’une application.</p>
<p>Cette amélioration vous permet d’interagir avec les utilisateurs et utilisatrices à l’aide de messages personnalisés et opportuns en temps réel, en exploitant les mêmes workflows de création et les mêmes fonctionnalités de ciblage que ceux déjà disponibles pour les notifications push mobiles.</p>
<!--p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Surveillance et reporting des actions personnalisées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La surveillance et la création de rapports d’action personnalisée sont désormais disponibles. Cette fonctionnalité offre une meilleure visibilité sur l’intégrité et l’exécution du parcours, y compris le statut du cycle de vie et les alertes de performances. Vous pouvez désormais rapidement comprendre quand, où et pourquoi une situation anormale se produit dans une action personnalisée.</p>
<!--p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p-->
</td>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>New source connectors for loyalty apps</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>New source connectors are now available in Adobe Experience Platform for the Talon.One, Capillary, and Kobie loyalty apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
</td>
</tr>
</tbody>
</table-->


<table>
<thead>
<tr>
<th><strong>Formulaires personnalisés de la page de destination</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Avec [!DNL Journey Optimizer], vous pouvez désormais capturer les attributs de profil via vos pages de destination.</p>
<p>Créez, concevez et gérez des formulaires personnalisés adaptés à vos besoins en fonction d’un jeu de données spécifique. Vous pouvez ensuite utiliser ces formulaires dans les pages de destination pour ajouter les attributs de profil de votre choix au jeu de données défini pour chaque formulaire.</p>
<p>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en obtenir l’accès.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<!--p>For more information, refer to the <a href="../landing-pages/lp-forms.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p-->
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
<li>Pour toute taille ou volume supplémentaire, vous pouvez acheter le module complémentaire Pièces jointes PDF . Pour plus d’informations, contactez votre représentant ou représentante Adobe.</li>
</ul>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<!--p>For more information, refer to the <a href="../email/pdf-attachments.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p-->
</td>
</tr>
</tbody>
</table>



* **Nouvelles alertes de Parcours**\
  De nouvelles alertes préconfigurées sont disponibles pour les parcours :

   * Taux de rejet du profil dépassé : ratio de rejets de profil par rapport aux profils entrés au cours des 5 dernières minutes ayant dépassé le seuil.
   * Taux d’erreurs d’action personnalisée dépassé : ratio des erreurs d’action personnalisée par rapport aux appels HTTP réussis au cours des 5 dernières minutes qui a dépassé le seuil.
   * Taux d’erreurs de profil dépassé : ratio de profils en erreur par rapport aux profils entrés au cours des 5 dernières minutes qui a dépassé le seuil.
<!--
  * [Profile Discard Rate Exceeded](../reports/alerts.md#profile-discard-rate-exceeded): Ratio of profile discards to entered profiles over the last 5 mins exceeded threshold.  
  * [Custom Action Error Rate Exceeded](../reports/alerts.md#custom-action-error-rate-exceeded): Ratio of custom action errors to successful HTTP calls over the last 5 mins exceeded threshold.  
  * [Profile Error Rate Exceeded](../reports/alerts.md#profile-error-rate-exceeded): Ratio of profiles-in-error to entered profiles over the last 5 mins exceeded threshold.-->

Vous pouvez modifier les valeurs de seuil et vous abonner à des alertes individuelles au niveau du parcours par rapport à la situation mondiale.

<!-- Availability date: Sept XX, 2025-->


* **Prise en charge des attributs personnalisés avec l’URL de désabonnement en un clic**\
  Avec Journey Optimizer, si vous gérez le consentement en dehors d’Adobe, vous pouvez définir un point d’entrée personnalisé externe en définissant votre propre lien de désabonnement en un clic dans la configuration du courrier électronique. Lorsque les personnes destinataires cliquent sur le lien de désabonnement, Journey Optimizer ajoute certains paramètres par défaut, spécifiques au profil, à l’événement de mise à jour du consentement.

  Pour personnaliser davantage l’adresse e-mail de désabonnement, vous pouvez maintenant définir des attributs personnalisés qui seront ajoutés à l’événement de consentement. Cette fonctionnalité est déjà disponible pour le lien de désabonnement en un clic personnalisé depuis la version du 25 août.

  <!-- Availability date: Sept XX, 2025-->
