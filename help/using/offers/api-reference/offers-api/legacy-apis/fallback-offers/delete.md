---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Suppression d’une offre de secours
description: Une offre de secours est envoyée aux clients s’ils ne sont pas éligibles à d’autres offres.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 5e97a1fd-7542-4c9a-8234-21c1fa419671
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '155'
ht-degree: 100%

---

# Suppression d’une offre de secours {#delete-fallback-offer}

Il peut parfois être nécessaire de supprimer (DELETE) une offre de secours. Seules les offres de secours que vous créez dans le conteneur de tenant peuvent être supprimées. Pour ce faire, il vous suffit d&#39;exécuter une requête DELETE sur l&#39;API [!DNL Offer Library] en utilisant le $id de l&#39;offre de secours que vous souhaitez supprimer.

**Format d&#39;API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les offres de secours. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID d’instance de l’offre de secours. | `b3966680-13ec-11eb-9c20-8323709cfc65` |

**Requête**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/b3966680-13ec-11eb-9c20-8323709cfc65' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie un statut HTTP 202 (Pas de contenu) et un corps vide.

Vous pouvez confirmer la suppression en tentant d’adresser une requête de recherche (GET) à l’offre de secours. Vous devez inclure un en-tête Accepter dans la requête, mais vous devriez recevoir le statut HTTP 404 (Introuvable) car l’offre de secours a été supprimée du conteneur.
