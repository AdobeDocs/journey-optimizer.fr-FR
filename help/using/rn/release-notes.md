---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
topic: Content Management
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: acc3d61b571f577187503157b78de1d27ce5e1ee
workflow-type: tm+mt
source-wordcount: '3066'
ht-degree: 57%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour. [!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

## Notes de mise à jour initiales du 24 octobre {#24-10-rn}

>[!CAUTION]
>
>**Les notes de mise à jour anticipées ci-dessous peuvent être modifiées sans préavis jusqu’à la date de publication**. Les liens, les copies d’écran et la documentation mise à jour sont publiés à la date de publication.

**Date de publication** : 29-30 octobre 2024

### Nouvelles fonctionnalités {#24-10-features}

Cette version apporte les nouvelles fonctionnalités détaillées ci-dessous.

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
<!--p>For more information, refer to the <a href="../content-management/gs-generative.md">detailed documentation</a>.</p>-->
<img src="assets/do-not-localize/ai-content.gif">
</td>
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
<p>Auparavant disponibles pour un ensemble d’organisations (LA), les stratégies d’approbation sont désormais disponibles pour tous les utilisateurs (GA).</p>
<p>Pour plus d’informations, consultez la <a href="../test-approve/gs-approval.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/approval.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Personnalisation de la configuration des emails (Disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais définir des sous-domaines dynamiques et des paramètres d’en-tête personnalisés lors de la création de configuration de canal e-mail pour une meilleure flexibilité et un meilleur contrôle de vos paramètres d’e-mail.</p><p>L'utilisation d'une configuration personnalisée dans une opération ou un parcours vous permet de prévisualiser le contenu de votre email afin de rechercher les erreurs potentielles avec les paramètres dynamiques que vous avez définis.</p>
<p>Anciennement disponible pour un ensemble d’organisations (LA), la personnalisation de la configuration des emails est désormais disponible pour tous les utilisateurs (GA).</p>
<p>Pour plus d’informations, consultez la <a href="../email/surface-personalization.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Testez votre contenu à l’aide d’exemples de données d’entrée (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’outil d’optimisation des parcours vous permet désormais de tester différentes variantes du contenu de votre email en le prévisualisant et en envoyant des bons à tirer à l’aide d’exemples de données d’entrée téléchargées à partir d’un fichier CSV ou ajoutées manuellement. Tous les attributs de profil utilisés dans votre contenu pour la personnalisation sont automatiquement détectés par le système et peuvent être utilisés pour vos tests afin de créer plusieurs variantes.</p>
<p>Cette fonctionnalité est actuellement disponible en version bêta.</p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
</td>
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
<p>Dans Journey Optimizer, la gestion du volume et du calendrier des campagnes et des parcours est essentielle pour éviter de submerger les clientes et clients avec un trop grand nombre d’interactions. Journey Optimizer propose désormais plusieurs outils de gestion des conflits et de hiérarchisation des priorités.</p><p><ul><li><b>Limitation de la fréquence des Parcours</b> : vous pouvez désormais créer des ensembles de règles à appliquer à vos parcours, ce qui vous permet de limiter le nombre de parcours d’un profil par jour, semaine ou mois, ainsi que de contrôler le nombre de parcours simultanés exécutés simultanément.</li>
<li><b>Score de priorité</b> : vous pouvez désormais attribuer un score de priorité à une campagne ou à un parcours, allant de 0 à 100. Les nombres plus élevés signalent une priorité plus élevée. Lorsque deux campagnes ou actions de parcours utilisent la même configuration de canal, Journey Optimizer sélectionne celle avec le score de priorité le plus élevé. Si les campagnes ont le même score, la campagne qui a été la moins récemment modifiée sera choisie.</li>
<li><b>Afficher les conflits potentiels</b> : un nouveau bouton "Afficher les conflits potentiels" dans les parcours et les campagnes vous permet désormais d’identifier le chevauchement avec d’autres parcours ou campagnes tels que la date de début, l’audience ciblée ou la configuration de canal sélectionnée.</li>
<li><b>Arbitrage du Parcours</b> : cette nouvelle fonctionnalité vous permet de prioriser les parcours les plus importants pour vos clients. Vous pouvez créer une règle pour supprimer une entrée dans un parcours de priorité inférieure lorsqu’un client est admissible pour un parcours de priorité supérieure à venir.</li></ul></p>
<!--<p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p>-->
<p>Les fonctionnalités de gestion des conflits et des priorités sont disponibles dans Disponibilité limitée pour un groupe sélectionné de clients. Veuillez noter que ces fonctionnalités seront progressivement déployées vers d’autres utilisateurs à l’avenir. Contactez l’équipe de votre compte si vous souhaitez être ajouté à la liste d’attente pour ces fonctionnalités.</p>

</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Mode d’édition non visuel pour le concepteur web</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Au lieu du concepteur web de Journey Optimizer, vous pouvez désormais ajouter des modifications à votre site web à l’aide d’un éditeur non visuel. Il vous permet de saisir vos modifications manuellement sans ouvrir les pages dans l’éditeur visuel.
Ce mode de modification non visuel est utile si vous ne pouvez pas installer d’extensions de navigateur telles que l’assistant visuel Adobe Experience Cloud, nécessaire pour charger vos pages dans le concepteur web.</p>
<!--p>For more information, refer to the <a href="../email/surface-personalization.md">detailed documentation</a>.</p-->
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
<p>Auparavant disponibles pour un ensemble d’organisations (LA), les expériences dans les parcours sont désormais disponibles pour tous les utilisateurs (GA).</p>
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
<p>La prise de décision, auparavant disponible pour un ensemble d’organisations (LA) et appelée prise de décision d’expérience, est désormais disponible pour tous les utilisateurs (GA). Elle simplifie la personnalisation en offrant un catalogue centralisé d'offres marketing appelées "éléments de décision" et un moteur de décision sophistiqué. Ce moteur tire parti des règles et des critères de classement pour sélectionner et présenter les éléments de décision les plus pertinents à chaque individu. Ces éléments de décision sont intégrés de manière transparente à un large éventail de surfaces entrantes par le biais du canal d’expérience basé sur le code.</p>

<p>Pour l’instant, la prise de décision n’est pas disponible pour les clients qui ont acheté les offres complémentaires Bouclier de santé et Bouclier de confidentialité et Bouclier de sécurité Adobe.</p>

<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Jeux de règles (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer des règles de limitation de la fréquence granulaires et les appliquer à vos messages ou parcours par le biais d’ensembles de règles. Grâce à cette nouvelle fonctionnalité, vous pouvez contrôler la fréquence à laquelle vos audiences reçoivent un message en définissant des règles cross-canal, qui excluent automatiquement les profils sur-sollicités des messages et actions.</p><p>Il vous permet également de limiter le nombre de parcours par jour, semaine ou mois, ainsi que de contrôler le nombre de parcours simultanés exécutés simultanément.</p>
<p>Les jeux de règles sont disponibles dans Disponibilité limitée pour un groupe sélectionné de clients. Veuillez noter que ces fonctionnalités seront progressivement déployées vers d’autres utilisateurs à l’avenir. Contactez l’équipe de votre compte si vous souhaitez être ajouté à la liste d’attente de cette fonctionnalité.</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
</td>
</tr>
</tbody>
</table>


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
<p>Antérieurement disponibles pour un ensemble d’organisations (LA), les messages multilingues sont désormais disponibles pour tous les utilisateurs (GA).</p>
<!--p>For more information, refer to the <a href="../configuration/business-rules.md">detailed documentation</a>.</p-->
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
<li>Accélérer les workflows de mise en oeuvre pour les clients Journey Optimizer à l’aide de Da Vinci pour la création et d’AJO pour l’optimisation et la diffusion</li>
<li>Optimisez les modèles Da Vinci avec les données d’Adobe.</li></ul></p>
<!--p>For more information, refer to the <a href="../code-based/get-started-code-based.md">detailed documentation</a>.</p-->
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
<p>Disponible depuis le 16 octobre 2024</p>
<p>Les rapports Journey Optimizer sont désormais disponibles dans l’ensemble (GA). Ils s’accompagnent d’une interopérabilité améliorée avec les fonctionnalités des Customer Journey Analytics, de la normalisation des rapports sur les deux plateformes et de l’amélioration de la cohérence et de la fiabilité des données. L’intégration transparente entre Journey Optimizer et Customer Journey Analytics fournit une meilleure visibilité des mesures de performance, ce qui aide les utilisateurs et les utilisatrices à prendre des décisions plus éclairées.</p>
<p>Avec la disponibilité générale, quatre nouvelles fonctionnalités sont introduites : la possibilité de créer des mesures simples, de créer et de publier des audiences, de poser des questions ad hoc à l’aide d’Insight Builder et de planifier des rapports qui seront automatiquement envoyés par courriel aux destinataires clés.</p>
<p>Pour plus d’informations, consultez la <a href="../reports/report-cja-manage.md">documentation détaillée</a>.</p>
<img src="assets/do-not-localize/ajo-cja.gif">
<p>Important : L’expérience de création de rapports actuelle sera abandonnée à compter de janvier 2025. À partir de cette date, la nouvelle expérience de création de rapports deviendra la norme. Nous vous recommandons de vous familiariser avec les nouvelles fonctionnalités pour garantir une transition fluide. <a href="../reports/report-gs-cja.md">Découvrir la nouvelle interface de création de rapports de Journey Optimizer</a></p>
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
<p>Disponible depuis le 1er octobre 2024</p>
<p>Grâce au nouveau canal d’expérience basée sur le code, Adobe Journey Optimizer vous permet d’effectuer des tests et des personnalisations avancés pour l’une de vos propriétés entrantes, ce qui vous permet de diffuser facilement des expériences personnalisées sur différents points de contact (touchpoints) tels que des applications web, des applications mobiles, des applications de bureau, des consoles vidéo, des appareils connectés à la télévision, des téléviseurs intelligents, des kiosques, des distributeurs automatiques, des périphériques IoT, etc. Le canal d’expérience basée sur le code est désormais disponible dans la zone de travail du parcours.</p>
<p>Pour plus d’informations, consultez la <a href="../code-based/create-code-based.md">documentation détaillée</a>.</p>
<img src="../assets/do-not-localize/code-based-journey.gif"/>
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
<p>Disponible depuis le 1er octobre 2024</p>
<p>Avec le canal web, Adobe Journey Optimizer vous permet de personnaliser l’expérience web que vous diffusez à votre clientèle par le biais de parcours web entrants. Le canal web est désormais disponible dans la zone de travail du parcours.</p>
<p>Pour plus d’informations, consultez la <a href="../web/create-web.md">documentation détaillée</a>.</p>
<img src="../assets/do-not-localize/web-journey.gif"/>
</tr>
</tbody>
</table>

### Améliorations {#24-10-improvements}

Cette version est fournie avec les améliorations répertoriées ci-dessous.

**Canal SMS**

Des améliorations ont été apportées aux SMS pour améliorer vos fonctionnalités de messagerie :

* Vous pouvez définir et gérer des mots-clés uniques pour vos campagnes et parcours SMS, ce qui permet une communication plus personnalisée et efficace.

* Vous pouvez créer et diffuser un SMS par défaut lorsqu&#39;un mot-clé n&#39;est pas reconnu.

* Vous pouvez désormais modifier ou supprimer une configuration de canal de l’API SMS.

<!--**Journeys**-->

<!--* **Path experiment in journeys** - With the journey path experiment, you can now define and track key metrics for your journey paths, allowing you to measure the impact of your activities and to provide clearer insights into your performance. -->

&lt;!—* **Nombre maximal de parcours en direct** - Journey Optimizer dispose désormais d’une barrière de sécurité de 500 parcours en direct sur les environnements de test de production, au lieu de 100. Le nombre de parcours actifs est visible dans la zone de travail du parcours. <!-- DOCAC-10977-->

**Jeux de données**

* **Barrière de sécurité de durée de vie** - À compter du 1er novembre 2024, une barrière de sécurité de durée de vie (TTL) sera déployée sur les jeux de données générés par le système Journey Optimizer dans les nouveaux environnements de test et les nouvelles organisations comme suit :

   * 90 jours pour les données dans la banque de profils
   * 13 mois pour les données du lac de données

  Cette modification sera déployée ultérieurement sur les environnements de test client existants dans une seconde phase.

  En outre, à compter du 1er novembre, la segmentation par flux ne prendra plus en charge l’utilisation des événements d’envoi et d’ouverture des jeux de données de suivi et de retour. Cette modification s’appliquera à tous les environnements de test et organisations clients à ce moment-là. [En savoir plus](../data/datasets-ttl.md)

* **Paramètres dans les actions personnalisées** (Date de disponibilité : 3 octobre 2024) - Les paramètres NULL et facultatifs sont désormais pris en charge dans les actions personnalisées. [En savoir plus](../action/about-custom-action-configuration.md#define-the-message-parameters).

**Créer des rapports**

* **Le rapport de prise de décision d’expérience** est désormais disponible et offre des informations essentielles sur la manière dont vos visiteurs interagissent avec vos expériences.

**Gouvernance des données et politiques de consentement** : date de disponibilité : 7 octobre 2024

* L’application des **politiques de gouvernance des données** a désormais lieu sur tous les canaux dans Journey Optimizer. Pour les clientes et clients qui ont créé des politiques dans Adobe Experience Platform, ces dernières sont appliquées aux actions marketing dans le cadre des configurations des canaux. Lorsque vous créez du contenu à l’aide d’une configuration, le système vérifie tous les champs de personnalisation à la recherche de toute violation de gouvernance des données. Si une violation est trouvée, la publication d’un parcours ou d’une campagne n’est pas possible. [En savoir plus](../action/action-privacy.md)

* Les **politiques de consentement personnalisé** s’appliquent désormais à tous les canaux Journey Optimizer. Lors de l’application, avant l’envoi d’un message ou avant la diffusion d’une expérience entrante, le système vérifie que la personne a donné son consentement pour utiliser des champs de personnalisation dans le contenu qu’elle reçoit. Si aucun consentement n’est donné, l’expérience ne s’affiche pas. [En savoir plus](../action/consent.md)

  >[!NOTE]
  >
  >Les politiques de consentement ne sont actuellement disponibles que pour les organisations qui ont acheté les offres complémentaires Adobe **Healthcare Shield** et **Privacy and Security Shield**.

**Audiences** : date de disponibilité : 8 octobre 2024

* Lors du ciblage d’une audience de fichier CSV, vous pouvez désormais utiliser les attributs du fichier dans l’éditeur de personnalisation et dans le créateur de règles de parcours et de campagnes. [En savoir plus](../audience/about-audiences.md)

* L’utilisation des audiences et des attributs du chargement personnalisé (fichiers CSV) est désormais disponible avec Healthcare Shield ou Privacy and Security Shield.

**Canal basé sur le code**

* Des modèles de contenu sont désormais disponibles. Vous pouvez accélérer la création de vos expériences basées sur du code à partir d’un modèle de contenu créé par vos développeurs. L’utilisation d’un modèle de contenu permet au marketeur de modifier uniquement certaines valeurs ou certains champs, au lieu de composer l’ensemble de l’HTML ou de la payload du contenu JSON.

**Prise de décision**

* Les utilisateurs d’ [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=fr) peuvent désormais choisir des modèles personnalisés à optimiser lors de la configuration d’un modèle d’IA dans la prise de décision (anciennement connu sous le nom de prise de décision d’expérience). Cela vous permet, par exemple, d’optimiser sur une table personnalisée &quot;achats&quot; plutôt que sur des contraintes définies telles que le taux de clics.&quot;

* Lors de l’ajout d’une stratégie de décision à une campagne basée sur du code avec la prise de décision (précédemment appelée prise de décision d’expérience), vous pouvez désormais sélectionner manuellement des éléments de décision uniques, en plus des stratégies de sélection. En outre, vous pouvez désormais sélectionner plusieurs offres de secours. Cela garantit qu’un certain nombre d’éléments de décision sont renvoyés. [En savoir plus](../experience-decisioning/create-decision.md)

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
<p>Pour plus d’informations, consultez la <a href="../content-card/get-started-content-card.md">documentation détaillée</a>.</p>
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
<th><strong>Accélérateur de contenu de l’assistant IA </strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Une fois que vous avez créé et personnalisé votre message, placez votre contenu au niveau supérieur avec l’accélérateur de contenu de l’assistant d’IA dans Journey Optimizer. Vous pouvez désormais utiliser l’assistant d’IA pour optimiser l’impact de votre message en testant différents titres et images principaux. Chaque variante est gérée en tant que traitement unique, afin de la mesurer et de la comparer pour savoir quel titre génère le plus de clics.</p>
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


![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous à la [newsletter trimestrielle d’Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} dès aujourd’hui, et recevez les dernières mises à jour produits, les articles les plus intéressants, des cas pratiques, des conseils et bien plus encore, directement dans votre boîte de réception, tous les trimestres.