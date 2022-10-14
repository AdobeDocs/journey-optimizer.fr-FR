---
title: Configurer des rapports Journey Optimizer pour l’expérimentation
description: Découvrez comment configurer la source de données de création des rapports
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
hide: true
hidefromtoc: true
exl-id: 327a0c45-0805-4f64-9bab-02d67276eff8
source-git-commit: 16c156d715a6b39652191909ca88f90e7f971706
workflow-type: tm+mt
source-wordcount: '727'
ht-degree: 100%

---

# Configurer des rapports pour l’expérimentation {#reporting-configuration}

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_config"
>title="Configurer des jeux de données pour la création de rapports"
>abstract="La configuration des rapports vous permet de récupérer des mesures supplémentaires qui seront utilisées sous l’onglet Objectifs de vos rapports de campagne. Elle doit être effectuée par un utilisateur technique."

>[!CONTEXTUALHELP]
>id="ajo_admin_reporting_dataset"
>title="Sélectionner un jeu de données"
>abstract="Vous pouvez uniquement sélectionner un jeu de données de type événement qui doit contenir au moins l’un des groupes de champs pris en charge : Détails de l’application, Détails du commerce, Détails web."

<!--The reporting data source configuration allows you to define a connection to a system in order to retrieve additional information that will be used in your reports.-->

