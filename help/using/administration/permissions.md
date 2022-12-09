---
solution: Journey Optimizer
product: journey optimizer
title: Gestion des utilisateurs et des profils de produits
description: Découvrez comment gérer les autorisations
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '691'
ht-degree: 0%

---

# Gestion des utilisateurs et des profils de produits {#manage-permissions}

>[!IMPORTANT]
>
> Chaque procédure décrite ci-dessous ne peut être effectuée que par un **[!UICONTROL Product]** ou **[!UICONTROL System]** administrateur. Voir à ce sujet la section [Documentation de la console d’administration](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL Product profiles]** sont des ensembles d’utilisateurs qui partagent les mêmes autorisations et environnements de test au sein de votre organisation.

Le [!DNL Journey Optimizer] vous permet de choisir parmi différents produits prêts à l’emploi. **[!UICONTROL Product profiles]** avec différents niveaux d’autorisations à affecter à vos utilisateurs. Pour plus d’informations sur les **[!UICONTROL Product profiles]**, voir à ce sujet [page](ootb-product-profiles.md).

Chaque utilisateur appartenant à un **[!UICONTROL Product profiles]** est autorisé avec les applications et services Adobe contenus dans le produit.

Vous pouvez également créer les vôtres **[!UICONTROL Product profiles]** si vous souhaitez affiner l’accès de vos utilisateurs à certaines fonctionnalités ou à certains objets de l’interface.

## Attribution d’un profil de produit {#assigning-product-profile}

Vous pouvez choisir d’affecter une **[!UICONTROL Product profile]** à vos utilisateurs.

Vous trouverez la liste de tous les profils de produit d’usine avec des autorisations attribuées dans la section [Profils de produit intégrés](ootb-product-profiles.md) .

Pour affecter une **[!UICONTROL Product profile]**:

1. Dans le [!DNL Admin Console], de la fonction **[!UICONTROL Products]** , sélectionnez la variable **[!UICONTROL Experience Cloud - Platform powered applications]** produit.

1. Sélectionnez une **[!UICONTROL Product profile]**.

   ![](assets/do-not-localize/access_control_2.png)

1. Dans la **[!UICONTROL Users]** , cliquez sur **[!UICONTROL Add user]**.

   ![](assets/do-not-localize/access_control_3.png)

1. Saisissez le nom ou l’adresse électronique de votre utilisateur, puis sélectionnez-le.

   Si l’utilisateur n’a pas été précédemment créé dans la variable [!DNL Admin Console], reportez-vous à la section [Ajout de la documentation sur les utilisateurs](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/do-not-localize/access_control_4.png)

1. Procédez comme ci-dessus pour ajouter d’autres utilisateurs à votre **[!UICONTROL Product profile]**. Cliquez ensuite sur **[!UICONTROL Save]**.

Votre utilisateur doit alors recevoir un email le redirigeant vers votre instance.

