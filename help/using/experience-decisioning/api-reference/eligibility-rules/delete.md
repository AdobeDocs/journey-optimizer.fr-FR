---
title: Supprimer une règle d’éligibilité
description: Les règles d’éligibilité permettent de définir les candidats éligibles en fonction de ce que vous souhaitez cibler, comme les attributs de profil et les audiences.
feature: API, Collections, Decisioning
topic: Integrations
role: Developer
level: Experienced
exl-id: 19baf888-23b7-46de-9d3c-9a0fa8ab2297
version: Journey Orchestration
source-git-commit: 1735324b5fd330ecfc9261a54d0317b71d57ff4f
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 100%

---

# Supprimer une règle d’éligibilité {#delete-eligibility-rule}

Il peut parfois être nécessaire de supprimer (DELETE) une règle d’éligibilité. Pour ce faire, il vous suffit d’effectuer une requête DELETE sur l’API Bibliothèque des offres en utilisant l’ID de la règle d’éligibilité à supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/eligibility-rules/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID de l’entité que vous souhaitez supprimer. | `rule1234` |

**Requête**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-rules/rule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie un état HTTP 200 et un corps vide.

Vous pouvez confirmer la suppression en tentant d’effectuer une requête de recherche (GET) sur la règle. Vous devriez recevoir le statut HTTP 404 (Introuvable) car la règle a été supprimée.
