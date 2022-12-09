---
product: experience platform
solution: Experience Platform
title: Création de modèles AI
description: Découvrez comment créer des modèles AI pour classer les offres
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: 3188bc97b8103d2a01101a23d8c242a3e2924f76
workflow-type: tm+mt
source-wordcount: '287'
ht-degree: 0%

---

# Création de modèles AI {#ai-rankings}

[!DNL Journey Optimizer] permet de créer des **Modèles AI** pour classer les offres en fonction des objectifs de votre entreprise.

>[!CAUTION]
>
>Pour créer, modifier ou supprimer des modèles AI, vous devez disposer de la variable **Gestion des stratégies de classement** autorisation. [En savoir plus](../../administration/high-low-permissions.md#manage-ranking-strategies)

## Création d’un modèle AI {#create-ranking-strategy}

Pour créer un modèle d’IA, procédez comme suit :

1. Dans le **[!UICONTROL Components]** , accédez au **[!UICONTROL Ranking]** , puis sélectionnez **[!UICONTROL AI models]**.

   ![](../assets/ai-ranking-list.png)

   Tous les modèles d’IA créés jusqu’à présent sont répertoriés.

1. Cliquez sur le bouton **[!UICONTROL Create AI model]** bouton .

1. Indiquez un nom unique et une description pour le modèle AI, puis sélectionnez le type de modèle AI à créer :

   * **[!UICONTROL Auto-optimization]** optimise les offres en fonction des performances des offres antérieures. [En savoir plus](auto-optimization-model.md)
   * **[!UICONTROL Personalized]** optimise et personnalise les offres en fonction des segments et des performances des offres. [En savoir plus](personalized-optimization-model.md)

   ![](../assets/ai-ranking-fields.png)

   >[!NOTE]
   >
   >Le **[!UICONTROL Optimization metric]** Cette section fournit des informations sur l’événement de conversion utilisé par le modèle AI pour calculer le classement des offres.
   >
   >[!DNL Journey Optimizer] classer les offres en fonction de la variable **taux de conversion** (Taux de conversion = Nombre total d’événements de conversion / Nombre total d’événements d’impression). Le taux de conversion est calculé à l’aide de deux types de mesures :
   >* **Événements d’impression** (offres affichées)
   >* **Événements de conversion** (offres qui génèrent des clics par email ou web).

   >
   >Ces événements sont automatiquement capturés à l’aide du SDK Web ou du SDK Mobile fourni. En savoir plus à ce sujet dans [Présentation du SDK Web d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=en).

1. Sélectionnez le ou les jeux de données dans lesquels les événements de conversion et d’impression sont collectés. Découvrez comment créer ce jeu de données dans [cette section](#create-dataset). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >Seuls les jeux de données créés à partir de schémas associés à la variable **[!UICONTROL Experience Event - Proposition Interactions]** Le groupe de champs (précédemment appelé mixin) s’affiche dans la liste déroulante.

1. Si vous créez une **[!UICONTROL Personalization]** Modèle AI, sélectionnez le ou les segments à utiliser pour entraîner le modèle AI.

   ![](../assets/ai-ranking-segments.png)

   >[!NOTE]
   >
   >Vous pouvez sélectionner jusqu’à 5 segments.

1. Enregistrez et activez le modèle AI.

   ![](../assets/ai-ranking-save-activate.png)
