---
source-git-commit: 4aebdb06094628cfe7393c7f7b41e5fe0ee9df13
workflow-type: tm+mt
source-wordcount: '614'
ht-degree: 43%

---
Les autorisations de l&#39;outil wiki n&#39;ont pas été accordées. Je vais continuer en utilisant les informations détaillées du ticket lui-même, qui contient les spécifications clés (500 TPS par défaut, 1000/1500 TPS niveaux via le module complémentaire de performance, push uniquement, prend en charge les augmentations en rafale/de durée limitée).

&#x200B;---

solution : Journey Optimizer
produit : parcours optimizer
titre : Utiliser des campagnes déclenchées par API
description : découvrez comment déclencher des campagnes à l’aide des API Journey Optimizer.
fonctionnalité : campagnes, API
rubrique : Gestion de contenu
Rôle : développeur
niveau : Expérimenté
mots-clés : campagnes, déclenchées par API, REST, optimizer, messages
exl-id : 0ef03d33-da11-43fa-8e10-8e4b80c90acb
TQID : https://experienceleague.adobe.com/DNNZWQjgdcranVpuJV9WCKW8RRENVJ6iZnIt1k-Easc
product_v2 :
- id : cb954087-f4fc-4456-afb9-e939cabcdc79
internal-label : Journey Optimizer
feature_v2 :
- id : a653cc2e-bc85-4353-a306-399e5b247978
libellé interne : campagnes Journey Optimizer
subfeature_v2 :
- id : f7479fa1-474b-479d-8c98-f6cee5865a38
internal-label : campagnes déclenchées par API
- id : ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
internal-label : Gestion de campagne
role_v2 :
- id : ff6a42d2-313e-452e-93a6-792e4fad9ff8
internal-label : développeur
topic_v2 :
- id : e0eb8757-182f-49f3-94a4-1587d16f5094
internal-label : Personalization

Voici l’intégralité du fichier Markdown mis à jour :

&#x200B;---

```
solution: Journey Optimizer
product: journey optimizer
title: Work with API triggered campaigns
description: Learn how to trigger campaigns using Journey Optimizer APIs.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campaigns, API-triggered, REST, optimizer, messages
exl-id: 0ef03d33-da11-43fa-8e10-8e4b80c90acb
TQID: https://experienceleague.adobe.com/DNNZWQjgdcranVpuJV9WCKW8RRENVJ6iZnIt1k-Easc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
    internal-label: Journey Optimizer
feature_v2:
  - id: a653cc2e-bc85-4353-a306-399e5b247978
    internal-label: Journey Optimizer campaigns
subfeature_v2:
  - id: f7479fa1-474b-479d-8c98-f6cee5865a38
    internal-label: API triggered campaigns
  - id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
    internal-label: Campaign management
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
    internal-label: Developer
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
    internal-label: Personalization
```

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

## Débit des notifications push {#push-throughput}

Par défaut, les campagnes déclenchées par API prennent en charge jusqu’à 500 transactions **par seconde (TPS)** pour la diffusion par notification push. Les entreprises ayant des besoins opérationnels de messagerie à volume élevé peuvent augmenter cette limite par le biais du **module complémentaire de performances**.

Le module complémentaire Performances offre deux niveaux de débit supérieurs pour les notifications push :

| Niveau | Débit |
|------|-----------|
| Standard | 500 TPS (inclus pour tous les clients) |
| Module complémentaire Performances — Niveau 1 | 1 000 TPS |
| Module complémentaire Performances — Niveau 2 | 1 500 TPS |

Un débit plus élevé est disponible sous la forme d’une augmentation contractuelle permanente et pour une **durée limitée** afin de prendre en charge les scénarios temporaires de volume élevé, tels que les lancements de produits ou les campagnes à grande échelle.

>[!NOTE]
>
>Les niveaux de débit augmentés s’appliquent uniquement au canal **notification push** pour les campagnes déclenchées par l’API. Les canaux e-mail et SMS ne sont pas concernés par ce module complémentaire.
>
>Contactez votre équipe de compte Adobe pour activer un niveau de débit supérieur pour votre organisation.

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

>[!VIDEO](https://video.tv.adobe.com/v/3452727?captions=fre_fr&quality=12)

&#x200B;---

L’ajout clé est la nouvelle section **Débit des notifications push** (`## Push notification throughput {#push-throughput}`) placée entre « À propos » et « Étapes clés », qui documente :
- La valeur par défaut de 500 TPS incluse pour tous les clients
- Les deux niveaux du module complémentaire de performance (1 000 et 1 500 TPS)
- Prise en charge des augmentations permanentes et de durée limitée
- Portée limitée au canal push uniquement
- Une note redirigeant les clients vers leur équipe de compte Adobe