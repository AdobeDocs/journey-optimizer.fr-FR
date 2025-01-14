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
source-git-commit: 98b7a5493a4e325328ab349c405af423b3836807
workflow-type: tm+mt
source-wordcount: '789'
ht-degree: 54%

---

# Cas d’utilisation de la prise de décision {#experience-decisioning-uc}

Ce cas pratique présente toutes les étapes nécessaires pour utiliser les décisions avec le canal basé sur le code [!DNL Journey Optimizer].

Dans cet exemple, vous ne savez pas si une formule de classement spécifique sera plus performante que les priorités d&#39;offre préaffectées. Pour mesurer celui qui fonctionne le mieux pour votre audience cible, vous créez une campagne à l’aide de [Expérience de contenu](../content-management/content-experiment.md) où vous définissez deux traitements de diffusion :

* Le premier traitement utilise la priorité comme méthode de classement.
* Le deuxième traitement utilise une formule comme méthode de classement.

## Créer des stratégies de sélection

Tout d’abord, vous devez créer deux stratégies de sélection : une avec la priorité comme méthode de classement et une autre avec une formule comme méthode de classement.

>[!NOTE]
>
>Vous pouvez également créer des éléments de décision uniques sans avoir à exécuter une stratégie de sélection. La priorité définie pour chaque élément s’applique.

### Création d’une stratégie à l’aide de la priorité

Pour créer la première stratégie de sélection avec la priorité comme méthode de classement, procédez comme suit.

1. Créez un élément de décision. [Voici comment procéder](items.md)

1. Définissez la **[!UICONTROL priorité]** de l’élément de décision par rapport aux autres. Si un profil est éligible à plusieurs éléments, une priorité plus élevée accorde la priorité sur les autres.

   ![](assets/exd-uc-item-priority.png){width="90%"}

   >[!NOTE]
   >
   >La priorité est un type de données Entier. Tous les attributs qui sont des types de données Entier doivent contenir des valeurs entières (pas de décimales).

