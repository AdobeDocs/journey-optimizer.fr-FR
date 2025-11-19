---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Suppression d’offres personnalisées
description: Une offre personnalisée est un message marketing personnalisable basé sur des contraintes et des règles d’éligibilité.
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 52a5053d-3b94-47fd-a064-a20f9a595150
version: Journey Orchestration
source-git-commit: d6a9a8a392f0492aa6e4f059198ce77b6b2cd962
workflow-type: ht
source-wordcount: '116'
ht-degree: 100%

---

# Supprimer une offre personnalisée {#delete-personalized-offer}

Il peut parfois être nécessaire de supprimer (DELETE) une offre personnalisée. Pour ce faire, il vous suffit d’adresser une requête DELETE à l’API [!DNL Offer Library] en utilisant l’identifiant de l’offre personnalisée que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/offers/{ID}?offer-type=personalized
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps/` |
| `{ID}` | ID de l’entité que vous souhaitez supprimer. | `personalizedOffer1234` |

**Requête**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offers/personalizedOffer1234?offer-type=personalized' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer  {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie un état HTTP 200 et un corps vide.

Vous pouvez confirmer la suppression en tentant d’adresser une requête de recherche (GET) à l’offre personnalisée. Vous devriez recevoir l’état HTTP 404 (Introuvable) car l’offre personnalisée a été supprimée.
