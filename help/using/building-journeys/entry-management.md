---
solution: Journey Optimizer
product: journey optimizer
title: Gestion des entrées de profil
description: Découvrez comment gérer l’entrée de profil
feature: Journeys
role: User
level: Intermediate
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: tm+mt
source-wordcount: '346'
ht-degree: 59%

---

# Gestion des entrées de profil {#entry-management}

Par défaut, les nouveaux parcours autorisent une rentrée. Vous pouvez désélectionner cette option pour les parcours « uniques » ; c&#39;est le cas, par exemple, si vous souhaitez offrir un cadeau à un utilisateur qui effectue sa première visite dans la boutique. Dans ce cas, vous ne voulez pas que le client puisse rejoindre de nouveau le parcours et rebénéficier de l&#39;offre.

![](assets/journey-re-entrance.png)

Lorsqu’un parcours se termine, son état est **[!UICONTROL Fermé]**. TNew ne peut plus entrer dans le parcours. Les personnes déjà dans le parcours terminent le parcours normalement.

Après le délai d’expiration global par défaut de 30 jours, le parcours passe à la variable **Terminé** statut.  [En savoir plus](journey-gs.md#global_timeout).


## Parcours unitaires{#entry-unitary}

Les parcours unitaires (commençant par un événement ou une qualification de segment) incluent une barrière de sécurité qui empêche les parcours d’être déclenchés par erreur plusieurs fois pour le même événement. La reprise du profil est temporairement bloquée par défaut pendant 5 minutes. Par exemple, si un événement déclenche un parcours à 12 h 01 pour un profil spécifique et qu’un autre arrive à 12 h 03 (qu’il s’agisse du même événement ou d’un autre déclenchant le même parcours), ce parcours ne reprendra pas pour ce profil.

En outre :

* Si la reprise est activée, un profil peut rejoindre à nouveau plusieurs fois un parcours, mais ne peut pas le faire tant qu’il n’a pas complètement quitté cette instance précédente du parcours.

* Si la reprise est désactivée, un profil ne peut pas rejoindre plusieurs fois le même parcours

## Lecture de parcours de segment{#entry-read-segment}

Dans un parcours de segment lu :

* Pour les parcours non récurrents : le profil rejoint une seule fois le parcours.

* Pour les parcours récurrents : le profil entre dans le parcours de chaque périodicité, s’il est dans l’état segment/attendu. S’il était toujours dans le parcours d&#39;une précédente périodicité, il la redémarrera dès le début.

Dans les parcours d’événements professionnels commençant par un **Lecture de segment** activité : sachant que ce parcours est basé sur la réception d’un événement professionnel, si le profil est qualifié dans le segment attendu, il saisira le parcours de chaque événement commercial reçu, ce qui signifie que ce profil peut être plusieurs fois dans le même parcours, en même temps, mais dans le contexte de différents événements professionnels.
