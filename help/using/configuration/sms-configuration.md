---
title: Configuration des SMS
description: Découvrez comment configurer votre environnement pour envoyer des SMS avec Journey Optimizer
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: c86c9121e601f0c208626f578e923e7d30adc9c4
workflow-type: tm+mt
source-wordcount: '414'
ht-degree: 35%

---

# Configurer le canal SMS {#sms-configuration}

>[!CAUTION]
>
> L’utilisation du canal SMS est actuellement disponible en accès anticipé uniquement pour certains utilisateurs. Si vous souhaitez utiliser cette fonctionnalité, contactez votre chargé de compte d’Adobe.

[!DNL Journey Optimizer] vous permet de créer vos parcours et d&#39;envoyer des messages à une audience ciblée.

## Création d’informations d’identification d’API {#create-api}

Pour configurer votre fournisseur de SMS avec Journey Optimizer, procédez comme suit :

1. Accédez au **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Informations d’identification de l’API]** , puis cliquez sur **[!UICONTROL Création d’informations d’identification d’API]**.

   ![](../assets/sms_4.png)

1. Sélectionnez Sinch comme votre **[!UICONTROL Fournisseur de SMS]**.

1. Saisissez un **[!UICONTROL Nom]** pour vos informations d’identification d’API.

1. Saisissez votre **[!UICONTROL ID de service]** et **[!UICONTROL Jeton API]**.

   >[!NOTE]
   >
   > Sinch nécessite des informations d’identification d’API spéciales. Pour rechercher votre **[!UICONTROL ID de service]** et **[!UICONTROL Jeton API]**, accédez au menu SMS > API depuis votre compte Sinch,

   ![](../assets/sms_5.png)

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification d’API.

Après avoir créé et configuré vos informations d’identification API, vous devez maintenant créer un paramètre prédéfini de message pour les messages SMS.

## Créer un paramètre prédéfini de message pour les SMS {#message-preset-sms}

Une fois votre canal SMS configuré, vous devez créer un paramètre prédéfini de message pour pouvoir envoyer des SMS depuis **[!DNL Journey Optimizer]**.

Pour créer un préréglage de message, procédez comme suit :

1. Accédez au menu **[!UICONTROL Canaux]**/**[!UICONTROL Marques]**/**[!UICONTROL Préréglages de message]**, puis cliquez sur **[!UICONTROL Créer un préréglage de message]**. 

   ![](../assets/preset-create.png)

1. Saisissez un nom et une description (facultatif) pour le paramètre prédéfini, puis sélectionnez le canal SMS.

   ![](../assets/sms_preset.png)

   >[!NOTE]
   >
   > Les noms doivent commencer par une lettre (A-Z). Ils ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser le trait de soulignement `_`, le point`.` et le trait d&#39;union `-`.

1. Configurez la variable **SMS** paramètres.

   ![](../assets/preset-sms.png)

   * Sélectionnez la **[!UICONTROL Type de SMS]** qui sera envoyé avec le paramètre prédéfini : **[!UICONTROL Transactionnel]** ou **[!UICONTROL Marketing]**.

   * Sélectionnez la **[!UICONTROL Configuration des SMS]** pour l’associer au paramètre prédéfini.

      Pour plus d&#39;informations sur la configuration de votre environnement pour envoyer des SMS, reportez-vous à la section [cette section](sms-configuration.md).

   * Saisissez le **[!UICONTROL Numéro d&#39;expéditeur]** &#x200B; que vous voulez utiliser pour vos communications.

1. Une fois tous les paramètres configurés, cliquez sur **[!UICONTROL Envoyer]** pour confirmer. Vous pouvez également enregistrer le préréglage de message en tant que version préliminaire et reprendre sa configuration ultérieurement.

   ![](../assets/sms_preset_2.png)

1. Une fois le préréglage de message créé, il s&#39;affiche dans la liste avec le statut **[!UICONTROL Traitement]**.

   >[!NOTE]
   >
   >Si les vérifications ne réussissent pas, découvrez les raisons possibles de l’échec dans [cette section](#monitor-message-presets).

1. Une fois les vérifications effectuées, le préréglage de message obtient le statut **[!UICONTROL Actif]**. Il est prêt à être utilisé pour diffuser des messages.

   ![](../assets/preset-active.png)

Pour savoir comment configurer un paramètre prédéfini de message pour les notifications push et les emails, reportez-vous à la section [cette section](message-presets.md).

Vous êtes maintenant prêt à envoyer des SMS avec Journey Optimizer.

**Rubrique connexe**

* [Créer un SMS](../create-sms.md)
* [Ajout d&#39;un message dans un parcours](../building-journeys/journeys-message.md)
