---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 4c2785d580e28bb7645b61edaef48929bf9f4ff3
workflow-type: tm+mt
source-wordcount: '2839'
ht-degree: 29%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] suit un modèle de diffusion continue, ce qui permet à Adobe de diffuser régulièrement de nouvelles fonctionnalités, de nouvelles améliorations et de nouveaux correctifs. Cette approche permet un déploiement évolutif et échelonné des fonctionnalités afin d’assurer les performances et la stabilité dans tous les environnements.

En raison de ce modèle, les notes de mise à jour sont mises à jour entre les versions mensuelles. Pour plus d’informations sur le cycle de publication et les phases de disponibilité, consultez le [cycle de publication de Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Notes de version préliminaire de mars 2026 {#march-26-rn}

**Les notes de version préliminaire ci-dessous peuvent être modifiées sans préavis jusqu’à la date de publication**. Les liens, les copies d’écran et la documentation mise à jour sont publiés dans les notes de mise à jour, à la date de publication.

Voir aussi les notes de mise à jour préliminaires de [&#128279;](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Date de publication** : 24-25 mars 2026

### Nouvelles fonctionnalités {#march-26-features}



<table>
<thead>
<tr>
<th><strong>Messages transactionnels dans des campagnes orchestrées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les campagnes orchestrées prennent désormais en charge les <strong>messages transactionnels</strong>, ce qui vous permet de déclencher des messages en temps réel pilotés par les événements, tels que les confirmations de commande, les notifications de réservation et les mises à jour de compte, directement dans votre workflow de campagne.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Déclencher des campagnes orchestrées à l’aide de l’API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais déclencher une campagne orchestrée à l’aide de l’API . Configurez la campagne cible comme « Déclenchée par un signal » et publiez-la. Utilisez ensuite un appel API pour déclencher la campagne. L’appel API peut inclure des paramètres qui seront disponibles en tant que variables dans la campagne déclenchée.</p>
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
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Chiffrement des paramètres d'URL</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les paramètres d’URL dans les liens de tracking et les pages de destination peuvent désormais être chiffrés, fournissant ainsi une couche de sécurité supplémentaire pour les données de paramètres sensibles.</p>
<ul>
<li>Enregistrez et gérez les clés de chiffrement dans un registre <strong>Administration</strong> dédié.</li>
<li>Utilisez le nouvel assistant de chiffrement dans les expressions pour chiffrer les données sensibles dans les liens de suivi et les URL de page de destination pour les paramètres de requête que vous souhaitez protéger au moment du rendu.</li>
</ul>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
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
<p>Utilisez le nouveau nœud Optimiser pour cibler des audiences spécifiques ou exécuter des tests A/B afin de déterminer le meilleur moyen d’atteindre vos indicateurs de performance clés orientés métier.
Cet outil vous permet de tester, varier et personnaliser les communications, le séquencement et les délais afin d’atteindre avec précision votre clientèle.
</p>
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale). <a href="../building-journeys/optimize.md">En savoir plus</a></p>
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
<p>Une nouvelle activité dans les parcours, la recherche de jeu de données, vous permet de récupérer dynamiquement des données à partir de jeux de données d’enregistrement Adobe Experience Platform au moment de l’exécution. Grâce à cette fonctionnalité, vous pouvez accéder à des données qui peuvent ne pas figurer dans la payload de profil ou d’événement, ce qui garantit des interactions clients pertinentes et au moment opportun. Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale). Pour plus d’informations, consultez la <a href="../building-journeys/dataset-lookup.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Activités d’action de canal natives obsolètes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Suite à la disponibilité générale de l’activité <strong>Action</strong> en février 2026, les activités de canal natives héritées (e-mail, notification push, SMS, in-app, web, expérience basée sur le code et carte de contenu) dans la zone de travail de parcours sont désormais obsolètes.</p>
<p>Vous utilisez désormais une seule <strong>activité Action</strong> pour configurer toutes les actions de canal, ce qui remplace la nécessité de nœuds distincts spécifiques au canal.</p>
Les parcours existants qui utilisent les activités de canal héritées continueront à fonctionner sans aucune modification ni migration requise.
<p>Pour plus d’informations, consultez la <a href="../building-journeys/journey-action.md">documentation détaillée</a>.</p>
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
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale). Avec cette version de disponibilité générale, les pages miroir sont désormais prises en charge.</p>
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/create-decision-policy.md">documentation détaillée</a>.</p>
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
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale). <a href="../content-management/image-to-html.md">En savoir plus</a></p>
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
<p>Date de disponibilité : mercredi 31 mars 2026</p>
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
<p>Pour plus d’informations, consultez la <a href="../content-management/email-template-expert-mode.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : mercredi 10 mars 2026</p>
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
<p>Date de disponibilité : mardi 2 mars 2026</p>
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
<p>Proposez des expériences en temps réel directement sur Lock Screens et Dynamic Island de vos clients grâce à l’activité iOS Live dans Adobe Journey Optimizer. Diffusez des mises à jour en direct, depuis le suivi des commandes et du statut des vols jusqu’au décompte des événements, aux scores en direct et à la progression de la diffusion, sans demander aux utilisateurs d’ouvrir votre application. Tenez votre public informé et engagé au bon moment, exactement où il se trouve.</p>
<p>Publiée précédemment en version bêta, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).</p>
<p>Pour plus d’informations, consultez la <a href="../mobile-live/get-started-mobile-live.md">documentation détaillée</a>.</p>
<p>Date de disponibilité : mercredi 3 mars 2026</p>
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
<p>Optimisé par <strong></strong> <strong>Journey Agent</strong> est disponible dans Journey Optimizer et vous permet d’analyser les parcours par le biais d’une interface en langage naturel. Vous pouvez désormais également générer et gérer du contenu spécifique à un canal directement dans Journey Agent, ce qui permet de créer du contenu pour des canaux tels que les e-mails et les notifications push, d’appliquer et de prévisualiser des modèles, d’affiner le ton et le style par le biais d’invites et d’ouvrir le contenu dans <strong>Content Designer</strong> pour une modification contextuelle.</p>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Pour plus d’informations, consultez la <a href="https://experienceleague.adobe.com/docs/experience-cloud-ai/experience-cloud-ai/agents/ajo-agent.html">documentation détaillée</a>.</p>
<p>Date de disponibilité : jeudi 4 mars 2026</p>
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
<p>Date de disponibilité : mardi 9 mars 2026</p>
</td>
</tr>
</tbody>
</table>


