---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
description: Notes de mise à jour de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: d759ecdbf915bf3dbbb01d25cb2537aa37a0e206
workflow-type: tm+mt
source-wordcount: '2466'
ht-degree: 100%

---

# Notes de mise à jour {#release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour.

Les notes de mise à jour précédentes sont disponibles sur [cette page](release-notes-2022.md). Vous pouvez également consulter la page relative aux [dernières mises à jour de la documentation](documentation-updates.md) pour prendre connaissance des autres modifications.

[!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous à la [newsletter trimestrielle d’Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} dès aujourd’hui, et recevez les dernières mises à jour produits, les articles les plus intéressants, des cas pratiques, des conseils et bien plus encore, directement dans votre boîte de réception, tous les trimestres.


## Notes de mise à jour de mai 2023 {#may-rn-2023}

<!--Information below is subject to change without prior notice until the release availability date. Updated documentation will be published at the release date, and direct links will be added in this page.

**Release date**: May 25, 2023-->

### Nouvelles fonctionnalités{#may-2023-features}

<!--
<table>
<thead>
<tr>
<th><strong>Audience Composition</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now create composition workflows to combine existing Adobe Experience Platform audiences into a visual canvas and leverage various activities (split, enrich...) to create new audiences. Newly created audiences are saved backed into Adobe Experience Platform along with existing audiences and can be leveraged in Journey Optimizer campaigns to target customers.</p>
<img src="../segment/assets/audiences-publish.png"/>
<!--p>For more information, refer to the <a href="../offers/ranking/personalized-optimization-model.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Expérimentation de contenu dans les campagnes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer prend désormais en charge les expériences dans les campagnes. Les expériences sont des essais randomisés, ce qui, dans le cadre des tests en ligne, signifie que vous exposez certains utilisateurs et utilisatrices sélectionnés de manière aléatoire à une variante donnée d’un message et un autre ensemble d’utilisateurs et utilisatrices sélectionnés de manière aléatoire à une autre variation de traitement. Après l’exposition, vous pouvez ensuite mesurer les mesures de résultats qui vous intéressent, par exemple les ouvertures d’e-mails, les abonnements ou les achats.</p>
<img src="assets/do-not-localize/experiment.gif"/>
<p>Pour plus d’informations, consultez la <a href="../campaigns/content-experiment.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Objective reporting and performance measurement in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now measure the performance of your campaigns across inbound and outbound through dedicated reports. Adobe Journey Optimizer reports can retrieve additional metrics to use in the Objectives tab of your campaign reports.</p>
<img src="assets/do-not-localize/performance_report.gif"/>
<p>For more information, refer to the <a href="../reports/campaign-global-report.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->


<table>
<thead>
<tr>
<th><strong>Créer et utiliser des fragments dans le contenu de votre e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer, utiliser et gérer des fragments pour rédiger rapidement vos e-mails et vos modèles de contenu. Un fragment est un composant réutilisable prédéfini, qui peut être intégré à plusieurs e-mails dans les campagnes et parcours Journey Optimizer, pour un processus de conception amélioré et plus rapide.</p>
<img src="assets/do-not-localize/fragments.gif"/>
<p>Pour plus d’informations, consultez la <a href="../email/fragments.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Utiliser des balises dans vos campagnes (version Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais attribuer des balises unifiées Adobe Experience Platform à vos campagnes. Vous pouvez ainsi facilement les classer et améliorer la recherche à partir de la liste des campagnes. Notez que la fonctionnalité de balises unifiées est actuellement en version Beta.</p>
<img src="assets/do-not-localize/campaigns-tag.gif"/>
<p>Pour plus d’informations, consultez la <a href="../start/search-filter-categorize.md#tags">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>



<table>
<thead>
<tr>
<th><strong>Modèle de classement AI d’optimisation personnalisée (disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les modèles de classement AI d’optimisation personnalisée sont désormais disponibles dans la gestion des décisions. Ce nouveau type de modèle permet d’optimiser et de personnaliser les offres en fonction des segments et des performances des offres.</p>
<img src="assets/do-not-localize/ai-ranking.gif"/>
<p>Pour plus d’informations, consultez la <a href="../offers/ranking/personalized-optimization-model.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>



### Améliorations {#may-2023-improvements}



**Audiences**

* En vue de la disponibilité générale de la fonctionnalité Audience Portal, Adobe Experience Platform met à jour l’utilisation d’audiences et de segments dans le système et dans la documentation.

   * Audience : ensemble de personnes, de comptes, de foyers ou d’autres entités qui partagent des caractéristiques et des comportements communs.
   * Définition d’un segment : règles utilisées pour décrire les caractéristiques ou le comportement clés d’une audience cible dans Adobe Experience Platform. Ce terme était auparavant appelé « segment ».

   Par conséquent, dans Adobe Journey Optimizer et l’interface utilisateur d&#39;Adobe Experience Platform, « Segments » est remplacé par « Audiences » pour refléter ce nouveau chemin de création et de gestion d’audience.

   Les traductions du terme « audience » lorsqu’elles font référence à un groupe de profils destinés à recevoir un message ont été harmonisées dans l’ensemble des produits de l’expérience digitale pour certaines langues :

   * Allemand : Zielgruppe
   * Portugais brésilien : público-alvo
   * Espagnol : público desatario


<!--* Enhancements have been made to the audience picker in journeys or campaigns, with the addition of new columns displaying the origin and update frequency of audiences.-->

**Canal SMS**

* Infobip a été ajouté en tant que fournisseur lors de la configuration des surfaces de vos canaux SMS. [En savoir plus](../sms/sms-configuration.md).
* Twillio – La configuration des informations d’identification API inclut désormais la possibilité d’ajouter le SID du service de messagerie pour une intégration transparente à votre compte Twillio. [En savoir plus](../sms/sms-configuration.md).

**Canal in-app**

* Ajout de nouvelles règles de déclenchement de message pour Adobe Places Service. [En savoir plus](../in-app/inapp-configuration.md).
* Ajout de nouvelles fonctionnalités Adobe Experience Platform Assurance permettant de capturer des événements d’appareil à ajouter en tant que règles de déclenchement.

<!--
**Journeys**

* You can now leverage API call responses in custom actions and orchestrate your journey based on these responses.
-->

**Campagnes**

* Il est désormais possible de dupliquer une campagne à partir de l’écran d’inventaire à l’aide du menu d’action représentant des points de suspension. [En savoir plus](../campaigns/modify-stop-campaign.md#duplicate).
* Vous pouvez désormais supprimer les brouillons des modifications d’une campagne active.
* Les étapes d’activation d’une campagne ont été simplifiées. [En savoir plus](../campaigns/modify-stop-campaign.md).

**Gestion des décisions**

* Vous pouvez désormais modifier le capping de la fréquence si le statut de l’offre est **[!UICONTROL Brouillon]** et si l’offre n’a jamais été publiée auparavant avec le capping de la fréquence activée. [En savoir plus](../offers/offer-library/add-constraints.md#frequency-capping).

**Personnalisation**

* Vous pouvez désormais sélectionner et insérer des références de ressources directement à partir de l’éditeur de personnalisation lorsque vous travaillez dans du contenu HTML.

### Correctifs{#may-2023-fixes}

* Messages in-app : correction d’un problème en raison duquel la planification de campagne était en conflit avec les paramètres de fréquence des messages.


## Notes de mise à jour d’avril 2023 {#apr-rn-2023}

<!--Information below is subject to change without prior notice until the release availability date. Updated documentation will be published at the release date, and direct links will be added in this page.

**Release date**: April 27, 2023-->

### Nouvelles fonctionnalités{#apr-2023-features}

<table>
<thead>
<tr>
<th><strong>Canal web (disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer étend ses fonctionnalités cross-canal en ajoutant la prise en charge du canal web. Vous pouvez désormais créer, modifier et prévisualiser des expériences web comme n’importe quel autre canal, au moyen d’une interface visuelle intelligente et intuitive qui vous permettra de personnaliser l’expérience de vos utilisateurs et utilisatrices. Notez qu’actuellement, Journey Optimizer permet de créer des expériences web dans les campagnes uniquement.</p>
<img src="assets/do-not-localize/web-authoring.gif"/>
<p>Pour plus d’informations, consultez la <a href="../web/get-started-web.md">documentation détaillée</a>.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Workflow de démarrage rapide de l’intégration mobile (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Le nouveau workflow de démarrage rapide de l’intégration mobile est désormais disponible. Utilisez cette nouvelle fonctionnalité de produit pour configurer rapidement le SDK mobile afin de commencer à collecter et valider les données d’événement mobile et d’envoyer des notifications push mobiles avec Adobe Journey Optimizer. Cette fonctionnalité est accessible via la page d’accueil de collecte de données en tant que version Beta publique.</p>
<img src="../push/assets/mobile-wf-home.png"/>
<p>Pour plus d’informations, consultez la <a href="../push/mobile-onboarding-wf.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Nouveau tableau de bord des parcours (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p> Le tableau de bord des parcours est maintenant divisé en deux onglets :</p>
<ul><li>Depuis l’onglet <strong>Aperçu</strong>, vous pouvez accéder à un nouveau tableau de bord qui affiche les mesures clés liées à vos parcours.</li>
<li>Utilisez l’onglet <strong>Parcourir</strong> pour accéder à la liste de tous les parcours.</li></ul>
<p>Cette fonctionnalité est accessible en version Beta publique dans tous les parcours.</p>
<img src="assets/do-not-localize/journey-dashboard.gif"/>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/journey-gs.md#journey-access">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#april-2023-improvements}

**Parcours**

* La zone de travail du parcours affiche désormais l’ID d’activité sur les activités de message et les balises de fin. Le reporting et le reciblage sont ainsi améliorés.
* La disposition du volet de configuration, qui s’affiche dans les actions, les sources de données, les événements et les parcours, a été améliorée.
* De nouveaux garde-fous ont été ajoutés aux parcours :
   * Le nombre d’activités d’un parcours est désormais limité à 50. [En savoir plus](../start/guardrails.md#journeys-guardrails-journeys).
   * Le nombre de **parcours actifs** dans une organisation est désormais limité à 100 par sandbox. Les parcours en mode test ne sont pas pris en compte. [En savoir plus](../start/guardrails.md#journeys-guardrails-journeys).

* Lors de l’ajout d’une action [E-mail](../email/create-email.md), [SMS](../sms/create-sms.md) ou [Push](../push/create-push.md) dans un parcours, la surface est désormais préremplie par défaut avec la dernière surface utilisée pour ce canal dans le parcours actuel.
* Vous pouvez désormais définir des paramètres de requête statiques ou dynamiques dans vos actions personnalisées. [En savoir plus](../action/about-custom-action-configuration.md#url-configuration).

**Créer des rapports**

* Vous pouvez désormais exporter des rapports Journey Optimizer en tant que PDF. [En savoir plus](../reports/global-report.md#export-reports).

**Concepteur de contenu**

* Le Concepteur de contenu d’Adobe Journey Optimizer a été mis à jour et l’accès aux styles et composants de conception est désormais plus facile. Cette nouvelle version offre une expérience client améliorée et s’accompagne de performances accrues, d’une compatibilité partielle du mode sombre et de nouvelles normes d’accessibilité.



## Notes de mise à jour de mars 2023 {#mar-2023}

### Nouvelles fonctionnalités{#mar-2023-features}

<table>
<thead>
<tr>
<th><strong>Canal in-app (Disponibilité générale)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais envoyer des messages in-app personnalisés aux utilisateurs et utilisatrices de votre application dans une campagne. Utilisez Journey Optimizer pour concevoir des notifications et personnaliser la mise en page, l’affichage, le texte et les boutons des messages afin de créer une expérience optimale.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>Pour plus d’informations, consultez la <a href="../in-app/get-started-in-app.md">documentation détaillée</a>.</p>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Suivi des clics dans les SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce au suivi des clics dans les SMS, vous pouvez surveiller les performances de vos URL raccourcies, identifier les clients et les clientes qui ont cliqué dessus et utiliser ces données pour les recibler dans vos campagnes ultérieures.</p>
<img src="assets/do-not-localize/sms-tracking.gif"/>
<p>Pour plus d’informations, consultez la <a href="../sms/create-sms.md#sms-content">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utiliser les balises dans les parcours (version Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>En tant qu’utilisateur ou utilisatrice de Journey Optimizer, vous pouvez désormais organiser vos objets commerciaux à l’aide de balises. Les balises constituent un moyen simple et rapide de classer des objets afin de faciliter leur recherche. Cette fonctionnalité est actuellement en version bêta et n’est disponible que pour les parcours.</p>
<p>Pour plus d’informations, consultez la <a href="../start/search-filter-categorize.md#tags">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#mar-2023-improvements}

**Parcours**

* La nouvelle **API de limitation** vous permet de limiter le nombre d’événements envoyés par seconde. Vous pouvez ainsi éviter les pics de trafic importants sur vos systèmes ou API externes. Lorsque la limite définie est atteinte, tous les appels API suivants sont placés en file d’attente et traités dès que possible, dans l’ordre dans lequel ils ont été reçus. Notez que cette fonctionnalité ne prend en charge qu’une seule configuration de limitation pour toutes vos sandbox. [En savoir plus](../configuration/external-systems.md).
* Amélioration de la zone de travail Parcours pour offrir une expérience utilisateur plus fluide et épurée. Suppression des espaces réservés vides à la fin de chaque chemin de la zone de travail. Vous pouvez maintenant simplement ajouter vos activités en les faisant glisser à la fin d’un chemin.
* Dans la zone de travail Parcours, la balise **Fin** n’est plus définie automatiquement avec le nom de l’activité précédente. Si nécessaire, les utilisateurs et utilisatrices peuvent indiquer un libellé personnalisé manuellement.
* Le délai d’expiration par défaut et la durée d’erreur dans les propriétés du parcours passent de 5 à 30 secondes. [En savoir plus](../configuration/external-systems.md#timeout).
* Le taux de limitation par défaut dans les activités de lecture de segment passe de 20 000 à 5 000 messages par seconde. [En savoir plus](../building-journeys/read-segment.md#configuring-segment-trigger-activity).
* Un mécanisme de sécurisation a été ajouté au mode test pour n’écouter que les événements envoyés via l’interface. Les événements envoyés par l’intermédiaire d’un outil externe ne sont pas pris en compte. [En savoir plus](../building-journeys/testing-the-journey.md)


<!-- 
* When adding an Email, SMS or Push action in a journey, the surface is now pre-filled, by default, with the last used surface for that channel.
* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)
* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)
* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->

**Gestion des décisions**

* Pour éviter toute confusion potentielle avec la version récente de la fonctionnalité des balises dans Adobe Experience Platform, les balises de gestion des décisions ont été renommées « qualificateurs de collection ».

   Notez que bien que le terme « balise » ne soit plus utilisé dans l’interface utilisateur de la gestion des décisions, il l’est toujours dans les services back-end, tels que les API et les jeux de données.

* Vous pouvez choisir de réinitialiser le compteur de limitation des offres tous les jours, toutes les semaines ou tous les mois. [En savoir plus](../offers/offer-library/add-constraints.md#capping).

* Vous pouvez également choisir l’événement Adobe Experience Platform à prendre en compte pour la limitation de la gestion des décisions. [En savoir plus](../offers/offer-library/add-constraints.md#capping).

* Des paramètres supplémentaires ont été ajoutés à l’écran de création d’emplacements. Ils vous permettent de contrôler si une offre peut être dupliquée à plusieurs emplacements et d’indiquer si le contenu et les métadonnées de l’offre doivent être inclus dans la réponse API. [En savoir plus](../offers/offer-library/creating-placements.md).

**Personnalisation**

* Vous pouvez désormais inclure un texte de remplacement par défaut dans les attributs de profil basés sur des chaînes de l’éditeur d’expression. Ces valeurs s’affichent si les attributs sélectionnés ne renvoient aucun résultat. [En savoir plus](../personalization/personalization-build-expressions.md#add).

**Créer des rapports**

* Amélioration de la fonctionnalité de widget de création de rapports et personnalisation de l’affichage des données des utilisateurs et utilisatrices. Grâce à cette amélioration, les utilisateurs et utilisatrices peuvent désormais choisir entre plusieurs options de visualisation, notamment les graphiques, les tableaux et les graphiques en anneau.

   Pour avoir accès aux derniers widgets, vous devrez réinitialiser les différents tableaux de bord de rapports. Pour plus d’informations sur la personnalisation des tableaux de bord, consultez la [documentation détaillée](../reports/global-report.md#modify-dashboard).

## Notes de mise à jour de février 2023 {#feb-2023}

### Nouvelles fonctionnalités{#feb-2023-features}

<table>
<thead>
<tr>
<th><strong>Canal in-app (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais envoyer des messages in-app personnalisés aux utilisateurs et utilisatrices de votre application dans une campagne. Utilisez Journey Optimizer pour concevoir des notifications et personnaliser la mise en page, l’affichage, le texte et les boutons des messages afin de créer une expérience optimale.</p>
<p><strong>Attention</strong> : cette fonctionnalité est actuellement en version bêta et disponible uniquement pour les clientes et clients bêta. Pour rejoindre le programme bêta, contactez l’assistance clientèle d’Adobe.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>Pour plus d'informations, consultez la <a href="../in-app/get-started-in-app.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Exporter des jeux de données Journey Optimizer vers des destinations d’espace de stockage (Beta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez maintenant établir une connexion active aux emplacements d’espace de stockage pour exporter le contenu de vos jeux de données. Les destinations disponibles sont les suivantes : espace de stockage Amazon S3, Blob Azure, Azure Data Lake Gen 2, zone d’atterrissage des données, Google Cloud Storage, SFTP.</p>
<p><strong>Attention</strong> : cette fonctionnalité est actuellement en version bêta et disponible uniquement pour les utilisateurs et utilisatrices d’Adobe Journey Optimizer. Contactez votre représentant ou représentante Adobe pour obtenir l’accès aux destinations si vous n’y avez pas déjà accès.</p>
<img src="assets/do-not-localize/gif-destinations.gif"/>
<p>Pour plus d’informations, consultez la <a href="../data/export-datasets.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<!--

<table>
<thead>
<tr>
<th><strong>Performance Measurement in campaigns</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now measure the performance of your campaigns across inbound and outbound through dedicated reports. Adobe Journey Optimizer reports can retrieve additional metrics to use in the <strong>Objective</strong> tab of your campaign reports. </p>
<img src="assets/do-not-localize/performance_report.gif"/>
<p>For more information, refer to the <a href="../privacy/data-hygiene.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>

+++ Learn more about Performance Measurement

The **[!UICONTROL Objective]** tab of your Campaign report allows you to better fine-tune your deliveries' reports by targeting one specific metric. With this feature, you can effectively track and analyze your campaign's performance and make informed decisions to improve your results.

The **[!UICONTROL Objectives]** listed are linked to **[!UICONTROL Datasets]** that define a connection to a system in order to retrieve additional information. A list of pre-configured **[!UICONTROL Objectives]** is available, but you can also customize your report by adding new **[!UICONTROL Datasets]** and defining your own objectives. 

By selecting the desired Objectives, the **[!UICONTROL Performance overview]** and **[!UICONTROL Campaign objective]** widgets provide a comprehensive and insightful summary of your delivery performance, allowing you to closely monitor and evaluate the success of your campaign.

With the **[!UICONTROL Campaign objective]** widget, you can also choose to compare your primary objective against another performance metric.

Note that each widget can be resized and deleted as needed.
+++




<table>
<thead>
<tr>
<th><strong>Use Tags in your Journeys</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>As a Journey Optimizer practitioner, you can now organize your business objects using tags. Tags are a quick and easy way of classifying objects to improve search. Tags are currently only available for Journeys.</p>
</td>
</tr>
</tbody>
</table>

-->

### Améliorations {#feb-2023-improvements}

**Parcours**

* Le champ **Période d’attente de reprise** a été ajouté aux propriétés du parcours. Ce champ vous permet de définir le temps d’attente avant d’autoriser un profil à entrer à nouveau dans le parcours en parcours unitaires (en commençant par un événement ou une qualification de segment). Cela empêche les parcours d’être déclenchés plusieurs fois par erreur pour le même événement. Par défaut, le champ est défini sur 5 minutes. [En savoir plus](../building-journeys/journey-gs.md#entrance).

* Des améliorations ont été apportées aux **dates de début et de fin de parcours**. Si vous n’avez pas spécifié de date de début, elle est désormais automatiquement ajoutée au moment de la publication. Pour les parcours **Lecture de segment**, vous pouvez désormais ajouter une date de fin. Cela permet aux profils de se fermer automatiquement lorsque la date est atteinte. [En savoir plus](../building-journeys/journey-gs.md#dates)

<!--

* The Journey canvas has been enhanced for a simpler and improved user experience. At the end of each path in the canvas, the empty placeholders have been removed. You can now simply add your activities by dragging them anywhere between nodes. [Learn more](../building-journeys/using-the-journey-designer.md)

* Timeout and error management has been improved in journeys. Timeout and error paths are now always added on the canvas. A new toolbar button is available to show/hide these paths. [Learn more](../building-journeys/journey-gs.md#timeout_and_error)

* A new type of system alert has been introduced. You can now get notified when a custom action fails. [Learn more](../reports/alerts.md)

* The Journey dashboard is now split in two tabs:
    * Use the **Overview** tab to access a new dashboard which displays key metrics related to your journeys.
    * Use the **Browse** tab to access list of all journeys.
-->


**Administration**

* **Liste autorisée** : vous pouvez désormais télécharger la liste autorisée sous la forme d’un fichier .csv. [En savoir plus](../configuration/allow-list.md#download-allowed-list).

* **Surface d’e-mail** : une vérification supplémentaire a été ajoutée aux paramètres de surface d’email. Si l’enregistrement MX pour le sous-domaine utilisé dans l’**adresse (e-mail) de réponse** ou dans l’**adresse e-mail en Cci** n’est pas correctement configuré, la surface d’email ne peut plus être créée. Vous devez le configurer ou en utiliser un autre. [En savoir plus](../email/email-settings.md#reply-to-email).

* **Surface d’email** : dans la section **Paramètres de suivi des URL** des paramètres de surface d’e-mail, la limite de chaque champ **Valeur** a été mise à jour de 255 caractères à 5 Ko pour des raisons de compatibilité avec le suivi Adobe Analytics. [En savoir plus](../email/email-settings.md#url-tracking)

**Gestion des décisions**

* **Emplacements** : ajout de paramètres supplémentaires à l’écran de création d’emplacements. Ils vous permettent de contrôler si une offre peut être dupliquée à plusieurs emplacements et d’indiquer si le contenu et les métadonnées de l’offre doivent être inclus dans la réponse API. [En savoir plus](../offers/offer-library/creating-placements.md).

* **Personnalisation des URL** : lorsque vous ajoutez des URL en tant que contenu aux représentations de vos offres, vous pouvez désormais personnaliser ces URL à l’aide de l’éditeur d’expression. [En savoir plus](../offers/offer-library/add-representations.md).

## Notes de mise à jour de janvier 2023{#jan-2023-release}

### Nouvelles fonctionnalités{#jan-2023-features}

<table>
<thead>
<tr>
<th><strong>Hygiène des données</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Experience Platform offre toute une gamme de fonctionnalités d’hygiène des données. Celles-ci vous permettent de gérer vos données stockées par le biais de suppressions programmées d’enregistrements et de jeux de données de consommateurs et consommatrices. Cette fonctionnalité est désormais disponible pour Adobe Journey Optimizer. </p>
<p>Vous pouvez gérer vos stocks de données pour vous assurer que les informations sont utilisées comme prévu, qu’elles sont mises à jour lorsque des données incorrectes doivent être corrigées et qu’elles sont supprimées lorsque les politiques d’entreprise le jugent nécessaire.</p>
<p><strong>Attention</strong> - Les fonctionnalités d’hygiène des données ne sont actuellement disponibles que pour les organisations qui ont acheté les offres complémentaires <strong>Healthcare Shield</strong> et <strong>Privacy and Security Shield</strong>.</p><p>Pour plus d’informations, consultez la <a href="../privacy/data-hygiene.md">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Modèles de contenu d’e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer des modèles de contenu autonomes qui peuvent être utilisés dans plusieurs parcours et campagnes pour une réutilisation rapide.</p> 
</p>
<img src="assets/do-not-localize/content-template.gif"/>
<p>Découvrez comment créer, modifier et utiliser des modèles de contenu dans <a href="https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/email-channel/content-templates.html?lang=fr">cette vidéo</a>. Pour plus d’informations, consultez la <a href="../email/content-templates.md">documentation détaillée</a>.
</p>
</td>
</tr>
</tbody>
</table>

### Améliorations {#jan-2023-improvements}

**Parcours**

* Lors de l’ajout d’une **Qualification de segment** ou **Lecture de segment** dans un parcours, l’espace de noms est maintenant prérempli par défaut avec le dernier espace de noms utilisé. Reportez-vous aux sections [Qualification de segment](../building-journeys/segment-qualification-events.md#about-segment-qualification) et [Lecture de segment](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Dans la zone de travail du parcours, un nouveau bouton est disponible dans la barre d’outils. Il permet de télécharger une copie d’écran de votre parcours.

**Concepteur d’e-mail**

* Vous pouvez désormais exporter le contenu de l’e-mail à partir du menu **Exporter le HTML**. Les fichiers exportés sont disponibles dans un fichier d’archive (.ZIP).

**Administration**

* Une nouvelle sous-section fournit des recommandations sur la création de l’adresse **Répondre à (e-mail)** et sur la garantie d’une gestion adéquate des réponses. [En savoir plus](../email/email-settings.md#reply-to-email)

* Lors de la création ou de la modification des **Groupes d’adresses IP**, les enregistrements PTR associés sont désormais affichés dans la liste des adresses IP et lorsque vous passez la souris sur les adresses IP sélectionnées. [En savoir plus](../configuration/ip-pools.md#create-ip-pool)

* Une fois qu’un groupe d’adresses IP a été sélectionné dans la surface d’un canal, les informations d’enregistrement PTR sont désormais visibles lorsque vous passez la souris sur les adresses IP. [En savoir plus](../email/email-settings.md#subdomains-and-ip-pools)

* L’interface utilisateur pour la modification des [enregistrements PTR](../configuration/ptr-records.md#edit-ptr-record) et des [champs d’exécution](../configuration/primary-email-addresses.md) a été mise à jour.

* L’interface utilisateur de création et de modification des sous-domaines a été améliorée. [En savoir plus](../configuration/delegate-subdomain.md)

* La liste de suppression de l’écran **Téléchargements récents** a été mise à jour. [En savoir plus](../configuration/manage-suppression-list.md#recent-uploads)

**Campagnes**

* Un exemple de requête cURL permettant l’exécution de campagnes déclenchées par l’API est désormais généré automatiquement et rendu disponible dans l’écran de la campagne. [En savoir plus](../campaigns/api-triggered-campaigns.md)


**Personnalisation**

* De nouvelles fonctions d’assistance sont disponibles : formatCurrency, charCodeAt, stringToDate, toString, formatNumber et toHexString. De plus, la fonction toDateTimeOnly accepte désormais les types de champs chaîne, date, long et int. [En savoir plus](../personalization/functions/functions.md)
