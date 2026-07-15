---
title: Création d’une configuration de canal pour un canal personnalisé
description: Découvrez comment créer une configuration de canal pour un canal personnalisé dans Adobe Journey Optimizer.
feature: Channel Configuration
topic: Content Management
role: Admin
level: Experienced
badge: label="Disponibilité limitée" type="Informative"
source-git-commit: 94ca2d9458152fb471e9590d053c4729a4a5134f
workflow-type: tm+mt
source-wordcount: '344'
ht-degree: 2%

---


# Créer une configuration des canaux {#create-channel-config}

Une configuration de canal associe votre canal personnalisé à un paramètre prédéfini nommé et réutilisable que les spécialistes marketing sélectionnent lors de la création de campagnes et de parcours.

Pour créer une configuration de canal pour un canal personnalisé, procédez comme suit.

1. Accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Configurations de canal]** et cliquez sur **[!UICONTROL Créer une configuration de canal]**. En savoir plus sur la [création d’une configuration de canal](../configuration/channel-surfaces.md).

1. Dans la liste déroulante **[!UICONTROL Sélectionner un canal]**, sélectionnez l’un de vos canaux personnalisés activés.

   ![Sélectionner le canal](assets/custom_channel_select_channel.png){width="100%"}

1. Si le canal sélectionné utilise l’authentification (le type n’est pas **Aucun**), le champ **[!UICONTROL Informations d’identification de l’API]** s’affiche. Sélectionnez les informations d’identification à utiliser pour cette configuration. [En savoir plus sur les informations d’identification d’API](custom-channel-api-credentials.md)

   ![Sélectionner les informations d’identification de l’API](assets/custom_channel_config_api_credentials.png){width="100%"}

1. Si vous avez configuré des sous-domaines pour les canaux personnalisés dans [!DNL Journey Optimizer], vous pouvez sélectionner un sous-domaine délégué à utiliser pour les liens de suivi présents dans la payload pour cette configuration. [Découvrez comment déléguer un sous-domaine](custom-channel-subdomains.md)

1. Si le canal sélectionné comporte des en-têtes ou des paramètres de requête [définis comme variables](create-custom-channel.md#endpoint-configuration) pour l’URL de point d’entrée, la section **[!UICONTROL Paramètres dynamiques]** s’affiche.

   Saisissez la valeur de chaque paramètre. Vous pouvez utiliser l’éditeur de personnalisation pour injecter des valeurs dynamiques (par exemple, un identifiant utilisateur résolu à partir du profil). Vous pouvez ainsi personnaliser la requête de chaque destinataire en fonction de ses données de profil.

   ![ Paramètres dynamiques ](assets/custom_channel_config_dynamic_parameters.png){width="100%"}

1. Si des champs de payload sont activés pour le canal personnalisé lorsque la case **[!UICONTROL Configuration du canal]** est cochée, ces champs s’affichent dans la section **[!UICONTROL Configuration de la payload]**. [En savoir plus](create-custom-channel.md#payload-configuration)

   ![Champs de payload](assets/custom_channel_config_payload.png){width="100%"}

   Configurez une valeur pour chaque champ en fonction de cette configuration. Cela s’avère utile pour les champs qui peuvent varier en fonction du contexte de la campagne ou du parcours, tels que les informations de l’expéditeur ou les modèles de message.

1. Pour les campagnes orchestrées, complétez la section **[!UICONTROL Détails d’exécution]** pour mapper les dimensions de profil et spécifier l’adresse d’exécution.

   ![Détails d’exécution dans les campagnes orchestrées](assets/custom_channel_oc_execution_details.png){width="80%"}

1. Cliquez sur **[!UICONTROL Envoyer]** pour enregistrer et activer la configuration du canal.

<!--
>[!CAUTION]
>
>If your organization uses approval policies, you may need to request approval before activating journeys or campaigns that use this channel configuration. [Learn more](../test-approve/gs-approval.md)
-->

## Étapes suivantes {#next-steps}

Votre canal personnalisé est maintenant entièrement configuré. Les marketeurs peuvent commencer à l’utiliser pour créer des expériences client :

* [Création d’expériences de canal personnalisé](create-custom-experience.md)
* [Test de votre canal personnalisé](test-custom-channel.md)
* [Surveillance des canaux personnalisés](configure-custom-channel.md)
