---
title: Configuration des rapports
description: Découvrez comment configurer la source de données de création de rapports
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: 711fdf1dce0688d2e21d405a4e3e8777612b2f3b
workflow-type: tm+mt
source-wordcount: '593'
ht-degree: 5%

---

# Configuration des rapports {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Configuration de jeux de données pour la création de rapports"
>abstract="La configuration des rapports vous permet de définir une connexion à un système afin de récupérer des informations personnalisées supplémentaires à utiliser dans vos rapports. Elle doit être effectuée par un utilisateur technique."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Sélectionner un jeu de données"
>abstract="Vous pouvez uniquement sélectionner un jeu de données de type événement qui doit contenir au moins l’un des groupes de champs pris en charge : experienceevent-web, experienceevent-application, experienceevent-commerce."

La configuration de la source de données de rapports vous permet de définir une connexion à un système afin de récupérer des informations supplémentaires qui seront utilisées dans vos rapports.

>[!NOTE]
>
>La configuration de la source de données doit être effectuée par un utilisateur technique. <!--Rights?-->

Pour cette configuration, vous devez ajouter un ou plusieurs jeux de données contenant les attributs que vous souhaitez utiliser pour vos rapports. Pour ce faire, suivez les étapes ci-après.

>[!CAUTION]
>
>Avant de pouvoir ajouter un jeu de données à la configuration de création de rapports, vous devez le créer. Découvrez comment dans la section [Documentation Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#create){target=&quot;_blank&quot;}.
>
>Vous pouvez uniquement ajouter des jeux de données de type événement, qui doivent contenir au moins l’un des jeux de données pris en charge. [groupes de champs](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;} : **experienceevent-web**, **experienceevent-application**, **experienceevent-commerce**.

<!--
➡️ [Discover this feature in video](#video)
-->

Par exemple, si vous souhaitez connaître l’impact d’une campagne par e-mail sur les données commerciales telles que les achats ou les commandes, vous devez créer un jeu de données d’événement d’expérience avec la variable **experienceevent-commerce** groupe de champs. De même, si vous souhaitez générer des rapports sur les interactions mobiles, vous devez créer un jeu de données d’événement d’expérience avec la variable **experienceevent-application** groupe de champs. <!--If you want to report on web interactions then you need to include the web field group.--> Vous pouvez ajouter ces groupes de champs à un ou plusieurs schémas qui seront utilisés dans un jeu de données ou dans différents jeux de données.

>[!NOTE]
>
>En savoir plus sur les schémas XDM et les groupes de champs dans la section [Présentation de la documentation du système XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target=&quot;_blank&quot;}.

1. Dans la **[!UICONTROL ADMINISTRATION]** menu, sélectionnez **[!UICONTROL Configurations]**. Dans le  **[!UICONTROL Reporting]** , cliquez sur **[!UICONTROL Gérer]**.

   ![](assets/reporting-config-menu.png)

   La liste des jeux de données déjà ajoutés s’affiche.

1. Dans la **[!UICONTROL Jeu de données]** , cliquez sur **[!UICONTROL Ajouter un jeu de données]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >Si vous sélectionnez la variable **[!UICONTROL Jeu de données système]** , seuls les jeux de données créés par le système s’affichent. Vous ne pourrez pas ajouter d’autres jeux de données.

1. Dans la **[!UICONTROL Jeu de données]** , sélectionnez le jeu de données à utiliser pour vos rapports.

   >[!CAUTION]
   >
   >Vous pouvez uniquement sélectionner un jeu de données de type événement, qui doit contenir au moins l’un des jeux de données pris en charge. [groupes de champs](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;} : **experienceevent-web**, **experienceevent-application**, **experienceevent-commerce**. Si vous sélectionnez un jeu de données ne correspondant pas à ces critères, vous ne pourrez pas enregistrer vos modifications.

   ![](assets/reporting-config-datasets.png)

   En savoir plus sur les jeux de données dans la section [Documentation Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=fr){target=&quot;_blank&quot;}.

1. Dans la **[!UICONTROL Identifiant de profil]** , sélectionnez l’attribut de champ de jeu de données qui sera utilisé pour identifier chaque profil dans vos rapports.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >Seuls les identifiants disponibles pour la création de rapports s’affichent.

1. Le **[!UICONTROL Utilisation de l’espace de noms d’identifiant Principal]** est activée par défaut. Si la variable **[!UICONTROL Identifiant de profil]** is **[!UICONTROL Mappage d’identités]**, vous pouvez désactiver cette option et choisir un autre espace de noms dans la liste déroulante qui s’affiche.

   ![](assets/reporting-config-namespace.png)

   En savoir plus sur les espaces de noms dans [Documentation Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=fr){target=&quot;_blank&quot;}.

1. Enregistrez vos modifications pour ajouter le jeu de données sélectionné à la liste de configuration des rapports.

   >[!CAUTION]
   >
   >Si vous avez sélectionné un jeu de données qui n’est pas de type événement, vous ne pourrez pas continuer.

Lors de la création des rapports de vos diffusions, vous pouvez désormais utiliser les données de ce jeu de données pour récupérer des informations personnalisées supplémentaires et optimiser vos rapports. [En savoir plus](content-experiment.md#objectives-global)

>[!NOTE]
>
>Si vous ajoutez plusieurs jeux de données, toutes les données de tous les jeux de données seront disponibles pour la création de rapports.


<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
