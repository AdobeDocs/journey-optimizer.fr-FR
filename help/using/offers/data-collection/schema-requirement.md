---
product: experience platform
solution: Experience Platform
title: Configurer la capture d’événements
description: Découvrez comment configurer votre schéma d’offre pour capturer les événements.
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: ht
source-wordcount: '206'
ht-degree: 100%

---

# Configurer la collecte de données {#schema-requirements}

<!--To send in feedback data, you must define how the experience events will be captured.-->

Pour obtenir des commentaires sur des types d’événement autres que les événements de décision, vous devez définir la valeur correcte de chaque type d’événement présent dans un **événement d’expérience** envoyé à Adobe Experience Platform.

Pour chaque type d’événement, assurez-vous que le schéma utilisé dans le jeu de données est associé au groupe de champs **[!UICONTROL Événement d’expérience - Interactions de proposition]**. [En savoir plus](create-dataset.md).

Vous trouverez ci-dessous les exigences du schéma que vous devez implémenter dans votre code JavaScript.

>[!NOTE]
>
>Les événements de décision ne doivent pas être envoyés, car la gestion des décisions génère automatiquement ces événements et les place dans le jeu de données **[!UICONTROL ODE DecisionEvents]**<!--to check--> généré automatiquement.

## Suivi des impressions

Assurez-vous que le type d’événement et la source sont les suivants :

**Type d’événement d’expérience :** `decisioning.propositionDisplay`
**Source :** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) ou ingestion par lots
+++**Exemple de payload :**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionDisplay",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4",
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5",
                }
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id - taken from experience event for "nextBestOffer"
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id - taken from experience event for "nextBestOffer"
        }
    ]
}
```

+++

## Suivi des clics

Assurez-vous que le type d’événement et la source sont les suivants :

**Type d’événement d’expérience :** `decisioning.propositionInteract`
**Source :** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) ou ingestion par lots
+++**Exemple de payload :**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionInteract",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4"
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5"
                },
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id
        }
    ]
}
```

+++

## Suivi des événements personnalisés

Pour les événements personnalisés, le schéma utilisé dans le jeu de données doit également être associé au groupe de champs **[!UICONTROL Événement d’expérience - Interactions de proposition]**. Il n’y a toutefois aucune exigence spécifique quant au type d’événement d’expérience qui doit être utilisé pour baliser ces événements.

<!--
## Using a ranking strategy {#using-ranking}

To use the ranking strategy you created above, follow the steps below:

Once a ranking strategy has been created, you can assign it to a placement in a decision. For more on this, see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md).

1. Create a decision.
1. Add a placement.
1. Add a collection.
1. Choose to rank offers by AI ranking (select it from the drop-down list).
1. Click Add ranking.
1. Select the ranking strategy that you created. All the details of the ranking strategy are displayed.
1. Click Next to confirm.
1. Save your decision.

It is now ready to be used in a decision to rank eligible offers for a placement (see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md)).
-->
