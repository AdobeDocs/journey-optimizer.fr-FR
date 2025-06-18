---
solution: Journey Optimizer
product: journey optimizer
title: Contrôle d’accès basé sur attribut
description: Le contrôle d’accès basé sur les attributs (ABAC) permet de définir des autorisations pour gérer l’accès aux données pour des équipes ou des groupes d’utilisateurs et d’utilisatrices spécifiques.
feature: Access Management
topic: Administration
role: Admin,Leader
level: Intermediate
keywords: abac, attribut, autorisations, données, accès, sensible, ressources
exl-id: 162b0848-313a-447e-9237-5a6dbc8102c6
source-git-commit: 25b1e6050e0cec3ae166532f47626d99ed68fe80
workflow-type: tm+mt
source-wordcount: '1006'
ht-degree: 43%

---

# Contrôle d’accès basé sur les attributs {#attribute-based-access}

La fonctionnalité de contrôle d’accès basé sur les attributs vous permet de définir des autorisations pour gérer l’accès aux données pour des équipes ou des groupes d’utilisateurs spécifiques. Son objectif est de protéger les ressources numériques sensibles contre les utilisateurs non autorisés, en offrant une protection supplémentaire des données personnelles.

Dans Adobe Journey Optimizer, le contrôle d’accès basé sur les attributs vous permet de protéger les données et d’accorder un accès spécifique à des éléments de champ particuliers, notamment des schémas de modèle de données d’expérience (XDM), des attributs de profil et des audiences.

Pour obtenir une liste plus détaillée de la terminologie utilisée avec le contrôle d’accès basé sur les attributs, consultez la documentation de [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/overview.html?lang=fr){target="_blank"}.

Dans cet exemple, un libellé est ajouté au champ de schéma **Nationalité** pour empêcher des utilisateurs non autorisés de l’utiliser. Pour que cela fonctionne, procédez comme suit :

1. Créez un **[!UICONTROL Rôle]** et attribuez-le à l’aide du **[!UICONTROL Libellé]** correspondant pour que les utilisateurs puissent accéder au champ de schéma et l’utiliser.

1. Attribuez un **[!UICONTROL Libellé]** au champ de schéma **Nationalité** dans Adobe Experience Platform.

1. Utilisez le **[!UICONTROL Champ de schéma]** dans Adobe Journey Optimizer.

Notez que les **[!UICONTROL Rôles]**, **[!UICONTROL Politiques]** et **[!UICONTROL Produits]** sont également accessibles avec l’API de contrôle d’accès basé sur les attributs. Pour plus d’informations, consultez cette [documentation](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/abac-api/overview.html?lang=fr){target="_blank"}.

## Création d’un rôle et attribution de libellés {#assign-role}

>[!IMPORTANT]
>
>>Avant de gérer les autorisations d’un rôle, créez une politique. Pour plus d’informations, consultez la [documentation Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/policies.html?lang=fr){target="_blank"}.

Les **[!UICONTROL rôles]** sont un ensemble d’utilisateurs qui partagent les mêmes autorisations, libellés et sandbox au sein de votre organisation. Chaque utilisateur appartenant à un **[!UICONTROL rôle]** a droit aux applications et services Adobe contenus dans le produit. Vous pouvez également créer vos propres **[!UICONTROL Rôles]** pour affiner l&#39;accès des utilisateurs à certaines fonctionnalités ou objets de l&#39;interface.

Pour accorder aux utilisateurs sélectionnés l’accès au champ **Nationalité** libellé C2, créez un nouveau **[!UICONTROL Rôle]** avec un ensemble spécifique d’utilisateurs et attribuez-leur le libellé C2, ce qui leur permet d’utiliser les détails **Nationalité** dans un Parcours ****.

