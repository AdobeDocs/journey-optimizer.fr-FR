---
solution: Journey Optimizer
product: journey optimizer
title: Intégration à Marketo Engage
description: Découvrir comment utiliser l’action Marketo Engage
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Developer, Admin
level: Intermediate
keywords: marketo, intégration marketo engage
exl-id: 70d1ef5a-743b-4362-bb65-93a8c996209f
TQID: https://experienceleague.adobe.com/-aRINahKmp9bI1tyW-XA-LzZOFeoEPXpWoH8JydG6Rk
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: df401a2a-327d-468c-a5e4-b7b7ccd071a0
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 326
ht-degree: 96%

---

# Intégration à Marketo Engage {#integrating-with-marketo-engage}

Optez pour une intégration transparente des données avec Marketo Engage. Une action personnalisée spécifique est disponible dans vos parcours pour intégrer Adobe Journey Optimizer et Marketo Engage. Cette action personnalisée prend en charge l’ingestion de deux types de données clés :

* **Personnes** (profils) : Marketo transforme les profils en informations exploitables.
* **Objets personnalisés** : personnalisez vos données avec des objets personnalisés tels que des produits, pour une approche marketing qui vous est propre.

## Conditions préalables {#prerequisites}

Les conditions préalables suivantes s’appliquent à cette intégration :

* L’instance cliente de Marketo Engage doit être compatible avec IMS.
* L’instance Marketo Engage et l’instance Adobe Experience Platform/Journey Optimizer doivent se trouver dans la même organisation.
* Le client ou la cliente doit recevoir un accès **MktoSync : service d’ingestion**.

## Configurer l’action {#configure-marketo-action}


Dans Journey Optimizer, vous devez configurer une action personnalisée pour Marketo Engage. Procédez comme suit :

1. Sélectionnez **[!UICONTROL Configurations]** dans la section du menu ADMINISTRATION.
1. Dans la section **[!UICONTROL Actions]**, cliquez sur **[!UICONTROL Créer une action]**. Le volet de configuration des actions s’ouvre sur le côté droit de l’écran.
1. Saisissez Nom, Description et sélectionnez **&#x200B;**&#x200B;comme **Type d&#39;action**
   ![](assets/engage-customaction-creation.png){width="40%" align="left"}
1. Cliquez sur **Modifier la payload** pour les payloads **Requête** et **Réponse**.
1. Dans les deux cas, composez votre payload et collez-la dans la fenêtre contextuelle dédiée.
   ![](assets/engage-customaction-payload.png){width="70%" align="left"}
1. Inspecter et configurer des valeurs de payload

   Remarque : pour transmettre des valeurs dynamiquement, remplacez **Constante** par **Variable** pour chaque champ.

   ![](assets/engage-customaction-payload-fields.png){width="70%" align="left"}

1. Cliquez sur **Enregistrer** dans l’écran de configuration du champ, puis sur **Enregistrer** pour votre action personnalisée.

Vous pouvez désormais utiliser votre action personnalisée dans la votre zone de travail de votre parcours.

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

Pour chaque action configurée, une activité d’action Marketo Engage est disponible dans la palette du concepteur de parcours.

Pour l’utiliser, procédez comme suit :

1. Faites glisser l’action personnalisée sur la zone de travail de parcours.

1. Saisissez le libellé et la description de cette action.

1. Dans la section **Paramètres de requête**, cliquez sur l’icône **Modifier** pour chaque paramètre et sélectionnez les valeurs dynamiques que vous avez configurées dans la payload.

![](assets/engage-use-canvas.png){width="70%" align="left"}
