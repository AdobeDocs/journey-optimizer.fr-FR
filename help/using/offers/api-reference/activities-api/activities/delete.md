---
title: Supprimer les décisions
description: Une décision contient la logique qui sous-tend la sélection d’une offre.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '146'
ht-degree: 1%

---

# Supprimer une décision

Il peut parfois être nécessaire de supprimer (DELETE) une décision (précédemment connue sous le nom d&#39;activité d&#39;offre). Seules les décisions que vous créez dans le conteneur locataire peuvent être supprimées. Pour ce faire, exécutez une requête de DELETE à l&#39;API [!DNL Offer Library] en utilisant $id de l&#39;offre de secours que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les décisions. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID d’instance de la décision. | `f88c9be0-1245-11eb-8622-b77b60702882` |

**Demande**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/f88c9be0-1245-11eb-8622-b77b60702882' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie l’état HTTP 202 (Aucun contenu) et un corps vide.

Vous pouvez confirmer la suppression en tentant d’envoyer une demande de recherche (GET) à la décision. Vous devez inclure un en-tête Accepter dans la requête, mais vous devez recevoir un état HTTP 404 (Non trouvé) car la décision a été supprimée du conteneur.
