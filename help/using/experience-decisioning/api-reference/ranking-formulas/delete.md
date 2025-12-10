---
title: Supprimer une formule de classement
description: Les formules de classement permettent de définir les fonctions de notation utilisées pour classer les éléments.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 4ea50481-b1b9-4e0c-ad4e-c4139891bfdf
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 100%

---

# Supprimer une formule de classement {#delete-selection-strategy}

Il peut parfois être nécessaire de supprimer (DELETE) une formule de classement. Pour ce faire, il vous suffit d’effectuer une requête DELETE sur l’API Bibliothèque des offres en utilisant l’ID de la formule de classement à supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/ranking-formulas/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID de l’entité que vous souhaitez supprimer. | `rankingFormula1234` |

**Requête**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/ranking-formulas/rankingFormula1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie un état HTTP 200 et un corps vide.

Vous pouvez confirmer la suppression en tentant d’effectuer une requête de recherche (GET) sur la formule de classement. Vous devriez recevoir le statut HTTP 404 (Introuvable), car la formule de classement a été supprimée.
