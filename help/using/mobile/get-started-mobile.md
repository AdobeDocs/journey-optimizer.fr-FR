---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main des messages mobiles
description: Découvrez comment créer et envoyer des messages mobiles dans Journey Optimizer
feature: SMS
topic: Content Management
role: User
level: Beginner
exl-id: c1027268-0bbe-4e35-a5a6-2aef78083dd3
TQID: https://experienceleague.adobe.com/Ev0xJ86fpweQxgf-VjGUEl4ebk6BdzhVof2BgiMR9EM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: c13ff12d-60f1-49cd-833a-d43359628223
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 4c82775044b5a0a3a48920f59b0afb8a3c6a6d80
workflow-type: tm+mt
source-wordcount: 1040
ht-degree: 24%

---

# Prise en main des messages mobiles {#get-started-sms}

>[!BEGINSHADEBOX]

**Sur cette page :** Prise en main de la messagerie mobile dans Adobe Journey Optimizer pour créer, personnaliser et envoyer des SMS, des MMS et des messages RCS dans les parcours et les campagnes, y compris la prise en charge du fournisseur, les exigences de configuration et les conditions préalables RCS.

>[!ENDSHADEBOX]

>[!IMPORTANT]
>
>Si c’est la première fois que vous créez des messages mobiles, vérifiez que le canal Message mobile a été configuré. [En savoir plus](mobile-configuration.md)

Utilisez [!DNL Journey Optimizer] pour envoyer des messages mobiles à vos clients sur trois canaux, **SMS**, **MMS** et **RCS**, à partir d’un seul éditeur SMS/MMS/RCS où vous pouvez créer, personnaliser et prévisualiser votre contenu.

