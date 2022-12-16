---
solution: Journey Optimizer
product: journey optimizer
title: Gestion des entrées de profil
description: Découvrez comment gérer l’entrée de profil.
feature: Journeys
role: User
level: Intermediate
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 100%

---

# Gestion des entrées de profil {#entry-management}

Par défaut, les nouveaux parcours autorisent une rentrée. Vous pouvez désélectionner cette option pour les parcours « uniques » ; c’est le cas, par exemple, si vous souhaitez offrir un cadeau à un utilisateur ou une utilisatrice qui effectue sa première visite dans la boutique. Dans ce cas, vous ne voulez pas que le client puisse rejoindre de nouveau le parcours et rebénéficier de l&#39;offre.

![](assets/journey-re-entrance.png)

Lorsqu’un parcours se termine, son statut passe au mode **[!UICONTROL Fermé]**. Les individus TNew ne peuvent plus intégrer le parcours. En revanche, les personnes qui ont déjà intégré le parcours le terminent normalement.

Au-delà de la temporisation globale par défaut de 30 jours, le statut du parcours passe à **Terminé**.  [En savoir plus](journey-gs.md#global_timeout).


## Parcours unitaires{#entry-unitary}

Les parcours unitaires (commençant par un événement ou une qualification de segment) incluent une barrière de sécurité qui empêche les parcours d’être déclenchés par erreur plusieurs fois pour le même événement. La reprise du profil est temporairement bloquée par défaut pendant 5 minutes. Par exemple, si un événement déclenche un parcours à 12 h 01 pour un profil spécifique et qu’un autre arrive à 12 h 03 (qu’il s’agisse du même événement ou d’un autre déclenchant le même parcours), ce parcours ne reprendra pas pour ce profil.

En outre :

* Si la reprise est activée, un profil peut rejoindre à nouveau plusieurs fois un parcours, mais ne peut pas le faire tant qu’il n’a pas complètement quitté cette instance précédente du parcours.

* Si la reprise est désactivée, un profil ne peut pas rejoindre plusieurs fois le même parcours

## Lire les parcours de segment{#entry-read-segment}

Dans un parcours de segment lu :

* Pour les parcours non récurrents : le profil rejoint une seule fois le parcours.

* Pour les parcours récurrents : le profil intègre le parcours à chaque récurrence, s’il est dans le segment ou a le statut prévu. S’il était toujours dans le parcours depuis une récurrence précédente, il redémarrera au début du parcours.

Dans les parcours d’événement métier commençant par une activité **Lecture de segment** : sachant que ce parcours est basé sur la réception d’un événement métier, si le profil est qualifié dans le segment prévu, il intègrera le parcours de chaque événement métier reçu, ce qui signifie que ce profil peut intégrer le même parcours plusieurs fois, au même moment, mais dans le contexte de divers événements métier.
