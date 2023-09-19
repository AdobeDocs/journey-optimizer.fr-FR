---
title: Cas d’utilisation de la prise de décision d’expérience
description: Découvrez comment créer des décisions à l’aide d’expériences avec le canal basé sur le code
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 4aea5c1434caa07aad26445c49a3d5c6274502ec
workflow-type: tm+mt
source-wordcount: '398'
ht-degree: 10%

---

# Cas d’utilisation de la prise de décision d’expérience {#experience-decisioning-uc}

>[!BEGINSHADEBOX]

Ce guide vous apportera la documentation suivante :

* [Prise en main d’Experience Decisioning](gs-experience-decisioning.md)
* Gestion des éléments de décision
   * [Configuration du catalogue d’éléments](catalogs.md)
   * [Création d’éléments de décision](items.md)
   * [Gestion des collections d’éléments](collections.md)
* Configuration de la sélection d’éléments
   * [Créer des règles de décision](rules.md)
   * [Création de méthodes de classement](ranking.md)
* [Créer des stratégies de sélection](selection-strategies.md)
* [Création de stratégies de décision](create-decision.md)
* **[Découvrir un cas pratique](experience-decisioning-uc.md)**

>[!ENDSHADEBOX]

Dans ce cas pratique, vous définissez deux traitements de diffusion contenant chacun une stratégie de décision différente afin de mesurer celui qui fonctionne le mieux pour votre audience cible.

## Création d’éléments et de stratégies

Vous devez d’abord créer des éléments, les regrouper dans des collections, configurer des règles et des méthodes de classement. Ces éléments vous permettront de créer des stratégies de sélection.

1. Accédez à **[!UICONTROL Experience Decisioning]** > **[!UICONTROL Éléments]** et créer plusieurs éléments d’offre. Définissez des contraintes à l’aide d’audiences ou de règles afin de limiter chaque élément à des profils spécifiques uniquement. [En savoir plus](items.md)

   <!--
   1. From the items list, click the **[!UICONTROL Edit schema]** button  and edit the custom attributes if needed. [Learn how to work with catalogs](catalogs.md)-->

1. Créer **collections** pour classer et regrouper vos éléments de décision en fonction de vos préférences. [En savoir plus](collections.md)

1. Créer **règles de décision** pour déterminer à qui un élément de décision peut être affiché. [En savoir plus](rules.md)

1. Créer **méthodes de classement** et les appliquer dans les stratégies de décision afin de déterminer l’ordre de priorité de la sélection des éléments de décision. [En savoir plus](ranking.md)

1. Build **stratégies de sélection** qui tirent parti des collections, des règles de décision et des méthodes de classement afin d’identifier les éléments de décision adaptés à l’affichage sur les profils. [En savoir plus](selection-strategies.md)

## Création de stratégies de décision

Pour présenter la meilleure offre et expérience dynamique aux visiteurs de votre site web ou de votre application mobile, ajoutez une stratégie de décision à une campagne basée sur du code.

Définissez deux traitements de diffusion contenant chacun une stratégie de décision différente.

1. Créez une opération et sélectionnez l’option **[!UICONTROL Expérience basée sur le code (bêta)]** action. [En savoir plus](../code-based/create-code-based.md)

   >[!NOTE]
   >
   >La fonctionnalité d’expérience basée sur le code est actuellement disponible en version bêta pour sélectionner uniquement les utilisateurs. Pour rejoindre le programme Beta, contactez l’assistance clientèle d’Adobe.

1. Dans la page de résumé de l&#39;opération, cliquez sur **[!UICONTROL Créer une expérience]** pour commencer à configurer votre expérience de contenu. [En savoir plus](../campaigns/content-experiment.md)

1. Sélectionnez la variable **[!UICONTROL Décisions]** icône, cliquez sur **[!UICONTROL Créer une décision]** et renseignez les détails de la décision. [En savoir plus](create-decision.md)

   ![](assets/decision-code-based-create.png)

1. Définissez les stratégies de sélection de votre décision. Cliquez sur **[!UICONTROL Ajouter une stratégie]**.

1. Cliquez sur **[!UICONTROL Créer]**. La nouvelle décision est ajoutée sous **[!UICONTROL Décisions]**.

   ![](assets/decision-code-based-decision-added.png)

1. Cliquez sur l’icône d’actions supplémentaires (trois points) et sélectionnez **[!UICONTROL Ajouter]**. Vous pouvez maintenant ajouter tous les attributs de décision que vous souhaitez dans cette section.

   ![](assets/decision-code-based-add-decision.png)

1. Vous pouvez également ajouter tout autre attribut disponible dans l’éditeur d’expression, tel que les attributs de profil.

   ![](assets/decision-code-based-decision-profile-attribute.png)

1. Créez le traitement B et répétez les étapes ci-dessus pour créer une autre décision.

1. Enregistrez votre contenu.


