---
solution: Journey Optimizer
product: journey optimizer
title: Étapes supplémentaires pour l’envoi d’événements à un parcours
description: Découvrez les étapes supplémentaires pour envoyer des événements à un parcours
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '279'
ht-degree: 0%

---

# Étapes supplémentaires pour l’envoi d’événements {#additional-steps-to-send-events}

Pour configurer les événements à envoyer à **[!UICONTROL Streaming Ingestion APIs]** et à utiliser dans [!DNL Journey Optimizer], procédez comme suit :

1. Récupérez l’URL d’inlet à partir des API d’Adobe Experience Platform. En savoir plus dans [Présentation des API d’ingestion en flux continu](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html){target=&quot;_blank&quot;}.
1. Copiez la payload à partir de l’aperçu de la payload dans le **[!UICONTROL Event]** . En savoir plus dans [cette page](../event/about-creating.md#define-the-payload-fields).

Vous devez ensuite configurer le système de données qui envoie les événements vers les API d’ingestion en flux continu à l’aide de la payload que vous avez copiée :

1. Configurez un appel d’API POST à l’URL des API d’ingestion en flux continu (appelée inlet).
1. Utilisez la payload à partir de laquelle vous avez copié [!DNL Journey Optimizer] dans le corps (&quot;section de données&quot;) de l’appel API aux API d’ingestion en flux continu. Voir ci-dessous pour un exemple
1. Déterminez où obtenir toutes les variables présentes dans la payload. Exemple : si l’événement est censé transmettre l’adresse, la payload collée indique &quot;address&quot; : &quot;string&quot;. &quot;string&quot; doit être remplacé par la variable qui renseigne automatiquement la valeur appropriée, à savoir l’email de la personne à qui envoyer un message. Notez que dans l’aperçu de la payload, dans la variable **[!UICONTROL Header]** , nous renseignons automatiquement de nombreuses valeurs censées faciliter votre travail.
1. Sélectionnez &quot;application/json&quot; comme type de corps.
1. Transmettez votre ID d’organisation dans l’en-tête à l’aide de la clé &quot;x-gw-ims-org-id&quot;. Pour la valeur , utilisez l’ID d’organisation (&quot;XXX@AdobeOrg&quot;).

Voici un exemple d’événement API d’ingestion en flux continu :

```
{
    "header": {
        "msgType": "xdmEntityCreate",
        "msgId": "c25585b9-252e-431d-b562-e73da70c04e7",
        "msgVersion": "1.0",
        "xactionId": "f5995abe-c49d-4848-9577-a7a4fc2996fb",
        "datasetId": "string - required if you want the data to land in a specific dataset - not mandatory",
        "imsOrgId": "XXX@AdobeOrg",
        "schemaRef": {
            "id": "XXX",
            "contentType": "application/vnd.adobe.xed-full+json;version=1"
        },
        "source": {
            "name": "Journeys"
        }
    },
    "body": {
        "xdmMeta": {
            "schemaRef": {
                "id": "XXX",
                "contentType": "application/vnd.adobe.xed-full+json;version=1"
            }
        },
        "xdmEntity": {
            "_instance_name": {
                "person": {
                    "firstName": "string",
                    "lastName": "string",
                    "gender": "string",
                    "birthYear": 10,
                    "emailAddress": "string"
                }
            },
            "identityMap": {
                "Email": [
                {
                    "id": "string"
                    }
                ]
            },
            "_id": "string",
            "timestamp": "2018-05-29T00:00:00.000Z",
            "_experience": {
                "campaign": {
                    "orchestration": {
                    "eventID": "XXX"
                    }
                }
            }
        }
    }
}
```

Pour identifier plus facilement l’emplacement où coller la partie &quot;données&quot;, vous pouvez utiliser un outil de visualisation JSON tel que [Formateur JSON](https://jsonformatter.curiousconcept.com){target=&quot;_blank&quot;}.

Pour résoudre les problèmes liés aux API d’ingestion en flux continu, reportez-vous à la section [Documentation d’Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html){target=&quot;_blank&quot;}.
