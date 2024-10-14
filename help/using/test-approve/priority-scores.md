---
title: Attribuer des scores de priorité aux parcours et aux campagnes
description: Découvrez comment attribuer des scores de priorité aux parcours et aux campagnes.
role: User
level: Beginner
badge: label="Disponibilité limitée"
hide: true
hidefromtoc: true
source-git-commit: e1121d998711ea4751da5293efdd7c1578ee44a2
workflow-type: tm+mt
source-wordcount: '313'
ht-degree: 6%

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

Journey Optimizer vous permet d’attribuer un score de priorité à un parcours ou à une campagne. La priorité est essentielle pour donner la priorité à un parcours, à une campagne ou à une action lorsqu’une contrainte est imposée (par exemple, une limite de fréquence). Dans les cas où un client est admissible pour de nombreux parcours, campagnes ou communications et où vous souhaitez être sélectif quant aux adresses auxquelles il doit entrer et recevoir, vous devez utiliser ce champ.

>[!NOTE]
>
>Le score de priorité est disponible pour les canaux entrants : web, in-app et code-based. En parcours, le score de priorité est disponible uniquement pour les canaux **in-app** et **basés sur du code**.

L’attribution d’un score de priorité est essentielle pour la communication entrante, par exemple web, mobile et in-app. Si plusieurs campagnes utilisent la même configuration de canal (une bannière dans la partie supérieure de votre page web, par exemple), cela peut s’avérer problématique, car seul le contenu d’une campagne peut être affiché. Le score de priorité est l&#39;emplacement où vous insérerez vos préférences pour la campagne qui doit s&#39;afficher lorsque le destinataire peut être admissible pour plusieurs campagnes.

Pour attribuer un score de priorité à un parcours ou à une campagne, saisissez une valeur numérique (de 0 à 100) dans le champ **[!UICONTROL Priority score]** situé dans les propriétés du parcours ou de la campagne. Veuillez noter que plus le nombre est élevé, plus la priorité est élevée. Si vous créez cette campagne et souhaitez vous assurer que le contenu de cette campagne s’affiche, vous lui donnez un score de 100.

![](assets/priority-score.png)

Dans les cas où deux campagnes ont le même score de priorité, la campagne qui a été activée en premier s’affiche.
