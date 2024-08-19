---
title: Suppression d’une collection d’éléments
description: Découvrez comment classer les décisions de groupe en collections.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: eb89bc5205d98a67cd0bb42bebbd9429786e33e7
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 28%

---


# Suppression d’une collection d’éléments {#delete-decision-item}

Il peut parfois être nécessaire de supprimer (DELETE) une collection d’articles. Pour ce faire, il vous suffit d’adresser une requête de DELETE à l’API de bibliothèque des offres à l’aide de l’identifiant de la collection d’articles que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/item-collections/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID de l’entité que vous souhaitez supprimer. | `itemCollections1234` |

**Requête**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/item-collections/itemCollections1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie un état HTTP 200 et un corps vide.

Vous pouvez confirmer la suppression en tentant d’adresser une requête de recherche (GET) à la collection d’éléments. Vous devriez recevoir le statut HTTP 404 (Introuvable) car la collection d’éléments a été supprimée.
