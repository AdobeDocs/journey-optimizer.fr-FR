---
product: journey optimizer
title: inSegment
description: En savoir plus sur la fonction inSegment
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inSegment, fonction, expression, parcours
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: 72bd00dedb943604b2fa85f7173cd967c3cbe5c4
workflow-type: tm+mt
source-wordcount: '201'
ht-degree: 35%

---

# inSegment {#inSegment}

Vérifie si un individu appartient à une audience donnée.

>[!NOTE]
>
>Vous pouvez récupérer jusqu’à 100 audiences.

Le nom de l’audience doit être une constante sous forme de chaîne. Il ne peut pas s’agir d’une référence de champ ni d’une expression.

Les audiences sont définies dans la variable [Adobe Experience Platform](https://platform.adobe.com/audience/overview). L’éditeur d’expression fournit une liste d’audiences complétée automatiquement.

Les audiences peuvent avoir trois états :

* existing : continue d’être dans l’audience.
* réalisé : est en train de saisir l’audience.
* exited : l’entité quitte l’audience.

Seuls les individus dotés de la fonction **Réalisé** et **Existant** les états de participation de l’audience seront considérés comme des membres de l’audience. Pour plus d’informations sur l’évaluation d’une audience, reportez-vous à la section [Documentation de Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=fr#interpret-segment-results).

`IF inSegment('segmentName') == true` signifie que vous avez un mappage segmentMembership avec le statut « entered/existing ».

`ELSE inSegment('segmentName') == false` signifie que vous avez un mappage segmentMembership avec le statut « exited ».

## Catégorie

Adobe Experience Platform

## Syntaxe de la fonction

`inSegment(<parameter>)`

## Paramètres

| Paramètre | Description | Type |
|--- |--- |--- |
| Segment | Nom de l’audience | `<string>` |

## Signature et type renvoyé

`inSegment(<string>)`

Renvoie une valeur booléenne.

## Exemple

`inSegment("men over 50")`

Explication :

La fonction renvoie **[!UICONTROL true]** si l’individu concerné par l’instance de parcours fait partie de l’audience Adobe Experience Platform nommée &quot;men over 50&quot; (hommes de plus de 50 ans), **[!UICONTROL false]** dans le cas contraire.
