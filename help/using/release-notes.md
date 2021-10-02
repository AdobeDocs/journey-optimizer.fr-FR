---
title: Notes de mise à jour
description: Notes de mise à jour de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 7c02f27f0160aea2c2f55c7dc5a8e7c3de3ac159
workflow-type: tm+mt
source-wordcount: '1529'
ht-degree: 70%

---

# Notes de mise à jour {#release-notes}

Cette page répertorie toutes les nouvelles fonctionnalités et améliorations d&#39;[!DNL Journey Optimizer]. Vous pouvez également consulter les dernières [mises à jour de la documentation](documentation-updates.md).



## Version de septembre 2021 {#september-2021-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>

<th><strong>Création de rapports - Meilleures informations sur l’audience ciblée</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>De nouvelles mesures sont disponibles dans les rapports : Les messages ciblés et exclus pour les emails et les notifications push sont visibles dans les rapports en ligne et globaux. </br> Pour avoir accès aux dernières mesures, vous devrez réinitialiser les différents tableaux de bord de rapports pour chaque canal et type de rapport. Pour plus d’informations sur la personnalisation des tableaux de bord, consultez la <a href="reports/live-report.md">documentation détaillée.</a></p>
<p>Une nouvelle colonne de la liste d'exécution des messages affiche le nombre de profils ciblés pour chaque exécution du message. </p>
<p>Pour plus d'informations, consultez la <a href="message-monitoring.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>Transmission dynamique de listes de données à l’aide d’actions personnalisées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais transmettre des collections ou une liste de données dans vos paramètres d’action personnalisés qui seront renseignés dynamiquement au moment de l’exécution. Deux types de collections sont pris en charge : collections simples et collections d’objets. Les actions personnalisées créées précédemment continueront à fonctionner. </p>
<p>Pour plus d’informations sur les collections, consultez la <a href="building-journeys/collections.md">documentation détaillée</a>. </p>
<p>Les fonctions de filtre et d’intersection ont été ajoutées à la liste des fonctions disponibles dans l’éditeur d’expression avancé. Cela offre davantage de possibilités de filtrage et de comparaison des collections.</p>
<p>Consultez la documentation sur les fonctions <a href="https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/main-functions-journey/list/functionfilter.html">filter</a> et <a href="https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/main-functions-journey/list/functionintersect.html">intersect</a> .</p>
</td>
</tr>
</tbody>
</table>

<!--
<table>
<thead>
<tr>
<th><strong>Decision Management - Personalize your offers</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>You can now personalize content added to your offers' representations using the expression editor.</p>
<p>For more information, refer to the <a href="offers/offer-library/creating-personalized-offers.md#content">detailed documentation</a>.</p>
</td>
</tr>
</tbody>
</table>
-->

### Améliorations

**Parcours**

