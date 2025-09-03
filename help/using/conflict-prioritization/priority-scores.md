---
title: Attribuer des scores de priorité aux parcours et aux campagnes
description: Découvrez comment attribuer des scores de priorité aux parcours et aux campagnes.
role: User
level: Beginner
exl-id: f33ca0a8-ed33-4964-a85c-8705a4ff728e
source-git-commit: e8f7f5862e3816481680fa999657ae90334ff888
workflow-type: tm+mt
source-wordcount: '608'
ht-degree: 46%

---

# Attribuer des scores de priorité {#priority}

Journey Optimizer permet d&#39;attribuer un score de priorité à un parcours, une campagne ou à une action de canal entrant dans le parcours **[!UICONTROL Action]** de l&#39;activité.

La priorité est essentielle pour donner la priorité à un parcours, une campagne ou une action en cas de contrainte imposée (telle qu’une limitation de fréquence).

Dans les cas où une personne est admissible pour plusieurs parcours, campagnes ou communications et que vous souhaitez choisir ceux qu’elle doit rejoindre et recevoir, vous devez utiliser ce champ.

## Attribuer des scores de priorité aux parcours et aux campagnes {#priority-journey-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_priority"
>title="Priorité"
>abstract="Attribuez un score de priorité à la campagne. La priorité est essentielle pour donner la priorité à une campagne en cas de contrainte imposée telle qu’une limitation de fréquence.</br>Entrez une valeur numérique (comprise entre 0 et 100). Notez que plus le nombre est élevé, plus la priorité l’est aussi. Si deux campagnes ont le même score de priorité, la campagne qui a été activée en premier s’affiche."

>[!CONTEXTUALHELP]
>id="ajo_journey_priority"
>title="Priorité"
>abstract="Attribuez un score de priorité au parcours. La priorité est essentielle pour donner la priorité à un parcours en cas de contrainte imposée telle qu’une limitation de fréquence.</br>Entrez une valeur numérique (comprise entre 0 et 100). Notez que plus le nombre est élevé, plus la priorité l’est aussi. Dans les cas où deux parcours ont le même score de priorité, le parcours qui a été activé en premier s’affiche."

➡️ [Découvrez cette fonctionnalité en vidéo.](#video)

L’attribution d’un score de priorité est essentielle pour la communication entrante, par exemple web, mobile et in-app. Si plusieurs campagnes utilisent la même configuration de canal (par exemple, une bannière en haut de votre page web), cela peut s’avérer problématique, car il n’est possible d’afficher que le contenu d’une seule campagne. Le score de priorité est l’emplacement où vous insérerez vos préférences pour la campagne qui doit s’afficher lorsque les destinataires peuvent être admissibles pour plusieurs campagnes.

>[!NOTE]
>
>Dans les campagnes, le score de priorité est disponible uniquement pour les canaux entrants web, in-app et basés sur du code.

Pour attribuer un score de priorité à un parcours ou à une campagne, saisissez une valeur numérique (de 0 à 100) dans le champ **[!UICONTROL Score de priorité]** situé dans les propriétés du parcours ou de la campagne. Plus le nombre est élevé, plus la priorité est élevée.

Si vous créez cette campagne et souhaitez vous assurer que le contenu de cette campagne s’affiche, donnez-lui un score de 100.

![](assets/priority-score.png)

>[!IMPORTANT]
>
>Si deux parcours ou campagnes ont le même score de priorité, le système ne dispose pas d’un mécanisme de rupture d’égalité. Assurez-vous que les scores de priorité sont uniques pour éviter les conflits.

## Attribuer des scores de priorité aux actions de canal entrant {#priority-action}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_priority"
>title="Priorité"
>abstract="Attribuez un score de priorité à l’action de parcours. La priorité est essentielle pour donner la priorité à une action entrante lorsqu’il existe plusieurs actions ou campagnes de parcours utilisant la même configuration de canal.</br>Entrez une valeur numérique (comprise entre 0 et 100). Notez que plus le nombre est élevé, plus la priorité l’est aussi. Par défaut, le score de priorité de l’action est hérité du score de priorité global du parcours."

Journey Optimizer vous permet également d’attribuer un score de priorité aux actions de canal entrant dans l’activité **[!UICONTROL Action]**.

Vous pouvez ainsi donner la priorité à une action entrante lorsqu’il existe plusieurs actions ou campagnes de parcours utilisant la même configuration de canal.

>[!NOTE]
>
>Dans l’activité **[!UICONTROL Action]**, le score de priorité est disponible uniquement pour les canaux entrants web, in-app et basés sur du code.

Dans la section **[!UICONTROL Gestion des conflits]** , l’option **[!UICONTROL Utiliser la priorité du parcours]** est sélectionnée par défaut, ce qui signifie que le score de priorité de l’action est hérité du score de priorité global du parcours.

Pour attribuer un score de priorité aux actions entrantes définies dans l&#39;activité **[!UICONTROL Action]**, désélectionnez l&#39;option **[!UICONTROL Utiliser la priorité du parcours]** et saisissez une valeur numérique (comprise entre 0 et 100) dans le champ **[!UICONTROL Priorité]**. Plus le nombre est élevé, plus la priorité est élevée.

![](assets/action-journey-priority-score.png){width=70%}

## Vidéo pratique {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3435529?quality=12)
