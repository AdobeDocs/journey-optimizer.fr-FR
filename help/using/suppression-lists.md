---
title: Surveillance de l’exécution des messages
description: Apprenez à surveiller et à fournir des directives
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '775'
ht-degree: 0%

---

# Gérer les listes de suppression {#manage-suppression-lists}

![](assets/do-not-localize/badge.png)

Une liste de suppression consiste en des adresses électroniques que vous souhaitez exclure de vos diffusions, car l&#39;envoi à ces contacts peut nuire à votre réputation d&#39;envoi et à vos taux de diffusion.

La liste de suppression **Journey Optimizer** est gérée au niveau de votre propre environnement. Il recueille les plaintes de spam, les rebonds durs et les rebonds doux qui se produisent de manière constante.

## Pourquoi supprimer les listes ? {#why-suppression-lists}

Pour contrôler les courriers électroniques reçus par leurs propriétaires de boîtes de réception et s&#39;assurer qu&#39;ils ne reçoivent que ceux qu&#39;ils veulent, les prestataires Internet (FAI) et les filtres de spam commercial disposent de leurs algorithmes propriétaires pour suivre la réputation globale des expéditeurs de courriels en fonction des adresses IP et des domaines d&#39;envoi qu&#39;ils utilisent.

Si vous ne tenez pas compte de leurs commentaires (tels que les plaintes de spam, les rebonds, etc.) en conséquence, ils évalueront votre réputation à la baisse. La liste de suppression vous aide à respecter les commentaires des FAI.

Les destinataires dont les adresses électroniques sont supprimées sont automatiquement exclus de la diffusion des messages. Cela permettra d&#39;accélérer les diffusions, car le taux d&#39;erreur a un effet significatif sur la vitesse de diffusion.

### Plaintes de spam {#spam-complaints}

La liste de suppression collecte les adresses électroniques qui marquent votre message comme indésirable. L&#39;envoi à des destinataires après qu&#39;ils ont déposé une plainte de spam peut avoir un impact énorme sur votre réputation d&#39;envoi, car il informe les FAI que vous pouvez envoyer des courriels indésirables et ne pas écouter vos destinataires.

Cela peut entraîner le blocage de votre adresse IP ou du domaine d’envoi, ce qui peut être évité si ces adresses sont sur la liste de suppression.

### Rebonds {#bounces}

En outre, la liste de suppression contient des adresses électroniques qui rebondissent fortement ou rebondissent trop souvent. Si vous continuez à envoyer ces adresses, cela peut avoir une incidence sur vos taux de diffusion, car cela indique aux FAI que vous ne suivez pas les bonnes pratiques de maintenance des listes d&#39;adresses de courriel et que, par conséquent, vous ne pouvez pas être un expéditeur digne de confiance.

## Gestion des listes de suppression {#suppression-list-management}

La liste de suppression de Journey Optimizer rassemble les adresses et les domaines de courriel qui sont supprimés pour toutes les envois **dans un seul environnement client**, ce qui signifie qu&#39;il s&#39;agit d&#39;un ID d&#39;organisation IMS associé à un ID de sandbox.

La liste de suppression vous permet de collecter automatiquement :
* Les adresses électroniques non valides ou qui rebondissent régulièrement et peuvent nuire à la réputation de votre messagerie si vous continuez à les inclure dans vos diffusions.
* Destinataires qui signalent un spam d&#39;une sorte contre l&#39;un de vos courriels.

Par exemple, si quelqu’un écrit à un service à la clientèle demandant de ne plus jamais recevoir de courrier de votre part, l’adresse électronique de cette personne sera supprimée sur l’ensemble de votre instance et vous ne pourrez plus livrer à cette adresse.

<!--For each address, the basic reason for suppression (soft bounces, a hard bounce or a spam complaint) will be shown in the Suppression list.-->

### Échec de la diffusion {#delivery-failures}

<!--Once a message is sent, the message logs allow you to view the delivery status for each recipient and the associated failure type and reason. [Learn more about monitoring message execution](monitoring.md). NO ACCESS TO LOGS YET-->

Il existe trois types d’erreurs lorsqu’une diffusion échoue :

* **Rebond** dur. Un rebond dur indique une adresse électronique non valide (c’est-à-dire une adresse électronique qui n’existe pas). Ceci implique un message de retour du serveur de messagerie de réception qui indique explicitement que l&#39;adresse n&#39;est pas valide, tel que &quot;utilisateur inconnu&quot;.
* **Rebonds** doux. Il s’agit d’un rebond temporaire de courrier électronique survenu pour une adresse électronique valide.
* **Ignoré**. Il s’agit d’un rebond de courrier électronique qui s’est produit pour une adresse électronique valide, mais qui est connu pour être temporaire, tel qu’une tentative de connexion ayant échoué, un problème temporaire lié au spam (réputation de courrier électronique) ou un problème technique temporaire.

Les rebonds durs et les rebonds en douceur peuvent être une raison pour laquelle une adresse électronique doit être automatiquement ajoutée à la liste de suppression.

### Qu&#39;y a-t-il sur la liste de suppression ? {#what-s-on-suppression-list}

Les adresses électroniques sont ajoutées à la liste de suppression comme suit :

* Toutes les **rebonds durs** et **plaintes de spam** envoient automatiquement les adresses électroniques correspondantes à la liste de suppression après une seule occurrence.

* **Les** virements douces n’envoient pas immédiatement une adresse électronique à la liste de suppression, mais incrémentent un compteur d’erreurs. Lorsque le compteur d’erreurs atteint le seuil, l’adresse est ajoutée à la liste de suppression.

   Le seuil est défini à trois erreurs :
   * Pour la même diffusion, à la troisième tentative, l&#39;adresse est supprimée.
   * S’il existe des diffusions différentes et que deux erreurs se produisent au moins à 24 heures d’intervalle, le compteur d’erreurs est incrémenté à chaque erreur et l’adresse est également supprimée à la troisième tentative.

   Lorsqu’une diffusion réussit après une nouvelle tentative, le compteur d’erreurs de l’adresse est réinitialisé.

### Reprises {#retries}

Si un message échoue en raison d’un rebond temporaire du type **Ignoré**, des Reprises sont effectuées pendant **3,5 jours** à partir du moment où le message a été ajouté à la file d’attente de courrier électronique.

Le délai minimal entre les Reprises et le nombre maximal de Reprises à exécuter est <!--managed by the Enhanced MTA,--> en fonction de l&#39;efficacité d&#39;une IP, à la fois historiquement et actuellement dans un domaine donné.

Au bout de 3,5 jours, tout message de la file d’attente des nouvelles tentatives est supprimé de la file d’attente et renvoyé sous forme de rebond.
