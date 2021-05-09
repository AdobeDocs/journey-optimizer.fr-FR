---
title: Supprimer les règles de décision
description: Les règles de décision sont des contraintes ajoutées à une offre personnalisée et appliquées à un profil pour déterminer son éligibilité.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 1%

---

# Supprimer une règle de décision

Il peut parfois être nécessaire de supprimer (DELETE) une règle de décision. Seules les règles de décision que vous créez dans le conteneur client peuvent être supprimées. Pour ce faire, exécutez une requête de DELETE à l&#39;API [!DNL Offer Library] à l&#39;aide de l&#39;ID d&#39;instance de la règle de décision que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les règles de décision. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID d&#39;instance de la règle de décision que vous souhaitez mettre à jour. | `eaa5af90-13d9-11eb-9472-194dee6dc381` |

**Demande**

```shell
curl -X DELETE \
  'https://platform.adobe.io/data/core/xcore/e0bd8463-0913-4ca1-bd84-6309134ca1f6/instances/eaa5af90-13d9-11eb-9472-194dee6dc381' \
  -H 'Accept: application/vnd.adobe.platform.xcore.xdm.receipt+json; version=1' \
  -H 'Authorization: Bearer {ACCESS_TOKEN}' \
  -H 'x-api-key: {API_KEY}' \
  -H 'x-gw-ims-org-id: {IMS_ORG}' \
  -H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie l’état HTTP 202 (Aucun contenu) et un corps vide.

Vous pouvez confirmer la suppression en tentant d’envoyer une requête de recherche (GET) à la règle de décision. Vous devez inclure un en-tête Accepter dans la requête, mais vous devez recevoir un état HTTP 404 (Non trouvé) car la règle de décision a été supprimée du conteneur.
