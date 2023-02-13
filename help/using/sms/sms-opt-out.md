---
solution: Journey Optimizer
product: journey optimizer
title: Gestion du processus de désinscription aux SMS
description: Découvrez comment gérer la désinscription aux SMS
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: 676e2d6788c8110b76a38e857a62ba9c1be5842c
workflow-type: tm+mt
source-wordcount: '421'
ht-degree: 48%

---

# Gestion du processus de désinscription aux SMS {#sms-opt-out}

Conformément aux normes et réglementations du secteur, tous les messages SMS de marketing doivent contenir un moyen permettant aux destinataires de se désabonner facilement. [En savoir plus sur la gestion de la confidentialité et de la désinscription](../privacy/opt-out.md)

>[!IMPORTANT]
>
>Les communications de messages texte peuvent être soumises à diverses exigences de conformité légale en fonction de leur nature, de l’emplacement d’où vous envoyez vos messages texte et de l’emplacement de vos destinataires. Bien que Adobe Journey Optimizer gère les messages sur les numéros longs et sans frais comme décrit ci-dessous, consultez votre service juridique pour vous assurer que vos communications de messagerie texte sont conformes à toutes les exigences de conformité légales applicables.

## Mots-clés entrants natifs{#sms-native-keywords}

Par défaut, Adobe Journey Optimizer traite les messages de réponse standard en anglais, tels que STOP, UNSTOP et START, pour les numéros gratuits et de code long, conformément aux normes du secteur régissant les intégrations natives telles que Sinch et Twilio.

Ces mots-clés déclenchent généralement une réponse standard automatique de votre fournisseur tiers (tel que Twilio ou Sinch). Contactez votre fournisseur ou consultez leur site de documentation pour en savoir plus.

Aucune procédure n’est requise pour s’assurer que les fonctionnalités d’exclusion des SMS fonctionnent dans Adobe Journey Optimizer lorsque les réponses des mots-clés STOP, UNSTOP et START sont automatiquement reconnues. Les statuts d’exclusion des profils sont mis à jour en temps réel dans Adobe Journey Optimizer.


## Listes bloquées{#sms-blocklists}

Outre l’arrêt par Adobe Journey Optimizer de l’envoi en fonction de l’état d’exclusion (pour les intégrations directes avec Twilio ou Sinch), la plupart des fournisseurs de passerelle SMS conservent également une liste bloquée vous garantissant qu’un SMS n’est pas délivré à une personne qui a choisi de ne pas l’envoyer. Si vous utilisez un fournisseur autre que Sinch ou Twilio, et que vous envoyez un SMS via [canal personnalisé](../building-journeys/using-custom-actions.md), vous devez le confirmer auprès de votre fournisseur.


## Codes courts {#short-codes}

Par défaut, Adobe Journey Optimizer ne prend pas en charge les mots-clés d’opt-out, d’opt-in ou d’aide pour les numéros courts de code. Vous devez vous assurer que votre numéro de code court est conforme à toutes les règles et réglementations du secteur en matière de traitement des désinscriptions.

## ID d’expéditeur alphanumérique {#alphanumeric}

Les ID d’expéditeur alphanumériques peuvent uniquement envoyer des SMS. Ils ne peuvent pas recevoir de messages entrants. Par conséquent, les mots-clés SMS STOP, START, HELP d’Adobe Journey Optimizer ne s’appliquent pas aux ID d’expéditeur alphanumériques. Dès lors, vous devez fournir d’autres instructions aux utilisateurs pour la désinscription des SMS. Par exemple, en leur offrant la possibilité d’écrire à l’équipe d’assistance, d’appeler un numéro d’aide ou d’envoyer un SMS à un autre numéro ou code.

## Vidéo {#video-sms}

Pour en savoir plus sur le fonctionnement de la prise en charge native des mots-clés entrants (START, STOP et UNSTOP) pour les SMS, regardez la vidéo suivante :

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
