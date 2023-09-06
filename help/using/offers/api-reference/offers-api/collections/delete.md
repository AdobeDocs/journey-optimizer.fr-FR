---
title: Suppression d’une collection
description: Les collections sont des sous-ensembles d’offres basés sur des conditions prédéfinies établies par un spécialiste marketing, telles que la catégorie de l’offre.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 2eaa0092-2436-4679-83f1-7530ab4a858f
source-git-commit: 3568e86015ee7b2ec59a7fa95e042449fb5a0693
workflow-type: tm+mt
source-wordcount: '115'
ht-degree: 48%

---

# Suppression d’une collection {#delete-collection}

Il peut parfois être nécessaire de supprimer (DELETE) une collection. Pour ce faire, il vous suffit d’adresser une requête de DELETE au [!DNL Offer Library] API utilisant la variable `id` de la collection que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/offer-collections/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison des API de persistance. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID de l’entité que vous souhaitez supprimer. | `offerCollection1234` |

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

Vous pouvez confirmer la suppression en tentant d’adresser une requête de recherche (GET) à la collection. Vous devriez recevoir le statut HTTP 404 (Introuvable) car la collection a été supprimée.
