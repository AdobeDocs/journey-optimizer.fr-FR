---
title: Suppression de balises
description: Les balises vous permettent de mieux organiser et trier vos offres.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '143'
ht-degree: 1%

---

# Suppression d’une balise

Il peut parfois être nécessaire de supprimer (DELETE) une balise. Seules les balises que vous créez dans le conteneur client peuvent être supprimées. Pour ce faire, exécutez une requête de DELETE à l&#39;API [!DNL Offer Library] en utilisant $id de la balise que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les balises. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID d’instance de la balise que vous souhaitez mettre à jour. | `d48fd160-13dc-11eb-bc55-c11be7252432` |

**Demande**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/d48fd160-13dc-11eb-bc55-c11be7252432' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie l’état HTTP 202 (Aucun contenu) et un corps vide.

Vous pouvez confirmer la suppression en tentant d’envoyer une requête de recherche (GET) à la balise . Vous devez inclure un en-tête Accepter dans la requête, mais vous devez recevoir l’état HTTP 404 (Introuvable) car la balise a été supprimée du conteneur.
