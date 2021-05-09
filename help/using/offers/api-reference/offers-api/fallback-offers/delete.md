---
title: Suppression d’une offre de secours
description: Une offre de secours est envoyée aux clients s'ils ne sont pas éligibles pour d'autres offres
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '153'
ht-degree: 1%

---

# Suppression d’une offre de secours

Il peut parfois être nécessaire de supprimer (DELETE) une offre de secours. Seules les offres de secours que vous créez dans le conteneur client peuvent être supprimées. Pour ce faire, exécutez une requête de DELETE à l&#39;API [!DNL Offer Library] en utilisant $id de l&#39;offre de secours que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les offres de secours. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID d’instance de l’offre de secours. | `b3966680-13ec-11eb-9c20-8323709cfc65` |

**Demande**

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

Une réponse réussie renvoie l’état HTTP 202 (Aucun contenu) et un corps vide.

Vous pouvez confirmer la suppression en tentant d’envoyer une demande de recherche (GET) à l’offre de secours. Vous devez inclure un en-tête Accepter dans la requête, mais vous devez recevoir l’état HTTP 404 (Introuvable) car l’offre de secours a été supprimée du conteneur.
