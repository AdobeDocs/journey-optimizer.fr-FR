---
title: Suppression de règles de décision
description: Les règles de décision sont des contraintes ajoutées à une offre personnalisée et appliquées à un profil pour déterminer son éligibilité.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 52f4803b-9e9a-4ad0-ae24-de652006763d
source-git-commit: 3568e86015ee7b2ec59a7fa95e042449fb5a0693
workflow-type: tm+mt
source-wordcount: '118'
ht-degree: 35%

---

# Supprimer une règle de décision {#delete-decision-rule}

Il peut parfois être nécessaire de supprimer (DELETE) une règle de décision. Pour ce faire, il vous suffit d’adresser une requête de DELETE au [!DNL Offer Library] API utilisant la variable `id` de la règle de décision que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/offer-rules/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point de terminaison des API de persistance. | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID de l’entité que vous souhaitez supprimer. | `offerRule1234` |

**Requête**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-rules/offerRule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie un état HTTP 200 et un corps vide.

Vous pouvez confirmer la suppression en tentant d’adresser une requête de recherche (GET) à la règle de décision et vous devriez recevoir le statut HTTP 404 (Introuvable) car la règle de décision a été supprimée.
