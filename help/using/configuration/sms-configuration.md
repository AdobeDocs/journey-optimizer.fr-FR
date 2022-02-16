---
title: Configuration des SMS
description: Découvrez comment configurer votre environnement pour envoyer des messages SMS avec Journey Optimizer
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 4dcd22ed-bf7e-4789-ab7b-33544c857db8
source-git-commit: b43e3432ede1d4985e0a6b57b57c5efc3cf60c50
workflow-type: ht
source-wordcount: '397'
ht-degree: 100%

---

# Configuration du canal SMS {#sms-configuration}

>[!CAUTION]
>
> Lʼutilisation du canal SMS est actuellement disponible en accès anticipé uniquement pour certains utilisateurs uniquement. Si vous souhaitez utiliser cette fonctionnalité, contactez votre gestionnaire de compte Adobe.

[!DNL Journey Optimizer] vous permet de créer vos parcours et dʼenvoyer des messages à une audience ciblée.

## Création d’informations d’identification API {#create-api}

Pour configurer votre fournisseur de SMS avec Journey Optimizer, procédez comme suit :

1. Accédez au menu **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Informations d’identification API]**, puis cliquez sur **[!UICONTROL Création d’informations d’identification API]**.

   ![](../assets/sms_4.png)

1. Sélectionnez Sinch an tant que **[!UICONTROL Fournisseur de SMS]**.

1. Entrez un **[!UICONTROL Nom]** pour vos informations d’identification API.

1. Saisissez votre **[!UICONTROL ID de service]** et **[!UICONTROL Jeton API]**.

   >[!NOTE]
   >
   > Sinch nécessite des informations d’identification API spéciales. Pour rechercher votre **[!UICONTROL ID de service]** et **[!UICONTROL Jeton API]**, accédez au menu SMS > API depuis votre compte Sinch,

   ![](../assets/sms_5.png)

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification API.

Après avoir créé et configuré vos informations d’identification API, vous devez maintenant créer un préréglage de message pour les messages SMS.

## Création dʼun préréglage de message pour les messages SMS {#message-preset-sms}

Une fois votre canal SMS configuré, vous devez créer un préréglage de message afin de pouvoir envoyer des SMS depuis **[!DNL Journey Optimizer]**.

Pour créer un préréglage de message, procédez comme suit :

1. Accédez au menu **[!UICONTROL Canaux]**/**[!UICONTROL Marques]**/**[!UICONTROL Préréglages de message]**, puis cliquez sur **[!UICONTROL Créer un préréglage de message]**. 

   ![](../assets/preset-create.png)

1. Saisissez un nom et une description (facultatif) pour le préréglage, puis sélectionnez le canal SMS.

   ![](../assets/sms_preset.png)

   >[!NOTE]
   >
   > Les noms doivent commencer par une lettre (A-Z). Ils ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser le trait de soulignement `_`, le point`.` et le trait d&#39;union `-`.

1. Configurez les paramètres des **SMS**.

   ![](../assets/preset-sms.png)

   * Sélectionnez le **[!UICONTROL Type de SMS]** qui sera envoyé avec le préréglage : **[!UICONTROL Transactionnel]** ou **[!UICONTROL Marketing]**.

   * Sélectionnez la **[!UICONTROL Configuration SMS]** à associer au préréglage.

      Pour plus dʼinformations sur la configuration de votre environnement pour envoyer des messages SMS, consultez [cette section](sms-configuration.md).

   * Saisissez le **[!UICONTROL Numéro dʼexpéditeur]** à utiliser lors de vos communications.

1. Une fois tous les paramètres configurés, cliquez sur **[!UICONTROL Envoyer]** pour confirmer. Vous pouvez également enregistrer le préréglage de message en tant que version préliminaire et reprendre sa configuration ultérieurement.

   ![](../assets/sms_preset_2.png)

1. Une fois le préréglage de message créé, il s&#39;affiche dans la liste avec le statut **[!UICONTROL Traitement]**.

   >[!NOTE]
   >
   >Si les vérifications ne réussissent pas, découvrez les raisons possibles de l’échec dans [cette section](#monitor-message-presets).

1. Une fois les vérifications effectuées, le préréglage de message obtient le statut **[!UICONTROL Actif]**. Il est prêt à être utilisé pour diffuser des messages.

   ![](../assets/preset-active.png)

Vous êtes maintenant prêt à envoyer des messages SMS avec Journey Optimizer.

**Rubriques connexes**

* [Création dʼun SMS](../messages/create-sms.md)
* [Ajout dʼun message dans un parcours](../building-journeys/journeys-message.md)
