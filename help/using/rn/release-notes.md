---
title: Notes de mise à jour
description: Notes de mise à jour de Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: ca9cb62770c1c50b2683486de48435d5b47b8729
workflow-type: tm+mt
source-wordcount: '2700'
ht-degree: 100%

---

# Notes de mise à jour {#release-notes}

Cette page répertorie toutes les nouvelles fonctionnalités et améliorations d&#39;[!DNL Journey Optimizer]. Vous pouvez également consulter la page relative aux [dernières mises à jour de la documentation](documentation-updates.md) pour prendre connaissance des autres modifications.



## Version de février 2022 {#feb-2022-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>
<th><strong>Pages de destination d’abonnement</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer et concevoir des pages de destination dans Journey Optimizer afin de diriger vos utilisateurs vers des formulaires en ligne où ils pourront s’inscrire ou se désinscrire de la réception de vos communications, ou s’abonner à un service spécifique, tel qu’une newsletter.</p>
<p>Pour plus d’informations, consultez la <a href="../landing-pages/create-lp.md">documentation détaillée</a> et le <a href="../landing-pages/lp-use-cases.md">cas d’utilisation type</a> correspondant.</p>
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
<p>Journey Optimizer propose désormais une bibliothèque qui vous donne accès à des expressions de personnalisation prédéfinies. Ces expressions sont configurées par les utilisateurs administrateurs.</p>
<p>Pour plus d’informations, consultez la <a href="../personalization/personalization-library.md">documentation détaillée</a>.</p>
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
The suppression list helps you with honoring the ISPs’ feedback to preserve sending IP reputation. The allow list helps you ensure that you send only to those email addresses which are in the allowed list, and typically to ensure that you don't send mails to customers from your development sandbox.</p>
<p>See <a href="https://developer.adobe.com/journey-optimizer-apis/">Adobe Journey Optimizer APIs</a>.</p>
</td>
</tr>
</tbody>
</table-->

<table>
<thead>
<tr>
<th><strong>Transmettre des informations pour suivre vos messages avec les paramètres de tracking UTM</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Dans le contenu des messages Journey Optimizer, vous pouvez maintenant ajouter des paramètres UTM à vos liens : ils peuvent fournir des données supplémentaires sur ce lien et vous aider à identifier où et pourquoi une personne a cliqué sur ce lien.</p>
<p>Pour plus d'informations, consultez la <a href="../configuration/message-presets.md#configure-email-settings">documentation détaillée</a>.</p-->
</td>
</tr>
</tbody>
</table>

### Améliorations

**Parcours**

