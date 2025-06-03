---
solution: Journey Optimizer
product: journey optimizer
title: Gérer les utilisateurs et utilisatrices et les rôles
description: Découvrez comment gérer les utilisateurs et utilisatrices et les rôles.
exl-id: 85fd386a-45fa-4f9a-89d1-cecc0749b90d
feature: Access Management
topic: Administration
role: Admin
level: Intermediate
keywords: produit, profils, sandbox
source-git-commit: 404fffa8d1f2ed40b18246002b67e2b533d8c19e
workflow-type: tm+mt
source-wordcount: '710'
ht-degree: 51%

---

# Gérer les utilisateurs et utilisatrices et les rôles {#manage-permissions}

Les **[!UICONTROL rôles]** se rapportent à un ensemble d’utilisateurs et d’utilisatrices qui partagent les mêmes autorisations et sandbox. Ces rôles vous permettent de gérer facilement les accès et les autorisations pour différents groupes d’utilisateurs et d’utilisatrices au sein de votre organisation.

Avec le produit [!DNL Journey Optimizer], vous pouvez choisir parmi un éventail de **[!UICONTROL rôles]** préexistants, chacun avec différents niveaux d’autorisations, à affecter à vos utilisateurs et utilisatrices. Pour plus d’informations sur les **[!UICONTROL rôles]** disponibles, consultez cette [page](ootb-product-profiles.md).

Lorsqu’un utilisateur appartient à un **[!UICONTROL rôle]**, il a accès aux applications et services Adobe contenus dans le produit.

Si les rôles préexistants ne répondent pas aux besoins spécifiques de votre organisation, vous pouvez également créer des **[!UICONTROL rôles]** personnalisés pour affiner l’accès à certaines fonctionnalités ou à certains objets de l’interface. Ainsi, vous vous assurez que chaque utilisateur n’a accès qu’aux ressources et outils dont il a besoin pour exécuter ses tâches efficacement.


>[!IMPORTANT]
>
>Les étapes et procédures détaillées ci-dessous ne peuvent être effectuées que par un administrateur **[!UICONTROL Produit]** ou **[!UICONTROL Système]**.


## Attribuer un rôle {#assigning-role}

Vous pouvez attribuer un **[!UICONTROL rôle]** personnalisé ou par défaut à vos utilisateurs.

La liste de tous les rôles prêts à l’emploi auxquels des autorisations sont attribuées est disponible dans la section [Rôles intégrés](ootb-product-profiles.md).

Pour attribuer un **[!UICONTROL rôle]** :

1. Pour attribuer un rôle à un utilisateur ou une utilisatrice dans le produit [!DNL Permissions], accédez à l’onglet **[!UICONTROL Rôles]** et sélectionnez le rôle de votre choix.

   ![](assets/do-not-localize/access_control_2.png)

1. Dans l’onglet **[!UICONTROL Utilisateurs]**, cliquez sur **[!UICONTROL Ajouter un utilisateur]**.

   ![](assets/do-not-localize/access_control_3.png)

1. Saisissez le nom ou l’adresse électronique de l’utilisateur ou sélectionnez-le dans la liste, puis cliquez sur **[!UICONTROL Enregistrer]**.

   Si la personne utilisatrice n’a pas été créée auparavant dans [!DNL Admin Console], consultez la [documentation relative à l’ajout d’utilisateurs et d’utilisatrices](https://experienceleague.adobe.com/docs/experience-platform/access-control/ui/users.html?lang=fr){target="_blank"}.

   ![](assets/do-not-localize/access_control_4.png)

L’utilisateur reçoit un e-mail le redirigeant vers votre instance.

Pour plus d&#39;informations sur la gestion des utilisateurs, consultez la [documentation sur le contrôle d&#39;accès](https://experienceleague.adobe.com/docs/experience-platform/access-control/home.html?lang=fr){target="_blank"}.

Lors de l’accès à l’instance, l’utilisateur voit une vue spécifique en fonction des autorisations attribuées dans le **[!UICONTROL rôle]**. Si l’utilisateur ne dispose pas du droit d’accès à une fonctionnalité, le message suivant s’affiche :

`You don't have permission to access this feature. Permission needed: XX.`

## Modifier un rôle existant {#edit-product-profile}

Pour les **[!UICONTROL rôles]** intégrés ou personnalisés, vous pouvez décider à tout moment d’ajouter ou de supprimer des autorisations.

Dans l’exemple ci-dessous, nous souhaitons ajouter des **[!UICONTROL autorisations]** liées à la ressource **[!UICONTROL Parcours]** pour les utilisateurs affectés à la visionneuse de Parcours **[!UICONTROL Rôle]**. Les utilisateurs et utilisatrices pourront alors publier des parcours.

>[!IMPORTANT]
>
>Les modifications apportées à un rôle intégré ou personnalisé affecteront tous les utilisateurs affectés à ce rôle.

1. Pour modifier un rôle dans le produit [!DNL Permissions], accédez à l’onglet **[!UICONTROL Rôles]** et sélectionnez le rôle souhaité, ici la visionneuse de Parcours **[!UICONTROL Rôle]**.
   ![](assets/do-not-localize/access_control_5.png)

1. À partir du tableau de bord **[!UICONTROL Rôle]**, cliquez sur **[!UICONTROL Modifier]**.

   ![](assets/do-not-localize/access_control_6.png)

1. Le menu **[!UICONTROL Ressources]** affiche la liste des ressources qui s’appliquent au produit **[!UICONTROL Experience Cloud - Applications proposées par Platform]**. Glissez-déposez les ressources pour attribuer des autorisations.

   Dans la liste déroulante de ressources **[!UICONTROL Parcours]**, nous choisissons ici l’**[!UICONTROL autorisation]** Publier le parcours.

   ![](assets/do-not-localize/access_control_14.png)

1. Si nécessaire, sous **[!UICONTROL Éléments d’autorisation inclus]**, cliquez sur l’icône X pour supprimer des autorisations ou des ressources de votre rôle.

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Enregistrer]**.