### Améliorations {#march-26-improv}

Les améliorations de cette version sont présentées ci-dessous.


#### Création de rapports

* **Exclure les clics de robots pour les rapports par e-mail et SMS** - Les rapports par e-mail et SMS filtrent désormais automatiquement les clics de robots des mesures de clics, ce qui permet d’obtenir des données d’engagement plus précises et d’empêcher le trafic automatisé de gonfler vos chiffres de performances.

* **Optimisation de l’heure d’envoi : emplacement des contrôles mis à jour et nouveau rapport d’effet élévateur** - Les contrôles de l’optimisation de l’heure d’envoi (STO) ont été déplacés vers le menu de configuration des actions. De plus, un nouveau rapport d’effet élévateur est désormais disponible dans les rapports Parcours afin de mesurer l’impact de la STO sur les mesures de performances de vos campagnes.
<!--
#### Email Designer

* **Email Designer displayed in Unified Shell** - The Email Designer is now displayed within the Unified Shell experience, providing a consistent navigation and header experience that aligns with other Adobe applications.

* **Text mode support in fragments** - To support text-based email workflows, you can now create and manage text versions of your visual fragments for optimal use in the plain text version of emails that include that fragment.

  **Caution:** When using a fragment that was created before the current release, the fragment text version may be incorrectly rendered—both in the Email Designer and in the final email delivered to your recipients. For best results with older fragments, edit, save and republish each fragment.-->

