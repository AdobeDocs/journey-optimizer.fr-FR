---
title: Configuration de notifications push
description: Découvrez comment configurer votre environnement pour envoyer des notifications push avec Journey Optimizer.
source-git-commit: 364861beb52e5663389a254ba145b31431b696ac
workflow-type: tm+mt
source-wordcount: '695'
ht-degree: 78%

---

# Configuration du canal Notification push {#push-notification-configuration}

![](assets/do-not-localize/badge.png)

Avant de commencer à envoyer des notifications push avec [!DNL Journey Optimizer], vous devez définir des paramètres dans [!DNL Adobe Experience Platform] et [!DNL Adobe Experience Platform Launch].

## Paramètres d’Adobe Experience Platform{#platform-settings}

Pour configurer votre application mobile dans [!DNL Adobe Experience Platform Launch], procédez comme suit :

1. [Accorder les droits de propriété et de société](#push-rights)
1. [Ajoutez les informations d’identification push de votre application mobile dans Platform Launch](#push-credentials-launch).
1. [Créez une configuration Edge](#edge-configuration) permettant à l’extension **[!UICONTROL Edge]** d’envoyer des données personnalisées d’un appareil mobile vers [!DNL Adobe Experience Platform].
1. [Configurez une propriété Platform Launch ](#launch-property).
1. [Publiez la propriété](#publish-property).
1. [Configurez la source ProfileDataSource](#configure-profiledatasource).

### Étape 1 : accordez les droits de propriété et de société {#push-rights}

Avant de créer une application mobile, vous devez d’abord vous assurer que vous possédez ou accordez les autorisations utilisateur appropriées.

Pour plus d’informations sur la gestion des utilisateurs avec [!DNL Adobe Experience Platform Launch], consultez la [documentation de Platform Launch](https://experienceleague.adobe.com/docs/launch/using/admin/user-permissions.html#experience-cloud-permissions).

Pour accorder les droits de propriété et de société :

1. Accédez à [!DNL Admin Console].

1. Dans l’onglet **[!UICONTROL Produits]**, sélectionnez la carte **[!UICONTROL Adobe Experience Platform Launch]**.

   ![](assets/push_product_1.png)

1. Sélectionnez un **[!UICONTROL Profil de produit]** existant ou créez-en un avec le bouton **[!UICONTROL Nouveau profil]**. Pour plus d’informations sur la création d’un **[!UICONTROL Nouveau profil]**, consultez la [documentation de la console Admin](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/create-profile.html#ui).

1. Dans l’onglet **[!UICONTROL Autorisations]**, sélectionnez **[!UICONTROL Droits de propriété]**.

   ![](assets/push_product_2.png)

1. Cliquez sur **[!UICONTROL Tout ajouter]**. Les droits suivants sont alors ajoutés à votre profil de produit :
   * **[!UICONTROL Approuver]**
   * **[!UICONTROL Développer]**
   * **[!UICONTROL Gérer les environnements]**
   * **[!UICONTROL Gérer les extensions]**
   * **[!UICONTROL Publier]**

   ![](assets/push_product_3.png)

1. Sélectionnez ensuite **[!UICONTROL Droits de Société]** dans le menu de gauche.

   ![](assets/push_product_4.png)

1. Ajoutez les droits suivants :

   * **[!UICONTROL Gérer les configurations d’application]**
   * **[!UICONTROL Gérer les propriétés]**

   ![](assets/push_product_5.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

Pour attribuer ce **[!UICONTROL Profil de produit]** à des utilisateurs :

1. Dans l’onglet **[!UICONTROL Produits]** de [!DNL Admin Console], sélectionnez la carte **[!UICONTROL Adobe Experience Platform Launch]**.

1. Sélectionnez votre **[!UICONTROL Profil de produit]** précédemment configuré.

1. Dans l’onglet **[!UICONTROL Utilisateurs]**, cliquez sur **[!UICONTROL Ajouter un utilisateur]**.

   ![](assets/push_product_6.png)

1. Saisissez le nom ou l’adresse email de votre utilisateur et sélectionnez l’utilisateur. Cliquez ensuite sur **[!UICONTROL Enregistrer]**.

   >[!NOTE]
   >
   >Si l’utilisateur n’a pas été créé auparavant dans Admin Console, consultez la [documentation relative à l’ajout d’utilisateurs](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/push_product_7.png)


Vous disposez désormais des autorisations utilisateur appropriées pour créer et configurer une application mobile dans [!DNL Adobe Experience Platform Launch].

### Étape 2 : ajoutez les informations d’identification push de votre application mobile dans Platform Launch {#push-credentials-launch}

Après avoir accordé les autorisations utilisateur appropriées, vous devez maintenant ajouter les informations d’identification push de votre application mobile dans [!DNL Adobe Experience Platform Launch].

Pour plus d’informations et de procédures sur l’ajout des informations d’identification push de votre application mobile, reportez-vous aux étapes détaillées dans la [documentation du SDK Mobile Adobe Experience Platform](https://aep-sdks.gitbook.io/docs/beta/adobe-journey-optimizer#configure-the-journey-optimizer-extension-in-launch).

<!--
Note that to add push credentials in [!DNL Adobe Experience Platform Launch], the owner of the mobile app should fetch them from APNs/FCM.
1. From [!DNL Adobe Experience Platform Launch], ensure that **[!UICONTROL Client Side]** is selected in the drop-down menu.

1. Select the **[!UICONTROL App Configurations]** tab in the left-hand panel and click **[!UICONTROL App Configuration]** to create a new configuration.

1. Enter a **[!UICONTROL Name]** for the configuration.

1. From the **[!UICONTROL Messaging Service Type]** drop-down menu, select the **[!UICONTROL Messaging service type]** to be used for these credentials. Here, we selected **[!UICONTROL Apple Push Notification Service]** since we are working with iOS.

1. Enter the mobile app **[!UICONTROL Bundle Id]** in the **[!UICONTROL App ID (iOS Bundle ID)]** field if you are using Apple push notification service or in the **[!UICONTROL App ID (Android package name)]** field if you are using Firebase Cloud Messaging.

    ![](assets/push_launch_app_configuration.png)

1. Drag and drop the .p8 key file or the .json private key file to the **[!UICONTROL Push Credentials]** field.

1. Enter the **[!UICONTROL Key Id]** and **[!UICONTROL Team Id]** if you are using Apple push notification service.

1. Click **[!UICONTROL Save]** to create your app configuration.
-->

### Étape 3 : créez une configuration Edge {#edge-configuration}

La **[!UICONTROL configuration Edge]** est utilisée par l’extension **[!UICONTROL Edge]** pour envoyer des données personnalisées d’un appareil mobile vers [!DNL Adobe Experience Platform].
Pour configurer [!DNL Adobe Experience Platform], vous devez fournir le nom du **[!UICONTROL Sandbox]** et le **[!UICONTROL Jeu de données d’événement]**.

Pour plus d’informations et de procédures sur la création de la **[!UICONTROL configuration Edge]**, reportez-vous aux étapes détaillées dans la [documentation du SDK Mobile Adobe Experience Platform](https://aep-sdks.gitbook.io/docs/getting-started/configure-datastreams).


<!--
1. From [!DNL Adobe Experience Platform Launch], select the **[!UICONTROL Edge Configurations]** tab and click **[!UICONTROL Edge Configurations]**.
    
1. Select **[!UICONTROL New Edge Configuration]** to add a new **[!UICONTROL Edge Configuration]**.
1. Enter a **[!UICONTROL Name]** and click **[!UICONTROL Save]**

1. Click the **[!UICONTROL Adobe Experience Platform]** toggle to enable it.

1. Fill in the **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** and **[!UICONTROL Profile Dataset]** fields. Then, click **[!UICONTROL Save]**.
    
    ![](assets/push-config-4.png)
-->

### Étape 4 : configurez une propriété Platform Launch {#launch-property}

Configurer une propriété [!DNL Adobe Experience Platform Launch] permet au développeur d’applications mobiles ou au spécialiste du marketing de configurer les attributs des SDK mobiles, tels que les temporisations de session, l’environnement Sandbox [!DNL Adobe Experience Platform] à cibler et les **[!UICONTROL Jeux de données Adobe Experience Platform]** à utiliser pour envoyer des données au SDK mobile.

Pour plus d’informations et de procédures sur la configuration d’une **[!UICONTROL propriété de Platform launch]**, reportez-vous aux étapes détaillées dans la [documentation du SDK Mobile Adobe Experience Platform](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#create-a-mobile-property).

Pour obtenir les SDK nécessaires au fonctionnement des notifications push, vous devez disposer des extensions SDK suivantes, pour Android et iOS :

* **[!UICONTROL Mobile Core]** (installée automatiquement)
* **[!UICONTROL Profil]** (installée automatiquement)
* **[!UICONTROL Adobe Experience Platform Edge]**
* **[!UICONTROL Adobe Experience Platform Assurance]**, facultative mais recommandée pour déboguer la mise en œuvre mobile.

Pour en savoir plus sur les extensions [!DNL Adobe Experience Platform Launch], consultez la [documentation de Platform Launch](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-mobile-android-apps-with-launch/configure-launch/launch-add-extensions.html).

<!--

1. From [!DNL Adobe Experience Platform Launch], ensure that **[!UICONTROL Client Side]** is selected in the drop-down menu.

1. select the **[!UICONTROL Properties]** tab and click **[!UICONTROL New Property]**.

    ![](assets/push-config-6.png)

1. Enter a **[!UICONTROL Name]** for your new property.

1. Select **[!UICONTROL Mobile]** as **[!UICONTROL Platform]**.

    ![](assets/push-config-7.png)

1. Click **[!UICONTROL Save]** to create your new property.

To configure **[!UICONTROL Adobe Experience Platform Edge Extension]** to send custom data from mobile devices to [!DNL Adobe Experience Platform].

1. Select your previously created property and select the **[!UICONTROL Extensions]** tab to view the extensions for this property.

    ![](assets/push-config-8.png)

1. Click **[!UICONTROL Configure]** under the **[!UICONTROL Adobe Experience Platform Edge]** Network' extension.

1. From the **[!UICONTROL Edge Configuration]** drop-down list, select the **[!UICONTROL Edge Configuration]** created in the previous steps. For more information on **[!UICONTROL Edge Configuration]**, refer to this [section](#edge-configuration).

1. Click **[!UICONTROL Save]**.

To configure **[!UICONTROL Adobe Experience Platform Messaging]** extension to send push profile and push interactions to the correct datasets, follow the same steps as above. Use **[!UICONTROL Sandbox]**, **[!UICONTROL Event dataset]** and **[!UICONTROL Profile Dataset]** created in the [Adobe Experience Platform setup](#edge-configuration).
-->

### Étape 5 : publiez la propriété {#publish-property}

Vous devez maintenant publier la propriété pour intégrer votre configuration et l’utiliser dans l’application mobile.

Pour publier votre propriété, reportez-vous aux étapes détaillées dans la [documentation du SDK mobile d’Adobe Experience Platform](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#publish-the-configuration).

### Étape 6 : configurez la source ProfileDataSource {#configure-profiledatasource}

Pour configurer `ProfileDataSource`, utilisez l’URL `ProfileDCInletURL` de [!DNL Adobe Experience Platform] et ajoutez ce qui suit dans l’application mobile :

```
    MobileCore.updateConfiguration(
    mutableMapOf("messaging.dccs" to <ProfileDCSInletURL>)
```

<!--
## Test your mobile app with custom action {#mobile-app-test}

After configuring your mobile app in both Adobe Experience Platform and Adobe Launch, you can now test it before sending push notifications to your profiles. In this use case, we will create a journey to target our mobile app and set a custom action which will trigger the push notification.

You can use a test mobile app for this use case. For more on this, refer to this [page](https://wiki.corp.adobe.com/pages/viewpage.action?spaceKey=CJM&title=Details+of+setting+the+mobile+test+app) (internal use only).

For this journey to work, you need to create an XDM schema. For more information, refer to [XDM documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#schemas-and-data-ingestion).

1. In the left menu, click **[!UICONTROL Data]** then **[!UICONTROL Schemas]** under **[!UICONTROL Data management]** to create your XDM schema.

    ![](assets/test_push_1.png)

1. Click **[!UICONTROL Create schema]** then select **[!UICONTROL XDM Experience event]**.

    ![](assets/test_push_2.png)

1. In the right pane, enter the name of your schema and description. Enable this schema for **[!UICONTROL Profile]**.

1. In the left pane, click **[!UICONTROL Add]** under **[!UICONTROL Mixins]** and select  **[!UICONTROL Create a new Mixin]**. For more information on how to create mixin, refer to [XDM System documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/create-mixin.html?lang=en#api).

    ![](assets/test_push_3.png)

1. Enter a **[!UICONTROL Display Name]** and a **[!UICONTROL Description]**. Click **[!UICONTROL Add mixin]** when done.

    ![](assets/test_push_4.png)

1. In the **[!UICONTROL Field properties]** window, add a **[!UICONTROL Field name]**, **[!UICONTROL Display name]** and select **[!UICONTROL String]** as **[!UICONTROL Type]**.

    ![](assets/test_push_5.png)

1. Check **[!UICONTROL Required]** and click **[!UICONTROL Apply]**.

1. Click **[!UICONTROL Save]**. Your schema is now created and can be used in an **[!UICONTROL Event schema]**.

You then need to set up an **[!UICONTROL Event schema]** where you will set the custom action which you will need to enter in your mobile app to trigger your push notification.

1. From the left menu of the home page, click the **[!UICONTROL Admin]** icon, then click **[!UICONTROL Manage]** from the **[!UICONTROL Events]** card to create your new **[!UICONTROL Event schema]**.

1. Click **[!UICONTROL Add]**, the event configuration pane opens on the right side of the screen.

    ![](assets/test_push_6.png)

1. Enter the name of your event. You can also add a description.

1. In the **[!UICONTROL Event ID type]** field, select **[!UICONTROL Rule Based]**.

1. In the **[!UICONTROL Parameters]**, select your previously created XDM event.

    ![](assets/test_push_7.png)

1. Click **[!UICONTROL Edit]** in the **[!UICONTROL Event ID condition]** field.

1. Drag and your previously added mixin to define the condition that will be used by the system to identify the events that will trigger your journey.

    ![](assets/test_push_8.png)

1. Type in the syntax that you will need to use to trigger your push notification in your test app, in this example **order confirmation**.

    ![](assets/test_push_9.png)

1. Select **[!UICONTROL ECID]** as your **[!UICONTROL Namespace]**.

1. Click **[!UICONTROL Ok]** then **[!UICONTROL Save]**.

Your **[!UICONTROL Event schema]** is now created and can now be used in a journey.

1. In the left menu from [!DNL Journey Optimizer] homepage, click **[!UICONTROL Journeys]**.

1. Click **[!UICONTROL Create]** to create a new journey.

    ![](assets/test_push_10.png)

1. Edit the journey's properties in the configuration pane displayed on the right side. Learn more in this [section](building-journeys/journey-gs.md#change-properties).

1. Start by drag and dropping the **[!UICONTROL Event schema]** created in the previous steps from the **[!UICONTROL Events]** drop-down.

    ![](assets/test_push_11.png)

1. From the **[!UICONTROL Actions]** drop-down, drag and drop a **[!UICONTROL Message]** activity to your journey.

1. Select a previously created message. For more information on how to create push notifications, refer to this [page](create-message.md).

1. Drag and drop an **[!UICONTROL End]** activity to your journey.

1. Activate **[!UICONTROL Test]** to your journey to start testing your push notifications and click **[!UICONTROL Trigger an event]**.

    ![](assets/test_push_12.png)

1. Enter your ECID in the **[!UICONTROL Key]** field then your event that will trigger the push notification in our case **order confirmation**.

    ![](assets/test_push_13.png)

1. Click **[!UICONTROL Send]**.

Your event will be triggered and you will receive your push notification to your mobile app.

![](assets/test_push_14.png)
-->

### Étape 7 : Créer un paramètre prédéfini de message {#message-preset}

Une fois votre application mobile configurée dans [!DNL Adobe Experience Platform Launch], vous devez créer un paramètre prédéfini de message afin de pouvoir envoyer des notifications push depuis **[!DNL Journey Optimizer]**.

Découvrez comment créer et configurer un paramètre de message prédéfini dans [cette section](configuration/message-presets.md).