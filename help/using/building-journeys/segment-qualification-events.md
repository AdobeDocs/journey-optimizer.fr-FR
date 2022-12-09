---
solution: Journey Optimizer
product: journey optimizer
title: Événements de qualification de segment
description: En savoir plus sur les événements de qualification de segment
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 7e70b8a9-7fac-4450-ad9c-597fe0496df9
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 0%

---

# Événements de qualification de segment {#segment-qualification}

## À propos des événements de qualification de segment{#about-segment-qualification}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_segment_qualification"
>title="Événements de qualification de segment"
>abstract="Cette activité permet à votre parcours d’écouter les entrées et les sorties des profils dans les segments Adobe Experience Platform afin de faire entrer ou avancer les individus dans un parcours."

Cette activité permet à votre parcours d’écouter les entrées et les sorties des profils dans les segments Adobe Experience Platform afin de faire entrer ou avancer les individus dans un parcours. Pour plus d’informations sur la création de segments, reportez-vous à cette section [section](../segment/about-segments.md).

Supposons que vous ayez un segment &quot;client Silver&quot;. Avec cette activité, vous pouvez faire entrer tous les nouveaux clients Silver dans un parcours et leur envoyer une série de messages personnalisés.

Ce type d’événement peut être positionné comme première étape ou plus tard dans le parcours.

>[!IMPORTANT]
>
>Gardez à l’esprit que les segments Adobe Experience Platform sont calculés une fois par jour (**batch** segments) ou en temps réel (**en flux continu** segments, à l’aide de l’option Audiences haute fréquence d’Adobe Experience Platform).
>
>Si le segment sélectionné est en flux continu, les individus appartenant à ce segment peuvent éventuellement rejoindre le parcours en temps réel. Si le segment est par lot, les personnes nouvellement qualifiées pour ce segment peuvent éventuellement rejoindre le parcours lorsque le calcul du segment est exécuté sur Adobe Experience Platform.
>
>Les groupes de champs d’événement d’expérience ne peuvent pas être utilisés dans les parcours commençant par un segment de lecture, une qualification de segment ou une activité d’événement commercial.


1. Développez l’objet **[!UICONTROL Events]** catégorie et déposer une **[!UICONTROL Segment Qualification]** dans votre zone de travail.

   ![](assets/segment5.png)

1. Ajouter un **[!UICONTROL Label]** à l’activité. Cette étape est facultative.

1. Cliquez sur dans le **[!UICONTROL Segment]** et sélectionnez les segments à exploiter.

   >[!NOTE]
   >
   >Notez que vous pouvez personnaliser les colonnes affichées dans la liste et les trier.

   ![](assets/segment6.png)

   Une fois le segment ajouté, la variable **[!UICONTROL Copy]** permet de copier son nom et son identifiant :

   `{"name":"Loyalty membership“,”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/segment-copy.png)

1. Dans le **[!UICONTROL Behaviour]** , choisissez si vous souhaitez écouter les entrées de segments, les sorties ou les deux.

   >[!NOTE]
   >
   >Notez que **[!UICONTROL Enter]** et **[!UICONTROL Exit]** correspondent au **Réalisé** et **Sortie** états de participation aux segments d’Adobe Experience Platform. Pour plus d’informations sur l’évaluation d’un segment, reportez-vous à la section [Documentation de Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target=&quot;_blank&quot;}.

1. Sélectionnez un espace de noms. Cela n’est nécessaire que si l’événement est positionné comme première étape du parcours.

   ![](assets/segment7.png)

La payload contient les informations contextuelles suivantes, que vous pouvez utiliser dans des conditions et des actions :

* le comportement (entrée, sortie) ;
* l’horodatage de la qualification
* l’identifiant du segment

Lors de l’utilisation de l’éditeur d’expression dans une condition ou une action qui suit un **[!UICONTROL Segment Qualification]** , vous avez accès au **[!UICONTROL SegmentQualification]** noeud . Vous pouvez choisir parmi les **[!UICONTROL Last qualification time]** et le **[!UICONTROL status]** (entrée ou sortie).

Voir [Activité de condition](../building-journeys/condition-activity.md#about_condition).

![](assets/segment8.png)

Un nouveau parcours incluant un événement de qualification de segment est opérationnel dix minutes après sa publication. Cet intervalle de temps correspond à l’intervalle d’actualisation du cache du service dédié. Par conséquent, vous devez attendre dix minutes avant d’utiliser ce parcours.

## Bonnes pratiques {#best-practices-segments}

Le **[!UICONTROL Segment Qualification]** activité permet une entrée immédiate dans les parcours des individus qualifiés ou disqualifiés d’un segment Adobe Experience Platform.

La vitesse de réception de ces informations est élevée. Les mesures effectuées montrent une vitesse de 10 000 événements reçus par seconde. Par conséquent, vous devez vous assurer de comprendre comment les pics d’entrée peuvent se produire, comment les éviter et comment préparer votre parcours pour eux.

### Segments par lot{#batch-speed-segment-qualification}

Lors de l’utilisation de la qualification du segment pour un segment par lot, notez qu’un pic d’entrée se produit au moment du calcul quotidien. La taille du pic dépend du nombre d’individus qui entrent (ou sortent) dans le segment quotidiennement.

De plus, si le segment par lot est créé et utilisé immédiatement dans un parcours, le premier lot de calculs peut faire qu’un très grand nombre d’individus rejoignent le parcours.

### Segments en flux continu{#streamed-speed-segment-qualification}

Lors de l’utilisation de la qualification du segment pour les segments en flux continu, le risque d’obtenir de grands pics d’entrées/de sorties est moindre en raison de l’évaluation continue du segment. Néanmoins, si la définition de segment conduit à qualifier un grand volume de clients en même temps, il peut y avoir un pic également.

Pour plus d’informations sur la segmentation par flux, reportez-vous à la section [Documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/api/streaming-segmentation.html#api)

### Comment éviter les surcharges{#overloads-speed-segment-qualification}

Voici quelques bonnes pratiques qui permettront d’éviter la surcharge des systèmes utilisés dans les parcours (sources de données, actions personnalisées, activités d’action de canal).

N’utilisez pas dans une **[!UICONTROL Segment Qualification]** activité : segment par lot immédiatement après sa création. Il évitera le premier pic de calcul. Notez qu’un avertissement jaune s’affichera dans la zone de travail du parcours si vous êtes sur le point d’utiliser un segment qui n’a jamais été calculé.

![](assets/segment-error.png)

Mettez en place une règle de limitation pour les sources de données et les actions utilisées dans les parcours pour éviter de les surcharger. En savoir plus dans [Documentation de Journey Orchestration](https://experienceleague.adobe.com/docs/journeys/using/working-with-apis/capping.html){target=&quot;_blank&quot;}. Notez que la règle de limitation ne fait l’objet d’aucune nouvelle tentative. Si vous devez effectuer une nouvelle tentative, vous devez utiliser un autre chemin dans le parcours en cochant la case **[!UICONTROL Add an alternative path in case of a timeout or an error]** dans des conditions ou des actions.

Avant d’utiliser le segment dans un parcours en production, évaluez toujours d’abord le volume d’individus qualifiés pour ce segment tous les jours. Pour ce faire, vous pouvez vérifier la variable **[!UICONTROL Segments]** , ouvrez le segment, puis examinez le **[!UICONTROL Profiles over time]** graphique.

![](assets/segment-overload.png)
