---
solution: Journey Optimizer
product: journey optimizer
title: 'Commencer la configuration des canaux  [!DNL Journey Optimizer] '
description: 'En savoir plus sur la configuration des canaux [!DNL Journey Optimizer] '
role: Admin, Developer
level: Intermediate, Experienced
exl-id: 0964a484-f957-4aae-a571-61b2a1615026
feature: Application Settings
topic: Administration
keywords: configuration, configurer, messages, canal, sandbox, optimizer
source-git-commit: efb943e5a6f27becc6e8b6128b776e46d6141823
workflow-type: ht
source-wordcount: '397'
ht-degree: 100%

---


# Commencer la configuration des canaux {#start-optimizer-configuration}

>[!CONTEXTUALHELP]
>id="ajo_channels_rate_controls"
>title="Contrôles de débit pour les canaux"
>abstract="Contrôles de débit pour les canaux"

Lors de l&#39;accès à [!DNL Journey Optimizer] pour la première fois, vous recevez un sandbox de production et un certain nombre d’adresses IP vous sont attribuées en fonction de votre contrat.

Pour envoyer des messages, vous devez suivre les étapes de configuration suivantes :

1. En tant qu’[administrateur ou administratrice système Adobe Journey Optimizer](../start/path/administrator.md), définissez les configurations propres à chaque canal. Découvrez comment effectuer ces configurations dans les pages suivantes :

   <table style="table-layout:fixed"><tr style="border: 0;">
    <td><a href="../email/get-started-email-config.md"><img alt="E-mail" src="../channels/assets/do-not-localize/email.png"></a>
    <div align="center"><a href="../email/get-started-email-config.md"><strong>E-mail</strong></a></div></td>
    <td><a href="../sms/sms-configuration.md"><img alt="sms" src="../channels/assets/do-not-localize/sms.png"></a>
    <div align="center"><a href="../sms/sms-configuration.md"><strong>SMS</strong></a></div></td>
    <td><a href="../push/push-configuration.md"><img alt="Notification push" src="../channels/assets/do-not-localize/push.png"></a>
    <div align="center"><a href="../push/push-configuration.md"><strong>Notification push</strong></a></div></td>
    <td><a href="../direct-mail/direct-mail-configuration.md"><img alt="Courrier" src="../channels/assets/do-not-localize/direct-mail.jpg"></a>
    <div align="center"><a href="../direct-mail/direct-mail-configuration.md"><strong>Courrier</strong></a></div></td>
    </tr></table>

   <table style="table-layout:fixed"><tr style="border: 0;">
    <td><a href="../in-app/inapp-configuration.md"><img alt="In-app" src="../channels/assets/do-not-localize/inapp.jpg"></a>
    <div align="center"><a href="../in-app/inapp-configuration.md"><strong>In-app</strong></a></div></td>
    <td><a href="../web/web-configuration.md"><img alt="web" src="../channels/assets/do-not-localize/web.jpg"></a>
    <div align="center"><a href="../web/web-configuration.md"><strong>Web</strong></a></div></td>
    <td><a href="../code-based/code-based-configuration.md"><img alt="Expérience basée sur du code" src="../channels/assets/do-not-localize/code.png"></a>
    <div align="center"><a href="../code-based/code-based-configuration.md"><strong>Expérience basée sur du code</strong></a></div></td>
    <td><a href="../content-card/content-card-configuration-prereq.md"><img alt="Cartes de contenu" src="../channels/assets/do-not-localize/cards.png"></a>
    <div align="center"><a href="../content-card/content-card-configuration-prereq.md"><strong>Cartes de contenu</strong></a></div></td>
    </tr></table>

   >[!NOTE]
   >
   >Pour les canaux mobiles, la [configuration guidée des canaux](set-mobile-config.md) facilite la configuration des canaux marketing, tout en garantissant la disponibilité des ressources requises dans Experience Platform, Journey Optimizer et la collecte de données. Cela permet à votre équipe marketing de lancer la création de campagnes et de parcours.

1. Une fois cette étape terminée, vous devez configurer tous les paramètres techniques nécessaires à la diffusion des messages en créant des **configurations de canal**. [En savoir plus sur les configurations de canal](channel-surfaces.md)

1. En fonction des canaux utilisés, de vos environnements et de vos besoins, vous devrez également effectuer les étapes suivantes :

   * Configurer et déléguer les sous-domaines pour vos canaux, tels que les [e-mails](about-subdomain-delegation.md), les [SMS](../sms/sms-subdomains.md), les [pages de destination](../landing-pages/lp-subdomains.md) et les [expériences web](../web/web-delegated-subdomains.md).

   * Mettre en place des plans de préchauffage des adresses IP pour garantir une délivrabilité optimale. [En savoir plus](ip-warmup-gs.md)

   * Définir une liste autorisée pour l’envoi des e-mails. [En savoir plus](allow-list.md)

   * Gérez le nombre de jours pendant lesquels de nouvelles tentatives sont effectuées avant d&#39;envoyer des adresses électroniques à la liste de suppression. [En savoir plus](manage-suppression-list.md)

   * Activez l’**option d’e-mail Cci** pour conserver une copie des messages envoyés aux personnes. [En savoir plus](archiving-support.md#enable-bcc)

   * Configurez les **règles métier** pour éviter de sur-solliciter vos destinataires. [En savoir plus](../conflict-prioritization/rule-sets.md)

   * Déterminez l’adresse e-mail et/ou le numéro de téléphone à utiliser en priorité pour vos destinataires lorsque plusieurs adresses/numéros sont disponibles dans Adobe Experience Platform. [En savoir plus](primary-email-addresses.md)

## Ressources supplémentaires

* **[Configurer des surfaces de canal](channel-surfaces.md)** : découvrez comment configurer et gérer des surfaces de canal pour les e-mails, les notifications push, les SMS et d’autres canaux.
* **[Déléguer des sous-domaines](delegate-subdomain.md)** : découvrez comment déléguer des sous-domaines à Adobe pour la délivrabilité des e-mails et le branding.
* **[Préchauffer les adresses IP](ip-warmup-gs.md)** : découvrez les bonnes pratiques de préchauffage des adresses IP pour améliorer la délivrabilité des e-mails et la réputation des expéditeurs et expéditrices.
* **[Gérer la liste de suppression](manage-suppression-list.md)** : découvrez comment gérer les listes de suppression pour gérer les rebonds et maintenir l’hygiène des listes.
* **[Configurer des applications mobiles](set-mobile-config.md)** : définissez les configurations d’applications mobiles pour les notifications push et la messagerie in-app.
* **[Tutoriels de configuration](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/configure-channels){target="_blank"}** : découvrez des tutoriels vidéo détaillés sur la configuration des canaux et les bonnes pratiques.
