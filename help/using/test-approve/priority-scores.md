---
title: Attribuer des scores de priorité aux parcours et aux campagnes
description: Découvrez comment attribuer des scores de priorité aux parcours et aux campagnes.
role: User
level: Beginner
badge: label="Disponibilité limitée"
hide: true
hidefromtoc: true
source-git-commit: 0eedadee1e8c1d4642d8602d48bcc9a49a0a2e53
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 85%

---


# Attribuer des scores de priorité aux parcours et aux campagnes {#priority}

>[!BEGINSHADEBOX]

Ce guide couvre les sujets suivants :

* [Prise en main de la gestion des conflits et de la hiérarchisation](gs-conflict-prioritization.md)
* [Détecter les conflits potentiels dans les parcours et campagnes](conflicts.md)
* **[Attribuer des scores de priorité aux parcours et campagnes](priority-scores.md)**
* [Limitation et arbitrage des parcours](journey-capping.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Les outils de gestion des conflits et de hiérarchisation des conflits sont actuellement disponibles en tant que disponibilité limitée pour certains utilisateurs uniquement.

Journey Optimizer vous permet d’attribuer un score de priorité à un parcours ou à une campagne. La priorité est essentielle pour donner la priorité à un parcours, à une campagne ou à une action lorsqu’une contrainte est imposée (par exemple, une limitation de la fréquence). Dans les cas où une personne est admissible pour plusieurs parcours, campagnes ou communications et que vous souhaitez choisir ceux qu’elle doit rejoindre et recevoir, vous devez utiliser ce champ.

>[!NOTE]
>
>Le score de priorité est disponible pour les canaux entrants : web, in-app et basé sur du code. Dans le parcours, le score de priorité est disponible uniquement pour les canaux **in-app** et **basés sur du code**.

➡️ [Découvrir cette fonctionnalité en vidéo](#video)

L’attribution d’un score de priorité est essentielle pour la communication entrante, par exemple web, mobile et in-app. Si plusieurs campagnes utilisent la même configuration des canaux (une bannière dans la partie supérieure de votre page web, par exemple), cela peut s’avérer problématique, car seul le contenu d’une campagne peut être affiché. Le score de priorité est l’emplacement où vous insérerez vos préférences pour la campagne qui doit s’afficher lorsque les destinataires peuvent être admissibles pour plusieurs campagnes.

Pour attribuer un score de priorité à un parcours ou à une campagne, saisissez une valeur numérique (de 0 à 100) dans le champ **[!UICONTROL Score de priorité]** situé dans les propriétés du parcours ou de la campagne. Notez que plus le nombre est élevé, plus la priorité est élevée. Si vous créez cette campagne et souhaitez vous assurer que le contenu de cette campagne s’affiche, donnez-lui un score de 100.

![](assets/priority-score.png)

Dans les cas où deux campagnes ont le même score de priorité, la campagne qui a été activée en premier s’affiche.

## Vidéo pratique {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3435529?quality=12)
