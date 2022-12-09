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
source-git-commit: 6014088011c41fd5f673eb3d36fb0609c4a01270
workflow-type: tm+mt
source-wordcount: '759'
ht-degree: 0%

---

# Liste de suppression {#suppression-list}

Une liste de suppression se compose d’adresses et de domaines que vous souhaitez exclure de vos diffusions, car l’envoi à ces contacts peut nuire à votre réputation d’envoi et à vos taux de diffusion.

Le [!DNL Journey Optimizer] la liste de suppression est gérée au niveau de votre propre environnement, c’est-à-dire pour un environnement de test donné.

Il rassemble les adresses électroniques et les domaines qui sont supprimés dans toutes les diffusions d’un seul environnement client, ce qui signifie spécifique à un ID d’organisation associé à un ID d’environnement de test.

>[!NOTE]
>
>Adobe tient à jour une liste des adresses incorrectes connues qui se sont avérées préjudiciables à l’engagement et à la réputation du publipostage, et s’assure que les emails ne leur sont pas remis. Cette liste est gérée dans une liste de suppression globale qui est commune à tous les clients Adobe. Les adresses et les noms de domaine contenus dans la liste de suppression globale sont masqués. Seul le nombre de destinataires exclus est indiqué dans les rapports de diffusion.

## Pourquoi une liste de suppression ? {#why-suppression-list}

Pour contrôler les emails reçus par les propriétaires de leur boîte de réception et s’assurer qu’ils ne reçoivent que ceux qu’ils veulent, les fournisseurs de services Internet (FAI) et les filtres anti-spam commerciaux disposent de leurs algorithmes propriétaires pour suivre la réputation globale des expéditeurs de messagerie en fonction des adresses IP et du ou des domaines d’envoi qu’ils utilisent.

Si vous n’acceptez pas leurs commentaires (comme les plaintes de spam, les rebonds, etc.) en fait, ils vont abaisser votre réputation. La liste de suppression vous aide à respecter les commentaires des FAI.

Les destinataires dont les adresses email sont supprimées sont automatiquement exclus de la diffusion du message. Cela permettra d&#39;accélérer les diffusions, car le taux d&#39;erreur a un effet significatif sur la vitesse de diffusion.

## Qu&#39;y a-t-il sur la liste de suppression ? {#what-s-on-suppression-list}

Les adresses sont ajoutées à la liste de suppression comme suit :

* Tous **hard bounces** et **plaintes relatives au spam** envoyer automatiquement les adresses correspondantes à la liste de suppression après une seule occurrence.

* **Soft bounces** n’envoyez pas immédiatement d’adresse à la liste de suppression, mais incrémentez un compteur d’erreurs. Plusieurs [reprises](../configuration/retries.md) sont ensuite exécutés et, lorsque le compteur d’erreurs atteint le seuil, l’adresse est ajoutée à la liste de suppression.

* Vous pouvez également [**manuellement** ajouter une adresse ou un domaine](../configuration/manage-suppression-list.md#add-addresses-and-domains) à la liste de suppression.

En savoir plus sur les hard bounces et les soft bounces dans [cette section](#delivery-failures).

>[!NOTE]
>
>Les adresses des utilisateurs désabonnés ne peuvent pas être envoyées à la liste de suppression, car ils ne reçoivent pas d’emails de [!DNL Journey Optimizer]. Leur choix est géré au niveau d’Experience Platform. En savoir plus sur [opt-out](../privacy/opt-out.md).

Pour chaque adresse, la raison de base de la suppression et la catégorie de suppression (soft, hard, etc.) s’affichent dans la liste de suppression. En savoir plus sur l’accès et la gestion de la liste de suppression dans [cette section](../configuration/manage-suppression-list.md).

>[!NOTE]
>
>Les profils avec **[!UICONTROL Suppressed]** sont exclus pendant le processus d’envoi des messages. Par conséquent, si la variable **Rapports de parcours** affiche ces profils comme ayant traversé le parcours ([Lecture de segment](../building-journeys/read-segment.md) et [activités de message](../building-journeys/journeys-message.md)), la variable **Rapports par courriel** ne les inclut pas dans la variable **[!UICONTROL Sent]** les mesures telles qu’elles sont filtrées avant l’envoi des emails.
>
>En savoir plus sur la [Rapport en direct](../reports/live-report.md) et [Rapport global](../reports/global-report.md). Pour connaître la raison de tous les cas d’exclusion, vous pouvez utiliser la variable [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html){target=&quot;_blank&quot;}.

### Diffusions en échec {#delivery-failures}

Il existe deux types d&#39;erreurs lorsqu&#39;une diffusion échoue :

* **Hard bounce**. Un hard bounce indique une adresse électronique non valide (c’est-à-dire une adresse électronique qui n’existe pas). Cela implique un message rebond du serveur de messagerie de réception qui indique explicitement que l’adresse n’est pas valide.
* **Soft bounce**. Il s’agit d’un rebond temporaire de courrier électronique qui s’est produit pour une adresse électronique valide.

A **hard bounce** ajoute automatiquement l’adresse électronique à la liste de suppression.

A **soft bounce** <!--or an **ignored** error--> qui se produit trop de fois envoie également l’adresse électronique à la liste de suppression après plusieurs tentatives. [En savoir plus sur les reprises](../configuration/retries.md)

Si vous continuez à envoyer des emails à ces adresses, cela peut affecter vos taux de diffusion, car cela indique aux FAI que vous ne suivez pas les bonnes pratiques de maintenance de la liste d’adresses email et que, par conséquent, vous ne pouvez pas être un expéditeur digne de confiance.

### Demandes de spam {#spam-complaints}

La liste de suppression collecte les adresses email qui marquent votre message comme du spam. Par exemple, si quelqu’un écrit à un service client demandant de ne plus jamais recevoir de courrier de votre part, l’adresse électronique de cette personne sera supprimée de votre instance et vous ne pourrez plus diffuser à cette adresse.

L’envoi aux destinataires après qu’ils ont soumis une plainte de spam peut avoir un impact énorme sur votre réputation d’envoi, car il informe les FAI que vous pouvez envoyer des emails indésirables et ne pas écouter vos destinataires.

Cela peut entraîner le blocage de votre adresse IP ou de votre domaine d’envoi, ce qui peut être évité si ces adresses figurent sur la liste de suppression.
