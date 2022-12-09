---
title: Suppression d’une collection
description: Les collections sont des sous-ensembles d’offres basés sur des conditions prédéfinies définies par un marketeur, telles que la catégorie de l’offre.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 2eaa0092-2436-4679-83f1-7530ab4a858f
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '154'
ht-degree: 0%

---

# Suppression d’une collection {#delete-collection}

Il peut parfois être nécessaire de supprimer (DELETE) une collection. Seules les collections que vous créez dans le conteneur client peuvent être supprimées. Pour ce faire, il vous suffit d’adresser une requête DELETE à l’événement [!DNL Offer Library] API utilisant le $id de la collection que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison des API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les collections. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID d’instance de la collection que vous souhaitez mettre à jour. | `0bf31c20-13f1-11eb-a752-e58fd7dc4cb3` |

**Requête**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/0bf31c20-13f1-11eb-a752-e58fd7dc4cb3' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie un état HTTP 202 (No Content) et un corps vide.

Vous pouvez confirmer la suppression en tentant d’adresser une requête de recherche (GET) à la collection. Vous devez inclure un en-tête Accepter dans la requête, mais vous devriez recevoir le statut HTTP 404 (Introuvable) car la collection a été supprimée du conteneur.
