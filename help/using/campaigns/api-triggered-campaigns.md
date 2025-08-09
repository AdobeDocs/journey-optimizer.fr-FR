---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser des campagnes déclenchées par API
description: Découvrez comment déclencher des campagnes à l’aide des API Journey Optimizer.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campagnes, déclenchement par API, REST, optimizer, messages
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
source-git-commit: 3a44111345c1627610a6b026d7b19b281c4538d3
workflow-type: tm+mt
source-wordcount: '246'
ht-degree: 94%

---


# Utiliser des campagnes déclenchées par API {#trigger-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="Campagnes déclenchées par API"
>abstract="**Campagnes transactionnelles déclenchées par API**<br/> Déclencher des messages en temps réel à l’aide d’appels API <br/><br/>**Messages marketing**<br/> Contenu promotionnel (nécessite un opt-in, soumis aux règles métier)<br/><br/>**Messages transactionnels**<br/> Contenu lié au service (confirmation, alertes, non soumis à un consentement marketing)<br/><br/>**Canaux disponibles**<br/> E-mail, SMS, notifications push"

## À propos des campagnes déclenchées par API {#about}

Les campagnes déclenchées par API permettent aux communications marketing d’atteindre une audience au moment opportun ou aux messages transactionnels/opérationnels (comme la réinitialisation d’un mot de passe) d’être envoyés à un individu. Elles sont utilisées quand une personnalisation de ces campagnes est nécessaire en utilisant non seulement l’attribut de profil, mais aussi les données contextuelles en temps réel du déclencheur, qui est une payload d’API REST.

Pour ce faire, vous devez d’abord créer une campagne déclenchée par API dans Journey Optimizer, puis lancer son exécution via un appel API à l’aide de l’[API REST Interactive Message Execution](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).

Les canaux disponibles pour les campagnes déclenchées par API sont E-mail, SMS et les messages push.

➡️ [Découvrez cette fonctionnalité en vidéo.](#video)

## Étapes clés de création de campagnes déclenchées par API {#steps}

1. [Définir les propriétés de la campagne](api-triggered-campaign-properties.md)
1. [Configurer l’action de campagne](api-triggered-campaign-action.md)
1. [Modifier le contenu de la campagne](api-triggered-campaign-content.md)
1. [Définir l’audience de la campagne](api-triggered-campaign-audience.md)
1. [Planifier la campagne](api-triggered-campaign-schedule.md)
1. [Vérifier et activer la campagne](review-activate-api-triggered-campaign.md)
1. [Déclencher l’exécution de la campagne](trigger-campaigns.md)

>[!IMPORTANT]
>
>Avant de créer votre campagne, vérifiez que vous avez consulté les conditions préalables générales de la campagne [campaign)](../campaigns/get-started-with-campaigns.md#prerequisites).

## Vidéos pratiques {#video}

Découvrez comment créer une campagne et la déclencher à partir d’un système externe en fonction des interactions des utilisateurs et utilisatrices, à l’aide de l’API REST Interactive Message Execution.

>[!VIDEO](https://video.tv.adobe.com/v/3452727?quality=12&captions=fre_fr)
