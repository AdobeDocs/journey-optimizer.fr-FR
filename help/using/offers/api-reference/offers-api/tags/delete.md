---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Supprimer des qualificateurs de collection
description: Les qualificateurs de collection vous permettent de mieux organiser et trier vos offres.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '122'
ht-degree: 100%

---


# Supprimer un qualificateur de collection {#delete-tag}

Il peut parfois être nécessaire de supprimer (DELETE) un qualificateur de collection (précédemment appelé « balise »). Pour ce faire, il vous suffit d’adresser une requête DELETE à l’API de la bibliothèque des offres en utilisant l’identifiant du qualificateur de collection à supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/tags/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | ID de l’entité que vous souhaitez supprimer. | `tag1234` |

**Requête**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/tags/tag1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie un état HTTP 200 et un corps vide.

Vous pouvez confirmer la suppression en tentant d’adresser une requête de recherche (GET) au qualificateur de collection. Vous devriez recevoir le statut HTTP 404 (Introuvable), car le qualificateur de collection a été supprimé.