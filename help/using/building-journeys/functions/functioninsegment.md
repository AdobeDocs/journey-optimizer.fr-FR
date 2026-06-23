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
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 521
ht-degree: 33%

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

Seules les personnes présentant le statut de participation d’audience **réalisé** sont considérées comme membres de l’audience. Pour plus d’informations sur l’évaluation d’une audience, consultez la [documentation du service de segmentation](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=fr#interpret-segment-results).

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

La fonction renvoie **[!UICONTROL true]** si la personne concernée par l’instance de parcours fait partie de l’audience Adobe Experience Platform nommée « men over 50 » (hommes de plus de 50 ans), **[!UICONTROL false]** dans le cas contraire.

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page documente la fonction `inSegment` héritée, qui vérifie si un profil de parcours appartient à une audience Adobe Experience Platform nommée et renvoie une valeur booléenne.

**Intentions:**
* Vérifier si un profil est un membre actif d’une audience nommée à l’aide de `inSegment`
* Utilisez `inSegment('name') == true` pour confirmer l’appartenance (active) à une audience réalisée dans une condition de parcours
* Utilisez `inSegment('name') == false` pour confirmer l’appartenance à une audience fermée (inactive)

**Glossaire:**
* **Réalisé** : statut de participation de l’audience, ce qui signifie que l’entité est actuellement qualifiée pour la définition de segment *(spécifique au produit)*
* **Sorti** : statut de participation de l’audience signifiant que l’entité quitte ou a quitté la définition de segment *(spécifique au produit)*

**Mécanismes de sécurisation :**
* Jusqu’à 100 audiences peuvent être récupérées dans un seul parcours
* Le nom de l’audience doit être une constante de chaîne ; les références aux champs et les expressions ne sont pas prises en charge en tant que paramètres

**Terminologie:**
* Nom canonique : inSegment — Acronyme : none — variantes : inAudience (fonction préférée actuelle)
* Synonymes : « inSegment » = « vérification de l’appartenance à l’audience » (hérité)
* Ne pas confondre : « inSegment » (fonction héritée/obsolète) ≠ « inAudience » (fonction recommandée actuelle)
* Ne pas confondre : « réalisé » (membre actif) ≠ « sorti » (n’est plus membre)

**FAQ:**
* **Q : Quelle est la différence entre `inSegment` et `inAudience` ?** — `inSegment` est le nom de la fonction héritée ; `inAudience` est la fonction actuellement recommandée. Tous deux vérifient l’appartenance à l’audience, mais `inAudience` dispose d’une documentation plus complète, y compris des mécanismes de sécurisation et des détails sur le délai de propagation.
* **Q : Que signifie `inSegment('name') == true` ?** — Cela signifie que le profil a un statut d’appartenance à un segment « réalisé », c’est-à-dire que la personne est un membre actif de l’audience.
* **Q : Puis-je transmettre une expression dynamique comme nom d’audience ?** — Non, le nom de l&#39;audience doit être une constante de chaîne ; les références aux champs et les expressions ne sont pas prises en charge.
* **Q : Combien d’audiences puis-je évaluer dans un parcours ?** — Jusqu&#39;à 100 audiences peuvent être récupérées dans un seul parcours.

+++
