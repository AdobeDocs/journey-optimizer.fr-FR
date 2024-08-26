---
title: Supprimer une stratégie de sélection
description: Les stratégies de sélection se composent de collections associées à des contraintes et à des méthodes de classement pour déterminer les offres.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: c555e6a6d88f43d7c29e27060d464b8fd21aed96
workflow-type: ht
source-wordcount: '121'
ht-degree: 100%

---


# Supprimer une stratégie de sélection {#delete-selection-strategy}

Il peut parfois être nécessaire de supprimer (DELETE) une stratégie de sélection. Pour ce faire, il vous suffit d’adresser une requête DELETE à l’API Bibliothèque des offres en utilisant l’identifiant de la stratégie de sélection à supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/selection-strategies/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID de l’entité que vous souhaitez supprimer. | `selectionStrategy1234` |

**Requête**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/selection-strategies/selectionStrategy1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie un état HTTP 200 et un corps vide.

Vous pouvez confirmer la suppression en tentant d’adresser une requête de recherche (GET) à la stratégie de sélection. Vous devriez recevoir le statut HTTP 404 (Introuvable), car la stratégie de sélection a été supprimée.
