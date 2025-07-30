---
title: Identifiant supplémentaire dans les parcours déclenchés par un événement
description: Découvrez comment utiliser un identifiant supplémentaire dans les parcours déclenchés par un événement.
badge: label="Disponibilité limitée" type="Informative"
exl-id: f6ebd706-4402-448a-a538-e9a4c2cf0f8b
source-git-commit: 5e4297fb0e2d0b910c9fe102299162e8bb46a311
workflow-type: tm+mt
source-wordcount: '971'
ht-degree: 96%

---

# Identifiant supplémentaire dans les parcours déclenchés par un événement {#supplemental-id}

>[!CONTEXTUALHELP]
>id="ajo_journey_parameters_supplemental_identifier"
>title="Utiliser un identifiant supplémentaire"
>abstract="L’identifiant supplémentaire est un identifiant secondaire qui fournit un contexte supplémentaire pour l’exécution d’un parcours. Pour le définir, sélectionnez le champ à utiliser comme identifiant supplémentaire et choisissez un espace de noms à lui associer."

>[!AVAILABILITY]
>
>Cette fonctionnalité est disponible uniquement pour un nombre limité d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.

Par défaut, les parcours déclenchés par un événement sont exécutés dans le contexte d’un **identifiant de profil**. Cela signifie que, tant que le profil est actif dans un parcours donné, il ne pourra pas rejoindre à nouveau un autre parcours. Pour éviter cela, Journey Optimizer vous permet de capturer un **identifiant supplémentaire** dans vos événements, tel qu’un identifiant de commande, d’abonnement ou d’ordonnance, en plus de l’identifiant de profil.
Dans cet exemple, nous avons ajouté un identifiant de réservation en tant qu’identifiant supplémentaire.

![](assets/event-supplemental-id.png){width=40% zoomable}

Ce faisant, les parcours déclenchés par l’événement sont exécutés dans le contexte de l’identifiant de profil associé à l’identifiant supplémentaire (ici, l’identifiant de réservation). Une instance du parcours est exécutée pour chaque itération de l’identifiant supplémentaire. Cela permet plusieurs entrées du même ID de profil dans les parcours s’ils ont effectué des réservations différentes.

En outre, Journey Optimizer vous permet d’utiliser les attributs de l’identifiant supplémentaire (par exemple, le numéro de réservation, la date de renouvellement de l’ordonnance, le type de produit) pour personnaliser les messages, ce qui garantit des communications hautement pertinentes. <!--Example: A healthcare provider can send renewal reminders for each prescription in a patient's profile.-->

