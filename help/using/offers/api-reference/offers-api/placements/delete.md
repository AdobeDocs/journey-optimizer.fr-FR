---
title: supprimer des emplacements
description: Les emplacements sont des conteneurs utilisés pour présenter vos offres.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: ca7af3b0-62cd-44ac-8856-b3d1ec15f284
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '145'
ht-degree: 0%

---

# Supprimer un emplacement {#delete-placement}

Il peut parfois être nécessaire de supprimer (DELETE) un emplacement. Seuls les emplacements que vous créez dans le conteneur de tenant peuvent être supprimés. Pour ce faire, il vous suffit d’adresser une requête DELETE à l’événement [!DNL Offer Library] API utilisant l’ID d’instance de l’emplacement que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison des API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les emplacements. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID d’instance de l’emplacement que vous souhaitez mettre à jour. | `9aa58fd0-13d7-11eb-928b-576735ea4db8` |

**Requête**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/9aa58fd0-13d7-11eb-928b-576735ea4db8' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie un état HTTP 202 (No Content) et un corps vide.

Vous pouvez confirmer la suppression en tentant d’adresser une requête de recherche (GET) à l’emplacement. Vous devez inclure un en-tête Accepter dans la requête, mais vous devriez recevoir le statut HTTP 404 (Introuvable) car l’emplacement a été supprimé du conteneur.
