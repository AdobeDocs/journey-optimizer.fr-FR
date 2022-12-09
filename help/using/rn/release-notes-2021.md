---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour précédentes (2021)
description: Notes de mise à jour de Journey Optimizer 2021
exl-id: 0e43be98-f471-4860-be84-8f99ab93e983
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '2077'
ht-degree: 0%

---

# Notes de mise à jour 2021 {#release-notes-2021}

Cette page répertorie toutes les fonctionnalités et améliorations pour [!DNL Journey Optimizer] publié en 2021.


## Version de novembre 2021 {#november-2021-release}

<table>
<thead>
<tr>
<th><strong>Délégation de sous-domaine CNAME</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer prend désormais en charge les CNAME. Un enregistrement CNAME, ou nom canonique, est un enregistrement qui pointe vers une autre adresse de domaine plutôt qu’une adresse IP. La délégation de sous-domaine CNAME vous permet de créer un sous-domaine et d’utiliser des CNAME pour pointer vers des enregistrements spécifiques à Adobe. Grâce à cette configuration, vous partagez avec Adobe la responsabilité de la maintenance du DNS afin de configurer un environnement pour l’envoi, le rendu et le suivi des emails.</p>
<p>Cette méthode est recommandée si les stratégies de votre entreprise limitent la méthode de délégation de sous-domaine complète.</p>
<p>En savoir plus sur la délégation de sous-domaine CNAME dans <a href="../configuration/delegate-subdomain.md#cname-subdomain-delegation">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


## Version d’octobre 2021 {#oct-2021-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>
<th><strong>Gestion des décisions - Simulation des offres</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais simuler les offres qui seront diffusées à un profil de test pour un emplacement donné dans l’interface utilisateur de Journey Optimizer. Cela vous permet de valider facilement votre logique de prise de décision, y compris les contraintes d’éligibilité et les algorithmes de classement avant de les mettre en production. Cette fonctionnalité permet aux utilisateurs non techniques et techniques de tester rapidement la gestion des décisions et de résoudre les problèmes potentiels.</p>
<p>Pour plus d’informations, reportez-vous à la section <a href="../offers/offer-activities/simulation.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gestion des décisions - Personnaliser vos offres</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais personnaliser le contenu de vos offres à l’aide des attributs de profil et des segments Adobe Experience Platform à l’aide du même composant d’éditeur d’expression que celui de l’interface utilisateur de Journey Optimizer. </p>
<p>Pour plus d’informations, reportez-vous à la section <a href="../offers/offer-library/creating-personalized-offers.md#custom-text">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


Voir aussi [Notes de mise à jour d’octobre d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/2021/october-2021.html){target=&quot;_blank&quot;} pour effectuer d’autres modifications.

### Améliorations

**Parcours**

* **Editeur d&#39;expression** - En tant qu’utilisateur avancé, vous pouvez désormais utiliser des fonctions pour travailler avec des cartes. Cette fonctionnalité peut être utilisée avec les listes d’abonnements. Par exemple, à partir d’un segment, vous pouvez désormais obtenir une adresse électronique à partir d’une liste d’abonnements. [En savoir plus dans cet exemple](../building-journeys/message-to-subscribers-uc.md)

