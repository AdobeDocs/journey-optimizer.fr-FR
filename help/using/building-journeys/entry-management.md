---
solution: Journey Optimizer
product: journey optimizer
title: Gestion des entrées de profil
description: Découvrez comment gérer l’entrée de profil.
feature: Journeys
role: User
level: Intermediate
keywords: reprise, parcours, profil, récurrent
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: 4112ac79a1f21fb369119ccd801dcbceac3c1e58
workflow-type: ht
source-wordcount: '610'
ht-degree: 100%

---


# Gestion des entrées de profil {#entry-management}

Il existe deux principaux types de parcours :

* Parcours basés sur un événement : à partir d’un événement, ces parcours sont unitaires et sont associés à un seul individu. Lorsque l’événement est reçu, l’individu rejoint le parcours. [En savoir plus](#entry-unitary).
* Parcours de lecture d’audience : à partir d’une lecture d’audience, il s’agit de parcours par lots. Les personnes appartenant à l’audience rejoignent toutes le même parcours. Ces parcours peuvent être récurrents ou ponctuels. [En savoir plus](#entry-read-segment)

Dans les deux types de parcours, un profil ne peut pas être présent plusieurs fois dans le même parcours, en même temps.

## Parcours unitaires{#entry-unitary}

Dans les parcours unitaires, vous pouvez activer ou désactiver la reprise :

* Si la reprise est activée, un profil peut rejoindre à nouveau plusieurs fois un parcours, mais ne peut pas le faire tant qu’il n’a pas complètement quitté cette instance précédente du parcours.

* Si la reprise est désactivée, un profil ne peut pas rejoindre plusieurs fois le même parcours

Par défaut, les nouveaux parcours autorisent une rentrée. Vous pouvez désélectionner cette option pour les parcours « uniques » ; c’est le cas, par exemple, si vous souhaitez offrir un cadeau à un utilisateur ou une utilisatrice qui effectue sa première visite dans la boutique. Dans ce cas, vous ne voulez pas que le client ou la cliente puisse rejoindre de nouveau le parcours et rebénéficier de l&#39;offre. Lorsqu’un parcours se termine, son statut passe en mode **[!UICONTROL Fermé]**. Aucune nouvelle personne ne peut rejoindre le parcours. En revanche, les personnes qui ont déjà intégré le parcours le terminent normalement. [En savoir plus](journey-gs.md#entrance)

![](assets/journey-re-entrance.png)

Au-delà de la temporisation globale par défaut de 30 jours, le statut du parcours passe à **Terminé**. Aucune nouvelle personne ne peut rejoindre le parcours. Les personnes déjà dans le parcours le terminent normalement. En raison de la temporisation de 30 jours du parcours, lorsque la reprise de celui-ci n’est pas autorisée, nous ne pouvons pas nous assurer que le blocage de la reprise fonctionnera plus de 30 jours. En effet, étant donné que nous supprimons toutes les informations sur les personnes qui ont rejoint le parcours 30 jours après leur entrée, rien ne nous permet de savoir qu&#39;une personne l&#39;a déjà rejoint il y a plus de 30 jours. [En savoir plus](journey-gs.md#global_timeout).

Les parcours unitaires (commençant par un événement ou une qualification d’audience) incluent une mécanisme de sécurisation qui empêche les parcours d’être déclenchés par erreur plusieurs fois pour le même événement. La reprise du profil est temporairement bloquée par défaut pendant 5 minutes. Par exemple, si un événement déclenche un parcours à 12 h 01 pour un profil spécifique et qu’un autre arrive à 12 h 03 (qu’il s’agisse du même événement ou d’un autre déclenchant le même parcours), ce parcours ne reprendra pas pour ce profil.

La clé sert également à vérifier qu&#39;une personne se trouve dans un parcours. En effet, une personne ne peut pas se trouver à deux endroits différents dans le même parcours. Par conséquent, le système n&#39;autorise pas qu&#39;une même clé (CRMID=3224, par exemple) se trouve à des endroits différents dans un même parcours.

## Parcours de lecture d’audience{#entry-read-segment}

Dans un parcours de lecture d’audience :

* Pour les parcours non récurrents : le profil rejoint une seule fois le parcours.

* Pour les parcours récurrents : par défaut, tous les profils appartenant à l’audience rejoignent le parcours à chaque périodicité. Elles doivent terminer le parcours avant de pouvoir rejoindre à nouveau une autre occurrence.

>[!NOTE]
>
>Deux options sont disponibles pour les parcours de lecture d’audience récurrents. L’option **Forcer une reprise sur une périodicité** permet de faire en sorte que tous les profils toujours présents dans le parcours le quittent automatiquement lors de la prochaine exécution. Lʼoption **Lecture incrémentielle** cible uniquement les personnes qui sont entrées dans l’audience depuis la dernière exécution du parcours. Reportez-vous à cette [section](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

Dans les parcours d’événement métier commençant par une activité **Lecture d’audience** : sachant que ce parcours est basé sur la réception d’un événement métier, si le profil est qualifié dans l’audience prévue, il rejoint le parcours de chaque événement métier reçu. Cela signifie que ce profil peut rejoindre le même parcours plusieurs fois, au même moment, mais dans le contexte de divers événements métier.