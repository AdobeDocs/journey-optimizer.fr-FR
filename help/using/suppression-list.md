---
title: Liste de suppression
description: Découvrez ce qu'est la liste de suppression, son objectif et ce qu'elle contient.
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
source-git-commit: 9408a93deecfb12f28a0a87c19fa0074c66844a9
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 74%

---

# Liste de suppression {#suppression-list}

Une liste de suppression est constituée d&#39;adresses e-mail que vous souhaitez exclure de vos diffusions, car l&#39;envoi d&#39;e-mails à ces contacts pourrait nuire à votre réputation d&#39;envoi et à vos taux de diffusion.

La liste de suppression de [!DNL Journey Optimizer] est gérée au niveau de votre propre environnement.

Elle rassemble les adresses e-mail et les domaines supprimés de tous les mailings dans un seul environnement client, c&#39;est-à-dire spécifiques à un ID d&#39;organisation IMS associé à un ID Sandbox.

<!--It gathers spam complaints, hard bounces, and soft bounces that occur consistently.-->

## Pourquoi une liste de suppression ?  {#why-suppression-list}

Pour contrôler les emails reçus par les propriétaires de boîte de réception et s&#39;assurer que ces derniers ne reçoivent que les emails souhaités, les fournisseurs d&#39;accès Internet (FAI) et les filtres de spam commercial disposent de leurs algorithmes propriétaires afin de suivre la réputation globale des expéditeurs d&#39;email en fonction des adresses IP et du ou des domaine(s) d&#39;envoi qu&#39;ils utilisent.

Si vous ne tenez pas compte de leurs retours (comme les plaintes contre le spam, les bounces, etc.), ils évalueront votre réputation à la baisse. La liste de suppression vous permet de tenir compte des retours des FAI.

Les destinataires dont les adresses email sont supprimées sont automatiquement exclus de la diffusion des messages. Le taux d&#39;erreur ayant une incidence importante sur la vitesse de diffusion, les envois sont ainsi accélérés.

## Que contient la liste de suppression ?  {#what-s-on-suppression-list}

Les adresses email sont ajoutées à la liste de suppression comme suit :

* Tous les **hard bounces** et les **plaintes contre le spam** envoient automatiquement les adresses email correspondantes à la liste de suppression après une seule occurrence.

* Les **soft bounces**<!--and temporary **ignored** errors--> n’envoient pas immédiatement l’adresse email à la liste de suppression, mais incrémentent un compteur d’erreurs. Plusieurs [reprises](configuration/retries.md) sont alors effectuées, et lorsque le compteur d’erreurs atteint le seuil, l’adresse est ajoutée à la liste de suppression.

* Vous pouvez également [**ajouter manuellement** une adresse ou un domaine](configuration/manage-suppression-list.md#add-addresses-and-domains) à la liste de suppression.

Pour en savoir plus sur les hard bounces et les soft bounces, consultez [cette section](#delivery-failures).

>[!NOTE]
>
>Les adresses des utilisateurs désabonnés ne peuvent pas être envoyées à la liste de suppression, car ils ne reçoivent pas d&#39;e-mails de [!DNL Journey Optimizer]. Leur choix est géré au niveau d&#39;Experience Platform. En savoir plus sur la [désinscription](../using/consent.md).
<!--Email addresses of recipients who **unsubscribe** from your sendings are NOT sent to the suppression list. Confirmed by eng.: "Subscribe and Unsubscribe are handled by the Consent/Subscription service. A user that opts out will not make it to the suppression list – we won’t send them emails."-->

Pour chaque adresse, la raison de base de la suppression et la catégorie de suppression (soft, hard, etc.) s&#39;affichent dans la liste de suppression. Pour en savoir plus sur l&#39;accès et la gestion de la liste de suppression, voir [cette section](configuration/manage-suppression-list.md).

<!--Once a message is sent, the message logs allow you to view the delivery status for each recipient and the associated failure type and reason. [Learn more about monitoring message execution](monitoring.md). NO ACCESS TO LOGS YET-->

>[!NOTE]
>
>Les profils ayant le statut **[!UICONTROL Supprimés]** sont exclus pendant le processus d’envoi du message. Par conséquent, bien que les **rapports de Parcours** indiquent que ces profils ont traversé le parcours ([Lecture de segment](building-journeys/read-segment.md) et [Message](building-journeys/journeys-message.md)), les **Rapports par e-mail** ne les incluront pas dans les mesures **[!UICONTROL Envoyés]** telles qu’elles sont filtrées avant l’envoi par e-mail .
>
>En savoir plus sur [Rapport dynamique](reports/live-report.md) et [Rapport global](reports/global-report.md). Pour connaître la raison de tous les cas d’exclusion, vous pouvez utiliser le [service de requête Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}.

### Échecs de diffusion {#delivery-failures}

Il existe deux types d&#39;erreurs lorsqu&#39;une diffusion échoue :

* **Hard bounce**. Un hard bounce indique une adresse email non valide (c&#39;est-à-dire une adresse email qui n&#39;existe pas). Cela implique un message rebond du serveur de messagerie de réception qui indique explicitement que l’adresse n’est pas valide.
* **Soft bounce**. Il s&#39;agit d&#39;un email bounce temporaire qui s&#39;est produit en raison d&#39;une adresse email valide.
<!--* **Ignored**. This is an email bounce that occurred for a valid email address but is known to be temporary, such as a failed connection attempt, a temporary Spam-related issue (email reputation), or a temporary technical issue.-->

Un **hard bounce** ajoute automatiquement l&#39;adresse e-mail à la liste de suppression.

Un **soft bounce** <!--or an **ignored** error--> qui survient trop de fois envoie également l’adresse électronique à la liste de suppression après plusieurs tentatives. [En savoir plus sur les reprises](configuration/retries.md)

Si vous continuez à envoyer des e-mails à ces adresses, cela peut avoir une incidence sur vos taux de diffusion, car cela indique aux FAI que vous ne suivez pas les bonnes pratiques en matière de gestion des listes d&#39;adresses e-mail et que, par conséquent, vous n&#39;êtes peut-être pas un expéditeur digne de confiance.

### Plaintes contre le spam {#spam-complaints}

La liste de suppression collecte les adresses email qui marquent votre message comme spam. Par exemple, si une personne demande à un service client de ne plus jamais recevoir d&#39;e-mails de votre part, son adresse e-mail est supprimée de votre instance et vous ne pourrez plus envoyer d&#39;e-mails à cette adresse.

Envoyer un email à des destinataires ayant déposé une plainte contre le spam peut avoir un très fort impact sur votre réputation d&#39;envoi, car cela indique aux FAI que vous envoyez des emails indésirables et que vous n&#39;êtes pas à l&#39;écoute de vos destinataires.

Votre adresse IP ou votre domaine d&#39;envoi peuvent ainsi être bloqués, ce qui pourrait être évité si ces adresses figuraient dans la liste de suppression.

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
