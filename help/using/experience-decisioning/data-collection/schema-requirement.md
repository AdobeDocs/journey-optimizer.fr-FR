---
solution: Journey Optimizer
product: Journey Optimizer
title: Configurer la capture d’événements
description: Découvrez comment configurer votre schéma d’offre pour capturer les événements.
feature: Ranking, Datasets, Decision Management
role: Developer
level: Experienced
exl-id: ce3a2c33-c15b-436f-90b1-7373d7b2b1ca
version: Journey Orchestration
source-git-commit: 5de16a8f69089e49484104bbae109df111cbf1ed
workflow-type: tm+mt
source-wordcount: '231'
ht-degree: 49%

---

# Configurer la collecte de données {#schema-requirements}

Pour obtenir des commentaires sur des types d’événement autres que les événements de décision, vous devez définir la valeur correcte de chaque type d’événement présent dans un **événement d’expérience** envoyé à Adobe Experience Platform.

>[!CAUTION]
>
>Pour chaque type d’événement, assurez-vous que le schéma utilisé dans le jeu de données est associé au groupe de champs **[!UICONTROL Événement d’expérience - Interactions de proposition]**. <!--[Learn more](create-dataset.md)-->

Vous trouverez ci-dessous les exigences du schéma que vous devez implémenter dans votre code JavaScript.

## Suivi des impressions {#track-impressions}

Vérifiez que les champs suivants sont correctement configurés :

**Type d’événement d’expérience :** `decisioning.propositionDisplay`

**propositionEventType:** `_experience.decisioning.propositionEventType.display`

**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) ou ingestion par lots

+++**Exemple de payload :**

```json
{
  "_experience": {
    "decisioning": {
      "propositionEventType": {
        "display": 1
      },
      "proposition": [
        {
          "items": [
            {
              "itemSelection": {
                "rankingDetail": {
                  "algorithmID": "RANDOM",
                  "strategyID": "1YYKhS4MImWqIBrpudMIf4",
                  "trafficType": "random",
                  "step": "aiModel"
                },
                "selectionDetail": {
                  "selectionType": "selectionStrategy",
                  "strategyName": "not a real selection strategy",
                  "strategyID": "dps:selection-strategy:1b630b32da42125a",
                  "version": "35a6b5b1-62ff-4a4b-94cd-96852a59d89a"
                }
              },
              "name": "not a real offer",
              "id": "dps:14c7468e7f6271ff8023748a1146d11f05f77b7fc1368081:1b630a7d8d9f2g4j",
              "score": 0.9765416360350985
            }
          ],
          "scopeDetails": {
            "decisionPolicy": {
              "id": "01c3ad3d-6d41-4013-a88f-5a4975579179"
            },
            "decisionProvider": "EXD",
            "placement": {
              "id": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test"
            },
            "correlationID": "28ca161e-552c-464e-dh37-bc38d4ce944b-0"
          },
          "scope": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test",
          "id": "86fb8f37-0498-4533-9dab-c206690c1f67"
        }
      ],
      "exdRequestID": "edb61199-ef92-46c8-adc5-f622df5b9078"
    }
  },
  "eventType": "decisioning.propositionDisplay",
  "_id": "04b5384e-c09c-4df8-b6f0-7c476a51b219",
  "timestamp": "2025-10-07T20:22:00Z"
}
```

+++

## Suivi des clics {#track-clicks}

Vérifiez que les champs suivants sont correctement configurés :

**Type d’événement d’expérience :** `decisioning.propositionInteract`

**propositionEventType:** `_experience.decisioning.propositionEventType.interact`

**Source:** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) ou ingestion par lots

Chaque offre dans une proposition comprend un jeton de suivi, qui est un identifiant unique généré par Adobe. Ce jeton doit être transmis exactement tel qu’il est reçu, sans modification, dans l’événement de clic ou d’impression correspondant. Les jetons de suivi correspondants permettent à Adobe d’associer précisément l’action de l’utilisateur à la décision d’offre correcte, ce qui active la création de rapports en aval et l’optimisation basée sur l’IA.

+++**Exemple de payload :**

```json
{
  "_experience": {
    "decisioning": {
      "propositionEventType": {
        "interact": 1
      },
      "propositionAction": {
        "tokens": [
          "Vx9fwWXmp6/kyYRVOUZWEQ"
        ]
      },
      "proposition": [
        {
          "items": [
            {
              "itemSelection": {
                "rankingDetail": {
                  "algorithmID": "RANDOM",
                  "strategyID": "1YYKhS4MImWqIBrpudMIf4",
                  "trafficType": "random",
                  "step": "aiModel"
                },
                "selectionDetail": {
                  "selectionType": "selectionStrategy",
                  "strategyName": "not a real selection strategy",
                  "strategyID": "dps:selection-strategy:1b630b32da42125a",
                  "version": "35a6b5b1-62ff-4a4b-94cd-96852a59d89a"
                }
              },
              "name": "not a real offer",
              "id": "dps:14c7468e7f6271ff8023748a1146d11f05f77b7fc1368081:1b630a7d8d9f2g4j",
              "score": 0.9765416360350985
            }
          ],
          "scopeDetails": {
            "decisionPolicy": {
              "id": "01c3ad3d-6d41-4013-a88f-5a4975579179"
            },
            "decisionProvider": "EXD",
            "placement": {
              "id": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test"
            },
            "correlationID": "28ca161e-552c-464e-dh37-bc38d4ce944b-0"
          },
          "scope": "a99d6b1e-5930-4ba6-hd64-17a14bb15032#farouk-img-test",
          "id": "86fb8f37-0498-4533-9dab-c206690c1f67"
        }
      ],
      "exdRequestID": "edb61199-ef92-46c8-adc5-f622df5b9078"
    }
  },
  "eventType": "decisioning.propositionInteract",
  "_id": "04b5384e-c09c-4df8-b6f0-7c476a51b765",
  "timestamp": "2025-10-07T20:50:00Z"
}
```

+++

## Suivi des événements personnalisés {#track-custom-events}

Pour les événements personnalisés, le schéma utilisé dans le jeu de données doit également être associé au groupe de champs **[!UICONTROL Événement d’expérience - Interactions de proposition]**. Il n’y a toutefois aucune exigence spécifique quant au type d’événement d’expérience qui doit être utilisé pour baliser ces événements.

<!--

>[!NOTE]
>
>To have your custom events accounted for in [capping](../items.md#capping), you need to connect the experience event to Adobe Experience Platform endpoints by sending it to either one of these two Edge data collection endpoints:
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>If you are using the [Adobe Experience Platform Web SDK](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html){target="_blank"} or [Adobe Experience Platform Mobile SDK](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html){target="_blank"}, the connection is made automatically.-->

