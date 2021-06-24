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
feature: Paramétrage de l’application
topic: Administration
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '215'
ht-degree: 100%

---


# Reprises {#retries}

Lorsqu&#39;un message échoue en raison d&#39;une erreur temporaire **Soft bounce** ou **Ignoré**, plusieurs reprises sont effectuées. Chaque erreur incrémente un compteur d&#39;erreurs. Lorsque ce compteur atteint le seuil limite, l&#39;adresse est ajoutée à la liste de suppression.

Dans la configuration par défaut<!--so can you edit this setting or not?? contradictory information was given-->, le seuil est défini à trois erreurs :

* Pour une même diffusion, à la troisième erreur rencontrée, l&#39;adresse est supprimée.

* S&#39;il existe des diffusions différentes et que deux erreurs se produisent au moins à 24 heures d&#39;intervalle, le compteur d&#39;erreurs est incrémenté à chaque erreur et l&#39;adresse est également supprimée à la troisième tentative.

Si une diffusion réussit après une reprise, le compteur d&#39;erreurs de l&#39;adresse est réinitialisé.

Vous pouvez modifier le seuil limite à l&#39;aide du bouton **[!UICONTROL Modifier]** depuis le menu **[!UICONTROL Canaux]** > **[!UICONTROL Configuration des e-mails]** > **[!UICONTROL Général]**.<!--currently you can edit this in staging // now I see in UI: Suppression rule > Bounce days??? > 4-->

![](../assets/retries-edition.png)

## Durée de la reprise du message {#retry-duration}

Les reprises seront effectuées pendant **3,5 jours** à partir du moment où le message a été ajouté à la file d&#39;attente des e-mails.

Le délai minimum entre les reprises et le nombre maximum de reprises à effectuer sont <!--managed by the Enhanced MTA,--> en fonction des performances d&#39;une adresse IP, à la fois historiquement et sur un domaine donné.

Après 3,5 jours, tout message de la file d&#39;attente des reprises est supprimé de la file d&#39;attente et renvoyé sous forme de bounce.<!--???-->