---
solution: Journey Optimizer
product: journey optimizer
title: Intégration avec Marketo Engage
description: Découvrez comment utiliser l’action du Marketo Engage
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
hide: true
hidefromtoc: true
keywords: marketo, marketo engagement de l’intégration
source-git-commit: 8a8741281edafb812f92ebb8da6dd68d3535f3e1
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 1%

---


# Intégration avec Marketo Engage {#integrating-with-marketo-engage}

Embarquez sur un parcours d’intégration transparente des données avec Marketo Engage. Cette action personnalisée spécifique dans Journey Optimizer prend en charge l’ingestion de deux types de données clés :

* Personnes (profils) : Marketo transforme les profils en informations exploitables.
* Objets personnalisés : personnalisez vos données avec des objets personnalisés, tels que des produits, pour une approche marketing personnalisée.

## Conditions préalables {#prerequisites}

* L’instance de client du Marketo Engage doit être compatible avec IMS.
* Les instances de Marketo Engage et AEP/AJO doivent se trouver dans la même organisation IMS. +link
* Le client doit être configuré avec l’accès à MktoSync : Ingestion Service (REMARQUE POUR AJOUTER ICI + lien).

## Configuration de l’action {#configure-marketo-action}

* Accédez à Administration > Paramétrages > Actions et cliquez sur Gérer .
* Dans la liste Actions , cliquez sur Créer une action. En savoir plus sur la création d’actions personnalisées ici (+lien)
* Saisissez le nom et la description, puis sélectionnez Adobe Marketo Engage comme type d’action.

![](assets/engage-customaction-creation.png){width="40%" align="left"}

* Cliquez sur Modifier la payload pour les payloads **Request** et **Response**.
* Pour les deux, composez votre payload et collez-la dans la fenêtre contextuelle dédiée.

![](assets/engage-customaction-payload.png){width="70%" align="left"}

* Inspect et configuration des valeurs de payload
Remarque : Pour transmettre des valeurs dynamiquement, pour chaque champ, remplacez **Constante** par **Variable**.

![](assets/engage-customaction-payload-fields.png){width="70%" align="left"}

* Cliquez sur **Enregistrer** dans la fenêtre de configuration du champ, puis sur **Enregistrer** pour votre action personnalisée.

Vous pouvez désormais utiliser votre action personnalisée sur votre zone de travail dédiée.


## Syntaxe de la payload {#payload-syntax}

### Personne

![](assets/payload-person.png)

### CustomObject

![](assets/payload-customobject.png)


**Exemple de payload pour Personne**

```json
{
   "munchkinID": "388-KKG-245",  
   "person": {
    "priority": "normal",
    "partitionName": "XYZ",
    "dedupeFields": {
      "field1": "email",
      "field2": "firstName"
    },
    "objects": [
      {
        "email": "Email address",
        "firstName": "First name",
        "lastName": "Last name"
      }
    ]
  }
}
```

**Exemple de payload pour un objet personnalisé**

```json
{
  "munchkinID": "388-KKG-245", 
  "customObject": {
    "priority": "normal",
    "objectName": "products",
    "objects": [
      {
        "email": "Email Address",
        "productName": "Product Name",
        "productQty": "Product Quantity",
        "priceTotal": "Price Total"
      }
    ]
  }
}
```


## Utilisation de l’action {#engage-using}

* Faites glisser l’action personnalisée sur le canevas de parcours. (Voir Comment utiliser une action/un lien personnalisé)
* Dans Paramètres de requête, cliquez sur Modifier pour chacun des paramètres avec des valeurs dynamiques que vous avez configurées dans la payload.

![](assets/engage-use-canvas.png){width="70%" align="left"}