* Pour optimiser les performances, tous les parcours en mode test qui n’ont pas été déclenchés depuis une semaine repassent désormais au statut Version préliminaire. [En savoir plus](../building-journeys/testing-the-journey.md#important_notes)
* L’intégration entre Journey Optimizer et Adobe Campaign Classic a été optimisée pour améliorer les performances. La configuration par défaut de limitation a été remplacée par 4 000 appels/5 minutes.	[En savoir plus](../action/acc-action.md#important-notes)

**Reporting**

* Les diffusions peuvent désormais être filtrées en fonction de leur statut :
   * Dans la liste Exécution des messages, vous pouvez désormais exclure les BAT de la liste de vos diffusions.
   * Dans vos rapports dynamiques/globaux, vous pouvez choisir d’exclure les événements de test.

* Vous pouvez désormais accéder aux rapports sur les données d’optimisation de l’heure d’envoi : le nombre de personnes qui ont reçu immédiatement des messages et le nombre de personnes qui ont reçu des messages avec une optimisation d’une heure, une optimisation de 2 heures, etc.

<!--* Offer Decisioning reports are now available in Journey Optimizer. You can access the following metrics: Offers sent - Offers' impression rate - Offers' click rate - Breakdown report on Offers' sent.-->

**Gestion des décisions**

* Les classements et le classement IA sont désormais regroupés dans un seul onglet.

## Version de janvier 2022 {#january-2022-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>
<th><strong>Parcours : optimisation de la montée en puissance des adresses IP à lʼaide des conditions de limite de profils</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Lors de la configuration d’une activité <strong>Condition</strong> dans un parcours, vous pouvez désormais définir une limite de profils. Utilisez ce nouveau type de condition pour définir un nombre maximal de profils pour le chemin dʼun parcours. Lorsque cette limite est atteinte, les profils entrants prennent un autre chemin. Vous pouvez ainsi augmenter le volume de vos diffusions (montée en puissance des adresses IP). Par exemple, vous pouvez augmenter le nombre de diffusions sur un domaine en fractionnant lʼexécution : envoi de 1 000 messages le premier jour, 2 000 le deuxième jour, etc.</p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/condition-activity.md#profile_cap">documentation détaillée</a> et le <a href="../building-journeys/ramp-up-deliveries-uc.md">cas d’utilisation type</a> correspondant.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Parcours : amélioration apportée à la lecture de segment</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Lʼoption <strong>Lecture incrémentielle</strong> a été ajoutée aux activités <strong>Lecture de segment</strong> récurrentes. Cette option permet de cibler uniquement les individus qui sont entrés dans le segment depuis la dernière exécution du parcours. La première exécution cible toujours tous les membres du segment.</p>
<p>Pour plus d'informations, consultez la <a href="../building-journeys/read-segment.md#configuring-segment-trigger-activity">documentation détaillée</a>.
</td>
</tr>
</tbody>
</table>

### Améliorations

**Parcours**

* Les événements d’étape Journey Optimizer peuvent désormais être liés à d’autres jeux de données dans [Adobe Customer Journey Analytics](https://experienceleague.adobe.com/docs/analytics-platform/using/cja-overview/cja-overview.html?lang=fr). Le champ **profileID**, dans le schéma intégré d’événement d’étape du parcours, est désormais défini comme un champ d’identité. [En savoir plus](../reports/sharing-overview.md#integration-cja)

**Offer Decisioning**

* La mise à jour dʼune offre, dʼune offre de secours, dʼune collection d’offres ou dʼune décision d’offre, directement ou indirectement référencée dans un message publié, est désormais automatiquement répercutée dans le message correspondant, sans quʼil soit nécessaire de le republier. [En savoir plus](../offers/offers-e2e.md#insert-decision-in-email)

* Lors de la simulation des offres qui seront diffusées pour un profil de test donné, vous pouvez maintenant modifier les paramètres de simulation par défaut et afficher le code correspondant à vos simulations qui peut être utilisé à des fins de dépannage. [En savoir plus](../offers/offer-activities/simulation.md#define-simulation-settings)

**Administration**

* Les administrateurs peuvent désormais modifier les enregistrements PTR avec un sous-domaine configuré en CNAME. [En savoir plus](../configuration/ptr-records.md#edit-ptr-subdomains-cname)

**Personnalisation**

* **Ajouter aux favoris** : pour aider à améliorer lʼefficacité lors de lʼutilisation de la personnalisation, nous avons introduit le concept d’enregistrement dans les favoris. L’ajout de différents attributs à votre menu de favoris vous permet dʼaccéder rapidement aux éléments que vous utilisez le plus fréquemment. [En savoir plus](../personalization/personalize.md#fav)

## Publication de novembre 2021 {#november-2021-release}

<table>
<thead>
<tr>
<th><strong>Délégation de sous-domaines CNAME</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer prend désormais en charge les enregistrements CNAME. Un CNAME, ou enregistrement de nom canonique, est un enregistrement qui pointe vers une autre adresse de domaine plutôt que vers une adresse IP. La délégation de sous-domaines CNAME permet de créer un sous-domaine et d’utiliser des CNAME pour pointer vers des enregistrements spécifiques à Adobe. Grâce à cette configuration, vous partagez avec Adobe la responsabilité de la maintenance du DNS afin de configurer un environnement pour l’envoi, le rendu et le suivi des e-mails.</p>
<p>Cette méthode est recommandée si les stratégies de votre organisation interdisent la méthode de délégation de sous-domaine complète.</p>
<p>En savoir plus sur la délégation de sous-domaines CNAME dans la <a href="../configuration/delegate-subdomain.md#cname-subdomain-delegation">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


## Version d’octobre 2021 {#oct-2021-release}

### Nouvelles fonctionnalités

<table>
<thead>
<tr>
<th><strong>Gestion des décisions - Simulation des offres</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais simuler les offres qui seront diffusées à un profil de test pour un emplacement donné dans l’interface utilisateur de Journey Optimizer. Cela vous permet de valider facilement votre logique de prise de décision, y compris les contraintes d’éligibilité et les algorithmes de classement avant de les mettre en production. Cette fonctionnalité permet aux utilisateurs non techniques et techniques de tester rapidement Offer Decisioning et de résoudre les problèmes potentiels. </p>
<p>Pour plus d’informations, consultez la <a href="../offers/offer-activities/simulation.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Gestion des décisions - Personnaliser vos offres</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais personnaliser le contenu de vos offres à l’aide des segments et des attributs de profil Adobe Experience Platform en utilisant le même composant d’éditeur d’expression que celui de l’interface utilisateur de Journey Optimizer.  </p>
<p>Pour plus d'informations, consultez la <a href="../offers/offer-library/creating-personalized-offers.md#custom-text">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


Voir également les [Notes de mise à jour d’octobre d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/2021/october-2021.html?lang=fr){target=&quot;_blank&quot;} pour effectuer d’autres modifications. 

### Améliorations

**Parcours**

* **Éditeur d&#39;expression** - En tant qu’utilisateur avancé, vous pouvez désormais utiliser des fonctions pour travailler avec les mappings. Cette fonctionnalité peut être exploitée avec les listes d’abonnements. Par exemple, à partir d’un segment, vous pouvez désormais obtenir une adresse e-mail à partir d’une liste d’abonnements. [En savoir plus dans cet exemple](../building-journeys/message-to-subscribers-uc.md)

* **Surveillance** - Les événements d’étape pour les parcours actifs et le mode test ont été améliorés. De [nouveaux champs](../reports/sharing-field-list.md#serviceevents) ont été ajoutés en rapport avec les tâches d’exportation de profil. Pour une meilleure expérience utilisateur, les champs d’événement d’étape sont désormais organisés en différentes catégories. Tous les champs d’événements d’étape précédents sont toujours disponibles dans la catégorie [stepEvents](../reports/sharing-legacy-fields.md).
* **Accessibilité** - Des améliorations d’accessibilité ont été apportées aux parcours. 
* **Collections** - Les tableaux d’objets contenant des sous-objets sont désormais pris en charge. [En savoir plus](../building-journeys/collections.md)
* **Listes** - Les écrans de liste ont été améliorés pour les parcours, les événements, les actions et les sources de données. 

**Reporting**

* **Format des données dans la vue globale** - Vous pouvez désormais basculer entre les chiffres et les pourcentages dans la **Vue globale** de l’onglet **Exécution**. [En savoir plus](../messages/message-monitoring.md)


**Administration**

* **Modifier les paramètres prédéfinis de message** - Vous pouvez désormais modifier les préréglages de message et surveiller leur statut de mise à jour. [En savoir plus](../configuration/message-presets.md#edit-message-preset)
* **Modification des enregistrements PTR** - Vous pouvez désormais modifier les enregistrements PTR et surveiller leur statut de mise à jour. [En savoir plus](../configuration/ptr-records.md#edit-ptr-record)

**Personnalisation**

* **Nouvelle fonction d’assistance pour le formatage des dates** - Vous pouvez désormais spécifier comment une chaîne de date doit être représentée. [En savoir plus](../personalization/functions/dates.md#format-date)


**Gestion des décisions**

* **Séquencement des évaluations** - Le nouveau flux de création de décision a été amélioré et vous permet non seulement de naviguer plus facilement entre les objets de décision, mais également de contrôler entièrement la manière dont les collections d’offres sont évaluées par le moteur de décision. Cela inclut les collections qui sont évaluées ensemble ou séparément, et dans quel ordre les collections doivent être évaluées. [En savoir plus](../offers/offer-activities/create-offer-activities.md#add-decision-scopes)

### Correctifs

* Correction d’un problème qui empêchait l’affichage de la liste des parcours, de la liste des messages et du concepteur d’e-mail lorsque la langue du navigateur n’était pas l’anglais.
* Correction d’une erreur de syntaxe qui survenait lors de l’ajout d’une personnalisation à l’aide d’une expression dans le Concepteur d’e-mail : les caractères étaient placés par erreur dans une séquence d’échappement. 
* Correction d’un problème qui entraînait une erreur 404 lors de la navigation dans le menu **Administration**. 
* Correction d’un problème qui déclenchait d’autres parcours actifs lors du test d’un parcours à l’aide d’un événement métier. 


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
<p>De nouvelles mesures sont disponibles dans les rapports : Ciblé et Exclu pour les e-mails et les messages push sont visibles dans les rapports dynamiques et globaux. </br> Pour avoir accès aux dernières mesures, vous devrez réinitialiser les différents tableaux de bord de rapports pour chaque canal et type de rapport. Pour plus d’informations sur la personnalisation des tableaux de bord, consultez la <a href="../reports/live-report.md">documentation détaillée.</a></p>
<p>Une nouvelle colonne de la liste d'exécution des messages affiche le nombre de profils ciblés pour chaque exécution du message. </p>
<p>Pour plus d'informations, consultez la <a href="../messages/message-monitoring.md">documentation détaillée</a>.</p>
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
<p>Vous pouvez désormais transmettre des collections ou une liste de données dans vos paramètres d’action personnalisés qui seront renseignés dynamiquement au moment de l’exécution. Deux types de collections sont pris en charge : collections simples et collections d’objets. Les actions personnalisées créées précédemment continueront à fonctionner. </p>
<p>Pour plus d'informations sur les collections, consultez la <a href="../building-journeys/collections.md">documentation détaillée</a>. </p>
<p>Les fonctions filter et intersect ont été ajoutées à la liste des fonctions disponibles dans l’éditeur d’expression avancé. Cela offre davantage de possibilités de filtrage et de comparaison des collections.</p>
<p>Consultez la documentation sur les fonctions <a href="../building-journeys/functions/functionfilter.md">filter</a> et <a href="../building-journeys/functions/functionintersect.md">intersect</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations

**Parcours**

* Les schémas et les jeux de données générés par le système qui ont été créés pendant l&#39;approvisionnement des événements d’étape sont désormais en lecture seule, ce qui permet d’éviter toute modification involontaire des schémas critiques. [En savoir plus](../reports/sharing-overview.md)
* Libellez de manière claire l’activité **Attente** avec un libellé qui s’affichera dans la zone de travail. Le libellé est également utilisé dans les journaux des modes de reporting et de test pour identifier clairement ce que vous faites. [En savoir plus](../building-journeys/about-journey-activities.md#best-practices)
* Trouvez plus rapidement vos événements et actions en filtrant les éléments dans les catégories **Événements** et **Action** à l’aide de la recherche. Les activités d’orchestration ne sont plus filtrées. [En savoir plus](../building-journeys/using-the-journey-designer.md)
* Lors de la définition d’une condition d’identifiant d’événement dans un événement métier ou basé sur des règles, l’opérateur &quot;contains&quot; est désormais disponible pour les types de chaînes de champs. [En savoir plus](../event/about-creating.md)

**Configuration des e-mails**

* Lorsqu’un groupe d’adresses IP a été associé à un préréglage de message, vous pouvez désormais le modifier, la mise à jour étant asynchrone. Vous pouvez également vérifier l’état de chaque mise à jour du groupe d’adresses IP. [En savoir plus](../configuration/ip-pools.md#edit-ip-pool)


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
<p>Envoyez automatiquement vos notifications push ou vos e-mails au meilleur moment pour chaque client avec Adobe Journey Optimizer. L’optimisation de l’heure d’envoi, optimisée par les services d’IA d’Adobe, prédit le meilleur moment pour envoyer un e-mail ou un message push afin d’optimiser l’engagement en fonction des taux d’ouverture et de clics historiques prêts à l’emploi.</p>
<p>Cette fonctionnalité est actuellement en version bêta et disponible uniquement pour les clients bêta. Pour rejoindre le programme bêta, contactez l’assistance clientèle d’Adobe.</p>
<p>Pour plus d'informations, consultez la <a href="../building-journeys/journeys-message.md#send-time-optimization">documentation détaillée</a>.</p>
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
<p>Pour plus d'informations, consultez la <a href="../event/experience-event-schema.md#leverage_schema_relationships">documentation détaillée</a>.</p>
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
<p>Les URL personnalisées orientent les destinataires vers des pages spécifiques d'un site web ou vers un microsite personnalisé, en fonction des attributs du profil. Dans Adobe Journey Optimizer, vous pouvez désormais ajouter une personnalisation aux URL dans le contenu de votre message. La personnalisation de l'URL peut être appliquée au texte et aux images, et utiliser les données de profil ou les données contextuelles.</p>
<p>Pour plus d'informations, consultez la <a href="../personalization/personalization-syntax.md#perso-urls">documentation détaillée</a>.</p>
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
<p>Pour plus d'informations, consultez la <a href="../configuration/retries.md#retry-duration">documentation détaillée</a>.</p>
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
<p>Pour plus d'informations, consultez la <a href="../configuration/manage-suppression-list.md#add-addresses-and-domains">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


### Améliorations

**Parcours**

* **En-têtes dynamiques** : vous pouvez désormais transmettre des données dynamiques dans les paramètres d’en-tête HTTP. Ces paramètres peuvent être utilisés par les systèmes d’intégration qui reçoivent les appels HTTP de l’action de parcours, par exemple l’horodatage ou l’ID de suivi. [En savoir plus](../action/about-custom-action-configuration.md#url-configuration)
* **Chemins d’URL dynamiques** : vous pouvez désormais configurer des chemins d’URL dynamiques pour les actions personnalisées. [En savoir plus](../action/about-custom-action-configuration.md#url-configuration)
* Le taux de limitation global pour les segments lus a été modifié de 17 000 à 20 000 messages par seconde. [En savoir plus](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Interface utilisateur**

* **Rechercher** : sur chaque page, vous pouvez désormais rechercher des objets métier et des articles d’aide directement dans le champ de recherche Unified Experience Cloud. [En savoir plus](../start/user-interface.md#unified-search)
* **Récents** : l’affichage des éléments récents de la page d’accueil d’Adobe Journey Optimizer est désormais étendu aux objets métier supplémentaires. Grâce à cette mise à jour, les raccourcis vers vos accès récents comprennent les messages, les parcours, les segments, les schémas, les jeux de données, les sources de données, les événements, les actions, les sources et les destinations. [En savoir plus](../action/about-custom-action-configuration.md#passing-collection)

**Conception de contenu**

* **Arrière-plan** : les images d’arrière-plan sont désormais prises en charge dans l’aperçu dynamique. [En savoir plus](../messages/preview.md)
* **Lien d’exclusion en un clic** : vous pouvez insérer un nouveau type de lien dans le contenu de votre e-mail : le lien d’**exclusion** permet aux utilisateurs de se désabonner de la réception de vos communications en un seul clic, sans être redirigé vers une page de destination pour confirmer leur désinscription. [En savoir plus](../messages/consent.md#one-click-opt-out-link)

**Personnalisation**

* **Éditeur d’expression** : vous pouvez désormais facilement ajouter une valeur de secours lors de la définition de la personnalisation : lorsque le champ de personnalisation est vide pour un profil, la valeur de secours s’affiche. [En savoir plus](../personalization/functions/helpers.md)

**Configuration des e-mails**

* **Liste autorisée** : la liste autorisée peut désormais être activée et désactivée sur un environnement de test hors production via un appel API. [En savoir plus](../messages/allow-list.md#enable-allow-list)
* **Navigation** : la liste de suppression, accessible sous le menu **Administration > Canaux > Configuration des emails > Général** a été déplacée vers le nouveau sous-menu  **Liste de suppression**, qui rassemble toutes les fonctionnalités associées pour un accès plus facile. [En savoir plus](../configuration/manage-suppression-list.md#access-suppression-list)

**Gestion des décisions**

* La manière dont vous ajoutez et configurez des représentations lors de la création d&#39;une offre a été mise à jour pour améliorer l&#39;expérience utilisateur. En particulier, la bibliothèque de ressources s&#39;affiche désormais uniquement lorsque vous définissez du contenu de type image pour une représentation. [En savoir plus](../offers/offer-library/creating-personalized-offers.md#representations)

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
<p>Enrichissez vos expériences avec les données de référence que vous avez chargées dans Journey Optimizer. Par exemple, la recherche de métadonnées sur un ID de réservation dans un événement d’expérience ou la recherche d’informations sur un produit à partir d’un SKU dans un événement d’expérience à utiliser dans la zone de travail. </p>
<p>Vous pouvez désormais tirer profit des relations entre les schémas afin d’utiliser un jeu de données comme table de recherche pour un autre. Vous pouvez ensuite exploiter tous les champs des tables liées lors de la configuration d’un événement unitaire, lors de l’utilisation de conditions dans un parcours, dans la personnalisation des messages et dans la personnalisation d’une action personnalisée.</p>
<p>Pour plus d'informations, consultez la <a href="../event/experience-event-schema.md#leverage_schema_relationships">documentation détaillée</a>.</p>
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
<p>Pour plus d'informations, consultez la <a href="../messages/allow-list.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Améliorations

**Parcours**

* Le taux de limitation global de toutes les lectures de segment qui s&#39;exécutent simultanément dans le même environnement Sandbox est limité à 17 000 messages par seconde. [En savoir plus](../building-journeys/read-segment.md#configuring-segment-trigger-activity)
* Le champ **Durée de mise en cache** a été supprimé du panneau de configuration de la source de données. [En savoir plus](../datasource/about-data-sources.md)
* Pour les sources de données externes, une règle de limitation de 15 appels par seconde est maintenant définie automatiquement. [En savoir plus](../configuration/external-systems.md#capping)
* Pour les parcours actifs, l’écran des propriétés du parcours affiche la date de publication et le nom de l’utilisateur qui a publié le parcours. [En savoir plus](../building-journeys/journey-gs.md#change-properties)
* Dans l&#39;écran Liste des parcours, le filtre de type de parcours a été ajouté. [En savoir plus](../start/user-interface.md#filter-lists)
* Le paramètre **[!UICONTROL Taux de limitation]** a été ajouté à l&#39;activité Lecture de segment. [En savoir plus](../building-journeys/read-segment.md#configuring-segment-trigger-activity)

**Prévisualiser et tester les messages**

* L&#39;identité et l&#39;espace de noms sont maintenant visibles dans l&#39;écran **[!UICONTROL Aperçu]**. [En savoir plus](../messages/preview.md#preview-your-messages)
* Le nombre d&#39;e-mails de test pour les BAT est maintenant limité à 10.
* Les caractères autorisés pour le **préfixe de ligne d&#39;objet** dans les BAT sont maintenant limités. [En savoir plus](../messages/preview.md#send-proofs)

**Personnalisation de l&#39;éditeur d&#39;expression**

* La liste déroulante des helpers a été renommée et réorganisée.

### Correctifs

* Correction d&#39;un problème qui entraînait la diffusion de messages en double pour la diffusion d&#39;e-mails par lots.
* Les événements sont maintenant générés en conséquence lorsque l&#39;envoi d&#39;e-mails n&#39;est pas effectué une fois la période de reprise terminée.
* Correction d&#39;un problème en raison duquel les informations IP manquaient dans l&#39;écran Enregistrements PTR.
* La localisation est maintenant implémentée dans le rail des offres au sein de l&#39;éditeur d&#39;expression.
* Correction d&#39;un espacement incorrect dans les fenêtres contextuelles d&#39;informations.
* Correction d’un problème dans le concepteur d’e-mails lors du téléchargement d’un fichier HTML en raison duquel la feuille de style interne avec la propriété `background-image` n’était pas prise en charge.
