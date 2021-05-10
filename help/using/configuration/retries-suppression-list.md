---
title: Reprises avant envoi à la liste de suppression
description: Découvrez comment xxxx
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
translation-type: tm+mt
source-git-commit: 6988a6ab9412e5d27f1ba9d1145cc11c7c06e7b7
workflow-type: tm+mt
source-wordcount: '111'
ht-degree: 0%

---


# Reprises avant envoi à la liste de suppression

Lorsqu’un message échoue en raison d’un échec de rebonds modéré, plusieurs Reprises sont effectuées avant d’envoyer l’adresse électronique à la liste de suppression. Chaque erreur incrémente un compteur d’erreurs. Lorsque ce compteur atteint le seuil limite, l&#39;adresse est placée dans la liste de suppression.

Dans la configuration par défaut, le seuil de limite est défini à 3 erreurs, ce qui signifie que l&#39;adresse est envoyée à la liste de quarantaine à la troisième erreur rencontrée. Si une diffusion réussit après une nouvelle tentative, le compteur d’erreurs est réinitialisé.

Vous pouvez modifier le seuil de limite à l’aide du bouton **[!UICONTROL Modifier]**.

![](../assets/retries-edition.png)
