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
source-git-commit: 73a347c104fe28799c264f9a8b6c3e5e12c8d892
workflow-type: ht
source-wordcount: '340'
ht-degree: 100%

---

# Commencer avec les messages WhatsApp {#get-started-whatsapp}

Vous pouvez désormais envoyer des messages WhatsApp directement par le biais de Journey Optimizer via l’API [Cloud](https://developers.facebook.com/docs/whatsapp/cloud-api/) de Meta. Cette fonctionnalité permet d’intégrer WhatsApp de manière transparente dans les parcours et les campagnes afin d’améliorer la communication et l’engagement des destinataires.

* Dans un **parcours**. Créez un parcours, ajoutez une activité **WhatsApp** et définissez les paramètres de base, puis accédez au volet de droite **[!UICONTROL Actions : WhatsApp]** pour créer le contenu du message WhatsApp. Découvrez comment créer un parcours sur [cette page](../building-journeys/journey-gs.md).

* Dans une **Campagne**. Créez une campagne, sélectionnez **WhatsApp** comme action et définissez les paramètres de base, puis modifiez le contenu du message WhatsApp à envoyer. Découvrez comment créer une [campagne d’action](../campaigns/campaign-action.md#action-campaign-action), une [campagne déclenchée par API](../campaigns/api-triggered-campaigns.md) ou une [campagne orchestrée](../orchestrated/create-orchestrated-campaign.md#create).

![](assets/do-not-localize/whatsapp-beta.png){zoomable="yes"}

## Prérequis {#prereq}

Pour intégrer WhatsApp à Journey Optimizer, vous avez besoin des éléments suivants :

* Compte Meta Business Manager
* [Compte professionnel WhatsApp avec nom d’expéditeur ou d’expéditrice et numéro de téléphone vérifiés](https://developers.facebook.com/docs/whatsapp/overview/business-accounts/)
* [Jeton d’autorisation utilisateur avec les autorisations appropriées](https://developers.facebook.com/blog/post/2022/12/05/auth-tokens/)
* [Modèles Meta approuvés](https://developers.facebook.com/docs/whatsapp/message-templates/guidelines/)

Vous devez également prendre connaissance des points suivants avant de procéder à l’intégration :

* [Règles de contenu WhatsApp](https://www.whatsapp.com/legal/messaging-guidelines)
* [Conformité aux politiques Meta](https://www.whatsapp.com/legal)
* [Limites de conversation sur une période de 24 heures](https://developers.facebook.com/docs/whatsapp/messaging-limits/)

## Limites {#limitations}

Les limites suivantes s’appliquent au canal WhatsApp :

* Le canal WhatsApp dans Adobe Journey Optimizer est conforme à la loi HIPAA, mais les fournisseurs tiers ne sont pas couverts par un accord de partenariat Adobe. Les clientes et les clients sont responsables de leur propre conformité et de la validation de leurs fournisseurs.

* Notez que les messages de réponse automatisés ou prédéfinis ne sont pas encore pris en charge.

* Depuis avril 2025, la diffusion de tous les messages de modèles marketing aux utilisateurs et aux utilisatrices de WhatsApp qui possèdent un numéro de téléphone aux États-Unis (numéro composé d’un indicatif +1 et d’un indicatif régional des États-Unis) a été temporairement suspendue. [En savoir plus dans la documentation de Meta](https://developers.facebook.com/docs/whatsapp/cloud-api/guides/send-message-templates#per-user-marketing-template-message-limits)

* La fonctionnalité d’intégration native ne permet pas l’intégration de prestataires de services professionnels (BSP) tiers.

## Vidéo pratique {#video}

La vidéo ci-dessous montre comment intégrer WhatsApp en tant que canal natif dans Adobe Journey Optimizer pour diffuser des messages sécurisés, personnalisés et en temps réel à grande échelle.

+++ Regarder la vidéo

>[!VIDEO](https://video.tv.adobe.com/v/3470246?captions=fre_fr&learn=on)

+++

## Ressources d’apprentissage supplémentaires

Explorez d&#39;autres tutoriels vidéo sur la messagerie et la configuration de WhatsApp.

➡️ [Tutoriels sur le canal WhatsApp](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/channels/whatsapp/whatsapp-introduction){target="_blank"}

