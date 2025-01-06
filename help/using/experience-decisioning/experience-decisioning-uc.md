---
title: Cas d’utilisation de la prise de décision
description: Découvrez comment créer des décisions à l’aide d’expériences avec le canal basé sur le code.
feature: Decisioning
topic: Integrations
role: User
level: Intermediate, Experienced
hide: true
hidefromtoc: true
exl-id: 09770df2-c514-4217-a71b-e31c248df543
source-git-commit: 83ad828a4d342bba10284cdd20d22eb325e3e1f7
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 37%

---

# Cas d’utilisation de la prise de décision {#experience-decisioning-uc}

Ce cas pratique présente toutes les étapes nécessaires pour utiliser Decisioning avec le canal basé sur le code [!DNL Journey Optimizer].

<!--In this use case, you create a campaign where you define two delivery treatments - each containing a different decision policy in order to measure which one performs best for your target audience.-->

Dans ce cas d&#39;utilisation, vous ne savez pas si une formule de classement spécifique sera plus performante que les priorités d&#39;offre préaffectées.

Pour mesurer celui qui fonctionne le mieux pour votre audience cible, créez une campagne où vous définissez deux traitements de diffusion :

<!--Set up the experiment such that:-->

* Le premier traitement contient une stratégie de sélection avec une priorité pour méthode de classement.
* Le second traitement contient une stratégie de sélection différente pour laquelle une formule est la méthode de classement.

## Créer des stratégies de sélection

Tout d’abord, vous devez créer deux stratégies de sélection : une avec la priorité comme méthode de classement et une autre avec une formule comme méthode de classement.

### Création de la première stratégie de sélection

Dans la première stratégie de sélection, sélectionnez priorité comme méthode de classement. Suivez les étapes ci-dessous.

1. Créez un élément de décision. [Voici comment procéder](items.md)

1. Définissez la **[!UICONTROL priorité]** de l’élément de décision par rapport aux autres. Si un profil est éligible à plusieurs éléments, une priorité plus élevée accorde la priorité sur les autres.

   ![](assets/exd-uc-item-priority.png)

   >[!NOTE]
   >
   >La priorité est un type de données Entier. Tous les attributs qui sont des types de données Entier doivent contenir des valeurs entières (pas de décimales).

1. Définissez des audiences ou des règles pour limiter l’élément à des profils spécifiques uniquement. [Découvrez comment définir l&#39;éligibilité de l&#39;élément de décision](items.md#eligibility)

1. Définissez des règles de limitation pour définir le nombre maximal de fois où une offre peut être présentée. [Voici comment procéder](items.md#capping)

<!--1. If needed, repeat the steps above to create one or more additional decision items.-->

1. Créez une **collection** où vos éléments de décision seront inclus. [En savoir plus](collections.md)

1. Créez une **stratégie de sélection**. [Voici comment procéder](selection-strategies.md#create-selection-strategy)

1. Sélectionnez la [collection](collections.md) qui contient la ou les offres à prendre en compte.

1. [Choisissez la méthode de classement](#select-ranking-method) à utiliser pour sélectionner la meilleure offre pour chaque profil. Dans ce cas, sélectionnez **[!UICONTROL Priorité des offres]**. [En savoir plus](selection-strategies.md#offer-priority)

   ![](assets/exd-uc-strategy-priority.png)

   <!--If multiple offers are eligible for this strategy, the [Offer priority](#offer-priority) method uses the value defined in the offers.-->

### Créer la deuxième stratégie de sélection

Dans la deuxième stratégie de sélection, sélectionnez une formule comme méthode de classement. Suivez les étapes ci-dessous.

1. Créez un élément de décision. [Voici comment procéder](items.md)

<!--1. Set the same **[!UICONTROL Priority]** as for the first decision item. TBC?-->

1. Définissez des audiences ou des règles pour limiter l’élément à des profils spécifiques uniquement. [Découvrez comment définir l&#39;éligibilité de l&#39;élément de décision](items.md#eligibility)

1. Définissez des règles de limitation pour définir le nombre maximal de fois où une offre peut être présentée. [Voici comment procéder](items.md#capping)

<!--1. If needed, repeat the steps above to create one or more additional decision items.-->

1. Créez une **collection** où vos éléments de décision seront inclus. [En savoir plus](collections.md)

1. Créez une **stratégie de sélection**. [Voici comment procéder](selection-strategies.md#create-selection-strategy)

1. Sélectionnez la [collection](collections.md) qui contient la ou les offres à prendre en compte.

1. [Sélectionnez la méthode de classement](#select-ranking-method) à utiliser pour sélectionner la meilleure offre pour chaque profil. Dans ce cas, sélectionnez **[!UICONTROL Formule]** pour utiliser un score calculé spécifique afin de choisir l’offre éligible à diffuser. [En savoir plus](selection-strategies.md#ranking-formula)

   ![](assets/exd-uc-strategy-formula.png)

<!--
## Create decision items and selection strategies

You first need to create items, group them together in collections, set up rules and ranking methods. These elements will allow you to build selection strategies.

1. Navigate to **[!UICONTROL Decisioning]** > **[!UICONTROL Catalogs]** and create several decision items. Set constraints using audiences or rules to restrict each item to specific profiles only. [Learn more](items.md)

1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)

1. Create **collections** to categorize and group your decision items according to your preferences. [Learn more](collections.md)

1. Create **decision rules** to determine to whom a decision item can be shown. [Learn more](rules.md)

1. Create **ranking methods** and apply them within decision strategies to determine the priority order for selecting decision items. [Learn more](ranking.md)

1. Build **selection strategies** that leverage collections, decision rules, and ranking methods to identify the decision items suitable for displaying to profiles. [Learn more](selection-strategies.md)
-->

## Créer des politiques de décision

<!--To present the best dynamic offer and experience to your visitors on your website or mobile app, add a decision policy to a code-based campaign.

Define two delivery treatments each containing a different decision policy.-->

1. Créez une campagne et sélectionnez l’action **[!UICONTROL Expérience basée sur du code]**. [En savoir plus](../code-based/create-code-based.md).

1. Dans la fenêtre **[!UICONTROL Modifier le contenu]**, commencez à personnaliser votre traitement A.

1. Sélectionnez l’icône **[!UICONTROL Décisions]**, cliquez sur **[!UICONTROL Créer une décision]** et renseignez les détails de la décision. [En savoir plus](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. Sélectionnez la première stratégie que vous avez créée. Cliquez sur **[!UICONTROL Ajouter une stratégie]**.

1. Cliquez sur **[!UICONTROL Créer]**. La nouvelle décision est ajoutée sous **[!UICONTROL Décisions]**.

   ![](assets/decision-code-based-decision-added.png)

1. Cliquez sur l’icône d’actions supplémentaires (points de suspension) et sélectionnez **[!UICONTROL Ajouter]**. Vous pouvez maintenant ajouter tous les attributs de décision que vous souhaitez dans cette section.

   ![](assets/decision-code-based-add-decision.png)

1. Vous pouvez également ajouter tout autre attribut disponible dans l’éditeur de personnalisation, tel que des attributs de profil.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. Dans la page de résumé de la campagne, cliquez sur **[!UICONTROL Créer une expérience]** pour commencer à configurer votre expérience de contenu. [En savoir plus](../content-management/content-experiment.md)

1. Dans la fenêtre **[!UICONTROL Modifier le contenu]**, sélectionnez le traitement B et répétez les étapes ci-dessus pour créer une autre décision.

1. Sélectionnez la deuxième stratégie que vous avez créée. Cliquez sur **[!UICONTROL Ajouter une stratégie]**.

1. Enregistrez votre contenu.
