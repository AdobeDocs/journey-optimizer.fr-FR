---
solution: Journey Optimizer
product: journey optimizer
title: Itérer sur les données contextuelles
description: Découvrez comment effectuer une itération sur des tableaux provenant de diverses sources de contexte à l’aide de la syntaxe Handlebars
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
hide: true
hidefromtoc: true
keywords: expression, éditeur, barres de contrôle, itération, tableaux, contexte, personnalisation
source-git-commit: a67707e50960e4848197fa1bd39ce95af3ef14ab
workflow-type: tm+mt
source-wordcount: '2484'
ht-degree: 3%

---

# Itérer sur les données contextuelles {#personalization-contexts}

Découvrez comment utiliser la syntaxe d’itération Handlebars pour afficher des listes dynamiques de données provenant de diverses sources dans vos messages, y compris les événements, les réponses d’action personnalisée et d’autres données contextuelles.

## Vue d’ensemble {#overview}

Journey Optimizer permet d’accéder aux données contextuelles provenant de plusieurs sources lors de la [personnalisation des messages](personalize.md). Vous pouvez effectuer une itération sur des tableaux à partir de ces sources à l’aide de la syntaxe Handlebars dans les canaux natifs ([e-mail](../email/get-started-email-design.md), [push](../push/create-push.md), [SMS](../sms/create-sms.md)) pour afficher du contenu dynamique tel que des listes de produits, des recommandations ou d’autres éléments répétés.

**Sources de contexte disponibles :**

