---
solution: Journey Optimizer
product: journey optimizer
title: Gérer les utilisateurs et utilisatrices, et les rôles
description: Découvrez comment gérer les utilisateurs et les rôles
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
keywords: produit, profils, sandbox
source-git-commit: 417eea2a52d4fb38ae96cf74f90658f87694be5a
workflow-type: tm+mt
source-wordcount: '786'
ht-degree: 26%

---

# Gérer les utilisateurs et utilisatrices, et les rôles {#manage-permissions}

>[!IMPORTANT]
>
> Chacune des procédures présentées ci-dessous ne peut être réalisée que par un administrateur **[!UICONTROL Produit]** ou **[!UICONTROL Système]**. Pour plus d&#39;informations à ce sujet, consultez la [documentation relative à Admin Console](https://helpx.adobe.com/fr/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

**[!UICONTROL Rôles]** se rapportent à un ensemble d’utilisateurs qui partagent les mêmes autorisations et environnements de test. Ces rôles vous permettent de gérer facilement les accès et les autorisations pour différents groupes d’utilisateurs au sein de votre entreprise.

Avec le [!DNL Journey Optimizer] produit, vous avez la possibilité de choisir parmi une gamme de **[!UICONTROL Rôles]**, chacun disposant de différents niveaux d’autorisations, à affecter à vos utilisateurs. Pour plus d’informations sur les **[!UICONTROL Rôles]**, voir à ce sujet [page](ootb-product-profiles.md).

Lorsqu’un utilisateur appartient à un **[!UICONTROL Rôle]**, ils ont accès aux applications et services Adobe contenus dans le produit.

Si les rôles préexistants ne répondent pas aux besoins spécifiques de votre entreprise, vous pouvez également créer des **[!UICONTROL Rôles]** pour affiner l’accès à certaines fonctionnalités ou à certains objets de l’interface. Ainsi, vous pouvez vous assurer que chaque utilisateur n’a accès qu’aux ressources et outils dont il a besoin pour exécuter ses tâches efficacement.

## Attribution d’un rôle {#assigning-role}

Vous pouvez choisir d’affecter une **[!UICONTROL Rôle]** à vos utilisateurs.

Vous trouverez la liste de tous les rôles d’usine avec les autorisations attribuées dans la section [Rôles intégrés](ootb-product-profiles.md) .

Pour affecter une **[!UICONTROL Rôle]**:

1. Pour affecter un rôle à un utilisateur dans la variable [!DNL Permissions] produit, accédez à la **[!UICONTROL Rôles]** et sélectionnez le rôle souhaité.

   ![](assets/do-not-localize/access_control_2.png)

1. Dans l&#39;onglet **[!UICONTROL Utilisateurs]**, cliquez sur **[!UICONTROL Ajouter un utilisateur]**.

   ![](assets/do-not-localize/access_control_3.png)

1. Saisissez le nom ou l’adresse électronique de votre utilisateur, ou sélectionnez l’utilisateur dans la liste, puis cliquez sur **[!UICONTROL Enregistrer]**.

   Si l&#39;utilisateur n&#39;a pas été créé auparavant dans [!DNL Admin Console], consultez la [documentation relative à l&#39;ajout d&#39;utilisateurs](https://helpx.adobe.com/fr/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html#add-users).

   ![](assets/do-not-localize/access_control_4.png)

L&#39;utilisateur doit alors recevoir un email le redirigeant vers votre instance.

Pour plus d&#39;informations sur la gestion des utilisateurs, consultez la [documentation relative à Admin Console](https://helpx.adobe.com/fr/enterprise/admin-guide.html/enterprise/using/manage-users-individually.ug.html).

Lors de l’accès à l’instance, l’utilisateur voit une vue spécifique en fonction des autorisations attribuées dans la variable **[!UICONTROL Rôle]**. Si l’utilisateur ne dispose pas du droit d’accès à une fonctionnalité, le message suivant s’affiche :

`You don't have permission to access this feature. Permission needed: XX.`

## Modification d’un rôle existant {#edit-product-profile}

Pour les paramètres d’usine ou personnalisés **[!UICONTROL Rôles]**, vous pouvez décider à tout moment d’ajouter ou de supprimer des autorisations.

Dans cet exemple, nous allons ajouter **[!UICONTROL Autorisations]** associé au **[!UICONTROL Parcours]** ressource pour les utilisateurs affectés à la visionneuse de Parcours **[!UICONTROL Rôle]**. Les utilisateurs pourront alors publier des parcours.

