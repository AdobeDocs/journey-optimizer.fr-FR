---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour 2022
description: Notes de mise à jour de Journey Optimizer 2022
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '3479'
ht-degree: 0%

---

# Notes de mise à jour 2022 {#release-notes-2022}

Cette page répertorie toutes les fonctionnalités et améliorations pour [!DNL Journey Optimizer] publié en 2022.


## Version de septembre 2022{#sept-2022-release}

### Nouvelles fonctionnalités{#sept-2022-features}

<table>
<thead>
<tr>
<th><strong>Contenu dynamique et nouveau créateur de règles conditionnelles</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez maintenant créer du contenu dynamique pour adapter le contenu de vos messages selon des règles conditionnelles.</p> 
<p>Les règles conditionnelles sont créées à l’aide d’un créateur de règles visuel dans l’éditeur d’expression, où vous pouvez les stocker pour les réutiliser ultérieurement dans vos parcours et campagnes.</p>
<img src="assets/do-not-localize/dynamic-content.gif"/>
<p>Pour plus d’informations, reportez-vous à la section <a href="../personalization/get-started-dynamic-content.md">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Campagnes déclenchées par l’API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Outre les campagnes planifiées existantes, vous pouvez désormais créer des campagnes déclenchées par l’API dans Journey Optimizer et les appeler à partir d’un système externe à l’aide d’API.</p>
<p>Cela vous permet de couvrir divers besoins de messagerie opérationnelle et transactionnelle tels que les réinitialisations de mot de passe, le jeton OTP, etc.</p>
<img src="assets/do-not-localize/api-triggered.gif"/>
<p>Pour plus d’informations, reportez-vous à la section <a href="../campaigns/api-triggered-campaigns.md">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Contrôle d’accès aux données</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce au contrôle d’accès basé sur les attributs, les administrateurs peuvent contrôler l’accès à des objets spécifiques en fonction de certains attributs. Ces attributs peuvent être des métadonnées ajoutées à un objet, comme des libellés. À compter de cette version, les administrateurs peuvent également définir des rôles utilisateur ayant accès à des champs et/ou des objets spécifiques, ainsi qu’à des données correspondant à ces champs et/ou objets.</p>
<p> L’utilisation du contrôle d’accès basé sur les attributs est actuellement limitée à certains clients et sera déployée dans tous les environnements dans une prochaine version.</p>
<img src="assets/do-not-localize/olac.gif"/>
<p>Pour plus d’informations, reportez-vous à la section <a href="../administration/object-based-access.md">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Gouvernance et confidentialité des données</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce à son cadre de gouvernance DULE (Data Usage Labelling and Enforcement), Journey Optimizer peut désormais tirer parti des stratégies de gouvernance d’Adobe Experience Platform pour empêcher l’exportation de champs sensibles vers des systèmes tiers au moyen d’actions personnalisées. Si le système identifie un champ restreint dans les paramètres d’action personnalisée, une erreur s’affiche vous empêchant de publier le parcours.</p>
<p>L’utilisation de l’outil DULE (Data Usage Labelling and Enforcement) est actuellement limitée à certains clients et sera déployée dans tous les environnements dans une prochaine version.</p>
<p>Pour plus d’informations, reportez-vous à la section <a href="../action/action-privacy.md">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Application du consentement automatisée (stratégies de consentement)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform vous permet d’adopter et d’appliquer facilement des stratégies marketing afin de respecter les préférences de consentement de vos clients. Les stratégies de consentement sont définies dans Adobe Experience Platform. Dans Journey Optimizer, vous pouvez appliquer ces stratégies de consentement à vos actions personnalisées. Vous pouvez, par exemple, définir des stratégies de consentement afin d’exclure les clients qui n’ont pas consenti à recevoir des communications par courrier électronique, push ou SMS.
<p>L’application automatisée du consentement n’est actuellement disponible que pour les organisations qui ont acheté l’offre complémentaire du Bouclier de santé.</p>
<p>Pour plus d’informations, reportez-vous à la section <a href="../action/consent.md">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gestion des autorisations</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer prend en charge la définition des rôles utilisateur et des stratégies d’accès afin de gérer les autorisations pour les fonctionnalités et les objets. Via <strong>Autorisations Adobe Experience Cloud</strong>, vous pouvez créer et gérer des rôles, ainsi qu’affecter les autorisations de ressources souhaitées pour ces rôles. Les autorisations vous permettent également de gérer les libellés, les environnements de test et les utilisateurs associés à un rôle spécifique.</p>
<p> L’utilisation des autorisations est actuellement limitée à certains clients et sera déployée dans tous les environnements dans une version ultérieure.</p>
<p>Pour plus d’informations, reportez-vous à la section <a href="../administration/attribute-based-access.md">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Alertes et surveillance</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>En tant qu’utilisateur de Journey Optimizer, vous pouvez désormais accéder aux alertes système via l’interface utilisateur afin d’être averti lorsque les parcours ne fonctionnent pas comme prévu. Vous pouvez afficher les alertes disponibles et vous y abonner. La première alerte disponible dans cette version vous avertit si une activité Lecture de segment n’a traité aucun profil pendant la période définie. D’autres informations seront disponibles maintenant que ce workflow est déverrouillé.</p>
<p>Pour plus d’informations, reportez-vous à la section <a href="../reports/alerts.md">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>Data Hygiene</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform provides a suite of data hygiene capabilities that allow you manage your stored data through programmatic deletions of consumer records and datasets. This capability is now available for Adobe Journey Optimizer. </p>
<p>You can manage your data stores to ensure that information is used as expected, is updated when incorrect data needs fixing, and is deleted when organizational policies deem it necessary.</p>
<p><strong>Caution</strong> - Data Hygiene capabilities are currently only available for organizations that have purchased the Healthcare Shield add-on offering.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->