1. Dans le produit [!DNL Permissions], sélectionnez le **[!UICONTROL rôle]** dans le menu du volet de gauche, puis cliquez sur **[!UICONTROL Créer un rôle]**. Notez que vous pouvez également ajouter un **[!UICONTROL libellé]** aux rôles intégrés.

   ![Créer un nouveau rôle dans le produit Autorisations](assets/role_1.png)

1. Ajoutez un **[!UICONTROL nom]** et une **[!UICONTROL description]** à votre nouveau **[!UICONTROL rôle]**, ici : Rôle démographique limité.

1. Dans la liste déroulante, sélectionnez votre **[!UICONTROL sandbox]**.

   ![](assets/role_2.png)

1. Dans le menu **[!UICONTROL Ressources]**, cliquez sur **[!UICONTROL Adobe Experience Platform]** pour ouvrir les différentes fonctionnalités. Ici, nous sélectionnons **[!UICONTROL Parcours]**.

   ![](assets/role_3.png)

1. Dans la liste déroulante, sélectionnez les **[!UICONTROL autorisations]** liées à la fonctionnalité sélectionnée, telles que **[!UICONTROL Afficher les parcours]** ou **[!UICONTROL Publier les parcours]**.

   ![](assets/role_6.png)

1. Après avoir enregistré votre **[!UICONTROL rôle]** nouvellement créé, cliquez sur **[!UICONTROL Propriétés]** pour configurer plus en détail l’accès à votre rôle.

   ![](assets/role_7.png)

1. Dans l&#39;onglet **[!UICONTROL Utilisateurs]**, cliquez sur **[!UICONTROL Ajouter des utilisateurs]**.

   ![](assets/role_8.png)

1. Dans l’onglet **[!UICONTROL Libellés]**, sélectionnez **[!UICONTROL Ajouter une étiquette]**.

   ![](assets/role_9.png)

1. Sélectionnez les **[!UICONTROL libellés]** que vous souhaitez ajouter à votre rôle, puis cliquez sur **[!UICONTROL Enregistrer]**. Pour cet exemple, accordez le libellé C2 pour que les utilisateurs puissent accéder au champ du schéma précédemment restreint.

   ![Enregistrez la configuration de libellé](assets/role_4.png)

Les utilisateurs du rôle **Rôle démographique limité** ont désormais accès aux objets libellés C2.

## Attribution de libellés à un objet dans Adobe Experience Platform {#assign-label}

>[!WARNING]
>
>Une utilisation incorrecte des libellés peut interrompre l’accès des personnes et déclencher des violations de politique.

**[!UICONTROL Les libellés]** peuvent être utilisés pour attribuer des zones de fonctionnalités spécifiques à l’aide du contrôle d’accès basé sur les attributs. Dans cet exemple, l’accès au champ **Nationalité** est limité. Ce champ est accessible uniquement aux utilisateurs qui disposent du **[!UICONTROL Libellé]** associé à leur **[!UICONTROL Rôle]**.

Notez que vous pouvez également ajouter un **[!UICONTROL libellé]** à un **[!UICONTROL schéma]**, à des **[!UICONTROL jeux de données]** et à des **[!UICONTROL audiences]**.

1. Créez votre **[!UICONTROL schéma]**. Pour plus d’informations, consultez [cette documentation](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=fr){target="_blank"}.

   ![](assets/label_1.png)

1. Dans le **[!UICONTROL schéma]** nouvellement créé, nous ajoutons tout d’abord le groupe de champs **[!UICONTROL Détails démographiques]** contenant le champ **Nationalité**.

   ![](assets/label_2.png)

1. Dans l’onglet **[!UICONTROL Libellés]**, vérifiez le nom du champ restreint, ici **Nationalité**. Ensuite, dans le menu du volet de droite, sélectionnez **[!UICONTROL Modifier les libellés de gouvernance]**.

   ![Modifier les libellés de gouvernance du champ](assets/label_3.png)

