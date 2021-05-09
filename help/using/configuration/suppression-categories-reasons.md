---
title: Catégories et motifs de suppression
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
source-git-commit: a65cefd0bbd15ffa389bac910eaceb40181cb38d
workflow-type: tm+mt
source-wordcount: '138'
ht-degree: 0%

---


# Catégories et motifs de suppression

Lorsqu’un message ne parvient pas à être envoyé à une adresse électronique, Journey Optimizer détermine pourquoi la diffusion a échoué et l’associe à une catégorie de suppression.

La catégorie de suppression détermine quand l&#39;adresse électronique est envoyée à la liste de suppression :

* Soft : Les erreurs douces envoient une adresse à la liste de suppression une fois que le compteur d&#39;erreurs atteint le seuil limite (voir la section -ref Reprises-).
* Difficile : L&#39;adresse électronique est immédiatement envoyée à la liste de suppression.
* Manuel : xxxx. ! comment les adresses sont-elles envoyées manuellement à la liste de suppression ?

Les raisons possibles de l’échec et leur catégorie associée sont les suivantes :

| Raison | Description | Catégorie de suppression |
|------|-----------|----|
| Zone de courrier plein | La boîte aux lettres du destinataire est pleine et n&#39;a pas pu recevoir le message. | Doux |
| Échec du DNS | xxx | Doux |
| Destinataire non valide | xxx | dur |
!- enrichir
