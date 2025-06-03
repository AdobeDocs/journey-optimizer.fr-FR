---
solution: Journey Optimizer
product: journey optimizer
title: Contrôle d’accès au niveau des objets
description: Découvrez le contrôle d’accès au niveau de l’objet (OLAC) qui vous permet de définir des autorisations pour gérer l’accès aux données d’une sélection d’objets.
feature: Access Management
topic: Administration
role: Admin, Developer, Architect
level: Experienced
keywords: objet, niveau, accès, contrôle, libellés, olac, autorisation
exl-id: 02ccdd95-426c-4b61-9834-7f2dcd5abdbb
source-git-commit: 1a2c6e97fcd30245cff1bf08fd5771ce8bc84ddc
workflow-type: tm+mt
source-wordcount: '480'
ht-degree: 52%

---

# Contrôle d’accès au niveau des objets {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Libellés de gestion des accès"
>abstract="Vous pouvez limiter l’accès à un objet en fonction des libellés d’accès. Cette approche protège les ressources numériques sensibles contre les utilisateurs non autorisés et assure une protection supplémentaire des données personnelles. **Sélectionnez uniquement les libellés pour lesquels vous disposez d’autorisations.**"

Vous pouvez limiter l’accès à un objet en fonction des libellés d’accès. Cette approche protège les ressources numériques sensibles contre les utilisateurs non autorisés et assure une protection supplémentaire des données personnelles.

La fonctionnalité de contrôle d’accès au niveau de l’objet (OLAC) vous permet de définir des autorisations pour gérer l’accès aux données d’une sélection d’objets :

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


## Conditions préalables {#prereq-labels}

Pour pouvoir [créer des libellés](#create-labels), vous devez appartenir à un rôle avec l’autorisation **[!UICONTROL Gérer les libellés d’utilisation]**.

Pour pouvoir [attribuer des libellés](#assign-labels), vous devez appartenir à un rôle avec une autorisation **Gérer**, c’est-à-dire [!DNL Manage journeys], [!DNL Manage Campaigns] ou [!DNL Manage decisions]. Sans cette autorisation, le bouton **[!UICONTROL Gérer l’accès]** sera grisé.

Pour en savoir plus sur les autorisations, consultez [cette section](../administration/permissions.md).

## Créer des libellés {#create-labels}

Les **[!UICONTROL étiquettes]** vous permettent de classer les jeux de données et les champs en fonction des politiques d’utilisation qui s’appliquent à ces données. Les **[!UICONTROL libellés]** peuvent être appliqués à tout moment, ce qui vous offre une certaine flexibilité dans la gestion des données.

Utilisez des libellés pour donner accès aux utilisateurs et appliquer la gouvernance des données et les politiques de consentement. Ces libellés de gouvernance peuvent affecter la consommation en aval.

Vous pouvez créer des libellés dans le produit [!DNL Permissions]. Pour plus d&#39;informations, consultez la documentation de [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html?lang=fr){target="_blank"}.

Vous pouvez également créer des **[!UICONTROL libellés]** directement dans Journey Optimizer. Pour créer un libellé, procédez comme suit :

1. À partir d’un objet Adobe Journey Optimizer, tel qu’un nouvel objet **[!UICONTROL Campaign]**, cliquez sur le bouton **[!UICONTROL Gérer l’accès]**.

   ![Bouton Gérer l’accès dans Adobe Journey Optimizer](assets/olac_1.png)

1. Dans la fenêtre **[!UICONTROL Gérer l’accès]**, cliquez sur **[!UICONTROL Créer une étiquette]**.

   ![](assets/olac_2.png)

1. Configurez votre libellé. Vous devez indiquer les informations suivantes :

   * **[!UICONTROL Nom]**
   * **[!UICONTROL Nom convivial]**
   * **[!UICONTROL Description]**

   ![Champs de configuration des libellés](assets/olac_3.png)

1. Cliquez sur **[!UICONTROL Créer]** pour enregistrer votre **[!UICONTROL Étiquette]**.

Votre nouvelle **[!UICONTROL Étiquette]** est désormais disponible dans la liste. Si nécessaire, vous pouvez la modifier dans le produit [!DNL Permissions].

## Attribuer des étiquettes {#assign-labels}

Pour attribuer des étiquettes d’utilisation des données personnalisées ou de base à vos objets Journey Optimizer, procédez comme suit :

1. À partir d’un objet Adobe Journey Optimizer, tel qu’un nouvel objet **[!UICONTROL Campaign]**, cliquez sur le bouton **[!UICONTROL Gérer l’accès]**.

   ![Bouton Gérer l’accès dans Adobe Journey Optimizer](assets/olac_1.png)

1. Dans la fenêtre **[!UICONTROL Gérer l’accès]**, sélectionnez votre ou vos étiquettes d’utilisation des données de base ou personnalisées pour gérer l’accès à cet objet.

   Pour plus d’informations sur les étiquettes d’utilisation des données de base, reportez-vous à [cette page](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=fr){target="_blank"}.

   ![](assets/olac_4.png)

1. Cliquez sur **[!UICONTROL Enregistrer]** pour appliquer cette restriction d’étiquette.

Pour accéder à cet objet, les utilisateurs doivent disposer du **[!UICONTROL libellé]** spécifique inclus dans leurs **[!UICONTROL rôles]**. Par exemple, un utilisateur avec le libellé C1 n’aura accès qu’aux objets libellés C1 ou non libellés.

Pour plus d’informations sur la manière d’attribuer un **[!UICONTROL libellé]** à un **[!UICONTROL rôle]**, consultez [cette page](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html?lang=fr#manage-labels-for-a-role){target="_blank"}.
