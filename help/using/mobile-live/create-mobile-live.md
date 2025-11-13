---
solution: Journey Optimizer
product: journey optimizer
title: Créer un message d’activité dynamique
description: Découvrez comment créer une activité Live dans Journey Optimizer
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
source-git-commit: bfd36dddb5795cd8b6eeb164f70b6cf3fdcb5750
workflow-type: tm+mt
source-wordcount: '317'
ht-degree: 23%

---

# Créer une activité Live {#create-mobile-live}

>[!BEGINSHADEBOX]

* [Prise en main de l’activité Live](get-started-mobile-live.md)
* [Configuration de l’activité en direct](mobile-live-configuration.md)
* [Intégration d’une activité en direct à Adobe Experience Platform Mobile SDK](mobile-live-configuration-sdk.md)
* **[Créer une activité dynamique](create-mobile-live.md)**
* [Questions fréquentes](mobile-live-faq.md)
* [Rapport de campagne d’activité dynamique](../reports/campaign-global-report-cja-activity.md)

>[!ENDSHADEBOX]

Après avoir configuré votre configuration mobile et implémenté votre SDK mobile Adobe Experience Platform, vous pouvez commencer à créer votre activité en direct dans Journey Optimizer :

1. Accédez au menu **[!UICONTROL Campagnes]**, puis cliquez sur **[!UICONTROL Créer une campagne]**.

1. Sélectionnez le type de campagne **déclenché par l’API**.

   * Sélectionnez **Marketing déclenché par API** pour les campagnes basées sur une audience

   * Sélectionnez **Transactionnel déclenché par API** pour des campagnes individuelles.

   >[!IMPORTANT]
   >
   > Notez que pour **Transactionnel déclenché par l’API**, l’option **[!UICONTROL Débit élevé]** ne doit pas être activée.

   ![](assets/create-live-1.png)

1. Dans la section **[!UICONTROL Propriétés]**, modifiez le **[!UICONTROL Titre]** et la **[!UICONTROL Description]** de votre campagne.

1. Dans la section **[!UICONTROL Actions]**, choisissez **[!UICONTROL Activité active]** et sélectionnez ou créez une configuration.

   En savoir plus sur la configuration de l’activité en direct sur [cette page](mobile-live-configuration.md).

   ![](assets/create-live-2.png)

1. Cliquez sur **[!UICONTROL Créer une expérience]** pour commencer à configurer votre expérience de contenu et créer des traitements afin de mesurer leurs performances et d’identifier la meilleure option pour votre audience cible. [En savoir plus](../content-management/content-experiment.md).

1. Dans l’onglet **[!UICONTROL Audience]**, choisissez votre **[!UICONTROL Type d’identité]** [En savoir plus](../audience/about-audiences.md).

1. Les campagnes sont conçues pour être exécutées à une date spécifique ou à une fréquence récurrente. Découvrez comment configurer le **[!UICONTROL Planning]** de votre campagne dans [cette section](../campaigns/create-campaign.md#schedule).

1. Une fois la configuration effectuée, cliquez sur **[!UICONTROL Vérifier pour activer]**, puis sur **[!UICONTROL Activer]**.

1. Une fois la campagne activée, utilisez la requête **cURL** fournie comme modèle pour déclencher les événements de début, de mise à jour ou de fin de l’activité dynamique. Mettez à jour l’exemple de payload avec vos données spécifiques avant l’exécution.

   Veillez également à copier les identifiants **[!UICONTROL Identifiant de campagne]** à inclure dans votre payload.

   ➡️ les exigences d’authentification, y compris les jetons OAuth et les clés d’API[&#x200B; dans la documentation sur les campagnes déclenchées par &#x200B;](https://developer.adobe.com/journey-optimizer-apis/references/messaging/)API .

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

Après avoir conçu votre activité dynamique, vous pouvez suivre la mesure de l’impact de votre activité dynamique à l’aide de [&#x200B; rapports intégrés &#x200B;](../reports/campaign-global-report-cja-activity.md).
