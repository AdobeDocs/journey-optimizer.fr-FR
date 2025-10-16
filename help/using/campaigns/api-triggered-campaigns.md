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
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 79%

---


# Utiliser des campagnes déclenchées par API {#trigger-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="Campagnes déclenchées par API"
>abstract="**Campagnes transactionnelles déclenchées par API**<br/> Déclencher des messages en temps réel à l’aide d’appels API <br/><br/>**Messages marketing**<br/> Contenu promotionnel (nécessite un opt-in, soumis aux règles métier)<br/><br/>**Messages transactionnels**<br/> Contenu lié au service (confirmation, alertes, non soumis à un consentement marketing)<br/><br/>**Canaux disponibles**<br/> E-mail, SMS, notifications push"

## À propos des campagnes déclenchées par API {#about}

Les campagnes déclenchées par API permettent aux communications marketing d’atteindre une audience au bon moment ou aux messages transactionnels/opérationnels d’être envoyés à une personne, comme la réinitialisation d’un mot de passe. La personnalisation de ces campagnes inclut les attributs de profil, mais aussi les données contextuelles en temps réel dans le déclencheur, qui est une payload de l’API REST.

Pour ce faire, vous devez d’abord créer une campagne déclenchée par API dans Journey Optimizer, puis lancer son exécution via un appel API à l’aide de l’[API REST Interactive Message Execution](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).

Les canaux disponibles pour les campagnes déclenchées par API sont E-mail, SMS et les messages push.

➡️ [Découvrez cette fonctionnalité en vidéo.](#video)


>[!NOTE]
>
>Les canaux pris en charge sont les suivants : [E-mail](../email/get-started-email.md), [SMS/MMS/RCS](../sms/get-started-sms.md), [Notifications push](../push/get-started-push.md).
>
>Les canaux disponibles varient en fonction de votre modèle d’attribution de licence et de vos modules complémentaires.

## Étapes clés de création de campagnes déclenchées par API {#steps}

Avant de commencer une campagne, vérifiez les conditions préalables suivantes répertoriées [dans cette section](get-started-with-campaigns.md#permissions). Une fois ces conditions préalables remplies, vous pouvez commencer à créer votre campagne :

1. [Définir les propriétés de la campagne](api-triggered-campaign-properties.md)
1. [Configurer l’action de campagne](api-triggered-campaign-action.md)
1. [Modifier le contenu de la campagne](api-triggered-campaign-content.md)
1. [Définir l’audience de la campagne](api-triggered-campaign-audience.md)
1. [Planifier la campagne](api-triggered-campaign-schedule.md)
1. [Vérifier et activer la campagne](review-activate-api-triggered-campaign.md)
1. [Déclencher l’exécution de la campagne](trigger-campaigns.md)

## Vidéos pratiques {#video}

Découvrez comment créer une campagne et la déclencher à partir d’un système externe en fonction des interactions des utilisateurs et utilisatrices, à l’aide de l’API REST Interactive Message Execution.

>[!VIDEO](https://video.tv.adobe.com/v/3425358?quality=12)
