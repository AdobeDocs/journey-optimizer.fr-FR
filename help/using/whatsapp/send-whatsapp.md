---
solution: Journey Optimizer
product: journey optimizer
title: Vérifier et tester vos messages WhatsApp
description: Découvrez comment vérifier et envoyer vos messages WhatsApp dans Journey Optimizer.
feature: Whatsapp
topic: Content Management
role: User
level: Beginner
exl-id: 31acb095-de90-495f-8e8c-43a78dedfa06
TQID: https://experienceleague.adobe.com/u2OevVu38fPdytpuTmHeSdEx3Wvpih7ifk-j88rhDFI
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: f8d2e9f0-69c9-40cd-890f-71336c8dfff7id: b8df23d2-98a2-4406-86cc-2babe8728d36
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 420
ht-degree: 58%

---

# Vérifier et envoyer vos messages WhatsApp {#send-whatsapp}

## Prévisualiser votre messages WhatsApp {#preview-whatsapp}

Une fois le contenu de votre message défini, vous pouvez utiliser des profils de test ou des exemples de données d’entrée chargés à partir d’un fichier CSV/JSON ou ajoutés manuellement pour prévisualiser son contenu. Si vous avez inséré du contenu personnalisé, vous pouvez vérifier la façon dont celui-ci s’affiche dans le message.

Pour ce faire, cliquez sur **[!UICONTROL Simuler du contenu]**, puis vérifiez votre message à l’aide des données de profil de test.

Vous trouverez des informations détaillées sur comment prévisualiser et tester votre contenu dans la section [Gestion de contenu](../content-management/preview-test.md).

## Valider votre contenu {#whatsapp-validate}

Vous devez vérifier les alertes dans la section supérieure de l’éditeur. Certaines d’entre elles sont de simples avertissements, mais d’autres peuvent vous empêcher d’envoyer le message. Deux types d’alertes peuvent se produire : avertissements et erreurs.

* Les **avertissements** se rapportent aux recommandations et aux bonnes pratiques. Par exemple, un message d’avertissement s’affiche si votre message texte est vide.

* Les **erreurs** vous empêchent de tester ou d’activer le parcours ou de publier la campagne tant que celles-ci ne sont pas corrigées. Par exemple, un message d’erreur vous avertit lorsque l’objet est manquant.

## Envoyer vos messages WhatsApp {#whatsapp-send}

>[!IMPORTANT]
>
> Si votre campagne est soumise à une politique de validation, vous devrez effectuer une demande d’approbation afin de pouvoir envoyer vos SMS. [En savoir plus](../test-approve/gs-approval.md)

Une fois votre message WhatsApp prêt, effectuez la configuration de votre [parcours](../building-journeys/publish-journey.md) ou [campagne](../campaigns/review-activate-campaign.md) pour l’envoyer.

## Analyse des interactions WhatsApp {#whatsapp-channel-context}

Journey Optimizer capture les données d’interaction supplémentaires renvoyées par le canal WhatsApp et les stocke dans le **Jeu de données d’événement d’expérience de suivi d’e-mail - Rapports** sous le groupe de champs `whatsAppChannelContext` . Utilisez ces champs pour créer des [audiences](../audience/about-audiences.md), exécuter des [requêtes](../data/get-started-queries.md) et analyser l&#39;engagement de WhatsApp. [En savoir plus sur les jeux de données système](../data/get-started-datasets.md#system-datasets).

Les champs suivants sont capturés :

| Champ | Description |
|-|-|
| `messageType` | Type de message WhatsApp (par exemple, `templateBased`, `response`). |
| `inboundMessage` | Contenu de la réponse entrante (par exemple, `stop`, `start`, `subscribe`). |
| `inboundNumber` | Identifiant de l’expéditeur où le message entrant a été reçu. |
| `channelType` | Catégorie de canal (`Utility`, `Marketing` ou `Promotional`). |
| `profileNumber` | Numéro de téléphone à partir duquel le message entrant a été reçu. |
| `origTimestamp` | Horodatage d&#39;origine de Meta / WhatsApp. |
| `status` | Statut de la diffusion, y compris les commentaires normalisés du fournisseur (`sent`, `delivered`, `bounce`, `error`, `delay`, `duplicate`, `denylist`, `exclude` ou `unknown`) et le message brut de statut du fournisseur. |
| `reactionEvent` | Contenu de la réponse de l’utilisateur : émoticône pour les réactions ou texte du message pour les réponses à un message spécifique. |
| `reactionMessageID` | ID du message d’origine auquel une réponse est apportée. |
| `reactionActionName` | Type d’action de réponse (`react`, `unreact` ou `reply`). |
| `interactiveSelectedTitle` | Titre sélectionné par l’utilisateur dans un message interactif WhatsApp. |
| `interactiveType` | Type de message interactif (`list reply`, `button reply` ou `button`). |
| `interactiveSelectedDescription` | Description de l&#39;option interactive WhatsApp sélectionnée. |
| `interactiveSelectedID` | Identifiant de l’option sélectionnée dans WhatsApp. |

Pour interroger ce jeu de données, utilisez la table `ajo_email_tracking_experience_event_dataset` dans Query Service. Pour les modèles de requête et les cas d’utilisation associés, voir [Exemples de requête de jeu de données](../data/datasets-query-examples.md).
