---
solution: Journey Optimizer
product: journey optimizer
title: Liste de suppression
description: Découvrez comment utiliser la liste de suppression est
feature: Deliverability
topic: Content Management
role: Admin
level: Intermediate, Experienced
exl-id: a4653378-b70f-454c-a446-ab4a14d2580a
TQID: https://experienceleague.adobe.com/cUhagNPBmqDDLIu-h9qcSSltOkbXTXx-pBh-rOskGr0
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: a9f73820-6899-47c2-a597-3fec28ab756aid: b49ca41f-eb7a-4f4b-abeb-a97c06fd0c04
subfeature_v2: id: d145add9-d5b9-481b-aa8a-e15e6bb7f813id: a7289281-9ae4-47b1-b8cf-4028b98af776id: b5afe8bf-bda6-41b5-ba06-922638872d63
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 7f28f19b11ead867b0851943fdd997dcc3af170b
workflow-type: tm+mt
source-wordcount: 870
ht-degree: 89%

---

# Liste de suppression {#suppression-list}

>[!BEGINSHADEBOX]

**Sur cette page :** Découvrez comment la liste de suppression exclut des adresses e-mail et des domaines spécifiques de vos diffusions pour protéger votre réputation d’envoi et vos taux de diffusion.

>[!ENDSHADEBOX]

Une liste de suppression est constituée d’adresses et de domaines que vous souhaitez exclure de vos diffusions, car l’envoi d’e-mails à ces contacts pourrait nuire à votre réputation d’envoi et à vos taux de diffusion.

La liste de suppression [!DNL Journey Optimizer] est gérée au niveau de votre propre environnement, c’est-à-dire pour un sandbox donné.

Elle rassemble les adresses e-mail et les domaines supprimés de tous les mailings dans un seul environnement client, c’est-à-dire spécifiques à un ID d’organisation associé à un ID de sandbox.

>[!NOTE]
>
>Adobe tient à jour une liste des adresses erronées connues qui se sont avérées préjudiciables à l’engagement et à la réputation du publipostage, et s’assure que les e-mails ne leur sont pas remis. Cette liste est gérée dans une liste de suppression globale qui est commune à tous les clients Adobe. Les adresses et les noms de domaine contenus dans la liste de suppression globale sont masqués. Seul le nombre de destinataires exclus est indiqué dans les rapports de diffusion.

