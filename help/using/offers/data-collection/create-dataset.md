---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Créer un jeu de données pour collecter des événements
description: Découvrez comment créer un jeu de données pour collecter des événements.
badge: label="Hérité" type="Informative"
feature: Ranking, Decision Management, Datasets
role: Developer
level: Experienced
exl-id: 99963ef4-0b19-475e-96f4-2eac3f680c6f
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '273'
ht-degree: 100%

---

# Créer un jeu de données pour collecter des événements {#create-dataset}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../../experience-decisioning/gs-experience-decisioning.md)

Pour collecter des événements d’expérience, vous devez d’abord créer un jeu de données où ces événements seront envoyés.

Commencez par créer le schéma qui sera utilisé dans votre jeu de données :

1. Dans le menu **[!UICONTROL Gestion des données]**, sélectionnez **[!UICONTROL Schéma]**.

1. Cliquez sur **[!UICONTROL Créer un schéma]**, dans le coin supérieur droit, sélectionnez **[!UICONTROL Événement d’expérience]** et cliquez sur **Suivant**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >Découvrez les schémas XDM et les groupes de champs dans la [documentation de présentation du système XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target="_blank"}.

1. Saisissez le nom et la description de votre schéma, puis cliquez sur **Terminer**.
   ![](../assets/ai-ranking-xdm-event-2.png)

1. Dans la section **[!UICONTROL Groupes de champs]** à gauche, sélectionnez **[!UICONTROL Ajouter]**.

   ![](../assets/ai-ranking-fields-groups.png)

1. Dans le champ **[!UICONTROL Rechercher]**, saisissez « interaction de proposition ».

1. Sélectionnez le groupe de champs **[!UICONTROL Événement d’expérience - Interactions de proposition]** et cliquez sur **[!UICONTROL Ajouter des groupes de champs]**.

   ![](../assets/ai-ranking-add-field-group.png)

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

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Sélectionnez le schéma que vous venez de créer dans la liste et cliquez sur **[!UICONTROL Suivant]**.

1. Attribuez un nom unique au jeu de données dans le champ **[!UICONTROL Nom]** et cliquez sur **[!UICONTROL Terminer]**.

   ![](../assets/ai-ranking-dataset-name.png)

>[!NOTE]
>
>Ce jeu de données est maintenant prêt à être sélectionné pour collecter les données dʼévénement lors de la [création dʼun modèle d’IA](../ranking/create-ranking-strategies.md).
