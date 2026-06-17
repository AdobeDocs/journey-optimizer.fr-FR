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
TQID: https://experienceleague.adobe.com/DNNZWQjgdcranVpuJV9WCKW8RRENVJ6iZnIt1k-Easc
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a653cc2e-bc85-4353-a306-399e5b247978
subfeature_v2: id: f7479fa1-474b-479d-8c98-f6cee5865a38id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: ae7ea7c6b3f111dca040173221eec5210c41bef8
workflow-type: tm+mt
source-wordcount: 322
ht-degree: 88%

---

# Utiliser des campagnes déclenchées par API {#trigger-campaigns}

>[!BEGINSHADEBOX]

**Sur cette page :** créez et lancez des campagnes déclenchées par l’API via un appel d’API REST afin d’envoyer des messages marketing et transactionnels en temps réel à l’aide de données de profil et contextuelles.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="campaigns_overview_api_triggered"
>title="Campagnes déclenchées par API"
>abstract="**Campagnes transactionnelles déclenchées par API**<br/> Déclencher des messages en temps réel à l’aide d’appels API <br/><br/>**Messages marketing**<br/> Contenu promotionnel (nécessite un opt-in, soumis aux règles métier)<br/><br/>**Messages transactionnels**<br/> Contenu lié au service (confirmation, alertes, non soumis à un consentement marketing)<br/><br/>**Canaux disponibles**<br/> E-mail, SMS, notifications push"

## À propos des campagnes déclenchées par API {#about}

Les campagnes déclenchées par API permettent aux communications marketing d’atteindre une audience au moment opportun ou aux messages transactionnels/opérationnels (comme la réinitialisation d’un mot de passe) d’être envoyés à un individu. Elles sont utilisées quand une personnalisation est nécessaire en utilisant non seulement l’attribut de profil, mais aussi les données contextuelles en temps réel du déclencheur, qui est une payload d’API REST.

Pour ce faire, vous devez d’abord créer une campagne déclenchée par API dans Journey Optimizer, puis lancer son exécution via un appel API à l’aide de l’[API REST Interactive Message Execution](https://developer.adobe.com/journey-optimizer-apis/references/messaging#tag/execution).

➡️ [Découvrez cette fonctionnalité en vidéo.](#video)

>[!NOTE]
>
>Pour plus d’informations sur les canaux pris en charge, reportez-vous au tableau de cette section : [Canaux dans les parcours et les campagnes](../channels/gs-channels.md#channels).
>
>Les canaux disponibles varient en fonction de votre modèle d’attribution de licence et de vos modules complémentaires.

## Étapes clés de création de campagnes déclenchées par API {#steps}

Avant de commencer une campagne, vérifiez les conditions préalables suivantes répertoriées [dans cette section](get-started-with-campaigns.md#prerequisites). Une fois ces conditions préalables remplies, vous pouvez commencer à créer votre campagne :

1. [Définir les propriétés de la campagne](api-triggered-campaign-properties.md)
1. [Configurer l’action de campagne](api-triggered-campaign-action.md)
1. [Modifier le contenu de la campagne](api-triggered-campaign-content.md)
1. [Définir l’audience de la campagne](api-triggered-campaign-audience.md)
1. [Planifier la campagne](api-triggered-campaign-schedule.md)
1. [Vérifier et activer la campagne](review-activate-api-triggered-campaign.md)
1. [Déclencher l’exécution de la campagne](trigger-campaigns.md)

En savoir plus sur le [workflow complet pour la création d’une campagne avec des guides spécifiques →](get-started-with-campaigns.md#workflow)

## Vidéos pratiques {#video}

Découvrez comment créer une campagne et la déclencher à partir d’un système externe en fonction des interactions des utilisateurs et utilisatrices, à l’aide de l’API REST Interactive Message Execution.

>[!VIDEO](https://video.tv.adobe.com/v/3425358?quality=12)
