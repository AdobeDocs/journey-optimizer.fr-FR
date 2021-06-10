---
title: Surveillance de l’exécution des messages
description: Découvrez les instructions de surveillance et de délivrabilité
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: ht
source-wordcount: '775'
ht-degree: 100%

---

# Gérer les listes de suppression {#manage-suppression-lists}

![](assets/do-not-localize/badge.png)

Une liste de suppression est constituée d’adresses email que vous souhaitez exclure de vos diffusions, car l’envoi d’emails à ces contacts pourrait nuire à votre réputation d’envoi et à vos taux de diffusion.

La **liste de suppression** de Journey Optimizer est gérée au niveau de votre propre environnement. Elle rassemble les plaintes contre le spam, les hard bounces et soft bounces qui surviennent de manière systématique.

## Pourquoi des listes de suppression ? {#why-suppression-lists}

Pour contrôler les emails reçus par les propriétaires de boîte de réception et s’assurer que ces derniers ne reçoivent que les emails souhaités, les fournisseurs d’accès Internet (FAI) et les filtres de spam commercial disposent de leurs algorithmes propriétaires afin de suivre la réputation globale des expéditeurs d’email en fonction des adresses IP et du ou des domaine(s) d’envoi qu’ils utilisent.

Si vous ne tenez pas compte de leurs retours (comme les plaintes contre le spam, les bounces, etc.), ils évalueront votre réputation à la baisse. La liste de suppression vous permet de tenir compte des retours des FAI.

Les destinataires dont les adresses email sont supprimées sont automatiquement exclus de la diffusion des messages. Le taux d’erreur ayant une incidence importante sur la vitesse de diffusion, les envois sont ainsi accélérés.

### Plaintes contre le spam {#spam-complaints}

La liste de suppression collecte les adresses email qui marquent votre message comme spam. Envoyer un email à des destinataires ayant déposé une plainte contre le spam peut avoir un très fort impact sur votre réputation d’envoi, car cela indique aux FAI que vous envoyez des emails indésirables et que vous n’êtes pas à l’écoute de vos destinataires.

Votre adresse IP ou votre domaine d’envoi peuvent ainsi être bloqués, ce qui pourrait être évité si ces adresses figuraient dans la liste de suppression.

### Bounces {#bounces}

La liste de suppression contient aussi les adresses email faisant trop souvent l’objet de hard bounces ou de soft bounces. Si vous continuez à envoyer des emails à ces adresses, cela peut avoir une incidence sur vos taux de diffusion, car cela indique aux FAI que vous ne suivez pas les bonnes pratiques en matière de gestion des listes d’adresses email et que, par conséquent, vous n’êtes peut-être pas un expéditeur digne de confiance.

## Gestion des listes de suppression {#suppression-list-management}

La liste de suppression de Journey Optimizer rassemble les adresses email et les domaines supprimés de tous les mailings **dans un seul environnement client**, c’est-à-dire spécifiques à un ID d’organisation IMS associé à un ID Sandbox.

La liste de suppression vous permet de collecter automatiquement :
* Les adresses email non valides ou qui font l’objet de soft bounces systématiques et qui sont susceptibles de nuire à votre réputation en matière d’emails si vous continuez à les inclure dans vos diffusions.
* Les destinataires qui déposent une plainte pour spam contre l’un de vos emails.

Par exemple, si une personne demande à un service client de ne plus jamais recevoir d’emails de votre part, son adresse email est supprimée de votre instance et vous ne pourrez plus envoyer d’emails à cette adresse.

<!--For each address, the basic reason for suppression (soft bounces, a hard bounce or a spam complaint) will be shown in the Suppression list.-->

### Échecs de diffusion {#delivery-failures}

<!--Once a message is sent, the message logs allow you to view the delivery status for each recipient and the associated failure type and reason. [Learn more about monitoring message execution](monitoring.md). NO ACCESS TO LOGS YET-->

Trois types d’erreur sont liés à une diffusion en échec :

* **Hard bounce**. Un hard bounce indique une adresse email non valide (c’est-à-dire une adresse email qui n’existe pas). Un message de rebond du serveur de messagerie de réception indique explicitement que l’adresse n’est pas valide (par exemple, « Utilisateur inconnu »).
* **Soft bounce**. Il s’agit d’un email bounce temporaire qui s’est produit en raison d’une adresse email valide.
* **Ignoré**. Il s’agit d’un email bounce qui s’est produit en raison d’une adresse email valide, mais qui est temporaire (par exemple, une tentative infructueuse de connexion, un problème temporaire lié à du spam (réputation relative aux emails) ou un problème technique temporaire).

Les hard bounces et les soft bounces peuvent être une raison pour laquelle une adresse email est automatiquement ajoutée à la liste de suppression.

### Que contient la liste de suppression ? {#what-s-on-suppression-list}

Les adresses email sont ajoutées à la liste de suppression comme suit :

* Tous les **hard bounces** et les **plaintes contre le spam** envoient automatiquement les adresses email correspondantes à la liste de suppression après une seule occurrence.

* Les **soft bounces** n’envoient pas immédiatement l’adresse email à la liste de suppression, mais incrémentent un compteur d’erreurs. Lorsque le compteur d’erreurs atteint le seuil, l’adresse est ajoutée à la liste de suppression.

   Le seuil est défini sur trois erreurs :
   * Pour une même diffusion, à la troisième tentative, l’adresse est supprimée.
   * S’il existe des diffusions différentes et que deux erreurs se produisent au moins à 24 heures d’intervalle, le compteur d’erreurs est incrémenté à chaque erreur et l’adresse est également supprimée à la troisième tentative.

   Lorsqu’une diffusion réussit après une reprise, le compteur d’erreurs de l’adresse est réinitialisé.

### Reprises {#retries}

Si un message échoue en raison d’un bounce temporaire de type **Ignoré**, des reprises ont lieu pendant **3,5 jours** à partir du moment où le message est ajouté à la file d’attente d’emails.

Le délai minimum entre les reprises et le nombre maximum de reprises à effectuer sont <!--managed by the Enhanced MTA,--> en fonction des performances d’une adresse IP, à la fois historiquement et sur un domaine donné.

Après 3,5 jours, tout message de la file d’attente des reprises est supprimé de la file d’attente et renvoyé sous forme de bounce.
