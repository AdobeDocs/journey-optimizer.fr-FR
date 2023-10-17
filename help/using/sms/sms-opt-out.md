---
solution: Journey Optimizer
product: journey optimizer
title: Gestion du processus de désinscription aux SMS
description: Découvrez comment gérer la désinscription aux SMS
feature: SMS
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: 45f19563c79d298eeec6cb757636a9ce47e54adf
workflow-type: tm+mt
source-wordcount: '447'
ht-degree: 85%

---

# Gestion du processus de désinscription aux SMS {#sms-opt-out}

Conformément aux normes et réglementations du secteur, tous les messages SMS de marketing doivent contenir un moyen permettant aux destinataires de se désabonner facilement. [En savoir plus sur la gestion de la confidentialité et de la désinscription](../privacy/opt-out.md)

>[!IMPORTANT]
>
>Les communications par SMS peuvent être soumises à diverses exigences légales qui dépendent de la nature de ces communications, de l’endroit d’où vous envoyez vos SMS et de celui de vos destinataires. Bien que Adobe Journey Optimizer gère les messages sur les numéros courts, longs et sans frais comme décrit ci-dessous, consultez votre service juridique pour vous assurer que vos communications de messagerie texte sont conformes à toutes les exigences de conformité légales applicables.
>

## Mots-clés entrants natifs {#sms-native-keywords}

Par défaut, Adobe Journey Optimizer gère les messages de réponse en anglais standard suivants pour les codes courts, les codes sans fil et les codes longs : STOP, UNSTOP, START, QUIT, CANCEL, END et UNSUBSCRIBE. Notez que seuls Sinch et Infobip prennent en charge les mots-clés natifs lorsqu’ils sont utilisés avec Journey Optimizer.

Ces mots-clés déclenchent généralement une réponse standard automatique de votre fournisseur tiers. Contactez votre fournisseur ou consultez son site de documentation pour en avoir la confirmation.

Aucune opération n’est nécessaire pour s’assurer que les fonctionnalités de désinscription par SMS fonctionnent dans Adobe Journey Optimizer, car les réponses par mot-clé STOP, UNSTOP, START, QUIT, CANCEL, END, et UNSUBSCRIBE sont automatiquement reconnues. Les statuts de désinscription des profils sont mis à jour en temps réel dans Adobe Journey Optimizer.


## Listes bloquées {#sms-blocklists}

En fonction du statut de désinscription, Adobe Journey Optimizer arrêtera l’envoi des messages (pour les intégrations directes à Twilio ou Sinch). De plus, la plupart des fournisseurs de passerelles SMS tiennent également à jour une liste bloquée, vous garantissant ainsi qu’aucun SMS ne sera envoyé à une personne qui a choisi de se désinscrire. Si vous utilisez un fournisseur autre que Sinch ou Twilio et que vous envoyez un SMS par le biais d’un [canal personnalisé](../building-journeys/using-custom-actions.md), vous devez le confirmer auprès de votre fournisseur.


## Codes courts {#short-codes}

Par défaut, les mots-clés relatifs à l’incription ou à l’aide pour les numéros de code court ne sont pas gérés par Adobe Journey Optimizer. Pour garantir la conformité aux réglementations du secteur et aux règles de gestion des désinscriptions, il est essentiel de vérifier que votre code court respecte toutes les directives.

Cependant, Journey Optimizer prend en charge les désinscriptions globales basées sur les mots-clés entrants avec différents ID d’expéditeur ou d’expéditrice.

## ID d’expéditeur alphanumérique {#alphanumeric}

Les ID d’expéditeur alphanumériques peuvent uniquement envoyer des SMS. Ils ne peuvent pas recevoir de messages entrants. Par conséquent, les mots-clés SMS STOP, START, HELP d’Adobe Journey Optimizer ne s’appliquent pas aux ID d’expéditeur alphanumériques. Dès lors, vous devez fournir d’autres instructions aux utilisateurs pour la désinscription des SMS. Par exemple, en leur offrant la possibilité d’écrire à l’équipe d’assistance, d’appeler un numéro d’aide ou d’envoyer un SMS à un autre numéro ou code.

## Vidéo {#video-sms}

Pour en savoir plus sur le fonctionnement de la prise en charge native des mots-clés entrants (START, STOP et UNSTOP) pour les SMS, regardez la vidéo suivante :

>[!VIDEO](https://video.tv.adobe.com/v/344026?quality=12)
