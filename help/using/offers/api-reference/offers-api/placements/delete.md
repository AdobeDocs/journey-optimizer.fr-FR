---
title: suppression d’emplacements
description: Les emplacements sont des conteneurs utilisés pour présenter vos offres.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: ca7af3b0-62cd-44ac-8856-b3d1ec15f284
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: ht
source-wordcount: '107'
ht-degree: 100%

---

# Supprimer un emplacement {#delete-placement}

Il peut parfois être nécessaire de supprimer (DELETE) un emplacement. Pour ce faire, il suffit d’adresser une requête DELETE à l’API [!DNL Offer Library] à l’aide de l’ID de l’emplacement que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/placements/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | ID d’instance de l’emplacement que vous souhaitez mettre à jour. | `offerPlacement1234` |

**Requête**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/placements/offerPlacement1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie un état HTTP 200 et un corps vide.

Vous pouvez confirmer la suppression en tentant d’adresser une requête de recherche (GET) à l’emplacement. Vous devriez recevoir le statut HTTP 404 (Introuvable), car l’emplacement a été supprimé.
