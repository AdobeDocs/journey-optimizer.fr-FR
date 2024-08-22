---
solution: Journey Optimizer
product: journey optimizer
title: Intégration à Marketo Engage
description: Découvrir comment utiliser l’action Marketo Engage
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: marketo, intégration marketo engage
source-git-commit: 92591457d2189e3c43ea38c4a09d7cf565bb5d57
workflow-type: tm+mt
source-wordcount: '247'
ht-degree: 76%

---


# Intégration à Marketo Engage {#integrating-with-marketo-engage}

Optez pour une intégration transparente des données avec Marketo Engage. Cette action personnalisée spécifique dans Journey Optimizer prend en charge l’ingestion de deux types de données clés :

* Personnes (profils) : Marketo transforme les profils en informations exploitables.
* Objets personnalisés : personnalisez vos données avec des objets tels que des produits, pour une approche marketing qui vous est propre.

## Conditions préalables {#prerequisites}

* L’instance cliente de Marketo Engage doit être compatible avec IMS.
* Les instances de Marketo Engage et AEP/AJO doivent se trouver dans la même organisation IMS.
* Le client doit être configuré avec **MktoSync : accès au service d’ingestion**

## Configurer l’action {#configure-marketo-action}

* Accédez à Administration > Configurations > Actions et cliquez sur Gérer.
* Dans la liste Actions, cliquez sur Créer une action. En savoir plus sur les [actions personnalisées](../building-journeys/using-custom-actions.md){target="_blank"}.
* Saisissez le nom et la description, puis sélectionnez Adobe Marketo Engage comme type d’action.

![](assets/engage-customaction-creation.png){width="40%" align="left"}

* Cliquez sur Modifier le payload pour les payloads **Requête** et **Réponse**.
* Dans les deux cas, composez votre payload et collez-le dans la fenêtre contextuelle dédiée.

![](assets/engage-customaction-payload.png){width="70%" align="left"}

* Inspecter et configurer des valeurs de payload
Note : pour transmettre des valeurs dynamiquement, pour chaque champ, remplacez **Constante** par **Variable**.

![](assets/engage-customaction-payload-fields.png){width="70%" align="left"}

* Cliquez sur **Enregistrer** dans la fenêtre de configuration du champ, puis sur **Enregistrer** pour votre action personnalisée.

Vous pouvez désormais utiliser votre action personnalisée sur votre zone de travail dédiée.


## Syntaxe du payload {#payload-syntax}

### Personne

![](assets/payload-person.png)

### CustomObject

![](assets/payload-customobject.png)


**Exemple de payload pour une personne**

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


## Utiliser l’action {#engage-using}

* Faites glisser l’action personnalisée sur le canevas de parcours.
* Dans la section **Paramètres de requête**, cliquez sur Modifier pour chacun des paramètres avec des valeurs dynamiques que vous avez configurées dans la payload.

![](assets/engage-use-canvas.png){width="70%" align="left"}

