---
title: Supprimer un élément de décision
description: Les éléments de décision sont des offres marketing que vous pouvez créer et organiser en collections et en catalogues.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 0fd608e0-df71-4e2d-8304-d7d5561c7c7a
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/OkPIse7NFATcyTdTT0pzNhjPMenbrvigSG2lSRatb-M
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 112
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