Si nécessaire, vous pouvez également créer un nouveau rôle avec des autorisations spécifiques.

## Créer un rôle {#create-product-profile}

[!DNL Journey Optimizer] vous permet de créer vos propres **[!UICONTROL rôles]** et d’attribuer un ensemble d’autorisations et de sandbox à vos utilisateurs et utilisatrices. Avec les **[!UICONTROL rôles]**, vous pouvez autoriser ou refuser l’accès à certaines fonctionnalités ou à certains éléments de l’interface.

Pour plus d’informations sur la création et la gestion des sandbox, consultez la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=fr){target="_blank"}.

Dans cet exemple, nous allons créer un rôle nommé **Parcours en lecture seule** dans lequel nous accorderons des droits en lecture seule à la fonction de Parcours. Les utilisateurs et utilisatrices pourront uniquement accéder aux parcours et les afficher. Ils ne pourront pas accéder à dʼautres fonctionnalités telles que **[!DNL Decision management]** dans [!DNL Journey Optimizer].

Pour créer notre **[!UICONTROL rôle]** **Parcours en lecture seule** :

1. Pour attribuer un rôle à un utilisateur ou une utilisatrice dans le produit [!DNL Permissions], accédez à l’onglet **[!UICONTROL Rôles]** et cliquez sur **[!UICONTROL Créer un rôle]**.

   ![](assets/do-not-localize/access_control_9.png)

1. Ajoutez un **[!UICONTROL nom]** et une **[!UICONTROL description]** à votre nouveau **[!UICONTROL rôle]**. Cliquez ensuite sur **[!UICONTROL Confirmer]**.

   ![](assets/do-not-localize/access_control_10.png)

1. Dans le menu déroulant des ressources **[!UICONTROL Sandbox]**, choisissez la ou les sandbox à attribuer à votre **[!UICONTROL Rôle]**. [En savoir plus sur les sandbox](sandboxes.md).

   ![](assets/do-not-localize/access_control_13.png)

1. Faites votre choix parmi les différentes ressources telles que **[!DNL Journeys]**, **[!DNL Segments]** ou **[!DNL Decision management]** disponibles dans [!DNL Journey Optimizer] répertoriées dans le menu de gauche.

   Nous sélectionnons ici la ressource **[!UICONTROL Parcours]**.

   ![](assets/do-not-localize/access_control_11.png)

1. Dans le menu déroulant **[!UICONTROL Parcours]**, sélectionnez les autorisations à attribuer à votre **[!UICONTROL Rôle]**.

   Nous sélectionnons ici **[!DNL View journeys]**, **[!DNL View journeys report]** et **[!DNL View journeys event, data sources, actions]**.

   ![](assets/do-not-localize/access_control_12.png)

1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Enregistrer]**.

Votre **[!UICONTROL rôle]** est désormais créé et configuré. Vous devez à présent l’affecter aux utilisateurs et utilisatrices.

Pour plus d&#39;informations sur la création et la gestion des rôles, consultez la documentation de [Adobe Admin Console](https://experienceleague.adobe.com/docs/experience-platform/access-control/abac/permissions-ui/roles.html?lang=fr){target="_blank"}.
