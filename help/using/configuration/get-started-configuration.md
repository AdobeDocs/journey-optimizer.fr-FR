---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main d’ [!DNL Journey Optimizer] configuration
description: En savoir plus sur [!DNL Journey Optimizer] configuration
role: Admin
level: Intermediate
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
source-git-commit: c6498633fdfdc9442203a3bf980f1b12bd1c6a6b
workflow-type: tm+mt
source-wordcount: '377'
ht-degree: 0%

---


# Prise en main d’ [!DNL Journey Optimizer] configuration {#start-optimizer-configuration}

Lors de l’accès à [!DNL Journey Optimizer] pour la première fois, un environnement de test de production vous est attribué et un certain nombre d’adresses IP vous est attribué selon votre contrat.

Pour pouvoir créer vos parcours et envoyer des messages, vous devez suivre les étapes de configuration ci-dessous.

## Configuration des messages et des canaux

1. Pour pouvoir créer et envoyer des messages, vous devez effectuer des paramétrages spécifiques en fonction du canal.

   * Pour le **Email** canal, vous devez déléguer des sous-domaines à Adobe et créer des pools d’adresses IP pour regrouper les adresses IP. [En savoir plus](../email/get-started-email-config.md)

   * Pour le **Push** canal, vous devez définir les paramètres des notifications push dans les deux [!DNL Adobe Experience Platform] et [!DNL Adobe Experience Platform Launch]. [En savoir plus](../push/push-configuration.md)

   * Pour le **SMS** , vous devez configurer votre instance pour envoyer des SMS, y compris en intégrant les paramètres du fournisseur à [!DNL Journey Optimizer]. [En savoir plus](../sms/sms-configuration.md)

1. Une fois cette opération terminée, vous devez créer **surfaces des canaux** pour configurer tous les paramètres techniques requis pour diffuser les messages. [En savoir plus](channel-surfaces.md)

1. Vous pouvez également :

   * Gérez le nombre de jours pendant lesquels des reprises sont effectuées avant d’envoyer des adresses électroniques à la liste de suppression. [En savoir plus](manage-suppression-list.md)

   * Activez la variable **Option d’email BBC** pour conserver une copie des messages envoyés aux individus. [En savoir plus](archiving-support.md#enable-bcc)

   * Configurer **règles de fréquence** pour éviter de sur-solliciter vos destinataires. [En savoir plus](frequency-rules.md)

   * Déterminez l’adresse électronique et/ou le numéro de téléphone à utiliser en priorité pour vos destinataires lorsque plusieurs adresses/numéros sont disponibles dans Adobe Experience Platform. [En savoir plus](primary-email-addresses.md)

<!--* Understand the push notification flow. [Learn more](../push/push-gs.md)-->

>[!NOTE]
>
>Ces étapes doivent être exécutées par une [Administrateur système Adobe Journey Optimizer](../start/path/administrator.md).

## Configuration des parcours

Pour créer des parcours, vous devez configurer **[!UICONTROL Data Sources]**, **[!UICONTROL Events]** et **[!UICONTROL Actions]**. [En savoir plus](about-data-sources-events-actions.md)

![](assets/admin-menu.png)

* Le **source de données** La configuration vous permet de définir une connexion à un système afin de récupérer des informations supplémentaires qui seront utilisées dans vos parcours. [En savoir plus](../datasource/about-data-sources.md)

* **Événements** vous permettent de déclencher vos parcours de manière unitaire pour envoyer des messages, en temps réel, à l’individu qui participe au parcours. Dans la configuration des événements, vous configurez les événements prévus dans les parcours. Les données des événements entrants sont normalisées conformément au modèle de données d’expérience Adobe (XDM). Les événements proviennent des API d’ingestion en flux continu pour les événements authentifiés et non authentifiés (tels que les événements du SDK Adobe Mobile). [En savoir plus](../event/about-events.md)

* [!DNL Journey Optimizer] est fourni avec des fonctionnalités de message intégrées qui vous permettent de concevoir et d’envoyer votre contenu. Si vous utilisez un système tiers pour envoyer vos messages, créez une **action personnalisée**. [En savoir plus](../action/action.md)