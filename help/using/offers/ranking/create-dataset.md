---
product: experience platform
solution: Experience Platform
title: Création d’un jeu de données pour la collecte d’événements
description: Découvrez comment créer un jeu de données pour collecter des événements
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 5abcef4ff057bb351abaafbf4dcb99e1ab61c6a9
workflow-type: tm+mt
source-wordcount: '221'
ht-degree: 0%

---

# Création d’un jeu de données pour la collecte d’événements {#create-dataset}

Avant de créer un modèle d’IA, vous devez créer un jeu de données dans lequel les événements de conversion seront collectés. Commencez par créer le schéma qui sera utilisé dans votre jeu de données :

1. Dans la **[!UICONTROL Data Management]** menu, sélectionnez **[!UICONTROL Schema]**, accédez au **[!UICONTROL Browse]** et cliquez sur **[!UICONTROL Create schema]**.

   ![](../assets/ai-ranking-create-schema.png)

1. Choisir **[!UICONTROL XDM ExperienceEvent]**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >En savoir plus sur les schémas XDM et les groupes de champs dans la section [Présentation de la documentation du système XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=en){target=&quot;_blank&quot;}.

1. Dans la **[!UICONTROL Field groups]** , sélectionnez **[!UICONTROL Add]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. Dans le **[!UICONTROL Search]** , saisissez &quot;interaction de proposition&quot; et sélectionnez l’option **[!UICONTROL Experience Event - Proposition Interactions]** groupe de champs.

   ![](../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >Le schéma qui sera utilisé dans votre jeu de données doit comporter la variable **[!UICONTROL Experience Event - Proposition Interactions]** groupe de champs qui lui est associé. Sinon, vous ne pourrez pas l’utiliser dans votre stratégie de classement.

1. Cliquez sur **[!UICONTROL Add field groups]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >Le groupe de champs était auparavant appelé mixin.

1. Saisissez un nom et enregistrez le schéma.

>[!NOTE]
>
>En savoir plus sur la création de schémas dans [Principes de base de la composition des schémas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=en#understanding-schemas){target=&quot;_blank&quot;}.

Vous êtes maintenant prêt à créer un jeu de données à l’aide de ce schéma. Pour ce faire, procédez comme suit :

1. Dans la **[!UICONTROL Data Management]** menu, sélectionnez **[!UICONTROL Datasets]**, accédez au **[!UICONTROL Browse]** et cliquez sur **[!UICONTROL Create dataset]**.

   ![](../assets/ai-ranking-create-dataset.png)

1. Sélectionner **[!UICONTROL Create dataset from schema]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Sélectionnez le schéma que vous venez de créer dans la liste.

   ![](../assets/ai-ranking-dataset-select-schema.png)

1. Cliquez sur **[!UICONTROL Next]**.

1. Attribuez un nom unique au jeu de données dans la variable **[!UICONTROL Name]** champ et clic **[!UICONTROL Finish]**.

   ![](../assets/ai-ranking-dataset-name.png)

Le jeu de données est maintenant prêt à être sélectionné pour collecter des données d’événement lors de la [création d’une stratégie de classement](#create-ranking-strategy).
