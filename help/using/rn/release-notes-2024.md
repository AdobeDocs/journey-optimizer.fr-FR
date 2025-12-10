---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour de 2024
description: Notes de mise à jour de 2024 pour Journey Optimizer
feature: Release Notes
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: bae533c5-1bfc-48bf-9f8d-1145383c040c
source-git-commit: fb74c0c14cf35aeb0c28719878d009e040be4214
workflow-type: tm+mt
source-wordcount: '6783'
ht-degree: 100%

---

# Notes de mise à jour de 2024 {#release-notes-2024}

Cette page répertorie toutes les fonctionnalités et améliorations pour [!DNL Journey Optimizer] publiées en 2024.

## Version d’octobre 2024 {#24-10-rn}

**Date de publication** : 29-30 octobre 2024

### Nouvelles fonctionnalités {#24-10-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous :

<table>
<thead>
<tr>
<th><strong>Verrouillage du contenu d’e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer vous permet désormais de verrouiller le contenu dans les modèles d’e-mail, soit en verrouillant l’intégralité du modèle, soit des structures et composants spécifiques. Cela vous permet d’éviter les modifications ou suppressions involontaires, de mieux contrôler la personnalisation des modèles et d’améliorer l’efficacité et la fiabilité de vos campagnes par e-mail.</p>
<p>Pour plus d’informations, consultez la <a href="../content-management/content-locking.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/gif-content-locking.gif">
<p>Disponible depuis le 24 octobre 2024</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Expériences basées sur le code dans les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce au nouveau canal d’expérience basée sur le code, Adobe Journey Optimizer vous permet d’effectuer des tests et des personnalisations avancés pour l’une de vos propriétés entrantes, ce qui vous permet de diffuser facilement des expériences personnalisées sur différents points de contact (touchpoints) tels que des applications web, des applications mobiles, des applications de bureau, des consoles vidéo, des appareils connectés à la télévision, des téléviseurs intelligents, des kiosques, des distributeurs automatiques, des périphériques IoT, etc. Le canal d’expérience basée sur le code est désormais disponible dans la zone de travail du parcours.</p>
<p>Pour plus d’informations, consultez la <a href="../code-based/create-code-based.md">documentation détaillée</a>.</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
<p>Disponible depuis le 1er octobre 2024</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Expériences web dans les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Avec le canal web, Adobe Journey Optimizer vous permet de personnaliser l’expérience web que vous diffusez à votre clientèle par le biais de parcours web entrants. Le canal web est désormais disponible dans la zone de travail du parcours.</p>
<p>Pour plus d’informations, consultez la <a href="../web/create-web.md">documentation détaillée</a>.</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
<p>Disponible depuis le 1er octobre 2024</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Gestion des conflits et des priorités (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dans Journey Optimizer, la gestion du volume et du calendrier des campagnes et des parcours est essentielle pour éviter de submerger les clientes et clients avec un trop grand nombre d’interactions. Journey Optimizer propose désormais plusieurs outils de gestion des conflits et de hiérarchisation des priorités. <p>Pour plus d’informations, consultez la <a href="../conflict-prioritization/gs-conflict-prioritization.md">documentation détaillée</a>.</p></p><p><ul><li><b>Capping de la fréquence des parcours</b> : vous pouvez désormais créer des jeux de règles à appliquer à vos parcours, ce qui vous permet de limiter le nombre de parcours d’un profil par jour, semaine ou mois, ainsi que de contrôler le nombre de parcours simultanés exécutés simultanément.</li>
<li><b>Score de priorité</b> : vous pouvez désormais attribuer un score de priorité à une campagne ou à un parcours, allant de 0 à 100. Un nombre plus élevé indique une priorité plus élevée. Lorsque deux campagnes ou actions de parcours utilisent la même configuration des canaux, Journey Optimizer sélectionne celle ayant le score de priorité le plus élevé. Si les campagnes ont le même score, la campagne la plus anciennement modifiée sera choisie.</li>
<li><b>Afficher les conflits potentiels</b> : un nouveau bouton « Afficher les conflits potentiels » dans les parcours et les campagnes vous permet désormais d’identifier le chevauchement avec d’autres parcours ou campagnes tels que la date de début, l’audience ciblée ou la configuration des canaux sélectionnée.</li>
<li><b>Arbitrage du parcours</b> : cette nouvelle fonctionnalité vous permet de hiérarchiser les parcours les plus importants pour vos clientes et clients. Vous pouvez créer une règle pour supprimer une entrée dans un parcours de priorité inférieure lorsqu’un client ou une cliente est admissible pour un parcours de priorité supérieure à venir.</li>
<li><b>Capping de la fréquence par type de communication : </b>avec les jeux de règles, vous pouvez désormais définir des règles granulaires par type de communication (par exemple, ventes, promotionnel) pour éviter de surcharger les clientes et clients avec des messages similaires. Vous pouvez contrôler la fréquence sur plusieurs canaux, en excluant automatiquement les profils sur-sollicités afin d’offrir une meilleure expérience client.</li></ul>

<img src="assets/do-not-localize/gif-conflict.gif">

<p>Les fonctionnalités de gestion des conflits et des priorités sont accessibles en disponibilité limitée pour un groupe sélectionné de clientes et clients. Notez que ces fonctionnalités seront progressivement déployées vers d’autres utilisateurs et utilisatrices à l’avenir. Contactez votre équipe de compte si vous souhaitez qu’elle vous ajoute à la liste d’attente pour ces fonctionnalités.</p>

</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Intégration de Movable Ink et d’Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais intégrer Movable Ink Da Vinci et Adobe Journey Optimizer. Avec cette nouvelle intégration, vous pouvez effectuer les actions suivantes : </p>
<p><ul><li>Tirer parti des puissantes fonctionnalités du produit Da Vinci de Movable Ink pour assembler et personnaliser les variations d’e-mail pour les campagnes par lot</li>
<li>Accélérer les workflows de mise en œuvre pour les clientes et clients Journey Optimizer à l’aide de Da Vinci pour la création et d’Adobe Journey Optimizer pour l’optimisation et la diffusion</li>
<li>Optimisez les modèles Da Vinci avec les données d’Adobe.</li></ul></p>
<p>Pour plus d’informations, consultez la <a href="https://movableink.com/adobe-and-movable-ink">documentation Da Vinci Movable Ink</a>.</p>
</tr>
</tbody>
</table>

Auparavant disponibles pour un ensemble d’organisations (disponibilité limitée), les fonctionnalités suivantes sont désormais disponibles pour tous les utilisateurs et utilisatrices (disponibilité générale) :

<table>
<thead>
<tr>
<th><strong>Personnalisation de la configuration du canal e-mail (disponibilité générale) </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Pour une flexibilité et un contrôle accrus de vos paramètres d’e-mail, vous pouvez définir des sous-domaines dynamiques et des paramètres d’en-tête personnalisés lors de la création de configurations de canal e-mail.
</p>
<p>Pour plus d’informations, consultez la <a href="../email/surface-personalization.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/surface-perso.gif"/>
<p>Disponible depuis le 23 octobre 2024</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Approbations dans les parcours et les campagnes (disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce aux politiques d’approbation, vous pouvez désormais configurer un processus d’approbation dans Journey Optimizer qui permet aux équipes marketing de s’assurer que les campagnes et les parcours sont examinés et approuvés par les parties prenantes appropriées avant qu’ils ne soient mis en ligne.</p>
<p>Pour plus d’informations, consultez la <a href="../test-approve/gs-approval.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/approval.gif"/>
<p>Disponible depuis le 22 octobre 2024</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Expérimentation de contenu dans les parcours (disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Déjà disponible dans les campagnes, Adobe Journey Optimizer prend désormais en charge les expérimentations dans les parcours. Les expériences sont des essais randomisés, ce qui, dans le cadre des tests en ligne, signifie que vous exposez certains utilisateurs et utilisatrices sélectionnés de manière aléatoire à une variante donnée d’un message et un autre ensemble d’utilisateurs et utilisatrices sélectionnés de manière aléatoire à une autre variation de traitement. Après l’exposition, vous pouvez ensuite mesurer les mesures de résultats qui vous intéressent, par exemple les ouvertures d’e-mails, les abonnements ou les achats.</p>
<p>Pour plus d’informations, consultez la <a href="../content-management/content-experiment.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Prise de décision (disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La prise de décision, auparavant disponible pour un ensemble d’organisations (LA) et appelée Décisions pour les expériences, est désormais disponible pour tous les utilisateurs et toutes les utilisatrices (GA), y compris les organisations qui ont acheté les offres de module complémentaire Adobe Healthcare Shield ou Privacy and Security Shield.</p><p>La prise de décision simplifie la personnalisation en offrant un catalogue centralisé d’offres marketing connues sous le nom d’« éléments de décision » et un moteur de décision sophistiqué. Ce moteur tire parti des règles et des critères de classement pour sélectionner et présenter les éléments de décision les plus pertinents à chaque personne. Ces éléments de décision sont intégrés de manière transparente à un large éventail de surfaces entrantes grâce au canal d’expérience basé sur le code.</p>
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/gs-experience-decisioning.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Messages multilingues dans les parcours et les campagnes (disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer facilement du contenu dans plusieurs langues au sein d’une campagne ou d’un parcours. Grâce à cette fonctionnalité, vous pouvez passer d’une langue à une autre lors de la modification de votre campagne ou de votre parcours, ce qui optimise l’ensemble du processus de modification et améliore votre capacité à gérer efficacement du contenu multilingue.</p>
<p>Pour plus d’informations, consultez la <a href="../content-management/multilingual-gs.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/multilingual.gif">
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Mise à jour de l’expérience de création de rapports (disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La création de rapports Journey Optimizer est désormais en disponibilité générale (GA) et est dotée d’une interopérabilité améliorée avec les fonctionnalités de Customer Journey Analytics, ce qui permet de normaliser la création de rapports sur les deux plateformes et d’améliorer la cohérence et la fiabilité des données. L’intégration transparente entre Journey Optimizer et Customer Journey Analytics fournit une meilleure visibilité des mesures de performance, ce qui aide les utilisateurs et les utilisatrices à prendre des décisions plus éclairées.</p>
<p>Avec la disponibilité générale, quatre nouvelles fonctionnalités sont introduites : la possibilité de créer des mesures simples, de créer et de publier des audiences, de poser des questions ad hoc à l’aide d’Insight Builder et de planifier des rapports qui seront automatiquement envoyés par e-mail aux personnes destinataires clés.</p>
<p>Pour plus d’informations, consultez la <a href="../reports/report-cja-manage.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Important : l’expérience actuelle de création de rapports sera abandonnée à compter de janvier 2025. À partir de cette date, la nouvelle expérience de création de rapports deviendra la norme. Nous vous recommandons de vous familiariser avec les nouvelles fonctionnalités pour garantir une transition fluide. <a href="../reports/report-gs-cja.md">Découvrir la nouvelle interface de création de rapports de Journey Optimizer</a></p>
<p>Disponible depuis le 16 octobre 2024</p>
</tr>
</tbody>
</table>

<!--The following capabilities are available to all customers in public beta:-->

<table>
<thead>
<tr>
<th><strong>Tester votre contenu à l’aide d’exemples de données d’entrée (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Désormais, Journey Optimizer vous permet de tester différentes variantes de votre contenu en le prévisualisant et en envoyant des BAT par e-mail à l’aide d’exemples de données d’entrée chargées à partir d’un fichier ou ajoutées manuellement. Tous les attributs de profil utilisés dans votre contenu pour la personnalisation sont automatiquement détectés par le système et peuvent être utilisés pour vos tests afin de créer plusieurs variantes.</p>
<p>Cette fonctionnalité est actuellement disponible pour l’ensemble des clientes et clients en version Beta publique, pour les canaux E-mail, SMS et Notification Push.</p>
<p>Pour plus d’informations, consultez la <a href="../test-approve/simulate-sample-input.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/gif-simulate.gif">
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Utiliser les données Adobe Experience Platform pour la personnalisation (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Exploitez les données d’Adobe Experience Platform dans l’éditeur de personnalisation pour personnaliser votre contenu. Pour ce faire, les jeux de données nécessaires à la personnalisation de la recherche doivent d’abord être activés par le biais d’un appel API. Une fois que vous avez terminé, vous pouvez utiliser leurs données pour personnaliser votre contenu dans [!DNL Journey Optimizer].</p>
<p>Cette fonctionnalité est actuellement disponible en version Beta publique pour l’ensemble des clientes et clients.</p>
<p>Pour plus d’informations, consultez la <a href="../personalization/aep-data-perso.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#24-10-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Canal SMS**

* Vous pouvez désormais modifier ou supprimer une configuration de canal de l’API SMS. [En savoir plus](../sms/sms-configuration.md)

* Les améliorations suivantes ont été ajoutées pour améliorer vos fonctionnalités de messagerie SMS avec Infobip et Sinch :

   * Vous pouvez définir et gérer des mots-clés uniques pour vos campagnes et parcours SMS, ce qui permet une communication plus personnalisée et efficace.

   * Vous pouvez créer et diffuser un SMS par défaut lorsqu’un mot-clé n&#39;est pas reconnu.

  Pour en savoir plus sur ces améliorations, consultez la documentation de la configuration des SMS pour [Infobip](../sms/sms-configuration-infobip.md) et [Sinch](../sms/sms-configuration-sinch.md).


<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

<!--* **Max number of Live journeys** - Journey Optimizer now has a guardrail of 500 live journeys on production sandboxes, instead of 100. The number of live journeys is visible in the journey canvas. (DOCAC-10977) -->

**Canal web**

* **Mode de modification non visuel pour le concepteur web** - Vous pouvez désormais apporter des modifications à votre site web à l’aide d’un éditeur non visuel au lieu d’utiliser le concepteur web de Journey Optimizer. Cela vous permet d’effectuer vos modifications manuellement sans ouvrir les pages dans l’éditeur visuel. Ce mode de modification non visuel est utile si vous ne pouvez pas installer d’extensions de navigateur telles que Visual Helper d’Adobe Experience Cloud, nécessaires pour charger vos pages dans le concepteur web. [En savoir plus](../web/web-non-visual-editor.md)


**Jeux de données**

* **Événements d’envoi et d’ouverture** : à compter du 1er novembre 2024, la segmentation du streaming ne prendra plus en charge l’utilisation des événements d’envoi et d’ouverture provenant des jeux de données de tracking et de commentaires de Journey Optimizer. Cette modification s’appliquera à l’ensemble des sandbox et organisations des clientes et clients. [En savoir plus](../data/datasets-ttl.md#segmentation-update)

* **Durée de vie du jeu de données (TTL)** : à compter de février 2025, un mécanisme de sécurisation sur la durée de vie (TTL) sera déployé sur les jeux de données générés par le système Journey Optimizer dans les nouveaux sandbox et les nouvelles organisations comme suit :

   * 90 jours pour les données dans la banque de profils
   * 13 mois pour les données du lac de données

  Cette modification sera déployée sur les sandbox des clientes et clients existants au cours d’une phase ultérieure. [En savoir plus](../data/datasets-ttl.md#ttl-guardrail)

* **Paramètres dans les actions personnalisées** - Date de disponibilité : 3 octobre 2024 - Les paramètres NULL et facultatifs sont désormais pris en charge dans les actions personnalisées. [En savoir plus](../action/about-custom-action-configuration.md#define-the-message-parameters).

**Créer des rapports**

* **La création de rapports pour la prise de décision** est désormais disponible et offre des informations essentielles sur la manière dont vos visiteurs et visiteuses interagissent avec vos expériences. [En savoir plus](../reports/campaign-global-report-cja-code.md#decisioning-kpis)

**Gouvernance des données et politiques de consentement** : date de disponibilité : 7 octobre 2024

* L’application des **politiques de gouvernance des données** a désormais lieu sur tous les canaux dans Journey Optimizer. Pour les clientes et clients qui ont créé des politiques dans Adobe Experience Platform, ces dernières sont appliquées aux actions marketing dans le cadre des configurations des canaux. Lorsque vous créez du contenu à l’aide d’une configuration, le système vérifie tous les champs de personnalisation à la recherche de toute violation de gouvernance des données. Si une violation est trouvée, la publication d’un parcours ou d’une campagne n’est pas possible. [En savoir plus](../action/action-privacy.md)

* Les **politiques de consentement personnalisé** s’appliquent désormais à tous les canaux Journey Optimizer. Lors de l’application, avant l’envoi d’un message ou avant la diffusion d’une expérience entrante, le système vérifie que la personne a donné son consentement pour utiliser des champs de personnalisation dans le contenu qu’elle reçoit. Si aucun consentement n’est donné, l’expérience ne s’affiche pas. [En savoir plus](../action/consent.md)

  >[!NOTE]
  >
  >Les politiques de consentement ne sont actuellement disponibles que pour les organisations qui ont acheté les offres complémentaires Adobe **Healthcare Shield** et **Privacy and Security Shield**.

**Audiences** : date de disponibilité : 8 octobre 2024

* Lors du ciblage d’une audience de fichier CSV, vous pouvez désormais utiliser les attributs du fichier dans l’éditeur de personnalisation et dans le créateur de règles de parcours et de campagnes. [En savoir plus](../audience/about-audiences.md)

* L’utilisation des audiences et des attributs du chargement personnalisé (fichiers CSV) est désormais disponible avec Healthcare Shield ou Privacy and Security Shield.

**Configuration** : date de disponibilité : 23 octobre 2024

* Lors de l’utilisation d’une configuration personnalisée dans une campagne ou un parcours, vous pouvez désormais prévisualiser le contenu de votre e-mail afin de rechercher les erreurs potentielles avec les paramètres dynamiques que vous avez définis. [En savoir plus](../email/surface-personalization.md#check-configuration)

**Canal basé sur le code**

* Des modèles de contenu sont désormais disponibles. Vous pouvez accélérer la création de vos expériences basées sur du code à partir d’un modèle de contenu créé par vos développeurs et développeuses. L’utilisation d’un modèle de contenu permet aux personnes spécialisées dans le marketing de modifier uniquement certaines valeurs ou certains champs, au lieu de composer l’ensemble du payload de contenu HTML ou JSON. [En savoir plus](../content-management/content-templates.md)

**Prise de décision**

* Les utilisateurs et utilisatrices d’[Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=fr) peuvent désormais choisir des modèles personnalisés à optimiser lors de la configuration d’un modèle IA dans la prise de décision (anciennement appelée Décisions pour les expériences). Cela vous permet, par exemple, d’optimiser un tableau personnalisé « achats » plutôt que des contraintes définies telles que le taux de clics. [En savoir plus](../experience-decisioning/ranking/ranking.md)

* Lors de l’ajout d’une politique de décision à une campagne basée sur du code avec la prise de décision, vous pouvez désormais sélectionner manuellement des éléments de décision uniques, en plus des stratégies de sélection. En outre, vous pouvez désormais sélectionner plusieurs offres de secours. Cela garantit qu’un certain nombre d’éléments de décision sont renvoyés. [En savoir plus](../experience-decisioning/create-decision.md)



## Version de septembre 2024 {#24-9-rn}

<!--
>[!CAUTION]
>
>**Early release notes below are subject to change without prior notice until the release date**. Links, screens and updated documentation are published at the release date.
>
-->

**Date de publication** : 24-26 septembre 2024

### Nouvelles fonctionnalités {#24-9-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Cartes de contenu pour les applications mobiles et les sites web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les cartes de contenu sont une nouvelle fonctionnalité de messagerie numérique d’Adobe Journey Optimizer qui fournit du contenu personnalisé et attrayant, directement dans les applications mobiles et les sites web. Contrairement aux notifications push traditionnelles, les cartes de contenu s’intègrent de manière transparente à l’interface d’utilisation, en offrant des mises à jour persistantes et non intrusives qui améliorent l’interaction et l’expérience des utilisateurs et utilisatrices.</p>
<p>Grâce à cette fonctionnalité, les spécialistes du marketing peuvent présenter du contenu multimédia pertinent aux utilisateurs et utilisatrices, augmenter l’engagement des personnes et veiller à ce que les messages importants soient affichés sans interrompre le parcours d’utilisation.</p>
<p>Pour plus d’informations, consultez la <a href="../../rp_landing_pages/content-card-landing-page.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/content-card.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Approbations dans les parcours et les campagnes (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce aux politiques d’approbation, vous pouvez désormais configurer un processus d’approbation dans Journey Optimizer qui permet aux équipes marketing de s’assurer que les campagnes et les parcours sont examinés et approuvés par les parties prenantes appropriées avant qu’ils ne soient mis en ligne.</p>
<p>Les politiques d’approbation ne sont actuellement disponibles que pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Pour plus d’informations, consultez la <a href="../test-approve/gs-approval.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Email Content Locking</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer now allows you to lock content in email templates, either by locking the entire template or specific structures and component. This allows you to prevent unintentional edits or deletions, giving you greater control over template customization, and improving the efficiency and reliability of your email campaigns.</p>
<p>For more information, refer to the <a href="../content-management/gs-generative.md">detailed documentation</a>.</p>
<img src="assets/do-not-localize/gif-content-locking.gif">
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Critères de sortie globale dans les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous définissez maintenant des critères de sortie au niveau du parcours. En ajoutant des critères de sortie, vous faites quitter le parcours aux profils dès qu’un événement se produit (un achat, par exemple) ou qu’ils répondent aux critères d’une audience. Cela évite à l’utilisateur ou à l’utilisatrice de recevoir d’autres communications du parcours.</p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/journey-properties.md#exit-criteria">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistant IA</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une fois que vous avez créé et personnalisé votre message, améliorez la qualité de votre contenu avec l’assistant IA dans Journey Optimizer. Vous pouvez désormais utiliser l’assistant IA pour optimiser l’impact de votre message en testant différents titres et images. Chaque variante est gérée en tant que traitement unique, afin de la mesurer et de la comparer pour savoir quel titre génère le plus de clics.</p>
<p>Découvrez une expérience pratique avec <a href="https://experienceleague.adobe.com/fr/apps/journey-optimizer/ai-assistant-content-accelerator">notre aperçu des fonctionnalités en direct</a>, conçu pour vous permettre d’explorer directement ses fonctionnalités et de les comprendre pleinement.</a>.</p>
<p>Pour plus d’informations, consultez la <a href="../content-management/gs-generative.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/ai-content.gif"/>
<p>Date de disponibilité : 12 septembre 2024</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Configuration de canal guidée</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La configuration de canal guidée vous permet d’automatiser et de valider la configuration de canal dans une expérience unifiée, ce qui accélère le processus de prise en main de Journey Optimizer. Cette nouvelle configuration guidée simplifie la configuration rapide des canaux, en s’assurant que toutes les ressources nécessaires sont facilement installées et qu’elles fonctionnent dans Experience Platform, Journey Optimizer et la Collecte de données. Cela permet aux équipes d’ingénierie marketing, produit et données de lancer rapidement la création de campagnes et de parcours.</p>
<p>Pour plus d’informations, consultez la <a href="../configuration/set-mobile-config.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/guided-setup.gif"/>
<p>Date de disponibilité : 3 septembre 2024</p>
</br>
</td>
</tr>
</tbody>
</table>


### Améliorations {#24-9-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Audiences** : date de disponibilité : 17 septembre 2024

**Utilisation de la licence** : le tableau de bord Utilisation de la licence affiche désormais les profils engageables au lieu des audiences engageables. [En savoir plus](../audience/license-usage.md)

**Gestion de contenu**

Vous pouvez désormais exporter des modèles de contenu et des fragments entre les sandbox. [En savoir plus](../configuration/copy-objects-to-sandbox.md)

**Parcours**

* **Améliorations des rapports dynamiques** : les rapports dynamiques fournissent des informations sur les performances de vos parcours au cours des dernières 24 heures. Nous les avons améliorés en ajoutant de nouvelles mesures (profils entrés, sortis, ignorés et profils en erreur), ce qui vous permet de mieux comprendre le comportement et les performances des utilisateurs et utilisatrices directement à partir de la zone de travail du parcours. [En savoir plus](../building-journeys/report-journey.md)


* (Date de disponibilité : 10 septembre) **Reprises automatiques sur la Lecture d’audience** : les reprises sont désormais appliquées par défaut sur les parcours déclenchés par l’audience (commençant par une **Lecture d’audience** ou un **Événement métier**) lors de la récupération du traitement d’export. Si une erreur se produit lors de la création du traitement d’export, des reprises sont effectuées toutes les 10 minutes, pendant 1 heure au maximum. Après cela, nous considérerons cela comme un échec. Ces types de parcours peuvent donc être exécutés jusqu’à 1 heure après l’heure planifiée. [En savoir plus](../building-journeys/read-audience.md#retries)

**Canal e-mail**

* **En-tête du message dans l’e-mail envoyé et copie en Cci** : un nouvel en-tête a été ajouté à tous les e-mails. La valeur de cet en-tête est propre à chaque e-mail envoyé et à sa copie d’e-mail en Cci correspondante. Cet en-tête est également stocké dans les jeux de données de retour des messages et des commentaires en Cci, ce qui permet de réconcilier la copie en Cci et les informations d’e-mail envoyées correspondantes. [En savoir plus](../configuration/archiving-support.md#bcc-header)

* **Notation de spam** (disponibilité générale) : vous pouvez désormais vérifier la notation de spam de votre contenu dans un **rapport de spam** dédié. Grâce à SpamAssassin, Adobe Journey Optimizer peut désormais tester le contenu de vos e-mails et lui attribuer un score pour indiquer si les FAI ou les fournisseurs de messagerie le considèrent comme un spam ou non. [En savoir plus](../content-management/spam-report.md)

**Canal SMS**

* **Modifier les informations d’identification de l’API** : vous pouvez désormais modifier les paramètres dans les informations d’identification de l’API SMS, y compris les mises à jour des mots-clés et réponses d’inclusion/exclusion.

**API**

* **API de simulation de campagne** : utilisez cette API pour déclencher le traitement de BAT d’une campagne. L’envoi du BAT de campagne est un processus asynchrone. L’API renvoie un BATJobId qui peut être utilisé pour vérifier le statut du BAT. [En savoir plus](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"}

* (Date de disponibilité : 10 septembre) La [documentation de l’API Adobe Journey Optimizer](https://developer.adobe.com/journey-optimizer-apis/references/simulations/){target="_blank"} est désormais interactive. Explorez les points d’entrée de l’API directement à partir des pages de la documentation pour obtenir des commentaires immédiats et accélérer votre implémentation technique.


  Toutes les pages de référence de l’API possèdent désormais une fonctionnalité **Essayer**. Cette fonctionnalité vous permet de tester les appels API directement sur la page du site web de la documentation. [Obtenez les informations d’authentification requises](https://developer.adobe.com/journey-optimizer-apis/references/authentication/){target="_blank"} et commencez à utiliser la fonctionnalité pour explorer les points d’entrée de l’API.

  Utilisez cette nouvelle fonctionnalité pour explorer les requêtes envoyées et les réponses issues des points d’entrée de l’API, afin d’obtenir des commentaires immédiats et d’accélérer votre implémentation technique.

  >[!CAUTION]
  >
  >Notez qu’en utilisant la fonctionnalité d’API interactive sur les pages de documentation, vous effectuez de vrais appels API vers les points d’entrée. Gardez cela à l’esprit lorsque vous effectuez des tests dans des sandbox de production.

**Configuration**

* **Plans de préchauffage des adresses IP** : cette fonctionnalité est désormais disponible pour l’ensemble de la clientèle, y compris les organisations qui ont acheté les offres complémentaires Adobe **Healthcare Shield** ou **Privacy and Security Shield**. [En savoir plus](../configuration/ip-warmup-gs.md)

<!--
![Newsletter](../assets/do-not-localize/nl-icon.png) Sign up for the [Adobe Journey Optimizer quarterly newsletter](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} today, and receive the latest product updates, exciting stories, use cases, tips and more delivered directly to your inbox every quarter.-->



## Version d’août 2024 {#8-2024}

**Date de publication** : 20-21 août 2024

### Nouvelles fonctionnalités {#8-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous.

<!--
<table>
<thead>
<tr>
<th><strong>Content Cards (Limited Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Content cards are a new digital messaging feature in Adobe Journey Optimizer that delivers personalized and engaging content directly within mobile apps and websites. Unlike traditional push notifications, Content Cards integrate seamlessly into the user interface, offering persistent, non-intrusive updates that enhance user interaction and experience.</p>
<p>This feature enables marketers to present relevant, rich media content to users, driving higher engagement and ensuring important messages are seen without disrupting the user journey.</p>
</br>
<p>Content card are currently only available for a set of organizations (Limited Availability). To gain access, contact your Adobe representative.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Amélioration des configurations de canal</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les fonctionnalités actuelles de surface de canal ont été améliorées afin de fournir une approche cohérente sur tous les canaux. Vous pouvez désormais définir, gérer et réutiliser ces configurations pour l’un de vos canaux, y compris les canaux web, les messages in-app ou l’expérience basée sur le code.</p>
<p><ul>
<li>Les surfaces de canal sont désormais renommées <strong>Configurations de canal</strong>.</li>
<li>Vous pouvez joindre une ou plusieurs actions marketing pour appliquer des politiques de consentement et de gouvernance des données.</li>
<li>Le contrôle d’accès au niveau de l’objet (OLAC) est désormais disponible pour chaque configuration de canal, ce qui vous permet de décider qui parmi vos utilisateurs et utilisatrices peut créer ou utiliser des configurations spécifiques.</li>
<li>Pour certains canaux, vous pouvez créer des configurations de canal qui ciblent plusieurs plateformes. Il peut s’agir, par exemple, d’une configuration de canal de messagerie in-app pouvant cibler une page web, une application iOS et une application Android.</li>
</ul></p>
<p>Pour plus d’informations, consultez la <a href="../configuration/channel-surfaces.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Action personnalisée Marketo Engage</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais intégrer Adobe Journey Optimizer à Adobe Marketo Engage pour créer vos cas d’utilisation B2B. Depuis un parcours, une nouvelle action personnalisée vous permet d’ingérer des données dans Marketo.</p>
<p>Pour plus d’informations, consultez la <a href="../action/marketo-engage.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Variables dans les fragments de contenu</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les variables globales de fragment améliorent la fonctionnalité de fragment existante afin d’optimiser l’efficacité de réutilisation du contenu et les cas d’utilisation de script. Les fragments peuvent désormais utiliser des variables d’entrée et créer des variables de sortie utilisables dans le contenu des campagnes et des parcours. Les fragments peuvent désormais utiliser des variables d’entrée, à la fois dans les <a href="../personalization/use-expression-fragments.md">fragments d’expression</a> et les <a href="../email/use-visual-fragments.md">fragments visuels</a>. Vous pouvez utiliser ces variables pour personnaliser le contenu et les paramètres de vos messages, dans vos campagnes et parcours.</p>
<p>Pour plus d’informations, consultez la <a href="../personalization/use-expression-fragments.md">documentation détaillée</a>.</p>
</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Workflow de préchauffage d’adresses IP</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Date de disponibilité : 13 août</p>
<p>Si vous envoyez des e-mails sur une toute nouvelle adresse IP, vous pouvez désormais facilement exécuter des workflows de préchauffage d’adresses IP directement à partir de l’interface d’utilisation. Adobe Journey Optimizer offre un moyen standardisé et efficace de préchauffer vos adresses IP en respectant les bonnes pratiques de délivrabilité optimale.</p>
<p>Pour plus d’informations, consultez la <a href="../configuration/ip-warmup-gs.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#8-improvements}

Cette version apporte les améliorations répertoriées ci-dessous.

**Parcours**

* Dans l’activité **Condition**, par défaut, la **[!UICONTROL Condition de temps]** est désormais définie par heure, de 00:00 à 12:00. [En savoir plus](../building-journeys/condition-activity.md#time_condition)
* Lors de la création de vos parcours, les alertes s’affichent désormais à partir du bouton **Alertes**, afin de s’aligner sur d’autres alertes et d’offrir une expérience d’utilisation cohérente. [En savoir plus](../building-journeys/troubleshooting.md#activity-errors)
* Les options de zoom de la barre d’outils des parcours ont été améliorées : le pourcentage de zoom est désormais visible et vous pouvez facilement réinitialiser sa valeur.

**Canal push**

* Vous pouvez maintenant ajouter vos informations d’identification push d’application mobile dans les paramètres de configuration du canal Adobe Journey Optimizer. La création d’une surface d’application dans la collecte de données Adobe Experience Platform n’est plus nécessaire.

### Autres modifications {#changes}

**Création de rapports**

* De nouveaux cas d’utilisation ont été ajoutés à la nouvelle expérience de création de rapports :

   * Créez des mesures calculées personnalisées directement dans vos rapports.
   * Créez une audience à partir des données de rapport.
   * Utilisez l’outil d’analyse exploratoire pour créer facilement des tableaux et des visualisations à partir des **[!UICONTROL dimensions]** et des **[!UICONTROL mesures]** sélectionnées.

  Pour plus d’informations, consultez la [documentation détaillée](../reports/report-cja-manage.md).



## Version de juillet 2024 {#24-7-2024}

**Date de version** : 30-31 juillet 2024

### Nouvelles fonctionnalités {#27-4-features}

Cette version apporte les nouvelles fonctionnalités répertoriées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Canal SMS avec n’importe quel fournisseur (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais configurer d’autres fournisseurs de SMS dans Journey Optimizer, en plus des fournisseurs par défaut Sinch, Infobip et Twilio.</p>
<img src="assets/do-not-localize/byo_sms.gif"/>
<p>Pour plus d’informations, consultez la <a href="../sms/sms-configuration-custom.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Composition d’audiences fédérées (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La composition d’audiences fédérées est désormais disponible dans Adobe Journey Optimizer. Elle permet aux entreprises de composer des données pour améliorer leur emploi dans divers cas d’utilisation. Grâce à cette nouvelle approche, en tant qu’utilisateur ou utilisatrice d’Adobe Real-Time Customer Data Platform et/ou d’Adobe Journey Optimizer, vous pouvez fédérer les jeux de données directement à partir de votre entrepôt de données existant pour créer et enrichir les audiences et les attributs Adobe Experience Platform dans un seul système.</p>
<p>Pour plus d’informations, consultez la <a href="https://experienceleague.adobe.com/fr/docs/federated-audience-composition/using/home"  target="_blank">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#27-4-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Parcours**

* (Date de disponibilité : 8 juillet) **Éditeur d’expression avancé dans la configuration des événements des parcours** : vous pouvez désormais utiliser l’éditeur d’expression avancé lors de la configuration d’un événement, ce qui vous permet de définir des expressions plus complexes ou d’utiliser des fonctions dans la condition d’identifiant d’événement. [En savoir plus](../event/about-creating.md#adv-exp-editor)



## Version de juin 2024 {#24-6-2024}

**Date de publication** : 18-19 juin 2024

### Nouvelles fonctionnalités {#june-24-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Personnalisation des fragments de contenu</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais définir des champs spécifiques dans un fragment qui peuvent être modifiés lors de l’ajout du fragment à une campagne ou à un parcours. Cela permet d’ajuster les portions de contenu au moment de l’utilisation, ce qui offre la possibilité de remplacer les valeurs par défaut par des informations spécifiques au contexte.</p>
<img src="../content-management/assets/do-not-localize/gif-fragments.gif"/>
<p>Pour plus d’informations, consultez la <a href="../content-management/customizable-fragments.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Créer des rapports avec Customer Journey Analytics (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>La création de rapports Journey Optimizer est fournie avec une interopérabilité améliorée avec les fonctionnalités de Customer Journey Analytics, ce qui permet de normaliser la création de rapports sur les deux plateformes et d’améliorer la cohérence et la fiabilité des données. L’intégration transparente entre Journey Optimizer et Customer Journey Analytics fournit une meilleure visibilité des mesures de performance, ce qui aide les utilisateurs et les utilisatrices à prendre des décisions plus éclairées.</p>
<img src="assets/do-not-localize/ajo-cja.gif"/>
<p>Pour plus d’informations, consultez la <a href="../reports/report-gs-cja.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Assistant IA dans Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’assistant IA est une fonctionnalité de l’interface d’utilisation qui vous permet de parcourir et de comprendre les concepts Adobe et d’obtenir des informations opérationnelles sur votre environnement spécifique. Il est disponible dans plusieurs produits Adobe Experience Cloud, y compris Adobe Journey Optimizer.</p>
<p>Pour plus d’informations, consultez la <a href="../start/ai-features.md#ai-assistant">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Messages multilingues dans les parcours et les campagnes (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer facilement du contenu dans plusieurs langues au sein d’une campagne ou d’un parcours. Grâce à cette fonctionnalité, vous pouvez passer d’une langue à une autre lors de la modification de votre campagne ou de votre parcours, ce qui optimise l’ensemble du processus de modification et améliore votre capacité à gérer efficacement du contenu multilingue.</p>
<p>Le contenu multilingue n’est actuellement disponible que pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Expérimentation dans les parcours (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Déjà disponible dans les campagnes, Adobe Journey Optimizer prend désormais en charge les expérimentations dans les parcours. Les expériences sont des essais randomisés, ce qui, dans le cadre des tests en ligne, signifie que vous exposez certains utilisateurs et utilisatrices sélectionnés de manière aléatoire à une variante donnée d’un message et un autre ensemble d’utilisateurs et utilisatrices sélectionnés de manière aléatoire à une autre variation de traitement. Après l’exposition, vous pouvez ensuite mesurer les mesures de résultats qui vous intéressent, par exemple les ouvertures d’e-mails, les abonnements ou les achats.</p>
<p>L’expérimentation dans les parcours n’est actuellement disponible que pour un ensemble donné d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Améliorations {#june24-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

#### Gestion des décisions

* **Prise en charge de plusieurs règles dans la gestion des décisions** : vous pouvez désormais ajouter jusqu’à 10 règles de limitation pour une offre donnée dans la gestion des décisions. Cela vous permet d’augmenter le niveau de contrôle sur la manière dont les offres sont envoyées. [En savoir plus](../offers/offer-library/add-constraints.md#capping)

<!--* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->

#### Fragments de contenu

>[!AVAILABILITY]
>
>Notez que ces améliorations seront progressivement déployées dans les jours qui suivront la version initiale. Certains utilisateurs et utilisatrices auront un accès immédiat, mais d’autres peuvent rencontrer un retard avant que cela ne soit disponible dans leurs environnements.

* Les fragments peuvent désormais être modifiés et les modifications peuvent être propagées dans tous les parcours actifs et toutes les campagnes dans lesquels elles sont utilisées.
* De nouveaux statuts pour les fragments de contenu ont été ajoutés : **Brouillon**, **Actif**, **Publication** et **Archivé**.
* Pour utiliser un fragment dans un parcours ou une campagne, il doit maintenant se trouver au statut **Actif**. Une nouvelle étape a été ajoutée au processus de création de fragment, permettant de publier le fragment et de le rendre disponible à l’utilisation dans les parcours et les campagnes. Notez que la publication de fragments nécessite une nouvelle autorisation.

  **ATTENTION** : depuis l’introduction des statuts **Brouillon** et **Actif** avec la version de juin de Journey Optimizer, tous les fragments créés avant cette version ont le statut **Brouillon**, même s’ils sont utilisés dans un parcours ou une campagne. Si vous apportez des modifications à ces fragments, vous devez [les publier](../content-management/create-fragments.md#publish) pour les rendre « actives » et les propager aux campagnes et parcours associés. Vous devez également créer une version de parcours/campagne et la publier.

En savoir plus dans la documentation sur les [fragments de contenu](../content-management/fragments.md).

#### Parcours

* Le délai d’expiration global des parcours a été étendu à 91 jours. [En savoir plus](../building-journeys/journey-properties.md#global_timeout)

  Ce nouveau délai d’expiration sera pris en compte pour tous les nouveaux parcours créés. Consultez cette [section Questions fréquentes](../building-journeys/journey-properties.md#timeout-faq) pour en savoir plus. Notez que ces modifications seront progressivement appliquées au cours du mois de juin.


* Adobe Journey Optimizer prend désormais en charge les demandes de suppression/d’accès pour les informations personnelles ainsi que les demandes de gestion du cycle de vie des données. [En savoir plus](../privacy/requests.md)
* Vous pouvez désormais redimensionner les colonnes de l’inventaire des parcours.
  <!--* **Advanced expression editor in Event configuration** is now GA - You can now leverage the advanced expression editor while configuring an event, allowing you to define more complex expressions or use functions in the event id condition. This capability is released in Limited Availability for selected customers. [Read more](../event/about-creating.md)-->
* **Les politiques de fusion** sont maintenant disponibles de manière générale : les politiques de fusion utilisées par un parcours sont désormais visibles et cohérentes dans l’ensemble du parcours. [En savoir plus](../building-journeys/journey-properties.md#merge-policies)


#### Campagnes

* Lors de la création d’une campagne dans Adobe Journey Optimizer, vous pouvez désormais choisir le type de campagne (planifiée ou déclenchée) dans une nouvelle boîte de dialogue modale. [En savoir plus](../campaigns/create-campaign.md)

#### Canal e-mail

* **Désabonnement de la liste** : comme suite aux récentes annonces Gmail et Yahoo! concernant les expéditions en masse, Journey Optimizer prend en charge l’option de désabonnement de la liste « post/1-click ». Consultez les pages suivantes : [Gestion du processus de désinscription aux e-mails](../email/email-opt-out.md#unsubscribe-header) et [Configurer les paramètres d’e-mail](../email/email-settings.md#list-unsubscribe).

  **NOTE** : pour toute nouvelle surface de canal, l’option d’en-tête de désabonnement de la liste est activée par défaut. Pour les surfaces existantes, l’option URL de désabonnement en un clic dans les paramètres de surface de canal est décochée par défaut. Si vous utilisiez précédemment une URL d’opt-out en un clic dans le corps de l’e-mail, ce paramètre est toujours valide. Si l’URL de désabonnement en un clic est cochée dans les paramètres de surface de canal, Adobe Journey Optimizer préférera utiliser l’URL de désabonnement en un clic générée par défaut dans les paramètres de surface de canal.

#### Canal SMS

* Vous pouvez désormais ajouter des codes courts uniques pour chaque sandbox avec une seule configuration d’API, ce qui rend le processus plus efficace et plus simple. [En savoir plus](../sms/sms-configuration.md)

* Après la création, le champ **Jeton API** sur le page **Détails des informations d’identification de l’API** est désormais masqué.

<!--* You can now modify existing SMS configurations.-->

#### Canal in-app

<!--* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

* Vous pouvez désormais utiliser le plug-in Edge Delivery pour obtenir les informations nécessaires pour comprendre et résoudre les problèmes liés à vos implémentations entrantes. [En savoir plus sur la vue Edge Delivery](https://experienceleague.adobe.com/fr/docs/experience-platform/assurance/view/edge-delivery){target="_blank"}.


#### Canal de publipostage direct

* Le canal de publipostage direct est désormais disponible pour l’ensemble des clientes et clients. [En savoir plus](../direct-mail/get-started-direct-mail.md)



## Version de mai 2024 {#may-2024}

**Date de publication** : 21-22 mai 2024

### Nouvelles fonctionnalités {#e-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Décisions pour les expériences  - Disponibilité limitée</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Décisions pour les expériences simplifie la personnalisation en offrant un catalogue centralisé d’offres marketing connues sous le nom d’« éléments de décision » et un moteur de décision sophistiqué. Ce moteur tire parti des règles et des critères de classement pour sélectionner et présenter les éléments de décision les plus pertinents à chaque personne.</p>
<p>Ces éléments de décision sont intégrés de manière transparente à un large éventail de configurations entrantes grâce au nouveau canal d’expérience basée sur le code, désormais accessible dans les campagnes Journey Optimizer. Les politiques de décisions pour les expériences ne peuvent être utilisées que dans des campagnes d’expérience basées sur du code.</p>
<p>Ces décisions pour les expériences ne sont actuellement disponibles que pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<img src="assets/do-not-localize/gif-exd.gif"/>
<p>Pour plus d’informations, consultez la <a href="../experience-decisioning/gs-experience-decisioning.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Personnalisation de la configuration du canal e-mail - Disponibilité limitée</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais définir des sous-domaines dynamiques et des paramètres d’en-tête personnalisés lors de la création de configuration de canal e-mail pour une meilleure flexibilité et un meilleur contrôle de vos paramètres d’e-mail.</p>
<p>La personnalisation de la configuration du canal e-mail n’est actuellement disponible que pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Pour plus d’informations, consultez la <a href="../email/surface-personalization.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>IP Warmup Workflow</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>If you are sending email on a brand new IP address, you can now easily perform IP warmup workflows directly from the user interface. Adobe Journey Optimizer offers a standardized and efficient way to warm up your IP adresses that follows the best practices for optimal deliverability.</p>
<p>For more information, refer to the <a href="../configuration/ip-warmup-gs.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<!--table>
<thead>
<tr>
<th><strong>Business rules - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create granular frequency capping rules, and apply them to different types of marketing communications through rule sets. This new capability lets you control how often your audiences receive a message by setting cross-channel rules, that automatically exclude over-solicited profiles from messages and actions.</p>
<p>Business rules capability is currently available as a beta. To join the beta program, contact your Adobe representative.</p>
<p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Extended personalization data - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now lookup and fetch data values within Adobe Experience Platform datasets, and use these values to build conditions in Adobe Journey Optimizer. You can leverage data from a lookup dataset when a relationship has been defined using an attribute inside of an array of objects. You can specify non-profile enabled datasets for lookup. Once enabled, you can use a profile attribute as a join key to the specified dataset to retrive further data for personalization.</p>
<p>This capability is currently available as a public beta.</p>
</td>
</tr>
</tbody>
</table-->

### Améliorations {#e-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Décisions pour les expériences** (Disponibilité limitée)

De la version Beta à cette version, les améliorations suivantes ont été ajoutées :

* **Décisions pour les expériences + expériences basées sur le code** : vous pouvez désormais tirer profit de la fonctionnalité de prise de décision basée sur l’expérience pour utiliser des éléments de décision dans vos campagnes basées sur du code. Note : le canal Expérience basée sur le code et les décisions pour les expériences ne sont pas disponibles pour les organisations qui ont acheté les offres complémentaires Healthcare Shield et Privacy and Security Shield d’Adobe. [En savoir plus](../code-based/get-started-code-based.md)
* **Données contextuelles** : vous pouvez désormais exploiter les données contextuelles d’Adobe Experience Platform dans vos règles de décision et formules de classement. [En savoir plus](../experience-decisioning/context-data.md)
* **Nouvelle autorisation** : une nouvelle autorisation « Gérer les décisions basées sur l’expérience » est désormais disponible pour la ressource Gestion des décisions. Elle vous permet de gérer les droits liés aux décisions pour les expériences. [En savoir plus](../experience-decisioning/gs-experience-decisioning.md)
* **Règles de limitation** : vous pouvez désormais ajouter plusieurs règles de limitation pour un élément de décision donné dans les décisions pour les expériences. Cela vous permet d’augmenter le niveau de contrôle sur la manière dont les offres sont envoyées. [En savoir plus](../experience-decisioning/items.md#capping)
* **Rapports** : vous pouvez désormais créer des tableaux de bord de rapports personnalisés pour les campagnes de décisions pour les expériences à l’aide de [!DNL Customer Journey Analytics]. [En savoir plus](../experience-decisioning/cja-reporting.md)


<!--**Decision Management**

* **Multi-rule support** - You can now add up to 10 capping rules for a given offer in Decision Management. This allows you to increase the level of control over the way offers are sent.
* **Audits** - The **Change log** tab allowing you to see all the changes that have been made to an offer or a decision has been removed. Changes related to offers and decisions can now be seen in the **Audits** menu. -->


**Canal e-mail**

<!--
* **List-unsubscribe** - Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. Refer to the following pages: [Email opt-out management](../email/email-opt-out.md#unsubscribe-header) and [Configure email settings](../email/email-settings.md#list-unsubscribe)
-->

* **Notation de spam** (Beta) : vous pouvez désormais vérifier la notation de spam de votre contenu dans un rapport de spam dédié. Grâce à SpamAssassin, Adobe Journey Optimizer peut désormais tester le contenu de vos e-mails et lui attribuer un score pour indiquer si les FAI ou les fournisseurs de messagerie le considèrent comme un spam ou non. [En savoir plus](../content-management/spam-report.md)

  >[!AVAILABILITY]
  >
  >Cette fonctionnalité est actuellement en version Beta et disponible uniquement pour les clientes et clients Beta. Pour rejoindre le programme Beta, contactez votre représentant ou représentante Adobe.

<!--
**Audiences**

* The use of audiences and attributes from audience composition and custom upload (CSV file) is now available for use with Healthcare Shield or Privacy and Security Shield.-->

<!--**Personalization**

* **Expression fragment** - Expression fragments are now available for the **In-app channel**. [Read more](../personalization/use-expression-fragments.md)-->

**Parcours**

<!--* **Merge policies** (Limited Availability)- Merge policies used by a journey are now visible and consistent throughout the journey.-->
* **Prise en charge de mTLS** : l’authentification mTLS est désormais prise en charge dans les actions personnalisées. Aucune configuration supplémentaire n’est requise dans l’action ou le parcours personnalisé pour activer mTLS. L’activation se produit automatiquement lorsqu’un point d’entrée compatible mTLS est détecté. [En savoir plus](../action/about-custom-action-configuration.md#mtls-protocol-support)
* **Tables de recherche dans les événements** :vous pouvez désormais exploiter les données d’un jeu de données de recherche lorsqu’une relation a été définie à l’aide d’un attribut dans un tableau d’objets. Les valeurs de recherche seront disponibles dans les parcours (conditions, actions personnalisées, etc.) et dans la personnalisation des messages. [En savoir plus](../event/experience-event-schema.md#relationships_limitations)
* **Éditeur d’expression avancé dans la configuration des événements** (LA) : vous pouvez désormais utiliser l’éditeur d’expression avancé lors de la configuration d’un événement, ce qui vous permet de définir des expressions plus complexes ou d’utiliser des fonctions dans la condition d’identifiant d’événement. Cette fonctionnalité est publiée en disponibilité limitée pour certaines clientes et certains clients uniquement. [En savoir plus](../event/about-creating.md#adv-exp-editor)
* **Politiques de fusion** (LA) : les politiques de fusion utilisées par un parcours sont désormais visibles et cohérentes dans l’ensemble du parcours. Cette fonctionnalité est publiée en disponibilité limitée pour certaines clientes et certains clients uniquement. [En savoir plus](../building-journeys/journey-properties.md#merge-policies)

**Mondialisation**

Dans le cadre de nos efforts continus pour offrir une expérience utilisateur et utilisatrice unifiée, nous harmonisons la terminologie utilisée dans les produits et applications Adobe Experience Cloud. Cela concerne le terme allemand « Titel » qui est remplacé par « Label » lorsqu’il se rapporte au nom d’un objet. Les modifications seront progressivement déployées dans l’interface utilisateur et dans la documentation.


## Version d’avril 2024 {#apr-2024}

**Date de publication** : 2 mai 2024

### Nouvelles fonctionnalités {#apr-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous.

<table>
<thead>
<tr>
<th><strong>MMS (service de messagerie multimédia) - tous les fournisseurs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Avec le canal SMS, vous pouvez maintenant améliorer votre communication en envoyant des MMS, ce qui vous permet de partager des images, des GIF ou des vidéos avec vos clientes et clients. Initialement disponibles uniquement avec Sinch, les MMS sont désormais également pris en charge par Infobip et Twilio.</p>
<img src="assets/do-not-localize/mms.gif"/>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Amélioration du concepteur de parcours et des rapports dynamiques</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dans cette version, nous avons amélioré l’interface d’utilisation de la zone de travail de parcours afin d’offrir une expérience client plus intuitive et efficace. Les activités sont plus claires et présentent plus d’informations sur la zone de travail de parcours avec moins de clics.</p>
<img src="assets/new-canvas3.gif"/>
<p>Outre la conception améliorée de la zone de travail de parcours, vous pouvez désormais afficher les mesures de création de rapports pour les dernières 24 heures directement dans la zone de travail de parcours. </p>
<img src="assets/new-canvas6bis.png"/>
<p><strong>Note</strong> : ces modifications seront progressivement déployées dans tous les environnements à compter de la version d’avril.</p>
<p>Pour plus d’informations, consultez la <a href="new-canvas.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<!-- table>
<thead>
<tr>
<th><strong>AI Assistant - Experience Variant Generation - Beta</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Once you have created and personalized your message, take your content to the next level with AI Assistant. You can now use AI Assistant to optimize your message's impact by experimenting with different main titles, and images. Each variant is managed as a unique Treatment, to measure and compare which title effectively generates more clicks.</p>
</td>
</tr>
</tbody>
</table-->


<!--table>
<thead>
<tr>
<th><strong>Email Surface Personalization - Private beta </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now define dynamic subdomains and personalized header parameters when creating email channel configurations, for increased flexibility and control over your email settings.</p>
</td>
</tr>
</tbody>
</table-->

### Améliorations {#apr-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

<!--
* **Expression Fragments supported for Web and In-App**: Expression fragments are now available for the Web and In-app channels. 
-->


<!--
* **DULE for AJO channel configuration**: It is now possible to apply a label on certain profile attributes to restrict their usage inside a channel configuration through marketing actions.
-->


<!--
* **List-Unsubscribe updates**: Following on the recent Gmail and Yahoo announcements for bulk senders, Journey Optimizer supports the "post/1-click" List-Unsubscribe option. 
-->

**Configuration**

* Vous pouvez désormais sélectionner une action marketing au niveau de la configuration des canaux. Lorsqu’elles sont utilisées dans la configuration, toutes les politiques de consentement associées à cette action marketing sont utilisées afin de respecter les préférences de vos clientes et clients. [En savoir plus](../action/consent.md#surface-marketing-actions)
* L’utilisation du contrôle d’accès au niveau de l’objet est désormais disponible pour les configurations de canal. [En savoir plus](../configuration/channel-surfaces.md#create-channel-surface)
* Lors de l’activation du désabonnement de la liste dans une configuration des canaux, vous pouvez maintenant définir le niveau de consentement pour vous aligner sur la manière dont vous gérez le consentement de toutes les autres sources. [En savoir plus](../email/email-settings.md#list-unsubscribe)

**Gestion de contenu**

* Vous pouvez désormais simuler des modèles de contenu pour tous les canaux. [En savoir plus](../content-management/content-templates.md#video-templates).

**Personnalisation**

* La nouvelle fonction d’assistant **toInt** est disponible dans l’éditeur d’expression. Elle vous permet de convertir n’importe lequel de ces types (nombre, double, entier, long, flottant, court, octet, booléen, chaîne) en entier. [En savoir plus](../personalization/functions/math.md#to-int)



## Version de mars 2024 {#mar-2024}

**Date de publication** : 19-20 mars 2024

### Nouvelle fonctionnalité {#mar-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Expériences basées sur le code</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce au nouveau canal d’expérience basé sur le code, Adobe Journey Optimizer vous permet d’effectuer des tests et des personnalisations avancés pour l’une de vos propriétés entrantes, ce qui vous permet de diffuser facilement des expériences personnalisées sur différents points de contact (touchpoints) tels que des applications web, des applications mobiles, des applications de bureau, des consoles vidéo, des appareils connectés à la télévision, des téléviseurs intelligents, des kiosques, des distributeurs automatiques, des périphériques IoT, etc.</p>
<P>Les fonctionnalités principales sont les suivantes :</p>
<ul><li> Personnalisation universelle : étendez les expériences personnalisées sur tous les points de contact, en assurant un parcours utilisateur cohérent et personnalisé.</li>
<li>Précision granulaire de la modification : modifiez du contenu spécifique à des emplacements spécifiques dans vos applications ou pages web.</li>
<li>Mise en œuvre polyvalente : prise en charge des méthodes de mise en œuvre côté serveur, basées sur les API ou basées sur le SDK pour une intégration transparente à votre environnement de développement.</li></ul></p>
<p>Pour plus d’informations, consultez la <a href="../code-based/get-started-code-based.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/code-based.gif"> 
</tr>
</tbody>
</table>

### Améliorations {#mar-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Modèles de contenu**

* **Miniatures** : un mode de **vue Grille** est désormais disponible pour les modèles de contenu, affichant ainsi les miniatures afin d’améliorer l’accès visuel. Actuellement, seuls les modèles HTML d’e-mail sont pris en charge. [En savoir plus](../content-management/content-templates.md#template-thumbnails)

  >[!AVAILABILITY]
  >
  >Cette fonctionnalité est publiée en disponibilité limitée pour un petit groupe de personnes.

**Parcours**

De nouveaux statuts intermédiaires ont été ajoutés au cycle de vie de création de parcours :

* Statut **Publication** entre le statut **Brouillon** et le statut **Actif**
* Statut **Arrêt en cours** entre le statut **Actif** et le statut **Arrêté**
* Statuts **Activer le mode test** ou **Désactiver le mode test** entre le statut **Brouillon** et le statut **Brouillon (test)**

Lorsqu’un parcours se trouve dans un état intermédiaire, il est en lecture seule. [En savoir plus](../building-journeys/journey-gs.md#filter)

## Version de février 2024 {#feb-2024}

**Date de publication** : 21-22 février 2024

### Nouvelles fonctionnalités{#feb-features}

Cette version apporte les nouvelles fonctionnalités répertoriées ci-dessous.


<table>
<thead>
<tr>
<th><strong>Messagerie in-app web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais utiliser la nouvelle fonctionnalité de messagerie in-app web pour afficher du contenu personnalisé directement sur les sites web, par le biais de messages de superposition modale. Cette fonctionnalité vous permet d’interagir efficacement avec les visiteurs et visiteuses web, ce qui améliore l’interaction, la rétention et les taux de conversion des utilisateurs et utilisatrices.<br/><br/></p>
<p>Pour plus d’informations, consultez la <a href="../in-app/create-in-app-web.md">documentation détaillée</a>.<br></br></p>
<img src="assets/do-not-localize/web_inapp.gif">
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Modèles de contenu multicanaux</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>En plus de la fonctionnalité E-mail, des modèles de contenu sont désormais disponibles pour les canaux suivants : Push, In-app, SMS et Courrier, chaque canal ayant des types de modèles dédiés. Pour E-mail, vous pouvez maintenant sélectionner le type de contenu, ce qui vous permet d’enregistrer l’objet dans le cadre de votre modèle d’e-mail. <br/><br/></p>
<p>Pour plus d’informations, consultez la <a href="../content-management/content-templates.md">documentation détaillée</a>.<br></br></p>
<img src="assets/do-not-localize/multi-chan-templates.gif"> 
</tr>
</tbody>
</table>


### Améliorations {#feb-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Audiences**

* **Listes de contrôle** : les variantes sont désormais prises en charge lors de l’utilisation de **listes de contrôle**. Les adresses de contrôle reçoivent une copie de toutes les variantes du même message (telles que les différents traitements d’une expérience de contenu). [En savoir plus](../configuration/seed-lists.md)

Auparavant disponibles en version Beta, les améliorations suivantes sont désormais disponibles pour l’ensemble des utilisateurs et utilisatrices :

* Vous pouvez désormais cibler les **audiences créées par le biais de la composition d’audiences** et utiliser les attributs d’enrichissement dans les parcours. [En savoir plus](../building-journeys/read-audience.md)

* Vous pouvez désormais cibler les **audiences chargées à partir d’un fichier CSV** dans les parcours et les campagnes. [En savoir plus](../audience/about-audiences.md#about-segments)

  >[!AVAILABILITY]
  >
  >* L’utilisation d’audiences et d’attributs provenant de la composition d’audiences et du chargement personnalisé (fichier CSV) n’est actuellement pas disponible avec Healthcare Shield ou Privacy and Security Shield.
  >* L’amélioration du **chargement de l’audience à partir d’un fichier CSV** sera progressivement déployée dans les jours qui suivront la version initiale. Certains utilisateurs et utilisatrices ont un accès immédiat, mais d’autres peuvent rencontrer un retard avant que cela ne soit disponible dans leur environnement.

**Parcours**

* **Filtrer vos parcours** : vous pouvez désormais utiliser les **dates personnalisées pour filtrer l’inventaire des parcours**, en plus des filtres de dates prédéfinis existants. Vous pouvez ainsi affiner la liste en affichant les parcours créés ou publiés à une date spécifique, au cours d’un mois donné, sur une année entière ou dans des périodes spécifiées. [En savoir plus](../building-journeys/journey-gs.md#filter)
* **Actions personnalisées** : vous pouvez maintenant mettre à jour l’en-tête **content-type**. Ce nouveau **content-type** doit référencer le contenu JSON. [En savoir plus](../action/about-custom-action-configuration.md#url-configuration)
* **Configuration** : l’attribut identityMap dans stepEvents est maintenant prérenseigné. L’identité principale est définie comme « primary = true ». [En savoir plus](../reports/sharing-field-list.md)
* **Interface utilisateur** : la barre supérieure, dans les écrans de parcours, a été réorganisée pour une expérience améliorée. Parmi les différentes mises à jour, l’icône « crayon » permettant d’accéder aux propriétés du parcours s’affiche désormais à gauche de la barre supérieure, en regard du nom du parcours. [En savoir plus](../building-journeys/journey-properties.md)

**Canal SMS**

* **Mots-clés opt-in/opt-out** : lors de la configuration de votre canal SMS, vous pouvez désormais personnaliser les **mots-clés opt-in et opt-out** selon vos préférences. Journey Optimizer déclenche la réponse en fonction de ces mots-clés spécifiés. [En savoir plus](../sms/sms-configuration.md)

**Campagnes**

* **Campagnes déclenchées par l’API** : le code cURL généré après l’activation d’une campagne déclenchée par une API a été amélioré. Il inclut désormais toutes les variables de personnalisation (profil et contexte) utilisées dans le message. [En savoir plus](../campaigns/api-triggered-campaigns.md#execute)

**Règles de fréquence**

* En plus des canaux E-mail et Push, vous pouvez maintenant créer des règles de fréquence pour les canaux SMS et Courrier. Les règles de fréquence excluent automatiquement les profils sur-sollicités des messages et actions lorsque la limite de fréquence est atteinte. [En savoir plus](../conflict-prioritization/rule-sets.md)

<!--**Decision management**

* **Capping rules** - You can now add **multiple capping rules** for one offer. This allows you to increase the level of control over the way offers are sent.-->


## Version de janvier 2024 {#jan-2024}

**Date de publication** : 30-31 janvier 2024

### Nouvelles fonctionnalités{#jan24-features}

Cette version apporte les nouvelles fonctionnalités répertoriées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Mises à jour de délivrabilité</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer prend désormais en charge la technologie d’authentification DMARC.</p>
<p>À compter du 1er février 2024, Google et Yahoo! exigent que vous disposiez d’un enregistrement DMARC pour tout domaine utilisé pour leur envoyer des e-mails. Vérifiez que l’enregistrement DMARC est configuré pour tous les sous-domaines que vous avez déjà délégués ou que vous déléguez actuellement à Adobe dans Journey Optimizer.</p>
<p>Pour plus d’informations, consultez la <a href="../configuration/dmarc-record-update.md">documentation détaillée</a>.</p>
<br/><img src="assets/do-not-localize/dmarc.gif"/>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Playbooks de cas d’utilisation</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Tirez profit d’un catalogue de playbooks de cas d’utilisation spécifiques à des secteurs d’activité dans Real-Time CDP et Journey Optimizer pour traiter les cas d’utilisation courants que vous pouvez exécuter à l’aide d’Adobe Experience Platform et d’Adobe Journey Optimizer.</p><p>Une fois que vous avez choisi le playbook qui correspond le mieux à vos besoins, vous pouvez lui permettre de générer les ressources nécessaires à la prise en charge de votre cas d’utilisation, telles que des parcours, des messages, des schémas ou des segments, et de les personnaliser dans votre schéma pour réduire le délai de rentabilisation.</p>
<p>Pour plus d’informations, consultez la <a href="../start/ai-features.md#playbooks">documentation détaillée</a>.</p>
<br/><img src="assets/do-not-localize/playbooks.gif"/>
</tr>
</tbody>
</table>

### Améliorations {#jan24-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Création de rapports**

* **Nouveaux widgets de répartition basés sur des domaines** – Ajout de nouveaux widgets pour améliorer vos rapports Campaign et Journey. Les widgets **Raisons de rebond par domaine**, **Envoyés et diffusés par domaine**, **Ouvertures et clics par domaine** et **Rebonds et erreurs par domaine** fournissent une répartition détaillée des mesures principales de diffusion et de suivi des e-mails au niveau du domaine. [En savoir plus](../reports/channel-report-cja.md)

**Canal SMS**

* **Double opt-in** – Le workflow Double opt-in pour les SMS garantit que les utilisateurs et les utilisatrices s’engagent explicitement à recevoir des messages lorsque la demande est envoyée à partir de leur appareil. Les utilisateurs et utilisatrices démarrent le processus de consentement en envoyant un SMS entrant. Une fois qu’ils ont confirmé leur consentement, un message de réponse est envoyé, demandant une vérification finale. Si un profil d’utilisateur ou d’utilisatrice n’existe pas, il est créé lors de la confirmation. [En savoir plus](../sms/sms-configuration.md)

  Notez que cette fonctionnalité est disponible avec les fournisseurs SMS Sinch et Infobip.

**Parcours**

* **Durée des événements de réaction** – La durée maximale que vous pouvez définir dans les **Événements de réaction** est désormais de 29 jours au lieu de 30. [En savoir plus](../building-journeys/reaction-events.md)

<!--* **Date filters** - You can now use custom dates to filter the journeys inventory, in addition to the existing predefined date filters. This allows you to refine the list by displaying journeys published on a specific date, within a particular month, throughout an entire year, or within specified time ranges. [Learn more](../building-journeys/journey-gs.md#filter)-->

* **Lecture d’audience** – L’activité **Lecture d’audience** repose désormais sur le jeu de données d’instantané de profil pour les segments par lots, qui n’est généré qu’une fois par jour après l’exécution du traitement par lots quotidien planifié. Par conséquent, les données sont à jour depuis le dernier traitement par lots quotidien. [En savoir plus](../building-journeys/read-audience.md)

* **Groupes de champs** – Cette version corrige un problème qui empêchait l’enregistrement de groupes de champs dans certains cas.

* La prise en charge de `<listObject>` a été modifiée dans plusieurs fonctions.

**Règles de fréquence**

* **Limite de fréquence hebdomadaire** – Vous pouvez désormais spécifier le nombre maximum de messages envoyés à un profil client par semaine, en plus de l’option par mois. La limite de fréquence est basée sur la période calendaire sélectionnée et est réinitialisée au début de la période correspondante. [En savoir plus](../conflict-prioritization/rule-sets.md)

  >[!NOTE]
  >
  >Une limite de fréquence quotidienne est également disponible à la demande. Contactez votre représentant ou représentante Adobe.

**Gestion des décisions**

* **Capping de la fréquence sur Edge** – Le compteur de capping de fréquence est maintenant mis à jour et disponible dans une décision de l’API Edge Decisioning en moins de 3 secondes. [En savoir plus](../offers/api-reference/offer-delivery-api/start-offer-delivery-apis.md)
