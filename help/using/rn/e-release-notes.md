---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour préliminaires pour Journey Optimizer
description: Notes de mise à jour préliminaires pour Adobe Journey Optimizer
feature: Release Notes
hide: true
exl-id: 6e7d1300-8efd-4fdc-90e3-3ccdc3babd2f
source-git-commit: b12904ef889530ebe7fc1962148e06b810908d18
workflow-type: tm+mt
source-wordcount: '2084'
ht-degree: 15%

---

# Notes de version préliminaire {#e-release-notes}

Adobe Journey Optimizer offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées à la fin de chaque mois dans les [notes de mise à jour](release-notes.md).

## Notes de version préliminaire d’avril 2026 {#april-26-rn}

**Les notes de version préliminaire ci-dessous peuvent être modifiées sans préavis jusqu’à la date de publication**. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les notes de mise à jour, à la date de publication.

Voir également les [Notes de mise à jour préliminaires d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Date de publication** : 28-29 avril 2026

### Nouvelles fonctionnalités {#april-26-features}


<table>
<thead>
<tr>
<th><strong>simulation de parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez maintenant définir votre parcours sur <strong> Simulation </strong>. Ce mode permet de valider la logique à l’aide d’<strong> utilisateurs simulés </strong>. Il s’agit de profils temporaires créés spécifiquement pour la simulation, qui vous permettent de tester librement sans avoir à gérer de profils de test persistants dans Adobe Experience Platform.</p>
<p>Tâche JIRA de documentation : <a href="https://jira.corp.adobe.com/browse/DOCAC-14050">DOCAC-14050</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Paramètres expéditeur dans l’en-tête de l’e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Avec Journey Optimizer, vous pouvez désormais envoyer des e-mails lorsque l’entité d’émission (expéditeur) diffère de l’entité de création (de). Les clients de messagerie qui prennent en charge cette fonctionnalité l’affichent généralement sous la forme « Expéditeur au nom de l’expéditeur » ou affichent un indicateur « via ». Renseignez les champs facultatifs <strong>En-têtes de l’expéditeur</strong> dans les paramètres du canal e-mail pour configurer cette fonctionnalité.</p>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Tâche JIRA de documentation : <a href="https://jira.corp.adobe.com/browse/DOCAC-14458">DOCAC-14458</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Champ CC dans les paramètres du canal e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais configurer un champ CC (copie carbone) facultatif dans les paramètres de votre canal e-mail. Contrairement aux destinataires en Cci, les destinataires en Cci sont visibles par le destinataire principal, ce qui permet une communication transparente et une propriété plus claire.</p>
<p>Vous pouvez ainsi copier automatiquement la bonne personne concernée sur chaque message, tel qu’un responsable de relation ou un propriétaire de compte, tout en vous assurant que le client sait à qui s’adresser pour le suivi.</p>
<p>Le champ CC prend en charge la personnalisation, de sorte qu’une configuration unique peut acheminer dynamiquement les copies en fonction des données de profil, ce qui la rend évolutive sur plusieurs cas d’utilisation sans configuration supplémentaire.</p>
<p>Tâche JIRA de documentation : <a href="https://jira.corp.adobe.com/browse/DOCAC-14581">DOCAC-14581</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Dossiers pour les parcours et les campagnes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais organiser vos parcours et campagnes dans des <strong>dossiers</strong> pour améliorer la navigation et la gestion dans l’interface.</p>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Tâche JIRA de documentation : <a href="https://jira.corp.adobe.com/browse/DOCAC-14038">DOCAC-14038</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Intégration de l’agent Journey Optimizer AI via MCP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer fournit désormais un serveur <strong>MCP (Model Context Protocol)</strong> qui surfacie les opérations de campagne, de fidélité et de sandbox directement dans toute application compatible MCP. Grâce à cette intégration, différentes personnes peuvent collaborer autour des mêmes données d’orchestration. Au lieu d’écrire des requêtes sur l’API REST AJO ou de parcourir plusieurs écrans d’interface utilisateur, vous pouvez décrire votre intention par la conversation et laisser le gestionnaire de ligne de commande appeler les outils MCP appropriés. Cette fonctionnalité est actuellement disponible dans Claude Web et Desktop.</p>
<p>Cette fonctionnalité est disponible pour tous les clients dans Public Beta.</p>
<p>Tâche JIRA de documentation : <a href="https://jira.corp.adobe.com/browse/DOCAC-14509">DOCAC-14509</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Copie de sandbox pour les campagnes orchestrées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>L’outil Sandbox</strong> prend désormais en charge l’exportation et l’importation de <strong>Campagnes orchestrées</strong> entre les sandbox via des packages.</p>
<p>Tâche JIRA de documentation : <a href="https://jira.corp.adobe.com/browse/DOCAC-13760">DOCAC-13760</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Activité Requête incrémentale dans les campagnes orchestrées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’activité <strong> Requête incrémentale </strong> est désormais disponible dans les <strong>Campagnes orchestrées</strong>. Cette activité de ciblage exécute votre requête à chaque exécution de la campagne et renvoie uniquement les enregistrements qui n’ont pas été renvoyés lors d’une exécution précédente. Vous pouvez envoyer des messages ou exporter uniquement les nouvelles inscriptions, les nouveaux membres Gold ou d’autres segments « nouveau depuis la dernière exécution » sans cibler à nouveau les mêmes profils.</p>
<p>Tâche JIRA de documentation : <a href="https://jira.corp.adobe.com/browse/DOCAC-14262">DOCAC-14262</a></p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Parcours Arbitration - AI Models</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais utiliser les <strong>modèles d’IA</strong> dans vos <strong>formules de classement</strong> pour améliorer automatiquement les <strong>scores de priorité de parcours </strong> en fonction des attributs du profil client et des facteurs contextuels, afin que les clients puissent accéder aux parcours les plus pertinents.</p>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Tâche JIRA de documentation : <a href="https://jira.corp.adobe.com/browse/DOCAC-14295">DOCAC-14295</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Optimisation des e-mails pour les boîtes de réception d’IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer comprend désormais une nouvelle fonctionnalité qui garantit que vos e-mails sont structurés de manière optimale pour les boîtes de réception optimisées par l’IA telles qu’Apple Intelligence et Google Gemini dans Gmail. Comme les assistants d’IA contrôlent de plus en plus la manière dont les destinataires lisent et agissent sur les e-mails, cette fonctionnalité vous permet de créer du contenu qui s’exécute correctement dans les tâches d’IA en aval, notamment la synthèse, le tri, la hiérarchisation et l’extraction d’intention.</p>
<p><img src="assets/do-not-localize/optimize-for-ai.gif"></p>
<p>Pour plus d’informations, voir <a href="../email/llm-email-optimizer.md">Optimisation des e-mails pour les boîtes de réception IA</a>.</p>
<p>Date de disponibilité : samedi 17 avril 2026</p>
<!--
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14520">DOCAC-14520</a></p>
-->
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Journey fragments</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Journey fragments</strong> are reusable sets of journey nodes that you can build once and drop into any journey across your sandbox. Whether it's an eligibility check, a preferred channel routing logic, or a welcome sequence, fragments help teams move faster and stay consistent — without rebuilding the same logic from scratch every time. Once created, fragments are stored in a dedicated <strong>Fragment inventory</strong> and can be inserted into any journey using the <strong>Journey fragments</strong> activity.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-11529">DOCAC-11529</a></p>
<p>Availability date: May 4, 2026</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Assistant AI pour les expressions Personalization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer comprend désormais un assistant AI pour les expressions de personnalisation. Vous pouvez l’ouvrir à partir de l’éditeur Personalization et de la barre d’outils Designer des e-mails lorsque vous concevez le contenu d’un e-mail. Décrivez en langage clair ce que vous souhaitez personnaliser et l’assistant génère une expression de personnalisation que vous pouvez utiliser en l’état ou affiner dans une courte conversation de suivi.
Vous pouvez également sélectionner un code de personnalisation existant et demander à l’assistant de l’expliquer, de le corriger ou de suggérer des améliorations. Une fois que vous avez généré une expression, l’option Afficher les aperçus des profils types exécute une vérification rapide par rapport à un ensemble limité de profils types synthétiques.</p>
<p>Pour plus d’informations, voir <a href="../content-management/generative-personalization-expressions.md">Assistant AI pour les expressions Personalization</a>.</p>
<p>Date de disponibilité : mardi 13 avril 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Boîte de réception</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Boîte de réception</strong> est une fonctionnalité mobile, disponible avec <strong>Cartes de contenu</strong>, qui permet aux clients de créer un emplacement centralisé dans leur application ou site web pour afficher les messages envoyés à leurs utilisateurs. Cela prolonge la durée de vie des communications marketing en s’assurant que les messages restent accessibles même après leur rejet.</p>
<p>Pour plus d’informations, consultez la <a href="../inbox/inbox-gs.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : mercredi 7 avril 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Expérimentation du chemin du parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Utilisez le nouveau nœud <strong>Optimiser</strong> pour exécuter des tests A/B ou des expériences de bandit à plusieurs bras afin de déterminer le meilleur moyen d’atteindre vos indicateurs de performance clés orientés métier. Cet outil vous permet de tester et de varier les communications, le séquencement et le timing afin d’atteindre au mieux vos clients. Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/path-experimentation.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : mercredi 7 avril 2026</p>
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
<p>Vous pouvez désormais utiliser <strong>Decisioning</strong> pour personnaliser et optimiser le contenu de vos e-mails. Tirez parti des <strong>scores de priorité</strong>, <strong>formules</strong> ou <strong>modèles d’IA</strong> pour afficher les offres et le contenu les plus pertinents pour chaque destinataire. Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale). Cette version de disponibilité générale prend désormais en charge les <strong>pages miroir</strong>.</p>
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/create-decision-policy.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : mardi 6 avril 2026</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#april-26-improv}

