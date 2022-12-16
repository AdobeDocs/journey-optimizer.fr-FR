---
title: Suppression de règles de décision
description: Les règles de décision sont des contraintes ajoutées à une offre personnalisée et appliquées à un profil pour déterminer son éligibilité.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52f4803b-9e9a-4ad0-ae24-de652006763d
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '159'
ht-degree: 100%

---

# Supprimer une règle de décision {#delete-decision-rule}

Il peut parfois être nécessaire de supprimer (DELETE) une règle de décision. Seules les règles de décision que vous créez dans le conteneur de tenant peuvent être supprimées. Pour ce faire, il vous suffit d’adresser une requête DELETE à l’API [!DNL Offer Library] à l’aide de l’ID d’instance de la règle de décision que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d&#39;accès de point d&#39;entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les règles de décision. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | ID d’instance de la règle de décision que vous souhaitez mettre à jour. | `eaa5af90-13d9-11eb-9472-194dee6dc381` |

**Requête**

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

Une réponse réussie renvoie un statut HTTP 202 (Pas de contenu) et un corps vide.

Vous pouvez confirmer la suppression en tentant d’adresser une requête de recherche (GET) à la règle de décision. Vous devez inclure un en-tête Accepter dans la requête, mais vous devriez recevoir le statut HTTP 404 (Introuvable) car la règle de décision a été supprimée du conteneur.
