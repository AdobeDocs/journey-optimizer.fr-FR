---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 3e2fbd4a800bdba143caaf0350026e6cd959271d
workflow-type: tm+mt
source-wordcount: '3944'
ht-degree: 16%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** fournit en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] suit un modèle de diffusion continu, ce qui permet à Adobe de fournir en continu de nouvelles fonctionnalités, de nouvelles améliorations et de nouveaux correctifs. Cette approche permet un déploiement évolutif et échelonné des fonctionnalités afin d’assurer les performances et la stabilité dans tous les environnements.

En raison de ce modèle, les notes de mise à jour sont mises à jour entre les versions mensuelles. Pour plus d’informations sur le cycle de publication et les phases de disponibilité, consultez le [cycle de publication de Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Notes de mise à jour préliminaires du 26 avril {#april-26-rn}

**Les notes de version préliminaire ci-dessous peuvent être modifiées sans préavis jusqu’à la date de publication**. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les notes de mise à jour, à la date de publication.

Voir également les [Notes de mise à jour préliminaires d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

Les nouvelles fonctionnalités et améliorations publiées début avril sont accompagnées de leur date de disponibilité.

**Date de publication** : 28 et 29 avril 2026

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
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
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
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Liens profonds dans le Designer des emails</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il est désormais possible d’ajouter des liens profonds au contenu de votre e-mail par le biais d’une option dédiée dans le Designer d’e-mail. Cela permet aux utilisateurs d’accéder directement au contenu in-app approprié au lieu d’être redirigés vers des navigateurs ou des boutiques d’applications, en préservant le contexte et l’engagement.</p>
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
<p>Adobe Journey Optimizer fournit désormais un serveur <strong>MCP (Model Context Protocol)</strong> qui surfacie les opérations de campagne, de fidélité, de configuration des canaux et de sandbox directement dans toute application compatible MCP. Grâce à cette intégration, différentes personnes peuvent collaborer autour des mêmes données d’orchestration. Au lieu d’écrire des requêtes sur l’API REST Adobe Journey Optimizer ou de parcourir plusieurs écrans d’interface utilisateur, vous pouvez décrire votre intention par la conversation et laisser le gestionnaire de ligne de commande appeler les outils MCP appropriés. Cette fonctionnalité est actuellement disponible dans Claude Web et Desktop.</p>
<p>Cette fonctionnalité est disponible pour tous les clients dans Public Beta.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Copie de campagnes orchestrées dans des sandbox</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’outil Sandbox prend désormais en charge le package et la copie de campagnes orchestrées d’un sandbox à un autre. Vous n’avez ainsi plus besoin de recréer manuellement les campagnes dans chaque environnement. Lorsqu’une campagne est empaquetée, ses objets dépendants principaux, tels que les politiques de fusion et les messages, sont automatiquement inclus. La campagne importée est donc prête à être configurée et validée. Pour protéger les environnements de production, toutes les campagnes importées atteignent le statut de brouillon dans le sandbox cible, ce qui permet aux équipes de passer en revue et d’approuver les campagnes avant qu’elles ne soient mises en ligne.</p>
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
<p>Les <strong>campagnes orchestrées</strong> prennent désormais en charge une activité <strong>Requête incrémentale</strong> qui cible uniquement les profils ou les événements nouvellement éligibles depuis la dernière exécution.

Cela permet de concentrer les campagnes récurrentes sur les nouvelles audiences (nouvelles inscriptions, membres nouvellement qualifiés du programme de fidélité et segments similaires) tout en réduisant la charge de travail des requêtes et en évitant les envois redondants au fil du temps.</p>
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
<p>Vous pouvez désormais utiliser des <strong>modèles d’IA</strong> dans vos formules de classement pour améliorer automatiquement les scores de priorité des parcours en fonction des attributs de profil client et des facteurs contextuels, afin que les clients saisissent les parcours les plus pertinents.</p>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Intégration d’Adobe Express</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’intégration <b>d’Adobe Express</b> dans Adobe Journey Optimizer vous permet d’utiliser les outils d’édition d’Adobe Express directement lors de la création de contenu. Vous pouvez ainsi redimensionner, supprimer des arrière-plans, recadrer et convertir des ressources en JPEG ou PNG.
</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<p><img src="assets/do-not-localize/express_resize.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../integrations/express.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 23 avril 2026</p>
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
<p>Adobe Journey Optimizer comprend désormais une nouvelle fonctionnalité qui garantit que vos e-mails sont structurés de manière optimale pour les boîtes de réception optimisées par l’IA telles qu’Apple Intelligence et Google Gemini dans Gmail.</p>
<p>Comme les assistants d’IA contrôlent de plus en plus la manière dont les destinataires lisent et agissent sur les e-mails, cette fonctionnalité vous permet de générer et de créer du contenu qui s’exécute correctement dans les tâches d’IA en aval, notamment la synthèse, le tri, la hiérarchisation et l’extraction d’intention.</p>
<p><img src="assets/do-not-localize/optimize-for-ai.gif"></p>
<p>Pour plus d’informations, voir <a href="../email/llm-email-optimizer.md">Optimisation des e-mails pour les boîtes de réception IA</a>.</p>
<p>Date de disponibilité : 17 avril 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistant AI pour les expressions Personalization</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] inclut désormais <strong>Assistant IA</strong> directement dans l’éditeur de personnalisation qui convertit les invites de langage naturel en expressions de personnalisation et en logique conditionnelle valides, aucune expertise en syntaxe requise. Décrivez la personnalisation que vous souhaitez obtenir. L’IA génère un code prêt à l’emploi que vous pouvez appliquer immédiatement ou affiner à l’aide d’invites de relance.</p>
<p>L'assistant travaille également à l'envers. Sélectionnez une expression existante et demandez-lui d’expliquer la logique, d’identifier les problèmes ou de suggérer des améliorations. Cela le rend utile non seulement pour créer de nouvelles expressions, mais aussi pour examiner et déboguer les expressions existantes dans votre équipe.</p>
<p><img src="assets/do-not-localize/assistant-perso.gif"></p>
<p>Pour plus d’informations, voir <a href="../content-management/generative-personalization-expressions.md">Assistant AI pour les expressions Personalization</a>.</p>
<p>Date de disponibilité : 13 avril 2026</p>
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
<p>Utilisez le nouveau nœud <strong>Optimiser</strong> pour exécuter des tests A/B ou des expériences de bandit à plusieurs bras afin de déterminer le meilleur moyen d’atteindre vos indicateurs de performance clés orientés métier. Cet outil vous permet de tester, varier et personnaliser les communications, le séquencement et les délais afin d’atteindre avec précision votre clientèle.
</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<p>Dans le cadre de la disponibilité générale, cette version introduit la sélection <strong>type d’expérience</strong> (A/B ou bandit manchot) et <strong>Mettre à l’échelle le gagnant</strong> pour les parcours unitaires.</p>
<p><img src="assets/do-not-localize/optimize-experiment.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/path-experimentation.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 7 avril 2026</p>
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
<p><strong>Boîte de réception</strong> est une fonctionnalité mobile, disponible avec les cartes de contenu, qui permet aux clients de créer un emplacement centralisé dans leur application ou site web pour afficher les messages envoyés à leurs utilisateurs. Cela prolonge la durée de vie des communications marketing en s’assurant que les messages restent accessibles même après leur rejet.</p>
<p><img src="assets/do-not-localize/inbox.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../inbox/inbox-gs.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 7 avril 2026</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Optimize email text for AI inboxes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer now includes a new capability that ensures your emails are optimally structured for AI-powered inboxes such as Apple Intelligence and Google Gemini in Gmail.</p>
<p>As AI assistants increasingly control how recipients read and act on email, this feature helps you author content that performs well across downstream AI tasks including summarization, triage, prioritization, and intent extraction.</p>
<p><img src="assets/do-not-localize/text-optimizer.gif"></p>
<p>For more information, refer to <a href="../email/llm-email-optimizer.md">Optimize email text for AI inboxes</a>.</p>
<p>Availability date: April 3, 2026</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Prise en charge de la prise de décision dans le canal e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais utiliser <strong>Decisioning</strong> pour personnaliser et optimiser le contenu de vos e-mails. Tirez parti des scores de priorité, des formules ou des modèles d’IA pour afficher les offres et le contenu les plus pertinents pour chaque destinataire.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale). Avec cette version de disponibilité générale, les pages miroir sont désormais prises en charge.</p>
<p><img src="assets/do-not-localize/exd-email.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/create-decision-policy.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 6 avril 2026</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#april-26-improv}

#### IA

* **Score d’alignement de la marque dans le tableau de bord Campaign** - Vous pouvez désormais évaluer votre score d’alignement de la marque directement dans votre tableau de bord Campaign pour vous assurer que le contenu reste fidèle à la marque. Vous pouvez ainsi vérifier les directives en un coup d’œil sans avoir à ouvrir le concepteur de contenu.

* **Amélioration de l’assistant d’invite** - Lorsqu’une invite est vague, incomplète ou mélange plusieurs objectifs, **l’assistant d’invite** peut désormais poser des questions précises pour clarifier ou suggérer une réécriture plus claire de votre demande avant la génération, ce qui vous aide à identifier ce dont vous avez besoin avant que l’assistant ne réponde, ce qui améliore la cohérence et réduit les reprises. [En savoir plus](../content-management/ai-assistant-prompting-guide.md)

#### Prise de décision

* **Joindre des fragments aux éléments de décision** - Journey Optimizer permet désormais de joindre des fragments aux éléments de décision. Ils peuvent être utilisés dans des expériences basées sur du code et des campagnes par e-mail via des politiques de décision. Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).

