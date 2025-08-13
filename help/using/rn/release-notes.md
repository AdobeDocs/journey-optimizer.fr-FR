---
solution: Journey Optimizer
product: journey optimizer
title: Notes de mise à jour
feature: Release Notes
topic: Content Management
description: Notes de mise à jour d’Adobe Journey Optimizer
exl-id: 06fa956a-b500-416e-9d42-b683c328e837
source-git-commit: 667f1a2bd03c958d7d1a95c4f9fb3378417276c0
workflow-type: tm+mt
source-wordcount: '1460'
ht-degree: 96%

---

# Notes de mise à jour {#release-notes}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card1"
>title="Nouveautés"
>abstract="**Adobe Journey Optimizer** offre en permanence de nouvelles fonctionnalités, des améliorations aux fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour."

[!DNL Adobe Journey Optimizer] offre en permanence de nouvelles fonctionnalités, des améliorations des fonctionnalités existantes et des correctifs. Toutes les modifications sont consolidées la dernière semaine de chaque mois dans ces notes de mise à jour. [!DNL Adobe Journey Optimizer] est créée de manière native sur [!DNL Adobe Experience Platform] et hérite de ses dernières innovations et améliorations. En savoir plus sur ces modifications dans les [Notes de mise à jour d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/release-notes/latest.html?lang=fr){target="_blank"}.


## Orchestration de campagne

**Date de disponibilité** : 4 août 2025

Journey Optimizer comprend désormais l’**orchestration des campagnes**, une nouvelle fonctionnalité spécialement conçue pour les campagnes par lots lancées par la marque. Cette version présente une zone de travail d’orchestration de campagne et une modélisation des données améliorée, qui fonctionnent ensemble pour permettre aux spécialistes marketing de planifier, de cibler et de diffuser des campagnes cross-canal personnalisées.

>[!IMPORTANT]
>
>Pour accéder à l’orchestration de Campaign, votre licence doit inclure le package **Journey Optimizer - Campagnes et Parcours** ou **Journey Optimizer - Campagnes**. Contactez votre représentant Adobe pour confirmer votre licence et effectuer une mise à jour si nécessaire.

![GIF de l’orchestration de campagne](assets/do-not-localize/release.gif)

