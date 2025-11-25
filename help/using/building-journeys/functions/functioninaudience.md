---
product: journey optimizer
title: Fonction inAudience
description: En savoir plus sur la fonction Adobe Experience Platform inAudience
feature: Journeys
role: Developer
level: Experienced
keywords: inAudience, fonction, expression, parcours, audience, segmentation
exl-id: 8417af75-6e97-4ad4-86b4-3ecd264a5560
version: Journey Orchestration
source-git-commit: 4f653c0bd3f6998dd54deeae996b7b0427a1744e
workflow-type: ht
source-wordcount: '600'
ht-degree: 100%

---

# Fonction inAudience {#inAudience}

La fonction `inAudience` est une fonction Adobe Experience Platform qui vous permet de vérifier si un individu de votre parcours appartient à une audience spécifique. Cette fonction puissante vous permet de créer des chemins de parcours personnalisés en fonction de l’appartenance à une audience, ce qui permet une segmentation et un ciblage sophistiqués au sein de vos expériences client.

Utilisez la fonction `inAudience` lorsque vous devez :

* diviser le parcours en fonction de l’appartenance à l’audience. [En savoir plus](../condition-activity.md#using-a-segment)
* Appliquer une logique conditionnelle qui dépend du fait qu’un profil appartient ou non à un segment spécifique
* Cibler des groupes spécifiques de clients et clientes avec des expériences personnalisées
* Évaluer la participation de l’audience en temps réel dans des conditions de parcours
* Combiner plusieurs vérifications d’audience pour créer des règles de ciblage complexes

La fonction évalue l’appartenance à l’audience en temps réel et renvoie une valeur booléenne, ce qui la rend idéale pour les nœuds de décision et les expressions conditionnelles. Les audiences sont définies et gérées dans [Adobe Experience Platform](https://platform.adobe.com/audience/overview){target="_blank"} (en savoir plus sur [l’utilisation des audiences](../../audience/about-audiences.md) dans Journey Optimizer). L’éditeur d’expression fournit des suggestions de saisie semi-automatique pour vous aider à les référencer avec précision.

**Statut de l’audience :**

Les audiences peuvent posséder deux statuts de participation :

* **Réalisé** : l’individu est éligible à la définition de l’audience et doit être un membre actif.
* **Sorti** : l’individu a quitté l’audience et ne se qualifie plus.

Seuls les individus ayant le statut **Réalisé** seront considérés comme des membres actifs de l’audience. Lorsque la fonction renvoie `true`, elle confirme que l’individu a le statut Réalisé ; lorsqu’elle renvoie `false`, elle indique le statut de sortie. Pour plus d’informations sur l’évaluation d’audience, reportez-vous à la [documentation de Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=fr#interpret-segment-results){target="_blank"}.

+++Syntaxe

`inAudience(<parameter>)`

+++

+++Paramètres

| Paramètre | Description | Type |
|--- |--- |--- |
| Audience | Nom de l’audience | `<string>` |

**Contraintes importantes :**

* Le nom de l’audience doit être une constante sous forme de chaîne.
* Il ne peut pas s’agir d’une référence de champ ou d’une expression.
* Vous pouvez récupérer jusqu’à 100 audiences dans un seul parcours.

+++

+++Signature et type renvoyé

`inAudience(<string>)`

Renvoie une valeur booléenne :
* `true` : l’individu est membre de l’audience (statut réalisé).

* `false` : l’individu n’est pas membre de l’audience (statut sorti).

+++

+++Exemples

`inAudience("men over 50")`

Renvoie **true** si l’individu concerné par l’instance de parcours figure dans l’audience Adobe Experience Platform « hommes de plus de 50 ans ». Sinon, elle renvoie **false**.

**Cas d’utilisation pratiques :**

```
// Simple audience check in a condition
inAudience("Premium Customers") == true

// Multiple audience evaluation
inAudience("High Value Customers") == true AND inAudience("Active Last 30 Days") == true

// Negation check
inAudience("Unsubscribed") == false
```

+++

## Mécanismes de sécurisation et limitations {#guardrails}

Lors de l’utilisation de la fonction `inAudience` dans vos parcours, tenez compte des mécanismes de sécurisation et limitations suivantes :

**Limite de récupération de l’audience :**
* Vous pouvez récupérer jusqu’à 100 audiences dans un seul parcours.
* L’éditeur d’expression fournit une liste d’audiences disponibles complétée automatiquement pour vous aider à les référencer correctement.

**Contraintes de paramètre :**
* Le nom de l’audience doit être une constante sous forme de chaîne.
* Les références et expressions de champ ne sont pas prises en charge en tant que paramètres.

**Modifications du nom de l’audience :**
* La modification du nom d’une audience existante dans Adobe Experience Platform ne met pas automatiquement à jour les références à cette audience dans vos expressions de parcours.
* Si votre nœud de condition utilise `inAudience('oldAudienceName')`, vous devez modifier manuellement l’expression pour utiliser le nouveau nom.
* Si vous ne mettez pas à jour le nom de l’audience, la condition de parcours ne fonctionnera plus et le comportement du parcours pourra être incorrect.

**Éléments à prendre en compte concernant la politique de fusion** :
* Lors de l’utilisation de plusieurs audiences avec la fonction `inAudience`, des incohérences avec les politiques de fusion peuvent entraîner des erreurs ou des alertes.
* Pour plus d’informations sur le comportement des politiques de fusion, consultez la section [Propriétés des parcours](../journey-properties.md).

## Rubriques connexes

Pour en savoir plus sur l’utilisation des audiences dans Adobe Journey Optimizer :

* **[À propos des audiences](../../audience/about-audiences.md)** - Découvrez comment fonctionnent les audiences dans Adobe Experience Platform et Journey Optimizer, y compris comment les créer et les gérer.
* **[Activité Lecture d’audience](../read-audience.md)** - Utilisez des audiences pour déclencher l’entrée dans un parcours et faire en sorte que tous les membres d’une audience rejoignent un parcours.
* **[Événements de qualification d’audience](../audience-qualification-events.md)** - Suivez les entrées et les sorties des profils dans les audiences pour déclencher des actions de parcours en temps réel.
* **[Utilisation d’audiences dans des conditions](../condition-activity.md#using-a-segment)** - Créez des chemins de parcours conditionnels en fonction de l’appartenance à une audience à l’aide de l’activité Condition.
* **[Propriétés de parcours - Politiques de fusion](../journey-properties.md)** - Découvrez comment fonctionnent les politiques de fusion lors de l’utilisation de plusieurs audiences avec la fonction inAudience.

