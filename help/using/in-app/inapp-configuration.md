---
title: Configuration in-app
description: Découvrez comment configurer votre environnement pour envoyer des messages in-app avec Journey Optimizer
role: Admin
level: Intermediate
keywords: in-app, message, configuration, platform
exl-id: 469c05f2-652a-4899-a657-ddc4cebe3b42
source-git-commit: 6f92f9ce0a4785f0359658f00150d283f1326900
workflow-type: tm+mt
source-wordcount: '551'
ht-degree: 67%

---

# Configurer le canal in-app {#inapp-configuration}

Avant d’envoyer des messages in-app, vous devez configurer votre canal in-app dans [!DNL Adobe Experience Platform Data Collection].

1. À partir de votre compte [!DNL Adobe Experience Platform Data Collection], accédez au menu **[!UICONTROL Train de données]** et cliquez sur **[!UICONTROL Nouveau train de données]**. Pour en savoir plus sur la création de train de données, consultez [cette page](https://experienceleague.adobe.com/docs/experience-platform/edge/datastreams/configure.html?lang=fr).

1. Sélectionnez le service [!DNL Adobe Experience Platform].

   [!DNL Edge Segmentation] et [!DNL Adobe Journey Optimizer] doivent être sélectionnés.

   ![](assets/inapp_config_6.png)

   >[!NOTE]
   >
   >Pour activer les expériences de contenu pour le canal in-app, vous devez vous assurer que le [jeu de données](../data/get-started-datasets.md) utilisé dans votre [train de données](https://experienceleague.adobe.com/docs/experience-platform/datastreams/overview.html?lang=fr){target="_blank"} in-app est également présent dans la configuration des rapports. Dans le cas contraire, les données in-app ne s’afficheront pas dans les rapports d’expérience de contenu. [Découvrez comment ajouter des jeux de données](../campaigns/reporting-configuration.md#add-datasets).
   >
   >Le jeu de données est utilisé en lecture seule par le système de création de rapports de [!DNL Journey Optimizer] et n’a aucune incidence sur la collecte ou l’ingestion de données.

1. Accédez ensuite au menu **[!UICONTROL Surfaces in-app]** et cliquez sur **[!UICONTROL Créer la surface d’application]**.

   >[!NOTE]
   >
   > Vous avez besoin de l’autorisation **Gérer la configuration de l’application** pour accéder au menu **[!UICONTROL Surfaces de l’application]**. Pour plus d’informations, regardez [cette vidéo](#video).

   ![](assets/inapp_config_1.png)

1. Ajoutez un nom à votre **[!UICONTROL Surface d’application]**.

   ![](assets/inapp_config_2b.png)

1. Dans la **[!UICONTROL Apple iOS]** , configurez votre application mobile pour Apple iOS.

+++ En savoir plus

   1. Saisissez votre **[!UICONTROL Identifiant du lot iOS]**. Voir la [Documentation Apple](https://developer.apple.com/documentation/appstoreconnectapi/bundle_ids) pour plus d’informations sur l’**ID de bundle**.

   1. (Facultatif) Choisissez la **[!UICONTROL Sandbox]** d’où vous souhaitez envoyer des notifications push. Notez que le choix d’un environnement de test spécifique nécessite les autorisations d’accès nécessaires.

      Pour plus d’informations sur la gestion des environnements de test, voir [cette page](../administration/sandboxes.md#assign-sandboxes).

   1. Activez la variable **[!UICONTROL Informations d’identification push]** pour faire glisser et déposer votre fichier de clé d’authentification .p8 si nécessaire.

      Vous pouvez également activer la variable **[!UICONTROL Saisie manuelle des informations d’identification push]** pour copier et coller directement votre clé d’authentification APNS.

   1. Saisissez votre **[!UICONTROL ID de clé]** et **[!UICONTROL Identifiant de l’équipe]**.

      ![](assets/inapp_config_2.png)

+++

1. Dans la **[!UICONTROL Android]** , configurez votre application mobile pour Android.

+++ En savoir plus

   1. Saisissez votre **[!UICONTROL Nom du package Android]**. Voir la [Documentation Android](https://support.google.com/admob/answer/9972781?hl=en#:~:text=The%20package%20name%20of%20an,supported%20third%2Dparty%20Android%20stores) pour plus d’informations sur le **nom du package**.

   1. (Facultatif) Choisissez la **[!UICONTROL Sandbox]** d’où vous souhaitez envoyer des notifications push. Notez que le choix d’un environnement de test spécifique nécessite les autorisations d’accès nécessaires.

      Pour plus d’informations sur la gestion des environnements de test, voir [cette page](../administration/sandboxes.md#assign-sandboxes).

   1. Activez la variable **[!UICONTROL Informations d’identification push]** pour faire glisser et déposer votre fichier de clé privée .json si nécessaire.

      Vous pouvez également activer la variable **[!UICONTROL Saisie manuelle des informations d’identification push]** pour copier et coller directement votre clé privée FCM.

      ![](assets/inapp_config_7.png)

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
   * Identité
   * Mobile Core
   * Profile

   Voir [cette page](https://experienceleague.adobe.com/docs/experience-platform/tags/ui/extensions/overview.html?lang=fr#add-a-new-extension) pour la procédure détaillée.

   ![](assets/inapp_config_5.png)

Le canal in-app est maintenant configuré. Vous pouvez commencer à envoyer des messages in-app à vos utilisateurs.

**Rubriques connexes :**

* [Créer un message in-app](create-in-app.md)
* [Création d’une campagne](../campaigns/create-campaign.md)
* [Concevoir un message in-app](design-in-app.md)
* [Rapport in-app](../reports/campaign-global-report.md#inapp-report)


## Tutoriels vidéo{#video}

* La vidéo ci-dessous montre comment attribuer l’autorisation **Gérer la configuration de l’application** pour accéder au menu Surfaces de l’application.

  +++Voir la vidéo

  >[!VIDEO](https://video.tv.adobe.com/v/3421607)

+++


