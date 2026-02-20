---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
role: User
level: Beginner, Intermediate
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 6c509ef134c4240b243d255fd1ab7ec6bb062bf0
workflow-type: tm+mt
source-wordcount: '1329'
ht-degree: 33%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] suit un modèle de diffusion continue, ce qui permet à Adobe de diffuser régulièrement de nouvelles fonctionnalités, de nouvelles améliorations et de nouveaux correctifs. Cette approche permet un déploiement évolutif et échelonné des fonctionnalités afin d’assurer les performances et la stabilité dans tous les environnements.

En raison de ce modèle, les notes de mise à jour sont mises à jour entre les versions mensuelles. Pour plus d’informations sur le cycle de publication et les phases de disponibilité, consultez le [cycle de publication de Journey Optimizer](releases.md).

[!DNL Adobe Journey Optimizer] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Notes de mise à jour de février 2026 {#feb-26-01-rn}

Les sections [Nouvelles fonctionnalités](#feb-26-01-features) et [Améliorations](#feb-26-01-improv) couvrent les fonctionnalités déjà disponibles. La section [ bientôt disponible ](#coming-soon) répertorie les fonctionnalités et améliorations dont la publication est prévue pour février.

<!--**The pre-release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published in the release notes, at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/en/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.-->

<!--**Release date**: February 17-18, 2026-->

### Nouvelles fonctionnalités {#feb-26-01-features}


<!--
<table>
<thead>
<tr>
<th><strong>Mobile Live Activities</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p><strong>Live Activities</strong> provide real-time updates and interactive experiences within mobile apps, allowing users to stay informed about ongoing events or tasks directly on their device's screen. This feature enhances engagement by delivering live information, such as progress tracking, event updates, or interactive content, without requiring users to open the app.</p>
<p>Previously released in beta, this capability is now available to all environments (General Availability).</p>
</td>
</tr>
</tbody>
</table>
-->

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

<p>Dans <strong>parcours</strong>, cette fonctionnalité n’est disponible que pour un ensemble d’organisations (disponibilité limitée). Pour y accéder, contactez votre représentant ou représentante Adobe. Pour plus d’informations, consultez la <a href="../building-journeys/send-using-waves.md">documentation détaillée</a>.</p>
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

### Améliorations {#feb-26-01-improv}

Les améliorations de cette version sont présentées ci-dessous.

#### Configuration

* **Utilisation des événements d’expérience dans les expressions de parcours** - À compter du 1er avril 2026, l’utilisation des attributs d’événement d’expérience dans les expressions de parcours ne sera plus prise en charge pour les organisations qui n’ont pas utilisé cette fonctionnalité au cours des 90 derniers jours. Cette fonctionnalité n’est déjà plus disponible pour les nouvelles organisations clientes depuis le 8 juillet 2025. Pour obtenir des alternatives, consultez [Recherche d’événement d’expérience dans les parcours ](../building-journeys/exp-event-lookup.md).

#### Concepteur d’e-mail

* **Retrait de texte** - Vous pouvez désormais appliquer un retrait de gauche personnalisable à la première ligne des paragraphes des composants de texte directement à partir du panneau des propriétés. <!--The new **Indentation** control lets you define indentation in pixels or percentage via a numeric input or slider, with live preview on the canvas. --> Cela améliore la lisibilité du contenu de forme longue tel que les éditoriaux et les articles.

  Date de disponibilité : 18 février 2026.

#### Modèles de contenu

* **Utiliser des thèmes pour convertir des images en modèles d’e-mail** - Lors de la conversion d’une image en modèle d’e-mail dans Journey Optimizer, vous pouvez désormais utiliser un thème comme entrée afin que l’HTML générée suive les paramètres de votre marque. Les styles tels que la couleur d’arrière-plan, la couleur du bouton, les polices, l’espacement des lignes, les marges et la marge intérieure sont appliqués automatiquement, ce qui réduit le travail de conception manuel et fournit un modèle prêt à l’emploi avec un minimum de modifications. [En savoir plus](../content-management/image-to-html.md)

  Date de disponibilité : 17 février 2026.


#### Décisions pour les expériences

* **Prise en charge entrante d’Edge pour l’utilisation des données Adobe Experience Platform dans la prise de décision** - L’utilisation des données Adobe Experience Platform dans la prise de décision prend désormais en charge les cas d’utilisation entrants Edge, en plus des e-mails et des actions personnalisées dans les parcours. [En savoir plus](../experience-decisioning/aep-data-exd.md)

  **Remarque** : cette fonctionnalité n’est disponible que pour un ensemble d’organisations (<strong>Disponibilité limitée</strong>). Pour en bénéficier, contactez votre représentant ou représentante Adobe.


* **Joindre des fragments aux éléments de décision** : Journey Optimizer permet désormais de joindre des fragments aux éléments de décision qui peuvent être utilisés dans les campagnes d’expérience basées sur du code par le biais de politiques de décision. [En savoir plus](../experience-decisioning/fragments-decision-policies.md)

  **Remarque** : cette fonctionnalité, précédemment disponible en disponibilité limitée, est désormais disponible dans tous les environnements (disponibilité générale).

  Date de disponibilité : 12 février 2026.

## Bientôt disponible {#coming-soon}

Les fonctionnalités et améliorations ci-dessous devraient être publiées plus tard en février. Les dates et la portée des versions peuvent changer sans préavis.

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
<p>Date de disponibilité : samedi 20 février 2026</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>arbitrage de parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais utiliser des <strong>formules de classement</strong> et des <strong>modèles d’IA</strong> pour améliorer automatiquement les scores de priorité des parcours en fonction des attributs de profil client et des facteurs contextuels, afin que les clients saisissent les parcours les plus pertinents.</p>
<p>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
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
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais proposée dans tous les environnements (disponibilité générale).</p>
<p>Date de disponibilité : samedi 20 février 2026</p>
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
<p>Date de disponibilité : samedi 20 février 2026</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#coming-soon-improv}

* **Aperçu d’Experience Decisioning dans le canal d’expérience basé sur le code** - Vous pouvez désormais prévisualiser les éléments de décision lors de la configuration d’Experience Decisioning avec le canal d’expérience basé sur le code. L’aperçu est disponible directement dans l’interface de création avant la mise en ligne.

  Date de disponibilité : 20 février 2026.

* **Intégration de modèles Firefly personnalisés et de modèles de génération d’images tiers** - Activez l’intégration transparente des modèles Firefly standard et personnalisés, ainsi que des modèles d’image tiers approuvés (par exemple, NanoBanana), pour offrir une plus grande flexibilité, un meilleur contrôle et un meilleur alignement de la marque lors de la génération d’images. Vous pouvez ainsi sélectionner le meilleur modèle pour chaque cas d’utilisation : Firefly standard pour les besoins généraux, Firefly personnalisé pour la génération sur marque ou modèles tiers approuvés pour des scénarios spécialisés ou expérimentaux.

  Date de disponibilité : 20 février 2026.

