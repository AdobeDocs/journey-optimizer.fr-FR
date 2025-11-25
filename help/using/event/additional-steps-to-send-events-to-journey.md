---
solution: Journey Optimizer
product: journey optimizer
title: Étapes supplémentaires pour l’envoi d’événements à un parcours
description: En savoir plus sur les étapes supplémentaires pour l’envoi d’événements à un parcours
feature: Journeys, Events
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: étapes, configuration, parcours, événements, flux, API
exl-id: e0144151-6c54-4656-9650-b544d8e7be16
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: ht
source-wordcount: '284'
ht-degree: 100%

---

# Étapes supplémentaires pour l’envoi d’événements {#additional-steps-to-send-events}

Pour configurer les événements qui doivent être envoyés aux **[!UICONTROL API d’ingestion en flux continu]** et utilisés dans [!DNL Journey Optimizer], procédez comme suit :

1. Récupérez l’URL d&#39;inlet à partir des API Adobe Experience Platform. En savoir plus sur [Présentation des API d&#39;ingestion en flux continu](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html?lang=fr){target="_blank"}.
1. Copiez la payload depuis son aperçu dans le menu **[!UICONTROL Événement]**. En savoir plus sur [cette page](../event/about-creating.md#define-the-payload-fields).

Vous devez ensuite configurer le système de données qui envoie les événements vers les API d’ingestion en flux continu à l’aide de la payload que vous avez copiée :

1. Configurez un appel d’API POST à l’URL des API d’ingestion en flux continu (désignée sous le nom « inlet »).
1. Utilisez la payload que vous avez copiée depuis [!DNL Journey Optimizer], dans le corps (« section de données ») de l’appel d’API, vers les API d’ingestion en flux continu. Reportez-vous à l’exemple ci-dessous.
1. Déterminez où obtenir toutes les variables présentes dans la payload. Exemple : si l’événement est censé transmettre l’adresse, la payload collée indique &quot;address&quot;: &quot;string&quot;. &quot;string&quot; doit être remplacé par la variable qui renseigne automatiquement la valeur appropriée, c’est-à-dire l’adresse e-mail du destinataire du message. Notez que dans la section **[!UICONTROL En-tête]** de l’aperçu de la payload, de nombreuses valeurs sont renseignées automatiquement afin de vous faciliter la tâche.
1. Sélectionnez &quot;application/json&quot; comme type de corps.
1. Transmettez votre identifiant d’organisation dans l’en-tête à l’aide de la clé « x-gw-ims-org-id ». Pour cette valeur, utilisez votre identifiant d’organisation (« XXX@AdobeOrg »).

Voici un exemple d’événement d’API d’ingestion en flux continu :

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
            "timestamp": "2023-05-29T00:00:00.000Z",
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

Pour identifier plus facilement l’endroit où coller la partie « données », vous pouvez utiliser un outil de visualisation JSON tel que le [formateur JSON](https://jsonformatter.curiousconcept.com){target="_blank"}.

Pour résoudre les problèmes liés aux API d’ingestion en streaming, consultez la [documentation Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=fr){target="_blank"}.