#### Prise de décision

* **Fragments facultatifs dans les éléments de décision** - Lors de l’utilisation de fragments dans les éléments de décision, vous pouvez désormais rendre un fragment facultatif. Ainsi, s’il est temporairement indisponible sur Edge, il est ignoré et le parcours ou la campagne continue son rendu au lieu d’échouer.

#### Configuration

* **Dossiers pour les parcours et les campagnes** - Vous pouvez désormais organiser vos parcours et campagnes en dossiers, ce qui permet une navigation structurée et une gestion plus facile pour les équipes qui travaillent avec de grands volumes de contenu. Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.

* **Renommage du jeu de données d’événement de retour du destinataire Secondaire AJO** - Le jeu de données `AJO Email BCC Feedback Event` a été renommé jeu de données `AJO Secondary Recipient Feedback Event`. L’impact varie en fonction de votre situation :

   * **Utilisateurs existants** : seul le nom d’affichage est mis à jour. Le nom de la table sous-jacente reste inchangé.
   * **Nouveaux utilisateurs et sandbox** : le nom d’affichage et le nom du tableau reflètent le nouveau nom.
   * **Utilisateurs existants avec de nouveaux sandbox** : le nom d’affichage et le nom du tableau sont mis à jour vers le nouveau nom.

  Date de disponibilité : mardi 2 mars 2026

#### Campagnes orchestrées

* **Variables globales dans les campagnes orchestrées** - Les campagnes orchestrées prennent désormais en charge les variables globales qui peuvent être définies une seule fois et réutilisées dans toutes les activités d’un workflow. Cela simplifie la configuration et garantit la cohérence des valeurs dynamiques, des expressions et de la personnalisation du contenu.

* **Simplification des dimensions de cible dans les campagnes orchestrées** - Vous pouvez désormais facilement sélectionner ou déduire automatiquement le ciblage et les dimensions secondaires appropriés dans les campagnes orchestrées pour une activation d’audience précise et efficace.

#### Parcours

* **Vague d’envoi des messages sortants dans les parcours** - Vous pouvez désormais planifier la diffusion des messages des parcours Journey Optimizer par lots contrôlés dans le temps. [En savoir plus](../building-journeys/send-using-waves.md)

  Publiée précédemment en disponibilité limitée et destinée aux parcours, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).

  Date de disponibilité : mardi 16 mars 2026

* **Détails de pause et de reprise dans les détails techniques du parcours** - Le parcours **détails techniques** inclut désormais des informations supplémentaires sur la pause et la reprise : la date et l’heure de la dernière pause et reprise, le nom d’affichage et l’identifiant interne de l’utilisateur ou de l’utilisatrice qui a effectué chaque action, ainsi qu’un ensemble complet de paramètres de parcours en pause, tels que le comportement de la pause, la durée maximale de la pause et l’état de reprise automatique. [En savoir plus](../building-journeys/journey-properties.md)

  Date de disponibilité : mardi 2 mars 2026


## Notes de mise à jour de février 2026 {#feb-26-01-rn}

Les sections [Nouvelles fonctionnalités](#feb-26-01-features) et [Améliorations](#feb-26-01-improv) couvrent les fonctionnalités déjà disponibles. <!--The [Coming soon](#coming-soon) section lists features and improvements scheduled for release later in February.-->

<!--**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

<!--**Release date**: February 17-18, 2026-->

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

<!--## Coming soon {#coming-soon}

The features and improvements below are planned for release later in February. Release dates and scope may change without prior notice.

### Improvements {#coming-soon-improv}

* **Decisioning preview in Code-based Experience channel** - You can now preview decision items when configuring Decisioning with the Code-based Experience channel. Preview is available directly in the authoring interface before going live.

  Availability date: February 18, 2026
-->

