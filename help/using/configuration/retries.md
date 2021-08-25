---
title: Reprises
description: Découvrez comment les reprises sont effectuées avant d'envoyer une adresse à la liste de suppression
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 79c3c47eb6978f377bf4dc49f787e9a509aa3f61
workflow-type: tm+mt
source-wordcount: '318'
ht-degree: 38%

---


# Reprises {#retries}

Lorsqu’un message électronique échoue en raison d’une erreur **Soft bounce** ou **Ignoré** temporaire, plusieurs reprises sont effectuées. Chaque erreur incrémente un compteur d&#39;erreurs. Lorsque ce compteur atteint le seuil limite, l&#39;adresse est ajoutée à la liste de suppression.

>[!NOTE]
>
>Pour en savoir plus sur les types d&#39;erreurs, consultez la section [Types d&#39;échec de diffusion](../suppression-list.md#delivery-failures) .

Dans la configuration par défaut, le seuil est défini à trois erreurs :

* Pour une même diffusion, à la troisième erreur rencontrée, l&#39;adresse est supprimée.

* S&#39;il existe des diffusions différentes et que deux erreurs se produisent au moins à 24 heures d&#39;intervalle, le compteur d&#39;erreurs est incrémenté à chaque erreur et l&#39;adresse est également supprimée à la troisième tentative.

Si une diffusion réussit après une reprise, le compteur d&#39;erreurs de l&#39;adresse est réinitialisé.

Vous pouvez modifier le seuil limite à l&#39;aide du bouton **[!UICONTROL Modifier]** depuis le menu **[!UICONTROL Canaux]** > **[!UICONTROL Configuration des e-mails]** > **[!UICONTROL Général]**.

![](../assets/retries-edition.png)

<!--The minimum delay between retries and the maximum number of retries to be performed are based on how well an IP is performing, both historically and currently, at a given domain.-->

## Période des reprises {#retry-duration}

La **période de reprise** est la période pendant laquelle tout message électronique de la diffusion ayant rencontré une erreur temporaire ou un soft bounce sera repris.

Par défaut, les reprises seront effectuées pendant **3,5 jours** (ou **84 heures**) à partir du moment où le message a été ajouté à la file d’attente des emails.

Cependant, pour vous assurer que les tentatives de reprise ne sont plus effectuées lorsque cela n’est plus nécessaire, vous pouvez modifier ce paramètre en fonction de vos besoins lors de la création ou de la modification d’un [paramètre prédéfini de message](message-presets.md) s’appliquant au canal email.

Par exemple, vous pouvez définir la période de reprise sur 24 heures pour un email transactionnel relatif à la réinitialisation du mot de passe et contenant un lien valide seulement pendant une journée. De même, pour une vente à minuit, vous pouvez définir une période de reprise de 6 heures.

>[!NOTE]
>
>La période de reprise ne peut pas dépasser 84 heures. La période de reprise minimale est de 6 heures pour les emails marketing et de 10 minutes pour les emails transactionnels.

Découvrez comment ajuster les paramètres de reprise d’email lors de la création d’un paramètre de message prédéfini dans [cette section](message-presets.md#create-message-preset).

<!--After 3.5 days, any message in the retry queue will be removed from the queue and sent back as a bounce.-->