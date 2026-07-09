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
TQID: https://experienceleague.adobe.com/uHzRC9X6rB9EXH4gIFiRxFaeNcrTD0-40RrxZkN4XFg
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b8df23d2-98a2-4406-86cc-2babe8728d36id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 75ebd043971ce40e2da0f627622441a46a8e667c
workflow-type: tm+mt
source-wordcount: 686
ht-degree: 65%

---

# Commencer avec les messages WhatsApp {#get-started-whatsapp}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez le fonctionnement du canal WhatsApp dans Journey Optimizer, ainsi que ses conditions requises et ses limitations, afin de pouvoir décider comment ajouter WhatsApp à vos parcours et vos campagnes.

>[!ENDSHADEBOX]

Vous pouvez désormais envoyer des messages WhatsApp directement par le biais de Journey Optimizer via l’API [Cloud](https://developers.facebook.com/docs/whatsapp/cloud-api/) de Meta. Cette fonctionnalité permet d’intégrer WhatsApp de manière transparente dans les parcours et les campagnes afin d’améliorer la communication et l’engagement des destinataires.

* Dans un **parcours**. Créez un parcours, ajoutez une activité **WhatsApp** et définissez les paramètres de base, puis accédez au volet de droite **[!UICONTROL Actions : WhatsApp]** pour créer le contenu du message WhatsApp. Découvrez comment créer un parcours sur [cette page](../building-journeys/journey-gs.md).

* Dans une **campagne**. Créez une campagne, sélectionnez **WhatsApp** comme action et définissez les paramètres de base, puis modifiez le contenu du message WhatsApp à envoyer. Découvrez comment créer une [campagne d’action](../campaigns/campaign-action.md#action-campaign-action), une [campagne déclenchée par API](../campaigns/api-triggered-campaigns.md) ou une [campagne orchestrée](../orchestrated/create-orchestrated-campaign.md#create).

![](assets/do-not-localize/whatsapp-beta.png){zoomable="yes"}

## Cas d’utilisation {#use-cases}

WhatsApp fonctionne mieux lorsque votre audience utilise déjà la plateforme et que vous souhaitez combiner du contenu riche avec une conversation réellement bidirectionnelle.

| Avantage | Pourquoi | Exemples de cas d’utilisation |
| --- | --- | --- |
| Engagement mondial élevé | Plateforme de messagerie largement utilisée et largement adoptée dans de nombreuses régions | Atteindre les audiences internationales déjà actives sur WhatsApp |
| Messages riches et interactifs | Prend en charge les images, vidéos, boutons et réponses rapides | Catalogues de produits, confirmations de rendez-vous avec options de réponse rapide |
| Expériences de conversation bidirectionnelles | Les destinataires peuvent répondre dans le même thread | Conversations avec le service clientèle, questions sur le suivi des commandes |
| Conformité et confiance via l’API officielle | Distribué via l’API Cloud vérifiée de Meta avec vérification de l’expéditeur | Communications vérifiées par la marque qui établissent la confiance des destinataires |
| Intégration à d’autres canaux | Peut être superposé à des parcours et des campagnes avec d’autres canaux. | Parcours multicanaux utilisant WhatsApp comme point de contact complémentaire |

## Quand ne pas utiliser {#when-not-to-use}

WhatsApp dépend de l&#39;adoption de l&#39;audience et du consentement explicite, donc il n&#39;est pas adapté à tous les scénarios. Prenons un autre canal dans les situations suivantes :

* Votre audience n&#39;utilise pas WhatsApp, car l&#39;adoption varie considérablement selon la région et la démographie
* Les destinataires n’ont pas donné d’accord préalable explicite, ce qui est requis par les politiques de messagerie de Meta
* Le message est urgent et nécessite une diffusion garantie, que les SMS ou les notifications push gèrent mieux compte tenu des contraintes de diffusion et de révision des modèles de WhatsApp
* Le contenu est long ou complexe et mieux adapté aux e-mails, qui offrent plus d’espace et une mise en forme plus riche
* Le support conversationnel en temps réel n&#39;est pas réalisable de votre côté, car les threads WhatsApp bidirectionnels définissent une attente de réponse en temps opportun

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

>[!VIDEO](https://video.tv.adobe.com/v/3470244?learn=on)

+++

## Ressources d’apprentissage supplémentaires

Explorez d&#39;autres tutoriels vidéo sur la messagerie et la configuration de WhatsApp.

➡️ [Tutoriels sur le canal WhatsApp](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/channels/whatsapp/whatsapp-introduction){target="_blank"}

