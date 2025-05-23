---
solution: Journey Optimizer
product: journey optimizer
title: Configuration du canal WhatsApp
description: Découvrez comment configurer votre environnement pour envoyer des messages WhatsApp avec Journey Optimizer
feature: Whatsapp, Channel Configuration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Beta" type="Informative"
exl-id: d1f40cd8-f311-4df6-b401-8858095cef3e
source-git-commit: b6fd60b23b1a744ceb80a97fb092065b36847a41
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 48%

---

# Prise en main de la configuration de WhatsApp {#whatsapp-config}

>[!BEGINSHADEBOX]

**Table des matières**

* [Commencer avec les messages WhatsApp](get-started-whatsapp.md)
* **[Prise en main de la configuration de WhatsApp](whatsapp-configuration.md)**
* [Créer un message WhatsApp](create-whatsapp.md)
* [Vérifier et envoyer des messages WhatsApp](send-whatsapp.md)

>[!ENDSHADEBOX]

Avant d&#39;envoyer votre message WhatsApp, vous devez configurer votre environnement Adobe Journey Optimizer et vous associer à votre compte WhatsApp. Procédez comme suit :

1. [Créer vos identifiants d&#39;API WhatsApp](#WhatsApp-credentials)
1. [Créer votre configuration WhatsApp](#WhatsApp-configuration)

Ces étapes doivent être exécutées par un [Administrateur ou une Administratrice système](../start/path/administrator.md) Adobe Journey Optimizer.

## Créer des identifiants d’API WhatsApp {#whatsapp-credentials}

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** `>` **[!UICONTROL Canaux]** et sélectionnez le menu **[!UICONTROL Informations d’identification de l’API]**. Cliquez sur le bouton **[!UICONTROL Créer des informations d’identification de l’API]**.

1. Configurez vos informations d’identification d’API, comme décrit ci-dessous :

   * **Jeton API** : saisissez votre jeton API. En savoir plus dans la [documentation Meta](https://developers.facebook.com/docs/facebook-login/guides/access-tokens/)
   * **Identifiant de compte professionnel** : saisissez le numéro unique associé à votre portefeuille professionnel. En savoir plus dans la [documentation Meta](https://www.facebook.com/business/help/1181250022022158?id=180505742745347).

   ![](assets/whatsapp-api.png)

1. Cliquez sur **[!UICONTROL Continuer]**.

1. Choisissez le **Compte professionnel** vous souhaitez vous connecter à vos identifiants d&#39;API WhatsApp.

   ![](assets/whatsapp-api-2.png)

1. Sélectionnez le **Numéro de téléphone** utilisé pour envoyer vos messages Whatsapp.

1. Les paramètres de votre numéro de téléphone sont automatiquement renseignés :

   * **Évaluation de la qualité** : reflète les commentaires des clients sur les messages envoyés au cours des dernières 24 heures.
      * Vert : Haute qualité
      * Jaune : qualité Medium
      * Rouge : mauvaise qualité

     En savoir plus sur la [Évaluation de la qualité](https://www.facebook.com/business/help/766346674749731#)

   * **Débit** : indique le taux auquel votre numéro de téléphone peut envoyer des messages.

1. Cliquez sur **[!UICONTROL Envoyer]** lorsque vous avez terminé la configuration de vos informations d’identification d’API.

Après avoir créé et configuré vos informations d’identification API, vous devez maintenant créer une configuration de canal pour les messages WhatsApp. [En savoir plus](#whatsapp-configuration)

## Créer une configuration WhatsApp {#whatsapp-configuration}

1. Dans le rail de gauche, accédez à **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** et sélectionnez **[!UICONTROL Paramètres généraux]** > **[!UICONTROL Configurations de canal]**. Cliquez sur le bouton **[!UICONTROL Créer une configuration de canal]**.

   ![](assets/whatsapp-config-1.png)

1. Saisissez un nom et une description (facultatif) pour la configuration, puis sélectionnez le canal WhatsApp.

   >[!NOTE]
   >
   > Les noms doivent commencer par une lettre (A-Z). Ils ne peuvent contenir que des caractères alphanumériques. Vous pouvez également utiliser le trait de soulignement `_`, le point`.` et le trait d&#39;union `-`.

1. Sélectionnez **[!DNL WhatsApp]** comme canal.

   ![](assets/whatsapp-config-2.png)

1. Sélectionnez **[!UICONTROL Action(s) marketing)]** pour associer des politiques de consentement aux messages à l’aide de cette configuration. Toutes les politiques de consentement associées à cette action marketing sont utilisées afin de respecter les préférences de vos clientes et clients. En savoir plus

1. Sélectionnez la **[!UICONTROL configuration de l’API WhatsApp]** créée précédemment.

   ![](assets/whatsapp-config-3.png)

1. Saisissez le **[!UICONTROL Numéro dʼexpéditeur]** à utiliser lors de vos communications.

1. Une fois tous les paramètres configurés, cliquez sur **[!UICONTROL Envoyer]** pour confirmer. Vous pouvez également enregistrer la configuration de canal en tant que brouillon et reprendre son paramétrage ultérieurement.

1. Une fois la configuration de canal créée, elle s’affiche dans la liste avec le statut **[!UICONTROL En cours de traitement]**.

   >[!NOTE]
   >
   >Si les vérifications ne réussissent pas, découvrez les raisons possibles de l’échec dans [cette section](../configuration/channel-surfaces.md).

1. Une fois les contrôles réussis, la configuration de canal obtient le statut **[!UICONTROL Actif]**. Elle est prête à être utilisée pour diffuser des messages.

Vous êtes maintenant prêt à envoyer des messages WhatsApp avec Journey Optimizer.
