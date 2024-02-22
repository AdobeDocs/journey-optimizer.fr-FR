---
product: journey optimizer
title: inAudience
description: En savoir plus sur la fonction inAudience
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inAudience, fonction, expression, parcours
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '191'
ht-degree: 83%

---

# inAudience {#inAudience}

Vérifie si une personne appartient à une audience donnée.

>[!NOTE]
>
>Vous pouvez récupérer jusqu’à 100 audiences.

Le nom de l’audience doit être une constante sous forme de chaîne. Il ne peut pas s’agir d’une référence de champ ni d’une expression.

Les audiences sont définies dans [Adobe Experience Platform](https://platform.adobe.com/audience/overview). L’éditeur d’expression fournit une liste des audiences remplie automatiquement.

Les audiences peuvent posséder trois statuts :

* existant : lʼentité reste dans l’audience.
* réalisé : lʼentité entre dans l’audience.
* sorti : lʼentité quitte l’audience.

Seules les personnes présentant les statuts de participationd&#39;audience d’audience **Réalisé** et **Existant** sont considérés comme membres de l’audience. Pour plus d’informations sur l’évaluation d’une audience, consultez la [documentation du service de segmentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=fr#interpret-segment-results).

`inAudience('audienceName') == true` signifie que vous disposez d’un segmentMembership avec le statut renseigné/existant.

`inAudience('audienceName') == false` signifie que vous disposez d’un segmentMembership avec le statut de sortie.

## Catégorie

Adobe Experience Platform

## Syntaxe de la fonction

`inAudience(<parameter>)`

## Paramètres

| Paramètre | Description | Type |
|--- |--- |--- |
| Audience | Nom de l’audience | `<string>` |

## Signature et type renvoyé

`inAudience(<string>)`

Renvoie une valeur booléenne.

## Exemple

`inAudience("men over 50")`

Explication :

La fonction renvoie **[!UICONTROL true]** si la personne concernée par l’instance de parcours figure dans l’audience Adobe Experience Platform « hommes de plus de 50 ans », **[!UICONTROL false]** dans le cas contraire.
