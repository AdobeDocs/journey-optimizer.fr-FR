---
title: Supprimer une offre de secours
description: Une offre de secours est envoyée aux clients s’ils ne sont pas éligibles pour d’autres offres
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 5c94842a-021c-4a3a-ad9c-ccc2af2c1526
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 0%

---

# Supprimer une offre de secours {#delete-fallback-offer}

Il peut parfois être nécessaire de supprimer (DELETE) une offre de secours. Seules les offres de secours que vous créez dans le conteneur client peuvent être supprimées. Pour ce faire, il vous suffit d’adresser une requête DELETE à l’événement [!DNL Offer Library] API utilisant le $id de l’offre de secours que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison des API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les offres de secours. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID d’instance de l’offre de secours. | `b3966680-13ec-11eb-9c20-8323709cfc65` |

**Requête**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/b3966680-13ec-11eb-9c20-8323709cfc65' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie un état HTTP 202 (No Content) et un corps vide.

Vous pouvez confirmer la suppression en tentant d’adresser une requête de recherche (GET) à l’offre de secours. Vous devez inclure un en-tête Accepter dans la requête, mais vous devriez recevoir le statut HTTP 404 (Introuvable) car l’offre de secours a été supprimée du conteneur.
