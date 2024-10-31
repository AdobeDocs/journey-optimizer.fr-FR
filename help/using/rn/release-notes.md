---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
topic: Content Management
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: a7fdde15f7c491fd9a3b1fef898f018ba9954cde
workflow-type: tm+mt
source-wordcount: '1812'
ht-degree: 43%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour. [!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Version du 24 octobre {#24-10-rn}

**Date de publication** : 29-30 octobre 2024

### Nouvelles fonctionnalités {#24-10-features}

Les nouvelles fonctionnalités présentées dans cette version sont les suivantes :

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
<p>Disponible depuis le 24 octobre 2024</p>
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
<p>Disponible depuis le 1er octobre 2024</p>
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
<p>Disponible depuis le 1er octobre 2024</p>
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
<p>Dans Journey Optimizer, la gestion du volume et du calendrier des campagnes et des parcours est essentielle pour éviter de submerger les clientes et clients avec un trop grand nombre d’interactions. Journey Optimizer propose désormais plusieurs outils de gestion des conflits et de hiérarchisation des priorités. <p>Pour plus d’informations, consultez la <a href="../email/surface-personalization.md">documentation détaillée</a>.</p></p><p><ul><li><b>Limitation de la fréquence des Parcours</b> : vous pouvez désormais créer des ensembles de règles à appliquer à vos parcours, ce qui vous permet de limiter le nombre de parcours d’un profil par jour, semaine ou mois, ainsi que de contrôler le nombre de parcours simultanés exécutés simultanément.</li>
<li><b>Score de priorité</b> : vous pouvez désormais attribuer un score de priorité à une campagne ou à un parcours, allant de 0 à 100. Les nombres plus élevés signalent une priorité plus élevée. Lorsque deux campagnes ou actions de parcours utilisent la même configuration de canal, Journey Optimizer sélectionne celle avec le score de priorité le plus élevé. Si les campagnes ont le même score, la campagne qui a été la moins récemment modifiée sera choisie.</li>
<li><b>Afficher les conflits potentiels</b> : un nouveau bouton "Afficher les conflits potentiels" dans les parcours et les campagnes vous permet désormais d’identifier le chevauchement avec d’autres parcours ou campagnes tels que la date de début, l’audience ciblée ou la configuration de canal sélectionnée.</li>
<li><b>Arbitrage du Parcours</b> : cette nouvelle fonctionnalité vous permet de prioriser les parcours les plus importants pour vos clients. Vous pouvez créer une règle pour supprimer une entrée dans un parcours de priorité inférieure lorsqu’un client est admissible pour un parcours de priorité supérieure à venir.</li>
<li><b>Limitation de la fréquence par type de communication : </b>Avec les jeux de règles, vous pouvez désormais définir des règles granulaires par type de communication (par exemple, Ventes, Promotionnel) pour éviter de surcharger les clients avec des messages similaires. Vous pouvez contrôler la fréquence sur plusieurs canaux, en excluant automatiquement les profils sur-sollicités afin d’offrir une meilleure expérience client.</li></ul>

<p>Les fonctionnalités de gestion des conflits et des priorités sont disponibles dans Disponibilité limitée pour un groupe sélectionné de clients. Veuillez noter que ces fonctionnalités seront progressivement déployées vers d’autres utilisateurs à l’avenir. Contactez l’équipe de votre compte si vous souhaitez être ajouté à la liste d’attente pour ces fonctionnalités.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Intégration d’encre mobile et de Adobe Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais intégrer Mofiable Ink Da Vinci et Adobe Journey Optimizer. Avec cette nouvelle intégration, vous pouvez : </p>
<p><ul><li>Tirez parti des puissantes fonctionnalités du produit Da Vinci de Mofiable Ink pour assembler et personnaliser les variations d’email pour les campagnes par lots</li>
<li>Accélérer les workflows des praticiens pour les clients Journey Optimizer à l’aide de Da Vinci pour la création et de Adobe Journey Optimizer pour l’optimisation et la diffusion</li>
<li>Optimisez les modèles Da Vinci avec les données d’Adobe.</li></ul></p>
<p>Pour plus d'informations, consultez la <a href="https://movableink.com/adobe-and-movable-ink">documentation sur l'encre mobile de Vinci</a>.</p>
</tr>
</tbody>
</table>

Antérieurement disponibles pour un ensemble d’organisations (LA), les fonctionnalités suivantes sont désormais disponibles pour tous les utilisateurs (GA) :

<table>
<thead>
<tr>
<th><strong>Personnalisation de la configuration des emails (Disponibilité générale) </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Pour une flexibilité et un contrôle accrus de vos paramètres d’email, vous pouvez définir des sous-domaines dynamiques et des paramètres d’en-tête personnalisés lors de la création de configurations de canal email.
</p>
<p>Pour plus d’informations, consultez la <a href="../email/surface-personalization.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/surface-perso.gif"/>
<p>Disponible depuis le 23 octobre 2024</p>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Validations dans les parcours et les opérations (Disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce aux politiques d’approbation, vous pouvez désormais configurer un processus d’approbation dans Journey Optimizer qui permet aux équipes marketing de s’assurer que les campagnes et les parcours sont examinés et approuvés par les parties prenantes appropriées avant qu’ils ne soient mis en ligne.</p>
<p>Pour plus d’informations, consultez la <a href="../test-approve/gs-approval.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/approval.gif"/>
<p>Disponible depuis le 22 octobre 2024</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Expérience de contenu en parcours (disponibilité générale)</strong><br/></th>
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


<!--<table>
<thead>
<tr>
<th><strong>Decisioning (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Decisioning, previously available for a set of organizations (LA) and known as Experience Decisioning, is now available to all users (GA), including organizations that have purchased the Adobe Healthcare Shield or Privacy and Security Shield add-on offerings.</p><p>Decisioning simplifies personalization by offering a centralized catalog of marketing offers known as 'decision items' and a sophisticated decision engine. This engine leverages rules and ranking criteria to select and present the most relevant decision items to each individual. These decision items are seamlessly integrated into a wide range of inbound surfaces through the code-based experience channel.</p>
<p>For more information, refer to the <a href="../experience-decisioning/gs-experience-decisioning.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Messages multilingues dans les parcours et les campagnes (Disponibilité générale)</strong><br/></th>
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
<p>Les rapports Journey Optimizer sont désormais disponibles dans l’ensemble (GA). Ils s’accompagnent d’une interopérabilité améliorée avec les fonctionnalités des Customer Journey Analytics, de la normalisation des rapports sur les deux plateformes et de l’amélioration de la cohérence et de la fiabilité des données. L’intégration transparente entre Journey Optimizer et Customer Journey Analytics fournit une meilleure visibilité des mesures de performance, ce qui aide les utilisateurs et les utilisatrices à prendre des décisions plus éclairées.</p>
<p>Avec la disponibilité générale, quatre nouvelles fonctionnalités sont introduites : la possibilité de créer des mesures simples, de créer et de publier des audiences, de poser des questions ad hoc à l’aide d’Insight Builder et de planifier des rapports qui seront automatiquement envoyés par courriel aux destinataires clés.</p>
<p>Pour plus d’informations, consultez la <a href="../reports/report-cja-manage.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Important : L’expérience de création de rapports actuelle sera abandonnée à compter de janvier 2025. À partir de cette date, la nouvelle expérience de création de rapports deviendra la norme. Nous vous recommandons de vous familiariser avec les nouvelles fonctionnalités pour garantir une transition fluide. <a href="../reports/report-gs-cja.md">Découvrir la nouvelle interface de création de rapports de Journey Optimizer</a></p>
<p>Disponible depuis le 16 octobre 2024</p>
</tr>
</tbody>
</table>


<!--The following capabilities are available to all customers in public beta:

<table>
<thead>
<tr>
<th><strong>Test your content using sample input data (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey optimizer now allows you to test different variants of your email content by previewing it and sending proofs using sample input data uploaded from a file or added manually. All the profiles attributes used in your content for personalization are automatically detected by the system and can be used for your tests to create multiple variants.</p>
<p>This capability is currently available to all customers as a public beta.</p>
<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<!--<table>
<thead>
<tr>
<th><strong>Use Adobe Experience Platform data for personalization (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Leverage data from Adobe Experience Platform in the personalization editor to personalize your content. To do this, datasets needed for lookup personalization must first be enabled through an API call. Once done, you can use their data to personalize your content into [!DNL Journey Optimizer].</p>
<p>This capability is currently available to all customers as a public beta.</p>
<p>For more information, refer to the <a href="../personalization/lookup-aep-data.md"</a>.</p>
</td>
</tr>
</tbody>
</table>-->

### Améliorations {#24-10-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Canal SMS**

Des améliorations ont été apportées aux SMS pour améliorer vos fonctionnalités de messagerie :

* Vous pouvez définir et gérer des mots-clés uniques pour vos campagnes et parcours SMS, ce qui permet une communication plus personnalisée et efficace.

* Vous pouvez créer et diffuser un SMS par défaut lorsqu&#39;un mot-clé n&#39;est pas reconnu.

* Vous pouvez désormais modifier ou supprimer une configuration de canal de l’API SMS.

Pour en savoir plus sur ces améliorations, consultez la documentation de configuration des SMS pour [Infobip](../sms/sms-configuration-infobip.md) et [Sinch](../sms/sms-configuration-sinch.md).

<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

&lt;!—* **Nombre maximal de parcours en direct** - Journey Optimizer dispose désormais d’une barrière de sécurité de 500 parcours en direct sur les environnements de test de production, au lieu de 100. Le nombre de parcours actifs est visible dans la zone de travail du parcours. <!-- DOCAC-10977-->

**Canal web**

* **Mode de modification non visuel pour le concepteur web** - En tant qu’alternative au concepteur web de Journey Optimizer, vous pouvez désormais ajouter des modifications à votre site web à l’aide d’un éditeur non visuel. Il vous permet de saisir vos modifications manuellement sans ouvrir les pages dans l’éditeur visuel. Ce mode de modification non visuel est utile si vous ne pouvez pas installer d’extensions de navigateur telles que l’assistant visuel Adobe Experience Cloud, nécessaire pour charger vos pages dans le concepteur web. [En savoir plus](../web/web-non-visual-editor.md)


**Jeux de données**

* **Envoyer et ouvrir des événements** - À compter du 1er novembre 2024, la segmentation par flux ne prendra plus en charge l’utilisation des événements d’envoi et d’ouverture à partir des jeux de données de suivi et de retour Journey Optimizer. Cette modification s’applique à tous les environnements de test et organisations de clients. [En savoir plus](../data/datasets-ttl.md#segmentation-update)

* **Durée de vie du jeu de données (TTL)** - À compter de février 2025, une barrière de sécurité de durée de vie (TTL) sera déployée sur les jeux de données générés par le système Journey Optimizer dans les nouveaux environnements de test et les nouvelles organisations comme suit :

   * 90 jours pour les données dans la banque de profils
   * 13 mois pour les données du lac de données

  Cette modification sera déployée sur les environnements de test client existants au cours d’une phase ultérieure. [En savoir plus](../data/datasets-ttl.md#ttl)

* **Paramètres dans les actions personnalisées** (Date de disponibilité : 3 octobre 2024) - Les paramètres NULL et facultatifs sont désormais pris en charge dans les actions personnalisées. [En savoir plus](../action/about-custom-action-configuration.md#define-the-message-parameters).

**Créer des rapports**

* **Le rapport de prise de décision d’expérience** est désormais disponible et offre des informations essentielles sur la manière dont vos visiteurs interagissent avec vos expériences. [En savoir plus](../reports/campaign-global-report-cja-code.md##decisioning-kpis)

**Gouvernance des données et politiques de consentement** : date de disponibilité : 7 octobre 2024

* L’application des **politiques de gouvernance des données** a désormais lieu sur tous les canaux dans Journey Optimizer. Pour les clients qui ont créé des stratégies dans Adobe Experience Platform, elles sont appliquées aux actions marketing dans le cadre de la configuration des canaux. Lorsque vous créez du contenu à l’aide d’une configuration, le système vérifie tous les champs de personnalisation à la recherche de toute violation de gouvernance des données. Si une violation est trouvée, la publication d’un parcours ou d’une campagne n’est pas possible. [En savoir plus](../action/action-privacy.md)

* Les **politiques de consentement personnalisé** s’appliquent désormais à tous les canaux Journey Optimizer. Lors de l’application, avant l’envoi d’un message ou avant la diffusion d’une expérience entrante, le système vérifie que la personne a donné son consentement pour utiliser des champs de personnalisation dans le contenu qu’elle reçoit. Si aucun consentement n’est donné, l’expérience ne s’affiche pas. [En savoir plus](../action/consent.md)

  >[!NOTE]
  >
  >Les politiques de consentement ne sont actuellement disponibles que pour les organisations qui ont acheté les offres complémentaires Adobe **Healthcare Shield** et **Privacy and Security Shield**.

**Audiences** : date de disponibilité : 8 octobre 2024

* Lors du ciblage d’une audience de fichier CSV, vous pouvez désormais utiliser les attributs du fichier dans l’éditeur de personnalisation et dans le créateur de règles de parcours et de campagnes. [En savoir plus](../audience/about-audiences.md)

* L’utilisation des audiences et des attributs du chargement personnalisé (fichiers CSV) est désormais disponible avec Healthcare Shield ou Privacy and Security Shield.

**Configuration** - Date de disponibilité : 23 octobre 2024

* Lors de l&#39;utilisation d&#39;une configuration personnalisée dans une opération ou un parcours, vous pouvez désormais prévisualiser le contenu de votre email afin de rechercher les erreurs potentielles avec les paramètres dynamiques que vous avez définis. [En savoir plus](../email/surface-personalization.md#check-configuration)

**Canal basé sur le code**

* Des modèles de contenu sont désormais disponibles. Vous pouvez accélérer la création de vos expériences basées sur du code à partir d’un modèle de contenu créé par vos développeurs. L’utilisation d’un modèle de contenu permet au marketeur de modifier uniquement certaines valeurs ou certains champs, au lieu de composer l’ensemble de l’HTML ou de la payload du contenu JSON. [En savoir plus](../content-management/content-templates.md)

**Prise de décision**

<!--* [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html) users can now choose custom models to optimize on when setting up an AI model in Decisioning (formerly known as Experience Decisioning). This allows you, for example, to optimize on a custom "purchases" table rather than defined constraints such as clickthrough rate."-->

* Lors de l’ajout d’une stratégie de décision à une campagne basée sur du code avec Experience Decisioning, vous pouvez désormais sélectionner manuellement des éléments de décision uniques, en plus des stratégies de sélection. En outre, vous pouvez désormais sélectionner plusieurs offres de secours. Cela garantit qu’un certain nombre d’éléments de décision sont renvoyés. [En savoir plus](../experience-decisioning/create-decision.md)