Les améliorations de cette version sont présentées ci-dessous.

#### IA

* **Score d’alignement de la marque dans le tableau de bord Campaign** - Vous pouvez désormais évaluer votre score d’alignement de la marque directement dans votre tableau de bord Campaign pour vous assurer que le contenu reste fidèle à la marque. Vous pouvez ainsi vérifier les directives en un coup d’œil sans avoir à ouvrir le concepteur de contenu.

  Tâche JIRA de documentation : [DOCAC-14516](https://jira.corp.adobe.com/browse/DOCAC-14516)

#### Prise de décision

* **Joindre des fragments aux éléments de décision** - Journey Optimizer permet désormais de joindre des fragments aux éléments de décision. Ils peuvent être utilisés dans des expériences basées sur du code et des campagnes par e-mail via des politiques de décision. Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).

  Tâche JIRA de documentation : [DOCAC-14452](https://jira.corp.adobe.com/browse/DOCAC-14452)

* **Fragments temporairement indisponibles sont ignorés** - Lors de l’utilisation de fragments dans des éléments de décision, si un fragment est temporairement indisponible sur Edge, il est ignoré et le parcours ou la campagne continue de s’afficher au lieu d’échouer. [En savoir plus](../experience-decisioning/fragments-decision-policies.md#temporary-unavailable-fragments)

  Date de disponibilité : mercredi 14 avril 2026

#### Conception d’e-mail

* **Éditeur HTML avancé pour le contenu d’e-mail** - Le mode HTML avancé vous permet de modifier la source HTML de votre contenu dans le Designer d’e-mail, d’ajouter des expressions avancées (comme des conditions) dans la source et de basculer entre les vues HTML et Bureau sans perdre vos modifications. Auparavant disponible uniquement pour les modèles de contenu d’e-mail, cette fonctionnalité est désormais déployée sur le contenu **e-mail** dans le Designer d’e-mail. Il est actuellement à disponibilité limitée. Contactez votre représentant Adobe pour y accéder. [En savoir plus](../email/email-expert-mode.md)

  Date de disponibilité : vendredi 9 avril 2026

#### SMS

* **Nombre de caractères** - Dans Adobe Journey Optimizer, vous pouvez désormais utiliser le nombre de caractères pour surveiller la longueur de vos SMS en temps réel. Cela vous permet de savoir quand un message sera divisé en plusieurs segments afin de mieux gérer la mise en forme et d’éviter des augmentations inattendues des coûts d’envoi. [En savoir plus](../sms/create-sms.md)

  Tâche JIRA de documentation : [DOCAC-14346](https://jira.corp.adobe.com/browse/DOCAC-14346)

* **Opt-out et consentement au numéro de téléphone et à l’expéditeur** - Pour les SMS, Journey Optimizer enregistre désormais le consentement et l’opt-out marketing au niveau du numéro de téléphone et du numéro court du profil. Si le numéro de téléphone d’un profil change, le consentement lié au numéro précédent n’est pas transféré au nouveau. Le destinataire doit à nouveau donner son accord, en s&#39;assurant que tous les messages restent alignés avec le consentement au niveau du numéro et de l&#39;expéditeur spécifiques.

  Actuellement, cette fonctionnalité n’est disponible que pour les configurations SMS Sinch. [En savoir plus](../sms/sms-configuration-sinch.md)

  Tâche JIRA de documentation : [DOCAC-14344](https://jira.corp.adobe.com/browse/DOCAC-14344)

* **Prise en charge de la sélection de jeux de données personnalisés** - Les événements de SMS entrants peuvent être écrits dans un **jeu de données personnalisé** de votre choix, afin que les audiences et les parcours puissent utiliser ces données plus tôt que s’ils attendaient le chemin de retour de message par défaut et l’actualisation de l’audience en flux continu, ce qui est utile pour les **SMS bidirectionnels**. [En savoir plus](../sms/sms-webhook.md)

  Tâche JIRA de documentation : [DOCAC-14356](https://jira.corp.adobe.com/browse/DOCAC-14356)

* **Amélioration de l’interface Webhook** - Lors de la configuration des Webhooks SMS, l’interface utilisateur comprend désormais un guide de configuration intégré avec des exemples pratiques, ce qui facilite l’alignement des payloads des fournisseurs et la résolution des problèmes sans quitter le flux de configuration. [En savoir plus](../sms/sms-webhook.md)

  Tâche JIRA de documentation : [DOCAC-14589](https://jira.corp.adobe.com/browse/DOCAC-14589)

#### WhatsApp

* **Boutons interactifs et suivi WhatsApp** - WhatsApp dans Journey Optimizer prend désormais en charge les boutons interactifs requis par vos modèles et cas d’utilisation, ainsi que le suivi d’interaction intégré afin que vous puissiez mesurer l’engagement et analyser les performances parallèlement à vos autres rapports de canal.

  Tâche JIRA de documentation : [DOCAC-14590](https://jira.corp.adobe.com/browse/DOCAC-14590)

#### Optimisation du chemin de parcours

* **Type d’expérience** - Vous pouvez désormais choisir entre une expérience A/B (division fixe au début) ou un bandit manchot (division automatique avec mises à jour hebdomadaires du poids) lors de la configuration d’une expérience de chemin. [En savoir plus](../building-journeys/path-experimentation.md)

  Date de disponibilité : mercredi 7 avril 2026

* **Expérimentation de parcours : mettre à l’échelle le gagnant** - Vous pouvez désormais déployer automatiquement ou manuellement le parcours gagnant d’une expérience sur l’ensemble de votre audience. Une fois qu’un gagnant est déterminé, vous pouvez amplifier sa portée et son efficacité sans surveiller constamment l’expérience. Cette fonctionnalité n’est disponible que dans les parcours unitaires (déclenchés par un événement et qualifications d’audience). [En savoir plus](../building-journeys/path-experimentation.md#scale-winner)

  Date de disponibilité : mercredi 7 avril 2026

* **Conditions** - L’activité [Optimiser](../building-journeys/optimize.md) est le nouveau moyen de créer des chemins conditionnels dans les parcours. Elle remplace l’ancienne activité **Condition**. Toute la logique conditionnelle est conservée et est désormais gérée via les conditions de l’activité **Optimiser**. Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale). [En savoir plus](../building-journeys/conditions.md)

  Date de disponibilité : mercredi 7 avril 2026

#### Intégrations Adobe Experience Manager

* **Sélecteur de gestionnaire d’accès** - Les sélecteurs Adobe Experience Manager Assets et Fragment de contenu sont désormais remplacés par le **sélecteur de gestionnaire d’accès**, une fenêtre modale unifiée qui vous permet de parcourir, rechercher, filtrer et accéder à tous les fragments de contenu AEM Assets et AEM. La prise en charge des rendus Dynamic Media est également incluse, ce qui vous permet d’ajouter des rendus d’image à partir de l’interface utilisateur lorsque des ressources Dynamic Media sont sélectionnées. Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).

  Tâche JIRA de documentation : [DOCAC-13802](https://jira.corp.adobe.com/browse/DOCAC-13802)

* **Personnalisation en temps ouvert avec compte à rebours à l’aide de Dynamic Media** l’intégration de Journey Optimizer et de Adobe Experience Manager Dynamic Media permet la personnalisation en temps ouvert des modèles Dynamic Media, ce qui déverrouille les cas d’utilisation hyper-personnalisés. Les clients peuvent créer et publier des modèles personnalisés dans Adobe Experience Manager et les utiliser dans Journey Optimizer, avec des données rendues au moment de l’ouverture.

  Tâche JIRA de documentation : [DOCAC-13801](https://jira.corp.adobe.com/browse/DOCAC-13801)

* **Prise en charge des variations de fragments de contenu Adobe Experience Manager** - Vous pouvez sélectionner **variations de fragments de contenu** (par exemple, variantes de langue ou de canal) lors de l’insertion de fragments de contenu Adobe Experience Manager, avec une gestion améliorée pour les scénarios régionaux et multilingues. Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe. [En savoir plus](../integrations/aem-fragments.md#aem-variations)

  Date de disponibilité : samedi 3 avril 2026

* **Contexte de fragment de contenu Adobe Experience Manager lors de la création** - Votre sélection de fragment de contenu reste active lorsque vous passez d’un champ de texte à un bloc de contenu. Vous pouvez ainsi ajouter d’autres champs de fragment sans rouvrir **Ouvrez le conseiller en contenu AEM** à chaque fois. Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe. [En savoir plus](../integrations/aem-fragments.md)

  Date de disponibilité : jeudi 1 avril 2026

<!--
#### WhatsApp

* **WhatsApp Channel: Embedded Sign Up** - Adobe Journey Optimizer now supports Meta's <strong>Embedded Sign Up</strong> flow for WhatsApp channel configuration. This streamlined onboarding experience allows you to connect your <strong>WhatsApp Business Account</strong> and phone numbers directly within the AJO interface, without navigating to <strong>Meta Business Manager</strong>, reducing setup time significantly. It also serves as a migration tool to transfer existing phone numbers and <strong>WhatsApp Business Accounts (WABAs)</strong> to Adobe.

  Documentation JIRA task: [DOCAC-13386](https://jira.corp.adobe.com/browse/DOCAC-13386)
-->

#### Configuration

* **Autorisations spécifiques pour les clés de chiffrement des paramètres d’URL** - Pour accéder aux clés de chiffrement des paramètres d’URL et les gérer, de nouvelles autorisations ont été créées. Vous devez maintenant disposer des autorisations **Afficher le registre des clés** et **Gérer le registre des clés** accordées.

  Tâche JIRA de documentation : [DOCAC-14490](https://jira.corp.adobe.com/browse/DOCAC-14490)

#### Campagnes orchestrées

* **Améliorations apportées à Data Modeler** - Pour les schémas relationnels orchestrés, Data Modeler prend désormais en charge la création de clés composites à l’aide de plusieurs champs. Les relations composites entre les tables sont créées lorsque vous chargez un schéma à partir d’un fichier DDL ou Excel. Dans la vue de relation d’entité, après le chargement d’un fichier, les liens composites affichent l’ensemble complet des paires de champs entre les tables.

  Tâche JIRA de documentation : [DOCAC-14334](https://jira.corp.adobe.com/browse/DOCAC-14334)

* **Variables globales dans les campagnes orchestrées** - Les campagnes orchestrées prennent désormais en charge les variables globales qui peuvent être définies une seule fois et réutilisées dans toutes les activités d’un workflow. Cela simplifie la configuration et garantit la cohérence des valeurs dynamiques, des expressions et de la personnalisation du contenu.

  Tâche JIRA de documentation : [DOCAC-14113](https://jira.corp.adobe.com/browse/DOCAC-14113)

<!--
## March '26 pre-release notes {#march-26-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: March 24-25, 2026

### New capabilities {#march-26-features}

<table>
<thead>
<tr>
<th><strong>LLM email optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now optimize your email content for deliverability using large language model (LLM) technology. The LLM email optimizer analyzes your email content and provides actionable recommendations to improve sender reputation, avoid spam filters, and enhance overall deliverability performance.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14340">DOCAC-14340</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Convert images to email content templates</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now convert images into email content templates directly in Journey Optimizer. Use AI-powered analysis to automatically generate structured HTML templates from visual references, significantly reducing email design time.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14324">DOCAC-14324</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Incremental query activity in Orchestrated Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Incremental query</strong> activity is now available in Orchestrated Campaigns. This activity queries only new or updated records since the last workflow execution, significantly reducing processing time and improving efficiency for recurring campaigns targeting large datasets.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14262">DOCAC-14262</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Transactional category in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>In Orchestrated campaigns, you can now set a channel activity to the <strong>Transactional</strong> category using the <strong>Category</strong> field. This applies transactional channel configurations to that activity and bypasses business rules for it.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14233">DOCAC-14233</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Test activity in Orchestrated Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Test</strong> activity is now available in Orchestrated Campaigns. This activity routes workflow execution to different branches based on defined conditions, enabling you to validate campaign logic and configurations before activating live deliveries.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14115">DOCAC-14115</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom forms in landing pages</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create <strong>custom forms</strong> in landing pages to collect specific subscriber data beyond standard opt-in fields. Define your own form fields, validation rules, and submission behaviors to support a wider range of subscription and profile enrichment use cases.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-13963">DOCAC-13963</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: Create Orchestrated Campaign use case</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Journey Agent</strong>, powered by Adobe Experience Platform Agent Orchestrator, can now create complete <strong>Orchestrated Campaign</strong> use cases through a natural language interface. Describe your campaign goal and requirements in plain language, and Journey Agent configures the campaign structure, activities, and targeting for you.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-13768">DOCAC-13768</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New profile acquisition in landing pages</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Landing pages now support <strong>new profile acquisition</strong> workflows, enabling you to capture and onboard new audience members directly from your landing page experiences. Configure acquisition forms to collect profile data and automatically provision new profiles in Adobe Experience Platform.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-13757">DOCAC-13757</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey path optimization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Journey path optimization</strong> uses AI to analyze historical journey performance and automatically select the best path for each customer, maximizing conversion and engagement outcomes.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-13492">DOCAC-13492</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisioning support in email channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use <strong>Decisioning</strong> to personalize and optimize the content of your email messages. Leverage Priority Scores, Formulas, or AI Models to display the most relevant offers and content to each recipient.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability). With this General Availability release, mirror pages are now supported.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-13182">DOCAC-13182</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Message inbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Message Inbox</strong> is now available in Adobe Journey Optimizer, providing a centralized view of received in-app, push, and SMS messages. Recipients can access and interact with all their messages in one place, enabling richer engagement and re-engagement scenarios.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-11382">DOCAC-11382</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Native channel action activities deprecated</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Following the General Availability of the <strong>Action activity</strong> in February 2026, legacy native channel action activities (Email, SMS, Push, In-App, etc.) in the journey canvas are now deprecated. Existing journeys using legacy channel activities continue to function without any changes or migration required.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14144">DOCAC-14144</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Dataset lookup support in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new activity in journeys, Dataset lookup, allows you to to dynamically retrieve data from Adobe Experience Platform record datasets during runtime. By leveraging this capability, you can access data that may not reside in the profile or event payload, ensuring your customer interactions are both relevant and timely. Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14351">DOCAC-14351</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Trigger orchestrated campaigns using API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now trigger an orchestrated campaign via API. Configure the target campaign as "Triggered by a signal" and publish it. Then use an API call to fire the campaign. The API call can include parameters that will be available as variables in the triggered campaign.</p>
<p>Documentation JIRA task: <a href="https://jira.corp.adobe.com/browse/DOCAC-14030">DOCAC-14030</a></p>
</td>
</tr>
</tbody>
</table>

### Improvements {#march-26-improv}

Improvements coming with this release are listed below.

#### Journeys

* **Journey Arbitration - AI Models** - In addition to ranking formulas, AI models can now be used with Journey Arbitration to automatically rank and prioritize journey entry for customers, using machine learning to determine the most relevant journey for each profile based on historical behavior and contextual signals. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.

  Documentation JIRA task: [DOCAC-14295](https://jira.corp.adobe.com/browse/DOCAC-14295)

#### Reporting

* **Exclude bot clicks for email and SMS reporting** - Email and SMS reporting now automatically filters out bot clicks from click metrics, providing more accurate engagement data and preventing automated traffic from inflating your performance figures.
  Documentation JIRA task: [DOCAC-14354](https://jira.corp.adobe.com/browse/DOCAC-14354)

* **Send-Time Optimization: updated controls location and new lift report** - Send-Time Optimization (STO) controls have been relocated to the Action configuration menu. Additionally, a new lift report is now available in Journeys reports to measure the impact of STO on your campaign performance metrics.

  Documentation JIRA task: [DOCAC-14335](https://jira.corp.adobe.com/browse/DOCAC-14335)

#### Email Designer

* **Open-time personalization using Dynamic Media (Beta)** - You can now personalize email content at open time using Adobe Dynamic Media assets, enabling real-time, recipient-specific images and visuals that are generated dynamically based on each recipient's attributes at the moment of email opening. This capability is currently in Beta.
  Documentation JIRA task: [DOCAC-14353](https://jira.corp.adobe.com/browse/DOCAC-14353)

* **Email Designer displayed in Unified Shell** - The Email Designer is now displayed within the Unified Shell experience, providing a consistent navigation and header experience that aligns with other Adobe applications.
  Documentation JIRA task: [DOCAC-14254](https://jira.corp.adobe.com/browse/DOCAC-14254)

* **Text mode support in fragments** - Fragments now support text mode editing, allowing you to create and manage plain text versions of your content fragments for use in text-based email workflows and multi-channel scenarios.
  Documentation JIRA task: [DOCAC-14204](https://jira.corp.adobe.com/browse/DOCAC-14204)

#### Decisioning

* **Expression Fragment Reference change feed support in Edge Decisioning** - This enhancement allows changes in fragment references to automatically be reflected in all items that reference fragments, without needing to refresh anything manually (republishing the campaign or decision policy).
  Documentation JIRA task: [DOCAC-14350](https://jira.corp.adobe.com/browse/DOCAC-14350)

* **Optional fragments in decision items** - Fragments attached to decision items can now be configured as optional, providing greater flexibility in content composition when not all decision item renderings require a specific fragment.
  Documentation JIRA task: [DOCAC-14309](https://jira.corp.adobe.com/browse/DOCAC-14309)

#### Configuration

* **URL parameters encryption** - URL parameters in tracking links and landing pages can now be encrypted, providing an additional layer of security for sensitive parameter data. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.
  Documentation JIRA task: [DOCAC-14349](https://jira.corp.adobe.com/browse/DOCAC-14349)

* **Folders for journeys and campaigns** - You can now organize your journeys and campaigns into folders, enabling structured navigation and easier management for teams working with large volumes of content. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.
  Documentation JIRA task: [DOCAC-14038](https://jira.corp.adobe.com/browse/DOCAC-14038)

#### Orchestrated campaigns

* **Target dimension simplification in Orchestrated Campaigns** - You can now easily select or automatically deduce the right targeting and secondary dimensions in Orchestrated campaigns for accurate, efficient audience activation.
  Documentation JIRA task: [DOCAC-13554](https://jira.corp.adobe.com/browse/DOCAC-13554)
-->

<!--
## February '26 pre-release notes {#feb-26-01-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: February 17, 2026

### New capabilities {#feb-26-01-features}

<table>
<thead>
<tr>
<th><strong>Wave sending of outbound messages</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can schedule outbound messages from <strong>campaigns</strong> or <strong>journeys</strong> to be delivered in controlled <strong>batches</strong> over time.</p>
<p>Wave sending offers the following benefits:</p>
<ul>
<li>Better <strong>deliverability</strong> – Spread sends over time to help maintain a strong <strong>sender reputation</strong> and reduce the risk of being flagged as spam.</li>
<li><strong>Load control</strong> – Avoid overwhelming downstream systems (e.g. call centers, landing pages) by limiting how many messages go out at once.</li>
<li>High-volume and time-sensitive use cases – Suited to large audiences or when you need to control timing (e.g. call center capacity, ramp-up, or time-bound offers).</li>
</ul>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey arbitration</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use <strong>formulas</strong> and <strong>AI models</strong> to automatically boost <strong>journey priority scores</strong> based on customer profile attributes and contextual factors, ensuring customers enter the most relevant journeys.</p>
<p>This capability is only available for a set of organizations (<strong>Limited Availability</strong>). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent: Channel Content Create</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Powered by <strong>Adobe Experience Platform Agent Orchestrator</strong>, <strong>Journey Agent</strong> is available in Journey Optimizer and enables you to analyze journeys through a <strong>natural language interface</strong>. You can now also generate and manage channel-specific content directly in Journey Agent, creating content for channels such as email and push, applying and previewing templates, refining tone and style through prompts, and opening content in <strong>Content Designer</strong> for in-context editing.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Mobile Live Activities</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Live Activities</strong> provide <strong>real-time updates</strong> and interactive experiences within mobile apps, allowing users to stay informed about ongoing events or tasks directly on their device's screen. This feature enhances engagement by delivering live information, such as progress tracking, event updates, or interactive content, without requiring users to open the app.</p>
<p>Previously released in beta, this capability is now available to all environments (<strong>General Availability</strong>).</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Action activity in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer supports a new generic <strong>Action activity</strong> that enables you to configure both single actions and <strong>multi-action inbound action groups</strong>, allowing for streamlined action configuration within the <strong>journey canvas</strong>. In particular, this new feature allows for:</p>
<ul>
<li>A simplified native action configuration within the journey canvas.</li>
<li>The capacity to create multi-action inbound action groups.</li>
<li>The ability to add <strong>optimization</strong> to any built-in channel action.</li>
<li>The ability to add both <strong>experimentation</strong> and <strong>multilingual</strong> options to any action.</li>
</ul>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
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
<p>Adobe Journey Optimizer now supports <strong>Web Push notifications</strong>, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both mobile and desktop browsers, enabling you to reach customers directly on their devices without requiring an app. This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same <strong>authoring workflows</strong> and <strong>targeting capabilities</strong> already available for mobile push.</p>
<p>Previously released in beta, this capability is now available to all environments (<strong>General Availability</strong>).</p>
<p>Availability date: February 13, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Content decision activity</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Content decision activity</strong> is now available in the <strong>journey canvas</strong> for integrating <strong>personalized offers</strong> directly into your customer journeys. This activity enables you to deliver decision-based content and reference those offers throughout your journey—in conditions for creating eligibility-based branching, in custom actions for passing offer data to external systems, and in other activities for building fully personalized customer experiences.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (<strong>General Availability</strong>).</p>
<p><img src="assets/do-not-localize/content-decision.gif"/></p>
<p>For more information, refer to the <a href="../building-journeys/content-decision.md">detailed documentation</a>.</p>
<p>Availability date: February 11, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Self-service migration tooling APIs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Migration tooling APIs</strong> are now available to programmatically migrate <strong>Decision management</strong> entities to <strong>Decisioning</strong>, featuring:</p>
<ul>
<li>Flexible migration scopes (<strong>sandbox</strong>, <strong>offer</strong>, or <strong>decision</strong> level)</li>
<li>Automated <strong>dependency analysis</strong> and validation</li>
<li><strong>Rollback support</strong> for completed migrations</li>
<li>Detailed migration reports with object mappings</li>
</ul>
<p>For more information, refer to the <a href="../experience-decisioning/decisioning-migration-api.md">detailed documentation</a>.</p>
<p>Availability date: February 3, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom action monitoring</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gain deeper insight into the health and performance of your <strong>custom action endpoints</strong> with a new <strong>monitoring dashboard</strong> and enriched <strong>journey step event data</strong>. Track successful calls, errors, throughput, response times, and queue wait times to quickly understand when, where, and why anomalies occur.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (<strong>General Availability</strong>).</p>
<p>For more information, refer to the <a href="../action/reporting.md">detailed documentation</a>.</p>
<p>Availability date: February 3, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisioning support in SMS channel</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now personalize and optimize the content of your <strong>SMS messages</strong> with <strong>Decisioning</strong>. Use <strong>Priority Scores</strong>, <strong>Formulas</strong>, or <strong>AI Models</strong> to display the best content to your customers.</p>
<p>For more information, refer to the <a href="../experience-decisioning/create-decision.md">detailed documentation</a>.</p>
<p>Availability date: February 2, 2026</p>
</td>
</tr>
</tbody>
</table>

### Improvements {#feb-26-01-improv}

Improvements coming with this release are listed below.

#### Configuration

* **Experience event usage in journey expressions** - Starting April 1, 2026, the use of experience event attributes in journey expressions will no longer be supported for organizations that have not used this capability in the last 90 days. This capability has already been unavailable for new customer organizations since July 8, 2025. For alternatives, see [Experience event lookup in journeys](../building-journeys/exp-event-lookup.md).


* **Subdomain delegation method switching** - You can now switch from one <strong>subdomain delegation</strong> method to another. This enables you to migrate domains using the <strong>CNAME delegation</strong> mode to the <strong>custom delegation</strong> method to adhere to your company's security policies.

  **Note**: This capability is only available for a set of organizations (<strong>Limited Availability</strong>). To gain access, contact your Adobe representative.


#### Email Designer

* **Use a brand theme to convert an image to an email template** - When converting an image to an email template in Journey Optimizer, you can now use a <strong>theme</strong> as input so the generated HTML follows your <strong>brand parameters</strong>. Styling such as background color, button color, fonts, line spacing, margins, and padding is applied automatically, reducing manual design work and delivering a template that is ready to use with minimal edits.


* **Update brands with new color tab** - <strong>Brand guidelines</strong> help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors section</strong> defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity.


#### AI

* **Integration of custom Firefly models and third-party image generation models** - Enable seamless integration of standard and custom <strong>Firefly models</strong>, along with approved <strong>third-party image models</strong> (e.g., NanoBanana), to provide greater flexibility, control, and brand alignment when generating images. This allows you to select the best model for each use case: standard Firefly for general needs, custom Firefly for on-brand generation, or approved third-party models for specialized or experimental scenarios.


#### Experience Decisioning

* **Edge inbound support for using Adobe Experience Platform data in Decisioning** - Decisioning support of <strong>Experience Platform data lookup</strong> now includes <strong>edge inbound</strong> channel use cases. The capability remains in Limited Availability; General Availability of the underlying data lookup feature is not yet announced (AEP/product dependency).

  **Note**: This capability is only available for a set of organizations (<strong>Limited Availability</strong>). To gain access, contact your Adobe representative.


* **Experience Decisioning preview in Code-based Experience channel** - You can now preview <strong>decision items</strong> when configuring <strong>Experience Decisioning</strong> with the <strong>Code-based Experience</strong> channel. Preview is available directly in the authoring interface before going live.


* **Offer Ranking AI Model Observability** - Journey Optimizer now allows you to monitor the <strong>health</strong>, <strong>training status</strong>, and <strong>performance</strong> of your <strong>AI models</strong> in Decisioning—so you can verify training success, troubleshoot failures, and understand impact on your outcomes. This capability is available for personalized optimization models only (not auto-optimization).


* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach <strong>fragments</strong> to <strong>decision items</strong> which can be leveraged in code-based experience campaigns through <strong>decision policies</strong>.

  **Note**: Previously released in Limited Availability, this capability is now available to all environments (General Availability).

  Availability date: February 12, 2026.


#### Journeys

* **Multiple inbound actions in journeys** - To simplify your journey orchestration, you can now define several <strong>inbound actions</strong> in a single journey. Previously available in campaigns, this capability enables you to deliver multiple <strong>code-based experiences</strong>, <strong>in-app messages</strong>, <strong>content cards</strong>, or <strong>web actions</strong> to different locations at the same time, each action containing specific content.

  **Note**: Previously released in Limited Availability, this capability is now available to all environments (General Availability).


* **SMS Webhooks** - <strong>Webhooks</strong> are now supported across all SMS providers. You can configure each webhook based on its intended purpose: <strong>Inbound webhooks</strong> to capture incoming messages and <strong>Feedback webhooks</strong> to receive delivery receipts, status updates, and other message-related events. [Read more](../sms/sms-webhook.md)

  Availability date: February 2, 2026.
-->
<!--
## January '26 pre-release notes {#jan-26-01-rn}

**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: January 27, 2026

### New capabilities {#jan-26-01-features}

<table>
<thead>
<tr>
<th><strong>Action activity in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer supports a new generic <strong>Action activity</strong> that enables you to configure both single actions and <strong>multi-action inbound action groups</strong>, allowing for streamlined action configuration within the journey canvas. In particular, this new feature allows for:</p>
<ul>
<li>A simplified native action configuration within the journey canvas.</li>
<li>The capacity to create multi-action inbound action groups.</li>
<li>The ability to add optimization to any built-in channel action.</li>
<li>The ability to add both experimentation and multi-lingual options to any action.</li>
</ul>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-111916">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Custom action monitoring</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Gain deeper insight into the health and performance of your custom action endpoints with a new <strong>monitoring dashboard</strong> and enriched journey step event data. Track successful calls, errors, throughput, response times, and queue wait times to quickly understand when, where, and why anomalies occur.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-126869">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Quiet Hours / Time Based Exclusions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Quiet hours let you define <strong>time-based exclusions</strong> for Email, SMS, Push, and WhatsApp channels. They ensure that no messages are sent during specific periods of time, helping you respect customer preferences and compliance requirements. You can apply quiet hours through <strong>rule sets</strong>, which can be assigned to individual actions in campaigns or journeys for precise control.</p>
<p>Previously released in Limited Availability, this feature is now available to all environments. With this General Availability release, the feature now includes the ability for customer to queue a campaign action until the completion of Quiet Hours, and the ability to preview the activated Quiet Hours rule.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-63912">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Direct Mail channel in journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Previously limited to Campaigns, the <strong>Direct Mail channel</strong> is now available on the <strong>journey canvas</strong>, enabling you to incorporate Direct Mail into your journeys. Direct Mail can now be used in both batch and 1:1 journey scenarios, with support for file extraction configuration and time-based frequency settings.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-38399">Link to PRODUCT JIRA task</a></p>
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
<p>Adobe Journey Optimizer now supports <strong>Web Push notifications</strong>, expanding the push channel beyond mobile. You can seamlessly deliver notifications to both mobile and desktop browsers, enabling you to reach customers directly on their devices without requiring an app. This enhancement allows you to engage users with timely, personalized messages in real time, leveraging the same authoring workflows and targeting capabilities already available for mobile push.</p>
<p>Previously released in Limited Availability, this capability is now available to all environments (General Availability).</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-37866">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Decisioning support in Push and SMS channels</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now add <strong>Decision policies</strong> into push and SMS journeys and campaigns. Decision policies are containers for your offers that leverage the Decisioning engine to dynamically return the best content to deliver for each audience member.</p>
<p>This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-55817">Link to PRODUCT JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-55818">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Direct mail channel in Orchestrated campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Direct mail channel is now available in orchestrated campaigns. The <strong>Direct mail activity</strong> facilitates direct mail sending within your Orchestrated campaign, for both one-time and recurring messages. It serves to automate the process of generating the <strong>extraction file</strong> required by direct mail providers. You can combine channel activities into the Orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-82584">Link to PRODUCT JIRA task</a></p>
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
<p>New <strong>source connectors</strong> are now available in Adobe Experience Platform for the Talon.One, Capillary and Kobie loyalty Apps. These connectors let you seamlessly stream loyalty data into Adobe Experience Platform and leverage these data in Journey Optimizer.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Message Export</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Message Export</strong> capability is now available for email and SMS channels. This feature allows you to automatically export sent message content to a dedicated Experience Platform dataset, enabling you to:</p>
<ul>
<li>Meet regulatory compliance requirements (such as HIPAA)</li>
<li>Archive messages for legal claims and customer care inquiries</li>
<li>Retain copies of personalized content sent to individuals</li>
</ul>
<p>Records are retained in the AJO Message Export Dataset for <strong>7 calendar days from ingestion</strong>. During this retention period, you can export the data to your own storage via Experience Platform destinations. The feature is enabled at the channel configuration level, giving you granular control over which messages are exported.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-105313">Link to PRODUCT JIRA task</a></p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent - Create a Journey</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Create Agent enables Journey Optimizer users to build and configure marketing journeys using a natural language interface. With Journey Create Agent, practitioners can quickly create journeys by describing their requirements in conversational prompts. The agent streamlines journey creation, allowing marketers to focus on strategy rather than technical configuration.</p>
<p><a href="https://experienceleague.adobe.com/en/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent#journey-create-agent-skill-overview-and-user-guide" target="_blank">Learn more</a></p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-95142">Link to PRODUCT JIRA task</a></p>
<p>Availability date: January 12, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New API to retrieve Action Campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>A new <strong>Journey Optimizer API</strong> is now available, enabling you to programmatically retrieve and inspect campaign-related data such as details, versions, and configurations.</p>
<p>For more information, refer to the <a href="https://developer.adobe.com/journey-optimizer-apis/references/campaigns-retrieve/">detailed documentation</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-96195">Link to PRODUCT JIRA task</a></p>
<p>Availability date: November 24, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>New journey alerts</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Three new <strong>journey alerts</strong> are now available to help you monitor and track journey lifecycle events and custom action performance:</p>
<ul>
<li><strong>Journey Published</strong>: Receive notifications when a journey is published by a practitioner in the journey canvas.</li>
<li><strong>Journey Finished</strong>: Get alerts when a journey has finished, with specific definitions based on journey type (Read Audience or Event-triggered).</li>
<li><strong>Custom Action Capping Triggered</strong>: Be notified when capping is activated on a custom action endpoint.</li>
</ul>
<p>These alerts can be subscribed to at the organization level or for specific journeys.</p>
<p>For more information, refer to the <a href="../reports/alerts.md#journey-alerts">detailed documentation</a>.</p>
<p>Availability date: November 5, 2025</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Themes in the Email Designer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now quickly apply <strong>pre-approved themes</strong> to ensure brand consistency across all emails, speed up your campaign creation process, and independently produce high-quality emails while reducing dependency on design teams.</p>
<p>Previously released in beta version, this capability is now available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
<img src="assets/do-not-localize/themes.gif">
<p>For more information, refer to the <a href="../email/apply-email-themes.md">detailed documentation</a>.</p>
<p><a href="https://jira.corp.adobe.com/browse/NEO-88838">Link to PRODUCT JIRA task</a></p>
<p>Availability date: November 5, 2025</p>
</td>
</tr>
</tbody>
</table>

### Improvements {#jan-26-01-improv}

Improvements coming with this release are listed below.

#### AI

* **AI Assistant Content Quality Checks** - In addition to brand alignment, you can now evaluate overall <strong>content quality</strong> to uncover potential issues with readability, cohesiveness, and effectiveness, independent of your brand guidelines. These automated checks help identify unclear messaging, inconsistent tone, or structural gaps.
  <a href="https://jira.corp.adobe.com/browse/CJM-103238">Link to PRODUCT JIRA task</a>
* **Update brands with new color tab** - Brand guidelines help ensure your brand is presented consistently across all touchpoints. The new <strong>Colors section</strong> defines the standards for your brand's color system, outlining how colors are selected, organized, and applied across experiences. It ensures consistent use of primary, secondary, accent, and neutral colors to support a cohesive, accessible, and recognizable brand identity.
  <a href="https://jira.corp.adobe.com/browse/CJM-121183">Link to PRODUCT JIRA task</a>

#### Campaigns

* **Schedule Campaign using Profile Time Zone** - Campaign scheduling can now use each profile's <strong>time zone</strong> to deliver messages at the intended local time.

  **Note**: This improvement is only available for a set of organizations (Limited Availability).
  <a href="https://jira.corp.adobe.com/browse/CJM-43782">Link to PRODUCT JIRA task</a>

#### Channels

* **SMS Webhooks: Phase II** - Description to be provided.
  <a href="https://jira.corp.adobe.com/browse/CJM-93914">Link to PRODUCT JIRA task</a>

#### Email Designer

* **In-place corrections in the Email designer** - <strong>AI-powered automatic content suggestions</strong> are now available in the Email Designer when violations are detected during content validation. If content is flagged as misaligned with brand guidelines or fails quality criteria, the system proactively generates corrected alternatives that can be reviewed and applied inline, improving compliance and accelerating production.
  <a href="https://jira.corp.adobe.com/browse/CJM-95365">Link to PRODUCT JIRA task</a>

#### Experience Decisioning

* **Self-service migration tooling APIs** - A new set of <strong>migration tooling APIs</strong> is available to migrate Offer management entities to Experience Decisioning. The tooling enables seamless migration between sandboxes with dependency resolution and rollback capabilities.
  <a href="https://jira.corp.adobe.com/browse/CJM-109695">Link to PRODUCT JIRA task</a>

* **Attach fragments to decision items** - Journey Optimizer now provides the ability to attach <strong>fragments</strong> to decision items which can be leveraged in code-based experience campaigns through decision policies.

  **Note**: Previously released in Limited Availability, this improvement is now available to all environments (General Availability).
  <a href="https://jira.corp.adobe.com/browse/CJM-110282">Link to PRODUCT JIRA task</a>

#### Journeys

* **Leverage a failure response payload in journey Custom Actions** - You can now define an optional <strong>error response payload</strong> for custom actions. When a call fails, the error payload is exposed in the journey context and is available in the timeout/error branch to support richer fallback logic and debugging.
  <a href="https://jira.corp.adobe.com/browse/CJM-113125">Link to PRODUCT JIRA task</a>

* **Combine native and Adobe Campaign message actions** - Journey Optimizer now lets you combine Adobe Campaign v7/v8 message actions with native channel actions in the same journey.
  <a href="https://jira.corp.adobe.com/browse/CJM-113103">Link to PRODUCT JIRA task</a>

* **Journey payload size validation in journeys** - Journey Optimizer now provides <strong>payload size validation</strong> to help ensure optimal performance and system stability. When building or publishing journeys, you receive clear warnings and errors if payload sizes approach or exceed recommended limits, along with actionable guidance to optimize your journey configuration. This proactive validation helps you identify potential issues early and maintain journey performance.
  <a href="https://jira.corp.adobe.com/browse/CJM-122236">Link to PRODUCT JIRA task</a>

* **Multiple inbound actions in journeys** - To simplify your journey orchestration, you can now define <strong>multiple inbound actions</strong> in a single journey. Previously available in campaigns, this capability enables you to deliver multiple code-based experiences, In-app messages, Content Cards or web actions to different locations at the same time, each action containing a specific content.

  **Note**: Previously released in Limited Availability, this improvement is now available to all environments (General Availability).
  <a href="https://jira.corp.adobe.com/browse/CJM-111916">Link to PRODUCT JIRA task</a>

#### Orchestrated campaigns

* **Select attributes and copy distribution values** - You can now select or copy values directly from the distribution of values view in orchestrated campaigns.
  <a href="https://jira.corp.adobe.com/browse/CJM-105244">Link to PRODUCT JIRA task</a>

* **Data usage label inheritance for audiences** - <strong>Data usage labels</strong> applied in Adobe Experience Platform now automatically carry over when saving audiences in orchestrated campaigns, reducing manual DULE tagging.
  <a href="https://jira.corp.adobe.com/browse/CJM-120769">Link to PRODUCT JIRA task</a>

* **Predefined retargeting filters** - To support easier retargeting for orchestrated campaign use cases, this release introduces new <strong>retargeting filters</strong>. These filters let you directly target audiences based on message engagement, such as sent, opened only, opened or clicked, or opened and clicked, and select the specific campaign or in-transition campaign you want to retarget.
  <a href="https://jira.corp.adobe.com/browse/CJM-116701">Link to PRODUCT JIRA task</a>

* **Predefined filters with parameters** - You can now create <strong>filters with parameters</strong> in orchestrated campaigns for reusable, editable rules.
  <a href="https://jira.corp.adobe.com/browse/CJM-115431">Link to PRODUCT JIRA task</a>

* **Message confirmation before send** - A <strong>confirmation step</strong> is now enabled by default before sending orchestrated campaigns to reduce accidental sends.
  <a href="https://jira.corp.adobe.com/browse/CJM-87219">Link to PRODUCT JIRA task</a>

* **User-generated metadata support** - The <strong>executionMetadata helper function</strong> is now available in the personalization editor for Orchestrated Campaigns, enabling you to attach contextual information to any native action and store it in a dataset for export to external systems.
  <a href="https://jira.corp.adobe.com/browse/CJM-112697">Link to PRODUCT JIRA task</a>

* **Restart button** - Orchestrated campaigns now include a <strong>restart button</strong> so you can quickly re-launch runs when needed before publishing the campaign.
  <a href="https://jira.corp.adobe.com/browse/CJM-106020">Link to PRODUCT JIRA task</a>

* **Rate control support** - Orchestrated campaigns now support <strong>rate control</strong> to help you pace deliveries and align with volume constraints.
  <a href="https://jira.corp.adobe.com/browse/CJM-113254">Link to PRODUCT JIRA task</a>

#### Permissions

* **Prevent self-approval for journeys and campaigns** - You can now require that creators cannot approve their own journeys or campaigns, improving <strong>separation of duties</strong> in approval workflows.
  <a href="https://jira.corp.adobe.com/browse/CJM-99957">Link to PRODUCT JIRA task</a> | <a href="https://jira.corp.adobe.com/browse/CJM-95676">Link to PRODUCT JIRA task</a>

## Coming soon {#jan-26-01-coming-soon}

In the next few days, the following capabilities and enhancements are scheduled for release. **Information is subject to change**. Updated links, screens, and documentation will be shared once these updates are live in production.

<table>
<thead>
<tr>
<th><strong>Content generation within Journey Agent</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Powered by Adobe Experience Platform Agent Orchestrator, <strong>Journey Agent</strong> is available in Journey Optimizer and enables you to analyze journeys through a natural language interface. You can now also generate and manage channel-specific content directly in Journey Agent, creating content for channels such as email and push, applying and previewing templates, refining tone and style through prompts, and opening content in Content Designer for in-context editing.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-111882">Link to PRODUCT JIRA task</a></p>
<p>Availability date: February 2, 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Content decision activity</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now include <strong>personalized offers</strong> in your journeys through a dedicated Content decision activity in the journey canvas, and use them in journey activities, including conditions and custom actions.</p>
<p><a href="https://jira.corp.adobe.com/browse/CJM-99223">Link to PRODUCT JIRA task</a></p>
<p>Availability date: February 3, 2026</p>
</td>
</tr>
</tbody>
</table>
-->
