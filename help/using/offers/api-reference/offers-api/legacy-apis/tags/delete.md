---
title: Supprimer des qualificateurs de collection
description: Les qualificateurs de collection vous permettent de mieux organiser et trier vos offres.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 335c1b80-f1f0-4fd0-add8-84b8cc5e2e00
source-git-commit: 54b92b19f2e3a6afa6557ffeff0d971a4c411510
workflow-type: tm+mt
source-wordcount: '116'
ht-degree: 35%

---

# Supprimer un qualificateur de collection {#delete-tag}

Il peut parfois être nécessaire de supprimer (DELETE) un qualificateur de collection (précédemment appelé « balise »). Pour ce faire, il vous suffit d’adresser une requête de DELETE au [!DNL Offer Library] API utilisant l’identifiant du qualificateur de collection que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/tags/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison des API de persistance. | `https://platform.adobe.io/data/core/dps/` |
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

Une réponse réussie renvoie un état HTTP 200 et un corps vide.

Vous pouvez confirmer la suppression en tentant d’adresser une requête de recherche (GET) au qualificateur de collection et vous devriez recevoir le statut HTTP 404 (Introuvable), car il a été supprimé.