---
title: Supprimer les décisions
description: Une décision contient la logique sous-tendant la sélection d’une offre.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 1eb19ff1-b210-4891-ab41-5488e2635527
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: tm+mt
source-wordcount: '109'
ht-degree: 100%

---

# Supprimer une décision {#delete-decision}

Il peut parfois être nécessaire de supprimer (DELETE) une décision. Pour ce faire, il vous suffit d’adresser une requête DELETE à l’API [!DNL Offer Library] à l’aide de `id` de la décision que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/offer-decisions/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | ID de l’entité que vous souhaitez supprimer. | `offerDecision1234` |

**Requête**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-decisions/offerDecision1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie un état HTTP 200 et un corps vide.

Vous pouvez confirmer la suppression en tentant d’exécuter une requête de recherche (GET) sur la décision. Vous devriez recevoir le statut HTTP 404 (Introuvable), car la décision a été supprimée.
