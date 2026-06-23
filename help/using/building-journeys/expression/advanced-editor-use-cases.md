---
solution: Journey Optimizer
product: journey optimizer
title: Utilisation de l’éditeur d’expression avancé
description: Découvrir comment créer des expressions avancées
feature: Journeys
role: Developer
level: Experienced
hide: true
keywords: expression, condition, cas d’utilisation, événements
exl-id: 753ef9f4-b39d-4de3-98ca-e69a1766a78b
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/UUeCcATC7MFHsLuI8TPoVHqwVe9GOXUq3U3RoAG-a1o
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1103
ht-degree: 51%

---

# Exemples d’expressions avancées{#advanced-expression-examples}

L’éditeur d’expression avancé sert à créer des conditions pour filtrer les utilisateurs et utilisatrices dans vos parcours. Ces conditions vous permettent de cibler des utilisateurs et des utilisatrices en fonction de l’heure, de la date, de l’emplacement ou de la durée pour pouvoir les cibler à nouveau dans le parcours.

>[!CAUTION]
>
>L’utilisation d’événements d’expérience dans des expressions/conditions de parcours n’est pas prise en charge. Si votre cas d’utilisation nécessite l’utilisation d’événements d’expérience, envisagez d’utiliser d’autres méthodes. [En savoir plus](../exp-event-lookup.md)


## Création de conditions pour les événements d’expérience


>[!CAUTION]
>
>L’utilisation d’événements d’expérience dans des expressions/conditions de parcours n’est pas prise en charge. Si votre cas d’utilisation nécessite l’utilisation d’événements d’expérience, envisagez d’utiliser d’autres méthodes. [En savoir plus](../exp-event-lookup.md)
>



L’éditeur d’expression avancé est obligatoire pour effectuer des requêtes sur des séries temporelles, comme une liste d’achats ou des clics antérieurs sur des messages. L’éditeur simple ne permet pas d’effectuer ces requêtes.

>[!NOTE]
>
>Les événements commencent par le caractère @, les sources de données par #.

Les événements d’expérience sont récupérés depuis Adobe Experience Platform sous la forme d’une collection dans l’ordre chronologique inverse. Par conséquent :

* La fonction first renvoie l’événement le plus récent.
* La fonction last renvoie l’événement le plus ancien.

Par exemple, supposons que vous vouliez cibler des clients ayant abandonné leur panier au cours des 7 derniers jours et envoyer un message lorsqu’un client se trouve à proximité d’un magasin, avec une offre sur les articles qu’il souhaitait et qui se trouvent en magasin.

**Vous devez créer les conditions suivantes :**

Tout d’abord, il s’agit de cibler les clients qui ont accédé à la boutique en ligne, mais n’ont pas finalisé la commande au cours des 7 derniers jours.

**Cette expression recherche une valeur spécifiée dans une valeur de chaîne :**

`In ("addToCart", #{field reference from experience event})`

**Cette expression recherche tous les événements relatifs à cette personne spécifiés au cours des 7 derniers jours :**

Ensuite, elle sélectionne tous les événements d’ajout au panier qui n’ont pas été transformés en completePurchase.

>[!NOTE]
>
>Pour insérer rapidement un champ dans l’expression, double-cliquez dessus dans le panneau de gauche de l’éditeur.

L’horodatage spécifié tient lieu de valeur de date et d’heure, la deuxième valeur correspond au nombre de jours.

```json
        in( "addToCart", #{ExperiencePlatformDataSource
                        .ExperienceEventFieldGroup
                        .experienceevent
                        .all(
                        inLastDays(currentDataPackField.timestamp, 7 ))
                        .productData
                        .productInteraction})
        and
        not(in( "completePurchase", #{ExperiencePlatformDataSource
                        .ExperienceEventFieldGroup
                        .experienceevent
                        .all(
                        inLastDays(currentDataPackField.timestamp, 7 ))
                        .productData
                        .productInteraction}))
```