➡️ [Découvrez cette fonctionnalité en vidéo.](#video)

## Mécanismes de sécurisation et limitations {#guardrails}

* **Limites d’instances simultanées** : les profils ne peuvent pas avoir plus de 10 instances de parcours simultanées.

<!--* **Array depth**: Supplemental identifier objects can have a maximum depth of 3 levels (2 levels of nesting).

    +++Example

    ```
    [
    (level 1) "Atorvastatin" : {
    "description" : "used to lower cholesterol",
    "renewal_date" : "11/20/25",
    "dosage" : "10mg"
    (level 2) "ingredients" : [
    (level 3) "Atorvastatin calcium",
    "lactose monohydrate",
    "microcrystalline cellulose",
    "other" ]
    }
    ]
    ```

    +++
-->
* **Critères de sortie** : si les critères de sortie sont déclenchés, toutes les instances du profil sont actives dans le parcours à ce moment-là. Il ne dépendrait pas du contexte de la combinaison identifiant de profil + identifiant supplémentaire.

* **Règles de fréquence** : chaque instance de parcours créée à partir de l’utilisation d’identifiants supplémentaires est comptabilisée dans le capping de la fréquence, même si un seul événement entraîne plusieurs instances de parcours.

* **Type de données et structure du schéma** : l’identifiant supplémentaire doit être de type `string`. Il peut s’agir d’un attribut de chaîne indépendant ou d’un attribut de chaîne dans un tableau d’objets. L’attribut de chaîne indépendant entraîne une instance de parcours unique, tandis que l’attribut de chaîne dans un tableau d’objets entraîne une instance de parcours unique par itération du tableau d’objets. Les tableaux et mappages de chaînes ne sont pas pris en charge.

* **Réentrée dans un parcours**

  Le comportement de réentrée d’un parcours avec des identifiants supplémentaires respecte la politique de réentrée existante :

   * Si le parcours ne prend pas en charge la rentrée, la même combinaison d’identifiant de profil + identifiant supplémentaire ne peut pas réintégrer le parcours.
   * Si le parcours prend en charge la rentrée avec une période, la même combinaison d’identifiant de profil + identifiant supplémentaire peut réintégrer après la période définie.

* **Configuration des événements en aval**

  Si vous utilisez un autre événement en aval dans le parcours, il doit utiliser le même ID supplémentaire et avoir le même espace de noms d’ID.

## Ajouter un identifiant supplémentaire et l’utiliser dans un parcours {#add}

Pour utiliser un identifiant supplémentaire dans un parcours, procédez comme suit :

1. **Marquez l’attribut comme identifiant dans le schéma d’événement.**

   1. Accédez au schéma d’événement et localisez l’attribut que vous souhaitez utiliser comme identifiant supplémentaire (par exemple, identifiant de réservation, identifiant d’abonnement) et marquez-le comme identifiant. [Découvrez comment utiliser les schémas.](../data/get-started-schemas.md)

   1. Marquez l’identifiant comme une **[!UICONTROL identité]**.

      ![](assets/supplemental-ID-schema.png)

      >[!IMPORTANT]
      >
      >Veillez à ne pas marquer l’attribut comme **identité principale**.

   1. Sélectionnez l’espace de noms à associer à l’identifiant supplémentaire. Il doit s’agir d’un espace de noms d’identifiant qui ne porte pas sur une personne.

1. **Ajoutez l’ID supplémentaire à l’événement.**

   1. Créez ou modifiez l’événement souhaité. [Découvrez comment configurer un événement unitaire.](../event/about-creating.md)

   1. Dans l’écran de configuration des événements, cochez l’option **[!UICONTROL Utiliser un identifiant supplémentaire]**.

      ![](assets/supplemental-ID-event.png)

   1. Utilisez l’éditeur d’expression pour sélectionner l’attribut que vous avez marqué comme ID supplémentaire.

      >[!NOTE]
      >
      >Veillez à utiliser l’éditeur d’expression en **[!UICONTROL mode avancé]** pour sélectionner l’attribut.

   1. Après avoir sélectionné l’ID supplémentaire, l’espace de noms associé s’affiche en lecture seule dans l’écran de configuration de l’événement.

1. **Ajoutez l’événement au parcours.**

   Faites glisser l’événement personnalisé sur la zone de travail de parcours. Cela déclenche l’entrée de parcours en fonction de l’identifiant de profil et de l’identifiant supplémentaire.

   ![](assets/supplemental-ID-journey.png)

1. **Utilisez des attributs d’ID supplémentaires.**

   Utilisez l’éditeur d’expression et l’éditeur de personnalisation pour référencer les attributs de l’identifiant supplémentaire à des fins de personnalisation ou de logique conditionnelle. Les attributs sont accessibles à partir du menu **[!UICONTROL Attributs contextuels]**.

   ![](assets/supplemental-ID-perso.png)

   >[!NOTE]
   >
   >Si vous utilisez des tableaux (par exemple, plusieurs ordonnances ou contrats d’assurance), utilisez une formule pour extraire des éléments spécifiques.

+++ Voir les exemples

   Dans un tableau d’objets avec l’ID supplémentaire comme `bookingNum` et un attribut au même niveau appelé `bookingCountry`, le parcours effectue une itération sur l’objet de tableau en fonction de bookingNum et crée une instance de parcours sur chaque objet.

   * L’expression suivante dans l’activité de condition effectue une itération sur le tableau d’objets et vérifie si la valeur de `bookingCountry` est égale à « FR » :

     ```
     @event{<event_name>.<object_path>.<object_array_name>.all(currentEventField.<attribute_path>.bookingNum==${supplementalId}).at(0).<attribute_path>.bookingCountry}=="FR"
     ```

   * L’expression suivante dans l’éditeur de personnalisation d’e-mail effectue une itération dans le tableau d’objets, extrait la valeur `bookingCountry` applicable à l’instance de parcours active et l’affiche dans le contenu :

     ```
     {{#each context.journey.events.<event_ID>.<object_path>.<object_array_name> as |l|}} 
     
     {%#if l.<attribute_path>.bookingNum = context.journey.technicalProperties.supplementalId%} {{l.<attribute_path>.bookingCountry}}  {%/if%}
     
     {{/each}}
     ```

   * Exemple d’événement de déclenchement du parcours :

     ```
     "bookingList": [
           {
               "bookingInfo": {
                   "bookingNum": "x1",
                         "bookingCountry": "US"
               }
           },
           {
               "bookingInfo": {
                   "bookingNum": "x2",
                   "bookingCountry": "FR"
               }
           }
       ]
     ```

+++

1. **Publiez le parcours.**

   Une fois configuré, publiez le parcours pour commencer à utiliser plusieurs entrées simultanées en fonction d’identifiants supplémentaires.

## Exemples de cas d’utilisation

### **Notifications de renouvellement des contrats d’assurance**

* **Scénario** : une compagnie d’assurance envoie des rappels de renouvellement portant sur chaque contrat d’assurance actif détenu par un client ou une cliente.
* **Exécution** :
   * Profil : « John ».
   * ID supplémentaires : `"AutoPolicy123", "HomePolicy456"`.
   * Le parcours s’exécute séparément pour chaque contrat d’assurance, avec des dates de renouvellement personnalisées, des détails sur la couverture et des informations sur les versements.

### **Gestion des abonnements**

* **Scénario** : un service d’abonnement envoie des messages personnalisés pour chaque abonnement lorsqu’un événement est déclenché pour cet abonnement.
* **Exécution** :
   * Profil : « Jane ».
   * ID supplémentaires : `"Luma Yoga Program ", "Luma Fitness Program"`.
   * Chaque événement comprend un ID d’abonnement et des détails sur cet abonnement. Le parcours s’exécute séparément pour chaque événement/abonnement, ce qui permet d’utiliser des offres de renouvellement personnalisées.

### **Recommandations de produit**

* **Scénario** : une plateforme d’e-commerce envoie des recommandations sur la base de produits spécifiques achetés par un client ou une cliente.
* **Exécution** :
   * Profil : « Alex ».
   * ID supplémentaires : `"productID1234", "productID5678"`.
   * Le parcours s’exécute séparément pour chaque produit, avec des opportunités de montée en gamme personnalisées.

## Vidéo pratique {#video}

Découvrez comment activer et appliquer un identifiant supplémentaire dans [!DNL Adobe Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3464794?quality=12&captions=fre_fr)
