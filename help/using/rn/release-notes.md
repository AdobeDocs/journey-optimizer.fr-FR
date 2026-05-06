---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 11234e03589d1e39efc0702a3c423e017cf9b816
workflow-type: tm+mt
source-wordcount: '2386'
ht-degree: 18%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**&#x200B;** fournit en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] suit un modèle de diffusion continu, ce qui permet à Adobe de fournir en continu de nouvelles fonctionnalités, de nouvelles améliorations et de nouveaux correctifs. Cette approche permet un déploiement évolutif et échelonné des fonctionnalités afin d’assurer les performances et la stabilité dans tous les environnements.

En raison de ce modèle, les notes de mise à jour sont mises à jour entre les versions mensuelles. Pour plus d’informations sur le cycle de publication et les phases de disponibilité, consultez le [cycle de publication de Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Mises à jour de mai 2026 {#may-26-rn}

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
<p>Cette fonctionnalité est disponible pour tous les clients en tant que disponibilité limitée avec des fonctionnalités essentielles.</p>
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
<th><strong>Règles de prise de décision et optimisation de l’IA dédiée aux formules de classement</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>[!DNL Adobe Journey Optimizer] utilise désormais l’IA pour détecter les règles de prise de décision et les formules de classement qui peuvent être simplifiées. Dans l’inventaire, un indicateur rouge s’affiche sur toute règle pour laquelle l’IA a identifié une opportunité d’optimisation. Cliquez sur l’indicateur pour afficher l’expression d’origine avec la version suggérée par l’IA. À partir de là, vous pouvez télécharger un fichier pour examiner la manière dont les profils simulés sont évalués par chaque version et confirmer qu’ils se comportent de manière identique, puis remplacer l’expression par l’expression optimisée.</p>
<p>Pour plus d’informations, consultez la <a href="../start/ai-features.md#decisioning-optimization">documentation détaillée</a>.</p>
<p>Date de disponibilité : 5 mai 2026</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Intégrations</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La fonctionnalité <b> Intégrations </b> vous permet de connecter des sources de données tierces directement à Adobe Journey Optimizer. En simplifiant la manière d’extraire des données externes et du <b>contenu composable</b>, cette fonctionnalité facilite la diffusion de messages dynamiques personnalisés sur tous vos canaux.</p>
<p>Publiée précédemment en version Beta, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).</p>
<p>Pour plus d’informations, consultez la <a href="../integrations/integrations.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 4 mai 2026</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#may-26-improv}

#### Prise de décision

* **API de workflow de migration Decisioning** - Le contrat d’API pour la création d’analyses des dépendances et de workflows de migration a été mis à jour : transmettez **`request-level`** en tant que **paramètre de requête** sur l’URL de la requête (`sandbox`, `offer` ou `decision`). Le niveau de requête ne doit plus être envoyé dans le corps JSON. [En savoir plus](../experience-decisioning/decisioning-migration-api.md)

  Date de disponibilité : 6 mai 2026

## Bientôt disponible {#coming-soon}

La publication des fonctionnalités et améliorations suivantes est prévue dans les prochains jours. **Les informations peuvent faire l’objet de modifications**. Les liens, les écrans et la documentation mis à jour seront partagés une fois que ces mises à jour seront en production.

### Nouvelles fonctionnalités {#comming-soon-features}

<table>
<thead>
<tr>
<th><strong>Liens profonds dans le Designer des emails</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Il est désormais possible d’ajouter des liens profonds au contenu de votre e-mail par le biais d’une option dédiée dans le Designer d’e-mail.</p><p>Cela permet aux utilisateurs d’accéder directement au contenu in-app approprié au lieu d’être redirigés vers des navigateurs ou des boutiques d’applications, en préservant le contexte et l’engagement.</p>
<!--<p><img src="assets/do-not-localize/forms.gif"></p>-->
<p>Pour plus d’informations, consultez la <a href="../email/message-tracking.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : 7 mai 2026</p>
</td>
</tr>
</tbody>
</table>

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
<p>Cette fonctionnalité ne sera disponible que pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<!--p>For more information, refer to the <a href="../building-journeys/journey-fragments.md">detailed documentation</a>.</p-->
<p>Date de disponibilité : 12 mai 2026</p>
</td>
</tr>
</tbody>
</table>



## Notes de mise à jour d’avril 2026 {#april-26-rn}

<!--
**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.
-->

Les nouvelles fonctionnalités et améliorations publiées début avril sont accompagnées de leur date de disponibilité.

**Date de publication** : 28 et 29 avril 2026

### Nouvelles fonctionnalités {#april-26-features}

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
<p>Pour plus d’informations, consultez la <a href="../orchestrated/activities/incremental-query.md#incremental-query-configuration">documentation détaillée</a>.</p>
<p>Date de disponibilité : 30 avril 2026</p>
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
<p><img src="assets/do-not-localize/sender-headers.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../email/header-parameters.md#sender-header">documentation détaillée</a>.</p>
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
<p><img src="../configuration/assets/email-config-cc.png"></p>
<p>Pour plus d’informations, consultez la <a href="../configuration/cc-email-field.md">documentation détaillée</a>.</p>
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
<p><img src="assets/do-not-localize/oc-sandbox.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../configuration/copy-objects-to-sandbox.md">documentation détaillée</a>.</p>
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
<p>Adobe Journey Optimizer fournit désormais un serveur <strong>MCP (Model Context Protocol)</strong> qui surfacie les opérations de campagne, de configuration de canal et de sandbox directement dans toute application compatible MCP. Grâce à cette intégration, différentes personnes peuvent collaborer autour des mêmes données d’orchestration. Au lieu d’écrire des requêtes sur l’API REST Adobe Journey Optimizer ou de parcourir plusieurs écrans d’interface utilisateur, vous pouvez décrire votre intention par la conversation et laisser le gestionnaire de ligne de commande appeler les outils MCP appropriés. Cette fonctionnalité est actuellement disponible dans Claude Web et Desktop.</p>
<p>Cette fonctionnalité est disponible pour tous les clients dans Public Beta.</p>
<p>Pour plus d’informations, consultez la <a href="../integrations/ajo-mcp.md">documentation détaillée</a>.</p>
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
<p><img src="assets/do-not-localize/journey-arbitration-ai-models.gif"></p>
<p>Pour plus d’informations, consultez la <a href="../conflict-prioritization/journey-ai-models.md">documentation détaillée</a>.</p>
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
<p>L’intégration <b>d’</b> dans Adobe Journey Optimizer vous permet d’utiliser les outils d’édition d’Adobe Express directement lors de la création de contenu. Vous pouvez ainsi redimensionner, supprimer des arrière-plans, recadrer et convertir des ressources en JPEG ou PNG.
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
<p>[!DNL Adobe Journey Optimizer] inclut désormais <strong>Assistant IA</strong> directement dans l’éditeur de personnalisation et le Designer d’e-mail qui convertit les invites en langage naturel en expressions de personnalisation valides et en logique conditionnelle, aucune expertise en syntaxe requise. Décrivez la personnalisation que vous souhaitez obtenir. L’IA génère un code prêt à l’emploi que vous pouvez appliquer immédiatement ou affiner à l’aide d’invites de relance.</p>
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

<!--
* **Brand alignment score in Campaign dashboard** - You can now assess your brand alignment score directly within your Campaign dashboard to ensure content stays on-brand. This allows you to verify guidelines at a glance without having to open the content designer.
-->

* **Amélioration de l’assistant d’invite** - L’assistant d’invite améliore la génération de contenu de l’IA en analysant les invites utilisateur en temps réel et en identifiant les lacunes de clarté, d’exhaustivité et de contexte. Il suggère des réécritures améliorées et fournit des conseils pratiques pour enrichir les invites avec des détails clés tels que l&#39;audience, le ton et l&#39;intention. La fonctionnalité pose également des questions ciblées pour clarifier les données afin d’aider les utilisateurs à affiner leurs entrées avant la génération. Vous obtenez ainsi des sorties plus précises et de haute qualité avec moins d’itérations. [En savoir plus](../content-management/ai-assistant-prompting-guide.md#prompt-assistant)

  Date de disponibilité : 5 mai 2026

#### Notification push

* **Personnaliser l’ID d’application dans les paramètres du canal** - Dans les paramètres de configuration du canal push, vous pouvez désormais personnaliser le champ **ID d’application** afin que chaque destinataire puisse recevoir une notification push de la marque appropriée en fonction des informations de son profil. [En savoir plus](../push/push-configuration.md#app-id-personalization)

#### Prise de décision

* **API de workflow de migration Decisioning** - Le contrat d’API pour la création d’analyses des dépendances et de workflows de migration a été mis à jour : transmettez **`request-level`** en tant que **paramètre de requête** sur l’URL de la requête (`sandbox`, `offer` ou `decision`). Le niveau de requête ne doit plus être envoyé dans le corps JSON. [En savoir plus](../experience-decisioning/decisioning-migration-api.md)

  Date de disponibilité : 6 mai 2026

* **Joindre des fragments aux éléments de décision** - Journey Optimizer permet désormais de joindre des fragments aux éléments de décision. Ils peuvent être utilisés dans des expériences basées sur du code et des campagnes par e-mail via des politiques de décision. [En savoir plus](../experience-decisioning/fragments-decision-policies.md)

  Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).

* **Fragments temporairement indisponibles sont ignorés** - Lors de l’utilisation de fragments dans des éléments de décision, si un fragment est temporairement indisponible sur Edge, il est ignoré et le parcours ou la campagne continue de s’afficher au lieu d’échouer. [En savoir plus](../experience-decisioning/fragments-decision-policies.md#temporary-unavailable-fragments)

  Date de disponibilité : 14 avril 2026

<!--
#### SMS

* **Character Count** - In Adobe Journey Optimizer, you can now use the Character Count to monitor the length of your SMS messages in real time. It helps you see when a message will be split into multiple segments to better manage formatting and avoid unexpected increases in sending costs. [Read more](../sms/create-sms.md)

* **Opt-out and consent at phone number and sender** - For SMS, Journey Optimizer now records marketing consent and opt-out at the level of both the profile's phone number and short code. 

  This capability is currently only available for Sinch SMS configurations. [Read more](../sms/sms-configuration-sinch.md)

* **SMS inbounds to a custom dataset** - In **SMS API credentials**, route **inbound SMS** to a **custom, profile-enabled Experience Event dataset** you select instead of only the default tracking dataset. [Read more](../sms/sms-webhook.md)

* **Webhook interface enhancement** - When configuring SMS webhooks, the user interface now includes a built-in setup guide with practical examples, making it easier to align provider payloads and troubleshoot issues without leaving the configuration flow. [Read more](../sms/sms-webhook.md)

#### WhatsApp

* **WhatsApp interactive buttons and tracking** - WhatsApp in Journey Optimizer now supports interactive buttons required by your templates and use cases, along with built-in interaction tracking so you can measure engagement and analyze performance alongside your other channel reporting.
-->

#### Intégrations Adobe Experience Manager

* **Prise en charge des variations de fragments de contenu Adobe Experience Manager** - Vous pouvez sélectionner **Variations de fragments de contenu** (par exemple, variantes de langue ou de canal) lors de l’insertion de fragments de contenu Adobe Experience Manager, avec une gestion améliorée pour les scénarios régionaux et multilingues. [En savoir plus](../integrations/aem-fragments.md#aem-variations)

  Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).

* **Contexte de fragment de contenu Adobe Experience Manager lors de la création** - Votre sélection de fragment de contenu reste active lorsque vous passez d’un champ de texte à un bloc de contenu. Vous pouvez ainsi ajouter d’autres champs de fragment sans rouvrir **Ouvrez le conseiller en contenu AEM** à chaque fois. [En savoir plus](../integrations/aem-fragments.md)

  Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).

#### Conception d’e-mail

* **Éditeur HTML avancé pour le contenu d’e-mail** - Le mode HTML avancé vous permet de modifier la source HTML de votre contenu dans le Designer d’e-mail, d’ajouter des expressions avancées (comme des conditions) dans la source et de basculer entre les vues HTML et Bureau sans perdre vos modifications.

  Auparavant disponible uniquement pour les modèles de contenu d’e-mail, cette fonctionnalité est désormais déployée sur le contenu **e-mail** dans le Designer d’e-mail (par exemple, les e-mails créés dans les parcours et les campagnes), en plus des modèles de contenu d’e-mail. Il est actuellement à disponibilité limitée. Contactez votre représentant Adobe pour y accéder. [En savoir plus](../email/email-expert-mode.md)

  Date de disponibilité : 9 avril 2026

#### Optimisation du chemin de parcours

* **Type d’expérience** - Vous pouvez désormais choisir entre une expérience A/B (division fixe au début) ou un bandit manchot (division automatique avec mises à jour hebdomadaires du poids) lors de la configuration d’une expérience de chemin. [En savoir plus](../building-journeys/path-experimentation.md)

  Date de disponibilité : 7 avril 2026

* **Expérimentation de parcours : mettre à l’échelle le gagnant** - Vous pouvez désormais déployer automatiquement ou manuellement le parcours gagnant d’une expérience sur l’ensemble de votre audience. Une fois qu’un gagnant est déterminé, vous pouvez amplifier sa portée et son efficacité sans surveiller constamment l’expérience. [En savoir plus](../building-journeys/path-experimentation.md#scale-winner)

  Cette fonctionnalité n’est disponible que dans les parcours unitaires (déclenchés par un événement et qualifications d’audience). Elle n’est pas disponible pour les parcours Lecture d’audience .

  Date de disponibilité : 7 avril 2026

* **Conditions** - L’activité [Optimiser](../building-journeys/optimize.md) est le nouveau moyen de créer des chemins conditionnels dans les parcours. Elle remplace l’ancienne activité **Condition**, qui a été supprimée de l’interface utilisateur. Toute la logique conditionnelle est conservée et est désormais gérée via les conditions de l’activité **Optimiser**. [En savoir plus](../building-journeys/conditions.md)

  Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).

  Date de disponibilité : 7 avril 2026

#### Campagnes orchestrées

* **Variables globales dans les campagnes orchestrées** - Les campagnes orchestrées prennent désormais en charge les variables globales qui peuvent être définies une seule fois et réutilisées dans toutes les activités d’un workflow. Cela simplifie la configuration et garantit la cohérence des valeurs dynamiques, des expressions et de la personnalisation du contenu. [En savoir plus](../orchestrated/global-variables.md)
* **Améliorations apportées à Data Modeler** - Les schémas relationnels orchestrés prennent désormais en charge les clés composites s’étendant sur plusieurs champs. Le chargement d’un schéma à partir d’un fichier DDL génère également des énumérations. En outre, le chargement d’un fichier DDL ou Excel crée automatiquement des relations composites entre les tables. Dans la vue de relation d’entité, les liens composites affichent désormais l’ensemble complet des paires de champs entre les tables après le chargement d’un fichier. [En savoir plus](../orchestrated/gs-schemas.md)
