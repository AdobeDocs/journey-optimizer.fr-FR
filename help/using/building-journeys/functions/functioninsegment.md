---
product: journey optimizer
title: inSegment
description: En savoir plus sur la fonction inSegment
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '185'
ht-degree: 0%

---

# inSegment {#inSegment}

Vérifie si un individu appartient à un segment donné.

>[!NOTE]
>
>Vous pouvez récupérer jusqu’à 100 segments.

Le nom du segment doit être une constante sous forme de chaîne. Il ne peut pas s’agir d’une référence de champ ou d’une expression.

Les segments sont définis dans la variable [Adobe Experience Platform](https://platform.adobe.com/segment/overview). L’éditeur d’expression fournit une liste de segments complétée automatiquement.

Les segments peuvent avoir trois états :

* existing : continue d’être dans le segment.
* réalisé : est en train de saisir le segment.
* exited : l’entité quitte le segment.

Seuls les individus dotés de la fonction **Réalisé** et **Existant** les états de participation au segment sont considérés comme des membres du segment. Pour plus d’informations sur l’évaluation d’un segment, reportez-vous à la section [Documentation de Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=en#interpret-segment-results).

`IF inSegment('segmentName') == true` signifie que vous disposez d’un segmentMembership avec le statut renseigné/existant.

`ELSE inSegment('segmentName') == false` signifie que vous disposez d’un segmentMembership avec le statut de sortie.

## Catégorie

Adobe Experience Platform

## Syntaxe de la fonction

`inSegment(<parameter>)`

## Paramètres

| Paramètre | Description | Type |
|--- |--- |--- |
| Segment | Nom du segment | `<string>` |

## Signature et type renvoyé

`inSegment(<string>)`

Renvoie une valeur booléenne.

## Exemple

`inSegment("men over 50")`

Explication :

La fonction renvoie **[!UICONTROL true]** si l’individu concerné par l’instance de parcours fait partie du segment Adobe Experience Platform &quot;men over 50&quot; (hommes de plus de 50 ans), **[!UICONTROL false]** dans le cas contraire.
