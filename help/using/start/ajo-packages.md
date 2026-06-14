---
solution: Journey Optimizer
product: journey optimizer
title: Fonctionnalités de Journey Optimizer par package
description: Identifiez les fonctionnalités Adobe Journey Optimizer disponibles en fonction de votre licence, de votre package et des canaux activés.
feature: Get Started
topic: Content Management
role: Admin, User
level: Beginner
keywords: parcours optimizer, package, licence, select, prime, ultimate, fonctionnalités, fonctionnalités, modulaire, canaux
hide: true
source-git-commit: 46a5a6dc0a3486633a1a71f8bba8a3cd53aaa618
workflow-type: tm+mt
source-wordcount: '1007'
ht-degree: 6%

---


# Que trouve-t-on dans mon [!DNL Adobe Journey Optimizer] ? {#ajo-packages}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez les fonctionnalités Adobe Journey Optimizer déverrouillées par votre package, que vous utilisiez le modèle Campagnes et Parcours actuel ou les anciennes licences Select, Prime et Ultimate, afin de confirmer les fonctionnalités disponibles et d’accéder à chaque fonctionnalité.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] fonctionnalités varient en fonction de votre contrat de licence, des canaux activés et des autorisations utilisateur. Utilisez ce guide pour comprendre les fonctionnalités généralement disponibles dans votre package et accédez directement à la documentation du produit pour chaque fonctionnalité.

La disponibilité peut également dépendre de la configuration du canal, des conditions préalables à l’implémentation et des modules complémentaires achetés. Sélectionnez l’onglet correspondant à votre modèle de licence.

>[!BEGINTABS]

>[!TAB Parcours et campagnes]

Cet onglet s’applique aux clients sous licence selon le modèle de package modulaire [!DNL Adobe Journey Optimizer] actuel (Journey Optimizer - Campagnes, Journey Optimizer - Parcours ou Journey Optimizer - Campagnes et Parcours).

## Packages de base {#current-packages}

| Package | Ce que cela inclut |
|---------|----------------|
| **Journey Optimizer - Campagnes** | Orchestration des campagnes : workflows d’audience à une ou plusieurs étapes pour l’engagement par lots. Messages transactionnels par e-mail, notification push et SMS inclus. |
| **Journey Optimizer - Parcours** | Journey Orchestration en temps réel : parcours déclenchés par un événement prenant en charge la diffusion en continu et le traitement par lots. Messages transactionnels par e-mail, notification push et SMS inclus. |
| **Journey Optimizer - Campagnes et Parcours** | Orchestration des campagnes et Journey Orchestration en temps réel combinés. Messages transactionnels par e-mail, notification push et SMS inclus. |

>[!NOTE]
>
>Le droit total au volume de données diffère selon le package : **Campagnes** les clients ont droit à 15 Ko par profil adressable ; **Parcours** et **Campagnes et Parcours** les clients ont droit à 75 Ko par profil adressable.

Les modules complémentaires suivants étendent la couverture de canal au-dessus de tout package de base. Le module complémentaire **Tous les canaux** regroupe les composants Diffusion sortante, Mobile et Web.

| Module complémentaire | Canaux déverrouillés |
|--------|----------------|
| **Diffusion sortante** | E-mail, notifications push, courrier. Inclut les principes de base de la délivrabilité. |
| **Mobile** | Messages in-app, notifications push, cartes de contenu et canaux basés sur du code pour les surfaces mobiles |
| **Web** | Canal web et canaux basés sur le code pour les surfaces web |
| **Tous les canaux** | Lots de diffusion sortante + Mobile + Web |
| **Prise de décision** | Offer Decisioning en temps réel et optimisation optimisée par l’IA |

## Matrice des fonctionnalités {#capability-matrix-current}

