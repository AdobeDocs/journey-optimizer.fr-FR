---
title: Administration et paramètres
description: Découvrez les instructions relatives à l'administration et aux paramètres
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
translation-type: tm+mt
source-git-commit: c7c0c3921374265072d9f4ad117ddd5115dbe8e6
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 8%

---


# Prise en main

Lors de l’accès à Journey Optimizer pour la première fois, vous disposez d’un sandbox de production et d’un certain nombre d’adresses IP selon votre contrat.

Pour pouvoir créer vos parcours et envoyer des messages, vous devez suivre les étapes de configuration suivantes :

1. **Déléguer des sous-domaines**.

   Pour tout nouveau sous-domaine à utiliser dans Journey Optimizer, la première étape consiste à le déléguer. [En savoir plus](about-subdomain-delegation.md)

1. **Créez des pools d’adresses IP.**

   Améliorez la délivrabilité et la réputation de vos e-mails en regroupant les adresses IP configurées avec votre instance. [En savoir plus](ip-pools.md)

1. **Configurez les courriers électroniques et les messages** Push.

   1. Avant de commencer à envoyer des notifications Push avec [!DNL Journey Optimizer], vous devez définir les paramètres dans [!DNL Adobe Experience Platform] et [!DNL Adobe Experience Platform Launch]. [En savoir plus](../push-configuration.md)

   1. Créez des paramètres prédéfinis de message pour configurer tous les paramètres techniques requis pour les messages de notification par courrier électronique et par notification Push. [En savoir plus](message-presets.md)

   1. Déterminez quelle adresse électronique utiliser en priorité pour vos destinataires lorsque plusieurs adresses sont disponibles dans Adobe Experience Platform. [En savoir plus](primary-email-addresses.md)

   1. Gérez le nombre de jours pendant lesquels les Reprises sont exécutées avant d&#39;envoyer des adresses électroniques à la liste de suppression. [En savoir plus](get-started-quarantines.md)

1. **Configuration de parcours**.

   Pour créer des parcours, vous devez configurer **[!UICONTROL Sources de données]**, **[!UICONTROL Événements]** et **[!UICONTROL Actions]**. [En savoir plus](about-data-sources-events-actions.md)