La configuration de la source de données de rapports vous permet de récupérer des mesures supplémentaires qui seront utilisées sous l’onglet **[!UICONTROL Objectifs]** de vos rapports de campagne. [En savoir plus](content-experiment.md#objectives-global)

>[!NOTE]
>
>La configuration des rapports doit être effectuée par un utilisateur technique. <!--Rights?-->

Pour cette configuration, vous devez ajouter un ou plusieurs jeu(x) de données contenant les éléments supplémentaires que vous souhaitez utiliser pour vos rapports. Pour ce faire, suivez les étapes [ci-après](#add-datasets).

<!--
➡️ [Discover this feature in video](#video)
-->

## Conditions préalables


Avant de pouvoir ajouter un jeu de données à la configuration de création de rapports, vous devez le créer. Découvrez comment le faire dans la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/user-guide.html?lang=fr#create){target=&quot;_blank&quot;}.

* Vous pouvez uniquement ajouter des jeux de données de type événement.

* Ces jeux de données doivent contenir au moins l’un des [groupes de champs](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html?lang=fr#field-group){target=&quot;_blank&quot;} suivants : **Détails de l’application**, **Détails du commerce**, **Détails web**.

   >[!NOTE]
   >
   >Seuls ces groupes de champs sont actuellement pris en charge.

   Par exemple, si vous souhaitez connaître l’impact d’une campagne par e-mail sur les données commerciales telles que les achats ou les commandes, vous devez créer un jeu de données d’événement d’expérience avec le groupe de champs **Détails du commerce**.

   De même, si vous souhaitez générer des rapports sur les interactions mobiles, vous devez créer un jeu de données d’événement d’expérience avec le groupe de champ **Détails de l’application**.

   Les mesures correspondant à chaque groupe de champs sont répertoriées [ici](#objective-list).

* Vous pouvez ajouter ces groupes de champs à un ou plusieurs schémas qui seront utilisés dans un ou plusieurs jeux de données.

>[!NOTE]
>
>Pour en savoir plus sur les schémas et les groupes de champs XDM, consultez la [Documentation de présentation du système XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target=&quot;_blank&quot;}.

## Objectifs correspondant à chaque groupe de champs {#objective-list}

Le tableau ci-dessous indique les mesures qui seront ajoutées à l’onglet **[!UICONTROL Objectifs]** de vos rapports de campagne pour chaque groupe de champs.

| Groupe de champs | Objectifs |
|--- |--- |
| Informations commerciales | Prix total<br>Montant du paiement<br>Passages en caisse (uniques)<br>Ajouts de listes de produits (uniques)<br>Ouvertures de listes des produits (uniques)<br>Suppression de la liste des produits (unique)<br>Vues de liste des produits (uniques)<br>Consultations de produit (uniques)<br>Achats (uniques)<br>Enregistrer pour plus tard (unique)<br>Prix total du produit<br>Nombre de produits |
| Détails de l’application | Lancements d’application (uniques)<br>Premiers lancements d’applications<br>Installations de l’application (uniques)<br>Mises à niveau d’application (uniques) |
| Informations web | Pages vues (uniques) |

## Ajouter des jeux de données {#add-datasets}

1. Dans la menu **[!UICONTROL ADMINISTRATION]**, sélectionnez **[!UICONTROL Configurations]**. Dans la section **[!UICONTROL Rapports]**, cliquez sur **[!UICONTROL Gérer]**.

   ![](assets/reporting-config-menu.png)

   La liste des jeux de données déjà ajoutés s’affiche.

1. Sous l’onglet **[!UICONTROL Jeu de données]**, cliquez sur **[!UICONTROL Ajouter un jeu de données]**.

   ![](assets/reporting-config-add.png)

   >[!NOTE]
   >
   >Si vous sélectionnez l’onglet **[!UICONTROL Jeu de données système]**, seuls les jeux de données créés par le système s’affichent. Vous ne pourrez pas ajouter d’autres jeux de données.

1. Dans la liste déroulante de **[!UICONTROL Jeu de données]**, sélectionnez le jeu de données que vous souhaitez utiliser pour vos rapports.

   >[!CAUTION]
   >
   >Vous pouvez uniquement sélectionner un jeu de données de type événement, qui doit contenir au moins l’un des [groupes de champs](https://experienceleague.adobe.com/docs/experience-platform/xdm/tutorials/create-schema-ui.html#field-group){target=&quot;_blank&quot;} pris en charge : **Détails de l’application**, **Détails du commerce**, **Détails web**. Si vous sélectionnez un jeu de données ne correspondant pas à ces critères, vous ne pourrez pas enregistrer vos modifications.

   ![](assets/reporting-config-datasets.png)

   Pour en savoir plus sur les jeux de données, consultez la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/catalog/datasets/overview.html?lang=fr){target=&quot;_blank&quot;}.

1. Dans la liste déroulante des **[!UICONTROL identifiants de profil]**, sélectionnez l’attribut de champ de jeu de données qui sera utilisé pour identifier chaque profil dans vos rapports.

   ![](assets/reporting-config-profile-id.png)

   >[!NOTE]
   >
   >Seuls les identifiants disponibles pour la création de rapports s’affichent.

1. L’option **[!UICONTROL Utiliser l’espace de noms d’identifiant principal]** est activée par défaut. Si l’**[!UICONTROL identifiant de profil]** sélectionné est **[!UICONTROL Mappage d’identités]**, vous pouvez désactiver cette option et choisir un autre espace de noms dans la liste déroulante qui s’affiche.

   ![](assets/reporting-config-namespace.png)

   Pour en savoir plus sur les espaces de noms d’identité, consultez la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/namespaces.html?lang=fr){target=&quot;_blank&quot;}.

1. Enregistrez vos modifications pour ajouter le jeu de données sélectionné à la liste de configuration des rapports.

   >[!CAUTION]
   >
   >Si vous avez sélectionné un jeu de données qui n’est pas de type événement, vous ne pourrez pas continuer.

Lors de la création des rapports de campagne, vous pouvez désormais voir les mesures correspondant aux groupes de champs utilisés dans les jeux de données que vous avez ajoutés. Allez à l’onglet **[!UICONTROL Objectifs]** et sélectionnez les mesures de votre choix pour affiner davantage vos rapports. [En savoir plus](content-experiment.md#objectives-global)

![](assets/reporting-config-objectives.png)

>[!NOTE]
>
>Si vous ajoutez plusieurs jeux de données, toutes les données de tous les jeux de données seront disponibles pour la création de rapports.

<!--
## How-to video {#video}

Understand how to configure Experience Platform reporting data sources.

>[!VIDEO]()
-->