Notez que si vous modifiez une **[!UICONTROL Rôle]**, cela aura un impact sur chaque utilisateur affecté à cette tâche. **[!UICONTROL Rôle]**.

1. Pour affecter un rôle à un utilisateur dans la variable [!DNL Permissions] produit, accédez à la **[!UICONTROL Rôles]** et sélectionnez le rôle de votre choix. Ici, la visionneuse de Parcours **[!UICONTROL Rôle]**.
   ![](assets/do-not-localize/access_control_5.png)

1. À partir de **[!UICONTROL Rôle]** tableau de bord, cliquez sur **[!UICONTROL Modifier]**.

   ![](assets/do-not-localize/access_control_6.png)

1. Le **[!UICONTROL Ressources]** affiche la liste des ressources qui s’appliquent au **[!UICONTROL Experience Cloud - Applications basées sur Platform]** produit. Effectuez un glisser-déposer des ressources pour attribuer une autorisation.

   Dans la **[!UICONTROL Parcours]** liste déroulante de ressources, nous choisissons ici le parcours de publication **[!UICONTROL Autorisation]**.

   ![](assets/do-not-localize/access_control_14.png)

1. Si nécessaire, sous **[!UICONTROL Éléments d’autorisation inclus]**, cliquez sur l’icône X en regard de pour supprimer les autorisations ou les ressources associées à votre rôle.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Enregistrer]**.

Si nécessaire, vous pouvez également créer un nouveau rôle avec des autorisations spécifiques. Voir à ce sujet la section [Création d’un rôle](#create-product-profile).

## Créer un rôle {#create-product-profile}

[!DNL Journey Optimizer] vous permet de créer les vôtres **[!UICONTROL Rôles]** et attribuez un ensemble d’autorisations et d’environnements de test à vos utilisateurs. Avec **[!UICONTROL Rôles]**, vous pouvez autoriser ou refuser l’accès à certaines fonctionnalités ou à certains objets de l’interface.

Pour plus d’informations sur la création et la gestion des sandbox, consultez la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=fr){target="_blank"}.

Dans cet exemple, nous allons créer un rôle nommé **Parcours en lecture seule** où nous accorderons des droits en lecture seule à la fonctionnalité de Parcours. Les utilisateurs pourront uniquement accéder aux parcours et les afficher. Ils ne pourront pas accéder à dʼautres fonctionnalités telles que **[!DNL  Decision management]** dans [!DNL Journey Optimizer].

Pour créer notre **Parcours en lecture seule** **[!UICONTROL Rôle]**:

1. Pour affecter un rôle à un utilisateur dans la variable [!DNL Permissions] produit, accédez à la **[!UICONTROL Rôles]** et cliquez sur **[!UICONTROL Création d’un rôle]**.

   ![](assets/do-not-localize/access_control_9.png)

1. Ajouter un **[!UICONTROL Nom]** et **[!UICONTROL Description]** pour votre nouveau **[!UICONTROL Rôle]**. Cliquez ensuite sur **[!UICONTROL Confirmer]**.

   ![](assets/do-not-localize/access_control_10.png)

1. Dans la **[!UICONTROL Sandbox]** menu déroulant des ressources, choisissez le ou les environnements de test à affecter à votre **[!UICONTROL Rôle]**. [En savoir plus sur les sandbox](sandboxes.md).

   ![](assets/do-not-localize/access_control_13.png)

1. Effectuez une sélection parmi les différentes ressources telles que **[!DNL Journeys]**, **[!DNL Segments]** ou **[!DNL Decision management]** disponible dans [!DNL Journey Optimizer] répertorié dans le menu de gauche.

   Ici, sélectionnez la variable **[!UICONTROL Parcours]** ressource.

   ![](assets/do-not-localize/access_control_11.png)

1. Dans la **[!UICONTROL Parcours]** , sélectionnez les autorisations à attribuer à votre **[!UICONTROL Rôle]**.

   Ici, sélectionnez **[!DNL View journeys]**, **[!DNL View journeys report]**  et **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Enregistrer]**.

Votre **[!UICONTROL Rôle]** est maintenant créé et configuré. Vous devez à présent l&#39;affecter aux utilisateurs.

Pour plus d&#39;informations sur la création et la gestion des rôles, reportez-vous à la section [Documentation du Admin Console](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/roles.html?lang=fr).