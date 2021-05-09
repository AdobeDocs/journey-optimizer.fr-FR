---
title: Autres étapes pour envoyer des événements à un parcours
description: Découvrez les étapes supplémentaires à suivre pour envoyer des événements à un parcours
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '292'
ht-degree: 0%

---

# Autres étapes pour envoyer des événements {#concept_xrz_n1q_y2b}

![](../assets/do-not-localize/badge.png)

Pour configurer les événements à envoyer aux **[!UICONTROL API d&#39;importation en flux continu]** et à utiliser dans [!DNL Journey Optimizer], procédez comme suit :

1. Récupérez l’URL d’entrée à partir des API Adobe Experience Platform. En savoir plus sur [Présentation des API d&#39;importation en flux continu](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/overview.html).
1. Copiez la charge utile de la prévisualisation de charge dans le menu **[!UICONTROL Événement]**. En savoir plus sur [cette page](../event/about-creating.md#define-the-payload-fields).

Vous devez ensuite configurer le système de données qui pousse les événements vers les API d&#39;importation en flux continu à l&#39;aide de la charge utile que vous avez copiée :

1. Configurez un appel d&#39;API POST vers l&#39;URL des API d&#39;importation en flux continu (appelée entrée).
1. Utilisez la charge utile que vous avez copiée à partir de [!DNL Journey Optimizer] dans le corps (&quot;section de données&quot;) de l&#39;appel d&#39;API aux API de gestion en flux continu. Voir ci-dessous pour un exemple
1. Déterminez où obtenir toutes les variables présentes dans la charge utile. Exemple : si le événement est censé transmettre l&#39;adresse, la charge utile collée indique &quot;adresse&quot; : &quot;string&quot;. &quot;string&quot; doit être remplacé par la variable qui renseigne automatiquement la bonne valeur, à savoir l’adresse électronique de la personne à laquelle envoyer un message. Notez que dans la prévisualisation de charge utile, dans la section **[!UICONTROL En-tête]**, nous renseignons automatiquement de nombreuses valeurs censées faciliter votre travail.
1. Sélectionnez &quot;application/json&quot; comme type de corps.
1. Transmettez votre ID d’organisation IMS dans l’en-tête à l’aide de la clé &quot;x-gw-ims-org-id&quot;. Pour cette valeur, utilisez votre ID d’organisation IMS (&quot;XXX@AdobeOrg&quot;).

Voici un exemple de événement d&#39;API d&#39;importation en flux continu :

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

Pour faciliter l’identification de l’emplacement où coller la partie &quot;données&quot;, vous pouvez utiliser un outil de visualisation JSON tel que [https://jsonformatter.curiousconcept.com](https://jsonformatter.curiousconcept.com)

Pour dépanner Streaming Ingestion APIs, consultez cette [page](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html).
