---
solution: Journey Optimizer
product: journey optimizer
title: Liste de suppression
description: Découvrez comment utiliser la liste de suppression est
feature: Deliverability
topic: Content Management
role: User
level: Intermediate
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 100%

---

# Liste de suppression {#suppression-list}

Une liste de suppression est constituée d’adresses et de domaines que vous souhaitez exclure de vos diffusions, car l’envoi d’e-mails à ces contacts pourrait nuire à votre réputation d’envoi et à vos taux de diffusion.

La liste de suppression [!DNL Journey Optimizer] est gérée au niveau de votre propre environnement, c’est-à-dire pour un sandbox donné.

Elle rassemble les adresses e-mail et les domaines supprimés de tous les mailings dans un seul environnement client, c’est-à-dire spécifiques à un ID d’organisation associé à un ID de sandbox.

>[!NOTE]
>
>Adobe tient à jour une liste des adresses erronées connues qui se sont avérées préjudiciables à l’engagement et à la réputation du publipostage, et s’assure que les e-mails ne leur sont pas remis. Cette liste est gérée dans une liste de suppression globale qui est commune à tous les clients Adobe. Les adresses et les noms de domaine contenus dans la liste de suppression globale sont masqués. Seul le nombre de destinataires exclus est indiqué dans les rapports de diffusion.

## Pourquoi une liste de suppression ? {#why-suppression-list}

Pour contrôler les emails reçus par les propriétaires de boîte de réception et s&#39;assurer que ces derniers ne reçoivent que les emails souhaités, les fournisseurs d&#39;accès Internet (FAI) et les filtres de spam commercial disposent de leurs algorithmes propriétaires afin de suivre la réputation globale des expéditeurs d&#39;email en fonction des adresses IP et du ou des domaine(s) d&#39;envoi qu&#39;ils utilisent.

Si vous ne tenez pas compte de leurs retours (comme les plaintes contre le spam, les bounces, etc.), ils évalueront votre réputation à la baisse. La liste de suppression vous permet de tenir compte des retours des FAI.

Les destinataires dont les adresses email sont supprimées sont automatiquement exclus de la diffusion des messages. Le taux d&#39;erreur ayant une incidence importante sur la vitesse de diffusion, les envois sont ainsi accélérés.

## Que contient la liste de suppression ? {#what-s-on-suppression-list}

Les adresses sont ajoutées à la liste de suppression comme suit :

* Tous les **hard bounces** et les **plaintes contre le spam** envoient automatiquement les adresses correspondantes à la liste de suppression après une seule occurrence.

* Les **soft bounces** n’envoient pas immédiatement l’adresse à la liste de suppression, mais incrémentent un compteur d’erreurs. Plusieurs [reprises](../configuration/retries.md) sont alors effectuées, et lorsque le compteur d’erreurs atteint le seuil, l’adresse est ajoutée à la liste de suppression.

* Vous pouvez également ajouter [**manuellement** une adresse ou un domaine](../configuration/manage-suppression-list.md#add-addresses-and-domains) à la liste de suppression.

Pour en savoir plus sur les hard bounces et les soft bounces, consultez [cette section](#delivery-failures).

>[!NOTE]
>
>Les adresses des utilisateurs désabonnés ne peuvent pas être envoyées à la liste de suppression, car ils ne reçoivent pas d&#39;e-mails de [!DNL Journey Optimizer]. Leur choix est géré au niveau d&#39;Experience Platform. En savoir plus sur la [désinscription](../privacy/opt-out.md).

Pour chaque adresse, la raison de base de la suppression et la catégorie de suppression (soft, hard, etc.) s&#39;affichent dans la liste de suppression. Pour en savoir plus sur l&#39;accès et la gestion de la liste de suppression, voir [cette section](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>Les profils ayant le statut **[!UICONTROL Supprimé]** sont exclus pendant le processus d’envoi du message. Par conséquent, bien que les **rapports de parcours** indiquent que ces profils ont traversé le parcours ([Lecture d’audience](../building-journeys/read-audience.md) et [activités de message](../building-journeys/journeys-message.md)), les **Rapports d’e-mails** ne les incluront pas dans les mesures **[!UICONTROL Envoyé]** étant donné qu’ils sont filtrés avant l’envoi des e-mails.
>
>En savoir plus sur le [Rapport dynamique](../reports/live-report.md) et le [Rapport global](../reports/global-report.md). Pour connaître la raison de tous les cas d’exclusion, vous pouvez utiliser le [service de requête d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html?lang=fr){target="_blank"}.

### Échecs de diffusion {#delivery-failures}

Deux types d’erreur sont liés à une diffusion en échec :

* **Hard bounce**. Un hard bounce indique une adresse email non valide (c&#39;est-à-dire une adresse email qui n&#39;existe pas). Un message de rebond du serveur de messagerie de réception indique explicitement que l’adresse n’est pas valide.
* **Soft bounce**. Il s&#39;agit d&#39;un email bounce temporaire qui s&#39;est produit en raison d&#39;une adresse email valide.

Un **hard bounce** ajoute automatiquement l&#39;adresse e-mail à la liste de suppression.

Un **soft bounce** <!--or an **ignored** error--> qui se produit trop de fois envoie également l’adresse e-mail à la liste de suppression après plusieurs reprises. [En savoir plus sur les reprises](../configuration/retries.md)

Si vous continuez à envoyer des e-mails à ces adresses, cela peut avoir une incidence sur vos taux de diffusion, car cela indique aux FAI que vous ne suivez pas les bonnes pratiques en matière de gestion des listes d&#39;adresses e-mail et que, par conséquent, vous n&#39;êtes peut-être pas un expéditeur digne de confiance.

### Plaintes contre le spam {#spam-complaints}

La liste de suppression collecte les adresses email qui marquent votre message comme spam. Par exemple, si une personne demande à un service client de ne plus jamais recevoir d&#39;e-mails de votre part, son adresse e-mail est supprimée de votre instance et vous ne pourrez plus envoyer d&#39;e-mails à cette adresse.

Envoyer un email à des destinataires ayant déposé une plainte contre le spam peut avoir un très fort impact sur votre réputation d&#39;envoi, car cela indique aux FAI que vous envoyez des emails indésirables et que vous n&#39;êtes pas à l&#39;écoute de vos destinataires.

Votre adresse IP ou votre domaine d&#39;envoi peuvent ainsi être bloqués, ce qui pourrait être évité si ces adresses figuraient dans la liste de suppression.
