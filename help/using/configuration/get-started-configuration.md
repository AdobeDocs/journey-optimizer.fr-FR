---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main de la configuration  [!DNL Journey Optimizer]  canaux
description: En savoir plus sur la configuration  [!DNL Journey Optimizer]  canaux .
role: Admin, Developer
level: Intermediate, Experienced
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
keywords: configuration, configurer, messages, canal, sandbox, optimizer
source-git-commit: ca6f551f7dd85a749ba8fe39ba7654da3c3d6804
workflow-type: tm+mt
source-wordcount: '252'
ht-degree: 61%

---


# Prise en main de la configuration des canaux {#start-optimizer-configuration}

Lorsque vous accédez à [!DNL Journey Optimizer] pour la première fois, un sandbox de production vous est alloué ainsi qu’un certain nombre d’adresses IP en fonction de votre contrat.


Pour pouvoir envoyer des messages, vous devez suivre les étapes de configuration répertoriées ci-dessous.

>[!NOTE]
>
>* Ces étapes doivent être exécutées par un [Administrateur système Adobe Journey Optimizer](../start/path/administrator.md).
>
>* Pour les canaux mobiles, la [configuration guidée de canal](set-mobile-config.md) facilite la configuration rapide des canaux marketing, en veillant à ce que toutes les ressources requises soient facilement disponibles dans Experience Platform, Journey Optimizer et la collecte de données. Cela permet à votre équipe marketing de lancer la création de campagnes et de parcours.


1. Définissez et testez des configurations spécifiques en fonction du canal. Découvrez comment configurer ces configurations dans les pages suivantes :

   * [Configuration du canal e-mail](../email/get-started-email-config.md)
   * [Configuration du canal push](../push/push-configuration.md)
   * [Configuration du canal SMS](../sms/sms-configuration.md)
   * [Configuration du publipostage direct](../direct-mail/direct-mail-configuration.md)
   * [Configuration du canal web](../web/web-configuration.md)
   * [Configuration des expériences basées sur du code](../code-based/code-based-configuration.md)
   * [Configuration des cartes de contenu](../content-card/content-card-configuration-prereq.md)


1. Une fois cette opération terminée, vous devez créer des **configurations de canal** pour configurer tous les paramètres techniques requis pour diffuser les messages. [En savoir plus sur les configurations de canal](channel-surfaces.md)

1. Vous pouvez également réaliser les opérations suivantes :

   * Gérez le nombre de jours pendant lesquels de nouvelles tentatives sont effectuées avant d&#39;envoyer des adresses électroniques à la liste de suppression. [En savoir plus](manage-suppression-list.md)

   * Activez l’**option d’e-mail Cci** pour conserver une copie des messages envoyés aux individus. [En savoir plus](archiving-support.md#enable-bcc)

   * Configurez les **règles métier** pour éviter de sur-solliciter vos destinataires. [En savoir plus](../configuration/rule-sets.md)

   * Déterminez l’adresse e-mail et/ou le numéro de téléphone à utiliser en priorité pour vos destinataires lorsque plusieurs adresses/numéros sont disponibles dans Adobe Experience Platform. [En savoir plus](primary-email-addresses.md)
