---
title: Configuration In-App
description: Découvrez comment configurer votre environnement pour envoyer des messages In-App avec Journey Optimizer
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: e7431d1b69e460471b01439c9bd2577fd69944ed
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 7%

---

# Configuration du canal In-App {#inapp-configuration}

Avant d’envoyer des messages In-App, vous devez configurer votre canal in-app dans [!DNL Adobe Experience Platform Data Collection].

1. À partir de [!DNL Adobe Experience Platform Data Collection] , accédez au **[!UICONTROL Datastream]** et cliquez sur **[!UICONTROL Nouveau flux de données]**. Pour plus d’informations sur la création de flux de données, reportez-vous à la section [cette page](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams).

1. Sélectionnez la [!DNL Adobe Experience Platform] service.

   [!DNL Edge Segmentation], [!DNL Offer Decisioning] et [!DNL Adobe Journey Optimizer] doit être sélectionné.

   ![](assets/inapp_config_6.png)

1. Ensuite, accédez à la **[!UICONTROL Surfaces de l’application]** , puis cliquez sur **[!UICONTROL Créer la surface de l’application]**.

   ![](assets/inapp_config_1.png)

1. Ajoutez un nom à votre **[!UICONTROL Surface de l’application]**.

1. Dans la liste déroulante Apple iOS, saisissez votre **Identifiant du lot iOS**. Voir [Documentation Apple](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) pour plus d’informations sur **Bundle ID**.

   ![](assets/inapp_config_2.png)

1. Dans la liste déroulante Android, saisissez votre **Nom du package Android**. Voir [Documentation Android](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) pour plus d’informations sur **Nom du module**.

1. Cliquez sur **[!UICONTROL Enregistrer]** lorsque vous avez terminé la configuration de votre **[!UICONTROL Surface de l’application]**.

   ![](assets/inapp_config_3.png)

   Votre **[!UICONTROL Surface de l’application]** sera désormais disponible lors de la création d’une campagne avec un message in-app. [En savoir plus](create-in-app.md)

1. Après avoir créé la surface de votre application, vous devez maintenant créer une propriété mobile.

   Voir [cette page](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html#for-mobile) pour la procédure détaillée.

   ![](assets/inapp_config_4.png)

1. Dans le menu Extensions de la propriété que vous venez de créer, installez les extensions suivantes :

   * Adobe Experience Platform Edge Network
   * Adobe Journey Optimizer
   * Assurance AEP
   * Consentement
   * Identifier
   * Mobile Core
   * Profile

   Voir [cette page](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=en#add-a-new-extension) pour la procédure détaillée.

   ![](assets/inapp_config_5.png)

Le canal In-App est maintenant configuré. Vous pouvez commencer à envoyer des messages In-App à vos utilisateurs.

**Rubriques connexes :**

* [Création d’un message in-app](create-in-app.md)
* [Créer une campagne](../campaigns/create-campaign.md)
* [Concevoir un message in-app](design-in-app.md)
* [Rapport in-app](inapp-report.md)
