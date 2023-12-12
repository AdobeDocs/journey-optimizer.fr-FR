---
solution: Journey Optimizer
product: journey optimizer
title: Gestion des entrées de profil
description: Découvrez comment gérer l’entrée de profil.
feature: Journeys, Profiles
role: User
level: Intermediate
keywords: reprise, parcours, profil, récurrent
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: a6b2c1585867719a48f9abc4bf0eb81558855d85
workflow-type: tm+mt
source-wordcount: '604'
ht-degree: 97%

---


# Gestion des entrées de profil {#entry-management}

Il existe deux principaux types de parcours :

* Parcours basés sur un événement : à partir d’un événement, ces parcours sont unitaires et sont associés à un seul individu. Lorsque l’événement est reçu, l’individu rejoint le parcours. [En savoir plus](#entry-unitary).
* Parcours de lecture d’audience : à partir d’une lecture d’audience, il s’agit de parcours par lots. Les personnes appartenant à l’audience rejoignent toutes le même parcours. Ces parcours peuvent être récurrents ou ponctuels. [En savoir plus](#entry-read-segment)

Dans les deux types de parcours, un profil ne peut pas être présent plusieurs fois dans le même parcours, en même temps.

## Parcours unitaires{#entry-unitary}

Dans les parcours unitaires, vous pouvez activer ou désactiver la reprise :

* Si la reprise est activée, un profil peut rejoindre à nouveau plusieurs fois un parcours, mais ne peut pas le faire tant qu’il n’a pas complètement quitté cette instance précédente du parcours.

* Si la rentrée est désactivée, un profil ne peut pas entrer plusieurs fois le même parcours.

Par défaut, les nouveaux parcours autorisent une reprise. Vous pouvez désélectionner cette option pour les parcours « uniques ». C’est le cas, par exemple, si vous souhaitez offrir un cadeau ponctuel à un utilisateur ou à une utilisatrice qui effectue sa première visite dans la boutique. Dans ce cas, le client ou la cliente ne doit pas pouvoir recommencer le parcours et bénéficier une nouvelle fois de l’offre. Lorsqu’un parcours se termine, son statut passe en mode **[!UICONTROL Fermé]**. Aucune nouvelle personne ne peut rejoindre le parcours. En revanche, les personnes qui ont déjà intégré le parcours le terminent normalement. [En savoir plus](journey-gs.md#entrance)

Lorsque l’option **Autoriser une reprise** est activée, le champ **Période d’attente de reprise** vous permet de définir le temps d’attente avant d’autoriser un profil à entrer à nouveau dans le parcours. Cela empêche les parcours d’être déclenchés plusieurs fois par erreur pour le même événement. Par défaut, le champ est défini sur 5 minutes. La durée maximale est de 29 jours.

![](assets/journey-re-entrance.png)

Après le [délai d’expiration global](journey-gs.md#global_timeout) par défaut de 30 jours, le statut du parcours passe à **Terminé**. Les profils de clientes et clients qui ont déjà intégré le parcours le terminent normalement. Les nouveaux profils de cleintes et clients ne peuvent plus rejoindre le parcours. Ce comportement est défini uniquement sur 30 jours (c’est-à-dire sur la valeur par défaut du délai d’expiration du parcours), car toutes les informations relatives aux profils déjà entrés dans le parcours sont supprimées 30 jours après leur entrée. Après cette période, les profils de clientes et clients peuvent entrer à nouveau dans le parcours. Pour éviter cela et désactiver complètement la possibilité de reprise pour ces profils, vous pouvez ajouter une condition de test pour savoir si le profil est déjà entré ou non, à l’aide des données de profil ou d’audience.

<!--
Due to the 30-day journey timeout, when journey re-entrance is not allowed, we cannot make sure the re-entrance blocking will work more than 30 days. Indeed, as we remove all information about persons who entered the journey 30 days after they enter, we cannot know the person entered previously, more than 30 days ago. -->

La clé sert à vérifier qu’une personne se trouve dans un parcours. En effet, une personne ne peut pas se trouver à deux endroits différents dans le même parcours. Par conséquent, le système n&#39;autorise pas qu&#39;une même clé (CRMID=3224, par exemple) se trouve à des endroits différents dans un même parcours.

## Parcours de lecture d’audience{#entry-read-segment}

Dans un parcours de lecture d’audience :

* Pour les parcours non récurrents : le profil rejoint une seule fois le parcours.

* Pour les parcours récurrents : par défaut, tous les profils appartenant à l’audience rejoignent le parcours à chaque périodicité. Elles doivent terminer le parcours avant de pouvoir rejoindre à nouveau une autre occurrence.

>[!NOTE]
>
>Deux options sont disponibles pour les parcours de lecture d’audience récurrents. L’option **Forcer une reprise sur une périodicité** permet de faire en sorte que tous les profils toujours présents dans le parcours le quittent automatiquement lors de la prochaine exécution. Lʼoption **Lecture incrémentielle** cible uniquement les personnes qui sont entrées dans l’audience depuis la dernière exécution du parcours. Reportez-vous à cette [section](../building-journeys/read-audience.md#configuring-segment-trigger-activity)

Dans les parcours d’événement métier commençant par une activité **Lecture d’audience** : sachant que ce parcours est basé sur la réception d’un événement métier, si le profil est qualifié dans l’audience prévue, il rejoint le parcours de chaque événement métier reçu. Cela signifie que ce profil peut rejoindre le même parcours plusieurs fois, au même moment, mais dans le contexte de divers événements métier.