| Fonctionnalité | Ce que vous pouvez faire | Journey Optimizer - Campagnes | JOURNEY OPTIMIZER - PARCOURS | Journey Optimizer - Campagnes et Parcours | Module complémentaire obligatoire | En savoir plus |
|-----------|----------------|:-----------------------------:|:----------------------------:|:----------------------------------------:|:---------------:|-----------|
| **Messages transactionnels** | Envoyer des messages déclenchés en temps réel par e-mail, notification push ou SMS | ✓ | ✓ | ✓ | — | [En savoir plus sur les messages transactionnels](../building-journeys/journey-gs.md) |
| **E-mail** | Concevoir et envoyer des e-mails personnalisés | ✓ | ✓ | ✓ | Diffusion sortante | [Découvrez comment envoyer des e-mails](../email/get-started-email.md) |
| **Notifications push** | Envoi d&#39;alertes push mobiles | ✓ | ✓ | ✓ | Diffusion sortante | [Découvrez comment envoyer des notifications push](../push/get-started-push.md) |
| **Courrier (publipostage direct)** | Création et envoi d’éléments de courrier physique | ✓ | ✓ | ✓ | Diffusion sortante | [Découvrez comment utiliser le courrier](../direct-mail/get-started-direct-mail.md) |
| **SMS/MMS** | Envoi de messages texte et multimédia | ✓ | ✓ | ✓ | Diffusion sortante | [Découvrez comment envoyer des messages mobiles](../mobile/get-started-mobile.md) |
| **Messagerie in-app** | Afficher des messages dans votre application mobile | ✓ | ✓ | ✓ | Mobile | [Découvrez comment utiliser la messagerie in-app](../in-app/get-started-in-app.md) |
| **Cartes de contenu** | Diffuser des messages intégrés au produit persistants et non intrusifs | ✓ | ✓ | ✓ | Mobile | [Découvrez comment utiliser les cartes de contenu](../content-card/get-started-content-card.md) |
| **Canal web** | Personnaliser des pages web en temps réel | ✓ | ✓ | ✓ | Web | [Découvrez comment utiliser le canal web](../web/get-started-web.md) |
| **Expériences basées sur du code** | Personnaliser n’importe quelle surface via l’API ou SDK | ✓ | ✓ | ✓ | Mobile ou Web | [Découvrez comment utiliser des expériences basées sur du code](../code-based/get-started-code-based.md) |
| **WhatsApp** | Envoyer des messages via WhatsApp Business | ✓ | ✓ | ✓ | WhatsApp | [Découvrez comment utiliser WhatsApp](../whatsapp/get-started-whatsapp.md) |
| **Campagnes orchestrées** | Concevez des workflows d’audience à plusieurs étapes pour l’engagement par lots. Canaux pris en charge : e-mail, SMS, notification push et publipostage direct uniquement. | ✓ | — | ✓ | — | [Découvrez comment utiliser des campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md) |
| parcours automatisés **** | Concevoir des parcours clients en temps réel déclenchés par un événement | — | ✓ | ✓ | — | [Découvrez comment créer des parcours ](../building-journeys/journey-gs.md) |
| **déclencheurs en temps réel** | Réagissez aux événements client dès qu’ils se produisent | — | ✓ | ✓ | — | [En savoir plus sur les événements de parcours ](../event/about-events.md) |
| **Prise de décision** | Sélectionnez la meilleure offre pour chaque client en temps réel | Dépend de votre licence | Dépend de votre licence | Dépend de votre licence | Prise de décision | [Découvrez comment utiliser la prise de décision](../experience-decisioning/gs-experience-decisioning.md) |
| **Classement optimisé par l’IA** | Optimiser la sélection des offres à l’aide du machine learning | Dépend de votre licence | Dépend de votre licence | Dépend de votre licence | Prise de décision | [En savoir plus sur les modèles d’IA ](../offers/ranking/ai-models.md) |

>[!TAB Sélectionner / Prime / Ultimate]

Cet onglet s’applique aux clients disposant de contrats de licence utilisant la terminologie des packages Select, Prime ou Ultimate.

## Résumés des packages {#package-summaries}

+++**Sélectionner**

Idéal pour les organisations qui commencent à utiliser la messagerie par lots et transactionnelle :

