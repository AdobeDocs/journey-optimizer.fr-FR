---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec les messages WhatsApp
description: Découvrir comment créer et envoyer des messages WhatsApp dans Journey Optimizer
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
exl-id: 22df2bfa-4d86-464e-ad83-3aa457e3a747
source-git-commit: 31e25c511d8873e54c7b92e65511108a77f84941
workflow-type: tm+mt
source-wordcount: '320'
ht-degree: 44%

---

# Commencer avec les messages WhatsApp {#get-started-whatsapp}

Vous pouvez désormais envoyer des messages WhatsApp directement via Journey Optimizer via l’API [Cloud](https://developers.facebook.com/docs/whatsapp/cloud-api/) de Meta. Cette fonctionnalité permet une intégration transparente de WhatsApp dans les parcours et les campagnes, ce qui améliore la communication et l’engagement avec les destinataires.

* Dans un **parcours**. Créez un parcours, ajoutez une activité **WhatsApp** et définissez les paramètres de base, puis accédez au volet de droite **[!UICONTROL Actions : WhatsApp]** pour créer le contenu du message WhatsApp. Découvrez comment créer un parcours sur [cette page](../building-journeys/journey-gs.md).

* Dans une **Campagne**. Créez une campagne, sélectionnez **WhatsApp** comme action et définissez les paramètres de base, puis modifiez le contenu du message WhatsApp à envoyer. Découvrez comment créer une campagne sur [cette page](../campaigns/create-campaign.md#configure).

![](assets/do-not-localize/whatsapp-beta.png){zoomable="yes"}

## Prérequis {#prereq}

Pour intégrer WhatsApp à Journey Optimizer, vous avez besoin des éléments suivants :

* Compte Meta Business Manager
* [Compte professionnel WhatsApp avec nom d&#39;expéditeur et numéro de téléphone vérifiés](https://developers.facebook.com/docs/whatsapp/overview/business-accounts/)
* [Jeton d’autorisation utilisateur avec les autorisations appropriées](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
* [Modèles Meta approuvés](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/)

Vous devez également prendre connaissance des points suivants avant de procéder à l’intégration :

* [Règles de contenu WhatsApp](https://www.whatsapp.com/legal/messaging-guidelines)
* [Conformité aux politiques Meta](https://www.whatsapp.com/legal)
* [Limites de conversation sur une période de 24 heures](https://developers.facebook.com/docs/whatsapp/messaging-limits/)

## Limites {#limitations}

Les restrictions suivantes s&#39;appliquent au canal WhatsApp :

* Le canal WhatsApp de Adobe Journey Optimizer est conforme à la loi HIPAA, mais les fournisseurs tiers ne sont pas couverts par la loi Adobe. Les clients sont responsables de leur propre conformité et de la validation du fournisseur.

* Notez que les messages de réponse automatisés ou prédéfinis ne sont pas encore pris en charge.

* À compter d’avril 2025, la diffusion de tous les messages de modèle marketing aux utilisateurs de WhatsApp qui ont un numéro de téléphone aux États-Unis (un numéro composé d’un indicatif +1 et d’un indicatif régional des États-Unis) a été temporairement suspendue. [En savoir plus dans la documentation sur les métadonnées](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/send-message-templates#per-user-marketing-template-message-limits)

* La fonctionnalité d’intégration native ne permet pas l’intégration à un fournisseur de services professionnels (BSP) tiers.

## Vidéo pratique {#video}

La vidéo ci-dessous montre comment intégrer WhatsApp en tant que canal natif dans Adobe Journey Optimizer pour diffuser des messages sécurisés, personnalisés et en temps réel à grande échelle.

+++ Voir la vidéo

>[!VIDEO](https://video.tv.adobe.com/v/3470244?learn=on)

+++

