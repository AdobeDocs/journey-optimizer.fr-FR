---
product: journey optimizer
title: inSegment
description: En savoir plus sur la fonction inSegment
feature: Journeys
role: Developer
level: Experienced
keywords: inSegment, fonction, expression, parcours
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: ht
source-wordcount: '183'
ht-degree: 100%

---

# inSegment {#inSegment}

Vérifie si une personne appartient à une audience donnée.

>[!NOTE]
>
>Vous pouvez récupérer jusqu’à 100 audiences.

Le nom de l’audience doit être une constante sous forme de chaîne. Il ne peut pas s’agir d’une référence de champ ni d’une expression.

Les audiences sont définies dans [Adobe Experience Platform](https://platform.adobe.com/audience/overview). L’éditeur d’expression fournit une liste des audiences remplie automatiquement.

Les audiences peuvent posséder deux statuts :

* réalisé : l’entité est admissible pour la définition de segment.
* sorti : lʼentité quitte la définition de segment.

Seules les personnes présentant le statut de participation d’audience **réalisé** sont considérées comme membres de l’audience. Pour plus d’informations sur l’évaluation d’une audience, consultez la [documentation du service de segmentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=fr#interpret-segment-results).

`inSegment('segmentName') == true` signifie que vous avez un mappage segmentMembership avec le statut « entered/existing ».

`inSegment('segmentName') == false` signifie que vous avez un mappage segmentMembership avec le statut « exited ».

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

La fonction renvoie **[!UICONTROL true]** si la personne concernée par l’instance de parcours figure dans l’audience Adobe Experience Platform « hommes de plus de 50 ans », **[!UICONTROL false]** dans le cas contraire.
