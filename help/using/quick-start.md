---
title: Démarrage rapide
description: Journey Optimizer - Démarrage rapide
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 71ab7369-fd84-46eb-95d2-941bd887d565
source-git-commit: 9c1edc8d79c58fcf4f2048b9fe81cd31ea621777
workflow-type: tm+mt
source-wordcount: '523'
ht-degree: 100%

---

# Démarrage rapide {#cjm-quick-start}

## Étapes clés pour débuter {#cjm-key-steps}

Avec [!DNL Adobe Journey Optimizer], vous pouvez importer du contenu de message existant ou concevoir un nouveau contenu, personnaliser les messages à l&#39;aide de données de profil client, créer des événements pour déclencher des messages, définir des segments et affiner les audiences, envoyer des messages multicanal, créer et ajouter des offres, et accéder à un ensemble complet d&#39;outils de reporting et de surveillance pour mesurer l&#39;impact de vos messages et de vos parcours client.

Selon votre organisation, vous pouvez définir plusieurs types d&#39;utilisateurs et leur accorder l&#39;accès à certaines fonctionnalités en fonction de leurs autorisations.

## Préparation et configuration de votre environnement

Avant de commencer à utiliser [!DNL Adobe Journey Optimizer], plusieurs étapes sont nécessaires pour préparer votre environnement.

En tant qu’administrateur système, vous devez **comprendre les profils de produit et attribuer des autorisations** pour l’administration des environnements sandbox et la configuration des canaux. Vous devez également configurer des environnements sandbox et les gérer pour les profils de produit disponibles.
Vous pourrez ensuite affecter des membres de l’équipe aux profils de produit et **définir la configuration du canal** pour la messagerie.

En savoir plus dans les pages suivantes :

* **Définissez des autorisations utilisateur** et accordez l&#39;accès aux membres de votre équipe. [En savoir plus](../using/administration/permissions.md)

* **Déployez[!DNL Adobe Experience Manager Assets Essentials]** pour gérer les ressources et les images dans vos messages : les utilisateurs qui ont besoin d’accéder à [!DNL Assets Essentials] doivent faire partie des profils de produit **Utilisateurs clients Assets Essentials** et/ou **Utilisateurs Assets Essentials**. [En savoir plus dans la documentation Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html?lang=fr){target=&quot;_blank&quot;}

* **Configurez vos canaux** : définissez les paramètres de vos e-mails et de vos notifications push. [En savoir plus](../using/configuration/get-started-configuration.md)

* **Définissez vos préréglages** et configurez vos paramètres de marque. [En savoir plus](../using/configuration/message-presets.md)

* **Gérez les environnements sandbox** pour partitionner votre instance en environnements virtuels séparés. [En savoir plus](../using/administration/sandboxes.md)


## Préparation des données et configuration des parcours

En tant qu’administrateur de données, vous devez **identifier les données et créer un schéma et un jeu de données** pour intégrer vos données dans Adobe Experience Platform.

Les étapes de création d’un espace de noms d’identité et d’un jeu de données activé pour les profils, la création de segments et de profils de test sont présentées dans les sections suivantes :

* Découvrez comment prévisualiser et créer un **jeu de données** dans la [documentation Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=fr){target=&quot;_blank&quot;}

* Découvrez comment créer un **espace de noms d&#39;identité** dans la [documentation Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=fr#manage-namespaces){target=&quot;_blank&quot;}

* Découvrez comment créer des **profils de test** dans [cette page](../using/building-journeys/creating-test-profiles.md)

* En savoir plus sur l’**ingestion de données** dans la [documentation Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/home.html?lang=fr){target=&quot;_blank&quot;}

* Découvrez comment **définir l’audience**, créer des segments, gérer le consentement et la confidentialité dans [cette page](../using/segment/about-segments.md)

En outre, pour pouvoir envoyer des messages dans des parcours, vous devez configurer les **[!UICONTROL sources de données]**, les **[!UICONTROL événements]** et les **[!UICONTROL actions]**. En savoir plus dans [cette section](../using/configuration/about-data-sources-events-actions.md)

## Création de messages, d’offres et de parcours

En tant que gestionnaire de parcours, reportez-vous aux sections suivantes pour configurer votre premier parcours, ajouter des offres et des ressources et envoyer des messages :

* **Créer des messages** : accédez aux messages, concevez ou chargez du contenu d&#39;email et push, ajoutez des messages de personnalisation et de prévisualisation. [En savoir plus](create-message.md)

* **Télécharger des ressources** : utilisez Adobe Experience Manager Assets Essentials pour gérer les ressources et les images. [En savoir plus](assets-essentials.md)

* **Ajouter des offres** : utilisez Journey Optimizer Decision Management pour ajouter des offres personnalisées dans vos messages. [En savoir plus](../using/offers/get-started/starting-offer-decisioning.md)

* **Créer des parcours** : envoyez des messages, utilisez des données contextuelles, affinez les audiences, concevez et exécutez des cas d&#39;utilisation à plusieurs étapes. [En savoir plus](building-journeys/journey.md)

* **Surveiller les messages et les parcours** : contrôlez l&#39;exécution des messages, vérifiez les rapports de message et de parcours, et assurez le suivi des mesures de délivrabilité. [En savoir plus](message-monitoring.md)
