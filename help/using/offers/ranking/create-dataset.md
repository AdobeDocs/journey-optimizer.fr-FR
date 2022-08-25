---
product: experience platform
solution: Experience Platform
title: Créer un jeu de données pour collecter des événements
description: Découvrez comment créer un jeu de données pour collecter des événements.
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
source-git-commit: 5abcef4ff057bb351abaafbf4dcb99e1ab61c6a9
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 86%

---

# Créer un jeu de données pour collecter des événements {#create-dataset}

Avant de créer un modèle d’IA, vous devez créer un jeu de données dans lequel les événements de conversion seront collectés. Commencez par créer le schéma qui sera utilisé dans votre jeu de données :

1. Dans le menu **[!UICONTROL Data Management]**, sélectionnez **[!UICONTROL Schéma]**, accédez à l&#39;onglet **[!UICONTROL Parcourir]** et cliquez sur **[!UICONTROL Créer un schéma]**.

   ![](../assets/ai-ranking-create-schema.png)

1. Sélectionnez **[!UICONTROL XDM ExperienceEvent]**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >En savoir plus sur les schémas XDM et les groupes de champs dans la section [Présentation de la documentation du système XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target=&quot;_blank&quot;}.

1. Dans la **[!UICONTROL Groupes de champs]** , sélectionnez **[!UICONTROL Ajouter]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. Dans le champ **[!UICONTROL Rechercher]**, saisissez « interaction de proposition » et sélectionnez le groupe de champs **[!UICONTROL Événement d&#39;expérience - Interactions de proposition]**.

   ![](../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >Le schéma qui sera utilisé dans votre jeu de données doit être associé au groupe de champs **[!UICONTROL Événement d&#39;expérience - Interactions de proposition]**. Sinon, vous ne pourrez pas l&#39;utiliser dans votre stratégie de classement.

1. Cliquez sur **[!UICONTROL Ajouter des groupes de champs]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >Le groupe de champs était auparavant appelé « mixin ».

1. Saisissez un nom et enregistrez le schéma.

>[!NOTE]
>
>En savoir plus sur la création de schémas dans [Principes de base de la composition des schémas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=fr#understanding-schemas){target=&quot;_blank&quot;}.

Vous êtes maintenant prêt à créer un jeu de données à l&#39;aide de ce schéma. Pour ce faire, procédez comme suit :

1. Dans le menu **[!UICONTROL Data Management]**, sélectionnez **[!UICONTROL Jeux de données]**, accédez à l&#39;onglet **[!UICONTROL Parcourir]** et cliquez sur **[!UICONTROL Créer un jeu de données]**.

   ![](../assets/ai-ranking-create-dataset.png)

1. Sélectionnez **[!UICONTROL Créer un jeu de données à partir d&#39;un schéma]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Sélectionnez le schéma que vous venez de créer dans la liste.

   ![](../assets/ai-ranking-dataset-select-schema.png)

1. Cliquez sur **[!UICONTROL Suivant]**.

1. Attribuez un nom unique au jeu de données dans le champ **[!UICONTROL Nom]** et cliquez sur **[!UICONTROL Terminer]**.

   ![](../assets/ai-ranking-dataset-name.png)

Le jeu de données est maintenant prêt à être sélectionné pour collecter les données dʼévénement lors de la [création dʼune stratégie de classement](#create-ranking-strategy).
