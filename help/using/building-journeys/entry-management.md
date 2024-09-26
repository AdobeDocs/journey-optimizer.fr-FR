---
solution: Journey Optimizer
product: journey optimizer
title: Gestion des entrées de profil
description: Découvrez comment gérer l’entrée de profil.
feature: Journeys, Profiles
role: User
level: Intermediate
keywords: réentrée, parcours, profil, récurrent
exl-id: 8874377c-6594-4a5a-9197-ba5b28258c02
source-git-commit: 7f21098d5ae157f1c0d3de3aa584564c6f73310a
workflow-type: tm+mt
source-wordcount: '701'
ht-degree: 83%

---


# Gestion des entrées de profil {#entry-management}

La gestion des entrées de profil dépend du type de parcours. Dans Adobe Journey Optimizer, les types de parcours suivants sont disponibles :

* Parcours **Événement unitaire** : ces parcours commencent par un événement unitaire. Lorsque l’événement est reçu, le profil associé rejoint le parcours. [En savoir plus](#entry-unitary)

* Parcours **Événement métier** : ces parcours commencent par un événement métier suivi immédiatement d’une activité **Lecture d’audience**. Lorsque l’événement est reçu, les profils appartenant à l’audience ciblée rejoignent le parcours. Une instance de ce parcours est créée pour chaque profil. [En savoir plus](#entry-business)

* Parcours **Lecture d’audience** : ces parcours commencent par une activité **Lecture d’audience**. Lorsque le parcours est exécuté, les profils appartenant à l’audience ciblée rejoignent le parcours. Une instance de ce parcours est créée pour chaque profil. Ces parcours peuvent être récurrents ou ponctuels. [En savoir plus](#entry-read-audience)

* Parcours **Qualification de l’audience** : ces parcours commencent par un événement Qualification de l’audience. Ces parcours écoutent les entrées et les sorties des profils dans les audiences. Lorsque cela se produit, le profil associé rejoint le parcours. [En savoir plus](#entry-unitary)

Dans tous les types de parcours, un profil ne peut pas être présent plusieurs fois dans le même parcours, en même temps. Pour vérifier qu’une personne se trouve dans un parcours, l’identité du profil est utilisée comme clé. Le système n’autorise pas qu’une même clé (CRMID=3224, par exemple) se trouve à des endroits différents dans un même parcours.

## Parcours Événement unitaire et Qualification de l’audience{#entry-unitary}

Dans les parcours **Événement unitaire** et **Qualification de l’audience**, vous pouvez activer ou désactiver la réentrée :

* Si la rentrée est activée, un profil peut entrer un parcours plusieurs fois, mais il ne peut pas le faire tant qu’il n’a pas complètement quitté l’instance précédente du parcours.

* Si la réentrée est désactivée, un profil ne peut pas entrer plusieurs fois le même parcours, dans le délai d’expiration du parcours global. Consultez cette [section](../building-journeys/journey-properties.md#global_timeout).

Par défaut, les parcours autorisent la réentrée. Lorsque l’option **Autoriser la rentrée** est activée, le champ **Période d’attente de rentrée** s’affiche. Il vous permet de définir le temps d’attente avant qu’un profil puisse rejoindre à nouveau le parcours. Cela empêche les parcours d’être déclenchés plusieurs fois par erreur pour le même événement. Par défaut, le champ est défini sur 5 minutes. La durée maximale est de 91 jours ([temporisation globale](journey-properties.md#global_timeout)).

<!--
When a journey ends, its status is **[!UICONTROL Closed]**. New individuals can no longer enter the journey. Persons already in the journey automatically exit the journey. 
-->

![](assets/journey-re-entrance.png)

Après la période de rentrée, les profils peuvent revenir au parcours. Pour éviter cela et désactiver complètement la réentrée pour ces profils, vous pouvez ajouter une condition afin de tester si le profil a déjà été renseigné ou non, à l&#39;aide des données de profil ou d&#39;audience.

<!--
Due to the 30-day journey timeout, when journey reentrance is not allowed, we cannot make sure the reentrance blocking will work more than 91 days. Indeed, as we remove all information about persons who entered the journey 91 days after they enter, we cannot know the person entered previously, more than 91 days ago. -->

## Parcours métier {#entry-business}

<!--
Business events follow reentrance rules in the same way as for unitary events. If a journey allows reentrance, the next business event will be processed.
-->

Dans les **parcours métier**, pour autoriser plusieurs exécutions d’événements métier, activez l’option correspondante dans la section **[!UICONTROL Exécution]** des propriétés du parcours.

![](assets/business-entry.png)

Dans le cas d’événements métier, pour un parcours donné, les données d’audience récupérées lors de la première exécution sont réutilisées pendant une période d’une heure.

Un profil peut être présent plusieurs fois dans le même parcours, en même temps, mais dans le contexte d’événements métier différents.

Pour plus d’informations, consultez cette [section](../event/about-creating-business.md).

## Parcours de lecture d’audience {#entry-read-audience}

Les parcours **Lecture d’audience** peuvent être récurrents ou ponctuels :

* Pour les parcours non récurrents/ponctuels : le profil rejoint une seule fois le parcours.

* Pour les parcours récurrents : par défaut, tous les profils appartenant à l’audience rejoignent le parcours à chaque périodicité. Elles doivent terminer le parcours avant de pouvoir rejoindre à nouveau une autre occurrence.

Deux options sont disponibles pour les parcours Lecture d’audience récurrents :

* Option **Lecture incrémentielle** : lorsqu’un parcours avec un événement récurrent **Lecture d’audience** s’exécute pour la première fois, tous les profils de l’audience rejoignent le parcours. Cette option vous permet de cibler, après la première occurrence, seulement les personnes qui sont entrées dans l’audience depuis la dernière exécution du parcours.

  >[!NOTE]
  >
  >Si vous ciblez une [audience de chargement personnalisé](../audience/about-audiences.md#segments-in-journey-optimizer) dans votre parcours, les profils ne sont récupérés que lors de la première périodicité si cette option est activée dans un parcours récurrent, car ces audiences sont fixes.

* **Forcer une reprise sur une périodicité** : cette option vous permet de faire en sorte que tous les profils toujours présents dans le parcours le quittent automatiquement lors de l’exécution suivante. Si la durée de vie de vos profils dans ce parcours peut être supérieure à la fréquence de périodicité (par exemple, si vous utilisez des activités d’attente), n’activez pas cette option pour vous assurer que les profils puissent terminer leur parcours.

![](assets/read-audience-options.png)

Pour plus d’informations, consultez cette [section](../building-journeys/read-audience.md#configuring-segment-trigger-activity).

<!--
After 91 days, a Read audience journey switches to the **Finished** status. This behavior is set for 91 days only (i.e. journey timeout default value) as all information about profiles who entered the journey is removed 91 days after they entered. Persons still in the journey automatically are impacted. They exit the journey after the 30 day timeout. 
-->