* **Fragments temporairement indisponibles sont ignorés** - Lors de l’utilisation de fragments dans des éléments de décision, si un fragment est temporairement indisponible sur Edge, il est ignoré et le parcours ou la campagne continue de s’afficher au lieu d’échouer. [En savoir plus](../experience-decisioning/fragments-decision-policies.md#temporary-unavailable-fragments)

  Date de disponibilité : 14 avril 2026

#### Notification push

* **Personnaliser l’ID d’application dans les paramètres du canal** - Dans les paramètres de configuration du canal push, vous pouvez désormais personnaliser le champ **ID d’application** afin que chaque destinataire puisse recevoir une notification push de la marque appropriée en fonction des informations de son profil.

#### SMS

* **Nombre de caractères** - Dans Adobe Journey Optimizer, vous pouvez désormais utiliser le nombre de caractères pour surveiller la longueur de vos SMS en temps réel. Cela vous permet de savoir quand un message sera divisé en plusieurs segments afin de mieux gérer la mise en forme et d’éviter des augmentations inattendues des coûts d’envoi. [En savoir plus](../sms/create-sms.md)

* **Opt-out et consentement au numéro de téléphone et à l’expéditeur** - Pour les SMS, Journey Optimizer enregistre désormais le consentement et l’opt-out marketing au niveau du numéro de téléphone et du numéro court du profil.

  Actuellement, cette fonctionnalité n’est disponible que pour les configurations SMS Sinch. [En savoir plus](../sms/sms-configuration-sinch.md)

* **SMS entrant dans un jeu de données personnalisé** - Dans **informations d’identification de l’API SMS**, acheminez **SMS entrant** vers un **jeu de données d’événement d’expérience personnalisé et activé pour le profil** que vous sélectionnez au lieu du seul jeu de données de suivi par défaut. [En savoir plus](../sms/sms-webhook.md)

* **Amélioration de l’interface Webhook** - Lors de la configuration des Webhooks SMS, l’interface utilisateur comprend désormais un guide de configuration intégré avec des exemples pratiques, ce qui facilite l’alignement des payloads des fournisseurs et la résolution des problèmes sans quitter le flux de configuration. [En savoir plus](../sms/sms-webhook.md)

#### WhatsApp

* **Boutons interactifs et suivi WhatsApp** - WhatsApp dans Journey Optimizer prend désormais en charge les boutons interactifs requis par vos modèles et cas d’utilisation, ainsi que le suivi d’interaction intégré afin que vous puissiez mesurer l’engagement et analyser les performances parallèlement à vos autres rapports de canal.

#### Intégrations Adobe Experience Manager

* **Prise en charge des variations de fragments de contenu Adobe Experience Manager** - Vous pouvez sélectionner **Variations de fragments de contenu** (par exemple, variantes de langue ou de canal) lors de l’insertion de fragments de contenu Adobe Experience Manager, avec une gestion améliorée pour les scénarios régionaux et multilingues. [En savoir plus](../integrations/aem-fragments.md#aem-variations)

  Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.

  Date de disponibilité : 3 avril 2026

* **Contexte de fragment de contenu Adobe Experience Manager lors de la création** - Votre sélection de fragment de contenu reste active lorsque vous passez d’un champ de texte à un bloc de contenu. Vous pouvez ainsi ajouter d’autres champs de fragment sans rouvrir **Ouvrez le conseiller en contenu AEM** à chaque fois. [En savoir plus](../integrations/aem-fragments.md)

  Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.

  Date de disponibilité : 1er avril 2026

#### Configuration

* **Autorisations spécifiques pour les clés de chiffrement des paramètres d’URL** - Pour accéder aux clés de chiffrement des paramètres d’URL et les gérer, de nouvelles autorisations ont été créées. Vous devez maintenant disposer des autorisations **Afficher le registre des clés** et **Gérer le registre des clés** accordées.

#### Campagnes orchestrées

* **Améliorations apportées à Data Modeler** - Les schémas relationnels orchestrés prennent désormais en charge les clés composites s’étendant sur plusieurs champs. Le chargement d’un schéma à partir d’un fichier DDL génère également des énumérations. En outre, le chargement d’un fichier DDL ou Excel crée automatiquement des relations composites entre les tables. Dans la vue de relation d’entité, les liens composites affichent désormais l’ensemble complet des paires de champs entre les tables après le chargement d’un fichier.

* **Variables globales dans les campagnes orchestrées** - Les campagnes orchestrées prennent désormais en charge les variables globales qui peuvent être définies une seule fois et réutilisées dans toutes les activités d’un workflow. Cela simplifie la configuration et garantit la cohérence des valeurs dynamiques, des expressions et de la personnalisation du contenu.

#### Conception d’e-mail

* **Éditeur HTML avancé pour le contenu d’e-mail** - Le mode HTML avancé vous permet de modifier la source HTML de votre contenu dans le Designer d’e-mail, d’ajouter des expressions avancées (comme des conditions) dans la source et de basculer entre les vues HTML et Bureau sans perdre vos modifications.

  Auparavant disponible uniquement pour les modèles de contenu d’e-mail, cette fonctionnalité est désormais déployée sur le contenu **e-mail** dans le Designer d’e-mail (par exemple, les e-mails créés dans les parcours et les campagnes), en plus des modèles de contenu d’e-mail. Il est actuellement à disponibilité limitée. Contactez votre représentant Adobe pour y accéder. [En savoir plus](../email/email-expert-mode.md)

  Date de disponibilité : 9 avril 2026

* **Assistant AI pour les expressions de personnalisation dans le Designer Email** - Dans le Designer Email, sélectionnez un composant et utilisez **Ajouter une expression** dans la barre d’outils contextuelle pour décrire la personnalisation dont vous avez besoin en langage clair, passer en revue l’expression générée et l’insérer sans quitter le concepteur. [En savoir plus](../content-management/generative-personalization-expressions.md#generate-email-designer)

  Date de disponibilité : 15 avril 2026

#### Optimisation du chemin de parcours

* **Type d’expérience** - Vous pouvez désormais choisir entre une expérience A/B (division fixe au début) ou un bandit manchot (division automatique avec mises à jour hebdomadaires du poids) lors de la configuration d’une expérience de chemin. [En savoir plus](../building-journeys/path-experimentation.md)

  Date de disponibilité : 7 avril 2026

* **Expérimentation de parcours : mettre à l’échelle le gagnant** - Vous pouvez désormais déployer automatiquement ou manuellement le parcours gagnant d’une expérience sur l’ensemble de votre audience. Une fois qu’un gagnant est déterminé, vous pouvez amplifier sa portée et son efficacité sans surveiller constamment l’expérience. [En savoir plus](../building-journeys/path-experimentation.md#scale-winner)

  Cette fonctionnalité n’est disponible que dans les parcours unitaires (déclenchés par un événement et qualifications d’audience). Elle n’est pas disponible pour les parcours Lecture d’audience .

  Date de disponibilité : 7 avril 2026

* **Conditions** - L’activité [Optimiser](../building-journeys/optimize.md) est le nouveau moyen de créer des chemins conditionnels dans les parcours. Elle remplace l’ancienne activité **Condition**, qui a été supprimée de l’interface utilisateur. Toute la logique conditionnelle est conservée et est désormais gérée via les conditions de l’activité **Optimiser**. [En savoir plus](../building-journeys/conditions.md)

  Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).

  Date de disponibilité : 7 avril 2026


## Notes de mise à jour de mars 2026 {#march-26-rn}

Les sections [Nouvelles fonctionnalités](#march-26-features) et [Améliorations](#march-26-improv) couvrent les fonctionnalités déjà disponibles. <!--The [Coming soon](#coming-soon) section lists features and improvements scheduled for release later in March.-->

<!--
**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform pre-release notes](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.
-->

**Date de publication** : 24 et 25 mars 2026

### Nouvelles fonctionnalités {#march-26-features}

<table>
<thead>
<tr>
<th><strong>Chiffrement des paramètres d'URL</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les paramètres d’URL dans les liens de tracking et de page de destination ajoutés à vos e-mails peuvent désormais être chiffrés, fournissant ainsi une couche de sécurité supplémentaire pour les données de paramètres sensibles.</p>
<ul>
<li>Enregistrez et gérez les clés de chiffrement dans le registre <strong>Administration</strong> dédié.</li>
<li>Utilisez la nouvelle fonction d’assistance « Encrypt » dans les expressions pour chiffrer les données sensibles dans les URL pour les paramètres de requête que vous souhaitez protéger au moment du rendu.</li>
</ul>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p><img src="assets/do-not-localize/encrypt-helper.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../personalization/url-parameter-encryption.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 31 mars 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Convertir des images en modèles de contenu d’e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais convertir des images en modèles de contenu d’e-mail directement dans Journey Optimizer. Utilisez l’analyse optimisée par l’IA pour générer automatiquement des modèles HTML structurés à partir de références visuelles, ce qui réduit considérablement le temps de conception des e-mails.</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<p><img src="assets/do-not-localize/image-converter.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../content-management/image-to-html.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 31 mars 2026</p>
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
<p>Avec [!DNL Journey Optimizer], vous pouvez capturer les attributs de profil par le biais de vos pages de destination.</p>
<p>Créez, concevez et gérez des formulaires personnalisés adaptés à vos besoins en fonction d’un jeu de données spécifique. Vous pouvez ensuite utiliser ces formulaires dans les pages de destination pour ajouter les attributs de profil de votre choix au jeu de données défini pour chaque formulaire.</p>
<p>Publiée précédemment en disponibilité limitée pour les clients et clientes des États-Unis et d’Australie, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).</p>
<p><img src="assets/do-not-localize/forms.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../landing-pages/lp-forms.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 26 mars 2026.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Activité Test dans les campagnes orchestrées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une nouvelle activité <strong>Test</strong> est désormais disponible dans les campagnes orchestrées. Cette activité achemine l’exécution du workflow vers différentes branches en fonction de conditions définies, ce qui vous permet de valider la logique de campagne et les configurations avant d’activer les diffusions actives.</p>
<p><img src="../orchestrated/assets/test-1.png"></p>
<p>Pour plus d’informations, consultez la <a href="../orchestrated/activities/test.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Prise en charge de la recherche de jeux de données dans parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une nouvelle activité <strong>Recherche de jeu de données</strong> dans les parcours vous permet de récupérer dynamiquement des données des jeux de données d’enregistrement Adobe Experience Platform au moment de l’exécution, ce qui vous donne accès à des informations qui ne font pas partie de la payload du profil ou de l’événement, afin que les interactions des clients restent pertinentes et opportunes.</p>
<p>Publiée précédemment en disponibilité limitée pour un ensemble restreint d’organisations, l’activité de recherche de jeu de données dans parcours est désormais disponible pour tous les clients autorisés à effectuer une [recherche de jeu de données](../data/lookup-aep-data.md), tout en restant en disponibilité limitée.</p>
<p><img src="../building-journeys/assets/aep-data-activity.png"></p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/dataset-lookup.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>L’activité Action remplace les activités de parcours spécifiques à un canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Suite à la disponibilité générale de l’activité <strong>Action</strong> en février 2026, les activités de canal natives héritées (e-mail, notification push, SMS, in-app, web, expérience basée sur le code et carte de contenu) dans la zone de travail de parcours sont désormais obsolètes.</p>
<p>Vous devez maintenant utiliser l’activité Action unique pour configurer toutes les actions de canal, en remplaçant le besoin de nœuds distincts spécifiques au canal.</p>
<p>Les parcours existants qui utilisent les activités de canal héritées continuent à fonctionner sans aucune modification ni migration requise.</p>
<p><img src="assets/do-not-localize/action-activity.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/journey-action.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Éditeur HTML avancé pour les modèles d’e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le mode HTML avancé pour les modèles de contenu d’e-mail permet de modifier la source HTML de votre contenu dans le Designer d’e-mail, d’ajouter des expressions avancées (telles que des conditions) dans la source et de basculer entre les vues HTML et Bureau sans perdre vos modifications.</p>
<p>Cette fonctionnalité est disponible dans les modèles de contenu pour le canal E-mail uniquement. Il est actuellement à disponibilité limitée. Contactez votre représentant Adobe pour y accéder.</p>
<p><img src="assets/do-not-localize/expert-mode.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../email/email-expert-mode.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 10 mars 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Intégration de modèles Firefly personnalisés et de modèles de génération d’images tiers</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Activez l’intégration transparente des modèles Firefly standard et personnalisés, ainsi que des modèles d’image tiers approuvés, afin d’offrir une plus grande flexibilité, un meilleur contrôle et un meilleur alignement de la marque lors de la génération d’images.</p>
<p>Choisissez le modèle adapté à vos besoins :</p>
<ul><li> <strong>Adobe model</strong> (optimisé par Firefly Image Model 4) pour la génération immédiate d’images sans configuration supplémentaire</li><li> <strong>Modèle partenaire</strong> (optimisé par Gemini 2.5 Flash) pour des fonctionnalités spécialisées</li><li><strong>Modèles personnalisés</strong> (modèles spécifiques à la marque entraînés sur vos propres ressources) pour une génération sur la marque qui s’aligne précisément sur l’identité, le style et les directives visuelles de votre marque.</li></ul>
<p>Pour plus d’informations, consultez la <a href="../content-management/generative-models.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 2 mars 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Activité en direct pour iOS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Proposez des expériences en temps réel directement sur Lock Screens et Dynamic Island de vos clients avec l’<strong>activité iOS Live</strong> dans Adobe Journey Optimizer. Diffusez des mises à jour en direct, depuis le suivi des commandes et du statut des vols jusqu’au décompte des événements, aux scores en direct et à la progression de la diffusion, sans demander aux utilisateurs d’ouvrir votre application. Tenez votre public informé et engagé au bon moment, exactement où il se trouve.</p>
<p>Publiée précédemment en version bêta, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).</p>
<p>Pour plus d’informations, consultez la <a href="../mobile-live/get-started-mobile-live.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 3 mars 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Journey Agent : création de contenu de canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Optimisé par <strong>Adobe Experience Platform Agent Orchestrator</strong> <strong>Journey Agent</strong> est disponible dans Journey Optimizer et vous permet d’analyser les parcours par le biais d’une interface en langage naturel. Vous pouvez désormais également générer et gérer du contenu spécifique à un canal directement dans Journey Agent, ce qui permet de créer du contenu pour des canaux tels que les e-mails et les notifications push, d’appliquer et de prévisualiser des modèles, d’affiner le ton et le style par le biais d’invites et d’ouvrir le contenu dans <strong>Content Designer</strong> pour une modification contextuelle.</p>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Pour plus d’informations, consultez la <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent.html?lang=fr" target="_blank">documentation détaillée</a>.</p>
<p>Date de disponibilité : 4 mars 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Surveillance des modèles d’IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer vous permet désormais de surveiller l’intégrité, le statut de la formation et les performances de vos modèles d’IA de prise de décision. Vous pouvez ainsi vérifier le succès de la formation, résoudre les problèmes et comprendre l’impact sur vos résultats afin de sélectionner les meilleures offres pour chaque client à l’aide de l’IA. Notez que cette fonctionnalité est disponible uniquement pour <strong>Decisioning</strong> (et non pour les modèles de gestion des décisions hérités).</p>
<p>Cette fonctionnalité est actuellement disponible uniquement pour les modèles <strong>optimisation personnalisée</strong> (et non pour l’optimisation automatique).</p>
<p><img src="assets/do-not-localize/ai-model-observability.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/ranking/ai-model-observability.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 9 mars 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Déclencher des campagnes orchestrées à l’aide d’un signal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les campagnes orchestrées peuvent désormais être déclenchées via un signal <strong>API</strong>. Pour configurer ce paramètre, configurez la campagne cible comme <strong>Déclenchée par un signal</strong>, publiez-la, puis déclenchez-la à l’aide d’un appel API. Tous les paramètres inclus dans l’appel API sont disponibles en tant que variables dans la campagne en cours d’exécution. Notez que les campagnes orchestrées déclenchées par signal restent des campagnes <strong>par lots</strong> et sont distinctes des campagnes déclenchées par API.</p>
<p><img src="assets/do-not-localize/oc-triggered.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../orchestrated/trigger-orchestrated-campaign.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Catégorie transactionnelle dans les campagnes orchestrées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dans les campagnes orchestrées, vous pouvez désormais définir une activité de canal dans la catégorie <strong>Transactionnel</strong>. Cela applique des configurations de canal transactionnel à cette activité. Cette fonctionnalité est utile lorsque les règles métier ne doivent pas s’appliquer ou lorsque l’accord préalable des clients n’est pas requis.</p>
<p><img src="assets/do-not-localize/oc-transactional.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../orchestrated/activities/channels.md#add">documentation détaillée</a>.</p>
<p>Cette fonctionnalité sera progressivement déployée dans toutes les régions au cours des prochains jours.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#march-26-improv}

Les améliorations de cette version sont présentées ci-dessous.

#### Personnalisation

* **Personnalisation complète/de base des URL** - Vous pouvez personnaliser les URL de destination à l’aide d’attributs de profil (par exemple, pour le domaine ou le chemin d’accès). Pour activer cette fonctionnalité, fournissez à Adobe votre liste de domaines acceptés. [En savoir plus](../personalization/personalization-build-expressions.md#where)

  Publiée précédemment en disponibilité limitée et destinée aux parcours, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).

  Date de disponibilité : 1er avril 2026

#### Création de rapports

* **Optimisation de l’heure d’envoi : emplacement des contrôles mis à jour et nouveau rapport d’effet élévateur** - Les contrôles de l’optimisation de l’heure d’envoi (STO) ont été déplacés vers le menu de configuration des actions. De plus, un nouveau rapport d’effet élévateur est désormais disponible dans les rapports Parcours afin de mesurer l’impact de la STO sur les mesures de performances de vos campagnes. [En savoir plus](../reports/channel-report-cja.md#optimization-models)

  Date de disponibilité : 27 mars 2026

<!--
* **Exclude bot clicks for email and SMS reporting** - Email and SMS reporting now automatically filters out bot clicks from click metrics, providing more accurate engagement data and preventing automated traffic from inflating your performance figures.

#### Email Designer

* **Email Designer displayed in Unified Shell** - The Email Designer is now displayed within the Unified Shell experience, providing a consistent navigation and header experience that aligns with other Adobe applications.

* **Text mode support in fragments** - To support text-based email workflows, you can now create and manage text versions of your visual fragments for optimal use in the plain text version of emails that include that fragment.

  **Caution:** When using a fragment that was created before the current release, the fragment text version may be incorrectly rendered—both in the Email Designer and in the final email delivered to your recipients. For best results with older fragments, edit, save and republish each fragment.
-->

#### Configuration

<!--* **Folders for journeys and campaigns** - You can now organize your journeys and campaigns into folders, enabling structured navigation and easier management for teams working with large volumes of content. This capability is only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.-->

* **Échec du renouvellement des certificats de domaine AJO** - Vous pouvez désormais vous abonner pour recevoir des alertes système, par e-mail ou dans le centre de notifications Journey Optimizer, lorsqu’un certificat de domaine utilisé pour la délivrabilité des e-mails approche de son expiration ou a déjà expiré. [En savoir plus](../reports/alerts.md#alert-certificates-renewal-unsuccessful)

  Date de disponibilité : 26 mars 2026

* **Renommage du jeu de données d’événement de retour du destinataire Secondaire AJO** - Le jeu de données `AJO Email BCC Feedback Event` a été renommé jeu de données `AJO Secondary Recipient Feedback Event`. L’impact varie en fonction de votre situation :

   * **Utilisateurs existants** : seul le nom d’affichage est mis à jour. Le nom de la table sous-jacente reste inchangé.
   * **Nouveaux utilisateurs et sandbox** : le nom d’affichage et le nom du tableau reflètent le nouveau nom.
   * **Utilisateurs existants avec de nouveaux sandbox** : le nom d’affichage et le nom du tableau sont mis à jour vers le nouveau nom.

  >[!NOTE]
  >
  >Les nouveaux jeux de données affichent immédiatement le nouveau nom. Pour les anciens noms de jeux de données, le renvoi et la réconciliation se déroulent progressivement et peuvent prendre plusieurs semaines.

  Date de disponibilité : 2 mars 2026


#### Parcours

* **Action Mettre à jour le profil : prise en charge de plusieurs attributs de profil** - L’activité d’action **Mettre à jour le profil** prend désormais en charge la mise à jour de cinq attributs de profil au maximum dans un seul nœud. Auparavant, chaque action ne pouvait mettre à jour qu’un seul attribut à la fois, ce qui nécessitait que plusieurs nœuds mettent à jour plusieurs attributs. Utilisez le nouveau bouton **Mettre à jour un autre champ** pour ajouter des paires champ/valeur supplémentaires, ce qui réduit la complexité de la zone de travail et améliore les performances. [En savoir plus](../building-journeys/update-profiles.md)

* **Vague d’envoi des messages sortants dans les parcours** - Vous pouvez désormais planifier la diffusion des messages des parcours Journey Optimizer par lots contrôlés dans le temps. [En savoir plus](../building-journeys/send-using-waves.md)

  Publiée précédemment en disponibilité limitée et destinée aux parcours, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).

  Date de disponibilité : 16 mars 2026

* **Détails de pause et de reprise dans les détails techniques du parcours** - Le parcours **détails techniques** inclut désormais des informations supplémentaires sur la pause et la reprise : la date et l’heure de la dernière pause et reprise, le nom d’affichage et l’identifiant interne de l’utilisateur ou de l’utilisatrice qui a effectué chaque action, ainsi qu’un ensemble complet de paramètres de parcours en pause, tels que le comportement de la pause, la durée maximale de la pause et l’état de reprise automatique. [En savoir plus](../building-journeys/journey-properties.md)

  Date de disponibilité : 2 mars 2026

#### Prise de décision

* **Migration de prise de décision - Attributs d’offre et de contexte** - Le mappage d’entité de l’API de migration répertorie désormais **attributs d’offre** (`migratedofferattributes` sur le schéma d’élément d’offre personnalisée) et **attributs de contexte** (`migratedcontextattributes` sur le schéma du jeu de données de migration). [En savoir plus](../experience-decisioning/decisioning-migration-api.md#entity-mapping)

  Date de disponibilité : 31 mars 2026

<!--
## Coming soon {#coming-soon}

The features and improvements below are planned for release later in March/early April. Release dates and scope are **subject to change without prior notice**.


WAITING RELEASE DATE CONFIRMATION * **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.


WAITING RELEASE DATE CONFIRMATION
* **Target dimension simplification in Orchestrated Campaigns** - The active targeting dimension is now shown on the workflow canvas, so you can see which dimension is used by a channel activity. The multi-entity segmentation flow is simpler as you no longer need a separate "Change dimension" activity. Moreover, you can now choose explicitly whether messages are sent at the profile level or at a secondary dimension level.
-->
