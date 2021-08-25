---
title: Notes de mise à jour
description: Notes de mise à jour de Journey Optimizer
source-git-commit: 77d392cc09bd0923faf3d27e951a17cd702d257c
workflow-type: tm+mt
source-wordcount: '967'
ht-degree: 38%

---


# Notes de mise à jour {#release-notes}

Cette page répertorie toutes les nouvelles fonctionnalités et améliorations d&#39;[!DNL Journey Optimizer]. Vous pouvez également consulter les dernières [mises à jour de la documentation](documentation-updates.md).


## Version d’août 2021 {#august-2021-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>

<th><strong>Envoyer des messages au meilleur moment - Optimisation de l’heure d’envoi</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Envoyez automatiquement vos notifications push ou vos e-mails au meilleur moment pour chaque client avec Adobe Journey Optimizer. L’optimisation du temps d’envoi, optimisée par les services d’IA d’Adobe, prédit le meilleur moment pour envoyer un email ou un message push afin d’optimiser l’engagement en fonction des taux d’ouverture et de clics historiques prêts à l’emploi.</p>
<p>Cette fonctionnalité est actuellement en version bêta et disponible uniquement pour les clients bêta. Pour rejoindre le programme bêta, contactez l’assistance clientèle d’Adobe.</p>
<p>Pour plus d'informations, consultez la <a href="building-journeys/journeys-message.md#send-time-optimization">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>Tirer parti des relations de schémas dans les événements métier - Gestion des tables de recherche</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais tirer parti des relations entre les schémas lors de la configuration d’événements professionnels. Cela s’ajoute à la possibilité d’exploiter des champs des tables liées lors de la configuration d’un événement unitaire, lors de l’utilisation de conditions dans un parcours, dans la personnalisation des messages et dans la personnalisation d’une action personnalisée.</p>
<p>Pour plus d'informations, consultez la <a href="event/experience-event-schema.md#leverage_schema_relationships">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>
<!--
<table>
<thead>
<tr>
<th><strong>Personalized URLs</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Personalized URLs take recipients to specific pages of a website, or to a personalized microsite, depending on the profile attributes. In Adobe Journey Optimizer, you can now add personalization to URLs in your message content. URL personalization can be applied to text and images, and use profile data or contextual data.</p>
<p>For more information, refer to the <a href="documentation-updates.md">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

<table>
<thead>
<tr>
<th><strong>Assurez-vous que vos emails parviennent à vos utilisateurs - Réessayer par email</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez maintenant définir la période de reprise sur une base par paramètre prédéfini afin de vous assurer que les tentatives de reprise ne sont plus exécutées lorsqu’elles ne sont plus nécessaires. Par exemple, vous pouvez définir la période de reprise sur 24 heures pour un message transactionnel réinitialisé par mot de passe contenant un lien valide seulement pendant une journée. Notez que les paramètres de reprise s’appliquent uniquement au canal email.</p>
<p>Pour plus d'informations, consultez la <a href="configuration/retries.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>
<!--
<table>
<thead>
<tr>
<th><strong>Customer Alerts</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now subscribe to event-based alerts regarding Adobe Journey Optimizer activities. The user interface allows you to view a history of received alerts based on metrics revealed by Adobe Experience Platform Observability Insights. The UI also allows you to view, enable, and disable available alert rules.</p>
<p>This feature is currently in beta version and only available to beta customers. To join the beta program, contact Adobe Customer Care.
</p>
<p>For more information, refer to the <a href="https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html">Adobe Experience Platform documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

### Améliorations

**Parcours**

