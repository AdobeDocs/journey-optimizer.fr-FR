---
title: Créer une boîte de réception
description: Commencez avec la boîte de réception dans Adobe Journey Optimizer pour diffuser des messages persistants et non intrusifs à vos utilisateurs et utilisatrices.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
exl-id: 60190d0b-d8e7-4a78-9924-d948f2769f6c
source-git-commit: c2bb6cf702a14b4eef8f2209082e39cd73338378
workflow-type: tm+mt
source-wordcount: '453'
ht-degree: 92%

---

# Commencer avec la boîte de réception {#inbox-gs}

>[!BEGINSHADEBOX]

**Sur cette page :** comprenez comment le canal de la boîte de réception maintient les messages marketing à un emplacement persistant dans votre application ou site web, afin que les utilisateurs puissent revenir pour les lire et agir sur eux à leur convenance.

>[!ENDSHADEBOX]

La boîte de réception diffuse des messages persistants et à faible friction en un seul endroit dans votre application mobile ou votre site web. Les messages in-app et push peuvent disparaître après un balayage ou une pression. La boîte de réception garde les messages disponibles afin que les utilisateurs et utilisatrices puissent les ouvrir, les lire et interagir avec eux quand cela leur convient.

La boîte de réception s’appuie sur le canal Cartes de contenu et ajoute ce qui suit :

* **Messages persistants** : le contenu reste dans la boîte de réception jusqu’à ce que vous le supprimiez ou qu’il expire, afin que les utilisateurs et utilisatrices puissent y revenir après avoir fermé une notification ou quitté l’application.
* **Emplacement centralisé** : une boîte aux lettres unique dans votre application ou site pour les messages marketing pertinents.
* **Mise en œuvre flexible** : utilisez le conteneur de boîte de réception prêt à l’emploi ou personnalisez l’expérience dans votre propre interface d’utilisation.
* **Statut de lecture** : les messages peuvent être marqués comme lus ou non lus sur l’appareil sur lequel ils sont ouverts.

## Guide de démarrage rapide

Pour configurer et utiliser la boîte de réception, procédez comme suit :

1. [Configurer Adobe Journey Optimizer](inbox-configuration.md)

   Ajoutez une configuration des canaux **Boîte de réception** sous **Configurations des canaux** afin que Journey Optimizer sache où et comment la boîte de réception s’exécute (page web ou règle, ou surface d’application mobile).

1. [Créer votre boîte de réception dans Journey Optimizer](inbox-create.md)

   Créez une campagne qui utilise l’action **Carte de contenu** et choisissez **Boîte de réception** comme emplacement de diffusion, avec une planification à partir de l’interface d’utilisation ou un déclenchement par API.

1. [Concevoir votre boîte de réception](inbox-design.md)

   Choisissez des modèles de boîte de réception et des mises en page étendues ou sous forme de liste pour que les messages correspondent à votre marque et à votre expérience d’utilisation.

1. [Créer votre carte de contenu et la lier à votre boîte de réception](../content-card/create-content-card.md)

   Créez le contenu de la carte dans le concepteur, définissez les options spécifiques à la boîte de réception, puis activez votre campagne pour que les messages atteignent la boîte de réception.

## Ressources supplémentaires

* [Interface d’utilisation de la boîte de réception (iOS)](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/iOS) : exigences, surface d’API publique, paramètres de la boîte de réception et liens vers des tutoriels pour la mise en œuvre de la boîte de réception Journey Optimizer dans une application iOS avec le SDK mobile Adobe Experience Platform (iOS 15 ou version ultérieure, Xcode 15 ou version ultérieure, Swift 5.1 ou version ultérieure).

* [Récupérer et afficher la boîte de réception](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/displaying-inbox) : chargez des messages de la boîte de réception Journey Optimizer et effectuez le rendu de l’interface d’utilisation de la boîte de réception sur Android (documentation Adobe Developer).

* [Personnaliser la boîte de réception](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/customizing-inbox) : ajustez la disposition, le style et le comportement de l’interaction de la boîte de réception pour votre application Android (documentation Adobe Developer).

* [Écouter des événements de boîte de réception](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/listening-inbox-events) : abonnez-vous aux rappels de boîte de réception pour les actions des utilisateurs et utilisatrices, et les mises à jour de cycle de vie sur Android (documentation Adobe Developer).
