---
title: Créer un message web in-app dans Journey Optimizer
description: Découvrez comment créer un message web in-app dans Journey Optimizer
feature: In App
topic: Content Management
role: User
level: Beginner
keywords: in-app, message, création, commencer
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: ht
source-wordcount: '408'
ht-degree: 100%

---


# Configurer le canal web in-app {#configure-in-app-web}

## Conditions préalables {#prerequisites}

* Assurez-vous d’utiliser la dernière version pour votre extension **SDK Web Adobe Experience Platform**.

* Installez l’extension **SDK Web Adobe Experience Platform** dans vos **Propriétés de balise** et activez l’option **Stockage de personnalisation**.

  Cette configuration est essentielle pour le stockage des historiques d’événements sur le client, condition préalable à l’implémentation des règles de fréquence dans le créateur de règles. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/tags/extensions/client/web-sdk/web-sdk-extension-configuration.html?lang=fr)

  ![](assets/configure_web_inapp_1.png)

## Configurer la règle Envoi de données à Platform {#configure-sent-data-trigger}

1. Accédez à votre instance de **collecte de données dʼAdobe Experience Platform** et aux **Propriétés de balise** configurées à l’aide de l’extension **SDK Web Adobe Experience Platform**.

1. Dans le menu **Création**, sélectionnez **Règles** puis **Créer une règle** ou **Ajouter une règle**.

   ![](assets/configure_web_inapp_2.png)

1. Dans la section **Événements**, cliquez sur **Ajouter** et configurez comme suit :

   * **Extension** : Core

   * **Type d’événement** : bibliothèque chargée (Haut de la page)

   ![](assets/configure_web_inapp_3.png)

1. Cliquez sur **Conserver les modifications** pour enregistrer la configuration d’événement.

1. Dans la section **Actions**, cliquez sur **Ajouter** et configurez comme suit :

   * **Extension** : SDK Web Adobe Experience Platform

   * **Type d’action** : envoyer un événement

   ![](assets/configure_web_inapp_4.png)

1. Dans la section **Personnalisation** de votre type **Action**, activez l’option **Rendu visuel des décisions de personnalisation**.

   ![](assets/configure_web_inapp_5.png)

1. Dans la section **Contexte de décision**, définissez les paires **Clé** et **Valeur** qui déterminent l’expérience à diffuser.

   ![](assets/configure_web_inapp_6.png)

1. Enregistrez la configuration de votre **Action** en cliquant sur **Conserver les modifications**.

1. Accédez au menu **Flux de publication**. Créez une **Bibliothèque** ou sélectionnez un **Bibliothèque** existante et ajoutez la **Règle** nouvellement créée à celle-ci. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=fr#create-a-library)

1. Dans votre **Bibliothèque**, sélectionnez **Enregistrer et créer pour le développement**.

   ![](assets/configure_web_inapp_7.png)

## Configurer une règle manuelle {#configure-manual-trigger}

1. Accédez à votre instance de **collecte de données d’Adobe Experience Platform** et aux **Propriétés de balise** configurées à l’aide de l’extension **SDK Web Adobe Experience Platform**.

1. Dans le menu **Création**, sélectionnez **Règles** puis **Créer une règle** ou **Ajouter une règle**.

   ![](assets/configure_web_inapp_8.png)

1. Dans la section **Événements**, cliquez sur **Ajouter** et configurez comme suit :

   * **Extension** : Core

   * **Type d’événement** : clic

   ![](assets/configure_web_inapp_9.png)

1. Dans **Configuration des clics**, définissez le **Sélecteur** qui sera évalué.

   ![](assets/configure_web_inapp_10.png)

1. Cliquez sur **Conserver les modifications** pour enregistrer la configuration d’**Événement**.

1. Dans la section **Actions**, cliquez sur **Ajouter** et configurez comme suit :

   * **Extension** : SDK Web Adobe Experience Platform

   * **Type d’action** : évaluation des jeux de règles

   ![](assets/configure_web_inapp_11.png)

1. Dans la section de l’**action Évaluation des jeux de règles** de votre type d’**Action**, activez l’option **Rendu visuel des décisions de personnalisation**.

   ![](assets/configure_web_inapp_13.png)

1. Dans la section **Contexte des décisions**, définissez les paires **Clé** et **Valeur** qui déterminent l’expérience à diffuser.

1. Accédez au menu **Flux de publication**, créez une **Bibliothèque** ou sélectionnez une **Bibliothèque** existante et ajoutez la **Règle** nouvellement créée. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/tags/publish/libraries.html?lang=fr#create-a-library)

1. Dans votre **Bibliothèque**, sélectionnez **Enregistrer et créer pour le développement**.

   ![](assets/configure_web_inapp_14.png)