Cette expression renvoie une valeur booléenne.

**Maintenant, créons une expression qui vérifie que le produit est en stock**

* Dans Inventory, cette expression recherche le champ de quantité d’un produit et indique qu’il doit être supérieur à 0.

`#{Inventory.fieldgroup3.quantity} > 0`

* Les valeurs nécessaires sont spécifiées à droite. Ici, nous devons récupérer l’emplacement du magasin, qui est mappé à partir de l’emplacement de l’événement « ArriveLumaStudio » :

`#{ArriveLumaStudio._acpevangelists1.location.location}`

* Spécifiez la référence du produit (SKU) à l’aide de la fonction `first` pour récupérer la dernière interaction &quot;addToCart&quot; :

  ```json
      #{ExperiencePlatformDataSource
                      .ExperienceEventFieldGroup
                      .experienceevent
                      .first(
                      currentDataPackField
                      .productData
                      .productInteraction == "addToCart"
                      )
                      .SKU}
  ```

De là, vous pouvez ajouter un autre chemin dans votre parcours pour les cas où le produit ne se trouve pas en magasin et envoyer une notification avec une offre d’engagement. Configurez les messages en conséquence et utilisez les données de personnalisation pour améliorer le ciblage de ces messages.

## Filtrage de date et heure dans les expressions

Lors du référencement de plusieurs événements d’activité de panier, spécifiez une fenêtre d’horodatage de début et de fin pour éviter de récupérer des données historiques. Par exemple :

```json
toDateTimeOnly(currentDataPackField.timestamp) >= toDateTimeOnly(@event{poc_UDXCartAddSavedCheckOutEv.timestamp})
AND
toDateTimeOnly(currentDataPackField.timestamp) < toDateTimeOnly(nowWithDelta(4, "hours"))
```

## Exemples de manipulations de chaînes avec l’éditeur d’expression avancé

**Dans des conditions**

Cette condition récupère uniquement les événements de limite géographique déclenchés dans Arlington :

```json
        @event{GeofenceEntry
                    .placeContext
                    .POIinteraction
                    .POIDetail
                    .name} == "Arlington"
```

Explication : il s’agit d’une comparaison de chaînes stricte (sensible à la casse), équivalente à une requête en mode simple qui utilise l’opérateur `equal to` avec `Is sensitive` coché.

La même requête avec `Is sensitive` non coché génère l’expression suivante en mode avancé :

```json
        equalIgnoreCase(@event{GeofenceEntry
                        .placeContext
                        .POIinteraction
                        .POIDetail
                        .name}, "Arlington")
```

**Dans des actions**

L’expression suivante permet de définir l’identifiant CRM dans un champ de personnalisation d’action :

```json
substr(
   @event{MobileAppLaunch
   ._myorganization
   .identification
   .crmid},
   1, 
   lastIndexOf(
     @event{MobileAppLaunch
     ._myorganization
     .identification
     .crmid},
     '}'
   )
)
```

Explication : cet exemple utilise les fonctions `substr` et `lastIndexOf` pour supprimer les accolades qui encadrent l’identifiant CRM transmis avec un événement de lancement d’application mobile.


Pour en savoir plus sur l’utilisation de l’éditeur d’expression avancé, regardez [cette vidéo](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/introduction-to-building-a-journey.html?lang=fr).

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page fournit des exemples pratiques d’utilisation de l’éditeur d’expression avancé pour créer des conditions de parcours qui filtrent les utilisateurs par activité de panier, statut d’inventaire, événements de limite géographique, manipulations de chaînes et fenêtres d’horodatage.

**Intentions:**

