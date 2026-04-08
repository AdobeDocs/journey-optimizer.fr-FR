---
title: Création d’une boîte de réception
description: Commencez avec la boîte de réception dans Adobe Journey Optimizer pour diffuser des messages persistants et non intrusifs à vos utilisateurs.
feature: Content Cards
topic: Content Management
role: User
level: Beginner
exl-id: 60190d0b-d8e7-4a78-9924-d948f2769f6c
source-git-commit: 2eb2e99e654516fc13a7f98125f48e7e8f672ee3
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 0%

---

# Prise en main de la boîte de réception {#inbox-gs}

La boîte de réception diffuse des messages persistants et à faible friction au même endroit dans votre application mobile ou votre site web. In-app et push peuvent disparaître après un balayage ou une pression ; la boîte de réception garde les messages disponibles afin que les utilisateurs puissent les ouvrir, les lire et agir sur eux quand cela leur convient.

La boîte de réception s’appuie sur le canal Cartes de contenu et ajoute :

* **Messages persistants** : le contenu reste dans la boîte de réception jusqu’à ce que vous le supprimiez ou qu’il expire, afin que les utilisateurs puissent y revenir après avoir fermé une notification ou quitté l’application.
* **Emplacement centralisé** : une boîte aux lettres unique dans votre application ou site pour les messages marketing pertinents.
* **Implémentation flexible** : utilisez le conteneur de boîte de réception prêt à l’emploi ou personnalisez l’expérience dans votre propre interface utilisateur.
* **Read-Status** : les messages peuvent être marqués comme lus ou non lus sur l&#39;appareil sur lequel ils sont ouverts.

## Guide de démarrage rapide

Pour configurer et utiliser la boîte de réception, procédez comme suit :

1. [Configuration de Adobe Journey Optimizer](inbox-configuration.md)

   Ajoutez une configuration de canal **Boîte de réception** sous **Configurations de canal** afin que Journey Optimizer sache où et comment la boîte de réception s’exécute (page web ou règle, ou surface d’application mobile).

1. [Création de votre boîte de réception dans Journey Optimizer](inbox-create.md)

   Créez une campagne qui utilise l’action **Carte de contenu** et choisissez **Boîte de réception** comme emplacement de diffusion, planifié à partir de l’interface utilisateur ou déclenché par l’API.

1. [Concevoir votre boîte de réception](inbox-design.md)

   Choisissez des modèles de boîte de réception et répertoriez ou étendez les mises en page pour que les messages correspondent à votre marque et à votre expérience utilisateur.

1. [Créez votre carte Contenu et liez-la à votre boîte de réception](../content-card/create-content-card.md)

   Créez le contenu de la carte dans le concepteur, terminez les options spécifiques à la boîte de réception, puis activez votre campagne pour que les messages atteignent la boîte de réception.

## Ressources supplémentaires

* [Récupérer et afficher la boîte de réception](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/displaying-inbox/) : chargement des messages de la boîte de réception Journey Optimizer et rendu de l’interface utilisateur de la boîte de réception sur Android (documentation Adobe Developer).
* [Personnalisation de la boîte de réception](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/customizing-inbox/) : ajustez la disposition, le style et le comportement de l’interaction de la boîte de réception pour votre application Android (documentation Adobe Developer).
* [Écoute des événements de boîte de réception](https://developer.adobe.com/client-sdks/edge/adobe-journey-optimizer/inbox-ui/Android/tutorial/listening-inbox-events/) : abonnez-vous aux rappels de boîte de réception pour les actions des utilisateurs et les mises à jour de cycle de vie sur Android (documentation Adobe Developer).
