---
title: Gestion des utilisateurs et des profils de produits
description: Découvrez comment gérer les autorisations.
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '834'
ht-degree: 100%

---

# Gestion des utilisateurs et des profils de produits {#manage-permissions}

>[!IMPORTANT]
>
> Chacune des procédures présentées ci-dessous ne peut être réalisée que par un administrateur **[!UICONTROL Produit]** ou **[!UICONTROL Système]**. Pour plus d&#39;informations à ce sujet, consultez la [documentation relative à Admin Console](https://helpx.adobe.com/fr/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

Les **[!UICONTROL profils de produit]** sont des ensembles d&#39;utilisateurs qui partagent les mêmes autorisations et environnements Sandbox au sein de votre organisation.

Le produit [!DNL Journey Optimizer] vous permet de choisir parmi différents **[!UICONTROL profils de produit]** prêts à l&#39;emploi avec différents niveaux d&#39;autorisations à affecter à vos utilisateurs. Pour plus d&#39;informations sur les **[!UICONTROL profils de produits]** disponibles, consultez cette [page](ootb-product-profiles.md).

Chaque utilisateur appartenant à un **[!UICONTROL profil de produit]** a droit aux applications et services d&#39;Adobe contenus dans le produit.

Vous pouvez également créer vos propres **[!UICONTROL profils de produit]** si vous souhaitez affiner l&#39;accès de vos utilisateurs à certaines fonctionnalités ou objets de l&#39;interface.

## Attribution d&#39;un profil de produit {#assigning-product-profile}

Vous pouvez choisir d&#39;attribuer un **[!UICONTROL profil de produit]** personnalisé ou par défaut à vos utilisateurs.

Vous trouverez dans la section [Profils de produits natifs](ootb-product-profiles.md), la liste de tous les profils de produit par défaut auxquels des autorisations sont associées.

Pour attribuer un **[!UICONTROL profil de produit]** :

1. Dans l&#39;onglet **[!UICONTROL Produits]** de [!DNL Admin Console], sélectionnez le produit **[!UICONTROL Experience Cloud - Applications de plateforme]**.

1. Sélectionnez un **[!UICONTROL profil de produit]**.

   ![](assets/do-not-localize/access_control_2.png)

1. Dans l&#39;onglet **[!UICONTROL Utilisateurs]**, cliquez sur **[!UICONTROL Ajouter un utilisateur]**.

   ![](assets/do-not-localize/access_control_3.png)

1. Saisissez le nom ou l&#39;adresse email de votre utilisateur et sélectionnez-le.

   Si l&#39;utilisateur n&#39;a pas été créé auparavant dans [!DNL Admin Console], consultez la [documentation relative à l&#39;ajout d&#39;utilisateurs](https://helpx.adobe.com/fr/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/do-not-localize/access_control_4.png)

1. Effectuez les mêmes étapes que précédemment pour ajouter d&#39;autres utilisateurs à votre **[!UICONTROL profil de produit]**. Cliquez ensuite sur **[!UICONTROL Enregistrer]**.

L&#39;utilisateur doit alors recevoir un email le redirigeant vers votre instance.

Pour plus d&#39;informations sur la gestion des utilisateurs, consultez la [documentation relative à Admin Console](https://helpx.adobe.com/fr/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

Lors de l&#39;accès à l&#39;instance, l&#39;utilisateur voit une vue spécifique en fonction des autorisations attribuées dans le **[!UICONTROL profil de produit]**. Si l’utilisateur ne dispose pas du droit d’accès à une fonctionnalité, le message suivant s’affiche :

`You don't have permission to access this feature. Permission needed: XX.`

## Modification d&#39;un profil de produit existant {#edit-product-profile}

Pour les **[!UICONTROL profils de produit]** personnalisés ou par défaut, vous pouvez décider à tout moment d’ajouter ou de supprimer des autorisations.

Dans cet exemple, nous souhaitons ajouter des **[!UICONTROL autorisations]** liées à la fonctionnalité **[!UICONTROL Parcours]** pour les utilisateurs affectés au **[!UICONTROL profil de produit]** Observateur de parcours. Les utilisateurs pourront alors publier des parcours.

Veuillez noter que si vous modifiez un **[!UICONTROL profil de produit]** personnalisé ou par défaut, cela aura un impact sur chaque utilisateur affecté à ce **[!UICONTROL profil de produit]**.

1. Dans l&#39;onglet **[!UICONTROL Produits]** de [!DNL Admin Console], sélectionnez le produit **[!UICONTROL Experience Cloud - Applications de plateforme]**.

1. Sélectionnez le **[!UICONTROL Profil produit]** Observateur de parcours.

1. Sélectionnez l&#39;onglet **[!UICONTROL Autorisations]**.

   L&#39;onglet **[!UICONTROL Autorisations]** affiche la liste des fonctionnalités qui s&#39;appliquent au produit **[!UICONTROL Experience Cloud - Applications optimisées par Platform]**.

   ![](assets/do-not-localize/access_control_5.png)

