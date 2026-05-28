---
solution: Journey Optimizer
product: journey optimizer
title: Gestion du processus d’opt-out pour les messages mobiles
description: Découvrez comment gérer le processus d’opt-out avec les messages SMS/RCS/MMS
feature: SMS
topic: Content Management
role: User
level: Intermediate
exl-id: 59ea67d9-e90c-4ad0-afb9-d0e0fd868855
TQID: https://experienceleague.adobe.com/mQVaZ8jb-hBBPxDnztkayDEI4vj0KvMTREI0KxOgAf0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d0a62d3c-b79e-47e4-929e-40ef3cffa037
subfeature_v2:
  - id: b3b09fe1-10f1-4793-9f6b-1ca0269eebe7
  - id: a9cf78bf-e9e4-4836-85a5-b6b3cf93bf56
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 674
ht-degree: 80%

---

# Gestion du processus d’opt-out pour les messages mobiles {#sms-opt-out}

Conformément aux normes et réglementations du secteur, tous les messages SMS de marketing doivent contenir un moyen permettant aux destinataires de se désabonner facilement. [En savoir plus sur la gestion de la confidentialité et du processus d’opt-out](../privacy/opt-out.md)

>[!IMPORTANT]
>
>Les communications par messages mobiles peuvent être soumises à diverses exigences légales qui dépendent de leur nature, de l&#39;endroit d&#39;où vous envoyez vos messages mobiles et de celui de vos destinataires. Bien que Adobe Journey Optimizer traite les messages sur des numéros courts, des numéros longs et des numéros gratuits comme décrit ci-dessous, consultez votre service juridique pour vous assurer que vos communications par messagerie mobile sont conformes à toutes les exigences légales applicables.
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

Si vous définissez des mots-clés de d’opt-out personnalisés dans vos informations d’identification de l’API SMS, ils remplacent les mots-clés entrants par défaut répertoriés ci-dessus. Pour que les mots-clés par défaut tels que STOP, QUIT, CANCEL, END et UNSUBSCRIBE continuent de fonctionner, incluez-les explicitement avec vos mots-clés personnalisés dans le champ Mots-clés d’opt-out de votre configuration SMS. Sinon, seuls vos mots-clés personnalisés sont reconnus et les mots-clés par défaut ne déclenchent plus d’actions d’opt-out.

Notez que si un client répond STOP à un Message mobile, le fournisseur bloque tous les SMS suivants à partir de cet identifiant d&#39;expéditeur spécifique (numéro court ou numéro long), y compris les messages transactionnels. Pour assurer la diffusion ininterrompue des SMS transactionnels, utilisez un identifiant d’expédition distinct qui n’a pas fait l’objet d’un opt-out précédemment.


>[!NOTE]
>
>Si vous prévoyez d’utiliser des SMS bidirectionnels (répondre par STOP, QUITTER, etc.), assurez-vous d’abord d’avoir envoyé au moins un SMS unidirectionnel pour établir le mapping du numéro de téléphone avec le profil. Les informations d’identification de fournisseur expirées ou mal configurées empêcheront les mots-clés entrants de mettre à jour le profil d’utilisateur ou d’utilisatrice, ce qui entraînera des enregistrements d’opt-out manquants ou retardés. Les réponses entrantes sont stockées dans le jeu de données système _Jeu de données d’événement d’activité entrant_. [En savoir plus](../data/get-started-datasets.md#system-datasets)


## Listes bloquées {#sms-blocklists}

En fonction du statut d’opt-out, Adobe Journey Optimizer peut arrêter l’envoi des messages (pour les intégrations directes à Twilio, Infobip ou Sinch). De plus, la plupart des fournisseurs de passerelles SMS tiennent à jour une liste bloquée, vous garantissant ainsi qu’aucun SMS ne sera envoyé à une personne qui a choisi l’opt-out. Si vous utilisez un fournisseur autre que Sinch ou Twilio et que vous envoyez un SMS par le biais d’un [canal personnalisé](../building-journeys/using-custom-actions.md), vous devez le confirmer auprès de votre fournisseur.


## Codes courts {#short-codes}

Par défaut, les mots-clés relatifs à l’incription ou à l’aide pour les numéros de code court ne sont pas gérés par Adobe Journey Optimizer. Pour garantir la conformité aux réglementations du secteur et aux règles de gestion des désinscriptions, il est essentiel de vérifier que votre code court respecte toutes les directives.

Cependant, Journey Optimizer prend en charge les désinscriptions globales basées sur les mots-clés entrants avec différents ID d’expéditeur ou d’expéditrice.

## ID d’expéditeur alphanumérique {#alphanumeric}

Les ID d’expéditeur alphanumériques peuvent uniquement envoyer des SMS. Ils ne peuvent pas recevoir de messages entrants. Par conséquent, les mots-clés SMS STOP, START et HELP d’Adobe Journey Optimizer ne s’appliquent pas aux ID d’expéditeur alphanumériques. Dès lors, vous devez fournir d’autres instructions aux utilisateurs et utilisatrices pour l’opt-out de SMS. Par exemple, en leur offrant la possibilité d’écrire à l’équipe d’assistance, d’appeler un numéro d’aide ou d’envoyer un SMS à un autre numéro ou code.

## Vidéo {#video-sms}

* La vidéo ci-dessous vous explique comment configurer le double opt-in pour les SMS.

  +++ Regarder la vidéo

  >[!VIDEO](https://video.tv.adobe.com/v/3427129/?learn=on)

  +++
