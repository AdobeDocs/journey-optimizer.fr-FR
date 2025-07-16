---
product: experience platform
solution: Experience Platform
title: Configurer la capture d’événements
description: Découvrez comment configurer votre schéma d’offre pour capturer les événements.
feature: Ranking, Datasets, Decision Management
role: Developer, Data Engineer
level: Experienced
hide: true
hidefromtoc: true
exl-id: ce3a2c33-c15b-436f-90b1-7373d7b2b1ca
source-git-commit: 0bba63855360d0dcd7daa98a2083f23995b88b94
workflow-type: ht
source-wordcount: '271'
ht-degree: 100%

---

# Configurer la collecte de données {#schema-requirements}

Pour obtenir des commentaires sur des types d’événement autres que les événements de décision, vous devez définir la valeur correcte de chaque type d’événement présent dans un **événement d’expérience** envoyé à Adobe Experience Platform.

>[!CAUTION]
>
>Pour chaque type d’événement, assurez-vous que le schéma utilisé dans le jeu de données est associé au groupe de champs **[!UICONTROL Événement d’expérience - Interactions de proposition]**. [En savoir plus](create-dataset.md).

Vous trouverez ci-dessous les exigences du schéma que vous devez implémenter dans votre code JavaScript.

>[!NOTE]
>
>Les événements de décision ne doivent pas être envoyés, car la gestion des décisions génère automatiquement ces événements et les place dans le jeu de données **[!UICONTROL ODE DecisionEvents]**<!--to check--> généré automatiquement.

## Suivi des impressions {#track-impressions}

Assurez-vous que le type d’événement et la source sont les suivants :

**Type d’événement d’expérience :** `decisioning.propositionDisplay`
**Source :** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) ou ingestion par lots
+++**Exemple de payload :**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2023-09-26T15:52:25+00:00",
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

## Suivi des clics {#track-clicks}

Assurez-vous que le type d’événement et la source sont les suivants :

**Type d’événement d’expérience :** `decisioning.propositionInteract`
**Source :** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) ou ingestion par lots
+++**Exemple de payload :**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2023-09-26T15:52:25+00:00",
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

## Suivi des événements personnalisés {#track-custom-events}

Pour les événements personnalisés, le schéma utilisé dans le jeu de données doit également être associé au groupe de champs **[!UICONTROL Événement d’expérience - Interactions de proposition]**. Il n’y a toutefois aucune exigence spécifique quant au type d’événement d’expérience qui doit être utilisé pour baliser ces événements.

>[!NOTE]
>
>Pour que vos événements personnalisés soient pris en compte dans la [limitation](../items.md#capping), vous devez connecter l’événement d’expérience aux points d’entrée Adobe Experience Platform en l’envoyant à l’un de ces deux points d’entrée de collecte de données Edge :
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>Si vous utilisez le [SDK Web Adobe Experience Platform](https://experienceleague.adobe.com//docs/experience-platform/edge/home.html?lang=fr){target="_blank"} ou le [SDK mobile Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=fr){target="_blank"}, la connexion est établie automatiquement.
