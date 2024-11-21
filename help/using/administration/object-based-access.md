---
solution: Journey Optimizer
product: journey optimizer
title: Contrôle d’accès au niveau de l’objet
description: Découvrez le contrôle d’accès au niveau de l’objet (OLAC) qui vous permet de définir des autorisations pour gérer l’accès aux données d’une sélection d’objets.
feature: Access Management
topic: Administration
role: Admin, Developer, Architect
level: Experienced
keywords: objet, niveau, accès, contrôle, libellés, olac, autorisation
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
source-git-commit: fbcd5ae83c024d672d608d5f5aefc6a4252ec8c0
workflow-type: tm+mt
source-wordcount: '460'
ht-degree: 60%

---

# Contrôle d’accès au niveau de l’objet {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Libellés de gestion des accès"
>abstract="Vous pouvez limiter l&#39;accès à cette campagne en fonction des libellés d&#39;accès. Pour ajouter une limitation d’accès, cliquez sur le bouton **Gérer l’accès** en haut de cette page. Veillez à sélectionner uniquement les étiquettes pour lesquelles vous disposez des autorisations."

La fonctionnalité de contrôle d&#39;accès au niveau objet (OLAC) permet de définir des autorisations pour gérer l&#39;accès aux données à une sélection d&#39;objets :

* Parcours
* Campagne
* Modèle
* Fragment
* Page de destination
* Offre
* Collection d’offres statique
* Décision d’offres
* Configuration des canaux
* Plan de préchauffage des adresses IP

Son objectif est de protéger les ressources numériques sensibles contre les utilisateurs non autorisés, ce qui permet une protection supplémentaire des données personnelles.

## Conditions préalables {#prereq-labels}

Pour pouvoir [créer des libellés](#create-labels), vous devez faire partie d’un rôle avec l’autorisation **[!UICONTROL Gérer les libellés d’utilisation]**.

Pour pouvoir [attribuer des étiquettes](#assign-labels), vous devez faire partie d’un rôle avec une autorisation **Gérer**, c’est-à-dire [!DNL Manage journeys], [!DNL Manage Campaigns] ou [!DNL Manage decisions]. Sans cette autorisation, le bouton **[!UICONTROL Gérer l&#39;accès]** est grisé.

Pour en savoir plus sur les autorisations, consultez [cette section](../administration/permissions.md).

## Créer des libellés {#create-labels}

Les **[!UICONTROL étiquettes]** vous permettent de classer les jeux de données et les champs en fonction des politiques d’utilisation qui s’appliquent à ces données. Vous pouvez appliquer des **[!UICONTROL étiquettes]** à tout moment, ce qui vous offre une certaine flexibilité quant à la manière dont vous choisissez de gérer les données.

Utilisez des étiquettes pour fournir l’accès aux utilisateurs, ainsi que pour appliquer la gouvernance des données et les stratégies de consentement. Ces étiquettes de gouvernance peuvent affecter la consommation en aval.

Vous pouvez créer des étiquettes dans le produit [!DNL Permissions]. Voir à ce propos [cette page](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html?lang=fr){target="_blank"}.

Vous pouvez également créer des **[!UICONTROL libellés]** directement dans Journey Optimizer. Pour créer un libellé, procédez comme suit :

1. Depuis un objet Adobe Journey Optimizer, ici une nouvelle **[!UICONTROL campagne]**, cliquez sur le bouton **[!UICONTROL Gérer l’accès]**.

   ![](assets/olac_1.png)

1. Dans la fenêtre **[!UICONTROL Gérer l’accès]**, cliquez sur **[!UICONTROL Créer une étiquette]**.

   ![](assets/olac_2.png)

1. Pour configurer votre étiquette, vous devez indiquer les informations suivantes :
   * **[!UICONTROL Nom]**
   * **[!UICONTROL Nom convivial]**
   * **[!UICONTROL Description]**

   ![](assets/olac_3.png)

1. Cliquez sur **[!UICONTROL Créer]** pour enregistrer votre **[!UICONTROL Étiquette]**.

Votre nouvelle **[!UICONTROL Étiquette]** est désormais disponible dans la liste. Si nécessaire, vous pouvez la modifier dans le produit [!DNL Permissions].

## Attribuer des étiquettes {#assign-labels}

Pour attribuer des étiquettes d’utilisation des données personnalisées ou de base à vos objets Journey Optimizer, procédez comme suit :

1. Depuis un objet Adobe Journey Optimizer, ici une nouvelle **[!UICONTROL campagne]**, cliquez sur le bouton **[!UICONTROL Gérer l’accès]**.

   ![](assets/olac_1.png)

1. Dans la fenêtre **[!UICONTROL Gérer l’accès]**, sélectionnez votre ou vos étiquettes d’utilisation des données de base ou personnalisées pour gérer l’accès à cet objet.

   Pour plus d&#39;informations sur les libellés d&#39;utilisation des données de base, consultez [cette page](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=fr){target="_blank"}.

   ![](assets/olac_4.png)

1. Cliquez sur **[!UICONTROL Enregistrer]** pour appliquer cette restriction d’étiquette.

Pour pouvoir accéder à cet objet, les utilisateurs doivent disposer de l’**[!UICONTROL étiquette]** spécifique incluse dans leurs **[!UICONTROL rôles]**.
Par exemple, un utilisateur avec l’étiquette C1 n’aura accès qu’aux objets étiquetés C1 ou non étiquetés.

Pour plus d&#39;informations sur l&#39;affectation de **[!UICONTROL Libellé]** à un **[!UICONTROL Rôle]**, consultez [cette page](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html?lang=fr#manage-labels-for-a-role){target="_blank"}.