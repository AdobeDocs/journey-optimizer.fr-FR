---
solution: Journey Optimizer
product: journey optimizer
title: Créer une campagne
description: Découvrez comment créer des campagnes dans [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: 617d623c-e038-4b5b-a367-5254116b7815
source-git-commit: 5f8a765eefe4033a642c46e18be518d29b196bc3
workflow-type: tm+mt
source-wordcount: '602'
ht-degree: 0%

---

# Créer une campagne {#create-campaign}

>[!NOTE]
>
>Avant de créer une nouvelle campagne, assurez-vous d’avoir un canal de surface (c’est-à-dire un paramètre prédéfini de message) et un segment Adobe Experience Platform prêt à l’emploi. En savoir plus dans les sections suivantes :
>
>* [Création de surfaces de canal](../configuration/channel-surfaces.md)
>* [Prise en main des segments](../segment/about-segments.md)


## Créer votre première campagne {#create}

1. Accédez au **[!UICONTROL Campaigns]** , puis cliquez sur **[!UICONTROL Create campaign]**.

   >[!NOTE]
   >
   >Vous pouvez également dupliquer une campagne active existante pour en créer une nouvelle. [En savoir plus](modify-stop-campaign.md#duplicate)

   ![](assets/create-campaign.png)

1. Dans le **[!UICONTROL Properties]** , indiquez comment exécuter l’opération :

   * **[!UICONTROL Scheduled]**
   * **[!UICONTROL API-triggered]**

   Pour plus d&#39;informations sur le type d&#39;opération et les interventions associées, reportez-vous à cette section [section](#campaigntype).

1. Dans le **[!UICONTROL Actions]** , choisissez le canal et la surface du canal à utiliser pour envoyer votre message, puis cliquez sur **[!UICONTROL Create]**.

   Une surface est une configuration définie par une [Administrateur système](../start/path/administrator.md). Il contient tous les paramètres techniques pour l’envoi du message, tels que les paramètres d’en-tête, le sous-domaine, les applications mobiles, etc. [En savoir plus](../configuration/channel-surfaces.md).

   ![](assets/create-campaign-action.png)

   >[!NOTE]
   >
   >Seules les surfaces de canal compatibles avec le type de campagne marketing sont répertoriées dans la liste déroulante.

1. Indiquez un titre et une description pour la campagne.

   <!--To test the content of your message, toggle the **[!UICONTROL Content experiment]** option on. This allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.[Learn more about content experiment](../campaigns/content-experiment.md).-->

1. Pour attribuer des libellés d’utilisation des données personnalisés ou de base à la campagne, cliquez sur le bouton **[!UICONTROL Manage access]** bouton . [En savoir plus sur le contrôle d’accès au niveau de l’objet (OLA)](../administration/object-based-access.md)

## Créer le message {#content}

Dans le **[!UICONTROL Actions]** , créez le message à envoyer avec la campagne.

1. Cliquez sur le bouton **[!UICONTROL Edit content]** , puis créez et concevez le contenu de votre message.

   Découvrez les étapes détaillées pour créer le contenu de votre message dans les pages suivantes :

   <table style="table-layout:fixed">
    <tr style="border: 0;">
    <td>
    <a href="../email/create-email.md">
    <img alt="prospect" src="../assets/do-not-localize/email.jpg">
    </a>
    <div><a href="../email/create-email.md"><strong>Créer des emails</strong>
    </div>
    <p>
    </td>
    <td>
    <a href="../push/create-push.md">
      <img alt="Inrégulier" src="../assets/do-not-localize/push.jpg">
    </a>
    <div>
    <a href="../push/create-push.md"><strong>Créer des notifications push</strong></a>
    </div>
    <p>
    </td>
    <td>
    <a href="../sms/create-sms.md">
      <img alt="Validation" src="../assets/do-not-localize/sms.jpg">
    </a>
    <div>
    <a href="../sms/create-sms.md"><strong>Créer des SMS</strong></a>
    </div>
    <p>
    </td>
    </tr>
    </table>

1. Une fois votre contenu défini, utilisez la variable **[!UICONTROL Simulate content]** pour prévisualiser et tester votre contenu avec des profils de test. [En savoir plus](../email/preview.md).

1. Cliquez sur la flèche pour revenir à l&#39;écran de création de la campagne.

   ![](assets/create-campaign-design.png)

1. Dans le **[!UICONTROL Actions tracking]** , indiquez si vous souhaitez suivre la réaction des destinataires à votre diffusion : vous pouvez effectuer le suivi des clics et/ou des ouvertures.

   Les résultats du tracking seront accessibles à partir du rapport de l&#39;opération, une fois l&#39;opération exécutée. [En savoir plus sur les rapports de campagne](../reports/campaign-global-report.md)

## Définition de l’audience {#audience}

1. Définissez l’audience à cibler. Pour ce faire, cliquez sur le bouton **[!UICONTROL Select audience]** pour afficher la liste des segments Adobe Experience Platform disponibles. [En savoir plus sur les segments](../segment/about-segments.md)

   >[!NOTE]
   >
   >Pour les campagnes déclenchées par l’API, l’audience doit être définie via un appel API. [En savoir plus](api-triggered-campaigns.md)

   Dans le **[!UICONTROL Identity namespace]** , choisissez l’espace de noms à utiliser pour identifier les individus du segment sélectionné. [En savoir plus sur les espaces de noms](../event/about-creating.md#select-the-namespace)

   ![](assets/create-campaign-namespace.png)

   >[!NOTE]
   >
   >Les personnes appartenant à un segment qui n’a pas l’identité sélectionnée (espace de noms) parmi leurs différentes identités ne seront pas ciblées par la campagne.

   <!--If you are are creating an API-triggered campaign, the **[!UICONTROL cURL request]** section allows you to retrieve the **[!UICONTROL Campaign ID]** to use in the API call. [Learn more](api-triggered-campaigns.md)-->

## Planification de la campagne {#schedule}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="Démarrage de campagne"
>abstract="TBC"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="Fin de campagne"
>abstract="TBC"

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="Déclencheurs d’action de campagne"
>abstract="TBC"

1. Pour exécuter votre campagne à une date spécifique ou à une fréquence récurrente, configurez la variable **[!UICONTROL Schedule]** . [Découvrez comment planifier des campagnes](#schedule)

1. Pour attribuer des libellés d’utilisation des données personnalisés ou de base à la campagne, cliquez sur le bouton **[!UICONTROL Manage access]** bouton . [En savoir plus sur le contrôle d’accès au niveau de l’objet (OLA)](../administration/object-based-access.md)

Une fois votre campagne prête, vous pouvez la réviser et la publier. [En savoir plus](#review-activate)

## Type de campagne {#campaigntype}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Type de campagne"
>abstract="Pour un message marketing en spécifiant une date d&#39;envoi, la variable **Planifié** type est le plus approprié. Cependant, si vous souhaitez envoyer des messages transactionnels tels que la réinitialisation du mot de passe ou l’abandon de carte, la variable **déclenché par l’API** type est le meilleur choix."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_category"
>title="Catégorie de campagne"
>abstract="La valeur de catégorie est directement associée à la valeur de type de campagne. Planification du type de campagne pour le **Marketing** catégorie et type déclenché par l’API pour la catégorie **Transactionnel**"

Deux types de campagne sont disponibles :

* **[!UICONTROL Scheduled]**: exécuter immédiatement l’opération ou à une date spécifiée ; Les campagnes planifiées visent à envoyer des **marketing** saisissez des messages.

* **[!UICONTROL API-triggered]**: exécutez la campagne à l’aide d’un appel API. Les campagnes déclenchées par l’API sont destinées à envoyer des **transactionnel** messages, c’est-à-dire messages envoyés suite à une action effectuée par un individu : réinitialisation du mot de passe, abandon de carte, etc. [Découvrez comment déclencher une campagne à l’aide d’API](api-triggered-campaigns.md)
