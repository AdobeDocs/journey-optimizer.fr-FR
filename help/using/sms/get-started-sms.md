---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec les SMS/MMS/RCS
description: Découvrez comment créer et envoyer des messages texte dans Journey Optimizer.
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: c1027268-0bbe-4e35-a5a6-2aef78083dd3
source-git-commit: 0a9c36b75f7433eadbc8894fb7252a8f846c78b2
workflow-type: tm+mt
source-wordcount: '744'
ht-degree: 30%

---

# Commencer avec les SMS {#get-started-sms}

Utilisez [!DNL Journey Optimizer] pour envoyer des SMS/MMS/RCS à vos clientes et clients sur leur appareil mobile. Vous pouvez créer, personnaliser et prévisualiser des messages au format texte à partir de l’éditeur de SMS/MMS/RCS.

Les messages texte peuvent être créés et envoyés dans un parcours ou dans une campagne. Pour les SMS, MMS et RCS, utilisez l’action SMS.

* Dans un **parcours**. Créez un parcours, ajoutez une activité SMS et définissez les paramètres de base. Accédez ensuite au volet Actions SMS à droite pour créer le contenu du message SMS, MMS ou RCS. [Découvrez comment créer un parcours.](../building-journeys/journey-gs.md)

* Dans une **campagne**. Créez une campagne, sélectionnez SMS comme action et définissez les paramètres de base. Modifiez ensuite le contenu du message pour définir le SMS, MMS ou RCS à envoyer. [Découvrez comment créer une campagne.](../campaigns/create-campaign.md#configure)

>[!IMPORTANT]
>
>Si c’est la première fois que vous créez des SMS, vérifiez que le canal SMS a été configuré. [En savoir plus](sms-configuration.md)

## Fonctionnalités de messagerie texte {#sms-capabilities}

Adobe Journey Optimizer fournit des fonctionnalités complètes de messagerie texte pour interagir avec vos clients sur plusieurs canaux :

**SMS (Short Message Service)**

Envoyez des messages texte uniquement de 160 caractères maximum. SMS est le format de messagerie texte le plus pris en charge sur tous les appareils mobiles.

**MMS (Multimedia Message Service)**

Améliorez votre communication avec le contenu multimédia, notamment les vidéos, les images, les clips audio et les GIF. Les messages MMS autorisent jusqu&#39;à 1600 caractères de texte en plus des fichiers multimédias. [En savoir plus sur les limitations MMS](../start/guardrails.md#sms-guardrails)

**RCS (Rich Communication Services)**

Envoyez des messages interactifs de marque avec des fonctionnalités avancées telles que des carrousels, des cartes enrichies, des actions suggérées et une prise en charge améliorée des médias. RCS offre une expérience de messagerie plus riche sur les appareils pris en charge.

## Principales fonctionnalités {#key-features}

**Personalization et contenu dynamique**

Créez des SMS personnalisés à l’aide de l’éditeur de personnalisation. Ajoutez des attributs de profil, du contenu conditionnel et des données dynamiques pour personnaliser les messages en fonction des destinataires individuels. [En savoir plus sur la personnalisation &#x200B;](../personalization/personalize.md)

**Prise en charge de plusieurs fournisseurs**

Adobe Journey Optimizer s’intègre aux principaux fournisseurs de services SMS :

* **Sinch** - [Guide de configuration](sms-configuration-sinch.md)
* **Twilio** - [Guide de configuration](sms-configuration-twilio.md)
* **Infobip** - [Guide de configuration](sms-configuration-infobip.md)
* **Fournisseurs personnalisés** - Configurez tout autre fournisseur SMS à l’aide de l’intégration d’API personnalisée. [En savoir plus](sms-configuration-custom.md)

**Raccourcissement et tracking d’URL**

Ajoutez des URL raccourcies pouvant être suivies à vos messages pour surveiller l’engagement. Une configuration de sous-domaine est requise pour la fonctionnalité de raccourcissement des URL. [Découvrez comment configurer des sous-domaines SMS](sms-subdomains.md)

**Gestion du droit d’opposition**

Garantissez la conformité aux normes et réglementations du secteur grâce à une gestion intégrée des désinscriptions. Journey Optimizer gère automatiquement les mots-clés de désinscription standard (STOP, QUIT, CANCEL, etc.) pour les fournisseurs Sinch et Infobip. [En savoir plus sur la gestion des désinscriptions](sms-opt-out.md)

**Prévisualisation et test**

Testez vos SMS avant l’envoi à l’aide de profils de test et de données d’exemple. Prévisualisez la personnalisation, le contenu et la mise en forme pour vous assurer que vos messages s’affichent correctement. [Découvrez comment envoyer des messages](send-sms.md)

**Reporting et Analytics**

Suivez les performances de vos campagnes et parcours SMS avec des fonctionnalités de création de rapports complètes :

* [Rapports de campagne par SMS](../reports/campaign-global-report-cja-sms.md)
* [Rapports de parcours SMS](../reports/journey-global-report-cja-sms.md)

## Exigences de configuration {#configuration-requirements}

Avant d’envoyer des SMS, vous devez :

1. **Choisir un fournisseur SMS** - Effectuez un choix parmi Sinch, Twilio, Infobip ou configurez un fournisseur personnalisé
2. **Configuration des informations d’identification d’API** - Intégrez les jetons API et les identifiants de service de votre fournisseur à Journey Optimizer
3. **Créer des configurations de canal** - Paramétrez les configurations SMS pour les messages marketing et transactionnels
4. **Configurer des sous-domaines (facultatif)** - Requis uniquement si vous prévoyez d’utiliser le raccourcissement des URL dans vos messages

Ces étapes de configuration sont généralement effectuées par un administrateur système. [Commencer la configuration des SMS](sms-configuration.md)

## Guide de démarrage rapide {#quick-start}

<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<a href="sms-configuration.md">
<img alt="Validation" src="../assets/do-not-localize/sms-config.jpg">
</a>
<div>
<a href="sms-configuration.md"><strong>Configurer le canal SMS</strong></a>
</div>
<p>Configurer les configurations de canal et de fournisseur SMS</p>
</td>
<td>
<a href="create-sms.md">
<img alt="Lead" src="../assets/do-not-localize/sms-create.jpeg">
</a>
<div><a href="create-sms.md"><strong>Créer un message texte</strong>
</div>
<p>Concevoir et personnaliser votre contenu SMS, MMS ou RCS</p>
</td>
<td>
<a href="send-sms.md">
<img alt="Peu fréquent" src="../assets/do-not-localize/sms-sending.jpg">
</a>
<div>
<a href="send-sms.md"><strong>Prévisualiser et envoyer</strong></a>
</div>
<p>Tester et envoyer vos SMS à votre audience</p>
</td>
<td>
<a href="sms-opt-out.md">
<img alt="Validation" src="../assets/do-not-localize/sms-opt-out.jpg">
</a>
<div>
<a href="sms-opt-out.md"><strong>Gérer les désinscriptions</strong></a>
</div>
<p>Gérer les demandes de désabonnement et garantir la conformité</p>
</td>
</tr></table>

## Ressources supplémentaires {#additional-resources}

**Guides de configuration**

* [Présentation de la configuration du canal SMS](sms-configuration.md)
* [Créer des configurations de canal SMS](sms-configuration-surface.md)
* [Configurer des sous-domaines SMS pour le raccourcissement des URL](sms-subdomains.md)

**Guides de configuration des fournisseurs**

* [Configurer le fournisseur Sinch](sms-configuration-sinch.md)
* [Configurer le fournisseur Twilio](sms-configuration-twilio.md)
* [Configurer le fournisseur Infobip](sms-configuration-infobip.md)
* [Configuration d’un fournisseur de SMS personnalisé](sms-configuration-custom.md)

**Création et gestion de contenu**

* [Créer des messages SMS/MMS](create-sms.md)
* [Prévisualiser, tester et envoyer des messages](send-sms.md)
* [Personalization dans les messages texte](../personalization/personalize.md)
* [Contenu dynamique](../personalization/get-started-dynamic-content.md)

**Conformité et confidentialité**

* [Gestion du droit d&#39;opposition](sms-opt-out.md)
* [Confidentialité et consentement](../privacy/opt-out.md#sms-opt-out-management-sms-opt-out-management)

**Suivi des performances**

* [Rapports de campagne par SMS](../reports/campaign-global-report-cja-sms.md)
* [Rapports de parcours SMS](../reports/journey-global-report-cja-sms.md)

**Intégration de Parcours et de Campaign**

* [Ajouter des SMS aux parcours](../building-journeys/journeys-message.md)
* [Créer des campagnes SMS](../campaigns/create-campaign.md)

## Vidéos pratiques {#videos}

**Configurer et envoyer des SMS**

Découvrez comment configurer, créer et inclure des messages SMS dans vos parcours clients.

+++Regarder la vidéo

>[!VIDEO](https://video.tv.adobe.com/v/3420509?learn=on)

+++

**Explorer les fonctionnalités de messagerie mobile**

Découvrez les fonctionnalités complètes de messagerie mobile que Adobe Journey Optimizer offre aux marketeurs.

+++Regarder la vidéo

>[!VIDEO](https://video.tv.adobe.com/v/3426021?quality=12&learn=on)

+++

**Envoyer des messages RCS de marque**

Découvrez comment configurer et envoyer des messages RCS interactifs d’une marque dans Adobe Journey Optimizer à l’aide d’un fournisseur de SMS personnalisé.

+++Regarder la vidéo

>[!VIDEO](https://video.tv.adobe.com/v/3464755)

+++

**Rubriques connexes**

* [Ajouter des messages dans les parcours](../building-journeys/journeys-message.md)
* [Création de campagnes marketing](../campaigns/create-campaign.md)
* [Mécanismes de sécurisation et limitations](../start/guardrails.md#sms-guardrails)
