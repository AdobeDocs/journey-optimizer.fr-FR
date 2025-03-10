---
title: Suppression d'une formule de classement
description: Les formules de classement vous permettent de définir les fonctions de notation utilisées pour classer les éléments.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '123'
ht-degree: 19%

---

# Suppression d&#39;une formule de classement {#delete-selection-strategy}

Il peut parfois être nécessaire de supprimer (DELETE) une formule de classement. Pour ce faire, il suffit d&#39;adresser une requête DELETE à l&#39;API de la bibliothèque des offres à l&#39;aide de l&#39;identifiant de la formule de classement que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/ranking-formulas/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | L’identifiant de l’entité que vous souhaitez supprimer. | `rankingFormula1234` |

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

Vous pouvez confirmer la suppression en tentant d’adresser une requête de recherche (GET) à la formule de classement. Vous devriez recevoir un statut HTTP 404 (Introuvable), car la formule de classement a été supprimée.