Pour plus d’informations sur la gestion des utilisateurs, reportez-vous à la section [Documentation d’Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

Lors de l’accès à l’instance, l’utilisateur voit une vue spécifique en fonction des autorisations attribuées dans la variable **[!UICONTROL Product profile]**. Si l&#39;utilisateur ne dispose pas du droit d&#39;accès à une fonctionnalité, le message suivant s&#39;affiche :

`You don't have permission to access this feature. Permission needed: XX.`

## Modification d’un profil de produit existant {#edit-product-profile}

Pour les paramètres d’usine ou personnalisés **[!UICONTROL Product profiles]**, vous pouvez décider à tout moment d’ajouter ou de supprimer des autorisations.

Dans cet exemple, nous allons ajouter **[!UICONTROL Permissions]** associé au **[!UICONTROL Journeys]** fonctionnalité pour les utilisateurs affectés à la visionneuse de parcours **[!UICONTROL Product profile]**. Les utilisateurs pourront alors publier les parcours.

Notez que si vous modifiez une **[!UICONTROL Product profile]**, cela aura un impact sur chaque utilisateur affecté à cette tâche. **[!UICONTROL Product profile]**.

1. Dans le [!DNL Admin Console], de la fonction **[!UICONTROL Products]** , sélectionnez la variable **[!UICONTROL Experience Cloud - Platform powered applications]** produit.

1. Sélectionnez la visionneuse de parcours **[!UICONTROL Product profile]**.

1. Sélectionnez la **[!UICONTROL Permissions]** .

   Le **[!UICONTROL Permissions]** affiche la liste des fonctionnalités qui s’appliquent au **[!UICONTROL Experience Cloud - Platform powered applications]** produit.

   ![](assets/do-not-localize/access_control_5.png)

1. Sélectionnez la **[!UICONTROL Journeys]** fonctionnalité.

   ![](assets/do-not-localize/access_control_6.png)

1. Dans la **[!UICONTROL Available Permission Items]** sélectionnez les autorisations à attribuer à votre **[!UICONTROL Product profile]** en cliquant sur l’icône plus (+).

   Ici, nous ajoutons le **[!UICONTROL Publish Journeys]** autorisation.

1. Si nécessaire, sous **[!UICONTROL Included Permission Items]**, cliquez sur l’icône X en regard de pour supprimer les autorisations de votre profil de produit.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

Si nécessaire, vous pouvez également créer un profil de produit avec des autorisations spécifiques. Voir à ce sujet la section [Création d’un profil de produit](#create-product-profile).

## Création d’un profil de produit {#create-product-profile}

[!DNL Journey Optimizer] vous permet de créer les vôtres **[!UICONTROL Product profiles]** et attribuez un ensemble d’autorisations et d’environnements de test à vos utilisateurs. Avec **[!UICONTROL Product profiles]**, vous pouvez autoriser ou refuser l’accès à certaines fonctionnalités ou à certains objets de l’interface.

Pour plus d’informations sur la création et la gestion des environnements de test, reportez-vous à la section [Documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html){target=&quot;_blank&quot;}.

Dans cet exemple, nous allons créer un profil de produit nommé **Parcours en lecture seule** où nous accorderons des droits en lecture seule à la fonctionnalité Parcours. Les utilisateurs ne pourront accéder qu’aux parcours et les afficher, mais pas accéder à d’autres fonctionnalités telles que **[!DNL  Decision management]** in [!DNL Journey Optimizer].

Pour créer notre **Parcours en lecture seule** **[!UICONTROL product profiles]**:

1. Accédez au [!DNL Admin Console].

1. Dans la **[!UICONTROL Products]** , sélectionnez la variable **[!UICONTROL Experience Cloud - Platform powered applications]** produit.

1. Cliquez sur **[!UICONTROL New Profile]**.

   ![](assets/do-not-localize/access_control_9.png)

1. Ajouter un **[!UICONTROL Product Profile Name]**, **[!UICONTROL Display Name]** et **[!UICONTROL Description]** pour votre nouveau **[!UICONTROL product profiles]**.

   ![](assets/do-not-localize/access_control_10.png)

1. Dans le **[!UICONTROL Notifications]** catégorie, choisissez si les utilisateurs seront avertis par e-mail lorsqu’ils seront ajoutés ou supprimés de ce profil de produit.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]** et sélectionnez le **[!UICONTROL product profiles]**.

1. Pour ajouter des autorisations d’accès aux différentes fonctionnalités aux utilisateurs, sélectionnez l’option **[!UICONTROL Permissions]** .

1. Effectuez une sélection parmi les différentes fonctionnalités telles que **[!DNL Journeys]**, **[!DNL Segments]** ou **[!DNL Decision management]** disponible dans [!DNL Journey Optimizer] répertorié dans le menu de gauche.

   Ici, sélectionnez la variable **[!UICONTROL Journeys]** fonctionnalité.

   ![](assets/do-not-localize/access_control_11.png)

1. Dans la **[!UICONTROL Available Permission Items]** sélectionnez les autorisations à attribuer à votre **[!UICONTROL Product profile]** en cliquant sur l’icône plus (+).

   Ici, sélectionnez **[!DNL View journeys]** et **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. Sélectionnez la **[!UICONTROL Sandbox access]** la possibilité de choisir quel(s) environnement(s) de test affecter à votre **[!UICONTROL Product profile]**.

   ![](assets/do-not-localize/access_control_13.png)

1. Sous **[!UICONTROL Available Permissions Items]**, cliquez sur l’icône plus (+) pour attribuer des environnements de test à votre profil. [En savoir plus sur les environnements de test](sandboxes.md).

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Save]**.

Votre **[!UICONTROL Product profile]** est maintenant créé et configuré. Vous devez maintenant l’affecter aux utilisateurs.

Pour plus d’informations sur la création et la gestion des profils de produits, reportez-vous à la section [Documentation d’Admin Console](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-product-profiles.ug.html).
