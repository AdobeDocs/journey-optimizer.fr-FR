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
source-git-commit: 528e1a54dd64503e5de716e63013c4fc41fd98db
workflow-type: tm+mt
source-wordcount: '244'
ht-degree: 64%

---


# Prise en main de la configuration des canaux {#start-optimizer-configuration}

Lorsque vous accédez à [!DNL Journey Optimizer] pour la première fois, un sandbox de production vous est alloué ainsi qu’un certain nombre d’adresses IP en fonction de votre contrat.


Pour pouvoir envoyer des messages, vous devez suivre les étapes de configuration répertoriées ci-dessous :

1. En tant qu’administrateur système de [Adobe Journey Optimizer](../start/path/administrator.md), définissez vos configurations de canal. Découvrez comment configurer ces configurations dans les pages suivantes :

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
>Pour les canaux mobiles, la [configuration guidée de canal](set-mobile-config.md) facilite la configuration rapide des canaux marketing, en veillant à ce que toutes les ressources requises soient facilement disponibles dans Experience Platform, Journey Optimizer et la collecte de données. Cela permet à votre équipe marketing de lancer la création de campagnes et de parcours.

1. Une fois cette opération terminée, vous devez créer des **configurations de canal** pour configurer tous les paramètres techniques requis pour diffuser les messages. [En savoir plus sur les configurations de canal](channel-surfaces.md)

1. Vous pouvez également réaliser les opérations suivantes :

   * Gérez le nombre de jours pendant lesquels de nouvelles tentatives sont effectuées avant d&#39;envoyer des adresses électroniques à la liste de suppression. [En savoir plus](manage-suppression-list.md)

   * Activez l’**option d’e-mail Cci** pour conserver une copie des messages envoyés aux individus. [En savoir plus](archiving-support.md#enable-bcc)

   * Configurez les **règles métier** pour éviter de sur-solliciter vos destinataires. [En savoir plus](../conflict-prioritization/rule-sets.md)

   * Déterminez l’adresse e-mail et/ou le numéro de téléphone à utiliser en priorité pour vos destinataires lorsque plusieurs adresses/numéros sont disponibles dans Adobe Experience Platform. [En savoir plus](primary-email-addresses.md)
