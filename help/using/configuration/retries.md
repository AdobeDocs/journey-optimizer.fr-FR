---
title: Reprises
description: Découvrez comment les reprises sont effectuées avant d’envoyer une adresse à la liste de suppression
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
feature: Paramétrage de l’application
topic: Administration
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 40%

---


# Reprises {#retries}

Lorsqu’un message échoue en raison d’une erreur **Soft bounce** ou **Ignoré** temporaire, plusieurs reprises sont effectuées. Chaque erreur incrémente un compteur d’erreurs. Lorsque ce compteur atteint le seuil limite, l’adresse est ajoutée à la liste de suppression.

Dans la configuration par défaut <!--so can you edit this setting or not?? contradictory information was given-->, le seuil est défini à trois erreurs :

* Pour une même diffusion, à la troisième erreur rencontrée, l&#39;adresse est supprimée.

* S’il existe des diffusions différentes et que deux erreurs se produisent au moins à 24 heures d’intervalle, le compteur d’erreurs est incrémenté à chaque erreur et l’adresse est également supprimée à la troisième tentative.

Si une diffusion aboutit après une nouvelle tentative, le compteur d&#39;erreurs de l&#39;adresse est réinitialisé.

Vous pouvez modifier le seuil limite à l&#39;aide du bouton **[!UICONTROL Modifier]** depuis le menu **[!UICONTROL Canaux]** > **[!UICONTROL Configuration des emails]** > **[!UICONTROL Général]**.<!--currently you can edit this in staging // now I see in UI: Suppression rule > Bounce days??? > 4-->

![](../assets/retries-edition.png)

## Durée de reprise du message {#retry-duration}

Les reprises seront effectuées pendant **3,5 jours** à partir du moment où le message a été ajouté à la file d’attente des emails.

Le délai minimum entre les reprises et le nombre maximum de reprises à effectuer sont <!--managed by the Enhanced MTA,--> en fonction des performances d’une adresse IP, à la fois historiquement et sur un domaine donné.

Après 3,5 jours, tout message de la file d’attente des reprises est supprimé de la file d’attente et renvoyé sous forme de bounce.<!--???-->