1. Sélectionnez la fonctionnalité **[!UICONTROL Parcours]**.

   ![](assets/do-not-localize/access_control_6.png)

1. Dans la liste **[!UICONTROL Éléments d&#39;autorisation disponibles]**, sélectionnez les autorisations à attribuer à votre **[!UICONTROL profil de produit]** en cliquant sur l&#39;icône plus (+).

   Ici, nous ajoutons l’autorisation **[!UICONTROL Publier les parcours]**.

1. Si nécessaire, dans **[!UICONTROL Éléments d&#39;autorisations disponibles]**, cliquez sur l&#39;icône X la plus proche pour supprimer les autorisations de votre profil de produit.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Enregistrer]**.

Si nécessaire, vous pouvez également créer un profil de produit avec des autorisations spécifiques. Voir à ce sujet la section [Créer un profil de produit](#create-product-profile).

## Création d&#39;un profil de produit {#create-product-profile}

[!DNL Journey Optimizer] vous permet de créer vos propres **[!UICONTROL profils de produit]** et d&#39;attribuer un ensemble de droits et d&#39;environnements Sandbox à vos utilisateurs. Avec les **[!UICONTROL profils de produit]**, vous pouvez autoriser ou refuser l&#39;accès à certaines fonctionnalités ou à certains objets de l&#39;interface.

Pour plus d&#39;informations sur la création et la gestion des environnements Sandbox, consultez la [documentation d&#39;Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=fr){target=&quot;_blank&quot;}.

Dans cet exemple, nous allons créer un profil de produit nommé **Parcours en lecture seule** dans lequel nous accorderons des droits en lecture seule à la fonction Parcours. Les utilisateurs pourront uniquement accéder aux parcours et les afficher. Ils ne pourront pas accéder à dʼautres fonctionnalités telles que **[!DNL  Decision management]** dans [!DNL Journey Optimizer].

Pour créer nos **[!UICONTROL profils de produit]** **Parcours en lecture seule** :

1. Accédez à [!DNL Admin Console].

1. Dans l&#39;onglet **[!UICONTROL Produits]**, sélectionnez le produit **[!UICONTROL Experience Cloud - Applications de plateforme]**.

1. Cliquez sur **[!UICONTROL Nouveau profil]**.

   ![](assets/do-not-localize/access_control_9.png)

1. Ajoutez un **[!UICONTROL Nom du profil de produit]**, **[!UICONTROL Nom d&#39;affichage]** et **[!UICONTROL Description]** pour vos nouveaux **[!UICONTROL profils de produit]**.

   ![](assets/do-not-localize/access_control_10.png)

1. Dans la catégorie **[!UICONTROL Notifications]**, indiquez si les utilisateurs seront avertis par e-mail lorsqu&#39;ils seront ajoutés ou supprimés de ce profil de produit.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Enregistrer]** et sélectionnez les **[!UICONTROL profils de produit]** que vous venez de créer.

1. Pour ajouter des autorisations permettant aux utilisateurs d&#39;accéder à différentes fonctionnalités, sélectionnez l&#39;onglet **[!UICONTROL Autorisations]**.

1. Choisissez entre les différentes fonctionnalités telles que **[!DNL Journeys]**, **[!DNL Segments]** ou **[!DNL Decision management]** disponibles dans [!DNL Journey Optimizer] dans le menu de gauche.

   Nous sélectionnons ici la fonctionnalité **[!UICONTROL Parcours]**.

   ![](assets/do-not-localize/access_control_11.png)

1. Dans la liste **[!UICONTROL Éléments d&#39;autorisation disponibles]**, sélectionnez les autorisations à attribuer à votre **[!UICONTROL profil de produit]** en cliquant sur l&#39;icône plus (+).

   Nous sélectionnons ici **[!DNL View journeys]** et **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. Sélectionnez la fonction **[!UICONTROL Accès à l&#39;environnement Sandbox]**, pour choisir un ou plusieurs environnements Sandbox à affecter à votre **[!UICONTROL profil de produit]**.

   ![](assets/do-not-localize/access_control_13.png)

1. Dans **[!UICONTROL Éléments d&#39;autorisations disponibles]**, cliquez sur l&#39;icône plus (+) pour affecter des environnements Sandbox à votre profil. [En savoir plus sur les environnements Sandbox](sandboxes.md).

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Enregistrer]**.

Votre **[!UICONTROL profil de produit]** est maintenant créé et configuré. Vous devez à présent l&#39;affecter aux utilisateurs.

Pour plus d&#39;informations sur la création et la gestion des profils de produits, consultez la [documentation relative à Admin Console](https://helpx.adobe.com/fr/enterprise/admin-guide.html/enterprise/using/manage-product-profiles.ug.html).
