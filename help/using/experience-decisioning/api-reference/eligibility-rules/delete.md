---
title: Supprimer une règle d'éligibilité
description: Les règles d’éligibilité vous permettent de définir les candidats éligibles en fonction de ce que vous souhaitez cibler, comme les attributs de profil et les audiences.
feature: Decision Management, API, Collections
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: 8fa34ebb7c853f9af5b3f58574374a3acb641dd9
workflow-type: tm+mt
source-wordcount: '127'
ht-degree: 25%

---

# Supprimer une règle d&#39;éligibilité {#delete-eligibility-rule}

Il peut parfois être nécessaire de supprimer (DELETE) une règle d’éligibilité. Pour ce faire, il suffit d&#39;adresser une requête DELETE à l&#39;API de la bibliothèque des offres à l&#39;aide de l&#39;identifiant de la règle d&#39;éligibilité que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/eligibility-rules/{ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API Persistence | `https://platform.adobe.io/data/core/dps` |
| `{ID}` | ID de l’entité que vous souhaitez supprimer. | `rule1234` |

**Requête**

```shell
curl -X DELETE 'https://platform.adobe.io/data/core/dps/offer-rules/rule1234' \
-H 'Content-Type: application/json' \
-H 'Authorization: Bearer {ACCESS_TOKEN}' \
-H 'x-api-key: {API_KEY}' \
-H 'x-gw-ims-org-id: {IMS_ORG}' \
-H 'x-sandbox-name: {SANDBOX_NAME}'
```

**Réponse**

Une réponse réussie renvoie un état HTTP 200 et un corps vide.

Vous pouvez confirmer la suppression en tentant d’adresser une requête de recherche (GET) à la règle . Vous devriez recevoir un statut HTTP 404 (Introuvable), car la règle a été supprimée.
