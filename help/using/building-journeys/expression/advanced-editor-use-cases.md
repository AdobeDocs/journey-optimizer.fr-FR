---
solution: Journey Optimizer
product: journey optimizer
title: Utilisation de l’éditeur d’expression avancé
description: Découvrir comment créer des expressions avancées
feature: Journeys
role: Developer
level: Experienced
hide: true
hidefromtoc: true
keywords: expression, condition, cas d’utilisation, événements
exl-id: 753ef9f4-b39d-4de3-98ca-e69a1766a78b
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: ht
source-wordcount: '547'
ht-degree: 100%

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
>Les événements commencent par le caractère @, les sources de données par #.

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
