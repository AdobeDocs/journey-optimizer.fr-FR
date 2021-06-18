---
title: Liste de suppression
description: Découvrez ce qu’est la liste de suppression, son objectif et ce qu’elle contient.
feature: Délivrabilité
topic: Gestion de contenu
role: User
level: Intermediate
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '643'
ht-degree: 64%

---

# Liste de suppression {#suppression-list}

Une liste de suppression se compose d’adresses email que vous souhaitez exclure de vos diffusions, car l’envoi à ces contacts peut nuire à votre réputation d’envoi et à vos taux de diffusion.

La [!DNL Journey Optimizer]liste de suppression de est gérée au niveau de votre propre environnement.

Il rassemble les adresses et les domaines de courriel qui sont supprimés dans toutes les diffusions d’un seul environnement client, ce qui signifie spécifique à un identifiant d’organisation IMS associé à un ID d’environnement de test.

<!--It gathers spam complaints, hard bounces, and soft bounces that occur consistently.-->

## Pourquoi une liste de suppression ? {#why-suppression-list}

Pour contrôler les emails reçus par les propriétaires de boîte de réception et s’assurer que ces derniers ne reçoivent que les emails souhaités, les fournisseurs d’accès Internet (FAI) et les filtres de spam commercial disposent de leurs algorithmes propriétaires afin de suivre la réputation globale des expéditeurs d’email en fonction des adresses IP et du ou des domaine(s) d’envoi qu’ils utilisent.

Si vous ne tenez pas compte de leurs retours (comme les plaintes contre le spam, les bounces, etc.), ils évalueront votre réputation à la baisse. La liste de suppression vous permet de tenir compte des retours des FAI.

Les destinataires dont les adresses email sont supprimées sont automatiquement exclus de la diffusion des messages. Le taux d’erreur ayant une incidence importante sur la vitesse de diffusion, les envois sont ainsi accélérés.

## Que contient la liste de suppression ? {#what-s-on-suppression-list}

Les adresses email sont ajoutées à la liste de suppression comme suit :

* Tous les **hard bounces** et les **plaintes contre le spam** envoient automatiquement les adresses email correspondantes à la liste de suppression après une seule occurrence.

* **Les** soft bounces et les  **** ignorances temporaires n’envoient pas immédiatement une adresse électronique à la liste de suppression, mais incrémentent un compteur d’erreurs. Plusieurs reprises sont alors effectuées, et lorsque le compteur d&#39;erreurs atteint le seuil, l&#39;adresse est ajoutée à la liste de suppression. En savoir plus sur les [reprises](configuration/retries.md).

<!--You can also manually add an address to the suppression list. Manual category will be available when ability to manually add an address to the suppression list (via API) is released.-->

>[!NOTE]
>
>Les adresses des utilisateurs désabonnés ne peuvent pas être envoyées à la liste de suppression, car ils ne reçoivent pas d’emails de [!DNL Journey Optimizer]. Leur choix est géré au niveau de l’Experience Platform. En savoir plus sur [opt-out](../using/consent.md).
<!--Email addresses of recipients who **unsubscribe** from your sendings are NOT sent to the suppression list. Confirmed by eng.: "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

Pour chaque adresse, la raison de base de la suppression et la catégorie de suppression (soft, hard, etc.) s’affichent dans la liste de suppression. Pour en savoir plus sur l’accès et la gestion de la liste de suppression, voir [cette section](configuration/manage-suppression-list.md).

<!--Once a message is sent, the message logs allow you to view the delivery status for each recipient and the associated failure type and reason. [Learn more about monitoring message execution](monitoring.md). NO ACCESS TO LOGS YET-->

### Échecs de diffusion {#delivery-failures}

Trois types d’erreur sont liés à une diffusion en échec :

* **Hard bounce**. Un hard bounce indique une adresse email non valide (c’est-à-dire une adresse email qui n’existe pas). Un message de rebond du serveur de messagerie de réception indique explicitement que l’adresse n’est pas valide (par exemple, « Utilisateur inconnu »).
* **Soft bounce**. Il s’agit d’un email bounce temporaire qui s’est produit en raison d’une adresse email valide.
* **Ignoré**. Il s’agit d’un email bounce qui s’est produit en raison d’une adresse email valide, mais qui est temporaire (par exemple, une tentative infructueuse de connexion, un problème temporaire lié à du spam (réputation relative aux emails) ou un problème technique temporaire).<!--does it exist in CJM?-->

Un **hard bounce** ajoute automatiquement l’adresse électronique à la liste de suppression.

Une erreur **soft bounce** ou **ignored** qui se produit trop de fois envoie également l’adresse électronique à la liste de suppression après plusieurs tentatives. [En savoir plus sur les reprises](configuration/retries.md)

Si vous continuez à envoyer des emails à ces adresses, cela peut avoir une incidence sur vos taux de diffusion, car cela indique aux FAI que vous ne suivez pas les bonnes pratiques en matière de gestion des listes d’adresses email et que, par conséquent, vous n’êtes peut-être pas un expéditeur digne de confiance.

### Plaintes contre le spam {#spam-complaints}

La liste de suppression collecte les adresses email qui marquent votre message comme spam. Par exemple, si une personne demande à un service client de ne plus jamais recevoir d’emails de votre part, son adresse email est supprimée de votre instance et vous ne pourrez plus envoyer d’emails à cette adresse.

Envoyer un email à des destinataires ayant déposé une plainte contre le spam peut avoir un très fort impact sur votre réputation d’envoi, car cela indique aux FAI que vous envoyez des emails indésirables et que vous n’êtes pas à l’écoute de vos destinataires.

Votre adresse IP ou votre domaine d’envoi peuvent ainsi être bloqués, ce qui pourrait être évité si ces adresses figuraient dans la liste de suppression.

<!--### Unsubscriptions {#unsubscriptions}

Every email sent to recipients must include an unsubscribe link. Upon clicking this link, if a recipient confirms [opting out](consent.md), the corresponding email address is immediately sent to the suppression list. This user must not receive communication from your brand until subscribed again.
NOT TRUE > "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

<!--MOVED to Configuration/Retries section

The threshold is set at three errors:
* For the same delivery, at the third attempt, the address is suppressed.
* If there are different deliveries and two errors occur at least 24 hours apart, the error counter is incremented upon each error and the address is also suppressed at the third attempt.
When a delivery is successful after a retry, the error counter of the address is reinitialized.

### Retries {#retries}

If a message fails due to a temporary bounce of the **Ignored** type, retries will be performed for **3.5 days** from the time the message was added to the email queue.

The minimum delay between retries and the maximum number of retries to be performed are ///managed by the Enhanced MTA/// based on how well an IP is performing, both historically and currently at a given domain.

After 3.5 days, any message in the retry queue will be removed from the queue and sent back as a bounce.-->
