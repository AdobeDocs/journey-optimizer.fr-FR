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
source-wordcount: '349'
ht-degree: 0%

---

# Gestion des entrées de profil {#entry-management}

Par défaut, les nouveaux parcours permettent une rentrée. Vous pouvez décocher l’option correspondant aux parcours &quot;ponctuels&quot;, par exemple si vous souhaitez offrir un cadeau ponctuel lorsqu’une personne entre dans une boutique. Dans ce cas, vous ne souhaitez pas que le client puisse revenir dans le parcours et recevoir à nouveau l’offre.

![](assets/journey-re-entrance.png)

Lorsqu’un parcours prend fin, son état est **[!UICONTROL Closed]**. TNew ne peut plus participer au parcours. Les personnes déjà engagées dans le parcours terminent normalement le parcours.

Après le délai d’expiration global par défaut de 30 jours, le parcours passe à la variable **Terminé** statut.  [En savoir plus](journey-gs.md#global_timeout).


## Parcours unitaires{#entry-unitary}

Les parcours unitaires (commençant par un événement ou une qualification de segment) incluent une barrière de sécurité qui empêche les parcours d’être déclenchés par erreur plusieurs fois pour le même événement. La rentrée du profil est temporairement bloquée par défaut pendant 5 minutes. Par exemple, si un événement déclenche un parcours à 12h01 pour un profil spécifique et qu’un autre arrive à 12h03 (s’il s’agit du même événement ou d’un autre déclenchant le même parcours), ce parcours ne redémarre pas pour ce profil.

En outre :

* Si la rentrée est activée, un profil peut entrer dans un parcours plusieurs fois, mais ne peut pas le faire tant qu’il n’a pas complètement quitté cette instance précédente du parcours.

* Si la rentrée est désactivée, un profil ne peut pas entrer plusieurs fois le même parcours

## Lire les parcours de segmentation{#entry-read-segment}

Dans un parcours de segment lu :

* Pour les parcours non récurrents : le profil entre une fois et une seule fois.

* Pour les parcours récurrents : le profil entre dans le parcours à chaque périodicité, s’il est dans l’état segment/attendu. S’il était toujours dans le parcours à partir d’une répétition précédente, il la redémarrera dès le début.

Dans les parcours d’événements professionnels commençant par un **Lecture de segment** activité : sachant que ce parcours est basé sur la réception d’un événement commercial, si le profil est qualifié dans le segment attendu, il entrera dans le parcours de chaque événement commercial reçu, ce qui signifie que ce profil peut être plusieurs fois dans le même parcours, en même temps, mais dans le contexte d’événements commerciaux différents.