1. Sélectionnez le **[!UICONTROL libellé]** correspondant, dans ce cas, le C2 - Les données ne peuvent pas être exportées vers un tiers. Pour obtenir la liste détaillée des libellés disponibles, reportez-vous à [cette page](https://experienceleague.adobe.com/docs/experience-platform/data-governance/labels/reference.html?lang=fr#contract-labels){target="_blank"}.

   ![](assets/label_4.png)

1. Personnalisez davantage votre schéma si nécessaire, puis activez-le. Pour obtenir des instructions détaillées sur la façon d’activer votre schéma, consultez cette [page](https://experienceleague.adobe.com/docs/experience-platform/xdm/ui/resources/schemas.html?lang=fr#profile){target="_blank"}.

Le champ de votre schéma ne sera désormais visible et utilisable que par les utilisateurs qui font partie d’un jeu de rôles avec le libellé C2. En appliquant un **[!UICONTROL Libellé]** à votre **[!UICONTROL Nom du champ]**, le **[!UICONTROL Libellé]** s’applique automatiquement au champ **Nationalité** dans chaque schéma créé.

![](assets/label_5.png)

## Accès aux objets libellés dans Adobe Journey Optimizer {#attribute-access-ajo}

Après avoir libellé le nom du champ **Nationalité** dans un nouveau schéma et rôle, l’impact de cette restriction peut être observé dans Adobe Journey Optimizer. Pour cet exemple :

* L’utilisateur X, ayant accès aux objets libellés C2, crée un parcours avec une condition ciblant le **[!UICONTROL Nom du champ]** restreint.
* L’utilisateur Y, sans accès aux objets libellés C2, tente de publier le parcours.


1. Dans Adobe Journey Optimizer, configurez la **[!UICONTROL source de données]** avec votre nouveau schéma.

   ![Configurer la source de données](assets/journey_1.png)

1. Ajoutez un nouveau **[!UICONTROL Groupe de champs]** de votre **[!UICONTROL Schéma]** nouvelle créé à la **[!UICONTROL Source de données intégrée]**. Vous pouvez également créer une nouvelle **[!UICONTROL source de données]** externe et des **[!UICONTROL Groupes de champs]** associés.

   ![Ajouter un groupe de champs à la source de données](assets/journey_2.png)

1. Après avoir sélectionné le **[!UICONTROL schéma]** précédemment créé, cliquez sur **[!UICONTROL Modifier]** à partir de la catégorie **[!UICONTROL Champs]**.

   ![](assets/journey_3.png)

1. Sélectionnez le **[!UICONTROL Nom du champ]** que vous voulez cibler. Ici, nous sélectionnons le champ **Nationalité** limité.

   ![](assets/journey_4.png)

1. Créez un parcours qui envoie un e-mail aux utilisateurs ayant une nationalité spécifique. Ajoutez un **[!UICONTROL Événement]** et un **[!UICONTROL Condition]**.

   ![](assets/journey_5.png)

1. Sélectionnez le champ **Nationalité** limité pour commencer à créer votre expression.

   ![](assets/journey_6.png)

1. Modifiez votre **[!UICONTROL condition]** pour cibler une population spécifique avec le champ **Nationalité** limité.

   ![](assets/journey_7.png)

1. Personnalisez votre parcours selon vos besoins. Nous ajoutons ici une action **[!UICONTROL E-mail]**.

   ![Ajouter une action e-mail au parcours ](assets/journey_8.png)

Si l’utilisateur Y, sans accès aux objets de libellé C2, doit accéder à ce parcours avec le champ restreint :

* L’utilisateur Y ne pourra pas utiliser le nom de champ restreint, car il ne sera pas visible.
* L’utilisateur Y ne pourra pas modifier l’expression avec le nom de champ restreint en mode avancé. L&#39;erreur suivante s&#39;affiche : `The expression is invalid. Field is no longer available or you do not have enough permission to see it`.
* L’utilisateur Y peut supprimer l’expression.
* L’utilisateur Y ne pourra pas tester le parcours.
* L’utilisateur Y ne pourra pas publier le parcours.