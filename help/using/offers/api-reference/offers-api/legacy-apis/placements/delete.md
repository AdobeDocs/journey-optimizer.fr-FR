---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: suppression d’emplacements
description: Les emplacements sont des conteneurs utilisés pour présenter vos offres.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 944efb12-6745-4bb2-be52-293e23925350
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 100%

---

# Supprimer un emplacement {#delete-placement}

Il peut parfois être nécessaire de supprimer (DELETE) un emplacement. Seuls les emplacements que vous créez dans le conteneur du tenant peuvent être supprimés. Pour ce faire, il suffit d’adresser une requête DELETE à l’API [!DNL Offer Library] à l’aide de l’ID d’instance de l’emplacement que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les emplacements. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID d’instance de l’emplacement que vous souhaitez mettre à jour. | `9aa58fd0-13d7-11eb-928b-576735ea4db8` |

**Requête**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/9aa58fd0-13d7-11eb-928b-576735ea4db8' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie un statut HTTP 202 (Pas de contenu) et un corps vide.

Vous pouvez confirmer la suppression en tentant d’envoyer une demande de recherche (GET) à l’emplacement. Vous devez inclure un en-tête Accepter dans la requête, mais vous devriez recevoir le statut HTTP 404 (Introuvable) car l’emplacement a été supprimé du conteneur.
