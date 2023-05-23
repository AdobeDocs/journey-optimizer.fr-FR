---
product: experience platform
solution: Experience Platform
title: Créer des modèles d’IA
description: Découvrez comment créer des modèles d’IA pour classer les offres.
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: b06b545d377fcd1ffe6ed218badeb94c1bb85ef2
workflow-type: tm+mt
source-wordcount: '401'
ht-degree: 100%

---

# Créer des modèles d’IA {#ai-rankings}

[!DNL Journey Optimizer] permet de créer des **modèles &#39;’IA** pour classer les offres en fonction des objectifs de votre entreprise.

>[!CAUTION]
>
>Pour créer, modifier ou supprimer des modèles d&#39;IA, vous devez disposer de la permission **Gestion des stratégies de classement**. [En savoir plus](../../administration/high-low-permissions.md#manage-ranking-strategies)

## Créer un modèle d’IA {#create-ranking-strategy}

Pour créer un modèle d’IA, procédez comme suit :

1. Créez un jeu de données dans lequel les événements de conversion seront collectés. [Voici comment procéder.](../data-collection/create-dataset.md)

1. Dans le menu **[!UICONTROL Composants]**, accédez à l’onglet **[!UICONTROL Classement]**, puis sélectionnez **[!UICONTROL Modèles d’IA]**.

   ![](../assets/ai-ranking-list.png)

   Tous les modèles d’IA créés jusqu’à présent y sont répertoriés.

1. Cliquez sur le bouton **[!UICONTROL Créer un modèle d’IA]**.

1. Indiquez un nom unique et une description pour le modèle d’IA, puis sélectionnez le type de modèle d’IA à créer :

   * L’option **[!UICONTROL Optimisation automatique]** optimise les offres en fonction des performances des offres antérieures. [En savoir plus](auto-optimization-model.md)
   * L’option **[!UICONTROL Personnalisé]** optimise et personnalise les offres en fonction des segments et des performances des offres. [En savoir plus](personalized-optimization-model.md)

   ![](../assets/ai-ranking-fields.png)

   >[!NOTE]
   >
   >La section **[!UICONTROL Mesure d’optimisation]** fournit des informations sur l’événement de conversion utilisé par le modèle d’IA pour calculer le classement des offres.
   >
   >Offres de classement de [!DNL Journey Optimizer] en fonction du **taux de conversion** (Taux de conversion = Nombre total d’événements de conversion/Nombre total d’événements d’impression). Le taux de conversion est calculé à l’aide de deux types de mesures :
   >* Les **événements d’impression** (les offres qui sont affichées).
   >* Les **événements de conversion** (les offres qui génèrent des clics par e-mail ou sur le Web).
   >
   >Ces événements sont automatiquement capturés à l’aide du SDK Web ou du SDK Mobile fourni. Pour en savoir plus à ce sujet, consultez la [présentation du SDK Web Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=fr).

1. Sélectionnez le ou les jeux de données dans lesquels les événements de conversion et d’impression sont collectés. Découvrez comment créer un jeu de données dans [cette section](../data-collection/create-dataset.md). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >Seuls les jeux de données créés à partir de schémas associés au groupe de champs **[!UICONTROL Événement d&#39;expérience - Interactions de propositions]** (précédemment appelé « mixin ») s&#39;affichent dans la liste déroulante.

1. Si vous créez un modèle d’IA **[!UICONTROL Personnalisation]**, sélectionnez le ou les segments à utiliser pour entraîner le modèle d’IA.

   ![](../assets/ai-ranking-segments.png)

   >[!NOTE]
   >
   >Vous pouvez sélectionner jusqu’à 5 segments.

1. Enregistrez et activez le modèle d’IA.

   ![](../assets/ai-ranking-save-activate.png)

<!--At this point, you must have:

* created the AI model,
* defined which type of event you want to capture - offer displayed (impression) and/or offer clicked (conversion),
* and in which dataset you want to collect the event data.-->

Désormais, chaque fois quʼune offre est présentée et/ou qu’un utilisateur ou une utilisatrice clique dessus, lʼévénement correspondant sera automatiquement capturé par le groupe de champs **[!UICONTROL Événement dʼexpérience - Interactions de proposition]** à lʼaide du [SDK web d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html?lang=fr#what-is-adobe-experience-platform-web-sdk%3F){target="_blank"} ou du SDK mobile.

Pour envoyer des types d’événement (offre affichée ou offre ayant fait l’objet d’un clic), vous devez définir la valeur correcte pour chaque type d’événement dans un événement d’expérience qui est envoyé dans Adobe Experience Platform. [Voici comment procéder.](../data-collection/schema-requirement.md)