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
source-git-commit: 38d537eb7a14f926cafd2769fd09821eebb1186a
workflow-type: tm+mt
source-wordcount: '634'
ht-degree: 89%

---

# Gestion des droits d’opposition pour les messages texte {#sms-opt-out}

Conformément aux normes et réglementations du secteur, tous les messages SMS de marketing doivent contenir un moyen permettant aux destinataires de se désabonner facilement. [En savoir plus sur la gestion de la confidentialité et du processus d’opt-out](../privacy/opt-out.md)

>[!IMPORTANT]
>
>Les communications par SMS peuvent être soumises à diverses exigences légales qui dépendent de la nature de ces communications, du lieu où vous envoyez vos SMS et de l’emplacement géographique de vos destinataires. Bien qu’Adobe Journey Optimizer traite les messages sur les numéros à code court, long ou les numéros gratuits comme décrit ci-dessous, vous devez consulter votre service juridique pour vous assurer que vos communications SMS sont conformes à toutes les exigences légales applicables.
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

Aucune opération n’est nécessaire pour s’assurer que les fonctionnalités de désinscription par SMS fonctionnent dans Adobe Journey Optimizer, car les réponses par mot-clé STOP, UNSTOP, START, QUIT, CANCEL, END et UNSUBSCRIBE sont automatiquement reconnues. Les statuts d’opt-out des profils sont mis à jour en temps réel dans Adobe Journey Optimizer.

Si vous définissez des mots-clés de désinscription personnalisés dans vos informations d’identification de l’API SMS, ils remplacent les mots-clés entrants par défaut répertoriés ci-dessus. Pour que les mots-clés par défaut tels que STOP, QUIT, CANCEL, END et UNSUBSCRIBE restent fonctionnels, incluez-les explicitement avec vos mots-clés personnalisés dans le champ Mots-clés d&#39;opt-out de votre configuration SMS. Sinon, seuls vos mots-clés personnalisés sont reconnus et les mots-clés par défaut ne déclenchent plus d’actions d’exclusion.

Notez que si un client ou une cliente répond STOP à un SMS, le fournisseur bloque tous les SMS suivants provenant de cet identifiant d’expédition spécifique (code court ou numéro long), y compris les messages transactionnels. Pour assurer la diffusion ininterrompue des SMS transactionnels, utilisez un identifiant d’expédition distinct qui n’a pas fait l’objet d’un opt-out précédemment.


>[!NOTE]
>
>Si vous prévoyez d’utiliser des SMS bidirectionnels (répondre par STOP, QUITTER, etc.), assurez-vous d’abord d’avoir envoyé au moins un SMS unidirectionnel pour établir le mapping du numéro de téléphone avec le profil. Les informations d’identification de fournisseur expirées ou mal configurées empêcheront les mots-clés entrants de mettre à jour le profil d’utilisateur ou d’utilisatrice, ce qui entraînera des enregistrements d’opt-out manquants ou retardés.


## Listes bloquées {#sms-blocklists}

En fonction du statut d’opt-out, Adobe Journey Optimizer peut arrêter l’envoi des messages (pour les intégrations directes à Twilio, Infobip ou Sinch). De plus, la plupart des fournisseurs de passerelles SMS tiennent à jour une liste bloquée, vous garantissant ainsi qu’aucun SMS ne sera envoyé à une personne qui a choisi l’opt-out. Si vous utilisez un fournisseur autre que Sinch ou Twilio et que vous envoyez un SMS par le biais d’un [canal personnalisé](../building-journeys/using-custom-actions.md), vous devez le confirmer auprès de votre fournisseur.


## Codes courts {#short-codes}

Par défaut, les mots-clés relatifs à l’incription ou à l’aide pour les numéros de code court ne sont pas gérés par Adobe Journey Optimizer. Pour garantir la conformité aux réglementations du secteur et aux règles de gestion des désinscriptions, il est essentiel de vérifier que votre code court respecte toutes les directives.

Cependant, Journey Optimizer prend en charge les désinscriptions globales basées sur les mots-clés entrants avec différents ID d’expéditeur ou d’expéditrice.

## ID d’expéditeur alphanumérique {#alphanumeric}

Les ID d’expéditeur alphanumériques peuvent uniquement envoyer des SMS. Ils ne peuvent pas recevoir de messages entrants. Par conséquent, les mots-clés SMS STOP, START et HELP d’Adobe Journey Optimizer ne s’appliquent pas aux ID d’expéditeur alphanumériques. Dès lors, vous devez fournir d’autres instructions aux utilisateurs et utilisatrices pour l’opt-out de SMS. Par exemple, en leur offrant la possibilité d’écrire à l’équipe d’assistance, d’appeler un numéro d’aide ou d’envoyer un SMS à un autre numéro ou code.

## Vidéo {#video-sms}

* La vidéo ci-dessous vous explique comment configurer le double opt-in pour les SMS.

  +++ Voir la vidéo

  >[!VIDEO](https://video.tv.adobe.com/v/3440276/?captions=fre_fr&learn=on)

  +++
