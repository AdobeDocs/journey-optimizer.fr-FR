---
solution: Journey Optimizer
product: journey optimizer
title: Configuration des rapports Journey Optimizer pour les expérimentations
description: Découvrez comment configurer la source de données de création de rapports
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '663'
ht-degree: 0%

---

# Configuration des rapports pour l’expérimentation {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Configuration de jeux de données pour la création de rapports"
>abstract="La configuration des rapports vous permet de récupérer des mesures supplémentaires qui seront utilisées dans l’onglet Objectifs de vos rapports de campagne. Elle doit être effectuée par un utilisateur technique."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Sélection d’un jeu de données"
>abstract="Vous pouvez uniquement sélectionner un jeu de données de type événement, qui doit contenir au moins l’un des groupes de champs pris en charge : Détails de l’application, Détails du commerce, Détails Web."

<!--The reporting data source configuration allows you to define a connection to a system in order to retrieve additional information that will be used in your reports.-->

La configuration de la source de données de rapports vous permet de récupérer des mesures supplémentaires qui seront utilisées dans la variable **[!UICONTROL Objectives]** de vos rapports d’opération. [En savoir plus](content-experiment.md#objectives-global)

>[!NOTE]
>
>La configuration du reporting doit être effectuée par un utilisateur technique. <!--Rights?-->

Pour cette configuration, vous devez ajouter un ou plusieurs jeux de données contenant les éléments supplémentaires que vous souhaitez utiliser pour vos rapports. Pour ce faire, procédez comme suit : [below](#add-datasets).

<!--
➡️ [Discover this feature in video](#video)
-->

## Conditions préalables


Avant de pouvoir ajouter un jeu de données à la configuration de création de rapports, vous devez le créer. Découvrez comment dans la section [Documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=en#create){target=&quot;_blank&quot;}.

* Vous pouvez uniquement ajouter des jeux de données de type événement.

* Ces jeux de données doivent contenir au moins l’une des variables suivantes : [groupes de champs](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;} : **Détails de l’application**, **Détails du commerce**, **Détails web**.

   >[!NOTE]
   >
   >Seuls ces groupes de champs sont actuellement pris en charge.

   Par exemple, si vous souhaitez connaître l’impact d’une campagne par e-mail sur les données commerciales telles que les achats ou les commandes, vous devez créer un jeu de données d’événement d’expérience avec la variable **Détails du commerce** groupe de champs.

   De même, si vous souhaitez générer des rapports sur les interactions mobiles, vous devez créer un jeu de données d’événement d’expérience avec la variable **Détails de l’application** groupe de champs.

   Les mesures correspondant à chaque groupe de champs sont répertoriées. [here](#objective-list).

* Vous pouvez ajouter ces groupes de champs à un ou plusieurs schémas qui seront utilisés dans un ou plusieurs jeux de données.

>[!NOTE]
>
>En savoir plus sur les schémas XDM et les groupes de champs dans la section [Présentation de la documentation du système XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=en){target=&quot;_blank&quot;}.

## Objectifs correspondant à chaque groupe de champs {#objective-list}

Le tableau ci-dessous indique les mesures qui seront ajoutées au **[!UICONTROL Objectives]** de vos rapports de campagne pour chaque groupe de champs.

| Groupe de champs | Objectifs |
|--- |--- |
| Détails du commerce | Prix total<br>Montant du paiement<br>Passages en caisse (uniques)<br>Ajout de listes de produits (uniques)<br>(Unique) La liste des produits s’ouvre<br>Suppression de la liste de produits (unique)<br>Vues de liste de produits (uniques)<br>Consultations de produit (uniques)<br>Achats (uniques)<br>(Unique) Enregistrer pour plus tard<br>Prix du produit total<br>Quantité de produit |
| Détails de l’application | Lancements d’application (uniques)<br>Premiers lancements d’applications<br>(Unique) Installations de l’application<br>Mises à niveau d’application (uniques) |
| Détails web | Pages vues (uniques) |

## Ajout de jeux de données {#add-datasets}

1. Dans la **[!UICONTROL ADMINISTRATION]** menu, sélectionnez **[!UICONTROL Configurations]**. Dans le  **[!UICONTROL Reporting]** , cliquez sur **[!UICONTROL Manage]**.

   ![](assets/reporting-config-menu.png)

   La liste des jeux de données déjà ajoutés s’affiche.

1. Dans la **[!UICONTROL Dataset]** , cliquez sur **[!UICONTROL Add dataset]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >Si vous sélectionnez la variable **[!UICONTROL System dataset]** , seuls les jeux de données créés par le système s’affichent. Vous ne pourrez pas ajouter d’autres jeux de données.

1. Dans la **[!UICONTROL Dataset]** , sélectionnez le jeu de données à utiliser pour vos rapports.

   >[!CAUTION]
   >
   >Vous pouvez uniquement sélectionner un jeu de données de type événement, qui doit contenir au moins l’un des jeux de données pris en charge. [groupes de champs](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;} : **Détails de l’application**, **Détails du commerce**, **Détails web**. Si vous sélectionnez un jeu de données ne correspondant pas à ces critères, vous ne pourrez pas enregistrer vos modifications.

   ![](assets/reporting-config-datasets.png)

   En savoir plus sur les jeux de données dans la section [Documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html){target=&quot;_blank&quot;}.

1. Dans la **[!UICONTROL Profile ID]** , sélectionnez l’attribut de champ de jeu de données qui sera utilisé pour identifier chaque profil dans vos rapports.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >Seuls les identifiants disponibles pour la création de rapports s’affichent.

1. Le **[!UICONTROL Use Primary ID namespace]** est activée par défaut. Si la variable **[!UICONTROL Profile ID]** is **[!UICONTROL Identity Map]**, vous pouvez désactiver cette option et choisir un autre espace de noms dans la liste déroulante qui s’affiche.

   ![](assets/reporting-config-namespace.png)

   En savoir plus sur les espaces de noms dans [Documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html){target=&quot;_blank&quot;}.

1. Enregistrez vos modifications pour ajouter le jeu de données sélectionné à la liste de configuration des rapports.

   >[!CAUTION]
   >
   >Si vous avez sélectionné un jeu de données qui n’est pas de type événement, vous ne pourrez pas continuer.

Lors de la création des rapports de campagne, vous pouvez désormais voir les mesures correspondant aux groupes de champs utilisés dans les jeux de données que vous avez ajoutés. Accédez au **[!UICONTROL Objectives]** et sélectionnez les mesures de votre choix pour affiner davantage vos rapports. [En savoir plus](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>Si vous ajoutez plusieurs jeux de données, toutes les données de tous les jeux de données seront disponibles pour la création de rapports.

<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
