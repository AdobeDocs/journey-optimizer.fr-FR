---
solution: Journey Optimizer
product: Journey Optimizer
title: Créer un jeu de données pour collecter des événements
description: Découvrez comment créer un jeu de données pour collecter des événements.
feature: Ranking, Datasets, Decisioning
role: Developer
level: Experienced
hide: true
exl-id: 96c1326f-be40-4738-8997-a67dc14872bb
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/U-4AWTYWPOzBhtT3gxE6ORtMI8jNKOZGns-0P3t7-lE
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2: id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
feature_v2: id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
subfeature_v2: id: a7a194a0-75e2-4913-8a83-14714fbf68e6id: eb547372-2a95-4d13-b0fd-f720c9895880
source-git-commit: ee394c77b226dd35a9c27f4a02e3b8d7a997ccbd
workflow-type: tm+mt
source-wordcount: 296
ht-degree: 91%

---

# Créer un jeu de données pour collecter des événements {#create-dataset}

>[!BEGINSHADEBOX]

**Sur cette page :** Créez le schéma d’événement d’expérience et le jeu de données nécessaires pour capturer les interactions de proposition, afin de pouvoir alimenter vos modèles de classement IA en commentaires sur la prise de décision.

>[!ENDSHADEBOX]

Pour collecter des événements d’expérience, vous devez d’abord créer un jeu de données où ces événements seront envoyés.

Commencez par créer le schéma qui sera utilisé dans votre jeu de données :

1. Dans le menu **[!UICONTROL Gestion des données]**, sélectionnez **[!UICONTROL Schéma]**.

1. Cliquez sur **[!UICONTROL Créer un schéma]**, dans le coin supérieur droit, sélectionnez **[!UICONTROL Événement d’expérience]** et cliquez sur **Suivant**.

   ![](../../offers/assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >Découvrez les schémas XDM et les groupes de champs dans la [documentation de présentation du système XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target="_blank"}.

1. Saisissez le nom et la description de votre schéma, puis cliquez sur **Terminer**.
   ![](../../offers/assets/ai-ranking-xdm-event-2.png)

1. Dans la section **[!UICONTROL Groupes de champs]** à gauche, sélectionnez **[!UICONTROL Ajouter]**.

   ![](../../offers/assets/ai-ranking-fields-groups.png)

1. Dans le champ **[!UICONTROL Rechercher]**, saisissez « interaction de proposition ».

1. Sélectionnez le groupe de champs **[!UICONTROL Événement d’expérience - Interactions de proposition]** et cliquez sur **[!UICONTROL Ajouter des groupes de champs]**.

   ![](../../offers/assets/ai-ranking-add-field-group.png)

   >[!CAUTION]
   >
   >Le schéma qui sera utilisé dans votre jeu de données doit être associé au groupe de champs **[!UICONTROL Événement d&#39;expérience - Interactions de proposition]**. Sinon, vous ne pourrez pas l&#39;utiliser dans votre modèle d’IA.

1. Enregistrez le schéma.

>[!NOTE]
>
>Pour plus d’informations sur la création de schémas, consultez la section [Principes de base de la composition de schémas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=fr#understanding-schemas){target="_blank"}.

Vous êtes maintenant en mesure de créer un jeu de données à l’aide de ce schéma. Pour ce faire, procédez comme suit :

1. Dans le menu **[!UICONTROL Gestion des données]**, sélectionnez **[!UICONTROL Jeux de données]** et accédez à l’onglet **[!UICONTROL Parcourir]**.

1. Cliquez sur **[!UICONTROL Créer un jeu de données]** et sélectionnez **[!UICONTROL Créer un jeu de données à partir d’un schéma]**.

   ![](../../offers/assets/ai-ranking-create-dataset-from-schema.png)

1. Sélectionnez le schéma que vous venez de créer dans la liste et cliquez sur **[!UICONTROL Suivant]**.

1. Attribuez un nom unique au jeu de données dans le champ **[!UICONTROL Nom]** et cliquez sur **[!UICONTROL Terminer]**.

   ![](../../offers/assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>Ce jeu de données peut maintenant être sélectionné pour collecter des données dʼévénement lors de la création dʼun [modèle d’IA](../ranking/create-ai-models.md).
