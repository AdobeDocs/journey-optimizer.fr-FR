---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
description: Notes de mise à jour de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 416da542b6e0ea8c66cdcebcc0219db63a9608fb
workflow-type: tm+mt
source-wordcount: '1317'
ht-degree: 81%

---

# Notes de mise à jour {#release-notes}

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour.

Les notes de mise à jour précédentes sont disponibles sur [cette page](release-notes-2022.md). Vous pouvez également consulter la page relative aux [dernières mises à jour de la documentation](documentation-updates.md) pour prendre connaissance des autres modifications.

[!DNL Adobe Journey Optimizer] est créé de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.

![Newsletter](../assets/do-not-localize/nl-icon.png) Inscrivez-vous à la [newsletter trimestrielle d’Adobe Journey Optimizer](https://www.adobe.com/subscription/Adobe_Journey_Optimizer_NL.html){target="_blank"} dès aujourd’hui, et recevez les dernières mises à jour produits, les articles les plus intéressants, des cas pratiques, des conseils et bien plus encore, directement dans votre boîte de réception, tous les trimestres.


## Notes de mise à jour de mars 2023 {#mar-2023}

Les informations ci-dessous peuvent être modifiées sans préavis jusqu’à la date de disponibilité de la version. La documentation mise à jour sera publiée à la date de publication et des liens directs seront ajoutés à cette page.


### Nouvelles fonctionnalités{#mar-2023-features}

<!--
<table>
<thead>
<tr>
<th><strong>In-app channel (General Availability)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now send personalized In-app messages to your app users within a campaign. Use Journey Optimizer to design notifications and customize the message layout, display, text, and buttons to create a seamless experience.</p>
<img src="assets/do-not-localize/in-app.gif"/>
<p>For more information, refer to the <a href="../in-app/get-started-in-app.md">detailed documentation</a>.</p>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Suivi des clics SMS</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Grâce au suivi des clics SMS, vous pouvez surveiller les performances de vos URL raccourcies, identifier qui a cliqué dessus et utiliser ces données pour recibler ces clients avec les campagnes suivantes.</p>
<img src="assets/do-not-localize/sms-tracking.gif"/>
<p>Pour plus d’informations, consultez la <a href="../sms/create-sms.md#sms-content">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Utilisation des balises dans vos Parcours (version bêta)</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>En tant qu’utilisateur ou utilisatrice de Journey Optimizer, vous pouvez désormais organiser vos objets commerciaux à l’aide de balises. Les balises constituent un moyen simple et rapide de classer des objets afin de faciliter leur recherche. Cette fonctionnalité est actuellement en version bêta et n’est disponible que pour les parcours.</p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/tags.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


### Améliorations {#mar-2023-improvements}

**Parcours**

* La nouvelle **API de limitation** vous permet de définir une limite au nombre d’événements envoyés par seconde, ce qui empêche des pics de trafic écrasants sur vos systèmes ou API externes. Lorsque la limite définie est atteinte, tous les appels API suivants sont placés en file d’attente et traités dès que possible, dans l’ordre dans lequel ils ont été reçus. Notez que cette fonctionnalité ne prend en charge qu’une seule configuration de limitation pour tous vos environnements de test. [En savoir plus](../configuration/external-systems.md).
* Le canevas de Parcours a été amélioré pour une expérience utilisateur plus simple et améliorée. À la fin de chaque chemin dans la zone de travail, les espaces réservés vides ont été supprimés. Vous pouvez maintenant simplement ajouter vos activités en les faisant glisser à la fin d’un chemin.
* Dans la zone de travail du parcours, le libellé de la propriété **Fin** n’est plus définie automatiquement avec le nom de l’activité précédente. Si nécessaire, les utilisateurs peuvent ajouter manuellement une étiquette personnalisée.
* Le délai d’expiration par défaut et la durée d’erreur dans les propriétés du parcours ont été modifiés de 5 à 30 secondes. [En savoir plus](../configuration/external-systems.md#timeout).
* Le taux de ralentissement par défaut dans les activités de segments lus a été modifié de 20 000 à 5 000 messages par seconde. [En savoir plus](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

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

<!--* Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)-->

<!--**Personalization**

* You can now include default fallback text for string-based profile attributes in the Expression Editor. These values will display if the selected attributes return no result. [Learn more](../personalization/personalization-build-expressions.md#add)-->

<!--
**Reporting**

* The reporting widget functionality has been improved with the ability to customize how users view their data. With this improvement, users can now choose between multiple visualization options, including graph, table, and donut charts.

    To have access to the latest widgets, please note that you will have to reset the different reporting dashboards. For more information on dashboard customization, refer to the [detailed documentation](../reports/global-report.md#modify-dashboard).
-->

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
<th><strong>Exporter des jeux de données Journey Optimizer vers des destinations d’espace de stockage (Beta)</strong><br/></th>
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

* **Surface d’e-mail** : une vérification supplémentaire a été ajoutée aux paramètres de surface d’email. Si l’enregistrement MX pour le sous-domaine utilisé dans l’**adresse (e-mail) de réponse** ou dans l‘**adresse e-mail en Cci** n’est pas correctement configuré, la surface d’email ne peut plus être créée. Vous devez le configurer ou en utiliser un autre. [En savoir plus](../email/email-settings.md#reply-to-email).

* **Surface d’email** : dans la section **Paramètres de suivi des URL** des paramètres de surface d’e-mail, la limite de chaque champ **Valeur** a été mise à jour de 255 caractères à 5 Ko pour des raisons de compatibilité avec le suivi Adobe Analytics. [En savoir plus](../email/email-settings.md#url-tracking)

**Gestion des décisions**

<!--
* **Placements** - Additional parameters have been added in placements creation screen. They allow you to control whether an offer can be duplicated across multiple placements, and to specify if the offer's content and metadata should be included in the API response. [Learn more](../offers/offer-library/creating-placements.md)
-->

* **Personnalisation des URL** : lorsque vous ajoutez des URL en tant que contenu aux représentations de vos offres, vous pouvez désormais personnaliser ces URL à l’aide de l’éditeur d’expression. [En savoir plus](../offers/offer-library/add-representations.md).

## Version de janvier 2023 {#jan-2023-release}

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
<p>Vous pouvez gérer vos stocks de données pour vous assurer que les informations sont utilisées comme prévu, qu’elles sont mises à jour lorsque des données incorrectes doivent être corrigées et qu’elles sont supprimées lorsque les stratégies d’entreprise le jugent nécessaire.</p>
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
