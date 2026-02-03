---
solution: Journey Optimizer
product: journey optimizer
title: Créer des défis de fidélité
description: Découvrez comment créer et configurer des défis de fidélité dans Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private Beta" type="Informative"
source-git-commit: 419c7b3913ca4da50c69ed36ffc1a8c8520607b4
workflow-type: tm+mt
source-wordcount: '1103'
ht-degree: 1%

---


# Créer des défis {#create-challenges}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_create_challenge"
>title="Créer un défi de fidélité"
>abstract="Créez un défi de fidélité pour définir l’offre d’engagement, configurer les cartes de contenu pour la diffusion, ajouter des tâches, configurer des récompenses et éventuellement configurer la messagerie sur plusieurs canaux."

Créez un défi de fidélité pour définir l’offre d’engagement, configurer les cartes de contenu, ajouter des tâches, configurer des récompenses et configurer la messagerie sur plusieurs canaux.

>[!BEGINSHADEBOX]

**Documentation sur les défis de fidélité :**

* [Prise en main des défis de fidélité](gs-loyalty-challenges.md) - Aperçu rapide et étapes suivantes
* [Présentation des défis de fidélité](get-started.md) - Fonctionnalités, workflow, conditions préalables
* **Créer des défis** ◀︎ **Vous êtes ici** - Créez et configurez des défis
* [Gérer les défis](manage-challenges.md) - Modifier, surveiller, optimiser

>[!ENDSHADEBOX]

## Avant de commencer {#before-you-start}

Avant de créer un défi, vérifiez que vous disposez des éléments suivants :

* Ingestion de données configurée et validée via les connecteurs source
* Création des audiences requises dans Experience Platform
* Préparation des ressources de contenu (images, texte, etc.) pour votre défi
* Défini les tâches et les récompenses que vous souhaitez offrir

## Créer un défi {#create-a-challenge}

Pour obtenir des instructions détaillées sur la création de défis, notamment :
* Configuration des propriétés du défi
* Types de défis (Standard, Séquentiel, Séquentiel)
* Sélection d’audience
* Configuration de la date

Voir le guide complet dans la [documentation principale](loyalty-challenges.md#create-challenges).

## Ajouter des tâches {#add-tasks}

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

## Configuration des cartes de contenu {#configure-content-cards}

Pour obtenir des instructions détaillées sur la configuration des cartes de contenu, notamment :
* Configuration de la carte de contenu
* Conception et personnalisation
* Prévisualisation et test

Voir le guide complet dans la [documentation principale](loyalty-challenges.md#configure-content-cards).

## Configurer la messagerie {#configure-messaging}

Pour obtenir des instructions détaillées sur la configuration de la messagerie multicanal, notamment :
* Canaux de message (in-app, e-mail, push)
* Étapes du message (lancement, en cours, terminé)
* Synchronisation des messages et déclencheurs

Voir le guide complet dans la [documentation principale](loyalty-challenges.md#configure-messaging).

## Révision et publication {#review-and-publish}

Avant de publier votre défi :

1. **Examiner tous les composants** : propriétés du défi, tâches, récompenses, contenu, messagerie
2. **Tester l’expérience** : utilisez des profils de test pour valider le contenu et les déclencheurs de tâche
3. **Publication** : activez ce défi pour votre audience cible

Le parcours généré automatiquement s’active à la date de début que vous avez spécifiée.

## Étapes suivantes {#next-steps}

* [Gérer les défis](manage-challenges.md) - Découvrez comment modifier, surveiller et optimiser les défis
* [Comprendre les défis de la fidélité](get-started.md) - Examinez les fonctionnalités et capacités
