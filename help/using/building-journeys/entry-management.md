---
solution: Journey Optimizer
product: journey optimizer
title: Gestion des entrées de profil
description: Découvrez comment gérer l’entrée de profil
feature: Journeys
role: User
level: Intermediate
source-git-commit: f04454860ebe597d3306e62b58de5f32e08342ee
workflow-type: tm+mt
source-wordcount: '260'
ht-degree: 95%

---

# Gestion des entrées de profil {#entry-management}

Dans un parcours unitaire :

* Si la reprise est activée, un profil peut rejoindre à nouveau plusieurs fois un parcours, mais ne peut pas le faire tant qu’il n’a pas complètement quitté cette instance précédente du parcours.

* Si la reprise est désactivée, un profil ne peut pas rejoindre plusieurs fois le même parcours

Pour plus d&#39;informations à ce sujet, consulter cette [section](../building-journeys/journey-gs.md#change-properties).

Dans un parcours de segment lu :

* Pour les parcours non récurrents : le profil rejoint une seule fois le parcours.
* Pour les parcours récurrents : le profil rejoint le parcours à chaque périodicité, s’il est dans le segment / le statut attendu. S’il était toujours dans le parcours d&#39;une précédente périodicité, il la redémarrera dès le début.

Dans les parcours d’événement métier commençant par une lecture de segment :

Sachant que ce parcours est basé sur la réception d’un événement métier, si le profil est qualifié dans le segment attendu, il rejoindra le parcours de chaque événement métier reçu, ce qui signifie que ce profil pourra être plusieurs fois dans le même parcours, au même moment, mais dans le contexte de différents événements métier.

Les parcours unitaires (commençant par un événement ou une qualification de segment) incluent une barrière de sécurité qui empêche les parcours d’être déclenchés par erreur plusieurs fois pour le même événement. La reprise du profil est temporairement bloquée par défaut pendant 5 minutes. Par exemple, si un événement déclenche un parcours à 12 h 01 pour un profil spécifique et qu’un autre arrive à 12 h 03 (qu’il s’agisse du même événement ou d’un autre déclenchant le même parcours), ce parcours ne reprendra pas pour ce profil.
