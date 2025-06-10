---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main de la configuration  [!DNL Journey Optimizer]  canaux
description: 'En savoir plus sur la configuration des canaux [!DNL Journey Optimizer] '
role: Admin, Developer
level: Intermediate, Experienced
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
keywords: configuration, configurer, messages, canal, sandbox, optimizer
source-git-commit: 6109c9176c160c2c0b1eafa06b855ebaf285e3ee
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 71%

---


# Commencer la configuration des canaux {#start-optimizer-configuration}

Lors de l&#39;accès à [!DNL Journey Optimizer] pour la première fois, vous recevez un sandbox de production et un certain nombre d’adresses IP vous sont attribuées en fonction de votre contrat.


Pour envoyer des messages, vous devez suivre les étapes de configuration suivantes :

1. En tant qu’administrateur système de [Adobe Journey Optimizer](../start/path/administrator.md), définissez vos configurations spécifiques à un canal. Découvrez comment effectuer ces configurations dans les pages suivantes :

   <table style="table-layout:fixed"><tr style="border: 0;">
    <td><a href="../email/get-started-email-config.md"><img alt="E-mail" src="../channels/assets/do-not-localize/email.png"></a>
    <div align="center"><a href="../email/get-started-email-config.md"><strong>E-mail</strong></a></div></td>
    <td><a href="../sms/sms-configuration.md"><img alt="SMS" src="../channels/assets/do-not-localize/sms.png"></a>
    <div align="center"><a href="../sms/sms-configuration.md"><strong>SMS</strong></a></div></td>
    <td><a href="../push/push-configuration.md"><img alt="Notification push" src="../channels/assets/do-not-localize/push.png"></a>
    <div align="center"><a href="../push/push-configuration.md"><strong>Notification push</strong></a></div></td>
    <td><a href="../direct-mail/direct-mail-configuration.md"><img alt="Courrier" src="../channels/assets/do-not-localize/direct-mail.jpg"></a>
    <div align="center"><a href="../direct-mail/direct-mail-configuration.md"><strong>Courrier</strong></a></div></td>
    </tr></table>

   <table style="table-layout:fixed"><tr style="border: 0;">
    <td><a href="../in-app/inapp-configuration.md"><img alt="In-app" src="../channels/assets/do-not-localize/inapp.jpg"></a>
    <div align="center"><a href="../in-app/inapp-configuration.md"><strong>In-app</strong></a></div></td>
    <td><a href="../web/web-configuration.md"><img alt="Web" src="../channels/assets/do-not-localize/web.jpg"></a>
    <div align="center"><a href="../web/web-configuration.md"><strong>Web</strong></a></div></td>
    <td><a href="../code-based/code-based-configuration.md"><img alt="Expérience basée sur du code" src="../channels/assets/do-not-localize/code.png"></a>
    <div align="center"><a href="../code-based/code-based-configuration.md"><strong>Expérience basée sur du code</strong></a></div></td>
    <td><a href="../content-card/content-card-configuration-prereq.md"><img alt="Cartes de contenu" src="../channels/assets/do-not-localize/cards.png"></a>
    <div align="center"><a href="../content-card/content-card-configuration-prereq.md"><strong>Cartes de contenu</strong></a></div></td>
    </tr></table>

   >[!NOTE]
   >
   >Pour les canaux mobiles, la [configuration guidée des canaux](set-mobile-config.md) facilite la configuration des canaux marketing, tout en garantissant la disponibilité des ressources requises dans Experience Platform, Journey Optimizer et la collecte de données. Cela permet à votre équipe marketing de lancer la création de campagnes et de parcours.

1. Une fois cette opération terminée, vous devez configurer tous les paramètres techniques requis pour diffuser les messages en créant des **configurations des canaux**. [En savoir plus sur les configurations de canaux](channel-surfaces.md)

1. En fonction des canaux que vous utilisez, de vos environnements et de vos besoins, vous devez également effectuer les étapes suivantes :

   * Configuration et délégation de sous-domaines pour vos canaux, tels que [e-mails](about-subdomain-delegation.md), [SMS](../sms/sms-subdomains.md), [landing pages](../landing-pages/lp-subdomains.md) et [expériences web](../web/web-delegated-subdomains.md).

   * Configurez des plans de préchauffage d’adresses IP pour une délivrabilité optimale. [En savoir plus](ip-warmup-gs.md)

   * Définissez une liste autorisée pour l’envoi d’e-mails. [En savoir plus](allow-list.md)

   * Gérez le nombre de jours pendant lesquels de nouvelles tentatives sont effectuées avant d&#39;envoyer des adresses électroniques à la liste de suppression. [En savoir plus](manage-suppression-list.md)

   * Activez l’**option d’e-mail Cci** pour conserver une copie des messages envoyés aux individus. [En savoir plus](archiving-support.md#enable-bcc)

   * Configurez les **règles métier** pour éviter de sur-solliciter vos destinataires. [En savoir plus](../conflict-prioritization/rule-sets.md)

   * Déterminez l’adresse e-mail et/ou le numéro de téléphone à utiliser en priorité pour vos destinataires lorsque plusieurs adresses/numéros sont disponibles dans Adobe Experience Platform. [En savoir plus](primary-email-addresses.md)
