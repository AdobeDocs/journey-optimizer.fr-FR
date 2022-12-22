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
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: ht
source-wordcount: '415'
ht-degree: 100%

---

# Gestion du processus de désinscription aux SMS {#sms-opt-out}

Conformément aux normes et réglementations du secteur, tous les messages SMS de marketing doivent contenir un moyen permettant aux destinataires de se désabonner facilement. [En savoir plus sur la gestion de la confidentialité et de la désinscription](../privacy/opt-out.md)

Par défaut, Adobe Journey Optimizer traite les messages de réponse standard en anglais, tels que STOP, UNSTOP et START, pour les numéros gratuits et de code long, conformément aux normes du secteur régissant les intégrations natives telles que Sinch et Twilio. Ces mots-clés déclenchent généralement une réponse standard automatique de votre fournisseur tiers (par exemple, Twilio, Sinch, etc.). Contactez votre fournisseur ou consultez leur site de documentation pour en savoir plus.

Aucune opération n’est nécessaire pour s’assurer que les fonctionnalités de désinscription par SMS fonctionnent dans Adobe Journey Optimizer, car les réponses par mot-clé STOP, UNSTOP et START sont automatiquement reconnues.

En fonction du statut de désinscription, Adobe Journey Optimizer arrêtera l’envoi des messages (pour les intégrations directes avec Twilio ou Sinch). De plus, la plupart des fournisseurs de passerelles SMS tiennent également à jour une liste bloquée, vous garantissant ainsi qu’un SMS ne sera pas envoyé à une personne qui a choisi de se désinscrire. Si vous utilisez un fournisseur autre que Sinch ou Twilio et que vous envoyez un SMS par le biais d’un [canal personnalisé](../building-journeys/using-custom-actions.md), vous devez le confirmer auprès de votre fournisseur.

>[!IMPORTANT]
>
>Les campagnes par SMS peuvent être soumises à diverses exigences légales, qui dépendent de la nature de vos campagnes par SMS, de l’endroit d’où vous envoyez vos messages texte et de celui de vos destinataires. <br>Bien qu’Adobe Journey Optimizer traite les messages sur les numéros de code long et gratuits comme décrit ci-dessus, vous devez consulter votre service juridique pour vous assurer que votre campagne par SMS est conforme à toutes les exigences légales applicables.

## Codes courts {#short-codes}

Par défaut, Adobe Journey Optimizer ne prend pas en charge les mots-clés relatifs à la désinscription, l’inscription ou l’aide pour les numéros de code court.

Vous devez vous assurer que votre numéro de code court est conforme à toutes les règles et réglementations du secteur en matière de traitement des désinscriptions.

## ID d’expéditeur alphanumérique {#alphanumeric}

Les ID d’expéditeur alphanumériques peuvent uniquement envoyer des SMS. Ils ne peuvent pas recevoir de messages entrants. Par conséquent, les mots-clés SMS STOP, START, HELP d’Adobe Journey Optimizer ne s’appliquent pas aux ID d’expéditeur alphanumériques. Dès lors, vous devez fournir d’autres instructions aux utilisateurs pour la désinscription des SMS. Par exemple, en leur offrant la possibilité d’écrire à l’équipe d’assistance, d’appeler un numéro d’aide ou d’envoyer un SMS à un autre numéro ou code.

## Vidéo {#video-sms}

Pour en savoir plus sur le fonctionnement de la prise en charge native des mots-clés entrants (START, STOP et UNSTOP) pour les SMS, regardez la vidéo suivante :

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
