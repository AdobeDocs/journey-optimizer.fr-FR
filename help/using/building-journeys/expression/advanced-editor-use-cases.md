---
solution: Journey Optimizer
product: journey optimizer
title: Utilisation de l’éditeur d’expression avancé
description: Découvrez comment créer des expressions avancées
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 753ef9f4-b39d-4de3-98ca-e69a1766a78b
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '489'
ht-degree: 0%

---

# Exemples d’expressions avancées{#advanced-expression-examples}

L’éditeur d’expression avancé permet de créer des conditions pour filtrer les utilisateurs dans vos parcours. Ces conditions vous permettent de cibler les utilisateurs à l’heure, à la date, à l’emplacement, à la durée ou à des actions telles que l’achat ou l’abandon de panier afin qu’ils puissent être reciblés dans le parcours.

>[!NOTE]
>
>Les événements commencent par @, les sources de données par #.

## Création de conditions pour les événements d’expérience

L’éditeur d’expression avancé est obligatoire pour exécuter des requêtes sur des séries temporelles, telles qu’une liste d’achats ou des clics antérieurs sur des messages. Ces requêtes ne peuvent pas être effectuées à l’aide de l’éditeur simple.

Les événements d’expérience sont récupérés à partir d’Adobe Experience Platform sous la forme d’une collection dans l’ordre chronologique inverse. Par conséquent :

* La fonction first renvoie l’événement le plus récent.
* La fonction last renvoie l’événement le plus ancien.

Supposons, par exemple, que vous souhaitiez cibler les clients ayant abandonné leur panier au cours des 7 derniers jours afin d’envoyer un message lorsque le client se trouve à proximité d’un magasin, avec une offre sur les articles qu’il souhaitait et qui se trouvent en magasin.

**Vous devez créer les conditions suivantes :**

Tout d’abord, ciblez les clients qui ont navigué sur la boutique en ligne sans avoir finalisé la commande au cours des 7 derniers jours.

<!--**This expression looks for a specified value in a string value:**

`In (“addToCart”, #{field reference from experience event})`-->

**Cette expression recherche tous les événements relatifs à cet utilisateur spécifiés au cours des 7 derniers jours :**

Il sélectionne ensuite tous les événements addtocart qui n’ont pas été transformés en completePurchase.

>[!NOTE]
>
>Pour insérer rapidement des champs dans l’expression, double-cliquez sur le champ dans le panneau de gauche de l’éditeur.

L’horodatage spécifié agit comme valeur de date et d’heure, la seconde est le nombre de jours.

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

**Maintenant, créons une expression vérifiant que le produit est en stock**

* Dans Inventory, cette expression recherche le champ de quantité d’un produit et indique qu’il doit être supérieur à 0.

`#{Inventory.fieldgroup3.quantity} > 0`

* À droite, les valeurs nécessaires sont spécifiées. Ici, nous devons récupérer l’emplacement du magasin, qui est mappé à partir de l’emplacement de l’événement &quot;ArriveLumaStudio&quot; :

`#{ArriveLumaStudio._acpevangelists1.location.location}`

* Spécifiez la SKU à l’aide de la fonction `first` pour récupérer la dernière interaction &quot;addToCart&quot; :

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

De là, vous pouvez ajouter un autre chemin dans votre parcours pour les cas où le produit n’est pas en magasin et envoyer une notification avec offre d’engagement. Configurez les messages en conséquence et utilisez les données de personnalisation pour améliorer la cible des messages.

## Exemples de manipulations de chaînes avec l’éditeur d’expression avancé

**Dans des conditions**

Cette condition récupère uniquement les événements de géorepérage déclenchés dans &quot;Arlington&quot; :

```json
        @{GeofenceEntry
                    .placeContext
                    .POIinteraction
                    .POIDetail
                    .name} == "Arlington"
```

Explication : Il s’agit d’une comparaison de chaînes stricte (sensible à la casse), équivalente à une requête en mode simple qui utilise `equal to` avec `Is sensitive` coché.

Même requête avec `Is sensitive` La case non cochée génère l’expression suivante en mode avancé :

```json
        equalIgnoreCase(@{GeofenceEntry
                        .placeContext
                        .POIinteraction
                        .POIDetail
                        .name}, "Arlington")
```

**Dans les actions**

L’expression suivante permet de définir l’identifiant CRM dans un champ de personnalisation d’action :

```json
substr(
   @{MobileAppLaunch
   ._myorganization
   .identification
   .crmid},
   1, 
   lastIndexOf(
     @{MobileAppLaunch
     ._myorganization
     .identification
     .crmid},
     '}'
   )
)
```

Explication : Cet exemple utilise `substr` et `lastIndexOf` pour supprimer les accolades qui encadrent l’identifiant CRM transmis avec un événement de lancement d’application mobile.

Pour plus d’informations sur l’utilisation de l’éditeur d’expression avancé, consultez [cette vidéo](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/create-journeys/introduction-to-building-a-journey.html).
