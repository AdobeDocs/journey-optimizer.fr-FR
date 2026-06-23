---
solution: Journey Optimizer
product: journey optimizer
title: Générer des expressions à l’aide de l’assistant d’expressions
description: Découvrez comment utiliser l’assistant Expression dans Adobe Journey Optimizer pour générer des expressions directement dans l’éditeur d’expression avancé du Parcours à l’aide d’invites en langage naturel.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
badge: label="Bêta publique" type="Informative"
mini-toc-levels: 2
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1147
ht-degree: 6%

---


# Générer des expressions à l’aide de l’assistant d’expressions {#expression-agent}

>[!CONTEXTUALHELP]
>id="journeyExpAI"
>title="Générer des expressions à l’aide de l’assistant d’expressions"
>abstract="L’assistant d’expressions utilise l’IA générative pour vous aider à créer et à générer des expressions directement dans l’éditeur d’expression avancé des parcours. Par exemple, dans les conditions, les activités **Optimiser** ou **Attente** qui utilisent une date personnalisée. Lorsque vous décrivez vos besoins en langage clair, l’assistant génère l’expression correspondante pour vous."

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version bêta **publique**. Pour plus d’informations sur le cycle de publication et les phases de disponibilité, consultez le [cycle de publication de Journey Optimizer](../../rn/releases.md).
>
>Avant d’utiliser l’assistant d’expression, lisez les [Mécanismes de sécurisation et limites](../../content-management/gs-generative.md#generative-guardrails) qui s’appliquent aux fonctionnalités d’IA générative dans Journey Optimizer.

L’assistant d’expression est une fonctionnalité optimisée par l’IA intégrée à l’éditeur d’expression avancé du Parcours. Cela vous permet de générer des expressions valides à partir d’invites en langage clair.

Elle est disponible où s’ouvre le Parcours **[!UICONTROL Éditeur d’expression avancé]**. Par exemple, lorsque vous configurez des conditions et le routage dans une activité **[Optimiser](../optimize.md)** ou lorsque vous configurez une activité [**[!UICONTROL Attente &#x200B;]**](../wait-activity.md) qui utilise une date personnalisée et pour laquelle vous avez besoin d’une expression `dateTimeOnly`.

## Générer une expression {#generate}

Pour générer une expression à l’aide de l’assistant d’expression :

1. Ouvrez l’**[!UICONTROL Éditeur d’expression avancé]** dans votre parcours, par exemple à partir d’une condition d’embranchement, d’une activité **[!UICONTROL Optimiser]** ou d’une activité **[!UICONTROL Attente]** avec une date personnalisée.

   ![](../assets/expression-assistant-pane.png)

1. Dans le champ de texte, décrivez l’expression que vous souhaitez générer en langage clair. Par exemple :

   * *« Utilisateurs originaires des États-Unis et âgés de plus de 18 ans »*
   * *« Clients ayant effectué un achat au cours des 30 derniers jours »*

   Voir [Exemples d’invites](#example-prompts) à la fin de cette page pour obtenir des idées.

1. Cliquez sur **[!UICONTROL Générer]** pour envoyer votre invite.

   L’assistant commence à générer l’expression correspondante et affiche des messages de statut de progression pendant que la génération est en cours.

   >[!NOTE]
   >
   >Si l&#39;assistant ne peut pas générer une expression valide (par exemple, si votre invite fait référence à des champs qui n&#39;existent pas dans les sources de données disponibles), un message d&#39;erreur s&#39;affiche. Lorsque cela se produit, révisez votre invite pour utiliser les noms de champ et les sources de données disponibles dans la configuration de votre parcours, puis générez à nouveau.

1. Une fois que l’expression est prête, passez en revue le résultat dans le panneau.

   ![](../assets/expression-assistant-result.png)

   * Cliquez sur l’icône ![Aperçu](../assets/do-not-localize/generation-preview.svg) avant l’application pour passer en revue la sortie de l’assistant pour le scénario que vous avez demandé.

   * Cliquez sur **[!UICONTROL Appliquer]** pour insérer l’expression générée directement dans l’éditeur d’expression avancé (le même emplacement que vous collez manuellement).
   * Utilisez le contrôle de copie pour récupérer le texte de l’expression suggérée et le coller ailleurs si nécessaire.

## Exemples d’invites {#example-prompts}

Les listes ci-dessous ne sont que des idées reçues. Elles n’affichent pas la syntaxe de l’expression générée. La sortie exacte dépend des champs et activités définis dans votre parcours.

### Événement de parcours et action personnalisée {#example-prompts-event-action}

* *« événement dont le total du prix de la commande est supérieur à 100 »*
* *« événement au cours duquel la commande a été créée au cours des 7 derniers jours »*
* *« événement pour lequel le type d’événement est un achat commercial »*
* *« événement avec commande créée au cours de la dernière heure »*
* *« événement dont le prix total de la commande est supérieur à 200 et la réponse de l’action comporte un code de statut »*

### Expressions de l’activité d’attente {#example-prompts-datetime}

Lorsqu’une activité **[!UICONTROL Attente]** utilise une date personnalisée, vous définissez le moment où le profil continue en créant une expression `dateTimeOnly` dans l’éditeur d’expression **[!UICONTROL avancé]**. Par exemple, à partir d’un attribut de profil, d’une date et heure d’événement, de données de qualification de segment ou d’un décalage calculé par rapport à l’heure actuelle. Pour savoir comment configurer les attentes personnalisées et les limites applicables, consultez [Attente personnalisée](../wait-activity.md#custom).

* *« utiliser la date de la dernière commande du client comme date et heure uniquement »*
* *« utiliser l’heure de l’e-mail de consentement comme date et heure uniquement »*
* *« convertir l’heure de la dernière qualification de l’appartenance au segment en heure de date uniquement »*
* *« nœud d’attente : une semaine après Noël 2024 sous la forme date et heure uniquement »*
* *« nœud d’attente : dans 30 jours, à 22 h, uniquement pour la date et l’heure »*
* *« attendez jusqu’à 9 h aujourd’hui dans le fuseau horaire UTC, renvoyez-le uniquement en tant qu’heure »*

## Ressources connexes {#related}

* [Utilisation de l’éditeur d’expression avancé](expressionadvanced.md) — Présentation de l’interface de l’éditeur d’expression et de la syntaxe prise en charge.
* [Prise en main de l’assistant AI dans Journey Optimizer](../../content-management/gs-generative.md) — Mécanismes de sécurisation généraux, accès et configuration pour les fonctionnalités d’IA génératives.

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page décrit l’assistant d’expression, une fonctionnalité optimisée par l’IA de l’éditeur d’expression avancé de Parcours qui génère des expressions de parcours valides à partir d’invites en langage clair.

**Intentions:**

* Générez une expression de parcours à partir d’une description en langage naturel à l’aide de l’assistant d’expression
* Appliquez une expression générée directement dans l’éditeur d’expression avancé à l’aide du bouton Appliquer .
* Utilisez l’assistant d’expression dans les activités d’optimisation, les activités de condition et les activités d’attente de date personnalisée
* Fournissez des exemples d’invites pour les conditions basées sur un événement et les expressions d’attente `dateTimeOnly`
* Résolvez les problèmes de génération en modifiant les invites pour référencer des noms de champs et des sources de données valides

**Glossaire:**

* **Assistant d’expression** : fonctionnalité générative optimisée par l’IA intégrée à l’éditeur d’expression avancé de Parcours qui convertit les invites en langage clair en expressions de parcours valides *(spécifiques au produit)*
* **Éditeur d’expression avancé** : interface Journey Optimizer permettant d’écrire des expressions complexes dans des conditions, des activités d’attente et des *de mappage de paramètres d’action (spécifiques au produit)*
* **dateTimeOnly** : type d’expression date-heure sans fuseau horaire, obligatoire pour les activités d’attente avec date personnalisée *(spécifiques au produit)*
* **Activité d’optimisation** : activité de parcours prenant en charge les conditions d’embranchement configurables via l’éditeur d’expression avancé *(spécifique au produit)*

**Mécanismes de sécurisation :**

* L&#39;assistant d&#39;expression est actuellement en version **bêta publique** — la disponibilité et le comportement peuvent changer
* Les mécanismes de sécurisation et limitations de l’IA générative de la documentation principale de l’assistant d’IA s’appliquent à cette fonctionnalité
* Si l&#39;assistant fait référence à des champs qui ne figurent pas dans les sources de données de votre parcours, il renvoie une erreur — révisez l&#39;invite pour utiliser les noms de champ disponibles
* La syntaxe exacte de l’expression générée dépend des champs et activités configurés dans votre parcours spécifique

**Terminologie:**

* Nom canonique : Assistant d’expression — Acronyme : none — variantes : IA dédiée à l’expression, générateur d’expression de parcours
* Synonymes : « Assistant d’expression » = « Générateur d’expression IA »
* Ne pas confondre : Assistant d’expression (générateur optimisé par l’IA) ≠ Éditeur d’expression avancé (l’éditeur de code manuel lui-même)

**FAQ:**

* **Q : Où l’assistant d’expression est-il disponible ?** — Elle est disponible à l&#39;emplacement où l&#39;éditeur d&#39;expression avancé de Parcours s&#39;ouvre, y compris les activités Condition, Optimiser et Attendre avec une date personnalisée.
* **Q : Que se passe-t-il si l’assistant ne peut pas générer une expression valide ?** — Un message d&#39;erreur s&#39;affiche ; vous devez réviser votre invite pour utiliser les noms de champ et les sources de données qui existent dans votre configuration de parcours.
* **Q : Comment insérer une expression générée dans l’éditeur ?** — Cliquez sur le bouton **Appliquer** dans le panneau de l&#39;assistant pour l&#39;insérer directement à l&#39;emplacement actuel du curseur dans l&#39;éditeur d&#39;expression avancé.
* **Q : L’assistant d’expression peut-il générer des expressions `dateTimeOnly` pour les activités d’attente ?** — Oui ; par exemple, l’invite « 30 jours à partir de maintenant à 22 h comme date et heure uniquement » génère l’expression de `dateTimeOnly` appropriée.
* **Q : L&#39;assistant d&#39;expression est-il généralement disponible ?** — Non ; il est actuellement en version bêta publique. Consultez la page du cycle de publication de Journey Optimizer pour connaître les mises à jour de disponibilité.

+++
