---
title: Contrôle d’accès au niveau de l’objet
description: En savoir plus sur le contrôle d’accès au niveau de l’objet
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 61293a2ad45d30d24e1b38d8a5df81534dc19b40
workflow-type: tm+mt
source-wordcount: '438'
ht-degree: 13%

---

# Contrôle d’accès au niveau de l’objet {#object-level-access}

>[!CONTEXTUALHELP]
>id="ajo_olac_manage_access"
>title="Contrôle d’accès au niveau de l’objet"
>abstract="Si vous appliquez des libellés auxquels vous n’avez pas accès, votre accès à cet objet sera révoqué."

>[!IMPORTANT]
>
>L’utilisation du contrôle d’accès au niveau de l’objet est actuellement limitée à certains clients et sera déployée dans tous les environnements dans une prochaine version.

Le contrôle d&#39;accès au niveau de l&#39;objet (OLAC) permet de définir des autorisations pour gérer l&#39;accès aux données à une sélection d&#39;objets :

* Parcours
* Campagne
* Landing page
* Offres
* Collection d&#39;offres
* Offer decisioning

Son objectif est de protéger les ressources numériques sensibles contre les utilisateurs non autorisés, ce qui permet une protection supplémentaire des données personnelles.

Dans Adobe Journey Optimizer, OLAC vous permet de protéger les données et d’accorder un accès spécifique à des objets spécifiques.

## Créer des étiquettes {#create-assign-labels}

>[!IMPORTANT]
>
>Pour pouvoir créer des libellés, vous devez faire partie d’un rôle avec la fonction **[!UICONTROL Gestion des libellés d’utilisation]** autorisation.

**[!UICONTROL Étiquettes]** vous permettent de classer les jeux de données et les champs en fonction des stratégies d’utilisation qui s’appliquent à ces données. **[!UICONTROL Vous pouvez appliquer les libellés à tout moment, ce qui vous offre une certaine flexibilité quant à la manière dont vous choisissez de gérer les données.]**

Vous pouvez créer des libellés dans le [!DNL Permissions] produit. Pour plus d’informations, consultez [cette page](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/labels.html).

**[!UICONTROL Étiquettes]** peut également être créé directement dans Journey Optimizer :

1. À partir d’un objet Adobe Journey Optimizer, voici une **[!UICONTROL Campagne]**, cliquez sur le bouton **[!UICONTROL Gérer l’accès]** bouton .

   ![](assets/olac_1.png)

1. Dans la **[!UICONTROL Gérer l’accès]** fenêtre, cliquez sur **[!UICONTROL Créer une étiquette]**.

   ![](assets/olac_2.png)

1. Configurez votre libellé, vous devez indiquer les informations suivantes :
   * **[!UICONTROL Nom]**
   * **[!UICONTROL Nom convivial]**
   * **[!UICONTROL Description]**

   ![](assets/olac_3.png)

1. Cliquez sur **[!UICONTROL Créer]** pour enregistrer votre **[!UICONTROL Libellé]**.

Votre **[!UICONTROL Libellé]** est désormais disponible dans la liste. Si nécessaire, vous pouvez le modifier dans la variable [!DNL Permissions] produit.

## Attribution de libellés {#assign-labels}

>[!IMPORTANT]
>
>Pour pouvoir attribuer des étiquettes, vous devez faire partie d’un rôle avec une autorisation Gérer , c’est-à-dire : [!DNL Manage journeys], [!DNL Manage Campaigns] ou [!DNL Manage decisions]. Sans cette autorisation, la variable **[!UICONTROL Gérer l’accès]** sera grisé.

Pour attribuer des libellés d’utilisation des données personnalisés ou de base à vos objets Journey Optimizer :

1. À partir d’un objet Adobe Journey Optimizer, voici une **[!UICONTROL Campagne]**, cliquez sur le bouton **[!UICONTROL Gérer l’accès]** bouton .

   ![](assets/olac_1.png)

1. Dans la **[!UICONTROL Gérer l’accès]** sélectionnez votre ou vos libellés d’utilisation des données de base ou personnalisés pour gérer l’accès à cet objet.

   Pour plus d’informations sur les libellés d’utilisation des données de base, reportez-vous à la section [cette page](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=fr).

   ![](assets/olac_4.png)

1. Cliquez sur **[!UICONTROL Enregistrer]** pour appliquer cette restriction de libellé.

Pour pouvoir accéder à cet objet, les utilisateurs doivent disposer de la variable **[!UICONTROL Libellé]** inclus à **[!UICONTROL Rôles]**.
Par exemple, un utilisateur avec l’étiquette C1 n’aura accès qu’aux objets étiquetés C1 ou non étiquetés.

Pour plus d’informations sur l’affectation **[!UICONTROL Libellé]** à **[!UICONTROL Rôle]**, voir [cette page](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/permissions.html?lang=en#manage-labels-for-a-role).