* **SMS (Short Message Service)** : envoyez des messages texte uniquement de 160 caractères maximum, pris en charge sur tous les appareils mobiles.
* **MMS (Multimedia Message Service)** : enrichissez vos messages avec des images, des vidéos, des clips audio et des GIF, ainsi que jusqu’à 1 600 caractères de texte. [En savoir plus sur les limitations des MMS](../start/guardrails.md#sms-guardrails)
* **RCS (Rich Communication Services)**:Deliver contenu interactif de marque directement dans l’application de messagerie native de vos clients, sans téléchargement d’application supplémentaire requis.

Les messages mobiles peuvent être créés et envoyés dans un parcours ou dans une campagne à l’aide de l’action Message mobile :

* Dans un Parcours **&#x200B;**&#x200B;: ajoutez une action Message mobile à votre parcours, définissez les paramètres de base, puis composez votre contenu dans le volet Actions de message mobile à droite. [Découvrez comment créer un parcours.](../building-journeys/journey-gs.md)

* Dans une **campagne**:Create une campagne, sélectionnez Message mobile comme action, définissez les paramètres de base, puis modifiez le contenu du message. Découvrez comment créer une [campagne d’action](../campaigns/campaign-action.md#action-campaign-action), une [campagne déclenchée par API](../campaigns/api-triggered-campaigns.md) ou une [campagne orchestrée](../orchestrated/create-orchestrated-campaign.md#create).


## Principales fonctionnalités {#key-features}

| Fonctionnalité | Description |
|---|---|
| **Personnalisation** | Personnalisez les messages avec des attributs de profil, du contenu conditionnel et des données dynamiques à l’aide de l’éditeur de personnalisation. [En savoir plus](../personalization/personalize.md) |
| **Prise en charge du fournisseur** | Connectez-vous avec [Sinch](mobile-configuration-sinch.md), [Twilio](mobile-configuration-twilio.md), [Infobip](mobile-configuration-infobip.md) ou tout [fournisseur personnalisé](mobile-configuration-custom.md) via l’intégration d’API. |
| **Raccourcissement d’URL** | Ajoutez des URL raccourcies pouvant être suivies pour surveiller l’engagement. Nécessite une configuration de sous-domaine. [En savoir plus](mobile-subdomains.md) |
| **Gestion du droit d’opposition** | Gestion intégrée des mots-clés de désinscription standard (STOP, QUIT, CANCEL, etc.) pour Sinch et Infobip. [En savoir plus](mobile-opt-out.md) |
| **Prévisualisation et test** | Validez le contenu avec des profils de test et des données d’exemple avant l’envoi. [En savoir plus](send-mobile-message.md) |
| **Créer des rapports** | Suivez les performances des campagnes et des parcours avec des [rapports de campagne](../reports/campaign-global-report-cja-sms.md) et [rapports de parcours dédiés](../reports/journey-global-report-cja-sms.md). |

## Exigences de configuration {#configuration-requirements}

Avant d&#39;envoyer des messages mobiles, vous devez :

1. **Choisir un fournisseur SMS** : sélectionnez Sinch, Twilio, Infobip ou configurez un fournisseur personnalisé
2. **Configurer les informations d’identification d’API** : intégrez les jetons d’API et les identifiants de service de votre fournisseur à Journey Optimizer
3. **Créer des configurations de canal** : définissez des configurations SMS pour les messages marketing et transactionnels
4. **Configurer des sous-domaines (facultatif)** : obligatoire uniquement si vous prévoyez d’utiliser le raccourcissement des URL dans vos messages

Ces étapes de configuration sont généralement effectuées par un administrateur ou une administratrice système. [Commencer avec la configuration des SMS](mobile-configuration.md)

### Configuration requise pour RCS {#requirement-rcs}

Les conditions préalables suivantes sont requises pour utiliser RCS dans Journey Optimizer :

* **Informations d’identification de l’API Sinch RCS** : un administrateur doit configurer les informations d’identification de l’API pour le fournisseur Sinch RCS (ID de projet, ID d’application et jeton API). [En savoir plus](mobile-configuration-sinch.md)
* **Configuration du canal de message mobile** : un administrateur doit créer une configuration de canal avec des informations d’identification activées pour RCS sélectionnées, de sorte que les messages soient diffusés en tant que RCS plutôt que SMS. [En savoir plus](mobile-configuration.md)
* **SMS de secours** : vivement recommandé. Les destinataires dont les appareils ne prennent pas en charge RCS ne recevront pas le message, sauf si un SMS de secours est disponible. Les clients sans volume SMS existant doivent acheter des SMS et un numéro court. [En savoir plus](design-mobile.md#rcs-content)
* **Fournisseur pris en charge** : la création native du serveur de collecte de données nécessite un serveur de collecte de données Sinch (revente ou vente directe Adobe). Twilio, Infobip et d&#39;autres fournisseurs doivent utiliser une intégration de fournisseur personnalisée.
* **Prise en charge des appareils** : la diffusion RCS est prise en charge sur les appareils Android et iOS. La disponibilité des transporteurs et des régions varie, RCS n&#39;est pas universellement disponible dans le monde.

## Ressources supplémentaires {#additional-resources}

Parcourez les rubriques ci-dessous pour en savoir plus sur la messagerie mobile dans Journey Optimizer.

+++Guides de configuration

Découvrez comment configurer votre environnement SMS :

* [Vue d’ensemble de la configuration du canal SMS](mobile-configuration.md)
* [Créer des configurations de canal SMS](mobile-configuration-surface.md)
* [Configurer des sous-domaines SMS pour le raccourcissement des URL](mobile-subdomains.md)

+++

+++Guides de configuration du fournisseur

Configuration détaillée de chaque fournisseur de services SMS :

* [Configurer le fournisseur Sinch](mobile-configuration-sinch.md)
* [Configurer le fournisseur Twilio](mobile-configuration-twilio.md)
* [Configurer le fournisseur Infobip](mobile-configuration-infobip.md)
* [Configurer un fournisseur de SMS personnalisé](mobile-configuration-custom.md)

+++

+++Création et gestion de contenu

Créez, personnalisez et gérez le contenu de votre message mobile :

* [Créer des messages SMS/RCS/MMS](create-mobile-message.md)
* [Prévisualiser, tester et envoyer des messages](send-mobile-message.md)
* [Personalization dans les messages mobiles](../personalization/personalize.md)
* [Contenu dynamique](../personalization/get-started-dynamic-content.md)
* [Générer du contenu SMS avec l’assistant IA](../content-management/generative-text.md)

+++

+++Conformité et confidentialité

Assurez-vous que vos messages mobiles sont conformes aux réglementations et aux normes de confidentialité :

* [Gestion du désabonnement](mobile-opt-out.md)
* [Confidentialité et consentement](../privacy/opt-out.md#opt-out-decision-management)

+++

+++Suivi des performances

Surveillez et analysez les performances de vos campagnes et parcours SMS.

* [Rapports de campagne par SMS](../reports/campaign-global-report-cja-sms.md)
* [Rapports de parcours SMS](../reports/journey-global-report-cja-sms.md)

+++

+++Intégration aux parcours et campagnes

Découvrez comment incorporer des SMS dans vos parcours et campagnes client :

* [Ajouter des SMS aux parcours](../building-journeys/journey-action.md)
* [Créer des campagnes SMS](../campaigns/create-campaign.md)

+++

+++Questions fréquentes sur RCS

**La messagerie RCS native est-elle disponible avec Twilio ou Infobip ?**

Non. Le concepteur RCS natif de Journey Optimizer n’est pas disponible lors de l’utilisation de fournisseurs SMS tiers tels que Twilio ou Infobip. Les messages RCS peuvent toutefois être envoyés via une [&#x200B; intégration de fournisseur personnalisé &#x200B;](mobile-configuration-custom.md).

**Pourquoi acheter des SMS avec RCS ?**

Achetez le volume du SMS et un numéro court pour activer la fonctionnalité SMS de secours, qui est le chemin d’accès recommandé. Si le SMS n’est pas configuré, les profils dont l’appareil ou l’opérateur ne prend pas en charge le serveur de collecte de données ne recevront pas le message du tout.

**La messagerie RCS native est-elle disponible pour les clients Sinch directs ?**

Oui. Les clients qui utilisent l’API de conversation de Sinch ont accès à la création RCS native, y compris la revente Adobe et la clientèle directe Sinch.

**RCS est-il disponible partout ?**

Non. L&#39;adoption des transporteurs continue de croître à l&#39;échelle mondiale, mais le RCS n&#39;est pas universellement pris en charge par tous les transporteurs et toutes les régions. La disponibilité régionale et le soutien des transporteurs doivent être étudiés lors de la planification des campagnes RCS.

**Où les messages RCS apparaissent-ils sur l’appareil ?**

Les messages RCS apparaissent au même endroit que les messages SMS standard, dans l’application de messagerie native de l’appareil. Ils arrivent d&#39;un expéditeur de marque et vérifié, donnant aux destinataires les signaux de confiance pour savoir que le message est légitime.

**Quelles sont les limites de caractères pour un message RCS ?**

Les types de messages Rich Media (Single) prennent en charge jusqu&#39;à 3 072 caractères, soit beaucoup plus que la limite de 160 caractères pour les SMS standard. Les types de message RCS de base sont limités à 160 caractères, ce qui correspond à la limite SMS standard.

+++

## Vidéos pratiques {#videos}

**Configurer et envoyer des SMS**

Découvrez comment configurer, créer et inclure des SMS dans vos parcours clients.

+++Regarder la vidéo

>[!VIDEO](https://video.tv.adobe.com/v/3422694?captions=fre_fr&learn=on)

+++

**Explorer les fonctionnalités de messagerie mobile**

Découvrez les fonctionnalités complètes de messagerie mobile qu’Adobe Journey Optimizer offre aux responsables marketing.

+++Regarder la vidéo

>[!VIDEO](https://video.tv.adobe.com/v/3430372?captions=fre_fr&quality=12&learn=on)

+++

**Envoyer des messages RCS au nom de la marque**

Découvrez comment configurer et envoyer des messages RCS interactifs d’une marque dans Adobe Journey Optimizer à l’aide d’un fournisseur de SMS personnalisé.

+++Regarder la vidéo

>[!VIDEO](https://video.tv.adobe.com/v/3464757?captions=fre_fr)

+++
