---
title: Configuration in-app
description: Découvrez comment configurer votre environnement pour envoyer des messages in-app avec Journey Optimizer
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '277'
ht-degree: 100%

---

# Configurer le canal in-app {#inapp-configuration}

Avant d’envoyer des messages in-app, vous devez configurer votre canal in-app dans [!DNL Adobe Experience Platform Data Collection].

1. À partir de votre compte [!DNL Adobe Experience Platform Data Collection], accédez au menu **[!UICONTROL Train de données]** et cliquez sur **[!UICONTROL Nouveau flux de données]**. Pour en savoir plus sur la création de train de données, consultez [cette page](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams).

1. Sélectionnez le service [!DNL Adobe Experience Platform].

   [!DNL Edge Segmentation], [!DNL Offer Decisioning] et [!DNL Adobe Journey Optimizer] doivent être sélectionnés.

   ![](assets/inapp_config_6.png)

1. Ensuite, accédez au menu **[!UICONTROL Surfaces d’application]**, puis cliquez sur **[!UICONTROL Créer la surface d’application]**.

   ![](assets/inapp_config_1.png)

1. Ajoutez un nom à votre **[!UICONTROL Surface d’application]**.

1. Dans le menu déroulant Apple iOS, saisissez votre **ID de bundle iOS**. Voir la [Documentation Apple](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) pour plus d’informations sur l’**ID de bundle**.

   ![](assets/inapp_config_2.png)

1. Dans le menu déroulant Android, saisissez votre **nom du package Android**. Voir la [Documentation Android](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) pour plus d’informations sur le **nom du package**.

1. Cliquez sur **[!UICONTROL Enregistrer]** lorsque vous avez terminé la configuration de votre **[!UICONTROL Surface d’application]**.

   ![](assets/inapp_config_3.png)

   Votre **[!UICONTROL Surface d’application]** sera désormais disponible lors de la création d’une nouvelle campagne avec un message in-app. [En savoir plus](create-in-app.md)

1. Après avoir créé votre surface d’application, vous devez maintenant créer une propriété mobile.

   Voir [cette page](https://experienceleague.adobe.com/docs/experience-platform/tags/admin/companies-and-properties.html?lang=fr) pour la procédure détaillée.

   ![](assets/inapp_config_4.png)

1. Dans le menu Extensions de la propriété que vous venez de créer, installez les extensions suivantes :

   * Adobe Experience Platform Edge Network
   * Adobe Journey Optimizer
   * Assurance AEP
   * Consentement
   * Identifier
   * Mobile Core
   * Profile

   Voir [cette page](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=fr#add-a-new-extension) pour la procédure détaillée.

   ![](assets/inapp_config_5.png)

Le canal in-app est maintenant configuré. Vous pouvez commencer à envoyer des messages in-app à vos utilisateurs.

**Rubriques connexes :**

* [Créer un message in-app](create-in-app.md)
* [Créer une campagne](../campaigns/create-campaign.md)
* [Concevoir un message in-app](design-in-app.md)
* [Rapport in-app](inapp-report.md)
