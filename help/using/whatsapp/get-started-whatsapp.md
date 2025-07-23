---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec les messages WhatsApp
description: Découvrir comment créer et envoyer des messages WhatsApp dans Journey Optimizer
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 22df2bfa-4d86-464e-ad83-3aa457e3a747
source-git-commit: 7f507dc0113e85191429c2c48b873112b590e3ce
workflow-type: tm+mt
source-wordcount: '332'
ht-degree: 55%

---

# Commencer avec les messages WhatsApp {#get-started-whatsapp}

>[!BEGINSHADEBOX]

**Table des matières**

* **[Commencer avec les messages WhatsApp](get-started-whatsapp.md)**
* [Commencer la configuration WhatsApp](whatsapp-configuration.md)
* [Créer un message WhatsApp](create-whatsapp.md)
* [Vérifier et envoyer vos messages WhatsApp](send-whatsapp.md)

>[!ENDSHADEBOX]

Vous pouvez désormais envoyer des messages WhatsApp directement via Journey Optimizer via l’API [Cloud](https://developers.facebook.com/docs/whatsapp/cloud-api/) de Meta. Cette fonctionnalité permet une intégration transparente de WhatsApp dans les parcours et les campagnes, ce qui améliore la communication et l’engagement avec les destinataires.

* Dans un **parcours**. Créez un parcours, ajoutez une activité **WhatsApp** et définissez les paramètres de base, puis accédez au volet de droite **[!UICONTROL Actions : WhatsApp]** pour créer le contenu du message WhatsApp. Découvrez comment créer un parcours sur [cette page](../building-journeys/journey-gs.md).

* Dans une **Campagne**. Créez une campagne, sélectionnez **WhatsApp** comme action et définissez les paramètres de base, puis modifiez le contenu du message WhatsApp à envoyer. Découvrez comment créer une campagne sur [cette page](../campaigns/create-campaign.md#configure).

![](assets/do-not-localize/whatsapp-beta.png){zoomable="yes"}

## Prérequis {#prereq}

Pour intégrer WhatsApp à Journey Optimizer, vous avez besoin des éléments suivants :

* Compte Meta Business Manager
* Compte WhatsApp Business
* Numéro de téléphone WhatsApp
* [Jeton d’autorisation utilisateur avec les autorisations appropriées](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
* [Modèles Meta approuvés](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/)
* [Configuration des méta-Webhooks](https://developers.facebook.com/docs/whatsapp/webhooks/)


Vous devez également prendre connaissance des points suivants avant de procéder à l’intégration :

* [Règles de contenu WhatsApp](https://www.whatsapp.com/legal/messaging-guidelines)
* [Conformité aux politiques Meta](https://www.whatsapp.com/legal)
* [Limites de conversation sur une période de 24 heures](https://developers.facebook.com/docs/whatsapp/messaging-limits/)

## Limites {#limitations}

Les restrictions suivantes s&#39;appliquent au canal WhatsApp :

* Le canal WhatsApp de Adobe Journey Optimizer est conforme à la loi HIPAA, mais les fournisseurs tiers ne sont pas couverts par la loi Adobe. Les clients sont responsables de leur propre conformité et de la validation du fournisseur.

* Notez que les messages de réponse automatisés ou prédéfinis ne sont pas pris en charge.

* À compter d’avril 2025, la diffusion de tous les messages de modèle marketing aux utilisateurs de WhatsApp qui ont un numéro de téléphone aux États-Unis (un numéro composé d’un indicatif +1 et d’un indicatif régional des États-Unis) a été temporairement suspendue. [En savoir plus dans la documentation sur les métadonnées](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/send-message-templates#per-user-marketing-template-message-limits)

* La fonctionnalité d’intégration native ne permet pas l’intégration à un fournisseur de services professionnels (BSP) tiers.

## Vidéo pratique {#video}


La vidéo ci-dessous montre comment créer un parcours avec une action WhatsApp.

+++ Voir la vidéo

>[!VIDEO](https://video.tv.adobe.com/v/3451621?learn=on)

+++
