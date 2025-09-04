---
product: journey optimizer
title: inAudience
description: En savoir plus sur la fonction inAudience
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: inAudience, fonction, expression, parcours
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
source-git-commit: 62783c5731a8b78a8171fdadb1da8a680d249efd
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 100%

---

# inAudience {#inAudience}

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

`inAudience('audienceName') == true` signifie que vous avez un segmentMembership avec le statut « entré ».

`inAudience('audienceName') == false` signifie que vous avez un segmentMembership avec le statut « quitté ».


>[!IMPORTANT]
>
>La modification du nom d’une audience existante ne met pas automatiquement à jour les références à cette audience dans vos expressions de parcours. Si votre nœud de condition utilise `inAudience('oldAudienceName')`, vous devez modifier manuellement l’expression pour utiliser le nouveau nom. Si vous ne le faites pas, la condition du parcours sera rompue.

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

La fonction renvoie **[!UICONTROL true]** si l’individu concerné par l’instance de parcours figure dans l’audience Adobe Experience Platform « hommes de plus de 50 ans ». Sinon, elle renvoie **[!UICONTROL false]**.

