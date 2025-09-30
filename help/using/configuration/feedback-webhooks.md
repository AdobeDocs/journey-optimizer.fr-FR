---
solution: Journey Optimizer
product: journey optimizer
title: Créer des webhooks de commentaires pour les campagnes déclenchées par API dans Journey Optimizer
description: Découvrez comment créer des webhooks de commentaires pour les campagnes déclenchées par l’API dans Journey Optimizer.
feature: Channel Configuration
topic: Administration
role: Admin
level: Experienced
source-git-commit: be07b0dfec31d23f741bfc2a9f89fe1a7891ef0b
workflow-type: tm+mt
source-wordcount: '301'
ht-degree: 1%

---


# Créer des webhooks de commentaires pour les campagnes déclenchées par API {#webhooks}

Les webhooks de retour d’informations vous permettent de recevoir des mises à jour de statut en temps réel pour les messages envoyés via des campagnes déclenchées par API transactionnelle. En configurant un webhook, vous pouvez recevoir automatiquement les résultats des diffusions directement dans vos systèmes, ce qui permet la surveillance, la journalisation et le traitement automatisé.

Vous pouvez gérer les configurations webhook à partir du menu **[!UICONTROL Administration]** / **[!UICONTROL Canaux]** / **[!UICONTROL Paramètres webhook des commentaires]**.

![](assets/webhook-list.png)

>[!NOTE]
>Une seule configuration webhook par combinaison **Organisation + sandbox** est autorisée.

## Créer un webhook de commentaires

Pour créer un webhook, procédez comme suit :

1. Accédez à **[!UICONTROL Administration]** / **[!UICONTROL Canaux]** / **[!UICONTROL Paramètres du webhook Commentaires]**.

1. Cliquez sur **Créer un Webhook pour les commentaires**.

1. Dans la section **[!UICONTROL Configuration de base]**, fournissez les détails suivants :

   ![](assets/webhook-config.png)

   * **Nom du webhook** - Saisissez un nom explicite pour identifier le webhook.
   * **Canaux** - Sélectionnez le ou les canaux pour lesquels ce webhook doit recevoir des commentaires (e-mail et/ou SMS).
   * **URL Webhook** - Indiquez le point d’entrée HTTPS où les événements de commentaires doivent être diffusés.

1. Dans la section **[!UICONTROL Authentification]**, sélectionnez la méthode d’authentification :

   ![](assets/webhook-authentication.png)

   * **Pas d’authentification** - Aucun en-tête d’authentification n’est ajouté.
   * **Authentification JWT** - Fournissez les détails requis si votre point d’entrée nécessite une authentification JWT.

1. Dans la section **[!UICONTROL Paramètres d’en-tête]** , configurez des en-têtes personnalisés supplémentaires à envoyer avec chaque requête webhook.

   ![](assets/webhook-header.png)

1. Cliquez sur **[!UICONTROL Envoyer]** pour enregistrer la configuration.

>[!NOTE]
>
>Vous pouvez modifier un webhook à tout moment. Pour ce faire, ouvrez-le dans l’inventaire, puis cliquez sur le bouton **[!UICONTROL Modifier]**.

## Structure de la payload du Webhook

Après l’exécution d’un message, **[!DNL Journey Optimizer]** envoie la payload suivante au point d’entrée configuré.

```
{
  "requestId": "8NoByJneShCdCGRnrGS1t1m3CdA73dhR",
  "imsOrg": "myImsOrg",
  "sandbox": {
    "id": "068abf40-575e-11ea-8512-9b1bfdb82603",
    "name": "prod"
  },
  "channel": "email",
  "eventType": "message.feedback",
  "messageExecution": {
    "messageExecutionID": "HUMA-26362805",
    "messageType": "transactional",
    "campaignID": "16f24a15-7e21-477c-848a-d5695ca7f137",
    "campaignVersionID": "2ca10c10-56dd-4505-87cd-fa5da84e7a5d"
  },
  "messageDeliveryFeedback": {
    "feedbackStatus": {
      "value": "bounce"
    },
    "offers": null,
    "messageExclusion": null,
    "messageFailure": {
      "category": "sync",
      "type": "Ignored",
      "code": "25",
      "reason": "Admin Failure"
    },
    "retryCount": 0
  },
  "identityMap": {
    "email": [
      {
        "id": "john.doe@luma.com",
        "primary": true
      }
    ]
  }
}
```

Le webhook peut capturer les événements suivants :

* Envoyés
* Diffusés
* Rebond (voir l’exemple ci-dessus)
* Erreurs

Chaque requête entrante inclut également un requestId unique renvoyé au webhook.

## Étapes suivantes {#next}

Une fois qu’un webhook de commentaires a été créé, vous pouvez l’activer lors de la configuration d’une audience de campagne **déclenchée par l’API transactionnelle**. En savoir plus dans cette section : [Activer les Webhooks](../campaigns/api-triggered-campaign-audience.md#webhook)