En outre, vous pouvez tirer parti de l’**API REST de suppression** Journey Optimizer pour contrôler vos messages sortants à l’aide des listes de suppression et des listes autorisées. [Découvrez comment utiliser l’API REST de suppression.](https://developer.adobe.com/journey-optimizer-apis/references/suppression){target="_blank"}

## Pourquoi une liste de suppression ? {#why-suppression-list}

Pour contrôler les e-mails reçus par les propriétaires de boîte de réception et s&#39;assurer que ces derniers ne reçoivent que les e-mails souhaités, les fournisseurs d&#39;accès Internet (FAI) et les filtres de spam commercial disposent de leurs algorithmes propriétaires afin de suivre la réputation globale des expéditeurs d&#39;e-mail en fonction des adresses IP et du ou des domaine(s) d&#39;envoi qu&#39;ils utilisent.

Si vous ne tenez pas compte de leurs commentaires (comme les plaintes contre le spam, les bounces, etc.) ils évalueront votre réputation à la baisse. La liste de suppression vous permet de tenir compte des retours des FAI.

Les destinataires dont les adresses e-mail sont supprimées sont automatiquement exclus de la diffusion des messages. Le taux d&#39;erreur ayant une incidence importante sur la vitesse de diffusion, les envois sont ainsi accélérés.

## Que contient la liste de suppression ? {#what-s-on-suppression-list}

Les adresses sont ajoutées à la liste de suppression comme suit :

* Tous les **rebonds définitifs** et **plaintes relatives aux spams** envoient automatiquement les adresses correspondantes à la liste de suppression après une seule occurrence. En savoir plus sur les plaintes relatives aux spams dans [cette section](#spam-complaints).

* Les **rebonds temporaires** n’envoient pas immédiatement l’adresse à la liste de suppression, mais incrémentent un compteur d’erreurs. Plusieurs [reprises](../configuration/retries.md) sont alors effectuées, et lorsque le compteur d’erreurs atteint le seuil, l’adresse est ajoutée à la liste de suppression.

* Vous pouvez également ajouter [**manuellement** une adresse ou un domaine](../configuration/manage-suppression-list.md#add-addresses-and-domains) à la liste de suppression.

En savoir plus sur les rebonds définitifs et les rebonds temporaires dans [cette section](#delivery-failures).

>[!NOTE]
>
>Les adresses des utilisateurs désabonnés ne peuvent pas être envoyées à la liste de suppression, car ils ne reçoivent pas d&#39;e-mails de [!DNL Journey Optimizer]. Leur choix est géré au niveau d&#39;Experience Platform. En savoir plus sur l’[opt-out](../privacy/opt-out.md).

Pour chaque adresse, la raison de base de la suppression et la catégorie de suppression (soft, hard, etc.) s’affichent dans la liste de suppression. En savoir plus sur l’accès et la gestion de la liste de suppression dans [cette section](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>Les profils ayant le statut **[!UICONTROL Supprimé]** sont exclus pendant le processus d’envoi du message. Par conséquent, bien que les **rapports de parcours** indiquent que ces profils ont traversé le parcours ([Lecture d’audience](../building-journeys/read-audience.md) et [activités de message](../building-journeys/journey-action.md)), les **rapports d’e-mails** ne les incluront pas dans les mesures **[!UICONTROL Envoyé]** étant donné qu’ils sont filtrés avant l’envoi des e-mails.
>
>En savoir plus sur le [rapport dynamique](../reports/live-report.md) et le [rapport Customer Journey Analytics](../reports/report-gs-cja.md). Pour connaître la raison de tous les cas d’exclusion, vous pouvez utiliser le [service de requête de ](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html?lang=fr){target="_blank"}.

### Échecs de diffusion {#delivery-failures}

Deux types d’erreur sont liés à une diffusion en échec :

* **Rebond définitif**. Un rebond définitif indique une adresse e-mail non valide (c’est-à-dire une adresse e-mail qui n’existe pas). Un message de rebond du serveur de messagerie de réception indique explicitement que l’adresse n’est pas valide.
* **Rebond temporaire**. Il s’agit d’un e-mail rejeté temporairement pour une adresse e-mail valide.

Un **rebond définitif** ajoute automatiquement l’adresse e-mail à la liste de suppression.

Un **soft bounce** <!--or an **ignored** error--> qui se produit trop de fois envoie également l’adresse e-mail à la liste de suppression après plusieurs reprises. [En savoir plus sur les reprises](../configuration/retries.md)

Si vous continuez à envoyer des e-mails à ces adresses, cela peut avoir une incidence sur vos taux de diffusion, car cela indique aux FAI que vous ne suivez pas les bonnes pratiques en matière de gestion des listes d&#39;adresses e-mail et que, par conséquent, vous n&#39;êtes peut-être pas un expéditeur digne de confiance.

### Plaintes contre le spam {#spam-complaints}

La liste de suppression collecte les adresses e-mail qui marquent votre message comme spam. Par exemple, si une personne demande à un service client de ne plus jamais recevoir d&#39;e-mails de votre part, son adresse e-mail est supprimée de votre instance et vous ne pourrez plus envoyer d&#39;e-mails à cette adresse.

Envoyer un e-mail à des destinataires ayant déposé une plainte contre le spam peut avoir un très fort impact sur votre réputation d&#39;envoi, car cela indique aux FAI que vous envoyez des e-mails indésirables et que vous n&#39;êtes pas à l&#39;écoute de vos destinataires.

Votre adresse IP ou votre domaine d&#39;envoi peuvent ainsi être bloqués, ce qui pourrait être évité si ces adresses figuraient dans la liste de suppression.

Certains FAI proposent un système de feedback (FBL) qui permet à l’expéditeur ou l’expéditrice de l’e-mail de recevoir un avertissement automatique lorsque l’utilisateur ou l’utilisatrice qui reçoit un e-mail choisit de le marquer comme spam. [En savoir plus](deliverability.md#feedback-loops)