* Créez une condition d’abandon de panier à l’aide de `in()` et `inLastDays()` pour cibler les utilisateurs et utilisatrices qui ont ajouté des articles mais n’ont pas effectué d’achat dans les 7 jours
* Filtrer les collections d’événements d’expérience par fenêtre d’horodatage pour éviter de capturer des données historiques
* Appliquez des comparaisons de chaînes sensibles à la casse et non sensibles à la casse aux champs d’événement de limite géographique
* Extraire et manipuler des identifiants CRM à partir d’événements de lancement d’application mobile à l’aide de `substr` et `lastIndexOf`
* Vérifier la disponibilité du stock de produits en comparant un champ de quantité à un seuil
* Combinaison de plusieurs expressions booléennes à l’aide de la logique `and`/`not` dans des conditions de parcours

**Glossaire:**

* **Éditeur d’expression avancé** : interface Journey Optimizer permettant d’écrire des expressions complexes au niveau du code à l’aide de fonctions, d’opérateurs et de références de champ *(spécifiques au produit)*
* **currentDataPackField** : variable de boucle utilisée lors de l’itération sur des collections de sources de données dans des fonctions `all()`, `first()` ou `last()` *(spécifiques à un produit)*
* **inLastDays(timestamp, N)** : fonction de date qui renvoie la valeur true si l’horodatage donné correspond aux N derniers jours *(spécifique au produit)*
* **Événements d’expérience** : enregistrements de données comportementales de série temporelle stockés dans Adobe Experience Platform, récupérés dans l’ordre chronologique inverse *(spécifique au produit)*

**Mécanismes de sécurisation :**

* L’utilisation d’événements d’expérience directement dans des expressions/conditions de parcours n’est pas prise en charge ; d’autres méthodes telles que des attributs calculés ou des segments d’audience doivent être utilisées à la place
* L’éditeur d’expression avancé doit être utilisé (et non l’éditeur simple) pour les requêtes sur les données de série temporelle telles que les collections d’achats ou de clics
* Double-cliquez sur un champ dans le panneau de gauche pour l’insérer rapidement dans l’expression. Évitez de saisir manuellement les chemins d’accès aux champs afin de réduire les erreurs
* Les expressions qui interrogent les événements d’expérience renvoient une valeur booléenne ; assurez-vous que la logique en aval attend un type booléen

**Terminologie:**

* Nom canonique : Éditeur d’expression avancé — Acronyme : none — variantes : éditeur d’expression, éditeur avancé
* Synonymes : « addToCart » = « interaction ajouter au panier » ; « completePurchase » = « événement d’achèvement de l’achat »
* Ne les confondez pas : événements (avec le préfixe `@`) ≠ sources de données (avec le préfixe `#`)

**FAQ:**

* **Q : Pourquoi dois-je utiliser l’éditeur avancé au lieu de l’éditeur simple pour les requêtes d’abandon de panier ?** — L’éditeur simple ne peut pas exécuter de requêtes sur les collections de séries temporelles ; l’éditeur avancé est requis pour les fonctions de collection `all()`, `first()` et `last()`.
* **Q : Comment référencer l’événement « addToCart » le plus récent dans une expression ?** — Utilisez la fonction `first()` sur la collection d’événements d’expérience filtrée par `productInteraction == "addToCart"`, puisque les événements sont renvoyés dans l’ordre chronologique inverse.
* **Q : Comment puis-je faire en sorte qu’une comparaison de chaînes ne respecte pas la casse dans l’éditeur avancé ?** — Utilisez la fonction `equalIgnoreCase()` au lieu de l&#39;opérateur `==`.
* **Q : À quoi sert l’ajout d’une fenêtre d’horodatage lors de l’interrogation d’événements de panier ?** — La spécification d&#39;un horodatage de début et d&#39;un horodatage de fin empêche la collecte de données historiques qui ne sont pas dans la fenêtre d&#39;activité prévue.
* **Q : Comment supprimer les accolades fermées d’une chaîne d’identifiant CRM transmise dans un événement ?** — Utilisez `substr()` combiné avec `lastIndexOf()` pour extraire le contenu entre les accolades.

+++