* Les schémas et les jeux de données générés par le système qui ont été créés pendant la mise en service des événements d’étape sont désormais en lecture seule, ce qui permet d’éviter toute modification involontaire des schémas critiques. [En savoir plus](reports/sharing-overview.md)
* Libellez de manière claire l’activité **Attente** avec un libellé qui s’affichera dans la zone de travail. Le libellé est également utilisé dans les journaux des modes de reporting et de test pour identifier clairement ce que vous faites. [En savoir plus](building-journeys/about-journey-activities.md#best-practices)
* Trouvez plus rapidement vos événements et actions en filtrant les éléments dans les catégories **Événements** et **Action** à l’aide de la recherche. Les activités d’orchestration ne sont plus filtrées. [En savoir plus](building-journeys/using-the-journey-designer.md)
* Lors de la définition d’une condition d’identifiant d’événement dans un événement d’entreprise ou basé sur des règles, l’opérateur &quot;contient&quot; est désormais disponible pour les types de chaînes de champs. [En savoir plus](event/about-creating.md)

**Configuration des e-mails**

* Lorsqu’un pool d’adresses IP a été associé à un paramètre prédéfini de message, vous pouvez désormais le modifier, la mise à jour étant asynchrone. Vous pouvez également vérifier l’état de chaque mise à jour du pool d’adresses IP. [En savoir plus](configuration/ip-pools.md#edit-ip-pool)

## Version d’août 2021 {#august-2021-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>

<th><strong>Envoi des messages au meilleur moment - Optimisation de l’heure d’envoi</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Envoyez automatiquement vos notifications push ou vos e-mails au meilleur moment pour chaque client avec Adobe Journey Optimizer. L’optimisation de l’heure d’envoi, optimisée par les services d’IA d’Adobe, prédit le meilleur moment pour envoyer un e-mail ou un message push afin d’optimiser l’engagement en fonction des taux d’ouverture et de clics historiques prêts à l’emploi.</p>
<p>Cette fonctionnalité est actuellement en version bêta et disponible uniquement pour les clients bêta. Pour rejoindre le programme bêta, contactez l’assistance clientèle d’Adobe.</p>
<p>Pour plus d'informations, consultez la <a href="building-journeys/journeys-message.md#send-time-optimization">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>

<th><strong>Exploitation des relations de schémas dans les événements métier - Gestion des tables de recherche</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais tirer profit des relations entre les schémas lors de la configuration d’événements métier. Cela s’ajoute à la possibilité d’exploiter des champs de tables liées lors de la configuration d’un événement unitaire, lors de l’utilisation de conditions dans un parcours, dans la personnalisation des messages et dans la personnalisation d’une action personnalisée.</p>
<p>Pour plus d'informations, consultez la <a href="event/experience-event-schema.md#leverage_schema_relationships">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>URL personnalisées</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Les URL personnalisées orientent les destinataires vers des pages spécifiques d'un site web ou vers un microsite personnalisé, en fonction des attributs du profil. Dans Adobe Journey Optimizer, vous pouvez désormais ajouter une personnalisation aux URL dans le contenu de votre message. La personnalisation de l'URL peut être appliquée au texte et aux images, et utiliser les données de profil ou les données contextuelles.</p>
<p>Pour plus d'informations, consultez la <a href="personalization/personalization-syntax.md#perso-urls">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>Assurance que vos e-mails parviennent à vos utilisateurs - Reprise d’e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez maintenant définir la période de reprise en vous basant sur un préréglage afin de vous assurer que les tentatives de reprise ne sont plus exécutées lorsqu’elles ne sont plus nécessaires. Par exemple, vous pouvez définir la période de reprise sur 24 heures pour un message transactionnel réinitialisé par mot de passe contenant un lien valide seulement pendant une journée. Notez que les paramètres de reprise s’appliquent uniquement au canal e-mail.</p>
<p>Pour plus d'informations, consultez la <a href="configuration/retries.md#retry-duration">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Définir des adresses à exclure de l'envoi - Liste de suppression</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’ajout d’adresses et de domaines de messagerie dans la liste de suppression est désormais disponible dans l’interface utilisateur, une par une, ou en masse via un téléchargement de fichier CSV.</p>
<p>Pour plus d'informations, consultez la <a href="configuration/manage-suppression-list.md#add-addresses-and-domains">documentation détaillée</a>.</p>
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

* **En-têtes dynamiques** : vous pouvez désormais transmettre des données dynamiques dans les paramètres d’en-tête HTTP. Ces paramètres peuvent être utilisés par les systèmes d’intégration qui reçoivent les appels HTTP de l’action de parcours, par exemple l’horodatage ou l’ID de suivi. [En savoir plus](action/about-custom-action-configuration.md#url-configuration)
* **Chemins d’URL dynamiques** : vous pouvez désormais configurer des chemins d’URL dynamiques pour les actions personnalisées. [En savoir plus](action/about-custom-action-configuration.md#url-configuration)
* Le taux de limitation global pour les segments lus a été modifié de 17 000 à 20 000 messages par seconde. [En savoir plus](building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Interface utilisateur**

* **Rechercher** : sur chaque page, vous pouvez désormais rechercher des objets métier et des articles d’aide directement dans le champ de recherche Unified Experience Cloud. [En savoir plus](user-interface.md#unified-search)
* **Récents** : l’affichage des éléments récents de la page d’accueil d’Adobe Journey Optimizer est désormais étendu aux objets métier supplémentaires. Grâce à cette mise à jour, les raccourcis vers vos accès récents comprennent les messages, les parcours, les segments, les schémas, les jeux de données, les sources de données, les événements, les actions, les sources et les destinations. [En savoir plus](action/about-custom-action-configuration.md#passing-collection)

**Conception de contenu**

* **Arrière-plan** : les images d’arrière-plan sont désormais prises en charge dans l’aperçu dynamique. [En savoir plus](preview.md)
* **Lien d’exclusion en un clic** : vous pouvez insérer un nouveau type de lien dans le contenu de votre e-mail : le lien d’**exclusion** permet aux utilisateurs de se désabonner de la réception de vos communications en un seul clic, sans être redirigé vers une landing page pour confirmer leur désinscription. [En savoir plus](message-tracking.md#one-click-opt-out-link)

**Personnalisation**

* **Éditeur d’expression**  : vous pouvez désormais facilement ajouter une valeur de secours lors de la définition de la personnalisation : lorsque le champ de personnalisation est vide pour un profil, la valeur de retour arrière s’affiche. [En savoir plus](personalization/functions/helpers.md)

**Configuration des e-mails**

* **Liste autorisée** : la liste autorisée peut désormais être activée et désactivée sur un environnement de test hors production via un appel API. [En savoir plus](allow-list.md#enable-allow-list)
* **Navigation**  : la liste de suppression, accessible sous  **Administration > Canaux > Configuration des emails >** Menu général, a été déplacée vers le nouveau sous-menu  **Liste de suppression** , qui rassemble toutes les fonctionnalités associées pour un accès plus facile. [En savoir plus](configuration/manage-suppression-list.md#access-suppression-list)

**Gestion des décisions**

* La manière dont vous ajoutez et configurez des représentations lors de la création d&#39;une offre a été mise à jour pour améliorer l&#39;expérience utilisateur. En particulier, la bibliothèque de ressources s&#39;affiche désormais uniquement lorsque vous définissez du contenu de type image pour une représentation. [En savoir plus](offers/offer-library/creating-personalized-offers.md#representations)

### Correctifs

* Correction d’un problème d’accessibilité dans la navigation par onglets des messages.
* Correction d’un problème de localisation dans les libellés du concepteur d’e-mails.
* Correction d’un problème lors de la sélection de plusieurs nœuds dans un parcours et du clic sur « Supprimer » dans le panneau des propriétés.
* Correction d’un problème qui empêchait l’ajout d’un nouvel en-tête à une action utilisée dans un parcours.
* Vous pouvez maintenant découvrir la raison pour laquelle la création d’un préréglage de message a échoué via un avertissement plus explicite dans l’interface utilisateur.


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
<p>Vous pouvez désormais tirer profit des relations entre les schémas afin d’utiliser un jeu de données comme table de recherche pour un autre. Vous pouvez ensuite exploiter tous les champs des tables liées lors de la configuration d’un événement unitaire, lors de l’utilisation de conditions dans un parcours, dans la personnalisation des messages et dans la personnalisation d’une action personnalisée.</p>
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
* Correction d’un problème dans le concepteur d’e-mails lors du téléchargement d’un fichier HTML en raison duquel la feuille de style interne avec la propriété `background-image` n’était pas prise en charge.
