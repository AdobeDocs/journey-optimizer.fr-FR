---
title: Attribuer des scores de priorité aux parcours et aux campagnes
description: Découvrez comment attribuer des scores de priorité aux parcours et aux campagnes.
role: User
level: Beginner
exl-id: f33ca0a8-ed33-4964-a85c-8705a4ff728e
source-git-commit: 528e1a54dd64503e5de716e63013c4fc41fd98db
workflow-type: tm+mt
source-wordcount: '375'
ht-degree: 86%

---

# Attribuer des scores de priorité aux parcours et aux campagnes {#priority}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_priority"
>title="Priorité"
>abstract="Attribuez un score de priorité à la campagne. La priorité est essentielle pour donner la priorité à une campagne en cas de contrainte imposée, comme un capping de la fréquence. Saisissez une valeur numérique (de 0 à 100). Notez que plus le nombre est élevé, plus la priorité est élevée. Dans les cas où deux campagnes ont le même score de priorité, la campagne qui a été activée en premier s’affiche."

>[!CONTEXTUALHELP]
>id="ajo_journey_priority"
>title="Priorité"
>abstract="Attribuez un score de priorité au parcours. La priorité est essentielle pour donner la priorité à un parcours en cas de contrainte imposée, telle qu’une limite de fréquence. Saisissez une valeur numérique (de 0 à 100). Veuillez noter que plus le nombre est élevé, plus la priorité est élevée."

Journey Optimizer vous permet d’attribuer un score de priorité à un parcours ou à une campagne. La priorité est essentielle pour donner la priorité à un parcours, à une campagne ou à une action lorsqu’une contrainte est imposée (par exemple, une limitation de la fréquence). Dans les cas où une personne est admissible pour plusieurs parcours, campagnes ou communications et que vous souhaitez choisir ceux qu’elle doit rejoindre et recevoir, vous devez utiliser ce champ.

>[!NOTE]
>
>Dans les campagnes, le score de priorité est disponible uniquement pour les canaux entrants web, in-app et basés sur du code.

➡️ [Découvrez cette fonctionnalité en vidéo](#video)

L’attribution d’un score de priorité est essentielle pour la communication entrante, par exemple web, mobile et in-app. Si plusieurs campagnes utilisent la même configuration des canaux (une bannière dans la partie supérieure de votre page web, par exemple), cela peut s’avérer problématique, car seul le contenu d’une campagne peut être affiché. Le score de priorité est l’emplacement où vous insérerez vos préférences pour la campagne qui doit s’afficher lorsque les destinataires peuvent être admissibles pour plusieurs campagnes.

Pour attribuer un score de priorité à un parcours ou à une campagne, saisissez une valeur numérique (de 0 à 100) dans le champ **[!UICONTROL Score de priorité]** situé dans les propriétés du parcours ou de la campagne. Notez que plus le nombre est élevé, plus la priorité est élevée. Si vous créez cette campagne et souhaitez vous assurer que le contenu de cette campagne s’affiche, donnez-lui un score de 100.

![](assets/priority-score.png)

>[!IMPORTANT]
>
>Si deux parcours ou campagnes ont le même score de priorité, le système ne dispose pas d’un mécanisme de rupture d’égalité. Assurez-vous que les scores de priorité sont uniques pour éviter les conflits.

## Vidéo pratique {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3445003?quality=12&captions=fre_fr)
