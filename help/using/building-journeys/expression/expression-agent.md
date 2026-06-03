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
source-git-commit: f39bcb2f8b68315b082014b96801c51223ac8a54
workflow-type: tm+mt
source-wordcount: 660
ht-degree: 13%

---


# Générer des expressions à l’aide de l’assistant d’expressions {#expression-agent}

>[!CONTEXTUALHELP]
>id="journeyExpAI"
>title="Générer des expressions à l’aide de l’assistant d’expressions"
>abstract="L’assistant d’expressions utilise l’IA générative pour vous aider à créer et à générer des expressions directement dans l’éditeur d’expression avancé des parcours. Par exemple, dans les conditions, les activités **Optimiser** ou **Attente** qui utilisent une date personnalisée. Décrivez vos besoins en termes simples et l’assistant génère l’expression correspondante."

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version bêta **publique**. Pour plus d’informations sur le cycle de publication et les phases de disponibilité, consultez le [cycle de publication de Journey Optimizer](../../rn/releases.md).
>
>Avant d’utiliser l’assistant d’expression, lisez les [Mécanismes de sécurisation et limites](../../content-management/gs-generative.md#generative-guardrails) qui s’appliquent aux fonctionnalités d’IA générative dans Journey Optimizer.

L’assistant d’expression est une fonctionnalité optimisée par l’IA intégrée à l’éditeur d’expression avancé du Parcours. Cela vous permet de générer des expressions valides à partir d’invites en langage clair.

Elle est disponible où s’ouvre le Parcours **[!UICONTROL Éditeur d’expression avancé]**. Par exemple, lorsque vous configurez des conditions et le routage dans une activité **[Optimiser](../optimize.md)** ou lorsque vous configurez une activité [**[!UICONTROL Attente ]**](../wait-activity.md) qui utilise une date personnalisée et pour laquelle vous avez besoin d’une expression `dateTimeOnly`.

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