* **Surveillance** - Les événements d’étape pour les parcours actifs et le mode test ont été améliorés. [Nouveaux champs](../reports/sharing-field-list.md#serviceevents) ont été ajoutés en rapport avec les traitements d&#39;export de profil. Pour une meilleure expérience utilisateur, les champs d’événement d’étape sont désormais organisés en différentes catégories. Tous les champs d’événements d’étape précédente sont toujours disponibles dans la variable [stepEvents](../reports/sharing-legacy-fields.md) catégorie.
* **Accessibilité** - Des améliorations de l’accessibilité ont été apportées aux parcours.
* **Collections** - Les tableaux d’objets contenant des sous-objets sont désormais pris en charge. [En savoir plus](../building-journeys/collections.md)
* **Listes** - Les écrans de liste ont été améliorés pour les parcours, les événements, les actions et les sources de données.

**Reporting**

* **Format des données dans la vue globale** - Vous pouvez désormais basculer entre les nombres et les pourcentages dans la variable **Vue globale** de **Exécution** .


**Administration**

* **Modifier les paramètres prédéfinis de message** - Vous pouvez désormais modifier les paramètres prédéfinis de message et surveiller leur état de mise à jour. [En savoir plus](../configuration/channel-surfaces.md#edit-channel-surface)
* **Modification des enregistrements PTR** - Vous pouvez désormais modifier les enregistrements PTR et surveiller leur état de mise à jour. [En savoir plus](../configuration/ptr-records.md#edit-ptr-record)

**Personnalisation**

* **Nouvelle fonction d’assistance pour le formatage des dates** - Vous pouvez maintenant spécifier comment une chaîne de date doit être représentée. [En savoir plus](../personalization/functions/dates.md#format-date)


**Gestion des décisions**

* **Séquencement des évaluations** - Le nouveau flux de création de décision, amélioré, vous permet non seulement de naviguer plus facilement entre les objets de décision, mais également de contrôler entièrement la manière dont les collections d’offres sont évaluées par le moteur de décision. Cela inclut les collections qui sont évaluées ensemble ou séparément, et dans quel ordre les collections doivent être évaluées. [En savoir plus](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

### Correctifs

* Correction d’un problème qui empêchait l’affichage de la liste Parcours, de la liste des messages et du Concepteur d’email lorsque la langue du navigateur n’était pas l’anglais.
* Correction d&#39;une erreur de syntaxe qui se produisait lors de l&#39;ajout d&#39;une personnalisation à l&#39;aide d&#39;une expression dans le Concepteur d&#39;email : Les caractères étaient échappés par erreur.
* Correction d’un problème qui entraînait une erreur 404 lors de la navigation dans la variable **Administration** .
* Correction d’un problème qui déclenchait d’autres parcours actifs lors du test d’un parcours à l’aide d’un événement d’entreprise.


## Version de septembre 2021 {#september-2021-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>

<th><strong>Création de rapports - Meilleures informations sur l’audience ciblée</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>De nouvelles mesures sont disponibles dans les rapports : Les messages ciblés et exclus pour les emails et les notifications push sont visibles dans les rapports en ligne et globaux. </br> Pour avoir accès aux dernières mesures, vous devrez réinitialiser les différents tableaux de bord de rapports pour chaque canal et type de rapport. Pour plus d’informations sur la personnalisation des tableaux de bord, reportez-vous à la section <a href="../reports/live-report.md">documentation détaillée.</a></p>
<p>Une nouvelle colonne de la liste d'exécution des messages affiche le nombre de profils ciblés pour chaque exécution du message. </p>
<p>Pour plus d’informations, reportez-vous à la section <a href="../reports/global-report.md">documentation détaillée</a>.</p>
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
<p>Pour plus d’informations sur les collections, reportez-vous à la section <a href="../building-journeys/collections.md">documentation détaillée</a>. </p>
<p>Les fonctions de filtre et d’intersection ont été ajoutées à la liste des fonctions disponibles dans l’éditeur d’expression avancé. Cela offre davantage de possibilités de filtrage et de comparaison des collections.</p>
<p>Consultez la documentation relative à la <a href="../building-journeys/functions/functionfilter.md">filter</a> et <a href="../building-journeys/functions/functionintersect.md">intersection</a> fonctions.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations

**Parcours**

* Les schémas et les jeux de données générés par le système qui ont été créés pendant la mise en service des événements d’étape sont désormais en lecture seule, ce qui permet d’éviter toute modification involontaire des schémas critiques. [En savoir plus](../reports/sharing-overview.md)
* Étiqueter précisément la variable **Attente** activité avec un libellé qui s’affichera dans la zone de travail. Le libellé est également utilisé dans les journaux des modes de reporting et de test pour identifier clairement ce que vous faites. [En savoir plus](../building-journeys/about-journey-activities.md#best-practices)
* Trouvez plus rapidement vos événements et actions en filtrant les éléments dans la variable **Événements** et **Action** catégories à l’aide de la recherche. Les activités d’orchestration ne sont plus filtrées. [En savoir plus](../building-journeys/using-the-journey-designer.md)
* Lors de la définition d’une condition d’identifiant d’événement dans un événement d’entreprise ou basé sur des règles, l’opérateur &quot;contient&quot; est désormais disponible pour les types de chaînes de champs. [En savoir plus](../event/about-creating.md)

**Configuration des emails**

* Lorsqu’un pool d’adresses IP a été associé à un paramètre prédéfini de message, vous pouvez désormais le modifier, la mise à jour étant asynchrone. Vous pouvez également vérifier l’état de chaque mise à jour du pool d’adresses IP. [En savoir plus](../configuration/ip-pools.md#edit-ip-pool)


## Version d’août 2021 {#august-2021-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>

<th><strong>Envoyer des messages au meilleur moment - Optimisation de l’heure d’envoi</strong><br/></th>
</thead>
<tbody>
<tr>
<td>
<p>Envoyez automatiquement vos notifications push ou vos e-mails au meilleur moment pour chaque client avec lequel vous interagissez avec Adobe Journey Optimizer. L’optimisation du temps d’envoi, optimisée par les services d’IA d’Adobe, prédit le meilleur moment pour envoyer un email ou un message push afin d’optimiser l’engagement en fonction des taux d’ouverture et de clics historiques prêts à l’emploi.</p>
<p>Cette fonctionnalité est actuellement en version bêta et disponible uniquement pour les clients bêta. Pour rejoindre le programme bêta, contactez l’assistance clientèle d’Adobe.</p>
<p>Pour plus d’informations, reportez-vous à la section <a href="../building-journeys/journeys-message.md#send-time-optimization">documentation détaillée</a>.</p>
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
<p>Vous pouvez désormais tirer parti des relations entre les schémas lors de la configuration d’événements professionnels. Cela s’ajoute à la possibilité d’exploiter des champs des tables liées lors de la configuration d’un événement unitaire, lors de l’utilisation de conditions dans un parcours, dans la personnalisation des messages et dans la personnalisation d’actions personnalisées.</p>
<p>Pour plus d’informations, reportez-vous à la section <a href="../event/experience-event-schema.md#leverage_schema_relationships">documentation détaillée</a>.</p>
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
<p>Pour plus d’informations, reportez-vous à la section <a href="../personalization/personalization-syntax.md#perso-urls">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


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
<p>Pour plus d’informations, reportez-vous à la section <a href="../configuration/retries.md#retry-duration">documentation détaillée</a>.</p>
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
<p>L’ajout d’adresses et de domaines de courriel dans la liste de suppression est désormais disponible dans l’interface utilisateur, une par une, soit en mode masse via un téléchargement de fichier CSV.</p>
<p>Pour plus d’informations, reportez-vous à la section <a href="../configuration/manage-suppression-list.md#add-addresses-and-domains">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


### Améliorations

**Parcours**

* **En-têtes dynamiques** - Vous pouvez désormais transmettre des données dynamiques dans les paramètres d’en-tête HTTP. Ces paramètres peuvent être utilisés par les systèmes d’intégration qui reçoivent les appels HTTP d’action de parcours, par exemple l’horodatage ou l’ID de suivi. [En savoir plus](../action/about-custom-action-configuration.md#url-configuration)
* **Chemins d’URL dynamiques** - Vous pouvez désormais configurer des chemins d’URL dynamiques pour les actions personnalisées. [En savoir plus](../action/about-custom-action-configuration.md#url-configuration)
* Le taux de ralentissement global pour les segments lus a été modifié de 17 000 à 20 000 messages par seconde. [En savoir plus](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Interface utilisateur**

* **Rechercher** - Sur chaque page, vous pouvez désormais rechercher des objets commerciaux et des articles d’aide directement à partir du champ de recherche d’Experience Cloud unifié. [En savoir plus](../start/user-interface.md#unified-search)
* **Récents** - L’affichage des éléments récents de la page d’accueil d’Adobe Journey Optimizer est désormais étendu à d’autres objets commerciaux. Grâce à cette mise à jour, les raccourcis vers vos accès récents comprennent les messages, les parcours, les segments, les schémas, les jeux de données, les sources de données, les événements, les actions, les sources et les destinations. [En savoir plus](../action/about-custom-action-configuration.md#passing-collection)

**Conception de contenu**

* **Contexte** - Les images d’arrière-plan sont désormais prises en charge dans l’aperçu en direct. [En savoir plus](../email/preview.md)
* **Lien d’exclusion en un clic** - Vous pouvez insérer un nouveau type de lien dans le contenu de votre email : la valeur **Exclusion** Le lien permet aux utilisateurs de se désabonner de la réception de vos communications en un seul clic, sans être redirigés vers une landing page pour confirmer leur désinscription. [En savoir plus](../privacy/opt-out.md#one-click-opt-out-link)

**Personnalisation**

* **Editeur d&#39;expression** - Vous pouvez désormais facilement ajouter une valeur de secours lors de la définition de la personnalisation : lorsque le champ de personnalisation est vide pour un profil, la valeur de retour arrière s’affiche. [En savoir plus](../personalization/functions/helpers.md)

**Configuration des emails**

* **Liste autorisée** - La liste autorisée peut désormais être activée et désactivée sur un environnement de test hors production via un appel API. [En savoir plus](../configuration/allow-list.md#enable-allow-list)
* **Navigation** - La liste de suppression, accessible sous le **Administration > Canaux > Configuration des emails > Général** a été déplacé vers le nouveau **Liste de suppression** , qui rassemble toutes les fonctionnalités associées pour un accès plus facile. [En savoir plus](../configuration/manage-suppression-list.md#access-suppression-list)

**Gestion des décisions**

* La manière dont vous ajoutez et configurez des représentations lors de la création d’une offre a été mise à jour pour améliorer l’expérience utilisateur. En particulier, la bibliothèque de ressources s’affiche désormais uniquement lorsque vous définissez du contenu de type image pour une représentation. [En savoir plus](../offers/offer-library/creating-personalized-offers.md#representations)

### Correctifs

* Correction d’un problème d’accessibilité dans la navigation par onglets des messages.
* Correction d’un problème de localisation dans les étiquettes du concepteur d’emails.
* Correction d’un problème lors de la sélection de plusieurs noeuds dans un parcours et du clic sur &quot;Supprimer&quot; dans le volet des propriétés.
* Correction d’un problème qui empêchait l’ajout d’un nouvel en-tête à une action utilisée dans un parcours.
* Vous pouvez maintenant découvrir la raison pour laquelle la création d’un paramètre prédéfini de message a échoué via un avertissement plus explicite dans l’interface utilisateur.


## Version de juillet 2021 {#july-2021-release}

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
<p>Pour plus d’informations, reportez-vous à la section <a href="../event/experience-event-schema.md#leverage_schema_relationships">documentation détaillée</a>.</p>
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
<p>Vous pouvez maintenant définir une liste spécifique de sécurité d’envoi au niveau de l’environnement de test, afin d’avoir un environnement sûr à des fins de test. Sur une instance hors production, où des erreurs peuvent se produire, la liste autorisée vous assure que vous n’avez aucun risque d’envoyer des messages indésirables à vos clients. Cette fonctionnalité est activée en utilisant les API de suppression.</p>
<p>Pour plus d’informations, reportez-vous à la section <a href="../configuration/allow-list.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations

**Parcours**

* Le taux de ralentissement global de tous les segments lus exécutés simultanément dans le même environnement de test est limité à 17 000 messages par seconde. [En savoir plus](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Le **Durée du cache** a été supprimé du volet de configuration de la source de données. [En savoir plus](../datasource/about-data-sources.md)
* Pour les sources de données externes, une règle de limitation de 15 appels par seconde est désormais définie automatiquement. [En savoir plus](../configuration/external-systems.md#capping)
* Pour les parcours actifs, l’écran des propriétés du parcours affiche désormais la date de publication et le nom de l’utilisateur qui a publié le parcours. [En savoir plus](../building-journeys/journey-gs.md#change-properties)
* Dans l’écran de liste des parcours, le filtre de type de parcours a été ajouté. [En savoir plus](../start/user-interface.md#filter-lists)
* Le **[!UICONTROL Throttling rate]** a été ajouté à l’activité Lecture de segment . [En savoir plus](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Aperçu et test**

* L’identité et l’espace de noms sont désormais visibles dans la variable **[!UICONTROL Preview]** écran. [En savoir plus](../email/preview.md#preview-your-messages)
* Le nombre d’emails de test pour les bons à tirer est désormais limité à 10.
* Caractères autorisés pour la variable **Préfixe de ligne d’objet** dans les bons à tirer sont désormais limités. [En savoir plus](../email/preview.md#send-proofs)

**Éditeur d’expression de personnalisation**

* La liste déroulante Aide a été renommée et réorganisée.

### Correctifs

* Correction d’un problème qui entraînait la diffusion de messages en double pour la diffusion d’emails par lots.
* Les événements sont désormais générés en conséquence lorsque l’envoi d’emails n’est pas effectué une fois la période de reprise terminée.
* Correction d’un problème en raison duquel les informations IP manquaient dans l’écran Enregistrements PTR.
* La localisation dans le rail des offres au sein de l&#39;éditeur d&#39;expression est désormais implémentée.
* Correction d’un espacement incorrect dans les fenêtres contextuelles d’informations.
* Correction d’un problème dans le concepteur d’emails lors du téléchargement d’un fichier HTML en raison duquel une feuille de style interne avec `background-image` n’était pas prise en charge.
