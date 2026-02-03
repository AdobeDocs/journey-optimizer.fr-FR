---
solution: Journey Optimizer
product: journey optimizer
title: Défis de fidélité
description: Découvrez comment créer et gérer des défis de fidélité dans Adobe Journey Optimizer pour créer des programmes de fidélité attrayants.
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private Beta" type="Informative"
version: Journey Orchestration
source-git-commit: ef8f7754b689491bb052023ffbef0c8400dd79fe
workflow-type: tm+mt
source-wordcount: '5146'
ht-degree: 1%

---


# Défis de fidélité {#loyalty-challenges}

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version **Private Beta** et peut ne pas être disponible dans votre environnement. Contactez votre représentant ou représentante Adobe pour en obtenir l’accès.

Les défis de fidélité vous permettent de créer des offres d’engagement personnalisées pour vos clients et d’orchestrer des programmes de fidélité à grande échelle. Vous pouvez concevoir des défis avec des tâches et des jalons spécifiques, récompenser les clients qui les ont réalisés et leur offrir une expérience via les canaux Adobe Journey Optimizer.

>[!BEGINSHADEBOX]
>
>**Dans ce guide :**
>
>* [Aperçu](#overview) - Comprenez ce qu’offrent les défis de fidélité
>* [Fonctionnement &#x200B;](#how-it-works) - Workflow détaillé allant de la configuration à la surveillance
>* [Conditions préalables](#prerequisites) - Configurer l’ingestion des données et les autorisations
>* [Accéder aux défis de fidélité](#access) - Ouvrez le menu et affichez les défis
>* [Créer des défis](#create-challenges) - Créez de nouveaux défis de fidélité
>* [Créer des tâches](#create-tasks) - Définissez ce que les clients doivent faire
>* [Gérer les défis](#manage-challenges) - Modifier, surveiller et optimiser
>
>[!ENDSHADEBOX]

## Vue d’ensemble {#overview}

Les défis de fidélité vous permettent de concevoir et de déployer des offres d’engagement personnalisées qui motivent les clients à effectuer des actions spécifiques et à gagner des récompenses. Cette fonctionnalité fournit une solution complète pour créer des programmes de fidélité à grande échelle, de la définition de tâches et de jalons à la diffusion de contenu et au suivi des performances sur l’ensemble des canaux. Vous pouvez créer trois types d’expériences de défi, configurer des récompenses, envoyer des notifications multicanaux à des étapes clés du cycle de vie et surveiller les performances par le biais de parcours générés automatiquement, tout en conservant l’intégration à votre système de gestion de la fidélité externe.

## Fonctionnement {#how-it-works}

La création et le lancement d’un défi de fidélité suivent ce workflow :

1. **Configurer l’ingestion des données** - Configurez les connecteurs source Experience Platform (tels que Capillaire) pour ingérer des données d’événement de fidélité qui effectuent le suivi des actions et de la progression des clients.

2. **Créer un défi** - Définissez les propriétés de base du défi, y compris le nom, le type (Standard, Streak ou Séquentiel), l’audience et la période.

3. **Ajouter des tâches** - Définissez les actions spécifiques que les clients doivent effectuer, y compris les types de tâches (achat, dépenses, visite, etc.), les quantités, les filtres de produit et les récompenses.

4. **Conception de cartes de contenu** - Créez la représentation visuelle de votre défi à l’aide de cartes de contenu Journey Optimizer qui s’affichent sur les appareils des clients.

5. **Configurer la messagerie** (facultatif) - Configurez des messages multicanaux (in-app, e-mail, push) pour les étapes clés : lancement, en cours et achèvement.

6. **Réviser et publier** - Testez votre défi avec des profils de test, puis publiez-le pour le rendre disponible auprès de votre audience cible.

7. **parcours généré automatiquement** - Lorsque vous publiez, Journey Optimizer crée automatiquement un parcours qui orchestre la diffusion et la messagerie des cartes de contenu.

8. **Activer le parcours** - Le parcours généré automatiquement est activé à la date de début de votre défi et gère toutes les interactions des clients.

9. **Surveiller les performances** - Suivez la participation, les taux d’achèvement, la distribution des récompenses et l’engagement des messages au moyen de rapports intégrés et de la zone de travail de parcours.

>[!NOTE]
>
>Le parcours généré automatiquement apparaît dans votre inventaire de parcours et peut être personnalisé si nécessaire. Toutefois, les modifications apportées directement au parcours ne sont pas resynchronisées avec la configuration de défi.

## Fonctionnalités principales

Utilisez les défis de fidélité pour :

* **Créez trois types de défis** :
   * **Standard** : les clients effectuent un certain nombre de tâches pour gagner des récompenses.
   * **Streak** : les clients effectuent la même tâche plusieurs fois.
   * **Séquentiel** : les clients exécutent des tâches dans un ordre spécifique.

* **Conception du contenu du défi** : utilisez des cartes de contenu Journey Optimizer pour créer la représentation visuelle de votre défi sur les appareils des clients. Les cartes de contenu affichent les informations sur le défi, la progression et les récompenses sur l’appareil du client.

* **Configurer les exigences de tâche** : définissez ce que les clients doivent faire pour gagner des récompenses, notamment :
   * Types de tâches (achat, montant des dépenses, visite, etc.)
   * Exigences de quantité
   * Inclusions/exclusions de produits à l’aide de SKU
   * Attributs et conditions personnalisés

* **Configurer les récompenses** : définissez les récompenses que les clients gagnent à l’achèvement de la tâche ou après avoir relevé l’ensemble du défi

* **Envoyer des notifications** : diffusez des messages sur plusieurs canaux (in-app, e-mail, push) à des étapes clés :
   * **Launch** : quand le défi commence
   * **En cours** : lorsque les clients sont à mi-chemin
   * **Terminé** : lorsque les clients terminent le défi

* **Suivre les performances** : surveiller les parcours générés automatiquement et examiner les performances des défis

### Limites importantes {#limitations}

* **Aucun système comptable** : Loyalty Challenges ne suit pas les valeurs monétaires ou les soldes en points. Lorsque les clients relèvent un défi et gagnent une récompense, Journey Optimizer appelle votre système de gestion de la fidélité externe pour gérer l’affectation des points.

* **Sélection d’audience uniquement** : vous pouvez sélectionner des audiences existantes, mais ne pouvez pas créer de nouvelles audiences à partir de l’interface utilisateur des défis de fidélité.

## Conditions préalables {#prerequisites}

Avant d’utiliser les défis de fidélité, vérifiez que vous disposez des éléments suivants :

* Configuration de l’ingestion des données

  Les défis de fidélité reposent sur des données ingérées par le biais des connecteurs source Experience Platform pour suivre la progression des clients et l’achèvement des tâches.

   1. **Configuration d&#39;un connecteur source pris en charge** : actuellement, le connecteur capillaire est généralement disponible. Des connecteurs supplémentaires sont prévus.

   2. **Valider l’ingestion des données** : assurez-vous que les événements de fidélité et les données client circulent dans Experience Platform et sont disponibles dans Journey Optimizer.

  Pour obtenir des instructions détaillées, voir :

   * [Documentation sur les sources Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/sources/home)
   * [Configuration des connecteurs source dans Journey Optimizer](../start/get-started-sources.md)

* Autorisations nécessaires {#required-permissions}

Pour utiliser les défis de fidélité, vous avez besoin des autorisations appropriées dans Journey Optimizer. Contactez votre administrateur si vous ne pouvez pas accéder à la fonctionnalité.

## Accès aux défis de fidélité {#access}

Pour accéder aux défis de fidélité :

1. Dans Adobe Journey Optimizer, sélectionnez **[!UICONTROL Défis de fidélité]** dans le menu de navigation de gauche.

   <!--![Loyalty challenges menu in left navigation](assets/loyalty-challenges-menu.png)-->

2. L’inventaire des défis de fidélité répertorie tous les défis existants avec des informations telles que :
   * Nom et description du défi
   * Statut (brouillon, actif, arrêté, etc.)
   * Type de défi (Standard, Séquentiel, Séquentiel)
   * Dates de début et de fin
   * Date de la dernière modification

   <!--![Loyalty challenges inventory showing list of challenges](assets/loyalty-challenges-inventory.png)-->

3. Sélectionnez **[!UICONTROL Créer un défi]** pour commencer à créer un nouveau défi.

### Défis liés à la recherche et au filtrage {#search-filter}

Utilisez les fonctionnalités de recherche et de filtrage pour trouver rapidement des défis spécifiques :

#### Recherche {#search}

Saisissez le nom du défi ou les mots-clés pour trouver les défis correspondants dans le champ **[!UICONTROL Rechercher]**.

#### Filtrer par statut {#filter-by-status}

Affichez les défis avec des statuts spécifiques dans **[!UICONTROL Filtrer par statut]** :

* Brouillon
* Planifiés
* Dynamique
* Terminé
* Arrêté
* Archivé

#### Filtrer par type {#filter-by-type}

Afficher uniquement les défis standard, en traînée ou séquentiels à l’aide de **[!UICONTROL Filtrer par type]**.

#### Filtrage par date {#filter-by-date}

Affichez les défis au sein d’une période spécifique à l’aide de **[!UICONTROL Filtrer par date]**.

#### Filtrer par balises {#filter-by-tags}

Afficher les défis liés à des balises spécifiques appliquées à l’aide de **[!UICONTROL Filtrer par balises]**.


**[!UICONTROL Remise]** : indiquez un code ou une valeur de remise.

* Saisir le type de remise (pourcentage ou montant fixe)
* Saisir la valeur de remise
* Indiquez éventuellement un code remise ou laissez le système en générer un

**[!UICONTROL Article gratuit]** : Accordez un produit ou un service gratuit.

* Spécifier le SKU ou la description de l’élément
* Indiquer comment l’article gratuit doit être demandé

**[!UICONTROL Récompense personnalisée]** : définissez un type de récompense personnalisée.

* Saisir la description de la récompense
* Fournissez tous codes ou identifiants pertinents
* Configurer la manière dont la récompense est remise ou demandée

#### Exemple de configuration de récompense {#reward-example}

**Challenge** : « Défi de l&#39;amoureux du café »

**Tâche 1** : Achat de 3 cafés

* Récompense : 30 points (10 points par café)
* Planning : une fois la tâche terminée

**Tâche 2** : Essayez 2 nouvelles boissons de saison

* Récompense : 50 points
* Planning : une fois la tâche terminée

**Récompense d’accomplissement du défi** :

* Récompense : café gratuit + 100 points bonus
* Planning : une fois toutes les tâches terminées

**Récompenses possibles totales** : 180 points + 1 café gratuit

### Attributs de tâche avancés {#advanced-attributes}

Pour les cas d’utilisation avancés, vous pouvez configurer des attributs de tâche supplémentaires :

**[!UICONTROL Conditions personnalisées]** : ajoutez une logique ou des conditions personnalisées au-delà des types de tâches standard à l’aide de segments ou de règles Experience Platform.

**[!UICONTROL Géofencing]** : (pour les tâches de visite) Nécessite des visites à des emplacements spécifiques définis par des coordonnées géographiques et un rayon.

**[!UICONTROL Exigences temporelles]** : exigent que les tâches soient terminées au cours d’heures, de jours ou de périodes spécifiques.

**[!UICONTROL Période de réflexion]** : définissez un temps minimum entre les tâches terminées pour éviter des actions répétées rapides.

**[!UICONTROL Dépendances de tâches]** : (pour les défis séquentiels) définissez les conditions préalables qui doivent être remplies avant que cette tâche ne soit disponible.

## Créer des défis {#create-challenges}

Créez un défi de fidélité pour définir l’offre d’engagement, configurer les cartes de contenu pour la diffusion, ajouter des tâches, configurer des récompenses et éventuellement configurer la messagerie sur plusieurs canaux.

### Avant de commencer {#before-you-start}

Avant de créer un défi, vérifiez que vous disposez des éléments suivants :

* Ingestion de données configurée et validée via les connecteurs source
* Création des audiences requises dans Experience Platform
* Préparation des ressources de contenu (images, texte, etc.) pour votre défi
* Défini les tâches et les récompenses que vous souhaitez offrir

### Créer un défi {#create-a-challenge}

Pour créer un nouveau défi de fidélité :

1. Dans Journey Optimizer, sélectionnez **[!UICONTROL Défis de fidélité]** dans le menu de navigation de gauche.

2. Sélectionnez **[!UICONTROL Créer un défi]** dans le coin supérieur droit.

   <!--![Create challenge button in loyalty challenges inventory](assets/create-challenge-button.png)-->

3. Dans l’écran des propriétés du défi, configurez les éléments suivants :

#### Propriétés de base {#basic-properties}

**[!UICONTROL Nom]** : saisissez un nom explicite pour votre défi. Ce nom apparaît dans l’inventaire et est inclus dans le nom du parcours généré automatiquement.

**[!UICONTROL Description]** : (facultatif) ajoutez une description pour vous aider, vous et votre équipe, à comprendre l’objectif et les détails de ce défi.

**[!UICONTROL Type de défi]** : sélectionnez le type de défi que vous souhaitez créer :

* **[!UICONTROL Standard]** : les clients peuvent effectuer un nombre illimité de tâches spécifiées dans n’importe quel ordre pour obtenir la récompense. Exemple : « Effectuer 5 achats ce mois-ci ».

* **[!UICONTROL Streak]** : les clients doivent effectuer la même tâche à plusieurs reprises. Exemple : « Visitez notre magasin 10 fois de suite. »

* **[!UICONTROL Séquentiel]** : les clients doivent effectuer des tâches dans un ordre spécifique. Exemple : « Effectuez d’abord un achat, puis rédigez un avis, puis recommandez un ami. »

<!--![Challenge type selection showing Standard, Streak, and Sequential options](assets/challenge-type-selection.png)-->

**[!UICONTROL Date de début]** : sélectionnez le moment où le défi devient actif et disponible pour les clients.

**[!UICONTROL Date de fin]** : sélectionnez le moment où le défi expire. Les clients qui n’ont pas terminé le défi à cette date ne pourront plus obtenir la récompense.

#### Sélection d’audience {#audience-selection}

**[!UICONTROL Sélectionner une audience]** : sélectionnez l’audience éligible à ce défi. Vous pouvez uniquement sélectionner des audiences existantes ; vous ne pouvez pas créer de nouvelles audiences à partir de l’interface utilisateur Défis de fidélité.

Pour créer ou affiner des audiences, voir [Création d’audiences dans Journey Optimizer](../audience/about-audiences.md).

1. Sélectionnez **[!UICONTROL Enregistrer comme brouillon]** pour continuer à configurer votre défi.

## Création de tâches {#create-tasks}

Les tâches définissent les actions ou jalons spécifiques que les clients doivent effectuer pour gagner des récompenses dans un défi de fidélité. Vous pouvez configurer les types de tâches, les quantités, les exigences en matière de produits et les valeurs de récompense pour créer des expériences de fidélité attrayantes et personnalisées.

### Vue d’ensemble des tâches {#task-overview}

Chaque tâche représente une action mesurable qui contribue à l&#39;achèvement du défi. Selon votre type de défi (Standard, Séquentiel ou Séquentiel), les clients exécutent les tâches différemment :

* **Défis standard** : les clients effectuent un nombre spécifié de tâches dans n’importe quel ordre
* **Défis en série** : les clients effectuent la même tâche plusieurs fois de suite
* **Défis séquentiels** : les clients exécutent des tâches dans un ordre défini

### Ajouter une tâche {#add-task}

Pour ajouter une tâche à votre défi :

1. Ouvrez votre défi ou créez-en un nouveau.

2. Accédez à la section **[!UICONTROL Tâches]**.

   <!--![Tasks section in challenge creation interface](assets/tasks-section.png)-->

3. Sélectionnez **[!UICONTROL Ajouter une tâche]** ou **[!UICONTROL Créer une tâche]**.

4. Dans l’écran de création de la tâche, configurez les propriétés suivantes.

### Propriétés de la tâche {#task-properties}

#### Informations de base sur la tâche {#basic-info}

**[!UICONTROL Nom de la tâche]** : saisissez un nom explicite pour la tâche. Ce nom est visible pour vous et votre équipe, mais peut ne pas être affiché pour les clients selon la conception de votre carte de contenu.

**[!UICONTROL Description de la tâche]** : (facultatif) ajoutez des détails sur l’objectif ou les exigences de la tâche.

**[!UICONTROL Type de tâche]** : sélectionnez le type d’action que les clients doivent effectuer. Les types de tâches disponibles sont les suivants :

* **[!UICONTROL Achat]** : le client effectue une transaction d’achat
* **[!UICONTROL Montant des dépenses]** : le client dépense un montant monétaire spécifié
* **[!UICONTROL Visite]** : le client visite un emplacement physique ou une propriété numérique
* **[!UICONTROL Engagement]** : le client s’engage dans le contenu, par exemple en regardant une vidéo ou en lisant un article
* **[!UICONTROL Événement personnalisé]** : le client déclenche un événement personnalisé suivi via votre ingestion de données

<!--![Task type selection dropdown showing available task types](assets/task-type-selection.png)-->

#### Exigences de quantité {#quantity-requirements}

**[!UICONTROL Quantité requise]** : indiquez le nombre de fois où le client doit effectuer la tâche pour l’effectuer.

Par exemple :

* Pour une tâche Achat : « Acheter 2 articles » (quantité = 2)
* Pour une tâche de montant des dépenses : « Dépense 50 $ » (quantité = 50)
* Pour une tâche Visite : « Visite 5 fois » (quantité = 5)

**[!UICONTROL Période de suivi]** : (facultatif) définissez la période pendant laquelle cette tâche doit être terminée :

* Par durée du défi (par défaut)
* Par jour
* Par semaine
* Par mois
* Période personnalisée

### Filtrage des produits et des SKU {#product-filtering}

Pour les tâches de montant d’achat et de dépense, vous pouvez spécifier quels produits sont qualifiés pour l’achèvement de la tâche.

#### Inclusions des produits {#product-inclusions}

Définissez les produits ou catégories qui seront pris en compte dans la tâche :

1. Sélectionnez **[!UICONTROL Ajouter des critères de produit]**.

   <!--![Add product criteria button in task configuration](assets/add-product-criteria.png)-->

2. Choisissez comment définir les produits admissibles :
   * **[!UICONTROL Par SKU]** : saisissez des codes SKU de produit spécifiques.
   * **[!UICONTROL Par catégorie]** : sélectionnez les catégories de produits dans votre catalogue.
   * **[!UICONTROL Par attribut]** : filtrez par attributs de produit tels que la marque, la taille, la couleur ou les attributs personnalisés.

3. Saisissez ou sélectionnez les identifiants de produit :

   **Exemple - Par SKU** :

   ```text
   SKU001, SKU002, SKU003
   ```

   **Exemple - Par catégorie** :

   * Boissons > Café
   * Boulangerie > Pâtisseries

   **Exemple - Par attribut** :

   * Marque = « Marque Premium »
   * Catégorie = « Articles Saisonniers »
   * Prix > 20 $

4. Sélectionnez **[!UICONTROL Ajouter]** pour enregistrer les critères de produit.

#### Exclusions de produits {#product-exclusions}

Facultativement, excluez des produits spécifiques de l’inventaire pour la tâche :

1. Sélectionnez **[!UICONTROL Ajouter des exclusions]**.

2. Utilisez les mêmes méthodes de filtrage que les inclusions de produits pour spécifier les produits à exclure.

3. Scénarios d’exclusion courants :

   * Articles de vente ou de dédouanement
   * Cartes cadeaux
   * Articles promotionnels ou gratuits
   * Marques ou catégories spécifiques

>[!NOTE]
>
>**Logique d’inclusion et d’exclusion** : lorsque des inclusions et des exclusions sont définies :
>
>* Les produits doivent correspondre aux critères d’inclusion.
>* Les produits répondant aux critères d’exclusion sont supprimés, même s’ils correspondent aux inclusions
>* Si aucune inclusion n’est définie, tous les produits sont qualifiés, sauf ceux qui sont explicitement exclus

#### Exemples de filtrage de produits {#product-filtering-examples}

##### Exemple 1 : défi Café {#example-1}

* Type de tâche : Achat
* Quantité requise : 3
* Inclusions : Catégorie = « Boissons > Café »
* Résultat : le client doit acheter 3 boissons au café

##### Exemple 2 : dépenses de primes {#example-2}

* Type de tâche : Montant des dépenses
* Quantité requise : 100 $
* Inclusions : Marque = « Marque Premium »
* Exclusions : Catégorie = « Clairance »
* Résultat : le client doit dépenser 100 $ sur des articles de marque Premium, à l’exclusion des articles de dédouanement

##### Exemple 3 : achat de produits spécifiques {#example-3}

* Type de tâche : Achat
* Quantité requise : 1
* Inclusions : SKU = « NEWPRODUCT2024 »
* Résultat : le client doit acheter le produit spécifique avec le SKU « NEWPRODUCT2024 »

### Configurer les récompenses {#configure-rewards}

Définissez ce que les clients gagnent pour exécuter les tâches. Les récompenses peuvent être accordées au niveau de la tâche ou du défi une fois toutes les tâches terminées.

#### Timing de récompense {#reward-timing}

Choisissez quand les clients reçoivent des récompenses :

**[!UICONTROL Une fois la tâche terminée]** : les clients reçoivent une récompense immédiatement après avoir terminé cette tâche spécifique (également appelée « récompenses progressives » ou « récompenses jalonnées »).

**[!UICONTROL Après l’achèvement du défi]** : les clients ne reçoivent une récompense qu’après avoir terminé toutes les tâches requises pour le défi (également appelées « récompenses finales » ou « grands prix »).

>[!TIP]
>
>Vous pouvez combiner les deux types de récompense dans un seul défi pour maintenir l’engagement sur l’ensemble du parcours client. Par exemple :
>
>* Accorder 10 points après chaque accomplissement de la tâche (récompenses progressives)
>* Donnez 100 points supplémentaires après avoir terminé le défi entier (récompense finale)

#### Types et valeurs de récompense {#reward-types}

**[!UICONTROL Points]** : attribuez des points de fidélité au compte du client.

* Entrez le nombre de points (par exemple, 100)
* Les points sont communiqués à votre système de gestion de la fidélité externe via l’API

## Configuration des cartes de contenu {#configure-content-cards}

Les cartes de contenu sont la principale manière dont les défis sont affichés pour les clients sur leurs appareils. Vous devez configurer une carte de contenu pour votre défi.

1. Dans votre défi, accédez à l’onglet **[!UICONTROL Contenu]**.

2. Sélectionnez **[!UICONTROL Modifier le contenu]** pour ouvrir l’éditeur de carte de contenu.

   <!--![Content tab with Edit content button](assets/content-tab-edit.png)-->

3. Configurez les propriétés de la carte de contenu :

   **[!UICONTROL Nom de la configuration]** : saisissez un nom pour cette configuration de carte de contenu.

   **[!UICONTROL Configuration]** : sélectionnez ou créez une configuration de carte de contenu. Cette option définit les paramètres techniques de diffusion de la carte de contenu.

4. Dans l’éditeur de carte de contenu, concevez votre carte de défi :

   * Ajoutez du texte pour décrire le défi, les tâches et les récompenses
   * Inclure des images ou d’autres éléments visuels
   * Utiliser la personnalisation pour inclure des informations spécifiques au client
   * Afficher les indicateurs de progression, le cas échéant
   * Ajout de boutons call-to-action

   L’éditeur de carte de contenu offre les mêmes fonctionnalités que les autres canaux Journey Optimizer. Pour obtenir des conseils détaillés, voir [Conception de cartes de contenu](../content-card/design-content-card.md).

5. Sélectionnez **[!UICONTROL Enregistrer]** pour enregistrer la configuration de votre carte de contenu.

>[!NOTE]
>
>La carte de contenu est diffusée par le biais du parcours généré automatiquement. Il s’affiche pour les membres de l’audience éligibles lorsque le défi est actif.

## Configurer la messagerie {#configure-messaging}

Vous pouvez éventuellement configurer les messages à envoyer aux clients à des étapes clés du cycle de vie du défi. Les messages sont disponibles en trois étapes :

* **[!UICONTROL Launch]** : envoyez un message lorsque le défi devient actif
* **[!UICONTROL En cours]** : envoyez un message lorsque les clients sont à mi-chemin du défi
* **[!UICONTROL Terminé]** : envoyez un message lorsque les clients relèvent le défi

### Ajouter des messages {#add-messages}

1. Dans votre défi, accédez à l’onglet **[!UICONTROL Messagerie]**.

   <!--![Messaging tab showing Launch, In progress, and Complete stages](assets/messaging-tab-stages.png)-->

2. Sélectionnez l’étape à laquelle vous souhaitez ajouter un message : Lancement, En cours ou Terminé.

3. Sélectionnez **[!UICONTROL Ajouter un message]**.

4. Choisissez le canal de votre message :
   * **[!UICONTROL In-app]** : affichez un message dans votre application
   * **[!UICONTROL Email]** : envoyez une notification par e-mail
   * **[!UICONTROL Push]** : envoyer une notification push

5. Sélectionnez **[!UICONTROL Modifier le contenu]** pour ouvrir l’éditeur de contenu pour le canal sélectionné.

6. Concevez votre message à l’aide de l’éditeur de contenu standard :
   * Ajouter du texte, des images et d’autres éléments de contenu
   * Utiliser la personnalisation pour inclure des informations spécifiques au client
   * Inclure les détails du défi comme la progression ou les récompenses
   * Ajouter du contenu dynamique en fonction des attributs ou des comportements du client

   Pour obtenir des conseils spécifiques aux canaux, voir :
   * [Créer des messages in-app](../in-app/create-in-app.md)
   * [Créer des e-mails](../email/create-email.md)
   * [Créer des notifications push](../push/create-push.md)

7. Sélectionnez **[!UICONTROL Enregistrer]** pour enregistrer votre message.

8. Répétez ces étapes pour ajouter des messages pour d’autres étapes ou canaux selon les besoins.

>[!NOTE]
>
>Vous pouvez ajouter plusieurs messages par étape, ce qui vous permet d’atteindre les clients sur différents canaux. Par exemple, vous pouvez envoyer à la fois un e-mail et une notification push lorsqu’un défi est lancé.

### Synchronisation des messages et déclencheurs {#message-timing}

**Messages de lancement** : envoyés lorsque le défi devient actif pour l’audience éligible.

**Messages en cours** : déclenché lorsque les clients atteignent un point de progression spécifié. Vous pouvez configurer les conditions de déclenchement en fonction des éléments suivants :

* Nombre de tâches terminées
* Pourcentage de défis terminés
* Achèvement de tâche spécifique
* Temps écoulé depuis le début du défi

**Messages terminés** : envoyés lorsque les clients effectuent avec succès toutes les tâches requises.

>[!TIP]
>
>**Bonnes pratiques relatives à la messagerie** :
>
>* Gardez les messages concis et concentrés sur le défi
>* Communiquez clairement la valeur et les récompenses
>* Utiliser une image de marque et un ton cohérents
>* Inclure des appels à l’action clairs
>* Tester les messages avant de publier votre défi

## Génération et personnalisation de parcours {#generate-journey}

Lorsque vous enregistrez un défi avec du contenu et des messages configurés, Journey Optimizer génère automatiquement un parcours sur le serveur principal.

### Fonctionnement de la génération de parcours {#journey-generation-process}

1. Lorsque vous enregistrez un défi et sélectionnez **[!UICONTROL Générer le parcours]**, Journey Optimizer crée un parcours.

2. Le parcours est automatiquement nommé en fonction du nom du défi (par exemple, « Défi : [ Votre nom de défi ]).

3. La zone de travail de parcours comprend :
   * Activité **[!UICONTROL Lecture d’audience]** avec l’audience que vous avez sélectionnée
   * **Carte de contenu** action de diffusion
   * **Activités de message** pour tout message que vous avez configuré (lancement, en cours, terminé)
   * **Attente** et **Condition** selon vos besoins et votre configuration

   <!--![Auto-generated journey canvas showing content card and message activities](assets/generated-journey-canvas.png)-->

4. Le parcours apparaît dans votre inventaire de parcours et est visible par tous les utilisateurs disposant des autorisations appropriées.

### Affichage du parcours généré {#view-journey}

Pour afficher le parcours généré automatiquement :

1. Accédez à **[!UICONTROL Parcours]** dans le menu de navigation de gauche.

2. Recherchez le parcours par nom de défi ou filtrez par balises si vous les avez attribuées.

3. Sélectionnez le parcours pour afficher sa zone de travail et sa configuration.

### Personnalisation du parcours {#customize-journey}

Vous pouvez modifier le parcours généré automatiquement pour ajouter une logique personnalisée, des activités supplémentaires ou des configurations avancées.

>[!IMPORTANT]
>
>**Points importants à prendre en compte lors de la modification de parcours** :
>
>* Les modifications apportées à la zone de travail de parcours **ne pas resynchroniser** dans l’interface utilisateur des défis de fidélité
>* Le défi reste la source de vérité pour la définition de l’expérience de base
>* Journey Optimizer affiche un avertissement lorsque vous passez en mode d’édition personnalisé
>* Si vous devez apporter des modifications aux tâches, aux récompenses ou aux propriétés des défis principaux, modifiez-les dans l’interface utilisateur des défis de fidélité, et non dans le parcours
>* Les modifications de parcours personnalisé sont appropriées pour la logique de routage, de minutage ou d’intégration avancée

Pour personnaliser le parcours :

1. Ouvrez le parcours généré à partir de l’inventaire des parcours.

2. Journey Optimizer affiche un avertissement relatif à la modification personnalisée. Lisez attentivement l&#39;avertissement et reconnaissez-le.

3. Effectuez les modifications souhaitées à l’aide de la zone de travail de parcours :
   * Ajouter des activités supplémentaires (attentes, conditions, actions)
   * Configurer des règles de minutage ou de fréquence avancées
   * Ajouter des actions ou des intégrations personnalisées
   * Modifier les conditions d’entrée d’audience

4. Testez minutieusement vos modifications avant de les publier.

5. Publiez le parcours une fois prêt.

Pour obtenir des conseils détaillés sur la modification de parcours, voir [Créer des parcours &#x200B;](../building-journeys/journey-gs.md).

### Considérations relatives à la zone de travail de parcours {#journey-considerations}

Lorsque vous utilisez des parcours générés automatiquement :

* **Modification impossible de l’audience dans le parcours** : si vous devez modifier l’audience, effectuez cette opération dans l’interface utilisateur des défis de fidélité et régénérez le parcours.

* **Mises à jour du contenu des messages** : les modifications du contenu des messages doivent être effectuées dans l’interface utilisateur Défis de fidélité pour maintenir la cohérence.

* **Statut du Parcours** : le statut du parcours (Brouillon, Actif, Arrêté) est géré indépendamment du statut du défi.

* **Tests** : testez l’ensemble du défi, pas seulement le parcours, pour vous assurer que tous les composants fonctionnent correctement ensemble.

## Révision et publication {#review-and-publish}

Avant de publier votre défi :

1. **Examinez tous les composants** :
   * Propriétés et dates du défi
   * Tâches et exigences relatives aux tâches
   * Configuration des récompenses
   * Conception de carte de contenu
   * Contenu et durée des messages
   * Structure de parcours générée

2. **Tester l’expérience** :
   * Utilisation de profils de test pour valider le rendu du contenu
   * Vérifiez que les tâches se déclenchent correctement en fonction des données de test
   * Vérifier la logique d’attribution de récompense
   * Tester la messagerie sur tous les canaux configurés
   * Vérifier l’exécution du parcours avec les audiences de test

3. **Publiez votre défi** :
   * Une fois prêt, sélectionnez **[!UICONTROL Publier]** dans les propriétés du défi
   * Le défi devient actif à la date de début spécifiée
   * Le parcours généré automatiquement est activé
   * Les membres de l’audience éligibles peuvent voir le défi et y participer

## Gestion des défis {#manage-challenges}

Après avoir créé et publié des défis de fidélité, vous pouvez les afficher, les modifier, les surveiller et les optimiser pour vous assurer qu’ils fournissent les résultats souhaités pour votre programme de fidélité.

### Statuts des défis {#challenge-statuses}

Chaque défi évolue au cours d’un cycle de vie reflété par son statut :

**[!UICONTROL Brouillon]** : le défi est en cours de création ou de modification, mais pas encore publié. Vous pouvez apporter des modifications aux brouillons des défis.

**[!UICONTROL Planifié]** : le défi est publié et devient actif à sa date de début. Les clients ne peuvent pas encore voir ni participer aux défis planifiés.

**[!UICONTROL En direct]** : le défi est actif et les clients de l’audience éligible peuvent le voir et y participer. Ce statut s’affiche lorsque la date actuelle est comprise entre les dates de début et de fin.

**[!UICONTROL Terminé]** : le défi a dépassé sa date de fin ou tous les objectifs ont été atteints. Les clients ne peuvent plus participer, mais vous pouvez afficher les données et les résultats historiques.

**[!UICONTROL Arrêté]** : le défi a été arrêté manuellement avant la fin. Les clients ne peuvent plus participer. Pour réactiver un défi arrêté, vous devez le dupliquer et créer une nouvelle version.

**[!UICONTROL Archivé]** : le défi a été archivé à des fins d’organisation. Les défis archivés peuvent être récupérés à l’aide de filtres, mais ils sont masqués dans la vue par défaut.

### Afficher les détails du défi {#view-details}

Pour afficher des informations détaillées sur un défi :

1. Dans l’inventaire, cliquez sur le nom du défi ou sélectionnez le menu **[!UICONTROL Autres actions]** (points de suspension) et choisissez **[!UICONTROL Afficher les détails]**.

   <!--![Challenge inventory with More actions menu highlighted](assets/challenge-more-actions.png)-->

2. L’écran des détails du défi affiche :

   Onglet **[!UICONTROL Aperçu]** :
   * Propriétés de base (nom, description, type, dates)
   * Informations sur le statut actuel et le cycle de vie
   * Informations sur l’audience
   * Historique de création et de modification

   Onglet **[!UICONTROL Tâches]** :
   * Liste de toutes les tâches du défi
   * Types de tâches, exigences et conditions
   * Récompenses configurées par tâche

   Onglet **[!UICONTROL Contenu]** :
   * Configuration et aperçu de la carte de contenu
   * Rendu visuel de la manière dont le défi apparaît aux clients

   Onglet **[!UICONTROL Messagerie]** :
   * Messages configurés pour les étapes de lancement, en cours et terminées
   * Affectations de canaux et aperçus de contenu

   Onglet **[!UICONTROL Performances]** (pour les défis actifs et terminés) :
   * Mesures de participation
   * Taux d’achèvement
   * Répartition des récompenses
   * Statistiques d’engagement des messages

### Modifier les défis {#edit-challenges}

Vous pouvez modifier les défis en fonction de leur statut actuel.

#### Modifier les brouillons de défis {#edit-draft}

Pour les défis dans l’état **[!UICONTROL Version préliminaire]** :

1. Cliquez sur le nom du défi ou sélectionnez **[!UICONTROL Modifier]** dans le menu d’actions.

2. Modifiez n’importe quel aspect du défi :
   * Propriétés de base
   * Tâches et récompenses
   * Cartes de contenu
   * Messagerie
   * Sélection d’audience

3. Sélectionnez **[!UICONTROL Enregistrer en tant que brouillon]** pour enregistrer les modifications sans publication, ou **[!UICONTROL Publier]** pour activer le défi.

#### Modifier les défis publiés {#edit-published}

Pour les défis **[!UICONTROL planifiés]** ou **[!UICONTROL en direct]** :

>[!IMPORTANT]
>
>**Impact de la modification des défis en direct** : les modifications apportées aux défis en direct peuvent affecter les clients qui participent déjà. Tenez compte des points suivants avant d’apporter des modifications :
>
>* La modification des exigences de la tâche peut invalider la progression du client
>* La modification des récompenses peut créer des incohérences pour les clients qui les ont déjà gagnées
>* Les modifications d’audience peuvent exclure les clients qui étaient auparavant éligibles
>* Les modifications de contenu apparaissent immédiatement pour les clients
>
>Pour apporter des modifications importantes, envisagez d’arrêter le défi actuel et de créer une nouvelle version.

**Modification limitée pour les défis en direct** :

Vous pouvez apporter ces modifications aux défis en direct sans les arrêter :

* Mettre à jour la description du défi (face à l’interne)
* Modification du texte et des visuels des cartes de contenu
* Mettre à jour le contenu des messages
* Ajuster la date de fin (étendre uniquement, ne pas raccourcir)
* Ajouter ou modifier des balises

**Modifications nécessitant la duplication des défis** :

Pour modifier ces propriétés, vous devez dupliquer le défi et créer une nouvelle version :

* Type de défi (Standard, Séquentiel, Séquentiel)
* Exigences et conditions relatives à la tâche
* Valeurs de récompense et règles d’attribution
* Date de début (pour les défis en direct)
* Audience (modifications majeures)

### Dupliquer un défi {#duplicate-challenge}

La duplication crée une copie d’un défi existant que vous pouvez modifier et publier en tant que nouveau défi :

1. Dans l’inventaire, sélectionnez le menu **[!UICONTROL Autres actions]** (points de suspension) correspondant au défi que vous souhaitez dupliquer.

2. Sélectionnez **[!UICONTROL Dupliquer]**.

3. Dans la boîte de dialogue de duplication :
   * Saisir un nouveau nom pour le défi dupliqué
   * Vous pouvez éventuellement modifier la description
   * Choisir s’il faut copier les paramètres de l’audience
   * Choisir si les configurations de messagerie doivent être copiées

4. Sélectionnez **[!UICONTROL Dupliquer]**.

5. Le défi dupliqué s’ouvre en mode brouillon, où vous pouvez apporter des modifications avant de le publier.

**Scénarios de duplication courants** :

* Réexécuter un défi réussi pour une nouvelle période
* Créer des variantes d’un défi pour différentes audiences
* Mettre à jour les exigences de tâche ou les récompenses pour une nouvelle version
* Réactiver un défi arrêté ou terminé

### Arrêter un défi {#stop-challenge}

Pour arrêter un défi en direct ou planifié avant sa date de fin naturelle :

1. Sélectionnez le défi dans l’inventaire.

2. Sélectionnez **[!UICONTROL Arrêter le défi]** dans le menu d’actions.

3. Dans la boîte de dialogue de confirmation, passez en revue l’impact :
   * Les clients participant actuellement ne peuvent plus progresser
   * Les clients qui ont terminé les tâches mais pas le défi complet ne recevront pas de récompenses finales
   * Le parcours associé est arrêté
   * Le défi ne peut pas être redémarré (doit être dupliqué pour être réutilisé)

4. Sélectionnez **[!UICONTROL Arrêter]** pour confirmer.

>[!NOTE]
>
>**Arrêt ou achèvement** : un défi arrêté se termine prématurément et ne suit pas le processus d’achèvement normal. Les clients reçoivent des récompenses partielles déjà attribuées, mais pas des récompenses finales pour l’accomplissement du défi. Envisagez de communiquer l’extrémité anticipée aux clients concernés.

### Défis liés à l’archivage {#archive}

Archivez les défis terminés ou arrêtés pour organiser votre inventaire :

1. Sélectionnez le menu **[!UICONTROL Autres actions]** (points de suspension) pour le défi.

2. Cliquez sur **[!UICONTROL Archiver]**.

3. Le défi passe au statut archivé et est masqué de la vue d’inventaire par défaut.

Pour afficher les défis archivés :

1. Dans l&#39;inventaire, appliquez le filtre **[!UICONTROL Statut]**.

2. Sélectionnez **[!UICONTROL Archivé]**.

3. Les défis archivés s’affichent avec les mêmes informations que les défis actifs.

Pour désarchiver un défi :

1. Recherchez le défi archivé à l’aide de filtres.

2. Sélectionnez **[!UICONTROL Désarchiver]** dans le menu d’actions.

3. Le défi revient à son statut précédent (Terminé ou Arrêté).

### Supprimer les défis {#delete}

Supprimez les défis qui ne sont plus nécessaires :

>[!IMPORTANT]
>
>**La suppression est permanente** : les défis supprimés ne peuvent pas être récupérés. Supprimez uniquement les défis dont vous êtes certain de ne plus avoir besoin à l’avenir. Pensez à archiver plutôt qu’à supprimer pour conserver les enregistrements historiques.

**Règles de suppression** :

* Vous pouvez uniquement supprimer des défis au statut **[!UICONTROL Brouillon]**
* Les défis publiés, planifiés, actifs ou terminés ne peuvent pas être supprimés
* Pour supprimer un défi publié, vous devez d’abord l’arrêter, puis l’archiver

Pour supprimer un brouillon de défi :

1. Sélectionnez le menu **[!UICONTROL Autres actions]** (points de suspension) pour le défi.

2. Sélectionnez **[!UICONTROL Supprimer]**.

3. Dans la boîte de dialogue de confirmation, confirmez la suppression.

## Surveillance des performances {#monitor-performance}

Suivez la façon dont les clients relèvent vos défis à l’aide de mesures de performances intégrées.

### Mesures de performances {#performance-metrics}

L’onglet Performances affiche les mesures clés des défis en cours et terminés :

<!--![Performance metrics dashboard showing participation and completion data](assets/performance-metrics-dashboard.png)-->

**[!UICONTROL Mesures de participation]** :

* **Nombre total de clients éligibles** : nombre de clients dans l’audience cible
* **Clients inscrits** : nombre de clients qui ont consulté le défi ou qui y ont participé
* **Taux d’inscription** : pourcentage de clients éligibles ayant été inscrits
* **Participants actifs** : Nombre de clients en cours de progression

**[!UICONTROL Mesures d’achèvement]** :

* **Clients terminés** : nombre de clients qui ont terminé toutes les tâches
* **Taux d’achèvement** : pourcentage de clients inscrits qui ont terminé le défi
* **Durée moyenne d’achèvement** : durée moyenne entre l’inscription et l’achèvement
* **Tâches terminées** : nombre total de tâches individuelles terminées pour tous les clients

**[!UICONTROL Mesures de récompense]** :

* **Total des récompenses distribuées** : somme de toutes les récompenses attribuées
* **Récompenses par type** : répartition par points, remises, articles gratuits, etc.
* **Récompense moyenne par client** : Valeur moyenne de récompense pour les clients participants

**[!UICONTROL Mesures d’engagement]** :

* **Impressions sur la carte de contenu** : nombre de fois où le défi a été affiché
* **Clics sur la carte de contenu** : nombre de fois que les clients ont interagi avec la carte de défi
* **Diffusion de messages** : nombre de messages envoyés pour les étapes de lancement, en cours et terminées
* **Engagement des messages** : taux d’ouverture, taux de clics des messages par étape et canal

### Affichage des rapports de performances {#view-reports}

Pour accéder aux données de performances détaillées :

1. Ouvrez le défi et accédez à l’onglet **[!UICONTROL Performances]**.

2. Sélectionnez la période pour la création de rapports (Aujourd’hui, 7 derniers jours, 30 derniers jours, Période personnalisée).

3. Examiner les mesures par :
   * **Aperçu** : résumé de haut niveau des mesures clés
   * **Chronologie** : Tendances des performances au fil du temps
   * **Répartition** : mesures segmentées par attributs, canaux ou tâches du client

4. Exportez les rapports à l’aide du bouton **[!UICONTROL Exporter]** pour une analyse plus approfondie.

### Surveiller le parcours généré {#monitor-journey}

Le parcours généré automatiquement contient des données d’exécution importantes :

1. Dans les détails du défi, sélectionnez **[!UICONTROL Afficher le parcours]** pour ouvrir le parcours associé.

2. Dans la zone de travail du parcours, passez en revue :
   * **Rapport de Parcours** : Statistiques globales d&#39;exécution
   * **Rapports d’activité** : performance des activités individuelles
   * **Mesures d’entrée et de sortie** : nombre de clients entrés et sortis
   * **Logs d&#39;erreur** : problèmes ou échecs d&#39;exécution

3. Utilisez la surveillance des parcours pour identifier :
   * Goulets d’étranglement lorsque les clients abandonnent
   * Problèmes techniques affectant la diffusion
   * Performances des messages par canal
   * Opportunités d’optimisation du minutage

Pour obtenir des conseils détaillés sur la surveillance des parcours, voir [&#x200B; Surveiller vos parcours &#x200B;](../building-journeys/report-journey.md).

### Optimiser les défis {#optimize}

Utilisez les données de performance pour relever les défis actuels et futurs :

**[!UICONTROL Variantes de test]** : créez des défis en double avec différentes tâches, récompenses ou messages pour comparer les performances.

**[!UICONTROL Ajuster le minutage]** : modifiez la durée du défi ou les échéances de la tâche en fonction des modèles d’achèvement.

**[!UICONTROL Affiner l’audience]** : étendez ou réduisez la sélection de l’audience en fonction de l’engagement et des taux d’achèvement.

**[!UICONTROL Mettre à jour le contenu]** : actualisez les cartes de contenu et les messages pour maintenir l’intérêt et la clarté.

**[!UICONTROL Optimisation des récompenses]** : ajustez les valeurs de récompense pour équilibrer le coût et la participation.

**[!UICONTROL Difficulté de la tâche]** : modifiez les exigences de la tâche si elles sont trop faciles ou trop difficiles en fonction des données d’achèvement.

## Validation et test des tâches {#validation-testing}

Avant de publier votre défi, vérifiez que les tâches sont correctement configurées :

1. **Vérifier la logique de la tâche** :
   * Vérifier que les exigences quantitatives sont réalistes
   * Vérifiez que les critères de filtrage de produit sont corrects.
   * Confirmer que les récompenses sont correctement configurées

2. **Test avec profils de test** :
   * Créer des profils de test représentant différents scénarios client
   * Envoyer des événements de test via votre pipeline d’ingestion de données
   * Vérifier que les tâches se déclenchent correctement
   * Confirmer que les récompenses sont attribuées comme prévu

3. **Vérifier le mappage des données** :
   * Assurez-vous que les données d’événement entrantes sont correctement mappées aux exigences de la tâche
   * Vérifiez que les SKU, catégories et attributs correspondent entre votre système source et Journey Optimizer.
   * Cas de test Edge (données manquantes, valeurs non valides, etc.)

## Bonnes pratiques {#best-practices}

### Création de défi

**Commencez simplement** : pour votre premier défi, commencez par un défi standard simple pour vous familiariser avec le processus.

**Tester minutieusement** : testez toujours votre défi avec les profils de test et les audiences avant de le publier pour l’ensemble de votre base de clients.

**Communication claire** : assurez-vous que les clients comprennent ce qu&#39;ils doivent faire, ce qu&#39;ils gagneront et à quel moment.

**Calendrier réaliste** : définissez des dates de début et de fin appropriées, ce qui laisse suffisamment de temps aux clients pour relever le défi.

**Récompenses attrayantes** : faites en sorte que les récompenses soient précieuses et pertinentes pour votre audience afin de stimuler la participation.

### Configuration de la tâche

**Exigences claires** : définissez des exigences de tâche claires et réalisables. Évitez les conditions trop complexes.

**Difficulté appropriée** : Équilibrez la difficulté de la tâche avec la valeur de récompense. Des tâches plus difficiles devraient offrir de meilleures récompenses.

**Précision du filtrage des produits** : vérifiez à nouveau les SKU, les catégories et les attributs pour garantir une correspondance exacte des produits.

**Récompenses progressives** : utilisez des récompenses jalonnées (après l’achèvement de la tâche) pour maintenir l’engagement du client tout au long du défi.

**Flexibilité** : pour les défis standard, laissez aux clients la possibilité d’effectuer les tâches avec souplesse, en fonction de leurs comportements et préférences.

### Management et monitoring

**Surveillance régulière** : vérifiez les performances des défis au moins une fois par semaine pour les défis en direct afin d’identifier les problèmes dès le début.

**Nom clair** : utilisez des noms descriptifs qui indiquent l’objectif du défi, l’audience ou la période pour une organisation facile.

**Utiliser des balises** : appliquez des balises cohérentes pour classer les défis par campagne, saison, segment d’audience ou autres attributs pertinents.

**Modifications du document** : notez les raisons pour lesquelles vous avez apporté des modifications aux défis pour vous y référer et en tirer des enseignements ultérieurement.

**Archiver de manière cohérente** : archivez régulièrement les défis terminés pour faciliter la gestion de vos stocks.

**Communiquer les modifications** : si vous modifiez un défi en direct, informez les clients concernés des modifications qui ont un impact sur leur participation.

**Analyser après l’achèvement** : examiner les performances une fois chaque défi terminé afin d’identifier les leçons apprises pour les défis futurs.

**Déploiement progressif** : pour les nouveaux types de défis ou les modifications importantes, envisagez de commencer par une audience plus réduite avant un déploiement complet.

**Contrôle de version** : utilisez un contrôle de version clair dans les noms de défi lors de la création d’itérations (par exemple, « Holiday Challenge 2024 - v2 »).

## Résolution des problèmes {#troubleshooting}

**Le défi n’apparaît pas aux clients** :

* Vérifier que le défi a le statut Actif
* Vérifier que les clients se trouvent dans l’audience éligible
* Vérifiez que la configuration de la carte de contenu est correcte.
* Consulter les logs d’exécution du parcours pour les problèmes de diffusion

**Faibles taux de participation** :

* Vérifier la visibilité et l’attrait des cartes de contenu
* Vérifier que la messagerie communique clairement la valeur
* S’assurer que les tâches sont réalisables et que les récompenses sont attrayantes
* Vérifiez que le ciblage des audiences est approprié.

**Les tâches ne se déclenchent pas** :

* Vérifier que les données sont correctement ingérées à partir des connecteurs source
* Vérifiez que les attributs d’événement correspondent aux exigences de la tâche
* Vérifier l’éligibilité de l’audience

**Récompenses non attribuées** :

* Confirmer que la configuration de récompense est correcte
* Vérifier la connexion au système de gestion de la fidélité externe
* Rechercher des erreurs dans les logs de diffusion de récompense

**Le filtrage de produit ne fonctionne pas** :

* Valider les codes SKU et les noms de catégorie
* Vérifiez que le mappage des attributs est correct
* Tester avec des exemples de données d’achat

Le Parcours **n&#39;est pas généré** :

* Vérifiez que toutes les configurations requises sont terminées.
* Rechercher des erreurs dans l’onglet Messagerie
* Vérifier que la carte de contenu est configurée
* Consulter les journaux d’erreurs système

**Les données de performances ne s’affichent pas** :

* Laisser le temps aux données de se propager (jusqu’à 24 heures)
* Vérifier que le suivi des événements est correct
* Vérification du statut d’ingestion des données
* S’assurer que les clients ont commencé à participer

## Beta feedback {#beta-feedback}

Pendant la phase bêta, vos commentaires nous aideront à relever les défis de fidélité. Partagez votre expérience, vos questions et vos suggestions avec votre représentant Adobe ou par le biais des canaux de commentaires bêta fournis lors du lancement.

## Rubriques connexes {#related-topics}

* [Création d’audiences dans Journey Optimizer](../audience/about-audiences.md)
* [Concevoir des cartes de contenu](../content-card/design-content-card.md)
* [Créer des messages in-app](../in-app/create-in-app.md)
* [Créer des e-mails](../email/create-email.md)
* [Créer des notifications push](../push/create-push.md)
* [Création de parcours](../building-journeys/journey-gs.md)
* [Surveiller vos parcours](../building-journeys/report-journey.md)
* [Documentation sur les sources Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/sources/home)
* [Configuration des connecteurs source dans Journey Optimizer](../start/get-started-sources.md)
