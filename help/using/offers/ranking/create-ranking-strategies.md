---
product: experience platform
solution: Experience Platform
title: Créer des modèles d’IA
description: Découvrez comment créer des modèles AI pour classer les offres.
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: 12b01cb9de84399e5ede987866609acc10b64c5f
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 39%

---

# Créer des modèles d’IA {#ai-rankings}

[!DNL Journey Optimizer] permet de créer des **modèles &#39;’IA** pour classer les offres en fonction des objectifs de votre entreprise.

>[!CAUTION]
>
>Pour créer, modifier ou supprimer des modèles d&#39;IA, vous devez disposer de la permission **Gestion des stratégies de classement**. [En savoir plus](../../administration/high-low-permissions.md#manage-ranking-strategies)

## Création d’un modèle AI {#create-ranking-strategy}

Pour créer un modèle d’IA, procédez comme suit :

1. Dans le **[!UICONTROL Composants]** , accédez au **[!UICONTROL Classement]** , puis sélectionnez **[!UICONTROL Modèles AI]**.

   ![](../assets/ai-ranking-list.png)

   Tous les modèles d’IA créés jusqu’à présent sont répertoriés.

1. Cliquez sur le bouton **[!UICONTROL Création d’un modèle AI]** bouton .

1. Spécifiez un nom unique et une description pour le modèle AI.

   <!--* **[!UICONTROL Auto-optimization]** optimizes offers based on past offer performance. [Learn more](auto-optimization-model.md)
    * **[!UICONTROL Personalized]** optimizes and personalizes offers based on segments and offer performance. [Learn more](personalized-optimization-model.md)-->

   ![](../assets/ai-ranking-fields.png)

   >[!NOTE]
   >
   >Le **[!UICONTROL Mesure d’optimisation]** Cette section fournit des informations sur l’événement de conversion utilisé par le modèle AI pour calculer le classement des offres.
   >
   >[!DNL Journey Optimizer] classer les offres en fonction de la variable **taux de conversion** (Taux de conversion = Nombre total d’événements de conversion / Nombre total d’événements d’impression). Le taux de conversion est calculé à l’aide de deux types de mesures :
   >* **Événements d’impression** (offres affichées)
   >* **Événements de conversion** (offres qui génèrent des clics par email ou web).

   >
   >Ces événements sont automatiquement capturés à l’aide du SDK Web ou du SDK Mobile fourni. Pour en savoir plus à ce sujet, consultez la [présentation du SDK web Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=fr).

1. Sélectionnez le ou les jeux de données dans lesquels les événements de conversion et d’impression sont collectés. Découvrez comment créer un jeu de données dans [cette section](#create-dataset). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >Seuls les jeux de données créés à partir de schémas associés au groupe de champs **[!UICONTROL Événement d&#39;expérience - Interactions de propositions]** (précédemment appelé « mixin ») s&#39;affichent dans la liste déroulante.

<!--1. If you are creating a **[!UICONTROL Personalization]** AI model, select the segment(s) to use to train the AI model.

    ![](../assets/ai-ranking-segments.png)

    >[!NOTE]
    >
    >You can select up to 5 segments.-->

1. Enregistrez et activez le modèle AI.

   ![](../assets/ai-ranking-save-activate.png)
