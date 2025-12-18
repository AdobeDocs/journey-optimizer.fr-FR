---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Supprimer des qualificateurs de collection
description: Les qualificateurs de collection vous permettent de mieux organiser et trier vos offres.
feature: Decision Management, API
badge: label="Hérité" type="Informative"
topic: Integrations
role: Developer
level: Experienced
exl-id: cc67519e-7a80-49c7-8c8b-c777be633026
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '177'
ht-degree: 100%

---

# Supprimer un qualificateur de collection {#delete-tag}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../../experience-decisioning/gs-experience-decisioning.md)


Il peut parfois être nécessaire de supprimer (DELETE) un qualificateur de collection (précédemment appelé « balise »). Seuls les qualificateurs de collection créés dans le conteneur client peuvent être supprimés. Pour ce faire, il vous suffit d’adresser une requête DELETE à l’API [!DNL Offer Library] en utilisant l’« $id » du qualificateur de collection que vous souhaitez supprimer.

**Format d’API**

```http
DELETE /{ENDPOINT_PATH}/{CONTAINER_ID}/instances/{INSTANCE_ID}
```

| Paramètre | Description | Exemple |
| --------- | ----------- | ------- |
| `{ENDPOINT_PATH}` | Chemin d’accès de point d’entrée pour les API de référentiel. | `https://platform.adobe.io/data/core/xcore/` |
| `{CONTAINER_ID}` | Conteneur où se trouvent les qualificateurs de collection. | `e0bd8463-0913-4ca1-bd84-6309134ca1f6` |
| `{INSTANCE_ID}` | Identifiant d’instance du qualificateur de collection que vous souhaitez mettre à jour. | `d48fd160-13dc-11eb-bc55-c11be7252432` |

**Requête**

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

Une réponse réussie renvoie un statut HTTP 202 (Pas de contenu) et un corps vide.

Vous pouvez confirmer la suppression en tentant d’adresser une requête de recherche (GET) au qualificateur de collection. Vous devez inclure l’en-tête Accept dans la requête, mais vous devriez recevoir le statut HTTP 404 (Introuvable), car le qualificateur de collection a été supprimé du conteneur.
