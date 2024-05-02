---
solution: Journey Optimizer
product: journey optimizer
title: Utilisation d’actions personnalisées pour écrire des événements de Parcours dans AEP
description: Utilisation d’actions personnalisées pour écrire des événements de Parcours dans AEP
feature: Journeys, Use Cases, Custom Actions
topic: Content Management
role: Developer, Data Engineer
level: Experienced
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '324'
ht-degree: 0%

---


# Cas pratique : utilisation d’actions personnalisées pour écrire des événements de Parcours dans Experience Platform{#custom-action-aep}

Ce cas pratique explique comment écrire des événements personnalisés dans Adobe Experience Platform à partir de Parcours à l’aide d’actions personnalisées et d’appels authentifiés.

## Configuration d’un projet d’E/S

1. Dans la console Adobe Developer, cliquez sur **Projet** et ouvrez votre projet d’E/S.

1. Dans le **Informations d’identification** , cliquez sur **OAuth serveur à serveur**.

   ![](assets/custom-action-aep-1.png)

1. Cliquez sur **Afficher cURL, commande**.

   ![](assets/custom-action-aep-2.png)

1. Copiez la commande cURL et stockez client_id, client_secret, grant_type et scope.

```
curl -X POST 'https://ims-na1.adobelogin.com/ims/token/v3' -H 'Content-Type: application/x-www-form-urlencoded' -d 'grant_type=client_credentials&client_id=1234&client_secret=5678&scope=openid,AdobeID,read_organizations,additional_info.projectedProductContext,session'
```

## Configuration de la source à l’aide de l’API HTTP Inlet

1. Créez un point de terminaison dans Adobe Experience Platform pour écrire les données à partir de parcours.

1. Dans Adobe Experience Platform, cliquez sur **Sources**, sous **Connexions** dans le menu de gauche. Sous **API HTTP**, cliquez sur **Ajouter des données**.

   ![](assets/custom-action-aep-3.png)

1. Sélectionner **Nouveau compte** et activez l’authentification. Cliquez sur **Connexion à la source**.

   ![](assets/custom-action-aep-4.png)

1. Cliquez sur **Suivant** et sélectionnez le jeu de données dans lequel vous souhaitez écrire les données. Cliquez sur **Suivant** et **Terminer**.

   ![](assets/custom-action-aep-5.png)

1. Ouvrez le nouveau flux de données. Copiez la payload du schéma et enregistrez-la dans votre notepad.

```
{
"header": {
"schemaRef": {
"id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
"contentType": "application/vnd.adobe.xed-full+json;version=1.0"
},
"imsOrgId": "<org_id>",
"datasetId": "<dataset_id>",
"source": {
"name": "Custom Journey Events"
}
},
"body": {
"xdmMeta": {
"schemaRef": {
"id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
"contentType": "application/vnd.adobe.xed-full+json;version=1.0"
}
},
"xdmEntity": {
"_id": "test1",
"<your_org>": {
"journeyVersionId": "",
"nodeId": "", "customer_Id":""
},
"eventMergeId": "",
"eventType": "",
"producedBy": "self",
"timestamp": "2018-11-12T20:20:39+00:00"
}
}
}
```

## Configuration de l’action personnalisée

1. Ouvrez Adobe Journey Optimizer, puis cliquez sur **Configurations**, sous **Administration** dans le menu de gauche. Sous **Actions**, cliquez sur **Gérer** et cliquez sur **Créer une action**.

1. Définissez l’URL et sélectionnez la méthode Post .

   `https://dcs.adobedc.net/collection/<collection_id>?syncValidation=false`

1. Assurez-vous que les en-têtes (Content-Type, Charset, sandbox-name) sont configurés.

   ![](assets/custom-action-aep-7bis.png)

### Configuration de l’authentification

1. Sélectionnez la variable **Type** as **Personnalisé** avec la charge utile suivante.

1. Collez client_secret, client_id, scope et grant_type (à partir de la charge utile du projet IO utilisée précédemment).

   ```
   {
   "type": "customAuthorization",
   "authorizationType": "Bearer",
   "endpoint": "https://ims-na1.adobelogin.com/ims/token/v3",
   "method": "POST",
   "headers": {},
   "body": {
   "bodyType": "form",
   "bodyParams": {
   "grant_type": "client_credentials",
   "client_secret": "********",
   "client_id": "<client_id>",
   "scope": "openid,AdobeID,read_organizations,additional_info.projectedProductContext,session"
   }
   },
   "tokenInResponse": "json://access_token",
   "cacheDuration": {
   "duration": 28000,
   "timeUnit": "seconds"
   }
   }
   ```

1. Utilisez la variable **Cliquez sur pour tester l’authentification.** pour tester la connexion.

   ![](assets/custom-action-aep-8.png)

### Configuration de la charge utile

1. Dans le **Requête** et **Réponse** , collez la charge utile de la connexion source utilisée auparavant.

   ```
   {
   "xdmMeta": {
   "schemaRef": {
   "id": "https://ns.adobe.com/<your_org>/schemas/<schema_id>",
   "contentType": "application/vnd.adobe.xed-full+json;version=1.0"
   }
   },
   "xdmEntity": {
   "_id": "/uri-reference",
   "<your_org>": {
   "journeyVersionId": "Sample value",
   "nodeId": "Sample value",
   "customer_Id":""
   },
   "eventMergeId": "Sample value",
   "eventType": "advertising.completes,
   "producedBy": "self",
   "timestamp": "2018-11-12T20:20:39+00:00"
   }
   }
   ```

1. Modifiez la configuration du champ de **Constante** to **Variable** pour les champs qui seront renseignés dynamiquement. Enregistrez l’action personnalisée.

## Parcours

1. Enfin, utilisez cette action personnalisée dans un parcours pour écrire les événements de parcours personnalisés.

1. Renseignez l’ID de version du Parcours, l’ID de noeud, le nom du noeud et d’autres attributs en fonction de votre cas d’utilisation.

   ![](assets/custom-action-aep-9.png)