Elle comprend des [jeux de données et des schémas relationnels](#oc-relational) et une [zone de travail de campagne](#oc-canvas). Ensemble, ces deux innovations ouvrent la voie à un nouveau standard d’orchestration des campagnes par lots dans Journey Optimizer. Les fonctionnalités principales sont répertoriées ci-dessous.

### Fonctionnalités principales {#oc-capabilities}

* **Workflows à plusieurs étapes**

  Pilotez des campagnes par lots multicanaux sophistiquées avec la nouvelle zone de travail personnalisée pour l’orchestration de campagne.

* **Audiences à la demande**

  Segmentez les audiences à la demande pour une activation immédiate.

* **Segmentation d’entités multiples**

  Créez des audiences à l’aide du contexte commercial (dimensions autres que les personnes), par exemple les produits, les magasins, les renouvellements, les réservations, etc.

* **Visibilité avant envoi**

  Examinez, affiner et optimiser les audiences et les campagnes avant le lancement et pendant l’exécution des campagnes.

### Zone de travail de campagne {#oc-canvas}

Une toute nouvelle interface d’orchestration visuelle, conçue spécialement pour les campagnes par lots. Cette zone de travail permet d’effectuer les opérations suivantes :

* Planification visuelle des flux de campagnes multicanaux et à plusieurs étapes

* Prise en charge des audiences à la demande créées à partir de requêtes relationnelles

* Partage d’audience, attentes et logique conditionnelle avancés

* Nombre précis de pré-envois après l’application de règles et de filtres métier

### Jeux de données et schémas relationnels {#oc-relational}

Adobe Journey Optimizer prend désormais en charge les entités relationnelles (par exemple, les produits, les magasins, les réservations, les contrats) liées à des profils basés sur des personnes. Cela permet la segmentation et la personnalisation sur des structures de données multidimensionnelles, en activant des cas d’utilisation tels que :

* Un message par réservation, abonnement ou contrat

* Segmentation basée sur les attributs d’entité associés (par exemple, catégorie de produits ou emplacement de magasin)

* Adressabilité améliorée (par exemple, envoi à tous les contacts connus liés à une entité)

### Importance de ces éléments

Cette version donne aux spécialistes marketing un contrôle total sur le marketing par lots initié par la marque et basé sur l’audience, en combinant la modélisation flexible des données avec une expérience d’orchestration personnalisée. Elle est spécialement conçue pour l’orchestration de campagne par lots à partir de parcours en temps réel, tout en offrant une personnalisation et une évolutivité avancées.

### En savoir plus

Pour en savoir plus, consultez la [documentation sur l’orchestration de campagne](../orchestrated/gs-orchestrated-campaigns.md).

<!--
## August '25 pre release notes {#25-7-rn}

**Pre release notes below are subject to change without prior notice until the release availability date**. Links, screens and updated documentation are published at the release date.

See also [Adobe Experience Platform Pre-release notes](https://experienceleague.adobe.com/fr/docs/experience-platform/release-notes/pre-release-notes){target="_blank"}.

**Release date**: August 19, 2025


### New capabilities {#Aug-25-8-features}

New capabilities coming with this release are detailed below.

### Improvements {#Aug-25-8-improv}

Improvements coming with this release are listed below.
-->

## Mises à jour d’août 2025 {#25.8-rn}

<table>
<thead>
<tr>
<th><strong>Optimisation des campagnes</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Journey Optimizer vous fournit désormais les outils nécessaires pour diffuser du contenu personnalisé et optimisé à l’audience de vos campagnes. Vous pouvez ainsi exécuter des expériences de contenu, créer un ciblage basé sur des règles et utiliser des combinaisons avancées des deux pour optimiser l’efficacité de vos campagnes.</p>
<p>Avec l’optimisation, vous pouvez réaliser les actions suivantes :</p>
<ul>
<li>Tester plusieurs variations de contenu pour identifier le message le plus efficace.</li>
<li>Diffuser du contenu personnalisé en fonction des attributs d’utilisation et des données contextuelles.</li>
<li>Combiner le ciblage et l’expérimentation pour obtenir des stratégies de campagne avancées.</li>
<li>Filtrer les utilisateurs et utilisatrices qui ne correspondent pas aux critères de variante.</li>
<li>Garantir des mécanismes de secours pour maintenir l’interaction client.</li>
</ul>
<P>Une fois la campagne active, les profils sont évalués en fonction des critères définis. Puis, en fonction des critères correspondants, ils sont diffusés avec l’expérience ou le contenu approprié de la campagne.</p>
<p><img src="assets/do-not-localize/campaign-optimization.gif"/></p>
<p>Date de publication : 8 août 2025</p>
<p>Pour plus d’informations, consultez la <a href="../campaigns/campaigns-message-optimization.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>



## Notes de mise à jour de juillet 2025 {#25-7-rn}

**Date de publication** : 29 juillet 2025

### Nouvelles fonctionnalités {#features-25-7}

Les nouvelles fonctionnalités de cette version sont présentées ci-dessous.

#### Fonctionnalités

<table>
<thead>
<tr>
<th><strong>Marques</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais créer et personnaliser vos propres marques pour définir clairement votre identité visuelle et verbale dans les communications. Grâce au score d’alignement de la marque, vous pouvez recevoir des commentaires en temps réel sur la cohérence de votre contenu avec le ton, le style et les directives de votre marque, ce qui vous permet de vous assurer que chaque message envoyé soit constamment en phase avec la marque.</p>
<p>Publiée précédemment en version Beta, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).</p>
<p><img src="assets/do-not-localize/brand-score.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../content-management/brands.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Utiliser la prise de décision dans le canal e-mail</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais ajouter des politiques de décision dans des parcours et des campagnes par e-mail. Les politiques de décision sont des conteneurs pour vos offres qui tirent profit du moteur de prise de décision afin d’effectuer un rendu dynamique du meilleur contenu à diffuser, pour chaque membre de l’audience.</p>
<p>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour obtenir l’accès.</p>
Pour plus d’informations, consultez la <a href="../experience-decisioning/create-decision.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Canal LINE</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Adobe Journey Optimizer a étendu ses fonctionnalités cross-canal afin d’inclure la prise en charge du canal LINE. Cette amélioration vous permet de créer, de modifier et de prévisualiser des expériences LINE offrant des interactions davantage personnalisées et plus attrayantes. Avec LINE, vous pouvez entrer en contact avec davantage de clientes et clients, envoyer du contenu pertinent et améliorer votre engagement.</p>
<p>Auparavant disponible uniquement sur demande, le canal LINE est désormais disponible pour tous les utilisateurs et utilisatrices (disponibilité générale).</p>
<p>Pour plus d’informations, consultez la <a href="../../rp_landing_pages/line-landing-page.md">documentation détaillée</a>.</p></td>
</tr>
</tbody>
</table>

<table>
<thead>
<tr>
<th><strong>Test à blanc du parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>L’essai de parcours est un mode de publication de parcours spécial dans Adobe Journey Optimizer qui permet aux concepteurs et conceptrices de tester un parcours à l’aide de données de production réelles sans contacter les clients et clientes ni modifier les informations de profil. Cette fonctionnalité permet aux concepteurs et conceptrices du parcours de valider leur conception et leur ciblage d’audience avant de publier le parcours.</p>
<img src="assets/do-not-localize/DryRun.gif">
<p>Publiée précédemment en disponibilité limitée, cette fonctionnalité est désormais disponible dans tous les environnements (disponibilité générale).</p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/journey-dry-run.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>


<table>
<thead>
<tr>
<th><strong>ID supplémentaire pour les parcours</strong><br/></th>
</tr>
</thead>
<tbody>
<tr>
<td>
<p>Vous pouvez désormais déclencher des parcours à l’aide d’un identifiant de profil ainsi que d’un autre identifiant, tel qu’un identifiant de commande, d’abonnement ou de prescription, ce qui permet au même profil de se trouver plusieurs fois dans le même parcours à la fois. Cela permet des scénarios tels que la gestion de plusieurs commandes ou abonnements en parallèle, chaque instance suivant son propre chemin d’accès dans le parcours.</p>
<p>Publiée précédemment en disponibilité limitée, l’utilisation d’ID supplémentaires dans les parcours est désormais disponible pour tous les environnements. Avec cette version en disponibilité générale, la fonctionnalité prend désormais en charge les parcours Lecture d’audience.</p>
<p><img src="assets/do-not-localize/gif-supplemental.gif"/></p>
<p>Pour plus d’informations, consultez la <a href="../building-journeys/supplemental-identifier.md">documentation détaillée</a>.</p>
</td>
</tr>
</tbody>
</table>

### Alertes intégrées au produit

Vous pouvez désormais vous abonner à des **alertes par e-mail et intégrées aux produits** pour connaître les mises à jour des produits Journey Optimizer.

Pour vous abonner :

* Accédez aux **préférences d’Adobe Experience Cloud**.
* Sous **Notifications**, recherchez **Nouvelles versions de Journey Optimizer**.
* Activer les notifications in-app et par e-mail

![](assets/do-not-localize/pulse-notif.png){width="70%" align="left"}


### Modification des conditions du parcours {#ee-change@}

À compter du 8 juillet, dans les nouvelles organisations clients, la création d’expressions à l’aide d’événements d’expérience n’est plus prise en charge dans l’éditeur d’expression utilisé dans les conditions de parcours. Par conséquent, les événements d’expérience dans la [source de données Experience Platform](../datasource/adobe-experience-platform-data-source.md) ne peuvent pas être utilisés pour créer des expressions. Les autres approches et bonnes pratiques pour créer des expressions/logiques avec des événements d’expérience sont référencées [ici](../building-journeys/exp-event-lookup.md).

L’accès aux données d’événement de contexte de parcours dans les parcours unitaires reste inchangé. Dans les éditeurs d’expression et de personnalisation, les utilisateurs et utilisatrices peuvent continuer à accéder aux données transmises avec l’événement de parcours initial.

Pour en savoir plus, consultez [ces questions fréquentes](../building-journeys/exp-event-lookup.md#faq-ee).

### Améliorations {#25-7-improv}

Les améliorations de cette version sont présentées ci-dessous.

* **Campagnes**

   * **Plusieurs actions entrantes dans les campagnes** : pour simplifier l’orchestration de campagne, vous pouvez désormais définir plusieurs actions entrantes dans une seule campagne. Cette fonctionnalité permet de diffuser plusieurs expériences basées sur du code, messages in-app, cartes de contenu ou actions web à différents emplacements en même temps, chaque action comportant du contenu spécifique.
     [En savoir plus](../campaigns/campaign-action.md#multi-action)

   * **Réorganisation de l’inventaire des campagnes** : les campagnes planifiées et déclenchées par API sont désormais divisées en onglets distincts dans l’inventaire des campagnes pour une navigation et une gestion plus faciles.

[En savoir plus](../campaigns/modify-stop-campaign.md)

* **Gestion des données**
   * **Mise à jour des jeux de données du système de gestion des décisions** : les offres personnalisées et de secours supprimées sont désormais marquées comme étant archivées dans les jeux de données « decision_object_repository_personalized_offers » et « decision_object_repository_fallback_offers ». Les enregistrements existants du jeu de données ne sont pas modifiés.

[En savoir plus](../offers/export-catalog/access-dataset.md)

* **Parcours**
   * **Améliorations des outils de sandbox de parcours** : lors de la copie de parcours dans plusieurs sandbox à l’aide des fonctionnalités d’export et d’import de package, les fonctionnalités suivantes sont désormais également disponibles :
      * Sélectionner un événement existant au niveau de la destination
      * Copier sur un événement indépendamment d’un parcours
      * Détecter des relations entre les groupes de champs et les sources de données, effectuer des liaisons vers ces dernières au niveau de la destination si elles existent, les créer si elles n’existent pas.

[En savoir plus](../configuration/copy-objects-to-sandbox.md)

* **Canal - In-app**
   * **Paires clé/valeur in-app** : avec les messages in-app, vous pouvez définir des paires clé/valeur pour inclure des variables personnalisées dans la payload du message. Ces paires clé-valeur vous permettent de transmettre des données supplémentaires en fonction de votre configuration et de votre cas d’utilisation spécifiques. [En savoir plus](../in-app/design-in-app.md)

* **Canal - Carte de contenu**

   * **Disqualification de campagne basée sur des règles** : lors de la modification de règles de diffusion supplémentaires, l’option Règles de diffusion précédente a été remplacée par trois types de règles distincts pour mieux contrôler le timing et la visibilité des messages :
      * Afficher le message si : conditions qui déterminent le moment auquel la carte de contenu est affichée.
      * Ignorer le message si : conditions qui masquent temporairement la carte de contenu. Elle peut réapparaître si les conditions d’affichage sont à nouveau remplies.
      * Disqualifier le message si : conditions qui empêchent définitivement l’affichage de la carte de contenu.

[En savoir plus](../content-card/design-content-card.md)

* **Prise de décision**
   * **API d’outils de migration** : l’équipe Journey Optimizer travaille actuellement sur des API d’outils de migration pour migrer les entités de gestion de décision vers la prise de décision. Ces outils permettent une migration transparente entre les sandbox avec des fonctionnalités de résolution de dépendance et de restauration. Si cela vous intéresse, contactez votre représentant ou représentante Adobe.

* **Personnalisation**
   * Une nouvelle fonction d’assistance, « SHA256 », a été ajoutée à l’éditeur de personnalisation. Cette fonction est utilisée pour calculer et renvoyer le hachage sha256 d’une chaîne.

[En savoir plus](../personalization/functions/string.md#sha256)
