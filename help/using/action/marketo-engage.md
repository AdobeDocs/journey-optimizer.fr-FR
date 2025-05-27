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
exl-id: 70d1ef5a-743b-4362-bb65-93a8c996209f
source-git-commit: d92c280e40419d2e3ec62a7ba85cd492a0867fde
workflow-type: tm+mt
source-wordcount: '325'
ht-degree: 29%

---

# Intégration à Marketo Engage {#integrating-with-marketo-engage}

Optez pour une intégration transparente des données avec Marketo Engage. Une action personnalisée spécifique est disponible dans vos parcours pour intégrer Adobe Journey Optimizer et Marketo Engage. Cette action personnalisée prend en charge l’ingestion de deux types de données clés :

* **Personnes** (profils) : Marketo transforme les profils en informations exploitables.
* **Objets personnalisés** : personnalisez vos données à l’aide d’objets personnalisés, tels que des produits, pour une approche marketing personnalisée.

## Conditions préalables {#prerequisites}

Les conditions préalables suivantes s’appliquent à cette intégration :

* L’instance client de Marketo Engage doit être compatible IMS
* L’instance Marketo Engage et l’instance Adobe Experience Platform/Journey Optimizer doivent se trouver dans la même organisation
* Le client ou la cliente doit recevoir un accès **MktoSync : service d’ingestion**.

## Configuration de l’action {#configure-marketo-action}


Dans Journey Optimizer, vous devez configurer une action personnalisée pour Marketo Engage. Procédez comme suit :

1. Sélectionnez **[!UICONTROL Configurations]** dans la section du menu ADMINISTRATION.
1. Dans la section **[!UICONTROL Actions]**, cliquez sur **[!UICONTROL Créer une action]**. Le volet de configuration des actions s&#39;ouvre dans la droite de l&#39;écran.
1. Saisissez Nom, Description et sélectionnez **Adobe Marketo Engage** comme **Type d&#39;action**

![](assets/engage-customaction-creation.png){width="40%" align="left"}

1. Cliquez sur l’icône **Modifier la payload** pour vos payloads **Requête** et **Réponse**.
1. Pour les deux, composez votre payload et collez-la dans la fenêtre contextuelle dédiée.

![](assets/engage-customaction-payload.png){width="70%" align="left"}

1. Inspecter et configurer des valeurs de payload
Note : pour transmettre des valeurs dynamiquement, pour chaque champ, remplacez **Constante** par **Variable**.

![](assets/engage-customaction-payload-fields.png){width="70%" align="left"}

1. Cliquez sur **Enregistrer** dans l’écran Configuration du champ, puis sur **Enregistrer** votre action personnalisée.

Vous pouvez maintenant utiliser votre action personnalisée sur la zone de travail du parcours.

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

Pour chaque action configurée, une activité d’action Marketo Engage est disponible dans la palette du Concepteur de parcours.

Pour l’utiliser, procédez comme suit :

1. Faites glisser l’action personnalisée sur la zone de travail de parcours.

1. Saisissez le libellé et la description de cette action.

1. Dans la section **Paramètres de requête**, cliquez sur l’icône **Modifier** pour chacun des paramètres et sélectionnez les valeurs dynamiques que vous avez configurées dans la payload.

![](assets/engage-use-canvas.png){width="70%" align="left"}
