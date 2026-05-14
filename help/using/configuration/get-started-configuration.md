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
TQID: https://experienceleague.adobe.com/zHp3C6KVKfRsQbi4B710ACFuMQhGuVxjaNIrXkxwhMc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: c343082f-e963-4f57-a96b-b64d27f8118e
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
  - id: e23d48b5-7858-4d45-9c56-9e2b4be8500e
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
  - id: e5329d1b-e590-4e24-a3fb-ef3fe0f2c721
  - id: efb19423-4da4-4fd1-88d8-5ee8c71ae766
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: e9001ce2-5245-4a8e-8601-dd958009072f
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 471
ht-degree: 88%

---

# Commencer la configuration des canaux {#start-optimizer-configuration}

>[!CONTEXTUALHELP]
>id="ajo_channels_rate_controls"
>title="Contrôles de débit pour les canaux"
>abstract="Contrôles de débit pour les canaux"

Lors du premier accès à [!DNL Journey Optimizer], vous recevez un sandbox de production et un certain nombre d’adresses IP vous sont attribuées en fonction de votre contrat.

Pour envoyer des messages, vous devez suivre les étapes de configuration suivantes :

1. En tant qu’[administrateur ou administratrice système Adobe Journey Optimizer](../start/path/administrator.md), définissez les configurations propres à chaque canal. Découvrez comment effectuer ces configurations dans les pages suivantes :

   <table style="table-layout:fixed"><tr style="border: 0;">
    <td><a href="../email/get-started-email-config.md"><img alt="E-mail" src="../channels/assets/do-not-localize/email.png"></a>
    <div align="center"><a href="../email/get-started-email-config.md"><strong>E-mail</strong></a></div></td>
    <td><a href="../sms/sms-configuration.md"><img alt="sms" src="../channels/assets/do-not-localize/sms.png"></a>
    <div align="center"><a href="../sms/sms-configuration.md"><strong>SMS</strong></a></div></td>
    <td><a href="../push/push-configuration.md"><img alt="notification push" src="../channels/assets/do-not-localize/push.png"></a>
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

   Pour les canaux supplémentaires, reportez-vous aux sections suivantes : [Activités iOS Live](../mobile-live/mobile-live-configuration.md), [WhatsApp](../whatsapp/whatsapp-configuration.md) et [LINE](../line/line-configuration.md).

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
* **[Configurer les activités iOS Live](../mobile-live/mobile-live-configuration.md)** - Configurez votre environnement pour envoyer des activités Live à l’écran de verrouillage d’iPhone et à l’île dynamique.
* **[Configurer WhatsApp](../whatsapp/whatsapp-configuration.md)** - Configurez la messagerie WhatsApp via l’API Cloud Meta pour les campagnes et les parcours.
* **[Configurer LINE](../line/line-configuration.md)** - Configurez la messagerie LINE pour les campagnes et les parcours.
* **[Tutoriels de configuration](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/configuration/channel-configuration/configure-channels){target="_blank"}** : découvrez des tutoriels vidéo détaillés sur la configuration des canaux et les bonnes pratiques.
