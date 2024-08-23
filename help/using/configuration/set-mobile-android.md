---
solution: Journey Optimizer
product: journey optimizer
title: Configuration d’Android Mobile
description: Découvrez comment configurer et surveiller les canaux mobiles Android
feature: Surface, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: canal, surface, technique, paramètres, optimizer
hide: true
hidefromtoc: true
source-git-commit: 8fb87d2e2085d98dd8b014df6aa4d734bab4e997
workflow-type: tm+mt
source-wordcount: '937'
ht-degree: 6%

---

# Configuration de la configuration mobile Android {#set-mobile-android}

>[!IMPORTANT]
>
>Pour garantir la compatibilité et des performances optimales, veillez à utiliser les versions suivantes du SDK :
>
> * Core 3.1.0 ou version ultérieure
> * Messagerie 3.1.0 ou ultérieure

Cette configuration d’Android simplifie la configuration rapide des canaux marketing, en veillant à ce que toutes les ressources nécessaires soient facilement accessibles dans les applications Experience Platform, Journey Optimizer et Data Collection. Cela permet à votre équipe marketing de commencer rapidement à créer des campagnes et des parcours.

## Création d’une configuration Android {#new-setup-android}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_android_initialization_code"
>title="Ajouter un code d’initialisation"
>abstract="TBC"

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_android_dependencies_add"
>title="Ajouter des dépendances"
>abstract="Vous devez ajouter les bibliothèques suivantes à votre projet à l’aide du fichier Gradle de l’application : Core, Assurance, Edge, Edge Identity et Messaging."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_android_dependencies_import"
>title="Importer les dépendances"
>abstract="Dans la classe Application de votre application, importez les modules suivants : Mobile Core, Assurance, Edge, Edge Identity et Messaging."
>additional-url="https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/install-sdks#import-extensions" text="Voir la documentation sur la collecte de données"

<!--
>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_push_token_android"
>title="Retrieve the device token"
>abstract="TBC"

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_push_android_studio"
>title="Launch the application from Android Studio"
>abstract="TBC"
-->

1. Sur la page d’accueil de Journey Optimizer, cliquez sur **[!UICONTROL Commencer]** dans la carte **[!UICONTROL Configurer les canaux mobiles et web]**.

   ![](assets/guided-setup-config-1.png)

1. Créez une configuration **[!UICONTROL New]**.

   Si vous disposez déjà de configurations, vous pouvez en sélectionner une ou en créer une nouvelle.

   ![](assets/guided-setup-config-2.png)

1. Saisissez un **[!UICONTROL Nom]** pour votre nouvelle configuration et sélectionnez ou créez votre **[!UICONTROL Datastream]**. Ce **[!UICONTROL nom]** sera utilisé pour toutes les ressources créées automatiquement.

1. Si votre entreprise dispose de plusieurs jeux de données, sélectionnez-en un parmi les options existantes. Si vous ne disposez pas d’un flux de données, celui-ci sera créé automatiquement.

1. Sélectionnez la plateforme Android que vous souhaitez configurer et cliquez sur **[!UICONTROL Créer automatiquement les ressources]**.

   ![](assets/guided-setup-config-4.png)

1. Pour simplifier le processus de configuration, les ressources nécessaires sont automatiquement créées pour vous aider à démarrer. Cela inclut la création d’une **[!UICONTROL propriété de balise mobile]** et l’installation d’extensions.

   Vous trouverez ci-dessous une liste complète de toutes les ressources générées automatiquement :

+++ Ressources créées

   <table>
    <thead>
    <tr>
    <th><strong>Solution</strong></th>
    <th><strong>Ressources créées automatiquement</strong></th>
    </tr>
    </thead>
    <tbody>
    <tr>
    <td>
    <p>Journey Optimizer</p>
    </td>
    <td>
    <ul>
    <li>Configuration de canal</li>
    <li>Informations d’identification push (message push mobile uniquement)</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>
    <p>Balises</p>
    </td>
    <td>
    <ul>
    <li>Propriété de balise mobile</li>
    <li>Règles</li>
    <li>Éléments de données</li>
    <li>Bibliothèque</li>
    <li>Environnements (évaluation, production, développement)</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>
    <p>Extensions de balises</p>
    </td>
    <td>
    <ul>
    <li>Adobe Experience Platform Edge Network</li>
    <li>Adobe Journey Optimizer</li>
    <li>Assurance AEP</li>
    <li>Consentement (avec activation des stratégies de consentement par défaut)</li>
    <li>Identité (avec ECID par défaut, avec règles de groupement par défaut)</li>
    <li>Mobile Core</li>
    </ul>
    </td>
    </tr>
    <tr>
    <td>
    <p>Assurance</p>
    </td>
    <td>
    <p>Session d’assurance</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Trains de données</p>
    </td>
    <td>
    <p>Flux de données avec services</p>
    </td>
    </tr>
    <tr>
    <td>
    <p>Experience Platform</p>
    </td>
    <td>
    <ul>
    <li>Jeu de données</li>
    <li>Schéma</li>
    </ul>
    </td>
    </tr>
    </tbody>
    </table>

+++

1. Une fois la génération des ressources terminée, cliquez sur **[!UICONTROL Configurer]** pour commencer à configurer votre SDK.

   ![](assets/guided-setup-config-android-1.png)