* **En-têtes dynamiques**  : vous pouvez désormais transmettre des données dynamiques dans les paramètres d’en-tête HTTP. Ces paramètres peuvent être utilisés par les systèmes d’intégration qui reçoivent les appels HTTP de l’action de parcours, par exemple l’horodatage ou l’ID de suivi. [En savoir plus](action/about-custom-action-configuration.md#url-configuration)
* **Chemins d’URL dynamiques**  : vous pouvez désormais configurer des chemins d’URL dynamiques pour les actions personnalisées. [En savoir plus](action/about-custom-action-configuration.md#url-configuration)
* Le taux de ralentissement global pour les segments lus a été modifié de 17 000 à 20 000 messages par seconde. [En savoir plus](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Interface utilisateur**

* **Rechercher**  : sur chaque page, vous pouvez désormais rechercher des objets commerciaux et des articles d’aide directement dans le champ de recherche Experience Cloud unifié. [En savoir plus](user-interface.md#unified-search)
* **Récents**  : l’affichage des éléments récents de la page d’accueil de Adobe Journey Optimizer est désormais étendu aux objets commerciaux supplémentaires. Grâce à cette mise à jour, les raccourcis vers vos accès récents comprennent les messages, les Parcours, les segments, les schémas, les jeux de données, les sources de données, les événements, les actions, les sources et les destinations. [En savoir plus](action/about-custom-action-configuration.md#passing-collection)

**Conception de contenu**

* **Arrière-plan**  : les images d’arrière-plan sont désormais prises en charge dans l’aperçu en direct. [En savoir plus](preview.md)
* **Lien d’exclusion en un clic**  : vous pouvez insérer un nouveau type de lien dans le contenu de votre email : le lien  **Opt-** outlink permet aux utilisateurs de se désabonner de la réception de vos communications en un seul clic, sans être redirigé vers une landing page pour confirmer leur désinscription. [En savoir plus](message-tracking.md#one-click-opt-out-link)

**Personnalisation**

<!--* **Expression Editor** - You can now easily add a fall-back value when defining personalization: when personalization field is empty for a profile, the fall-back value will display. [Learn more](documentation-updates.md)-->

**Configuration des e-mails**

* **Liste autorisée**  : la liste autorisée peut désormais être activée et désactivée sur un environnement de test hors production via un appel API. [En savoir plus](allow-list.md#enable-allow-list)

<!--* **Suppression list** - Adding email addresses and domains into the suppression list is now available from the user interface, either one by one, either in bulk mode through a CSV file upload. [Learn more](configuration/manage-suppression-list.md#add-addresses-and-domains)-->
<!--* **Navigation** - The suppression list, which was accessible under the **Channels > Email configuration > General** menu, has been moved to the **Channels > Email configuration > Suppression list** menu for easier access. [Learn more](configuration/manage-suppression-list.md#access-suppression-list)-->


### Correctifs

* Correction d’un problème d’accessibilité dans la navigation par onglets des messages.
* Correction d’un problème de localisation dans les étiquettes du concepteur d’emails.
* Correction d’un problème lors de la sélection de plusieurs noeuds dans un parcours et du clic sur &quot;Supprimer&quot; dans le panneau des propriétés.
* Correction d’un problème qui empêchait l’ajout d’un nouvel en-tête à une action utilisée dans un parcours.
* Vous pouvez maintenant découvrir la raison pour laquelle la création d’un paramètre prédéfini de message a échoué via un avertissement plus explicite dans l’interface utilisateur.


## Version de juillet 2021 {#july-2021-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>
<th><strong>Utilisation des métadonnées dans vos messages - Gestion des tables de recherche</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Enrichissez vos expériences avec les données de référence que vous avez chargées dans Journey Optimizer. Par exemple, la recherche de métadonnées sur un ID de réservation dans un événement d’expérience ou la recherche d’informations sur un produit à partir d’un SKU dans un événement d’expérience à utiliser dans la zone de travail. </p>
<p>Vous pouvez désormais tirer parti des relations entre les schémas afin d’utiliser un jeu de données comme table de recherche pour un autre. Vous pouvez ensuite exploiter tous les champs des tables liées lors de la configuration d’un événement unitaire, lors de l’utilisation de conditions dans un parcours, dans la personnalisation des messages et dans la personnalisation de l’action personnalisée.</p>
<p>Pour plus d'informations, consultez la <a href="event/experience-event-schema.md#leverage_schema_relationships">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Liste autorisée</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez maintenant définir une liste d'envoi sécurisé spécifique au niveau de l'environnement Sandbox, afin d'avoir un environnement sécurisé à des fins de test. Sur une instance hors production, où des erreurs peuvent se produire, la liste autorisée garantit que vous n'avez aucun risque d'envoyer des messages indésirables à vos clients. Cette fonctionnalité est activée en utilisant les API de suppression.</p>
<p>Pour plus d'informations, consultez la <a href="allow-list.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations

**Parcours**

* Le taux de limitation global de toutes les lectures de segment qui s&#39;exécutent simultanément dans le même environnement Sandbox est limité à 17 000 messages par seconde. [En savoir plus](building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Le champ **Durée de mise en cache** a été supprimé du panneau de configuration de la source de données. [En savoir plus](datasource/about-data-sources.md)
* Pour les sources de données externes, une règle de limitation de 15 appels par seconde est maintenant définie automatiquement. [En savoir plus](configuration/external-systems.md#capping)
* Pour les parcours actifs, l’écran des propriétés du parcours affiche la date de publication et le nom de l’utilisateur qui a publié le parcours. [En savoir plus](building-journeys/journey-gs.md#change-properties)
* Dans l&#39;écran Liste des parcours, le filtre de type de parcours a été ajouté. [En savoir plus](user-interface.md#section_lgm_hpz_pgb)
* Le paramètre **[!UICONTROL Taux de limitation]** a été ajouté à l&#39;activité Lecture de segment. [En savoir plus](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Prévisualiser et tester les messages**

* L&#39;identité et l&#39;espace de noms sont maintenant visibles dans l&#39;écran **[!UICONTROL Aperçu]**. [En savoir plus](preview.md#preview-your-messages)
* Le nombre d&#39;e-mails de test pour les BAT est maintenant limité à 10.
* Les caractères autorisés pour le **préfixe de ligne d&#39;objet** dans les BAT sont maintenant limités. [En savoir plus](preview.md#send-proofs)

**Personnalisation de l&#39;éditeur d&#39;expression**

* La liste déroulante des helpers a été renommée et réorganisée.

### Correctifs

* Correction d&#39;un problème qui entraînait la diffusion de messages en double pour la diffusion d&#39;e-mails par lots.
* Les événements sont maintenant générés en conséquence lorsque l&#39;envoi d&#39;e-mails n&#39;est pas effectué une fois la période de reprise terminée.
* Correction d&#39;un problème en raison duquel les informations IP manquaient dans l&#39;écran Enregistrements PTR.
* La localisation est maintenant implémentée dans le rail des offres au sein de l&#39;éditeur d&#39;expression.
* Correction d&#39;un espacement incorrect dans les fenêtres contextuelles d&#39;informations.
* Correction d’un problème dans le concepteur d’emails lors du téléchargement d’un fichier HTML en raison duquel la feuille de style interne avec la propriété `background-image` n’était pas prise en charge.