* **[Événements](#event-data)** : données issues d&#39;événements de parcours (événements métier, événements unitaires)
* **[Réponses à une action personnalisée](#custom-action-responses)** : données renvoyées par des appels API externes via des actions personnalisées
* **[Recherche de jeu de données](#dataset-lookup)** : données enrichies extraites de jeux de données Adobe Experience Platform
* **[Propriétés techniques](#technical-properties)** : métadonnées de Parcours telles que l’identifiant du parcours et les identifiants supplémentaires
* **[Parcours context](#other-contexts)** : autres données relatives au parcours accessibles lors de l&#39;exécution.

Ce guide vous explique comment effectuer une itération sur des tableaux à partir de chacune de ces sources dans vos messages et comment utiliser des tableaux lors de la configuration des activités de parcours. Commencez par [Syntaxe d’itération Handlebars](#syntax) pour comprendre les principes de base de la personnalisation des messages, ou passez à [Utiliser des tableaux dans des expressions de Parcours ](#arrays-in-journeys) pour savoir comment transmettre des données de tableau à des actions personnalisées et à des recherches de jeux de données.

## Syntaxe de l’itération Handlebars {#syntax}

Handlebars fournit la `{{#each}}` [helper](functions/helpers.md) pour effectuer une itération sur des tableaux. La syntaxe de base est :

```handlebars
{{#each arrayPath as |item|}}
  <!-- Access item properties here -->
  {{item.property}}
{{/each}}
```

**Points clés :**

* Remplacez `arrayPath` par le chemin d’accès aux données de votre tableau
* Remplacez `item` par le nom de variable de votre choix (par exemple `product`, `response`, `element`).
* Accès aux propriétés de chaque élément à l’aide de `{{item.propertyName}}`
* Vous pouvez imbriquer plusieurs blocs de `{{#each}}` pour des tableaux à plusieurs niveaux

## Itérer sur les données d’événement {#event-data}

Les données d’événement sont disponibles lorsque votre parcours est déclenché par un [ événement ](../event/about-events.md). Cela s’avère utile pour afficher les données capturées au moment du démarrage du parcours, telles que le contenu du panier, les éléments de commande ou les envois de formulaire.

>[!TIP]
>
>Vous pouvez combiner des données d’événement avec d’autres sources. Pour obtenir des exemples[ voir ](#combine-sources) Combiner plusieurs sources de contexte .

### Chemin d’accès au contexte pour les événements

```handlebars
context.journey.events.<event_ID>.<fieldPath>
```

* `<event_ID>` : ID unique de votre événement tel que configuré dans le parcours
* `<fieldPath>` : chemin d’accès au champ ou au tableau dans votre schéma d’événement

### Exemple : éléments du panier d’un événement

Si votre [schéma d’événement](../event/experience-event-schema.md) comprend un tableau `productListItems` (format [XDM standard](https://experienceleague.adobe.com/docs/experience-platform/xdm/data-types/product-list-item.html?lang=fr){target="_blank"}), vous pouvez afficher le contenu du panier comme suit :

```handlebars
{{#each context.journey.events.event_ID.productListItems as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    <p>Quantity: {{product.quantity}}</p>
    <p>Price: ${{product.priceTotal}}</p>
  </div>
{{/each}}
```

### Exemple : tableaux imbriqués dans des événements

Pour les structures imbriquées, utilisez des blocs de `{{#each}}` imbriqués. En savoir plus sur l’imbrication dans [ Bonnes pratiques ](#best-practices).

```handlebars
{{#each context.journey.events.event_ID.categories as |category|}}
  <h2>{{category.name}}</h2>
  <ul>
    {{#each category.items as |item|}}
      <li>{{item.title}}</li>
    {{/each}}
  </ul>
{{/each}}
```

## Effectuer une itération sur les réponses d’action personnalisées {#custom-action-responses}

[Action personnalisée](../action/about-custom-action-configuration.md) les réponses contiennent des données renvoyées par des appels API externes. Cela s’avère utile pour afficher des informations en temps réel sur vos systèmes, telles que les points de fidélité, les recommandations de produits, le statut de l’inventaire ou les offres personnalisées.

>[!NOTE]
>
>Les actions personnalisées doivent être configurées avec un payload de réponse pour utiliser cette fonctionnalité. En savoir plus dans [cette section](../action/action-response.md#config-response). Vous pouvez également combiner des réponses d’action personnalisées avec des données d’événement ou des recherches de jeu de données. Pour consulter des exemples, voir [Combiner plusieurs sources de contexte](#combine-sources).

### Chemin d’accès au contexte pour les actions personnalisées

```handlebars
context.journey.actions.<actionName>.<fieldPath>
```

* `<actionName>` : nom de votre [action personnalisée](../action/about-custom-action-configuration.md) tel que configuré dans le parcours
* `<fieldPath>` : chemin d’accès au champ ou au tableau dans la payload de réponse

### Exemple : recommandations de produit à partir d’une API

Si votre action personnalisée renvoie des recommandations de produit :

**Réponse de l’API :**

```json
{
  "recommendations": [
    {
      "productId": "12345",
      "productName": "Summer Jacket",
      "price": 89.99,
      "imageUrl": "https://example.com/jacket.jpg"
    },
    {
      "productId": "67890",
      "productName": "Running Shoes",
      "price": 129.99,
      "imageUrl": "https://example.com/shoes.jpg"
    }
  ]
}
```

**Personnalisation des messages :**

```handlebars
<h2>Recommended for You</h2>
<div class="recommendations">
  {{#each context.journey.actions.GetRecommendations.recommendations as |item|}}
    <div class="product-card">
      <img src="{{item.imageUrl}}" alt="{{item.productName}}" />
      <h3>{{item.productName}}</h3>
      <p class="price">${{item.price}}</p>
    </div>
  {{/each}}
</div>
```

### Exemple : tableaux imbriqués à partir d’actions personnalisées

Si votre action personnalisée renvoie des tableaux imbriqués (par exemple, des catégories avec des produits). Pour des modèles d’imbrication plus complexes, consultez [Bonnes pratiques](#best-practices).

**Réponse de l’API :**

```json
{    
  "id": "84632848268632",    
  "responses": [
    { "productIDs": [1111, 2222, 3333] },
    { "productIDs": [4444, 5555, 6666] },
    { "productIDs": [7777, 8888, 9999] }
  ]
}
```

**Personnalisation des messages :**

```handlebars
<h2>Product Groups</h2>
{{#each context.journey.actions.GetProducts.responses as |response|}}
  <div class="product-group">
    <ul>
      {{#each response.productIDs as |productID|}}
        <li>Product ID: {{productID}}</li>
      {{/each}}
    </ul>
  </div>
{{/each}}
```

### Exemple : avantages du niveau de fidélité

Afficher les avantages dynamiques en fonction du statut de fidélité :

**Réponse de l’API :**

```json
{
  "loyaltyTier": "gold",
  "benefits": [
    { "name": "Free shipping", "icon": "truck" },
    { "name": "20% discount", "icon": "percent" },
    { "name": "Priority support", "icon": "headset" }
  ]
}
```

**Personnalisation des messages :**

```handlebars
<h2>Your {{context.journey.actions.GetLoyaltyInfo.loyaltyTier}} Member Benefits</h2>
<ul class="benefits">
  {{#each context.journey.actions.GetLoyaltyInfo.benefits as |benefit|}}
    <li>
      <span class="icon-{{benefit.icon}}"></span>
      {{benefit.name}}
    </li>
  {{/each}}
</ul>
```

## Itérer sur les résultats de la recherche de jeu de données {#dataset-lookup}

L’activité [Recherche de jeu de données](../building-journeys/dataset-lookup.md) vous permet de récupérer des données de [jeux de données Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=fr){target="_blank"} pendant l’exécution du parcours. Les données enrichies sont stockées sous la forme d’un tableau et peuvent être itérées dans vos messages.

>[!AVAILABILITY]
>
>L’activité de recherche de jeu de données n’est disponible que pour un nombre limité d’organisations. Pour en bénéficier, contactez votre représentant ou représentante Adobe.

En savoir plus sur la configuration de l’activité de recherche de jeu de données dans [cette section](../building-journeys/dataset-lookup.md). La recherche de jeux de données est particulièrement puissante lorsqu’elle est combinée avec des données d’événement. Voir [Exemple : données d’événement enrichies par la recherche de jeux de données](#combine-sources) pour un cas d’utilisation pratique.

### Chemin d’accès au contexte pour les recherches de jeux de données

```handlebars
context.journey.datasetLookup.<activityID>.entities
```

* `<activityID>` : identifiant unique de votre activité de recherche de jeu de données
* `entities` : tableau de données enrichies extraites du jeu de données

### Exemple : détails du produit d’un jeu de données

Si vous utilisez une activité de recherche de jeu de données pour récupérer des informations sur les produits en fonction des SKU :

**Configuration de la recherche de jeu de données:**

* Clés de recherche : `list(@event{purchase_event.products.sku})`
* Champs à renvoyer : `["SKU", "category", "price", "name"]`

**Personnalisation des messages :**

```handlebars
<h2>Product Details</h2>
<table>
  <thead>
    <tr>
      <th>Product Name</th>
      <th>Category</th>
      <th>Price</th>
    </tr>
  </thead>
  <tbody>
    {{#each context.journey.datasetLookup.3709000.entities as |product|}}
      <tr>
        <td>{{product.name}}</td>
        <td>{{product.category}}</td>
        <td>${{product.price}}</td>
      </tr>
    {{/each}}
  </tbody>
</table>
```

### Exemple : itération filtrée avec des données de jeu de données

Afficher uniquement les produits d’une catégorie spécifique. En savoir plus sur le filtrage conditionnel dans [ Bonnes pratiques ](#best-practices).

```handlebars
<h2>Household Products</h2>
{{#each context.journey.datasetLookup.3709000.entities as |product|}}
  {{#if product.category = "household"}}
    <div class="product">
      <h3>{{product.name}}</h3>
      <p>Price: ${{product.price}}</p>
    </div>
  {{/if}}
{{/each}}
```

### Exemple : calcul de totaux à partir de la recherche de jeux de données

```handlebars
{% let householdTotal = 0 %}
{{#each context.journey.datasetLookup.3709000.entities as |product|}}
  {%#if product.category = "household"%}
    {% let householdTotal = householdTotal + product.price %}
  {%/if%}
{{/each}}

<p>Your household products total: ${{householdTotal}}</p>
```

## Utilisation des propriétés techniques de parcours {#technical-properties}

Les propriétés techniques du parcours permettent d’accéder aux métadonnées sur l’exécution du parcours, telles que l’identifiant du parcours et les identifiants supplémentaires. Elles peuvent s’avérer utiles lorsqu’elles sont combinées à des modèles d’itération, en particulier pour filtrer des tableaux en fonction d’instances de parcours spécifiques.

### Propriétés techniques disponibles

```handlebars
context.journey.technicalProperties.journeyUID
context.journey.technicalProperties.supplementalId
```

### Exemple : filtrage d’éléments de tableau à l’aide d’un identifiant supplémentaire

Lors de l’utilisation d’identifiants supplémentaires dans des parcours déclenchés par un événement avec des tableaux, vous pouvez filtrer afin d’afficher uniquement l’élément approprié pour l’instance de parcours active. En savoir plus sur les identifiants supplémentaires dans [ce guide](../building-journeys/supplemental-identifier.md).

**Scénario** : un parcours est déclenché avec plusieurs réservations, mais vous souhaitez afficher les informations uniquement pour la réservation spécifique (identifiée par un ID supplémentaire) qui a déclenché cette instance de parcours.

```handlebars
{{#each context.journey.events.event_ID.bookingList as |booking|}}
  {%#if booking.bookingInfo.bookingNum = context.journey.technicalProperties.supplementalId%}
    <div class="booking-details">
      <h3>Your Booking: {{booking.bookingInfo.bookingNum}}</h3>
      <p>Destination: {{booking.bookingInfo.bookingCountry}}</p>
      <p>Date: {{booking.bookingInfo.bookingDate}}</p>
    </div>
  {%/if%}
{{/each}}
```

### Exemple : inclure l’ID de parcours pour le suivi

```handlebars
<footer>
  <p>Journey Reference: {{context.journey.technicalProperties.journeyUID}}</p>
</footer>
```

## Combinaison de plusieurs sources de contexte {#combine-sources}

Vous pouvez combiner des données provenant de différentes sources dans le même message pour créer des expériences riches et personnalisées. Cette section présente des exemples pratiques d’utilisation conjointe de plusieurs sources de contexte.

**Les sources de contexte peuvent être combinées :**

* [Données d’événement](#event-data) + [Réponses d’action personnalisées](#custom-action-responses)
* [Données d’événement](#event-data) + [Recherche de jeu de données](#dataset-lookup)
* [Sources multiples](#combine-sources) + [Propriétés techniques](#technical-properties)

### Exemple : articles de panier avec stock en temps réel

Combinez les données d’événement (contenu du panier) avec les données d’action personnalisée (statut d’inventaire) :

```handlebars
<h2>Your Cart</h2>
{{#each context.journey.events.cartEvent.productListItems as |product|}}
  <div class="cart-item">
    <h3>{{product.name}}</h3>
    <p>Quantity: {{product.quantity}}</p>
    <p>Price: ${{product.priceTotal}}</p>
  </div>
{{/each}}

<h2>We Also Recommend</h2>
{{#each context.journey.actions.GetRecommendations.items as |recommendation|}}
  <div class="recommendation">
    <h4>{{recommendation.name}}</h4>
    <p>${{recommendation.price}}</p>
    {{#if recommendation.inStock}}
      <span class="badge">In Stock</span>
    {{else}}
      <span class="badge out-of-stock">Out of Stock</span>
    {{/if}}
  </div>
{{/each}}
```

### Exemple : données d’événement enrichies avec la recherche de jeu de données

Combinez les [SKU d’événement](#event-data) avec des informations détaillées sur les produits provenant d’une [recherche de jeu de données](#dataset-lookup) :

```handlebars
<h2>Your Order Details</h2>
{{#each context.journey.events.orderEvent.productListItems as |item|}}
  <div class="order-item">
    <p><strong>SKU:</strong> {{item.SKU}}</p>
    <p><strong>Quantity:</strong> {{item.quantity}}</p>
    
    <!-- Enrich with dataset lookup data -->
    {{#each context.journey.datasetLookup.1234567.entities as |enrichedProduct|}}
      {{#if enrichedProduct.SKU = item.SKU}}
        <p><strong>Product Name:</strong> {{enrichedProduct.name}}</p>
        <p><strong>Category:</strong> {{enrichedProduct.category}}</p>
        <img src="{{enrichedProduct.imageUrl}}" alt="{{enrichedProduct.name}}" />
      {{/if}}
    {{/each}}
  </div>
{{/each}}
```

### Exemple : combinaison de plusieurs sources avec des propriétés techniques

```handlebars
<div class="personalized-content">
  <!-- Profile data -->
  <h1>Hello {{profile.person.name.firstName}},</h1>
  
  <!-- Event data iteration -->
  <h2>Your Recent Purchases</h2>
  {{#each context.journey.events.purchaseEvent.items as |purchase|}}
    <div class="purchase">
      <p>{{purchase.productName}} - ${{purchase.price}}</p>
    </div>
  {{/each}}
  
  <!-- Custom action response iteration -->
  <h2>Recommended for You</h2>
  {{#each context.journey.actions.GetPersonalizedRecs.recommendations as |rec|}}
    <div class="recommendation">
      <h3>{{rec.title}}</h3>
      <p>{{rec.description}}</p>
    </div>
  {{/each}}
  
  <!-- Technical properties -->
  <footer>
    <p class="fine-print">Journey ID: {{context.journey.technicalProperties.journeyUID}}</p>
  </footer>
</div>
```

## Autres types de contexte {#other-contexts}

Bien que ce guide se concentre sur l’itération sur les tableaux, d’autres types de contexte sont disponibles pour la personnalisation qui ne nécessitent généralement pas d’itération. Ils sont accessibles directement plutôt que par bouclage :

* **[Attributs de profil](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=fr){target="_blank"}** (`profile.*`) : champs de profil individuels de Adobe Experience Platform
* **[Audiences](../audience/about-audiences.md)** (`inAudience()`) : contrôles de l’appartenance à une audience
* **[Décisions d’offre](../offers/get-started/starting-offer-decisioning.md)** : offres de gestion des décisions
* **[Attributs de la cible](../orchestrated/activities/channels.md#add-personalization)** (campagnes orchestrées uniquement) : attributs calculés dans la zone de travail de la campagne
* **Jeton** (`context.token`) : jetons de session ou d’authentification

Pour obtenir une syntaxe de personnalisation complète et des exemples d’utilisation de ces sources, reportez-vous à :

* [Ajouter une personnalisation](personalization-build-expressions.md)
* [Syntaxe de personnalisation](personalization-syntax.md)

## Utilisation de tableaux dans les expressions de Parcours {#arrays-in-journeys}

Bien que les sections précédentes se concentrent sur l’itération sur des tableaux dans la personnalisation des messages à l’aide de Handlebars, vous travaillez également avec des tableaux lors de la configuration des activités de parcours. Cette section explique comment utiliser les données de tableau des événements dans les expressions de Parcours, en particulier lors de la transmission de données à des actions personnalisées ou de l’utilisation de tableaux avec des recherches de jeux de données.

>[!IMPORTANT]
>
>Les expressions de parcours utilisent une syntaxe différente de la personnalisation Handlebars. Dans la configuration de parcours (paramètres ou conditions d&#39;action personnalisée, par exemple), vous utilisez l&#39;éditeur d&#39;expression de Parcours [](../building-journeys/expression/expressionadvanced.md) avec des fonctions telles que `first`, `all` et `serializeList`. Dans le contenu des messages, vous utilisez la syntaxe Handlebars avec des boucles `{{#each}}`.

### Transmettre des valeurs de tableau aux paramètres d’action personnalisés {#arrays-to-custom-actions}

Lors de la configuration d’[actions personnalisées](../action/about-custom-action-configuration.md), vous devez souvent extraire des valeurs des tableaux d’événements et les transmettre en tant que paramètres. Cette section couvre les modèles courants.

En savoir plus sur la transmission de collections dans [Transmettre des collections dans des paramètres d’action personnalisés](../building-journeys/collections.md#passing-collection).

#### Extraire une seule valeur d’un tableau

**Cas d’utilisation** : obtenez un champ spécifique d’un tableau d’événements à transmettre en tant que paramètre de requête dans une requête GET.

**Exemple de scénario** : extrayez le premier SKU avec un prix supérieur à 0 d’une liste de produits.

**Exemple de schéma d’événement** :

```json
{
  "commerce": {
    "productListItems": [
      { "SKU": "SKU-1", "priceTotal": 10.0 },
      { "SKU": "SKU-2", "priceTotal": 0.0 },
      { "SKU": "SKU-3", "priceTotal": 20.0 }
    ]
  }
}
```

**Configuration d’une action personnalisée** :

1. Dans votre action personnalisée, configurez un paramètre de requête (par exemple, `sku`) avec le type `string`
2. Marquer comme `Variable` pour autoriser les valeurs dynamiques

**Paramètre d&#39;expression de Parcours en action**:

```javascript
@event{YourEventName.commerce.productListItems.first(currentEventField.priceTotal > 0).SKU}
```

**Explication** :

* `@event{YourEventName}` : fait référence à votre événement de parcours.
* `.first(currentEventField.condition)` : renvoie le premier élément du tableau correspondant à la condition
* `currentEventField` : représente chaque élément du tableau d’événements pendant que vous le parcourez
* `.SKU` : extrait le champ SKU de l’élément correspondant
* Résultat : `"SKU-1"` (chaîne appropriée pour le paramètre d’action)

En savoir plus sur la fonction `first` dans [Fonctions de gestion des collections](../building-journeys/expression/collection-management-functions.md).

#### Création d’une liste de valeurs à partir d’un tableau

**Cas d’utilisation** : créez une liste d’identifiants séparés par des virgules à transmettre en tant que paramètre de requête (par exemple, `/products?ids=sku1,sku2,sku3`).

**Configuration d’une action personnalisée** :

1. Configurez un paramètre de requête (par exemple, `ids`) avec le type `string`
2. Marquer comme `Variable`

**Expression de Parcours** :

```javascript
serializeList(
  @event{YourEventName.commerce.productListItems.all(currentEventField.priceTotal > 0).SKU},
  ",",
  true
)
```

**Explication** :

* `.all(currentEventField.condition)` : renvoie tous les éléments du tableau correspondant à la condition (renvoie une liste)
* `currentEventField` : représente chaque élément du tableau d’événements pendant que vous le parcourez
* `.SKU` : les projets de la liste incluent uniquement les valeurs de SKU
* `serializeList(list, delimiter, addQuotes)` : joint la liste en chaîne
   * `","` : utiliser une virgule comme délimiteur
   * `true` : ajoutez des guillemets autour de chaque élément de chaîne.
* Résultat : `"SKU-1,SKU-3"` (adapté à un paramètre de requête)

En savoir plus sur :

* [`all`](../building-journeys/expression/collection-management-functions.md)
* [`serializeList`](../building-journeys/functions/list-functions.md#serializeList)

La gestion des collections pour les actions personnalisées est traitée dans la section [Transmettre des collections dans des paramètres d’action personnalisée](../building-journeys/collections.md#passing-collection).

#### Transmettre un tableau d’objets à une action personnalisée

**Cas d’utilisation** : envoyez un tableau complet d’objets dans un corps de requête (pour POST ou GET avec le corps).

**Exemple de corps de requête** :

```json
{
  "ctxt": {
    "products": [
      {
        "id": "productA",
        "name": "Product A",
        "price": 20.1,
        "color": "blue"
      }
    ]
  }
}
```

**Configuration d’une action personnalisée** :

1. Dans le corps de la requête, définissez `products` comme type `listObject`
2. Marquer comme `Variable`
3. Définissez les champs d’objet : `id`, `name`, `price`, `color` (chacun devient mappable)

Configuration de la zone de travail de Parcours **** :

1. En mode avancé, définissez l’expression de collection :

   ```javascript
   @event{YourEventName.commerce.productListItems.all(currentEventField.priceTotal > 0)}
   ```

1. Dans l’interface utilisateur du mappage des collections :
   * Mapper `id` → `productListItems.SKU`
   * Mapper `name` → `productListItems.name`
   * Mapper `price` → `productListItems.priceTotal`
   * Mapper `color` → `productListItems.color`

Journey Optimizer construit le tableau d’objets correspondant à la structure de votre payload d’action.

>[!NOTE]
>
>Lorsque vous utilisez des tableaux d’événements, utilisez `currentEventField` pour référencer chaque élément. Pour les collections de sources de données (Adobe Experience Platform), utilisez `currentDataPackField`. Pour les collections de réponses d’actions personnalisées, utilisez `currentActionField`.

En savoir plus sur la section [ Transmettre des collections dans des paramètres d’action personnalisés ](../building-journeys/collections.md#passing-collection).

### Utilisation de tableaux avec les recherches de jeux de données {#arrays-with-dataset-lookup}

Lors de l’utilisation de l’activité [Recherche de jeu de données](../building-journeys/dataset-lookup.md), vous pouvez transmettre un tableau de valeurs en tant que clés de recherche pour récupérer des données enrichies.

**Exemple** : recherchez les détails du produit pour tous les SKU d’un tableau d’événements.

**Configuration de la recherche de jeu de données** :

Dans le champ clés de recherche , utilisez `list()` pour convertir un chemin d’accès au tableau en liste :

```javascript
list(@event{purchaseEvent.productListItems.SKU})
```

Cela crée une liste de toutes les valeurs de SKU à rechercher dans le jeu de données. Les résultats sont disponibles sous la forme d’un tableau à l’`context.journey.datasetLookup.<activityID>.entities` sur lequel vous pouvez effectuer une itération dans votre message (voir [Itérer sur les résultats de la recherche de jeu de données](#dataset-lookup)).

### Restrictions et modèles {#array-limitations}

Gardez à l’esprit ces limites lorsque vous utilisez des tableaux dans des parcours :

#### Pas de boucle dynamique sur les tableaux dans le flux de parcours

Les parcours ne peuvent pas créer de boucles dynamiques dans lesquelles un nœud d’action est exécuté plusieurs fois pour chaque élément d’un tableau. Cela est intentionnel afin d’éviter des problèmes de performances d’emballement.

**Ce que vous ne pouvez pas faire** :

* Exécutez dynamiquement une action personnalisée une fois par élément de tableau
* Création de plusieurs branches de parcours en fonction de la longueur du tableau

**Modèles recommandés à la place** :

1. **Envoyer tous les éléments en une seule fois** : transmettez l’ensemble du tableau ou d’une liste sérialisée à une seule action personnalisée qui traite tous les éléments. Voir [Création d’une liste de valeurs à partir d’un tableau](#arrays-to-custom-actions).

2. **Utiliser l’agrégation externe** : demandez à votre API externe d’accepter plusieurs identifiants et de renvoyer les résultats combinés en un seul appel.

3. **Pré-calcul dans AEP** : utilisez [attributs calculés](../audience/computed-attributes.md) pour précalculer les valeurs des tableaux au niveau du profil.

4. **Extraction de valeur unique** : si vous n’avez besoin que d’une seule valeur, extrayez-la à l’aide de `first` ou `head`. Voir [Extraire une seule valeur d’un tableau](#arrays-to-custom-actions).

En savoir plus sur la [Mécanismes de sécurisation et limitations](../start/guardrails.md).

#### Considérations relatives à la taille des tableaux

Les baies volumineuses peuvent avoir un impact sur les performances du parcours :

* **Tableaux d’événements** : conservez les payloads d’événements en dessous de 50 Ko au total
* **Réponses d’action personnalisées** : les payloads de la réponse doivent être sous 100KB
* **Résultats de la recherche de jeux de données** : limitez le nombre de clés de recherche et d’entités renvoyées

### Exemple complet : tableau d’événements pour une action personnalisée {#complete-example}

Voici un workflow complet montrant comment utiliser un tableau d’événements avec une action personnalisée.

**Scénario** : lorsqu’un utilisateur abandonne son panier, envoyez les données du panier à une API de recommandation externe pour obtenir des suggestions personnalisées, puis affichez-les dans un e-mail.

**Étape 1 : configurer l’action personnalisée**

Créez une action personnalisée « GetCartRecommendations » :

* **Méthode** : POST
* **URL** : `https://api.example.com/recommendations`
* **Corps de la requête** :

```json
{
  "cartItems": [
    {
      "sku": "string",
      "price": 0,
      "quantity": 0
    }
  ]
}
```

* Marquer `cartItems` comme type `listObject` et `Variable`
* Définir les champs : `sku` (chaîne), `price` (nombre), `quantity` (entier)

En savoir plus dans [Configuration d’une action personnalisée](../action/about-custom-action-configuration.md).

**Étape 2 : configurer la payload de réponse**

Dans l’action personnalisée, configurez la réponse :

```json
{
  "recommendations": [
    {
      "productId": "string",
      "productName": "string",
      "price": 0,
      "imageUrl": "string"
    }
  ]
}
```

En savoir plus dans [Utilisation des réponses d’appel API](../action/action-response.md).

**Étape 3 : câbler l&#39;action dans le parcours**

1. Après votre événement d’abandon de panier, ajoutez l’action personnalisée
1. En mode avancé pour la collecte de `cartItems` :

   ```javascript
   @event{cartAbandonment.commerce.productListItems.all(currentEventField.quantity > 0)}
   ```

1. Mappez les champs de collection :
   * `sku` → `productListItems.SKU`
   * `price` → `productListItems.priceTotal`
   * `quantity` → `productListItems.quantity`

**Étape 4 : utiliser la réponse dans votre e-mail**

Dans le contenu de votre e-mail, effectuez une itération sur les recommandations :

```handlebars
<h2>We noticed you left these items in your cart</h2>
{{#each context.journey.events.cartAbandonment.productListItems as |item|}}
  <div class="cart-item">
    <p>{{item.name}} - Quantity: {{item.quantity}}</p>
  </div>
{{/each}}

<h2>You might also like</h2>
{{#each context.journey.actions.GetCartRecommendations.recommendations as |rec|}}
  <div class="recommendation">
    <img src="{{rec.imageUrl}}" alt="{{rec.productName}}" />
    <h3>{{rec.productName}}</h3>
    <p>${{rec.price}}</p>
  </div>
{{/each}}
```

**Étape 5 : tester votre configuration**

Avant d’exécuter un parcours en direct, testez l’action personnalisée à l’aide de la fonctionnalité « Envoyer la demande de test » de la configuration de l’action pour vérifier la demande et les valeurs créées.

1. Utiliser le mode test de parcours [](../building-journeys/testing-the-journey.md)
2. Déclencheur avec des exemples de données d’événement, y compris un tableau de `productListItems`
3. Vérifiez que l’action personnalisée reçoit la structure de baie appropriée.
4. Vérifiez les journaux de test [action](../action/action-response.md#test-mode-logs)
5. Prévisualisez l’e-mail pour confirmer que les deux tableaux s’affichent correctement

En savoir plus dans [Résolution des problèmes liés aux actions personnalisées](../action/troubleshoot-custom-action.md).

## Bonnes pratiques {#best-practices}

Suivez ces bonnes pratiques lors de l’itération sur les données contextuelles pour créer une personnalisation performante et maintenable.

### Utiliser des noms de variables descriptifs

Choisissez des noms de variables qui indiquent clairement ce sur quoi vous effectuez une itération. Cela rend votre code plus lisible et plus facile à gérer. En savoir plus sur la [syntaxe de personnalisation](personalization-syntax.md) :

```handlebars
<!-- Good -->
{{#each products as |product|}}
{{#each users as |user|}}
{{#each recommendations as |recommendation|}}

<!-- Less clear -->
{{#each items as |item|}}
{{#each array as |element|}}
```

### Gérer les tableaux vides

Utilisez la clause `{{else}}` pour fournir un contenu de secours lorsqu’un tableau est vide. En savoir plus sur les [fonctions helper](functions/helpers.md) :

```handlebars
{{#each context.journey.actions.GetRecommendations.items as |item|}}
  <div>{{item.name}}</div>
{{else}}
  <p>No recommendations available at this time.</p>
{{/each}}
```

### Combinaison avec des assistants conditionnels

Utilisez des `{{#if}}` dans des boucles pour le contenu conditionnel. En savoir plus sur les [règles conditionnelles](create-conditions.md) et consultez des exemples dans les sections [Réponses d’action personnalisées](#custom-action-responses) et [Recherche de jeu de données](#dataset-lookup).

```handlebars
{{#each context.journey.actions.GetProducts.items as |product|}}
  <div class="product">
    <h3>{{product.name}}</h3>
    {{#if product.onSale}}
      <span class="badge">On Sale!</span>
    {{/if}}
    {{#if product.newArrival}}
      <span class="badge">New</span>
    {{/if}}
  </div>
{{/each}}
```

### Limiter l’itération pour les performances

Pour les tableaux volumineux, pensez à limiter le nombre d’itérations :

```handlebars
<!-- Display only first 5 items -->
{{#each context.journey.actions.GetProducts.items as |product|}}
  {{#if @index < 5}}
    <div>{{product.name}}</div>
  {{/if}}
{{/each}}
```

### Accès aux métadonnées des tableaux

Handlebars fournit des variables spéciales dans les boucles qui aident à obtenir des modèles d’itération avancés :

* `@index` : index d’itération actuel (basé sur 0)
* `@first` : Vrai pour la première itération
* `@last` : True pour la dernière itération

```handlebars
{{#each products as |product|}}
  <div class="product {{#if @first}}featured{{/if}}">
    {{@index}}. {{product.name}}
  </div>
{{/each}}
```

>[!NOTE]
>
>Ces variables Handlebars (`@index`, `@first`, `@last`) ne sont disponibles que dans les boucles `{{#each}}` dans la personnalisation des messages. Pour utiliser des tableaux dans des expressions de Parcours (comme obtenir le premier élément d’un tableau avant de transmettre à une action personnalisée), utilisez des fonctions de tableau telles que [`head`](../personalization/functions/arrays-list.md#head), [`first`](../building-journeys/expression/collection-management-functions.md) ou [`all`](../building-journeys/expression/collection-management-functions.md). Voir [ Utilisation de tableaux dans les expressions de Parcours ](#arrays-in-journeys) pour plus d’informations.

## Résolution des problèmes {#troubleshooting}

Vous rencontrez des problèmes avec l’itération ? Cette section couvre les problèmes courants et les solutions.

### Tableau non affiché

**Problème** : votre itération de tableau n’affiche aucun contenu.

**Causes possibles et solutions** :

1. **Chemin d’accès incorrect** : vérifiez le chemin d’accès exact de votre tableau en fonction de la source de contexte :
   * Pour les [événements](#event-data) : `context.journey.events.<event_ID>.<fieldPath>`
   * Pour les [actions personnalisées](#custom-action-responses) : `context.journey.actions.<actionName>.<fieldPath>`
   * Pour les [recherches de jeux de données](#dataset-lookup) : `context.journey.datasetLookup.<activityID>.entities`

2. **Le tableau est vide** : ajoutez une clause `{{else}}` pour vérifier si le tableau ne contient aucune donnée. Voir [Bonnes pratiques](#best-practices) pour obtenir des exemples.

3. **Données pas encore disponibles** : assurez-vous que l’action personnalisée, l’événement ou l’activité de recherche de jeu de données a été exécuté avant l’activité de message dans votre flux de parcours.

### Erreurs de syntaxe

**Problème** : la validation de l’expression échoue ou le message ne s’affiche pas.

**Erreurs courantes** :

* Balises de fermeture manquantes : chaque `{{#each}}` doit avoir une `{{/each}}`. Consultez [Syntaxe d’itération Handlebars](#syntax) pour obtenir une structure appropriée.
* Nom de variable incorrect : assurez-vous que le nom de variable est utilisé de manière cohérente dans tout le bloc. Voir [Bonnes pratiques](#best-practices) pour connaître les conventions de nommage.
* Séparateurs de chemin incorrects : utilisez des points (`.`) et non des barres obliques ou d’autres caractères.

### Test de vos itérations

Utilisez le mode de test de parcours [](../building-journeys/testing-the-journey.md) pour vérifier vos itérations. Ceci est particulièrement important lors de l’utilisation de [actions personnalisées](#custom-action-responses) ou [recherches de jeux de données](#dataset-lookup) :

1. Démarrez votre parcours en [mode test](../building-journeys/testing-the-journey.md)
2. Déclencher l’événement ou l’action personnalisée avec des exemples de données
3. Vérifiez l’[aperçu du message](../content-management/preview.md) pour vous assurer que l’itération s’affiche correctement
4. Consultez les journaux du mode test pour connaître les erreurs éventuelles (voir [Journaux du mode test d’action personnalisée](../action/action-response.md#test-mode-logs)).

## Rubriques connexes {#related-topics}

**Principes de base de Personalization :**

* [Commencer avec la personnalisation](personalize.md)
* [Ajouter une personnalisation](personalization-build-expressions.md)
* [Syntaxe de personnalisation](personalization-syntax.md)
* [Fonctions d’assistance](functions/helpers.md)
* [Créer des règles conditionnelles](create-conditions.md)

Configuration du Parcours ****

* [À propos des événements](../event/about-events.md)
* [Configurer des actions personnalisées](../action/about-custom-action-configuration.md)
* [Transmettre des collections dans des paramètres d’actions personnalisées](../building-journeys/collections.md#passing-collection)
* [Utiliser des réponses d’appel API dans des actions personnalisées](../action/action-response.md)
* [Résoudre les problèmes liés aux actions personnalisées](../action/troubleshoot-custom-action.md)
* [Utiliser des données Adobe Experience Platform dans les parcours](../building-journeys/dataset-lookup.md)
* [Utiliser des identifiants supplémentaires dans les parcours](../building-journeys/supplemental-identifier.md)
* [Mécanismes de sécurisation et limitations](../start/guardrails.md)
* [Tester votre parcours](../building-journeys/testing-the-journey.md)

**Fonctions d&#39;expression de Parcours :**

* [Éditeur d’expression avancé](../building-journeys/expression/expressionadvanced.md)
* [Fonctions de gestion des collections](../building-journeys/expression/collection-management-functions.md) (en premier, en dernier)
* [Fonctions de liste](../building-journeys/functions/list-functions.md) (serializeList, filter, sort)
* [Fonctions de tableau](../personalization/functions/arrays-list.md) (head, tail)

**Cas d’utilisation de Personalization :**

* [E-mail d’abandon de panier](personalization-use-case-helper-functions.md)
* [Notification de statut de la commande](personalization-use-case.md)

**Conception de message :**

* [Commencer la conception d’e-mails](../email/get-started-email-design.md)
* [Créer des notifications push](../push/create-push.md)
* [Création de SMS](../sms/create-sms.md)
* [Prévisualiser et tester le contenu](../content-management/preview-test.md)

