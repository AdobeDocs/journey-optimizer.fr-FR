---
title: Attribuer des scores de priorité aux parcours et aux campagnes
description: Découvrez comment attribuer des scores de priorité aux parcours et aux campagnes.
role: User
level: Beginner
badge: label="Disponibilité limitée"
source-git-commit: 4ab4b48ba87c73552a15c9815877517934029d57
workflow-type: tm+mt
source-wordcount: '448'
ht-degree: 76%

---


# Attribuer des scores de priorité aux parcours et aux campagnes {#priority}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_priority"
>title="Priorité"
>abstract="Attribuez un score de priorité à la campagne. La priorité est essentielle pour prioriser une campagne en cas de contrainte imposée, telle qu’une limite de fréquence. Saisissez une valeur numérique (de 0 à 100). Notez que plus le nombre est élevé, plus la priorité est élevée. Dans les cas où deux campagnes ont le même score de priorité, la campagne qui a été activée en premier s’affiche."

>[!CONTEXTUALHELP]
>id="ajo_journey_priority"
>title="Priorité"
>abstract="Attribuez un score de priorité au parcours. La priorité est essentielle pour donner la priorité à un parcours lorsqu’il existe une contrainte imposée telle qu’un plafond de fréquence. Entrez une valeur numérique (de 0 à 100). Notez que plus le nombre est élevé, plus la priorité est élevée. Dans les cas où deux parcours ont le même score de priorité, le parcours qui a été activé en premier s’affiche."

>[!AVAILABILITY]
>
>Les fonctionnalités de conflit et de hiérarchisation sont actuellement disponibles dans Disponibilité limitée pour un groupe sélectionné de clients. Notez que ces fonctionnalités seront progressivement déployées vers d’autres utilisateurs et utilisatrices à l’avenir. Contactez votre équipe de compte si vous souhaitez qu’elle vous ajoute à la liste d’attente pour ces fonctionnalités.

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
