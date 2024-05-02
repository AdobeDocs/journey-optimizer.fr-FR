---
solution: Journey Optimizer
product: journey optimizer
title: Gestion des droits d’opposition pour les messages texte
description: Découvrez comment gérer les droits d’opposition avec les messages SMS/MMS.
feature: SMS
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
source-git-commit: 0571a11eabffeb5e318bebe341a8df18da7db598
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 89%

---

# Gestion des droits d’opposition pour les messages texte {#sms-opt-out}

Conformément aux normes et réglementations du secteur, tous les messages SMS de marketing doivent contenir un moyen permettant aux destinataires de se désabonner facilement. [En savoir plus sur la gestion de la confidentialité et de la désinscription](../privacy/opt-out.md)

>[!IMPORTANT]
>
>Les communications par SMS peuvent être soumises à diverses exigences légales qui dépendent de la nature de ces communications, de l’endroit d’où vous envoyez vos SMS et de celui de vos destinataires. Bien qu’Adobe Journey Optimizer traite les messages sur les numéros de code long, court et les numéros gratuits comme décrit ci-dessus, vous devez consulter votre service juridique pour vous assurer que vos communications par SMS sont conformes à toutes les exigences légales applicables.
>

## Mots-clés entrants natifs {#sms-native-keywords}

>[!NOTE]
>
> Seuls Sinch et Infobip prennent en charge les mots-clés natifs lorsqu’ils sont utilisés avec Journey Optimizer.

Par défaut, Adobe Journey Optimizer gère les messages de réponse en anglais standard suivants pour les messages sans frais, et à code long et court :

* **Opt-out** : STOP (arrêter), QUIT (quitter), CANCEL (annuler), END (terminer), UNSUBSCRIBE (se désabonner), NO (non).
* **Opt-in** : SUBSCRIBE (s’abonner), YES (oui), UNSTOP (redémarrer), START (démarrer), CONTINUE (continuer), RESUME (reprendre), BEGIN (commencer).
* **Aide** : HELP (aide).

Ces mots-clés déclenchent généralement une réponse standard automatique de votre fournisseur tiers. Contactez votre fournisseur ou consultez son site de documentation pour en avoir la confirmation.

Lors de l’utilisation d’Infobip, assurez-vous que l’action Transfert est définie sur la configuration de tirage.

Aucune opération n’est nécessaire pour s’assurer que les fonctionnalités de désinscription par SMS fonctionnent dans Adobe Journey Optimizer, car les réponses par mot-clé STOP, UNSTOP, START, QUIT, CANCEL, END, et UNSUBSCRIBE sont automatiquement reconnues. Les statuts de désinscription des profils sont mis à jour en temps réel dans Adobe Journey Optimizer.


## Listes bloquées {#sms-blocklists}

Outre l’arrêt par Adobe Journey Optimizer de l’envoi en fonction de l’état d’exclusion (pour les intégrations directes avec Twilio, Infobip ou Sinch), la plupart des fournisseurs de passerelle SMS conservent également une liste bloquée vous garantissant qu’un SMS n’est pas délivré à une personne qui a choisi de se désinscrire. Si vous utilisez un fournisseur autre que Sinch ou Twilio et que vous envoyez un SMS par le biais d’un [canal personnalisé](../building-journeys/using-custom-actions.md), vous devez le confirmer auprès de votre fournisseur.


## Codes courts {#short-codes}

Par défaut, les mots-clés relatifs à l’incription ou à l’aide pour les numéros de code court ne sont pas gérés par Adobe Journey Optimizer. Pour garantir la conformité aux réglementations du secteur et aux règles de gestion des désinscriptions, il est essentiel de vérifier que votre code court respecte toutes les directives.

Cependant, Journey Optimizer prend en charge les désinscriptions globales basées sur les mots-clés entrants avec différents ID d’expéditeur ou d’expéditrice.

## ID d’expéditeur alphanumérique {#alphanumeric}

Les ID d’expéditeur alphanumériques peuvent uniquement envoyer des SMS. Ils ne peuvent pas recevoir de messages entrants. Par conséquent, les mots-clés SMS STOP, START, HELP d’Adobe Journey Optimizer ne s’appliquent pas aux ID d’expéditeur alphanumériques. Dès lors, vous devez fournir d’autres instructions aux utilisateurs et utilisatrices pour l’opt-out de SMS. Par exemple, en leur offrant la possibilité d’écrire à l’équipe d’assistance, d’appeler un numéro d’aide ou d’envoyer un SMS à un autre numéro ou code.

## Vidéo {#video-sms}

* La vidéo ci-dessous vous explique comment configurer le double opt-in pour les SMS.

+++ Voir la vidéo

  >[!VIDEO](https://video.tv.adobe.com/v/3427129/?learn=on)

+++
