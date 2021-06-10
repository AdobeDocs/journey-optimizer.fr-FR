---
title: Supprimer les décisions
description: Une décision contient la logique sous-tendant la sélection d’une offre.
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: ht
source-wordcount: '146'
ht-degree: 100%

---

# Supprimer une décision

Il peut parfois être nécessaire de supprimer (DELETE) une décision (auparavant « activité d’offre »). Seules les décisions que vous créez dans le conteneur du tenant peuvent être supprimées. Pour ce faire, il vous suffit d’adresser une requête DELETE à l’API [!DNL Offer Library] en utilisant le $id de l’offre de secours que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les décisions. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID d’instance de la décision. | `f88c9be0-1245-11eb-8622-b77b60702882` |

**Requête**

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

Une réponse réussie renvoie un statut HTTP 202 (Pas de contenu) et un corps vide.

Vous pouvez confirmer la suppression en tentant d’exécuter une requête de recherche (GET) sur la décision. Vous devez inclure un en-tête Accepter dans la requête, mais vous devriez recevoir le statut HTTP 404 (Introuvable) car la décision a été supprimée du conteneur.
