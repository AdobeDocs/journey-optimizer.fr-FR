---
solution: Journey Optimizer
product: journey optimizer
title: Gestion des opt-out des SMS
description: Découvrez comment gérer l’exclusion avec les SMS
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '415'
ht-degree: 0%

---

# Gestion des opt-out des SMS {#sms-opt-out}

Conformément aux normes et réglementations du secteur, tous les messages de marketing SMS doivent contenir un moyen pour que les destinataires puissent facilement se désabonner. [En savoir plus sur la gestion de la confidentialité et de l’exclusion](../privacy/opt-out.md)

Par défaut, Adobe Journey Optimizer gère les messages de réponse en anglais standard tels que STOP, UNSTOP et START pour les messages sans fil et à code long, conformément aux normes de l’industrie pour l’intégration native telle que Sinch et Twilio. Ces mots-clés déclenchent généralement une réponse standard automatique de votre fournisseur tiers (par exemple, Twilio, Sinch, etc.). Vous pouvez le confirmer directement auprès de votre fournisseur ou via leur site de documentation.

Aucune procédure n’est requise pour s’assurer que les fonctionnalités d’exclusion des SMS fonctionnent dans Adobe Journey Optimizer, car les réponses de mots-clés STOP, UNSTOP et START seront automatiquement reconnues.

Outre Adobe Journey Optimizer qui arrête l’envoi en fonction de l’état d’exclusion (pour les intégrations directes avec Twilio ou Sinch), la plupart des fournisseurs de passerelle SMS tiennent également une liste bloquée pour vous assurer qu’un SMS ne sera pas délivré à une personne qui a choisi de ne pas l’envoyer. Si vous utilisez un fournisseur autre que Sinch ou Twilio et que vous envoyez un SMS via [canal personnalisé](../building-journeys/using-custom-actions.md), vous devez le confirmer auprès de votre fournisseur.

>[!IMPORTANT]
>
>Les campagnes par SMS peuvent être soumises à diverses exigences de conformité légales en fonction de la nature de votre campagne de messagerie texte, de l’emplacement d’où vous envoyez vos messages texte et de l’emplacement de vos destinataires. <br>Bien qu’Adobe Journey Optimizer gère les messages sur les numéros longs et sans frais comme décrit ci-dessus, vous devez consulter votre service juridique pour vous assurer que votre campagne de messagerie texte est conforme à toutes les exigences de conformité légales applicables.

## Codes courts {#short-codes}

Par défaut, Adobe Journey Optimizer ne prendra pas en charge les mots-clés d’opt-out, d’opt-in ou d’aide pour les numéros de code courts.

Vous devez vous assurer que votre numéro court est conforme à toutes les règles et réglementations du secteur pour la gestion des exclusions.

## Identifiant de l’expéditeur alphanumérique {#alphanumeric}

Les identifiants d’expéditeur alphanumériques sont réservés à la messagerie unidirectionnelle et ne peuvent pas recevoir de messages entrants. Par conséquent, les mots-clés SMS STOP, START et HELP d’Adobe Journey Optimizer ne s’appliquent pas aux identifiants d’expéditeur Alpha. Vous devez fournir d’autres instructions, telles que l’écriture dans l’équipe d’assistance, l’appel d’une ligne téléphonique d’assistance ou l’envoi d’un texto à un autre numéro de téléphone ou code pour permettre aux utilisateurs de se désabonner des messages envoyés par l’intermédiaire de l’ID d’expéditeur alphanumérique.

## Vidéo {#video-sms}

Pour en savoir plus sur le fonctionnement de la prise en charge native des mots-clés entrants (START, STOP et UNSTOP) pour les SMS, reportez-vous à la vidéo suivante :

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
