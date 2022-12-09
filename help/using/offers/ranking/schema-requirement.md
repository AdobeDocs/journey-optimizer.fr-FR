---
product: experience platform
solution: Experience Platform
title: Configuration de la capture d’événements
description: Découvrez comment configurer votre schéma d’offre pour capturer des événements
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: f70ba749-f517-4e09-a381-243b21713b48
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# Configuration de la capture d’événements {#schema-requirements}

À ce stade, vous devez disposer des éléments suivants :

* a créé le modèle d’IA,
* a défini le type d&#39;événement que vous souhaitez capturer : offre affichée (impression) et/ou offre sur laquelle l&#39;utilisateur a cliqué (conversion),
* et dans quel jeu de données vous souhaitez collecter les données d’événement.

Désormais, chaque fois qu’une offre est affichée et/ou que vous cliquez dessus, vous souhaitez que l’événement correspondant soit automatiquement capturé par la variable **[!UICONTROL Experience Event - Proposition Interactions]** groupe de champs à l’aide de [SDK Web d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html#what-is-adobe-experience-platform-web-sdk%3F){target=&quot;_blank&quot;} ou SDK Mobile.

Pour pouvoir envoyer des types d’événement (offre affichée ou offre sur laquelle l’utilisateur a cliqué), vous devez définir la valeur correcte de chaque type d’événement dans un événement d’expérience envoyé dans Adobe Experience Platform. Vous trouverez ci-dessous les exigences de schéma à implémenter dans votre code JavaScript :

## Scénario d&#39;offre affichée

**Type d’événement :** `decisioning.propositionDisplay`
**Source :** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) ou par ingestion par lots
+++**Exemple de payload :**

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

### Scénario sur l’offre cliquée

**Type d’événement :** `decisioning.propositionInteract`
**Source :** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) ou par ingestion par lots
+++**Exemple de payload :**

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
