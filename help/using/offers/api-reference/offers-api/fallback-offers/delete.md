---
title: Suppression d’une offre de secours
description: Une offre de secours est envoyée aux clients s’ils ne sont pas éligibles à d’autres offres.
feature: Decision Management, API
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 5c94842a-021c-4a3a-ad9c-ccc2af2c1526
source-git-commit: 07b1f9b885574bb6418310a71c3060fa67f6cac3
workflow-type: tm+mt
source-wordcount: '117'
ht-degree: 100%

---


# Suppression d’une offre de secours {#delete-fallback-offer}

Il peut parfois être nécessaire de supprimer (DELETE) une offre de secours. Pour ce faire, il vous suffit d’exécuter une requête DELETE sur l’API [!DNL Offer Library] en utilisant l’identifiant de l’offre de secours que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/offers/{ID}?offer-type=fallback
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | ID de l’entité que vous souhaitez supprimer. | `fallbackOffer1234` |

**Requête**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offers/fallbackOffer1234?offer-type=fallback' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie un état HTTP 200 et un corps vide.

Vous pouvez confirmer la suppression en tentant d’adresser une requête de recherche (GET) à l’offre. Vous devriez recevoir le statut HTTP 404 (Introuvable) car l’offre de secours a été supprimée.
