---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Configurer la capture d’événements
description: Découvrez comment configurer votre schéma d’offre pour capturer les événements.
badge: label="Hérité" type="Informative"
feature: Ranking, Datasets, Decision Management
role: Developer
level: Experienced
exl-id: f70ba749-f517-4e09-a381-243b21713b48
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '290'
ht-degree: 100%

---

# Configurer la collecte de données {#schema-requirements}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../../experience-decisioning/gs-experience-decisioning.md)

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
>Pour que vos événements personnalisés soient pris en compte dans le [capping de la fréquence](../offer-library/add-constraints.md#capping), vous devez connecter l’événement d’expérience aux points d’entrée Adobe Experience Platform en l’envoyant à l’un de ces deux points d’entrée de collecte de données Edge :
>
>* POST /ee/v2/interact
>* POST /ee/v2/collect
>
>Si vous utilisez le [SDK Web Adobe Experience Platform](https://experienceleague.adobe.com//docs/experience-platform/edge/home.html?lang=fr){target="_blank"} ou le [SDK mobile Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/data-collection/mobile-sdk/overview.html?lang=fr){target="_blank"}, la connexion est établie automatiquement.
