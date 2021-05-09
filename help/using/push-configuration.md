---
title: Configuration des notifications Push
description: Découvrez comment configurer votre environnement pour envoyer des notifications Push avec Journey Optimizer
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '902'
ht-degree: 0%

---

# Configuration de la notification Push {#push-notification-configuration}

![](assets/do-not-localize/badge.png)

## Commencer la configuration Push {#gs-push}

Avant de commencer à envoyer des notifications Push avec [!DNL Journey Optimizer], vous devez définir les paramètres dans [!DNL Adobe Experience Platform] et [!DNL Adobe Experience Platform Launch].

## Paramètres Adobe Experience Platform {#platform-settings}

Pour configurer votre application mobile dans [!DNL Adobe Experience Platform Launch], procédez comme suit :

1. [Attribuer des droits de propriété et de Société](#push-rights)
1. [Ajoutez les informations d’identification Push de votre application mobile dans Platform launch](#push-credentials-launch).
1. [Créez une ](#edge-configuration) configuration Edge à utiliser par  **** Edgeextension pour envoyer des données personnalisées depuis un périphérique mobile vers  [!DNL Adobe Experience Platform].
1. [Configurez une propriété](#launch-property) de Platform launch.
1. [Publiez la propriété](#publish-property).
1. [Configurez ProfileDataSource](#configure-profiledatasource).

### Étape 1 : Attribuer des droits de propriété et de Société {#push-rights}

Avant de créer une application mobile, vous devez d’abord vous assurer que vous disposez des autorisations d’utilisateur appropriées ou que vous les accordez.

Pour plus d&#39;informations sur la gestion des utilisateurs avec [!DNL Adobe Experience Platform Launch], consultez la [documentation du Platform launch](https://experienceleague.adobe.com/docs/launch/using/admin/user-permissions.html#experience-cloud-permissions).

Pour attribuer des droits de propriété et de Société :

1. Accédez à [!DNL Admin Console].

1. Dans l&#39;onglet **[!UICONTROL Produits]**, sélectionnez la carte **[!UICONTROL Adobe Experience Platform Launch]**.

   ![](assets/push_product_1.png)

1. Sélectionnez un **[!UICONTROL Profil de produits]** existant ou créez-en un nouveau avec le bouton **[!UICONTROL Nouveau profil]**. Pour plus d&#39;informations sur la création d&#39;un **[!UICONTROL nouveau profil]**, consultez la [documentation de la console d&#39;admin](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/create-profile.html#ui).

1. Dans l&#39;onglet **[!UICONTROL Permissions]**, sélectionnez **[!UICONTROL Droits de propriété]**.

   ![](assets/push_product_2.png)

1. Cliquez sur **[!UICONTROL Ajouter]**. Vous ajouterez ainsi les droits suivants à votre profil de produits :
   * **[!UICONTROL Approuver]**
   * **[!UICONTROL Développer]**
   * **[!UICONTROL Gérer les Environnements]**
   * **[!UICONTROL Gérer les extensions]**
   * **[!UICONTROL Publier]**

   ![](assets/push_product_3.png)

1. Sélectionnez ensuite **[!UICONTROL droits de Société]** dans le menu de gauche.

   ![](assets/push_product_4.png)

1. Ajoutez les droits suivants :

   * **[!UICONTROL Gérer les configurations d’application]**
   * **[!UICONTROL Gérer les propriétés]**

   ![](assets/push_product_5.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

Pour attribuer ce **[!UICONTROL profil de produit]** aux utilisateurs :

1. Dans l&#39;onglet [!DNL Admin Console] Produits **[!UICONTROL Produits]**, sélectionnez la carte **[!UICONTROL Adobe Experience Platform Launch]**.

1. Sélectionnez votre **[!UICONTROL profil de produits]** précédemment configuré.

1. Dans l&#39;onglet **[!UICONTROL Utilisateurs]**, cliquez sur **[!UICONTROL Ajouter l&#39;utilisateur]**.

   ![](assets/push_product_6.png)

1. Saisissez le nom ou l’adresse électronique de votre utilisateur et sélectionnez-le. Cliquez ensuite sur **[!UICONTROL Enregistrer]**.

   >[!NOTE]
   >
   >Si l’utilisateur n’a pas été créé auparavant dans la console d’administration, consultez la [documentation de l’utilisateur Ajouté](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/push_product_7.png)


Vous disposez désormais des autorisations utilisateur appropriées pour créer et configurer une application mobile dans [!DNL Adobe Experience Platform Launch].

### Étape 2 : Ajoutez vos informations d’identification Push d’application mobile dans le Platform launch {#push-credentials-launch}

>[!NOTE]
>
> Pour ajouter des informations d’identification Push dans [!DNL Adobe Experience Platform Launch], le propriétaire de l’application mobile doit les récupérer des APN/FCM.

1. Dans [!DNL Adobe Experience Platform Launch], vérifiez que **[!UICONTROL Client Side]** est sélectionné dans le menu déroulant.

1. Sélectionnez l’onglet **[!UICONTROL Configurations de l’application]** dans le panneau de gauche et cliquez sur **[!UICONTROL Configuration de l’application]** pour créer une nouvelle configuration.

1. Entrez un **[!UICONTROL nom]** pour la configuration.

1. Dans le menu déroulant **[!UICONTROL Type de service de messagerie]**, sélectionnez le **[!UICONTROL type de service de messagerie]** à utiliser pour ces informations d’identification. Ici, nous avons sélectionné **[!UICONTROL Apple Push Notification Service]** puisque nous travaillons avec iOS.

1. Saisissez l’application mobile **[!UICONTROL Bundle Id]** dans le champ **[!UICONTROL App ID (iOS Bundle ID)]** si vous utilisez le service de notification Push Apple ou dans le champ **[!UICONTROL App ID (nom du pack Android)]** si vous utilisez Firebase Cloud Messaging.

   ![](assets/push_launch_app_configuration.png)

1. Faites glisser et déposez le fichier de clé .p8 ou le fichier de clé privée .json dans le champ **[!UICONTROL Pousser les informations d’identification]**.

1. Saisissez les **[!UICONTROL ID de clé]** et **[!UICONTROL ID d’équipe]** si vous utilisez le service de notification Push Apple.

1. Cliquez sur **[!UICONTROL Enregistrer]** pour créer la configuration de votre application.

### Étape 3 : Créer une configuration Edge {#edge-configuration}

**[!UICONTROL La]** configuration Edge est utilisée par  **** Edgeextension pour envoyer des données personnalisées depuis un périphérique mobile vers  [!DNL Adobe Experience Platform].
Pour configurer [!DNL Adobe Experience Platform], vous devez fournir le nom **[!UICONTROL Sandbox]** et **[!UICONTROL Événement Dataset]**.

1. Dans [!DNL Adobe Experience Platform Launch], sélectionnez l&#39;onglet **[!UICONTROL Edge Configurations]** et cliquez sur **[!UICONTROL Edge Configurations]**.

1. Sélectionnez **[!UICONTROL Nouvelle configuration Edge]** pour ajouter une nouvelle **[!UICONTROL configuration Edge]**.
1. Saisissez un **[!UICONTROL nom]** et cliquez sur **[!UICONTROL Enregistrer]**.

1. Cliquez sur la bascule **[!UICONTROL Adobe Experience Platform]** pour l’activer.

1. Renseignez les champs **[!UICONTROL Sandbox]**, **[!UICONTROL Événement de données]** et **[!UICONTROL Profil de données]**. Cliquez ensuite sur **[!UICONTROL Enregistrer]**.

   ![](assets/push-config-4.png)

### Étape 4 : Configurer une propriété de Platform launch {#launch-property}

La configuration d’une propriété [!DNL Adobe Experience Platform Launch] permet au développeur d’applications mobiles ou au spécialiste du marketing de configurer les attributs des SDK mobiles, tels que les dépassements de délai de session, le sandbox [!DNL Adobe Experience Platform] à cibler et les **[!UICONTROL jeux de données Adobe Experience Platform]** à utiliser pour envoyer des données au SDK mobile.

1. Dans [!DNL Adobe Experience Platform Launch], vérifiez que **[!UICONTROL Client Side]** est sélectionné dans le menu déroulant.

1. sélectionnez l&#39;onglet **[!UICONTROL Propriétés]** et cliquez sur **[!UICONTROL Nouvelle propriété]**.

   ![](assets/push-config-6.png)

1. Entrez un **[!UICONTROL nom]** pour votre nouvelle propriété.

1. Sélectionnez **[!UICONTROL Mobile]** comme **[!UICONTROL Plateforme]**.

   ![](assets/push-config-7.png)

1. Cliquez sur **[!UICONTROL Enregistrer]** pour créer votre nouvelle propriété.

Pour que les SDK requis pour la notification Push fonctionnent, vous devez disposer des extensions SDK suivantes, pour Android et iOS :

* **[!UICONTROL Mobile Core]**  (installé automatiquement)
* **[!UICONTROL Profil]**  (installé automatiquement)
* **[!UICONTROL Edge de Adobe Experience Platform]**
* **[!UICONTROL Adobe Experience Platform Assurance]**, facultatif mais recommandé pour déboguer l’implémentation mobile.

Pour en savoir plus sur les extensions [!DNL Adobe Experience Platform Launch], consultez la [documentation du Platform launch](https://experienceleague.adobe.com/docs/launch-learn/implementing-in-mobile-android-apps-with-launch/configure-launch/launch-add-extensions.html).

Pour configurer **[!UICONTROL Adobe Experience Platform Edge Extension]** pour envoyer des données personnalisées à partir de périphériques mobiles vers [!DNL Adobe Experience Platform].

1. Sélectionnez votre propriété créée précédemment et sélectionnez l&#39;onglet **[!UICONTROL Extensions]** pour vue les extensions de cette propriété.

   ![](assets/push-config-8.png)

1. Cliquez sur **[!UICONTROL Configurer]** sous l&#39;extension **[!UICONTROL Adobe Experience Platform Edge]** Network&#39;.

1. Dans la liste déroulante **[!UICONTROL Edge Configuration]**, sélectionnez la **[!UICONTROL Edge Configuration]** créée lors des étapes précédentes. Pour plus d&#39;informations sur **[!UICONTROL Edge Configuration]**, consultez cette [section](#edge-configuration).

1. Cliquez sur **[!UICONTROL Enregistrer]**.

Pour configurer l&#39;extension **[!UICONTROL Adobe Experience Platform Messaging]** afin d&#39;envoyer des profils Push et des interactions Push aux jeux de données corrects, suivez les mêmes étapes que ci-dessus. Utilisez **[!UICONTROL Sandbox]**, **[!UICONTROL Événement de données]** et **[!UICONTROL Profil de données]** créés dans la configuration [Adobe Experience Platform](#edge-configuration).

### Étape 5 : Publier la propriété {#publish-property}

Vous devez maintenant publier la propriété pour intégrer votre configuration et l’utiliser dans l’application mobile.
Pour publier votre propriété, reportez-vous aux étapes détaillées dans la [documentation du SDK mobile de Adobe Experience Platform](https://aep-sdks.gitbook.io/docs/getting-started/create-a-mobile-property#publish-the-configuration)

### Étape 6 : Configurer ProfileDataSource {#configure-profiledatasource}

Pour configurer `ProfileDataSource`, utilisez la configuration `ProfileDCInletURL` de [!DNL Adobe Experience Platform] et ajoutez ce qui suit dans l&#39;application mobile :

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
