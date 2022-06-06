---
title: Notes de mise à jour 2022
description: Notes de mise à jour 2022 pour Journey Optimizer
exl-id: 0997a640-3f89-4460-ba93-ea21a9d4efc5
source-git-commit: f5e3b7cee816be420a09abd8aa9404faaccfec87
workflow-type: ht
source-wordcount: '1069'
ht-degree: 100%

---

# Notes de mise à jour 2022 {#release-notes-2022}

Cette page répertorie toutes les fonctionnalités et améliorations pour [!DNL Journey Optimizer] publiées en 2022.

Les dernières notes de mise à jour sont disponibles [dans cette page](release-notes.md).

## Version d&#39;avril 2022 {#april-2022-release}

### Améliorations

**Pages de destination**

* **Nouvelle option pour les cases à cocher de type opt-in/opt-out** : vous pouvez désormais insérer une seule case à cocher de type opt-in/opt-out dans les pages de destination des abonnements. Les utilisateurs doivent cocher la case pour donner leur consentement (opt-in), et la décocher pour supprimer leur consentement (opt-out). [En savoir plus](../landing-pages/design-lp.md#define-lp-specific-content)

* **Préremplir les champs des pages de destination** : il est désormais possible de donner aux utilisateurs la possibilité de préremplir les champs des pages de destination avec des informations de profil. [En savoir plus](../landing-pages/create-lp.md#configure-primary-page)

**Gestion des décisions**

* **API Decisioning sur Edge** : l’API Edge Decisioning peut diffuser et renvoyer des offres personnalisées qui sont gérées dans Offer Decisioning. Vous pouvez créer vos offres et d’autres objets connexes en utilisant l’interface utilisateur (UI) ou les API d’Offer Decisioning. [En savoir plus](../offers/api-reference/offer-delivery-api/edge-decisioning-api.md)

**Administration**

* **Durée d’envoi des PTR** : la durée pour que la modification des PTR soit effective est maintenant de quelques heures. [En savoir plus](../configuration/ptr-records.md#processing)

**Conception d’e-mail**

* **20 nouveaux modèles d’e-mail** sont maintenant disponibles pour concevoir le contenu de vos e-mails dans Journey Optimizer.

**Interface utilisateur**

* **Aide contextuelle dans l’interface utilisateur de Journey Optimizer** : des liens d’aide contextuelle ont été ajoutés à plusieurs pages de Journey Optimizer. Lorsqu’ils sont disponibles, cliquez sur l’icône « i » pour afficher une description rapide de la fonctionnalité en cours et accéder aux articles connexes.

**Intégration à Adobe Campaign Standard**

En tant que client d’Adobe Campaign Standard, vous pouvez désormais envoyer des e-mails, des notifications push et des SMS à l’aide de Journey Optimizer. Utilisez les nouvelles actions intégrées pour tirer profit des fonctionnalités de messagerie transactionnelle de Campaign Standard dans Journey Optimizer.  [En savoir plus](../action/acs-action.md)

<!--
### Fixes

* Fixed an issue which caused tracking reports not to be available as the `JourneyActionId` was not properly populated. PLATIR-19854, CJM-26006
* Fixed an error on business events which could block the journey publication. CJM-25931
* Fixed an issue which could prevent images in Email Designer templates from being displayed. PLATIR-18176, CJM-25008
-->

## Version de mars 2022 {#march-2022-release}

### Améliorations

**Parcours**

* Pour éviter d’avoir des champs inutiles dans le schéma de profil unifié, le schéma Événement d’étape du parcours n’est plus activé par défaut pour les profils. Si nécessaire, vous pouvez l’activer. [En savoir plus](../reports/sharing-overview.md)
* Les nouveaux événements d’étape liés aux tâches d’exportation sont désormais envoyés par Journey Optimizer à Adobe Experience Platform. Des exemples de requêtes ont été ajoutés à la documentation. [En savoir plus](../reports/query-examples.md)

**Gestion des décisions**

* Vous pouvez désormais spécifier si la limitation de l’offre est appliquée à tous les utilisateurs ou à un profil spécifique, à tous les emplacements ou par emplacement. [En savoir plus](../offers/offer-library/add-constraints.md#capping)
* L’API Batch Decisioning permet aux entreprises d’utiliser la fonctionnalité Offer Decisioning pour tous les profils d’un segment donné en un seul appel. Le contenu de l’offre pour chaque profil du segment est placé dans un jeu de données AEP où il est disponible pour les workflows par lots personnalisés. [En savoir plus](../offers/api-reference/offer-delivery-api/batch-decisioning-api.md)

**Administration**

* Vous pouvez maintenant activer/désactiver le lien de désabonnement dans/à partir de l’en-tête de l’e-mail au niveau du paramètre de message prédéfini, et définir une URL de désabonnement personnalisée au niveau du message. [En savoir plus](../configuration/message-presets.md#list-unsubscribe)
* La liste autorisée peut désormais être activée et désactivée via l’interface [!DNL Journey Optimizer] sur les environnements de test de production et hors production. [En savoir plus](../reports/allow-list.md#enable-allow-list)

**Personnalisation**

* Vous pouvez désormais enregistrer plus de 40 expressions de personnalisation dans la bibliothèque. [En savoir plus](../personalization/personalization-library.md)

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
