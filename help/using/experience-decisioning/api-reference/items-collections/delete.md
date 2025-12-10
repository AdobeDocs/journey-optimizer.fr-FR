---
title: Supprimer une collection d’éléments
description: Découvrez comment classer vos décisions de groupe en collections.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 7290c857-cbc7-4197-ae13-430adcf1649b
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 100%

---

# Supprimer une collection d’éléments {#delete-decision-item}

Il peut parfois être nécessaire de supprimer (DELETE) une collection d’éléments. Pour ce faire, il vous suffit d’adresser une requête DELETE à l’API Bibliothèque des offres en utilisant l’identifiant de la collection d’éléments à supprimer.

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

Vous pouvez confirmer la suppression en tentant d’adresser une requête de recherche (GET) à la collection d’éléments. Vous devriez recevoir le statut HTTP 404 (Introuvable), car la collection d’éléments a été supprimée.
