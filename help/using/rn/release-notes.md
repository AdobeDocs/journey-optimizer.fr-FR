---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
topic: Content Management
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3eb73751fdb746dd2659e31c1b776fe2d767809f
workflow-type: tm+mt
source-wordcount: '2478'
ht-degree: 64%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] suit un modèle de diffusion continue, ce qui permet à Adobe de diffuser régulièrement de nouvelles fonctionnalités, de nouvelles améliorations et de nouveaux correctifs. Cette approche permet un déploiement évolutif et échelonné des fonctionnalités afin d’assurer les performances et la stabilité dans tous les environnements.

En raison de ce modèle, les notes de mise à jour sont mises à jour entre les versions mensuelles.  Une section dédiée [Dernières mises à jour](#updates-rn) met en évidence les nouvelles fonctionnalités et améliorations apportées lors de leur déploiement en production. Vous êtes ainsi toujours informé de tous les changements en temps réel. <!--For full details about the release cycle and availability phases, see [Journey Optimizer release cycle](#releases.md).-->

[!DNL Adobe Journey Optimizer] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Notes de mise à jour préliminaires du 25 octobre {#oct-25-10-rn}

**Les notes de version préliminaire ci-dessous peuvent être modifiées sans préavis jusqu’à la date de publication**. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les notes de mise à jour, à la date de publication.

Voir également les [Notes de mise à jour préliminaires d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Date de publication** : jeudi 22 octobre 2025

### Nouvelles fonctionnalités {#oct-25-10-features}

<table>
<thead>
<tr>
<th><strong>Heures calmes/exclusions temporelles</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les heures calmes vous permettent de définir des exclusions temporelles pour les canaux E-mail, SMS, Notification push et WhatsApp. Ils garantissent qu’aucun message n’est envoyé pendant des périodes spécifiques, ce qui vous aide à respecter les préférences des clients et les exigences de conformité.</p>
<p>Vous pouvez appliquer des heures calmes par le biais d’ensembles de règles, qui peuvent être affectés à des actions individuelles dans des campagnes ou des parcours pour un contrôle précis. En rationalisant ces processus.</p>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
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
<p>Cette fonctionnalité offre une meilleure visibilité sur l’intégrité et l’exécution du parcours, y compris le statut du cycle de vie et les alertes de performances. Vous pouvez désormais rapidement comprendre quand, où et pourquoi une situation anormale se produit dans une action personnalisée.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>RCS Basic Messaging</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>With the new RCS Basic add-on offering, you can now deliver basic Rich Communication Services (RCS) messaging in Journey Optimizer, enabling the following enhanced messaging capabilities subject to provider and geographical support:</p>
<ul>
<li><strong>Branded and verified sender support:</strong> Send messages using verified business profiles with branding elements (logo, sender name, etc.).</li>
<li><strong>Message delivery insights:</strong> Receive detailed delivery reports including message status updates (e.g., sent, delivered, read).</li>
<li><strong>Link tracking:</strong> Embed and track URLs within RCS messages for engagement analytics.</li>
<li><strong>Fallback to SMS:</strong> Automatic fallback to SMS when the recipient's device does not support RCS or is temporarily unreachable via RCS.</li>
<li><strong>Basic message composition:</strong> Send basic text-based RCS messages.</li>
</ul>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct mail channel in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail channel is now available in orchestrated campaigns. The Direct mail activity facilitates direct mail sending within your Orchestrated campaign, for both one-time and recurring messages. It serves to automate the process of generating the extraction file required by direct mail providers. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Direct Mail channel in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously limited to Campaigns, Direct Mail channel is now available on the journey canvas, enabling you to incorporate Direct Mail into your journeys. Direct Mail can now be used in both batch and 1:1 journey scenarios, with support for file extraction configuration and time-based frequency settings.</p>
<p> Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
<!--/td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Nouvelle API pour récupérer les campagnes d’action</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une nouvelle API Journey Optimizer est désormais disponible, ce qui vous permet de récupérer et d’inspecter par programmation les données liées à la campagne, telles que les détails, les versions et les configurations.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nouveaux connecteurs source pour les applications de fidélité</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De nouveaux connecteurs source sont désormais disponibles dans Adobe Experience Platform pour les applications de fidélité Talon.One, Capillary et Kobie. Ces connecteurs vous permettent de diffuser facilement des données de fidélité dans Adobe Experience Platform et d’exploiter ces données dans Journey Optimizer.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Prise en charge de la prise de décision dans le canal e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais ajouter des politiques de décision dans des parcours et des campagnes par e-mail. Les politiques de décision sont des conteneurs pour vos offres qui tirent profit du moteur de prise de décision afin d’effectuer un rendu dynamique du meilleur contenu à diffuser, pour chaque membre de l’audience.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mode à débit élevé pour les campagnes par e-mail déclenchées par l’API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Un nouveau mode à débit élevé est désormais disponible dans les campagnes déclenchées par API. Ce mode est conçu pour la messagerie en temps réel à grande échelle (jusqu’à 5 000 transactions par seconde) et offre une disponibilité supérieure avec une latence plus faible.</p>
<p>Cette fonctionnalité n’est disponible que pour le canal e-mail, pour les organisations qui ont acheté l’offre complémentaire de messagerie transactionnelle à haut débit d’Adobe. Pour plus d’informations, contactez votre représentant ou représentante Adobe.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Règles de ciblage réutilisables</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer vous permet désormais de créer des règles à partir d’un menu d’interface utilisateur dédié et de les exploiter lors de la création du ciblage, dans le cadre de l’optimisation du contenu d’une campagne ou d’un parcours, dans l’activité Optimiser le parcours .</p>
<p>Les règles de ciblage sont actuellement disponibles pour les organisations qui ont acheté le module complémentaire Decisioning et elles sont disponibles à la demande pour les autres organisations (disponibilité limitée).</p>
<p>Cette fonctionnalité sera progressivement déployée pour tous les clients. En attendant, contactez votre représentant Adobe pour obtenir l’accès.</p>
<!--img src="assets/do-not-localize/FILE.gif"-->
<!-- p>For more information, refer to the <a href="../FILE.md">detailed documentation</a>.</p -->
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
<p>Vous pouvez désormais appliquer rapidement des thèmes préapprouvés pour garantir la cohérence de la marque dans tous les e-mails, accélérer le processus de création de vos campagnes et produire de manière autonome des e-mails de haute qualité tout en réduisant la dépendance à l’égard des équipes de conception.</p>
<p>Publiée auparavant en version bêta, cette fonctionnalité est désormais disponible pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<img src="assets/do-not-localize/themes.gif">
<p>Pour plus d’informations, consultez la <a href="../email/apply-email-themes.md">documentation détaillée</a>.</p>
<!--p>Availability date: October 22, 2025</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nouvelles alertes de Parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>De nouvelles alertes préconfigurées sont disponibles pour surveiller l’exécution de votre parcours :</p>
<ul><li><a href="../reports/alerts.md#alert-discard-rate">Taux de rejet du profil dépassé </a> : ratio de rejets de profil par rapport aux profils entrés au cours des 5 dernières minutes ayant dépassé le seuil</li>
<li><a href="../reports/alerts.md#alert-custom-action-error-rate">Taux d’erreur des actions personnalisées dépassé</a> : ratio des erreurs d’actions personnalisées par rapport aux appels HTTP réussis au cours des 5 dernières minutes ayant dépassé le seuil</li>
<li><a href="../reports/alerts.md#alert-profile-error-rate">Taux d’erreur de profil dépassé</a> : ratio de profils en erreur par rapport aux profils saisis au cours des 5 dernières minutes qui a dépassé le seuil.</li></ul> <p>Vous pouvez modifier les valeurs de seuil et vous abonner à des alertes individuelles au niveau du parcours et non globalement.</p>
<p>Pour plus d’informations, consultez la <a href="../reports/alerts.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 14 octobre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistant Métadonnées d’exécution</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une nouvelle fonction d’assistance « executionMetadata » est disponible dans l’éditeur de personnalisation. Il vous permet d’ajouter des informations contextuelles à toute action native et de les capturer dans un jeu de données pour les exporter vers des systèmes externes.</p>
<p>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en obtenir l’accès.</p>
<p>Pour plus d’informations, consultez la <a href="../personalization/functions/helpers.md#execution-metadata">documentation détaillée</a>.</p>
<p>Date de disponibilité : 13 octobre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>L’agent d’expérimentation est ici !</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Optimisé par <a href="https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator.html" target="_blank">Adobe Experience Platform Agent Orchestrator</a>, l’agent d’expérimentation est disponible dans Journey Optimizer. </p>
<p>L’agent d’expérimentation est un outil optimisé par l’IA qui modernise la manière dont vous pouvez exécuter et gérer des expériences numériques sur des sites web, des e-mails, des messages push et des applications. Cela vous permet d’exécuter des expériences plus efficacement, d’organiser les objectifs commerciaux et de générer des informations exploitables, en mettant en évidence ce qui a fonctionné, ce qui n’a pas fonctionné et où tester ensuite.</p>
<p>Pour plus d’informations, consultez la <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-experiment.html" target="_blank">documentation détaillée</a>.</p>
<p>Date de disponibilité : 10 octobre 2025</p>
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
<li>Pour augmenter la taille ou le volume, vous pouvez acheter le module complémentaire Pièces jointes PDF. Pour plus d’informations, contactez votre représentant ou représentante Adobe.</li>
</ul>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<p><img src="assets/do-not-localize/pdf-attachments.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../email/pdf-attachments.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 30 septembre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>API publique pour récupérer les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une nouvelle API Journey Optimizer est désormais disponible pour récupérer les parcours et leurs objets associés tels que les campagnes et les surfaces.</p>
<p>Pour plus d’informations, consultez la <a href="https://developer.adobe.com/journey-optimizer-apis/references/journeys-retrieve/">documentation détaillée</a>.</p>
<p>Date de disponibilité : 25 septembre 2025</p>
</td>
</tr>
</tbody>
</table>




<!--
## Latest updates {#updates-rn}

New capabilities and improvements released in the past weeks are listed below, with their availability date. They will be grouped with the next release notes content at the end of the month. See also the latest [release notes below](#latest-rn).
-->

### Améliorations {#updates-improvements}

**Champ d’exécution pour le canal WhatsApp**

Outre les e-mails et les SMS, vous pouvez savoir mettre à jour le champ d’exécution par défaut de vos diffusions WhatsApp au niveau du sandbox. Il est également possible de remplacer le champ d&#39;exécution défini globalement en le modifiant dans les paramètres avancés de l&#39;activité parcours WhatsApp ou dans la configuration du canal WhatsApp. <!-- [Read more](../FILE.md) -->

**Prise en charge des attributs personnalisés pour l’adresse Mailto (unsubscribe)**

Avec Journey Optimizer, si vous gérez le consentement en dehors d’Adobe, vous pouvez définir des points d’entrée personnalisés externes en définissant votre propre lien de désabonnement en un clic et une adresse e-mail de désabonnement personnalisée dans la configuration du canal e-mail. Lorsque les personnes destinataires cliquent sur le lien de désabonnement, Journey Optimizer ajoute certains paramètres par défaut, spécifiques au profil, à l’événement de mise à jour du consentement.

Pour personnaliser davantage vos points d’entrée personnalisés, vous pouvez maintenant définir des attributs personnalisés qui seront également ajoutés à l’événement de consentement. [En savoir plus](../email/list-unsubscribe.md#custom-attributes)

>[!AVAILABILITY]
>
>Cette fonctionnalité est déjà disponible pour l’URL de désabonnement en un clic personnalisée **[!UICONTROL One-click Unsubscribe URL]** depuis le 25 août et est désormais disponible pour l’option **[!UICONTROL Mailto (unsubscribe)]** en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en obtenir l’accès.

Date de disponibilité : 6 octobre 2025

## Notes de mise à jour de septembre 2025 {#latest-rn}

**Date de publication** : 23 et 24 septembre 2025

### Nouvelles fonctionnalités {#sept-25-9-features}

<table>
<thead>
<tr>
<th><strong>Experimentation Accelerator de Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Experimentation Accelerator de Journey Optimizer est un produit IA conçu pour faire passer votre expérimentation au niveau supérieur. Conçu pour les utilisateurs et utilisatrices d’Adobe Journey Optimizer et d’Adobe Target, il unifie la gestion des expériences, fournit des informations et des opportunités optimisées par l’IA et introduit un nouvel agent d’expérimentation.</p>
<p>Vous pouvez vous attendre aux points suivants :</p>
<ul>
<li><strong>Inventaire d’expériences unifié :</strong> permet d’afficher, de filtrer et de gérer rapidement toutes les expériences d’Adobe Journey Optimizer et d’Adobe Target dans un espace de travail central.</li>
<li><strong>Informations et opportunités des expériences IA :</strong> allez au-delà des lectures statistiques avec des informations et des recommandations pilotées par GenAI. Chaque expérience fait désormais apparaître des opportunités exploitables, accompagnées d’une justification, afin que les équipes puissent décider en toute confiance de la suite des tests.</li>
<li><strong>Prise en charge du bandit manchot (MAB) dans Journey Optimizer :</strong> optimisez l’impact tout en réduisant le trafic gâché grâce aux expériences de bandit manchot. Au lieu de répartir les audiences de manière égale, MAB affecte automatiquement davantage de visiteurs et visiteuses aux variations les plus performantes en temps réel, afin que vous puissiez offrir de meilleures expériences à davantage de clientes et clients, tout en découvrant ce qui fonctionne.</li></ul>
<p><img src="assets/do-not-localize/experimentation-accelerator.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../content-management/experiment-accelerator.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 3 octobre 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>L’agent Journey est là !</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Optimisé par <a href="https://experienceleague.adobe.com/fr/docs/experience-cloud-ai/experience-cloud-ai/agents/agent-orchestrator" target="_blank">Adobe Experience Platform Agent Orchestrator</a>, l’agent Journey est disponible dans Journey Optimizer. Il permet d’analyser les parcours par le biais d’une interface en langage naturel. L’agent détecte les conflits d’audience ou de planning et les rejets de profils dans un parcours afin de vous permettre de prendre des mesures pour les résoudre. Vous pourrez bientôt créer des parcours avec l’aide d’un agent.</p>
<p>Pour plus d’informations, consultez la <a href="https://experienceleague.adobe.com/fr/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent-analyze" target="_blank">documentation détaillée</a>.</p>
<p>Date de disponibilité : 24 septembre 2025</p>
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
<th><strong>Utiliser les données Adobe Experience Platform pour la personnalisation et la prise de décision</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Publiée précédemment en version Beta publique, cette fonctionnalité est désormais disponible dans tous les environnements. Les améliorations suivantes ont été apportées à cette version :</p>
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


### Améliorations {#sept-25-9-improvements}

* **Prise en charge des webhooks pour les campagnes déclenchées par API**\
  Les campagnes déclenchées par API prennent désormais en charge les webhooks. Configurez une URL webhook pour recevoir des mises à jour en temps réel de l’état de chaque message, ce qui améliore l’observabilité et permet une surveillance et une automatisation transparentes. [En savoir plus](../configuration/feedback-webhooks.md)

  Date de disponibilité : 29 septembre 2025

* **Prise en charge de mTLS pour le canal SMS**
Lors de la configuration d’un fournisseur de SMS personnalisé, vous avez désormais la possibilité d’activer l’authentification TLS mutuelle (mTLS), qui nécessite que le client et le serveur confirment mutuellement leur identité avant qu’une connexion sécurisée ne soit établie. [En savoir plus](../sms/sms-configuration-custom.md) - Date de disponibilité : 23 septembre 2025

* **Schémas basés sur des modèles**\
  Les schémas basés sur des modèles peuvent désormais être utilisés pour prendre en charge vos besoins de modélisation relationnelle dans les campagnes orchestrées. [En savoir plus](../orchestrated/gs-schemas.md) - Date de disponibilité : 23 septembre 2025

* **Prise en charge de la recherche de jeux de données dans les parcours**\
  Une nouvelle activité dans les parcours, intitulée **Recherche de jeu de données**, permet de récupérer dynamiquement des données à partir de jeux de données d’enregistrement Adobe Experience Platform au moment de l’exécution. Grâce à cette fonctionnalité, vous pouvez accéder à des données qui peuvent ne pas figurer dans la payload de profil ou d’événement, ce qui garantit des interactions clients pertinentes et au moment opportun. [En savoir plus](../building-journeys/dataset-lookup.md) - Date de disponibilité : 23 septembre 2025

  Cette activité est disponible uniquement pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.

* **Prise en charge de la redirection dans les actions personnalisées de parcours**\
  Les redirections (302) sont désormais prises en charge dans les actions personnalisées de parcours. - Date de disponibilité : 23 septembre 2025

* **Alertes de surveillance de la configuration des canaux** : vous pouvez désormais vous abonner pour recevoir des alertes système, soit par e-mail, soit dans le centre de notifications Journey Optimizer, en cas d’erreur de configuration du canal e-mail utilisant le type de délégation de sous-domaine personnalisé. [En savoir plus](../reports/alerts.md#alert-channel-config-failure) - Date de disponibilité : 23 septembre 2025

* **Demandes de désabonnement en un clic** : nous avons apporté des améliorations qui renforcent encore davantage le traitement des demandes de désabonnement en un clic configurées sous Adobe Managed, en garantissant un traitement fiable et cohérent. - Date de disponibilité : 23 septembre 2025

* **Les paramètres de corps JSON imbriqués sont désormais pris en charge dans l’authentification personnalisée.**\
  Lors de la configuration de l’authentification personnalisée pour une action personnalisée, les objets JSON imbriqués (par exemple, les sous-objets dans `bodyParams`) sont désormais pris en charge. [En savoir plus](../datasource/external-data-sources.md#custom-authentication-mode) - Date de disponibilité : 18 septembre 2025

* **Fréquence du capping redéfini à l’heure** : vous pouvez désormais appliquer un capping de la fréquence à l’heure pour les jeux de règles de canal. Auparavant proposée en disponibilité limitée, cette fonctionnalité est désormais proposée pour tous les environnements et permet de choisir une heure (auparavant trois heures). [En savoir plus](../conflict-prioritization/channel-capping.md) - Date de disponibilité : 17 septembre 2025

* **Simulation des variations de contenu pour tous les canaux entrants**\
  Auparavant uniquement disponible pour les canaux E-mail, SMS et Notification push, la simulation de variations de contenu s’applique désormais également à tous les canaux entrants. [En savoir plus](../test-approve/simulate-sample-input.md) - Date de disponibilité : 17 septembre 2025

* **Expression pour les règles de limitation de prise de décision** : vous pouvez désormais créer vos propres expressions pour définir le seuil d’une règle de limitation pour un élément de décision. [En savoir plus](../experience-decisioning/items.md#capping) - Date de disponibilité : 16 septembre 2025

* **Prise en charge des domaines dynamiques** : Journey Optimizer prend désormais en charge la personnalisation complète/de base des URL pour les domaines prédéfinis acceptés par Adobe. [En savoir plus](../personalization/personalization-build-expressions.md#where) - Date de disponibilité : 12 septembre 2025

  Cette fonctionnalité est proposée en disponibilité limitée pour un certain nombre de clientes et clients.

* **Webhooks** - Cette version introduit les améliorations suivantes pour les Webhooks lors de la configuration d’un fournisseur de SMS personnalisé :

   * Vous pouvez maintenant définir l’objectif de votre webhook, soit Entrant, soit Commentaires, en fonction du type de données que vous souhaitez capturer. [En savoir plus](../sms/sms-configuration-custom.md#webhook) - Date de disponibilité : 23 septembre 2025

   * L’interface de configuration des mots-clés a été améliorée afin de faciliter la configuration. [En savoir plus](../sms/sms-configuration-custom.md#webhook) - Date de disponibilité : 23 septembre 2025

* **SMS**

   * Lors de la configuration d’un fournisseur de SMS personnalisé, vous pouvez désormais définir un mot-clé **Default** utilisé lorsqu’un SMS entrant contient un mot-clé non reconnu. Vous pouvez également créer des mots-clés **personnalisés** pour des actions spécifiques. [En savoir plus](../sms/sms-configuration-custom.md) - Date de disponibilité : 23 septembre 2025

   * Vous pouvez désormais accéder aux réponses par mots-clés entrants non définies qui sont envoyées par l’intermédiaire d’un SMS, y compris les fautes de frappe, les mots ou les phrases qui ne sont pas explicitement définis dans la configuration. Elles sont stockées pendant 13 mois dans le jeu de données **Événement d&#39;expérience de tracking d&#39;e-mail AJO**, sous **InboundMessage**. Disponible uniquement avec Sinch, Infobip et le fournisseur de SMS personnalisé. - Date de disponibilité : 23 septembre 2025

<!--
* **Approval policy permissions**
  Added an option when creating or setting Approval Policy to prevent Journey/Campaign creators from approving their own objects. [Read more](../test-approve/approval-policies.md) - Availability date: Sept 23, 2025-->

<!--
### Coming soon {#sept-25-9-soon}

In the next few days, the following capabilities and enhancements are scheduled for release. **Information is subject to change**. Updated links, screens, and documentation will be shared once these updates are live in production.

<table>
<thead>
<tr>
<th><strong>New Web Push notifications channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now supports Web Push notifications, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both mobile and desktop browsers, enabling you to reach customers directly on their devices without requiring an app.</p>
<p>This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same authoring workflows and targeting capabilities already available for mobile push.</p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom action monitoring and reporting</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Custom action monitoring and reporting is now available. This capability provides better visibility into journey health and execution, including lifecycle status and performance alerts. You can now quickly understand when, where, and why an anomalous situation is occurring in a custom action.</p>
<p>For more information, refer to the <a href="../FILE.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</td>
</tr>
</tbody>
</table>

<table>
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
</table>


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
<p>This capability is available in Limited Availability. Contact your Adobe representative to gain access.</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>For more information, refer to the <a href="../landing-pages/lp-forms.md">detailed documentation</a></p>
<p>Availability date: Sept XX, 2025</p>
</td>
</tr>
</tbody>
</table>
-->
