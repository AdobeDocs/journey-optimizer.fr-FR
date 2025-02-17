---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
topic: Content Management
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ce2c5e26ae4d17898f50f890c146ccfafc93a7c2
workflow-type: tm+mt
source-wordcount: '2760'
ht-degree: 79%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations des fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour. [!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Version du 25 février {#25-02-rn}

**Date de publication** : 18 et 19 février 2025


### Nouvelles fonctionnalités {#25-02-features}

Les nouvelles fonctionnalités de cette version sont présentées ci-dessous.

<table>
<thead>
<tr>
<th><strong>Créer et gérer des règles métier</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer des règles métier à l’aide d’ensembles de règles. Les ensembles de règles sont des groupes de règles qui vous permettent de limiter les messages envoyés dans les campagnes et les actions de parcours sur plusieurs canaux, ainsi que de contrôler les entrées de profils dans les parcours.<p>
<p><ul><li>Créez des ensembles de règles de canal pour limiter le nombre de messages envoyés sur un ou plusieurs canaux. Appliquez-les à des campagnes ou à des actions de parcours pour appliquer les règles définies dans l’ensemble de règles. L’ensemble de règles de canal vous permet d’appliquer des règles de limitation en fonction des types de communication. Par exemple, définissez un ensemble de règles pour limiter les « messages promotionnels » et un autre pour les « newsletters ». Appliquez le jeu de règles approprié dans votre campagne ou action de parcours en fonction du type de communication que vous envoyez.</li>
<li> Créez des ensembles de règles de parcours pour contrôler les entrées de profil dans les parcours. Limiter la fréquence à laquelle un profil peut rejoindre un parcours au cours d’une période donnée ou le nombre de parcours auxquels un profil peut être inscrit simultanément. Appliquez-les au niveau du parcours pour assurer une bonne gestion des entrées.</li></p>
<p>Auparavant disponibles pour un ensemble d’organisations (LA), les règles métier sont désormais disponibles pour tous les utilisateurs (GA).</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Générer des pages de destination avec l’assistant AI</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce à l’assistant d’IA, vous pouvez désormais concevoir du contenu attrayant pour vos pages de destination, notamment des conceptions de pages complètes, du texte personnalisé et des visuels personnalisés.</p>
<img src="assets/do-not-localize/ai-lp.gif">
<!--p>For more information on AI Assistant, refer to the <a href="../email/generative-lp.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Directives relatives aux marques (version bêta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez maintenant définir vos propres directives relatives à la marque pour définir l’identité visuelle et verbale de votre marque. Notez que la fonctionnalité Marques est disponible en version bêta privée pour un nombre limité de clientes et clients. Elle sera progressivement disponible pour tous les clients dans les prochaines versions.</p>
<!--p>For more information, refer to the <a href="../content-management/brands.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Modèles Customer Journey Analytics</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous avez désormais la possibilité d’améliorer vos rapports Journey Optimizer à l’aide de modèles Customer Journey Analytics. Cette nouvelle fonctionnalité vous permet de rationaliser votre processus de création de rapports à l’aide de modèles préconçus et adaptés à vos besoins en matière d’analyse.
</p>
<img src="assets/do-not-localize/cja-templates.gif">
<p>Pour plus d’informations, consultez la <a href="../reports/report-cja-manage.md#cja-template">documentation détaillée</a>.</p>
<p>Date de disponibilité : à partir du 15 janvier 2025</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Évaluation D’Audience Flexible (Disponibilité Limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’évaluation d’audience flexible vous permet d’exécuter une tâche de segmentation à la demande pour des audiences sélectionnées, en vous assurant de toujours disposer des données d’audience les plus récentes avant de les cibler dans des parcours et des campagnes Journey Optimizer.</p>
<img src="assets/do-not-localize/flexible-audience.gif">
<p>Pour plus d’informations, consultez la <a href="../audience/about-audiences.md#flexible">documentation détaillée</a>.</p>
<p> L’évaluation flexible des audiences n’est disponible que pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.</p>
<p>Date de disponibilité : 28 janvier 2025</p>
</tr>
</tbody>
</table>
</table>


### Améliorations {#25-02-improvements}

Les améliorations ci-dessous accompagnent la mise à jour de février.

* **Parcours** - Vous pouvez désormais tester vos actions personnalisées en envoyant des appels d’API à partir de la section administration. Cette nouvelle fonctionnalité vous permet de résoudre les problèmes liés à vos actions personnalisées avant ou après leur utilisation dans un parcours.

* **Durée de vie (TTL) du jeu de données** - À compter de ce mois-ci, un mécanisme de sécurisation de durée de vie (TTL) sera déployé vers les jeux de données générés par le système Journey Optimizer dans de nouveaux sandbox et de nouvelles organisations, comme suit :

   * 90 jours pour les données dans la banque de profils
   * 13 mois pour les données du lac de données

  Cette modification sera déployée dans les sandbox clients existants au cours d’une phase ultérieure.

  En savoir plus sur cette mise à jour dans [la FAQ dédiée](../data/datasets-ttl.md#frequently-asked-questions).

<!--* **Playbooks** - You can now create and publish your own Use Case Playbooks in Journey Optimizer.-->

* **Publipostage direct** - Un nouveau type de serveur, la zone d’entrée des données, est désormais pris en charge pour le routage des fichiers dans la configuration du canal de publipostage direct.

* **SMS** - Vous pouvez désormais gérer la diffusion de messages SMS à partir de points d’entrée multi-régionaux en remplaçant les URL de diffusion, de retour, d’entrée et de rappel. Pour ce faire, une nouvelle URL de remplacement de champ a été ajoutée à la configuration des informations d’identification d’API. Cette modification est disponible uniquement auprès du fournisseur Sinch. [En savoir plus](../sms/sms-configuration-sinch.md)

* **Personalization** (Date de disponibilité : 29 janvier 2025) - De nouvelles fonctions d’assistance date/heure sont disponibles dans l’éditeur de personnalisation. [En savoir plus](../personalization/functions/dates.md)


<!--
* The personalization editor has been enhanced with new capabilities such as Auto-complete, Search, and filtering options. You can also show or hide deprecated attributes.-->


* **Configuration des e-mails** (Date de disponibilité : 12 février 2025) - Si vous gérez le consentement en dehors d’Adobe, vous pouvez désormais définir une adresse e-mail de désabonnement personnalisée et une URL de désabonnement en un clic personnalisée dans le cadre des paramètres de configuration de votre canal e-mail. [En savoir plus](../email/list-unsubscribe.md#custom-managed)

  ![](../email/assets/surface-list-unsubscribe-custom.png){width="80%"}

* **Prise de décision** (date de disponibilité : 28 janvier 2025) - La prise de décision prend désormais en charge les types de données d’objet lors de la modification du schéma du catalogue d’articles. [En savoir plus](../experience-decisioning/catalogs.md)


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
<th><strong>Tester votre contenu à l’aide d’exemples de données d’entrée (version bêta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Désormais, Journey Optimizer vous permet de tester différentes variantes de votre contenu en le prévisualisant et en envoyant des BAT par e-mail à l’aide d’exemples de données d’entrée chargées à partir d’un fichier ou ajoutées manuellement. Tous les attributs de profil utilisés dans votre contenu pour la personnalisation sont automatiquement détectés par le système et peuvent être utilisés pour vos tests afin de créer plusieurs variantes.</p>
<p>Cette fonctionnalité est actuellement disponible pour tous les clientes et clients en version bêta publique, pour les canaux E-mail, SMS et Notification Push.</p>
<p>Pour plus d’informations, consultez la <a href="../test-approve/simulate-sample-input.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/gif-simulate.gif">
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Utiliser les données Adobe Experience Platform pour la personnalisation (version bêta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Exploitez les données d’Adobe Experience Platform dans l’éditeur de personnalisation pour personnaliser votre contenu. Pour ce faire, les jeux de données nécessaires à la personnalisation de la recherche doivent d’abord être activés par le biais d’un appel API. Une fois que vous avez terminé, vous pouvez utiliser leurs données pour personnaliser votre contenu dans [!DNL Journey Optimizer].</p>
<p>Cette fonctionnalité est actuellement disponible en version bêta publique pour l’ensemble des clientes et clients.</p>
<p>Pour plus d’informations, consultez la <a href="../personalization/lookup-aep-data.md">documentation détaillée</a>.</p>
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

  Cette modification sera déployée sur les sandbox des clientes et clients existants au cours d’une phase ultérieure. [En savoir plus](../data/datasets-ttl.md#ttl)

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

* Les utilisateurs et utilisatrices d’[Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=fr) peuvent désormais choisir des modèles personnalisés à optimiser lors de la configuration d’un modèle IA dans la prise de décision (anciennement appelée Décisions pour les expériences). Cela vous permet, par exemple, d’optimiser un tableau personnalisé « achats » plutôt que des contraintes définies telles que le taux de clics. [En savoir plus](../experience-decisioning/ranking.md)

* Lors de l’ajout d’une politique de décision à une campagne basée sur du code avec la prise de décision, vous pouvez désormais sélectionner manuellement des éléments de décision uniques, en plus des stratégies de sélection. En outre, vous pouvez désormais sélectionner plusieurs offres de secours. Cela garantit qu’un certain nombre d’éléments de décision sont renvoyés. [En savoir plus](../experience-decisioning/create-decision.md)
