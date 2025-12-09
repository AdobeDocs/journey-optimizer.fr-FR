---
solution: Journey Optimizer
product: journey optimizer
title: Créer un message d’activité en direct
description: Découvrez comment créer une activité en direct dans Journey Optimizer.
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: bfd36dddb5795cd8b6eeb164f70b6cf3fdcb5750
workflow-type: ht
source-wordcount: '317'
ht-degree: 100%

---

# Créer une activité en direct {#create-mobile-live}

>[!BEGINSHADEBOX]

* [Commencer avec les activités en direct](get-started-mobile-live.md)
* [Configuration des activités en direct](mobile-live-configuration.md)
* [Intégration des activités en direct au SDK mobile Adobe Experience Platform](mobile-live-configuration-sdk.md)
* **[Créer une activité en direct](create-mobile-live.md)**
* [Questions fréquentes](mobile-live-faq.md)
* [Rapport de campagne d’activités en direct](../reports/campaign-global-report-cja-activity.md)

>[!ENDSHADEBOX]

Après avoir effectué la configuration mobile et implémenté le SDK mobile Adobe Experience Platform, vous pouvez créer une activité en direct dans Journey Optimizer :

1. Accédez au menu **[!UICONTROL Campagnes]**, puis cliquez sur **[!UICONTROL Créer une campagne]**.

1. Sélectionnez le type de campagne **Déclenchée par API**.

   * Sélectionnez **Marketing déclenché par API** pour les campagnes basées sur les audiences.

   * Sélectionnez **Transactionnelle déclenchée par API** pour les campagnes individuelles.

   >[!IMPORTANT]
   >
   > Notez que pour **Transactionnelle déclenchée par API**, l’option **[!UICONTROL Débit élevé]** ne doit pas être activée.

   ![](assets/create-live-1.png)

1. Dans la section **[!UICONTROL Propriétés]**, modifiez le **[!UICONTROL Titre]** et la **[!UICONTROL Description]** de votre campagne.

1. Dans la section **[!UICONTROL Actions]**, sélectionnez **[!UICONTROL Activité en direct]** et sélectionnez ou créez une nouvelle configuration.

   Pour en savoir plus sur la configuration des activités en direct, consultez [cette page](mobile-live-configuration.md).

   ![](assets/create-live-2.png)

1. Cliquez sur **[!UICONTROL Créer une expérience]** pour commencer à configurer votre expérience de contenu et créer des traitements afin de mesurer leurs performances et d’identifier la meilleure option pour votre audience cible. [En savoir plus](../content-management/content-experiment.md).

1. Dans l’onglet **[!UICONTROL Audience]**, choisissez le **[!UICONTROL Type d’identité]** [En savoir plus](../audience/about-audiences.md).

1. Les campagnes sont conçues pour être exécutées à une date spécifique ou à une fréquence récurrente. Découvrez comment configurer le **[!UICONTROL Planning]** de votre campagne dans [cette section](../campaigns/create-campaign.md#schedule).

1. Une fois la configuration effectuée, cliquez sur **[!UICONTROL Réviser pour activer]**, puis sur **[!UICONTROL Activer]**.

1. Une fois la campagne activée, utilisez la **requête cURL** fournie comme modèle pour déclencher les événements de démarrage, de mise à jour ou d’arrêt de l’activité en direct. Modifiez l’exemple de payload en incluant vos données avant l’exécution.

   Veillez également à copier les identifiants **[!UICONTROL ID de campagne]** à inclure dans votre payload.

   ➡️ Les exigences d’authentification, y compris les jetons OAuth et les clés d’API, sont disponibles dans la [documentation sur les campagnes déclenchées par API](https://developer.adobe.com/journey-optimizer-apis/references/messaging/).

   ![](assets/create-live-3.png)

   +++ Exemple de payload individuelle

   Notez que la plupart des champs de l’exemple de payload suivant sont obligatoires, seuls `requestId`, `dismissal-date` et `alert` sont facultatifs.

   ```json
   {
       "requestId": "your-request-id",
       "campaignId": "your-campaign-id",
       "recipients": [
   {
       "type": "aep",
       "userId": "testemail@gmail.com",
       "namespace": "email",
       "context": {
        "requestPayload": {
       "aps": {
       "content-available": 1,
       "timestamp": 1756984054,              // current epoch time
       "dismissal-date": 1756984084,         // optional – auto remove when event="end"
       "event": "update",                    // start | update | end
   
       // Fields from FoodDeliveryLiveActivityAttributes
       "content-state": {
         "orderStatus": "Delivered"
       },
   
       "attributes-type": "FoodDeliveryLiveActivityAttributes",
       "attributes": {
         "restaurantName": "Pizza",
         "liveActivityData": {
           "liveActivityID": "orderId1"       // customer reference ID
         }
       },
   
       "alert": {
         "title": "Order Delivered!",
         "body": "Your pizza has arrived."
       }
     }
   }
   }
   }
   ]
   }
   ```

   +++

Après avoir créé votre activité en direct, vous pouvez suivre son impact à l’aide des [rapports intégrés](../reports/campaign-global-report-cja-activity.md).