### Améliorations{#sept-2022-improvements}

**Parcours**

* Le **Jeu de données d’entité** est désormais disponible en tant que jeu de données d’usine dans Adobe Journey Optimizer. Ce jeu de données de recherche comprend des métadonnées pour enrichir les informations sur les jeux de données de suivi et de retour. Vous pourrez ainsi améliorer vos rapports et requêtes avec des données plus compréhensibles. [En savoir plus](../data/datasets-query-examples.md#entity-dataset)
* Une nouvelle barrière de sécurité a été ajoutée aux parcours unitaires (commençant par un événement ou une qualification de segment) pour empêcher que les parcours ne soient déclenchés par erreur plusieurs fois pour le même événement. La rentrée du profil sera désormais temporairement bloquée par défaut pendant 5 minutes. [En savoir plus](../start/guardrails.md#events-g)

**Administration**

* Lors de l’activation ou de la désactivation de la liste autorisée, un nouvel avertissement s’affiche maintenant pour détailler les impacts de chaque action. [En savoir plus](../configuration/allow-list.md#enable-allow-list)
* Mise à jour de l’interface utilisateur pour la création de surfaces de canal, la création de pools d’adresses IP, la gestion de la liste de suppression et de la liste autorisée, ainsi que la configuration du canal SMS -
* Désormais, lors de la création de la première surface de canal pour un sous-domaine donné, le temps de traitement prendra entre 10 minutes et 10 jours, et jusqu’à 3 heures uniquement pour les surfaces suivantes utilisant ce sous-domaine. [En savoir plus](../configuration/channel-surfaces.md#create-channel-surface)
* Mise à jour de l’interface utilisateur pour la création de paramètres prédéfinis de landing page et de sous-domaines de landing page - [En savoir plus](../landing-pages/lp-subdomains.md)

**Contrôles de contrôle**

* Avec Journey Optimizer, vous pouvez identifier les actions effectuées par les utilisateurs du système sur divers services et fonctionnalités tels que les campagnes, parcours, messages, landing pages, etc. Les ressources du journal d’audit incluent désormais des modifications sur diverses autres actions et sont enregistrées automatiquement au fur et à mesure de l’activité. En savoir plus [dans cette page](../privacy/audit-logs.md).

**Prise en charge de l’archivage**

* La nouvelle **Jeu de données d’entité** inclut un champ Modèle qui permet d&#39;exporter le format et la structure des messages envoyés sur tous les canaux à des fins d&#39;archivage. [En savoir plus](../configuration/archiving-support.md)

**Landing pages**

* Vous pouvez désormais utiliser des données contextuelles provenant d&#39;une autre page dans la même landing page. Par exemple, si vous associez une case à cocher à une liste d’abonnements sur la page d’entrée principale, vous pouvez utiliser cette liste d’abonnements sur la sous-page &quot;merci&quot;. [En savoir plus](../landing-pages/lp-content.md#use-primary-page-context)

<!--* When configuring the primary page, you can now create additional data to enable storing information when the landing page is being submitted. [Learn more](../landing-pages/lp-content.md#use-additional-data)-->

<!--* You can now use information that was submitted on a landing page to send communications to your customers. For example, if a user subscribes to a given subscription list, you can leverage that information to send an email recommending other subscription lists to that user.-->

### Autres modifications{#sept-2022-other}

* Le mode d’accélération du parcours a été remplacé par le mode de livraison rapide de Campaign. [En savoir plus](../campaigns/create-campaign.md#rapid-delivery)
* Pour améliorer les performances, les groupes de champs d’événement d’expérience ne peuvent plus être utilisés dans les parcours commençant par un segment de lecture, une qualification de segment ou une activité d’événement professionnel. Cette modification s’applique uniquement aux nouveaux parcours. Ceux qui existent déjà conserveront le comportement actuel. [En savoir plus](../start/guardrails.md#expression-editor)
* La limitation d’une heure pour les parcours de segments de lecture programmés a été supprimée. Ces parcours peuvent désormais être exécutés sans délai.




## Version d’août 2022 {#aug-2022-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>
<th><strong>Créer et gérer des campagnes dans Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Utilisez les campagnes Journey Optimizer pour diffuser du contenu ponctuel sur un segment spécifique à l’aide de divers canaux. Lors de l’utilisation de parcours, les actions sont conçues pour être exécutées en séquence. Avec les campagnes, les actions sont exécutées simultanément, immédiatement ou selon un planning spécifié. </p>
<img src="assets/do-not-localize/campaigns.gif"/>
<p>Découvrez comment créer une campagne dans le <a href="../campaigns/get-started-with-campaigns.md">documentation détaillée</a> et <a href="https://video.tv.adobe.com/v/346680">vidéo sur les fonctionnalités</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Envoyer des SMS à vos utilisateurs (disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer, personnaliser et envoyer des SMS dans Journey Optimizer, grâce à une intégration avec <b>Sinch</b> ou <b>Twilio</b>.</p>
<img src="assets/do-not-localize/SMS.gif"/>
<p>Découvrez comment créer et envoyer un SMS dans cette <a href="../sms/create-sms.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>New Dynamic Expression Builder</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create conditional content blocks across different authoring services to personalize your content.</p>
<p>In addition to the Personalization Expression Library, the Expression Editor provides a new Conditional Rule Builder to help you design and save your content blocks.</p>
<p>For more information, refer to the <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">detailed documentation</a>.
</td>
</tr>
</tbody>
</table-->


### Améliorations

**Reporting**

* Le tableau et le graphique des stratégies de consentement sont désormais disponibles dans les rapports globaux du parcours. Ces widgets vous permettent de suivre les profils exclus des stratégies de vos actions personnalisées. [En savoir plus](../reports/journey-global-report.md#journey-global)

   Pour avoir accès aux derniers widgets, vous devrez réinitialiser les différents tableaux de bord de rapports. Pour plus d’informations sur la personnalisation des tableaux de bord, reportez-vous à la section [la documentation détaillée ;](../reports/global-report.md).

**Administration**

* Il est désormais possible de mettre à jour le numéro de téléphone principal à utiliser pour le canal SMS. [En savoir plus](../configuration/primary-email-addresses.md)


## Version de juillet 2022 {#july-2022-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>
<th><strong>Nouveau flux de messagerie en ligne</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer fournit un nouveau flux pour la création de messages dans les parcours. La messagerie en ligne permet aux utilisateurs de gagner du temps et de rationaliser le processus de création et de diffusion d’un email, d’une notification push ou d’un SMS dans Journey Optimizer. En supprimant les messages comme une étape distincte et en les rendant modifiables en ligne dans le cadre d’une action sur le Canevas du parcours, les utilisateurs devront cliquer sur moins de boutons et parcourir moins d’écrans pour concevoir et modifier leur contenu.</p>
<img src="assets/do-not-localize/inline.gif"/>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Contrôle d’accès basé sur les attributs (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais identifier les champs de schéma avec des libellés qui définissent les portées d’utilisation des données ou de l’organisation. Les administrateurs peuvent utiliser l’interface Autorisations pour définir des stratégies d’accès couvrant les champs de schéma XDM et mieux gérer l’accès attribué aux utilisateurs ou groupes d’utilisateurs (utilisateurs internes, externes ou tiers) et gérer l’accès à des types de données spécifiques (c’est-à-dire des données personnelles sensibles/SPD).</p>
<p>L’utilisation du contrôle d’accès basé sur les attributs est actuellement limitée à certains utilisateurs et sera déployée dans tous les environnements dans une prochaine version.</p>
<p>Pour plus d’informations, reportez-vous à la section <a href="../administration/attribute-based-access.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Tâches de prise de décision par lots</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais exécuter des tâches de prise de décision par lots à partir de l’interface utilisateur, de sorte que je n’ai pas besoin d’un développeur pour exécuter des tâches d’api par lots et que je puisse réduire le temps nécessaire au marketing. Cette nouvelle interface vous permet de créer des tâches et de gérer les tâches actuelles/antérieures.</p>
<img src="assets/do-not-localize/batch.gif"/>
<p>Pour plus d’informations, reportez-vous à la section <a href="../offers/batch-delivery.md">documentation détaillée.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utiliser automatiquement l’offre la plus performante dans vos décisions (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais utiliser des systèmes de modèles d’optimisation personnalisés dans la gestion des décisions. Ce nouveau type de modèle permet d’optimiser et de personnaliser les offres en fonction des segments et des performances des offres.</p>
<p>L’utilisation des modèles d’optimisation personnalisée d’AI est actuellement limitée à certains utilisateurs et sera déployée dans tous les environnements dans une prochaine version.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Pour plus d’informations, reportez-vous à la section <a href="../offers/ranking/personalized-optimization-model.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations

**Parcours**

* **Fin d’un parcours** - Dans la zone de travail du parcours, la variable **Fin** l’activité a été supprimée de la palette. Les balises de fin sont désormais ajoutées par défaut à la fin de chaque chemin et ne peuvent pas être supprimées. Cette amélioration permet de mieux signaler le moment où un client a abandonné le parcours, sans aucune action requise de la part du praticien du parcours. Reportez-vous à la section [documentation](../building-journeys/end-journey.md) et [vidéo sur les fonctionnalités](https://video.tv.adobe.com/v/345376){target=&quot;_blank&quot;}.


* Le **Fuseau horaire du profil** est désormais décochée par défaut dans les propriétés du parcours. [En savoir plus](../building-journeys/timezone-management.md#timezone-from-profiles)

**Messages**

* Les paramètres de message prédéfinis sont désormais **surfaces des canaux**. [En savoir plus](../configuration/channel-surfaces.md)

**Administration**

* **Modification des enregistrements PTR** - Désormais, lors de la mise à jour d’un enregistrement PTR, le temps de traitement ne prendra que 3 heures. [En savoir plus](../configuration/ptr-records.md#processing)

* **Interface utilisateur des listes autorisées** - Vous pouvez désormais utiliser l’interface utilisateur de Journey Optimizer pour ajouter de nouvelles adresses électroniques ou de nouveaux domaines à la liste autorisée. [En savoir plus](../configuration/allow-list.md)

* **Mise à jour de la logique de liste autorisée** - Désormais, la logique de liste autorisée s’applique dès que la fonction est activée, même si la liste est vide. [En savoir plus](../configuration/allow-list.md#logic)

* **Paramètres de suivi des URL** - Vous pouvez désormais utiliser l’éditeur d’expression pour configurer les paramètres de suivi d’URL sur vos surfaces d’email (c’est-à-dire les paramètres prédéfinis). [En savoir plus](../email/email-settings.md#url-tracking)

**Gestion des décisions**

* **Taille de l’audience** - Un nouveau composant d’estimation de la taille de l’audience s’affiche désormais dans l’interface utilisateur lors de la création d’une règle de décision, lors de la sélection d’un segment ou d’une règle pour définir l’éligibilité d’une offre ou lors de l’ajout d’un segment ou d’une règle à une portée de décision.


## Version de juin 2022 {#june-2022-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>
<th><strong>Envoyer des SMS à vos utilisateurs (disponibilité limitée)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer, personnaliser et envoyer des SMS dans Journey Optimizer, grâce à une intégration avec <b>Sinch</b> ou <b>Twilio</b>.</p>
<!--img src="assets/do-not-localize/SMS.gif"/-->
<p>Le canal SMS est actuellement disponible uniquement pour un ensemble d’organisations (disponibilité limitée). Pour plus d’informations, contactez votre représentant Adobe.</p>
<p>Découvrez comment créer et envoyer un SMS dans cette <a href="../sms/create-sms.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Trouvez plus rapidement d’images d’impact grâce à l’intégration d’Adobe Stock.</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le plug-in d’intégration du Concepteur d’email d’Adobe Stock et d’Adobe Journey Optimizer fournit aux clients un moyen simple de naviguer, d’acquérir sous licence et d’enregistrer des images pour les utiliser dans la création de messages. </br> La nouvelle <b>Rechercher des photos Stock similaires</b> Cette option vous permet également de localiser les photos Stock qui correspondent au contenu, à la couleur et à la composition de vos images. </p>
<!--img src="assets/do-not-localize/stock-rn.gif"/-->
<p>Pour plus d’informations, reportez-vous à la section <a href="../email/stock.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utiliser la fonctionnalité Email Cci sur tous vos emails</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais utiliser la fonctionnalité Email Cci (copie carbone invisible) pour stocker les emails envoyés par Adobe Journey Optimizer. Activez cette option dans vos paramètres prédéfinis d’e-mail de sorte que chaque e-mail envoyé soit copié aveuglément vers votre adresse Cci.</p>
<!--img src="assets/do-not-localize/bcc-rn.gif"/-->
<p>Pour plus d’informations, reportez-vous à la section <a href="../configuration/archiving-support.md#bcc-email">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--<table>
<thead>
<tr>
<th><strong>Automatically use the best performing offer in your decisions</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now use personalized optimization model systems in Decision Management. This new type of model allows you to optimize and personalize offers based on segments and offer performance.</p>
<p>The use of personalized optimization AI models is currently restricted to selected users, and will be deployed to all environments in a future release.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>-->

<table>
<thead>
<tr>
<th><strong>Copie d’objets entre des environnements de test</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais recréer les expériences d’un environnement de test Journey Optimizer vers un autre, par exemple d’un environnement de test hors production vers un environnement de test de production. Cette nouvelle fonctionnalité copie l’intégralité d’un parcours, y compris tous les objets dont le parcours dépend pour s’exécuter correctement, d’un environnement à un autre. Outre les parcours, vous pouvez également copier d’autres composants, tels que les offres, les messages, les schémas, les jeux de données, les sources de données, les événements et les actions.</p>
<p>Pour plus d’informations, reportez-vous à la section <a href="../building-journeys/copy-to-sandbox.md">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>




### Améliorations

**Gestion des décisions**

* **Prise en charge des fichiers HTML et JSON** - Vous pouvez désormais faire glisser et déposer des fichiers HTML et JSON externes de la bibliothèque de ressources Adobe Experience Cloud dans le contenu de représentation de l’offre. [En savoir plus](../offers/offer-library/add-representations.md#html-json)


**Email**

* **Enregistrer en tant que modèle** - Vous pouvez désormais enregistrer un contenu d&#39;email en tant que modèle et le réutiliser lors de la création d&#39;autres messages. [En savoir plus](../email/email-templates.md)


**Administration**

* **Aperçu des paramètres d’URL de suivi** - Lors de la configuration d&#39;un paramètre prédéfini de message, si vous définissez des paramètres de tracking URL, un aperçu dynamique de l&#39;URL de tracking résultante s&#39;affiche désormais. [En savoir plus](../email/email-settings.md#url-tracking)

* **Modification des paramètres prédéfinis de message** - Désormais, lors de la mise à jour d’un paramètre prédéfini de message, le temps de traitement ne peut excéder 3 heures. [En savoir plus](../configuration/channel-surfaces.md#edit-channel-surface)

* **Modification du pool d’adresses IP** - Désormais, lors de la mise à jour d’un pool d’adresses IP, le temps de traitement ne peut excéder 3 heures. [En savoir plus](../configuration/ip-pools.md#edit-ip-pool)




## Version de mai 2022 {#may-2022-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>
<th><strong>Règles de fréquence des messages</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais définir des règles métier cross-canal qui excluront automatiquement les profils sur-sollicités des messages et actions.</p>
<!--img src="assets/do-not-localize/frequency-rn.gif"/-->
<p>Pour plus d’informations, reportez-vous à la section <a href="../configuration/frequency-rules.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gestion des décisions - Modèle d’optimisation automatique du classement AI</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais utiliser des systèmes de modèle formés dans la gestion de la décision. Cette nouvelle fonctionnalité classe les offres à afficher pour un profil donné.</p>
<!--img src="assets/do-not-localize/optimization.gif"/-->
<p>Pour plus d’informations, reportez-vous à la section <a href="../offers/offer-activities/configure-offer-selection.md#use-ranking-strategy">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--table>
<thead>
<tr>
<th><strong>Attribute-based Access Control (ABAC)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Permission management in Journey Optimizer has been extended to data access. You can now manage data access for specific teams or groups of users (i.e. internal, external, 3rd parties) ​and manage access to specific types of data (i.e. Sensitive Personal Data/SPD).</p>
<p>This capability is available for a limited set of customers.</p>
<p>For more information, refer to the <a href="../landing-pages/create-lp.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Journaux d’audit de Journey Optimizer</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais surveiller les actions effectuées par les utilisateurs sur les ressources Adobe Journey Optimizer.</p>
<!--img src="assets/do-not-localize/audit-rn.gif"/-->
<p>Pour plus d’informations, reportez-vous à la section <a href="../privacy/audit-logs.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations

**Personnalisation**

* **Nouvelle fonction d’assistance pour le masquage des caractères** - Le `mask` La fonction d’assistance vous permet de remplacer une partie d’une chaîne par des caractères &quot;X&quot;. [En savoir plus](../personalization/functions/string.md#mask)

**Landing pages**

* **Landing pages sans formulaire** - Vous pouvez désormais créer et publier une landing page qui ne contient pas de formulaire et ne nécessite aucune action de la part des visiteurs.
* **Modèles de landing page** - Vous pouvez désormais enregistrer une landing page en tant que modèle et la réutiliser lors de la création d&#39;autres landing pages. [En savoir plus](../landing-pages/lp-templates.md)
* **Retour à la page principale** - Vous pouvez désormais ajouter un lien vers la page principale à partir de n’importe quelle sous-page de la même page d’entrée.
* **Prise en charge JavaScript personnalisée** - Vous pouvez désormais ajouter du code JavaScript personnalisé au contenu de votre page d’entrée pour appliquer un style avancé ou ajouter des comportements personnalisés à vos pages d’entrée.    [En savoir plus](../landing-pages/lp-custom-js.md)

**Parcours**

* **Lecture de segment** - Les parcours de lecture en une seule fois de segment passent désormais à l’état Terminé 30 jours après l’exécution du parcours. Pour les segments de lecture planifiés, il s’agit de 30 jours après l’exécution de la dernière occurrence. [En savoir plus](../building-journeys/read-segment.md)
* **Editeur d&#39;expression** - Le [limit](../building-journeys/functions/functionlimit.md) a été ajoutée pour vous permettre de limiter le nombre d’éléments d’une liste. Le [sort](../building-journeys/functions/functionsort.md) vous permet désormais de trier un objet de liste. La prise en charge de listObject a également été ajoutée à la fonction [disctinct](../building-journeys/functions/functiondistinct.md) et [distinctWithNull](../building-journeys/functions/functiondistinctwithnull.md) fonctions.

**Administration**

* **Mise à jour du tableau de bord d’utilisation des licences** - Le tableau de bord de l’utilisation de la licence disponible dans la [!DNL Adobe Journey Optimizer] L’interface utilisateur reflète désormais la valeur exacte de la variable **Sous licence** Richesse moyenne des profils. Une baisse de cette représentation de mesure s’affiche, ce qui signifie que la limite de licence est désormais correctement signalée. [En savoir plus](../segment/license-usage.md)


## Version d’avril 2022 {#april-2022-release}

### Améliorations

**Landing pages**

* **Nouvelle option pour les cases à cocher d’inclusion/exclusion** - Vous pouvez désormais insérer une seule case à cocher pour les opt-in/opt-out dans les landing pages d&#39;abonnement. Les utilisateurs doivent cocher la case pour accepter (opt-in) et la décocher pour supprimer leur consentement (opt-out). [En savoir plus](../landing-pages/design-lp.md#define-lp-specific-content)

* **Préremplir les champs des landing pages** - Il est désormais possible de donner aux utilisateurs la possibilité de préremplir les champs de la landing page avec les informations de profil. [En savoir plus](../landing-pages/create-lp.md#configure-primary-page)

**Gestion des décisions**

* **API de prise de décision sur Edge** - L’API Edge Decisioning peut diffuser et générer des offres personnalisées gérées dans la gestion des décisions. Vous pouvez créer vos offres et d’autres objets associés à l’aide de l’interface utilisateur (interface utilisateur) ou des API de la gestion de décision. [En savoir plus](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**Administration**

* **Durée d’envoi des PTR** - La durée d’efficacité de la modification PTR est désormais de quelques heures. [En savoir plus](../configuration/ptr-records.md#processing)

**Conception d&#39;email**

* **20 nouveaux modèles d&#39;email** sont désormais disponibles pour concevoir le contenu de votre email dans Journey Optimizer.

**Interface utilisateur**

* **Aide contextuelle dans l’interface utilisateur de Journey Optimizer** - Des liens d’aide contextuelle ont été ajoutés à plusieurs pages dans Journey Optimizer. Lorsque cette option est disponible, cliquez sur l’icône &quot;i&quot; pour afficher une description rapide de la fonctionnalité actuelle et accéder aux articles connexes.

**Intégration à Adobe Campaign Standard**

En tant que client Adobe Campaign Standard, vous pouvez désormais envoyer des emails, des notifications push et des SMS à l’aide de Journey Optimizer. Utilisez les nouvelles actions intégrées pour tirer parti des fonctionnalités de messagerie transactionnelle de Campaign Standard dans Journey Optimizer.  [En savoir plus](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## Version de mars 2022 {#march-2022-release}

### Améliorations

**Parcours**

* Pour éviter d’avoir des champs inutiles dans le schéma de profil unifié, le schéma Événement d’étape du parcours n’est plus activé par défaut pour les profils. Si nécessaire, vous pouvez l’activer. [En savoir plus](../reports/sharing-overview.md)
* Les nouveaux événements d’étape liés aux tâches d’exportation sont désormais envoyés par Journey Optimizer à Adobe Experience Platform. Des exemples de requêtes ont été ajoutés à la documentation. [En savoir plus](../reports/query-examples.md)

**Gestion des décisions**

* Vous pouvez maintenant spécifier si la limitation de l’offre est appliquée à tous les utilisateurs ou à un profil spécifique, à tous les emplacements ou à chaque emplacement. [En savoir plus](../offers/offer-library/add-constraints.md#capping)
* L’API Batch Decisioning permet aux entreprises d’utiliser la fonctionnalité de gestion de la décision pour tous les profils d’un segment donné en un seul appel. Le contenu de l’offre pour chaque profil du segment est placé dans un jeu de données AEP où il est disponible pour les workflows par lots personnalisés. [En savoir plus](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**Administration**

* Vous pouvez maintenant activer/désactiver le lien de désabonnement dans/à partir de l’en-tête de l’email au niveau du paramètre prédéfini de message, et définir une URL de désabonnement personnalisée au niveau du message. [En savoir plus](../configuration/channel-surfaces.md#list-unsubscribe)
* La liste autorisée peut désormais être activée et désactivée via la variable [!DNL Journey Optimizer] sur les environnements de test de production et hors production. [En savoir plus](../configuration/allow-list.md#enable-allow-list)

**Personnalisation**

* Vous pouvez désormais enregistrer plus de 40 expressions de personnalisation dans la bibliothèque. [En savoir plus](../personalization/personalization-library.md)

## Version de février 2022 {#feb-2022-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>
<th><strong>Pages d’entrée d’abonnements</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer et concevoir des landing pages dans Journey Optimizer et orienter vos utilisateurs vers des formulaires en ligne où ils peuvent s’inscrire ou se désinscrire de la réception de vos communications, ou s’abonner à un service spécifique tel qu’une newsletter.</p>
<p>Pour plus d’informations, reportez-vous à la section <a href="../landing-pages/create-lp.md">documentation détaillée</a> et connexes <a href="../landing-pages/lp-use-cases.md">exemple de cas d’utilisation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nouvelle bibliothèque d’expressions de personnalisation</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer fournit désormais une bibliothèque dans laquelle vous pouvez accéder aux expressions de personnalisation prédéfinies. Ces expressions sont configurées par les utilisateurs administrateurs.</p>
<p>Pour plus d’informations, reportez-vous à la section <a href="../personalization/personalization-library.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<!--table>
<thead>
<tr>
<th><strong>API Developer Site and Suppression API</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer provide RESTful APIs that allow you to programmatically perform key operations in your applications.
Developer SDK for Journey Optimizer is now available with the Suppression API (beta).</p>
<p>With this API, you can control your outgoing messages using suppression and allow lists.
The suppression list helps you with honoring the ISPs' feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
<p>See <a href="https://developer.adobe.com/journey-optimizer-apis/">Adobe Journey Optimizer APIs</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Transmettre des informations pour suivre vos messages avec les paramètres de suivi UTM</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dans le contenu du message Journey Optimizer, vous pouvez désormais ajouter des paramètres UTM à vos liens : ils peuvent fournir des données supplémentaires sur ce lien et vous aider à identifier où et pourquoi une personne a cliqué sur ce lien.</p>
<p>Pour plus d’informations, reportez-vous à la section <a href="../configuration/channel-surfaces.md#configure-email-settings">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations

**Parcours**

* Pour optimiser les performances, tous les parcours en mode test qui n’ont pas été déclenchés depuis une semaine repasseront désormais à l’état En création . [En savoir plus](../building-journeys/testing-the-journey.md#important_notes)
* L’intégration entre Journey Optimizer et Adobe Campaign Classic a été optimisée pour améliorer les performances. La configuration par défaut de limitation a été remplacée par 4 000 appels / 5 minutes.    [En savoir plus](../action/acc-action.md#important-notes)

**Reporting**

* Les diffusions peuvent désormais être filtrées en fonction de leur état :
   * Dans la liste Exécution des messages , vous pouvez désormais exclure les BAT de la liste de vos diffusions.
   * Dans vos rapports en direct/globaux, vous pouvez choisir d’exclure les événements de test.

* Vous pouvez désormais accéder aux rapports sur les données d’optimisation de l’heure d’envoi : le nombre de personnes qui ont reçu immédiatement des messages et le nombre de personnes qui ont reçu des messages avec une optimisation d’une heure, une optimisation de 2 heures, etc.

<!--* decision management reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**Gestion des décisions**

* Les classements et le classement AI sont désormais regroupés dans un seul onglet.

## Version de janvier 2022 {#january-2022-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>
<th><strong>Parcours - Optimisation de la progression de votre adresse IP avec des conditions de limitation de profil</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Lors de la configuration d’un <strong>Condition</strong> dans un parcours, vous pouvez maintenant définir une limite de profil. Ce nouveau type de condition vous permet de définir un nombre maximal de profils pour un chemin de parcours. Lorsque cette limite est atteinte, les profils entrant prennent un autre chemin. Vous pouvez ainsi augmenter le volume de vos diffusions (montée en puissance de l'IP). Par exemple, vous pouvez augmenter le nombre de diffusions sur un domaine en fractionnant l'exécution : envoyer 1 000 messages le 1er jour 2000 le 2 jour, etc.</p>
<p>Pour plus d’informations, reportez-vous à la section <a href="../building-journeys/condition-activity.md#profile_cap">documentation détaillée</a> et connexes <a href="../building-journeys/ramp-up-deliveries-uc.md">exemple de cas d’utilisation</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Parcours - Lecture de l’amélioration des segments</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le <strong>Lecture incrémentale</strong> a été ajoutée à l’option récurrente <strong>Lecture de segment</strong> activités. Cette option vous permet de cibler uniquement les individus entrés dans le segment depuis la dernière exécution du parcours. La première exécution cible toujours tous les membres du segment.</p>
<p>Pour plus d’informations, reportez-vous à la section <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>

### Améliorations

**Parcours**

* Les événements d’étape de Journey Optimizer peuvent désormais être liés à d’autres jeux de données dans [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html). Le **profileID** dans le schéma d’événement d’étape du parcours intégré, est désormais défini comme un champ d’identité. [En savoir plus](../reports/sharing-overview.md#integration-cja)

**Gestion des décisions**

* Lorsque vous mettez à jour une offre, une offre de secours, une collecte d’offres ou une décision d’offre directement ou indirectement référencée dans un message publié, les mises à jour sont désormais automatiquement répercutées dans le message correspondant, sans avoir à la republier. [En savoir plus](../offers/offers-e2e.md#insert-decision-in-email)

* Lors de la simulation des offres qui seront diffusées pour un profil de test donné, vous pouvez maintenant modifier les paramètres de simulation par défaut et afficher le code correspondant à vos simulations, qui peut être utilisé à des fins de dépannage. [En savoir plus](../offers/offer-activities/simulation.md#define-simulation-settings)

**Administration**

* Les administrateurs peuvent désormais modifier les enregistrements PTR avec un CNAME configuré comme sous-domaine. [En savoir plus](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**Personnalisation**

* **Ajouter aux favoris** - Pour améliorer l’efficacité lors de l’utilisation de la personnalisation, nous avons introduit le concept d’enregistrement des favoris. L’ajout d’attributs différents à votre menu favoris permet d’accéder rapidement aux éléments que vous utilisez le plus souvent. [En savoir plus](../personalization/personalize.md#fav)
