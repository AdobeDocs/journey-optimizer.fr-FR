---
title: supprimer des emplacements
description: Les emplacements sont des conteneurs utilisés pour présenter vos offres.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---

# Suppression d’un emplacement

Il peut parfois être nécessaire de supprimer (DELETE) un emplacement. Seuls les emplacements que vous créez dans le conteneur locataire peuvent être supprimés. Pour ce faire, exécutez une requête de DELETE à l&#39;API [!DNL Offer Library] à l&#39;aide de l&#39;ID d&#39;instance de l&#39;emplacement que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les emplacements. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID d&#39;instance de l&#39;emplacement que vous souhaitez mettre à jour. | `9aa58fd0-13d7-11eb-928b-576735ea4db8` |

**Demande**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/9aa58fd0-13d7-11eb-928b-576735ea4db8' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie l’état HTTP 202 (Aucun contenu) et un corps vide.

Vous pouvez confirmer la suppression en tentant d’envoyer une demande de recherche (GET) à l’emplacement. Vous devez inclure un en-tête Accepter dans la requête, mais vous devez recevoir l’état HTTP 404 (Non trouvé) car l’emplacement a été supprimé du conteneur.
