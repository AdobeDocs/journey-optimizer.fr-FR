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
TQID: https://experienceleague.adobe.com/DU8HtduB2-GmakiaHBMFU1vzBBPoVTNvrOCPWQrr5SU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1279
ht-degree: 47%

---

# Fonction inAudience {#inAudience}

La fonction `inAudience` est une fonction Adobe Experience Platform qui vous permet de vérifier si un individu de votre parcours appartient à une audience spécifique. Cette fonction puissante vous permet de créer des chemins de parcours personnalisés en fonction de l’appartenance à une audience, ce qui permet une segmentation et un ciblage sophistiqués au sein de vos expériences client.

Utilisez la fonction `inAudience` lorsque vous devez :

* diviser le parcours en fonction de l’appartenance à l’audience. [En savoir plus](../conditions.md#using-a-segment)
* Appliquer une logique conditionnelle qui dépend du fait qu’un profil appartient ou non à un segment spécifique
* Cibler des groupes spécifiques de clients et clientes avec des expériences personnalisées
* Évaluer la participation de l’audience en temps réel dans des conditions de parcours
* Combiner plusieurs vérifications d’audience pour créer des règles de ciblage complexes

La fonction évalue l’appartenance à l’audience en temps réel et renvoie une valeur booléenne, ce qui la rend idéale pour les nœuds de décision et les expressions conditionnelles. Les audiences sont définies et gérées dans [Adobe Experience Platform](https://platform.adobe.com/audience/overview){target="_blank"} (en savoir plus sur [l’utilisation des audiences](../../audience/about-audiences.md) dans Journey Optimizer). L’éditeur d’expression fournit des suggestions de saisie semi-automatique pour vous aider à les référencer avec précision.

**Statut de l’audience :**

Les audiences peuvent posséder deux statuts de participation :

* **Réalisé** : l’individu est éligible à la définition de l’audience et doit être un membre actif.
* **Sorti** : l’individu a quitté l’audience et ne se qualifie plus.

Seuls les individus ayant le statut **Réalisé** seront considérés comme des membres actifs de l’audience. Lorsque la fonction renvoie `true`, elle confirme que l’individu a le statut Réalisé ; lorsqu’elle renvoie `false`, elle indique le statut de sortie. Pour plus d’informations sur l’évaluation d’audience, reportez-vous à la [documentation de Segmentation Service](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=fr#interpret-segment-results){target="_blank"}.

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

**Délai de propagation :** {#propagation-timing}

Lors de l’utilisation de `inAudience()` dans un nœud de condition, le délai d’évaluation de l’appartenance au segment varie en fonction de l’emplacement de la condition dans le parcours :

* **Dans un parcours Lecture d’audience, avant une activité Attente :** Journey Optimizer lit à partir de la projection par lots du profil. Les données de cette projection sont actualisées dans les **2 heures** suivant l’ingestion. Les audiences qui reposent sur des conditions basées sur la journée ou sur l’heure peuvent subir un retard supplémentaire. Ajoutez une courte [activité d’attente](../wait-activity.md) au début du parcours ou patientez le temps pour vous assurer que la dernière appartenance au segment est prise en compte.
* **Dans un parcours d’événement unitaire, ou après une activité Attente :** l’appartenance à un segment est lue à partir de la projection en flux continu (unitaire). Les données sont généralement disponibles en **15 minutes**. Pour plus d’informations, consultez la documentation sur l’ingestion par flux de [&#128279;](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/streaming/overview){target="_blank"}.

## Rubriques connexes

Pour en savoir plus sur l’utilisation des audiences dans Adobe Journey Optimizer :

* **[À propos des audiences](../../audience/about-audiences.md)** - Découvrez comment fonctionnent les audiences dans Adobe Experience Platform et Journey Optimizer, y compris comment les créer et les gérer.
* **[Activité Lecture d’audience](../read-audience.md)** - Utilisez des audiences pour déclencher l’entrée dans un parcours et faire en sorte que tous les membres d’une audience rejoignent un parcours.
* **[Événements de qualification d’audience](../audience-qualification-events.md)** - Suivez les entrées et les sorties des profils dans les audiences pour déclencher des actions de parcours en temps réel.
* **[Utilisation d’audiences dans des conditions](../conditions.md#using-a-segment)** - Créez des chemins de parcours conditionnels en fonction de l’appartenance à l’audience à l’aide de l’activité Optimiser
* **[Propriétés de parcours - Politiques de fusion](../journey-properties.md)** - Découvrez comment fonctionnent les politiques de fusion lors de l’utilisation de plusieurs audiences avec la fonction inAudience.

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page documente la fonction `inAudience`, qui vérifie en temps réel si un profil de parcours appartient à une audience Adobe Experience Platform nommée et renvoie une valeur booléenne utilisée dans des conditions de parcours.

**Intentions:**
* Branchement d’un chemin de parcours en fonction du fait qu’un profil est membre d’une audience spécifique à l’aide de `inAudience`
* Combinez plusieurs contrôles `inAudience` avec une logique AND/OR pour créer des conditions de ciblage complexes
* Vérifiez qu’un profil n’a pas rejoint une audience spécifique à l’aide d’une vérification par négation (`inAudience("...") == false`)
* Comprenez les différences de temps de propagation entre les parcours Lecture d’audience et les parcours d’événement unitaire.
* Identifiez et corrigez les références d’audience rompues causées par les changements de noms d’audience dans Adobe Experience Platform

**Glossaire:**
* **Réalisé** : statut de participation à l’audience indiquant que l’individu est actuellement qualifié pour la définition de l’audience et est un *membre actif (spécifique au produit)*
* **Sorti** : statut de participation de l’audience indiquant que l’individu a quitté l’audience et ne se qualifie plus *(spécifique au produit)*
* **Politique de fusion** : règle de Adobe Experience Platform qui détermine la manière dont les données de profil de plusieurs jeux de données sont combinées lors de l’évaluation des *d’appartenance à une audience (spécifiques à un produit)*
* **Projection par lots** : la banque de données de profils s’est actualisée selon un calendrier (dans les 2 heures suivant l’ingestion) utilisé par l’*Lecture de parcours d’audience (spécifique au produit)*
* **Projection en flux continu** : banque de données de profil en temps réel (généralement disponible dans les 15 minutes) utilisée dans les parcours d’événement unitaire et après les activités d’attente *(spécifique au produit)*

**Mécanismes de sécurisation :**
* Un seul parcours peut récupérer jusqu’à 100 audiences
* Le paramètre du nom de l’audience doit être une constante de chaîne ; les références aux champs et les expressions dynamiques ne sont pas prises en charge
* Le changement de nom d’une audience dans Adobe Experience Platform ne met pas automatiquement à jour les références `inAudience` dans les expressions de parcours. Des mises à jour manuelles sont nécessaires
* Des politiques de fusion incohérentes entre plusieurs audiences utilisées dans le même parcours peuvent provoquer des erreurs ou des alertes

**Terminologie:**
* Nom canonique : inAudience — Acronyme : none — variantes : inSegment (nom hérité)
* Synonymes : « inAudience » = « fonction de vérification de l’appartenance à une audience »
* Ne pas confondre : « Réalisé » (membre actif) ≠ « Sorti » (n’est plus membre)
* Ne pas confondre : « inAudience » (fonction actuelle) ≠ « inSegment » (fonction héritée obsolète)

**FAQ:**
* **Q : Que renvoie-`inAudience` lorsqu’un profil a quitté l’audience ?** — Renvoie `false` ; seuls les profils avec le statut « Réalisé » sont considérés comme des membres actifs et renvoient des `true`.
* **Q : Combien d’audiences puis-je archiver dans un seul parcours ?** — Jusqu&#39;à 100 audiences peuvent être récupérées dans un seul parcours.
* **Q : Que se passe-t-il si je renomme une audience dans Adobe Experience Platform après l’avoir utilisée dans un parcours ?** — L&#39;expression de parcours n&#39;est pas mise à jour automatiquement ; vous devez modifier manuellement l&#39;appel `inAudience` pour utiliser le nouveau nom d&#39;audience, sinon la condition sera rompue.
* **Q : À quelle vitesse l’appartenance à une audience est-elle disponible après une mise à jour de profil dans un parcours Lecture d’audience ?** — Dans un parcours Lecture d’audience avant une activité Attente , les données sont lues à partir de la projection par lots actualisée dans les 2 heures suivant l’ingestion.
* **Q : Puis-je transmettre un attribut de profil en tant que paramètre de nom d’audience ?** — Non, le nom de l&#39;audience doit être une constante de chaîne ; les références aux champs et les expressions ne sont pas prises en charge.

+++