- Campagnes par lots planifiées et messages transactionnels
- Exécution des campagnes principales et des parcours
- E-mail, SMS, notification push et bases de canal d’action personnalisée
- Mécanismes de sécurisation d’orchestration standard

+++

+++****

Inclut tout dans Select, ainsi que l’orchestration en temps réel et les canaux entrants :

- Orchestration des parcours en temps réel déclenchée par un événement
- Canaux entrants : web, messagerie in-app, expériences basées sur du code, cartes de contenu et courrier
- Segmentation et ciblage avancés des audiences

+++

+++****

Inclut tous les éléments de Prime, ainsi que la prise de décision et l’optimisation avancée :

- Prise de décision et personnalisation des offres en temps réel
- Modèles de classement et d’optimisation optimisés par l’IA
- Fonctionnalités avancées de reporting et d’expérimentation

+++

## Matrice des fonctionnalités {#capability-matrix-legacy}

| Fonctionnalité | Ce que vous pouvez faire | Sélectionner | Prime | Ultimate | En savoir plus |
|-----------|----------------|:------:|:-----:|:--------:|-----------|
| **E-mail** | Concevoir et envoyer des e-mails personnalisés | Inclus | Inclus | Inclus | [Découvrez comment envoyer des e-mails](../email/get-started-email.md) |
| **SMS/MMS** | Envoi de messages texte et multimédia | Inclus | Inclus | Inclus | [Découvrez comment envoyer des messages mobiles](../mobile/get-started-mobile.md) |
| **Notifications push** | Envoi d&#39;alertes push mobiles | Inclus | Inclus | Inclus | [Découvrez comment envoyer des notifications push](../push/get-started-push.md) |
| **Campagnes par lots** | Planifier des messages pour une audience | Inclus | Inclus | Inclus | [Découvrez comment créer des campagnes](../campaigns/get-started-with-campaigns.md) |
| parcours automatisés **** | Concevoir des parcours client déclenchés par un événement | Inclus | Inclus | Inclus | [Découvrez comment créer des parcours ](../building-journeys/journey-gs.md) |
| **Déclencheurs de parcours en temps réel** | Réagissez au comportement du client dès que cela se produit. | — | Inclus | Inclus | [En savoir plus sur les événements de parcours ](../event/about-events.md) |
| **Messagerie in-app** | Afficher des messages dans votre application mobile | — | Inclus | Inclus | [Découvrez comment utiliser la messagerie in-app](../in-app/get-started-in-app.md) |
| **Canal web** | Personnaliser des pages web en temps réel | — | Inclus | Inclus | [Découvrez comment utiliser le canal web](../web/get-started-web.md) |
| **Expériences basées sur du code** | Personnaliser n’importe quelle surface via l’API ou SDK | — | Inclus | Inclus | [Découvrez comment utiliser des expériences basées sur du code](../code-based/get-started-code-based.md) |
| **Cartes de contenu** | Diffuser des messages intégrés au produit persistants et non intrusifs | — | Inclus | Inclus | [Découvrez comment utiliser les cartes de contenu](../content-card/get-started-content-card.md) |
| **Courrier (publipostage direct)** | Création et envoi d’éléments de courrier physique | — | Disponible avec Prime et versions ultérieures | Inclus | [Découvrez comment utiliser le courrier](../direct-mail/get-started-direct-mail.md) |
| **Prise de décision** | Sélectionnez la meilleure offre pour chaque client en temps réel | — | — | Inclus | [Découvrez comment utiliser la prise de décision](../experience-decisioning/gs-experience-decisioning.md) |
| **Classement optimisé par l’IA** | Optimiser la sélection des offres et des contenus à l’aide du machine learning | — | — | Inclus | [En savoir plus sur les modèles d’IA ](../offers/ranking/ai-models.md) |
| **WhatsApp** | Envoyer des messages via WhatsApp Business | Dépend de votre licence et de la configuration du canal | Dépend de votre licence et de la configuration du canal | Dépend de votre licence et de la configuration du canal | [Découvrez comment utiliser WhatsApp](../whatsapp/get-started-whatsapp.md) |

>[!ENDTABS]