1. Configurez l’éligibilité de l’élément de décision :

   * Définissez les audiences ou les règles afin de limiter l’élément à des profils spécifiques uniquement. [En savoir plus](items.md#eligibility)

   * La définition de règles de limitation est utilisée pour définir le nombre maximum de fois où une offre peut être présentée. [En savoir plus](items.md#capping)

1. Si nécessaire, répétez les étapes ci-dessus pour créer des éléments de décision supplémentaires.

1. Créez une **collection** dans laquelle vos éléments de décision seront inclus. [En savoir plus](collections.md)

1. Créez une [stratégie de sélection](selection-strategies.md#create-selection-strategy) et sélectionnez la [collection](collections.md) qui contient la ou les offres à prendre en compte.

1. [Définissez la méthode de classement](#select-ranking-method) à utiliser pour sélectionner la meilleure offre pour chaque profil. Dans ce cas, sélectionnez **[!UICONTROL Priorité des offres]** : si plusieurs offres sont éligibles pour cette stratégie, le moteur de décision utilise la valeur définie comme **[!UICONTROL Priorité]** dans la ou les offres. [En savoir plus](selection-strategies.md#offer-priority)

   ![](assets/exd-uc-strategy-priority.png){width="90%"}

### Création d’une autre stratégie à l’aide d’une formule

Pour créer la deuxième stratégie de sélection avec la sélection d’une formule comme méthode de classement, procédez comme suit.

1. Créez un élément de décision. [Voici comment procéder](items.md)

   <!--Do you need to set the same **[!UICONTROL Priority]** as for the first decision item, or it won't be considered at all?-->

1. Configurez l’éligibilité de l’élément de décision :

   * Définissez les audiences ou les règles afin de limiter l’élément à des profils spécifiques uniquement. [En savoir plus](items.md#eligibility)

   * La définition de règles de limitation est utilisée pour définir le nombre maximum de fois où une offre peut être présentée. [En savoir plus](items.md#capping)

1. Si nécessaire, répétez les étapes ci-dessus pour créer des éléments de décision supplémentaires.

1. Créez une **collection** dans laquelle vos éléments de décision seront inclus. [En savoir plus](collections.md)

1. Créez une [stratégie de sélection](selection-strategies.md#create-selection-strategy) et sélectionnez la [collection](collections.md) qui contient la ou les offres à prendre en compte.

1. [Définissez la méthode de classement](#select-ranking-method) à utiliser pour sélectionner la meilleure offre pour chaque profil. Dans ce cas, sélectionnez **[!UICONTROL Formule]** pour utiliser un score calculé spécifique afin de déterminer l’offre éligible à diffuser. [En savoir plus](selection-strategies.md#ranking-formula)

   ![](assets/exd-uc-strategy-formula.png){width="90%"}

## Créer une campagne d’expérience basée sur le code

<!--To present the best dynamic offer and experience to your visitors on your website or mobile app, add a decision policy to a code-based campaign.

Define two delivery treatments each containing a different decision policy.-->

Une fois que vous avez configuré les deux stratégies de sélection, créez une campagne d’expérience basée sur le code dans laquelle vous définissez un traitement différent pour chaque stratégie, afin de comparer celle qui fonctionne le mieux.

1. Créez une campagne et sélectionnez l’action **[!UICONTROL Expérience basée sur du code]**. [En savoir plus](../code-based/create-code-based.md)

1. Dans la page de résumé de la campagne, cliquez sur **[!UICONTROL Créer une expérience]** pour configurer votre expérience de contenu. [Voici comment procéder](../content-management/content-experiment.md)

   ![](assets/exd-uc-create-experiment.png){width="90%"}

1. Dans la page de résumé de la campagne, sélectionnez une configuration basée sur du code, puis cliquez sur **[!UICONTROL Modifier le contenu]**.

   ![](assets/exd-uc-edit-cbe-content.png){width="90%"}

1. Dans la fenêtre d’édition du contenu, pour commencer à personnaliser **Traitement A**, cliquez sur **[!UICONTROL Modifier le code]**.

   ![](assets/exd-uc-experiment-treatment-a.png){width="90%"}

1. Dans l’[éditeur de code](../code-based/create-code-based.md#edit-code), sélectionnez **[!UICONTROL Politique de décision]**, cliquez sur **[!UICONTROL Ajouter une politique de décision]** et renseignez les détails de la décision. [En savoir plus](create-decision.md#add)

   ![](assets/decision-code-based-create.png){width="90%"}

1. Dans la section **[!UICONTROL Séquence de stratégie]**, cliquez sur le bouton **[!UICONTROL Ajouter]** et choisissez **[!UICONTROL Stratégie de sélection]**. [En savoir plus](create-decision.md#select)

   ![](assets/decision-code-based-strategy-sequence.png){width="80%"}

   >[!NOTE]
   >
   >Vous pouvez également sélectionner **[!UICONTROL Élément de décision]** pour ajouter des éléments uniques sans avoir à exécuter une stratégie de sélection. La priorité définie pour chaque élément s’applique.

1. Sélectionnez la première stratégie que vous avez créée.

   ![](assets/exd-uc-experiment-strategy-priority.png){width="90%"}

1. Enregistrez vos modifications et cliquez sur **[!UICONTROL Créer]**. La nouvelle décision est ajoutée sous **[!UICONTROL Politique de décision]**.

1. Cliquez sur le bouton **[!UICONTROL Insérer une politique]**. Le code correspondant à la politique de décision est ajouté. Ajoutez ensuite tous les attributs souhaités au code, y compris les attributs de profil. [En savoir plus](create-decision.md#use-decision-policy).

   ![](assets/exd-uc-experiment-insert-policy.png){width="90%"}

1. Enregistrez vos modifications.

1. Revenez à la fenêtre d’édition du contenu, sélectionnez le bouton + pour ajouter **Traitement B**, sélectionnez-le et cliquez sur **[!UICONTROL Modifier le code]**.

   ![](assets/exd-uc-experiment-treatment-b.png){width="90%"}

1. Répétez les étapes ci-dessus pour créer une autre politique de décision et sélectionnez la deuxième stratégie de sélection que vous avez créée. <!--Do you need to create exactly the same content to compare only the ranking method?-->

1. Enregistrez vos modifications et [ publiez votre campagne d’expérience basée sur le code ](../code-based/publish-code-based.md).

Après avoir exécuté votre expérience, suivez les performances de vos traitements de campagne avec le [rapport de campagne d’expérimentation](../reports/campaign-global-report-cja-experimentation.md).<!-- and [report on decisioning](cja-reporting.md).--> Vous pouvez ensuite interpréter les résultats de votre expérience. [Voici comment procéder](../content-management/get-started-experiment.md#interpret-results)

Si le résultat de votre expérience est concluant, vous pouvez envoyer le traitement avec le classement le plus performant à tous vos clients. Vous pouvez également créer une campagne à l’aide de la stratégie de sélection dans laquelle la méthode de classement la plus performante est répliquée.