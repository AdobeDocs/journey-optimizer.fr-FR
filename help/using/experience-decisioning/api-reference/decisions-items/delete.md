---
title: Supprimer un élément de décision
description: Les éléments de décision sont des offres marketing que vous pouvez créer et organiser en collections et en catalogues.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: eb89bc5205d98a67cd0bb42bebbd9429786e33e7
workflow-type: ht
source-wordcount: '112'
ht-degree: 100%

---


# Supprimer un élément de décision {#delete-decision-item}

Pour supprimer un élément de décision, il vous suffit d’adresser une requête DELETE à l’API Bibliothèque des offres en utilisant l’identifiant de l’élément de décision à supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/offer-items/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID de l’entité que vous souhaitez supprimer. | `offerItem1234` |

**Requête**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-items/offerItem1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}' \
-H 'x-schema-id: {SCHEMA_ID}'
```

**Réponse**

Une réponse réussie renvoie un état HTTP 200 et un corps vide.

Vous pouvez confirmer la suppression en tentant d’exécuter une requête de recherche (GET) sur l’élément de décision. Vous devriez recevoir le statut HTTP 404 (Introuvable), car l’élément de décision a été supprimé.