1. Vous devez d’abord ajouter et importer des dépendances comme décrit dans l’interface utilisateur. [En savoir plus](https://experienceleague.adobe.com/en/docs/platform-learn/implement-mobile-sdk/app-implementation/install-sdks).

1. Copiez-collez le code suivant dans la méthode onCreate() de votre application.

1. Pour valider directement votre SDK sur votre application mobile, ouvrez simplement votre application mobile et autorisez l’accès à [Adobe Assurance](https://experienceleague.adobe.com/en/docs/experience-platform/assurance/home). Assurance est un outil puissant qui vous permet de tester et valider minutieusement votre mise en oeuvre, en veillant à ce que tout fonctionne correctement.

   Une fois connecté, votre appareil sera automatiquement détecté et répertorié dans le menu déroulant **[!UICONTROL Périphérique disponible]**, ce qui vous permet de surveiller et de résoudre en temps réel vos problèmes de configuration.

   ![](assets/guided-setup-config-android-2.png)

1. Cliquez sur **[!UICONTROL Connect]**.

1. Vous pouvez maintenant configurer vos canaux [In-App](#inapp-channel) et/ou [Push](#push-channel).

1. Une fois la configuration terminée, partagez la **[!UICONTROL configuration de canal]** générée automatiquement avec les membres de l’équipe chargés de la création des Parcours et des campagnes.

   La **[!UICONTROL configuration de canal]** doit être référencée dans l’interface Campagnes ou Parcours, ce qui permet une connexion transparente entre votre configuration et l’exécution des parcours et campagnes ciblés pour votre audience.

   ![](assets/guided-setup-config-ios-8.png)

## Modifier une configuration existante {#reconnect}

Après avoir créé votre configuration, vous pouvez facilement la revoir à tout moment pour ajouter des canaux supplémentaires ou effectuer d’autres réglages en fonction de vos besoins.

1. Sur la page d’accueil de Journey Optimizer, cliquez sur **[!UICONTROL Commencer]** dans la carte **[!UICONTROL Configurer les canaux mobiles et web]**.

   ![](assets/guided-setup-config-1.png)

1. Sélectionnez **[!UICONTROL Existant]** et choisissez votre **[!UICONTROL propriété de balise]** existante dans la liste déroulante.

   ![](assets/guided-setup-config-6.png)

1. Lors de l’accès à votre configuration existante, vous devez vous reconnecter à Adobe Assurance. Dans le menu Configuration du SDK, cliquez sur **[!UICONTROL Reconnecter]**.

1. Sélectionnez votre appareil dans la liste déroulante **[!UICONTROL Appareils disponibles]** et cliquez sur **[!UICONTROL Se connecter]**.

1. Vous pouvez maintenant mettre à jour votre configuration si nécessaire.

## Configuration de la chaîne In-App {#inapp-channel}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_inapp_tag_property"
>title="Choisir votre propriété de balise"
>abstract="TBC"

Le canal In-App ne nécessite aucune configuration supplémentaire. Pour vérifier la précision de votre configuration, vous pouvez envoyer facilement un message de test à l’aide de la fonction Assurance. Cela vous permettra d’obtenir des commentaires immédiats sur la disponibilité du système à diffuser efficacement les messages In-App.

Pour ce faire, cliquez simplement sur **[!UICONTROL Afficher le message in-app]**.

Pour simplifier le processus de configuration, les ressources nécessaires sont automatiquement créées pour vous aider à démarrer. Cela inclut la création d’une configuration de canal.

Vous pouvez désormais envoyer des messages In-App à l’aide de la **[!UICONTROL configuration de canal]** configurée précédemment. [Découvrez comment créer des messages in-app](../in-app/create-in-app.md)

## Configuration du canal push {#push-channel}

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_push_token"
>title="Récupérer le jeton d’appareil"
>abstract="Pour vous assurer que le jeton push du périphérique est correctement synchronisé avec votre profil Adobe Experience Platform, vous devez incorporer le code suivant dans votre application. Cette intégration est essentielle pour maintenir des fonctionnalités de communication à jour et garantir une expérience utilisateur transparente."

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_setup_push_xcode"
>title="Lancer l’application à partir de Xcode"
>abstract="TBC"

>[!CONTEXTUALHELP]
>id="ajo_mobile_web_push_certificate_fcm"
>title="Fournir un certificat push"
>abstract="Glissez-déposez votre fichier de clé privée .json . Ce fichier contient les informations d’authentification requises pour l’intégration et la communication sécurisées entre votre application et le serveur."

1. Une fois votre SDK mobile configuré, cliquez sur **[!UICONTROL Ajouter]** depuis la carte de notification push.

1. Récupérez le jeton de périphérique en insérant le code fourni dans la fonction de rappel `FireBaseMessaging.getInstance.getToken ()` de l’interface utilisateur.

1. Enregistrez le service de messagerie en ajoutant le code fourni dans l’interface utilisateur à votre fichier `AndroidManifest.xml`.

1. Glissez-déposez votre fichier de clé privée .json .

1. Pour vérifier la précision de votre configuration, vous pouvez envoyer facilement un message de test à l’aide de la fonction Assurance. Cela vous permettra d’obtenir des commentaires immédiats sur la préparation du système à diffuser efficacement les notifications push.

   Pour ce faire, cliquez simplement sur **[!UICONTROL Envoyer un message push]**.

Pour simplifier le processus de configuration, les ressources nécessaires sont automatiquement créées pour vous aider à démarrer. Cela inclut la création d’une **[!UICONTROL configuration de canal]** et d’ **[!UICONTROL informations d’identification push]**.

Vous pouvez maintenant envoyer des notifications push à l’aide de la **[!UICONTROL configuration de canal]** configurée précédemment. [Découvrez comment créer une notification push](../push/create-push.md)
