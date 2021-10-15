---
product: experience platform
solution: Experience Platform
title: Octroi de l'accès à Offer Decisioning
description: Découvrez comment gérer les autorisations des utilisateurs pour le service Offer Decisioning via Adobe Admin Console.
feature: Collections
role: User
level: Intermediate
exl-id: 2a2fece9-1ad5-498e-b0ee-5bb0b73a2cd5
source-git-commit: 43fb98a08555e6b889ad537e79dba78286dafeb9
workflow-type: tm+mt
source-wordcount: '293'
ht-degree: 100%

---

# Octroi de l’accès à la gestion des décisions {#granting-acess-to-decision-management}

Les autorisations d’accès et d’utilisation des fonctionnalités d’Offer Decisioning sont gérées à l’aide d’[Adobe Admin Console](https://helpx.adobe.com/fr/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}.

Pour accorder l’accès à la fonctionnalité de gestion des décisions, vous devez créer un **[!UICONTROL profil de produit]** et attribuer les autorisations correspondantes à vos utilisateurs. Pour en savoir plus sur la gestion des utilisateurs et des autorisations [!DNL Journey Optimizer], consultez [cette section](../../administration/permissions.md).

Les autorisations spécifiques à la gestion des décisions sont répertoriées dans [cette section](../../administration/high-low-permissions.md#manage-decisioning).

<!--If you are a [!DNL Journey Optimizer] user leveraging the **Decision Management** functionality, you need to have the [Decision management permissions](../../administration/high-low-permissions.md#decisions-permissions) enabled to acces all related capabilities. Learn more on managing [!DNL Journey Optimizer] users and permissions in [this section](../../administration/permissions.md).

If you are an [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/home.html){target="_blank"} user leveraging the **Offer Decisioning** application service, follow the steps [below](#granting-acess-to-offer-decisioning) to grant access to [!DNL Offer Decisioning].

Grant access to Offer Decisioning

The steps below only apply to **Experience Platform users** leveraging the [!DNL Offer Decisioning] service.-->

1. Ouvrez l&#39;[Admin Console](https://helpx.adobe.com/enterprise/managing/user-guide.html), puis sélectionnez **[!UICONTROL Adobe Experience Platform]**.

   <!--![](../../assets/offers_admin_console.png)-->

1. Les profils de produit du service s&#39;affichent. Pour créer un profil de produit, cliquez sur le bouton **[!UICONTROL Nouveau profil]**.

   ![](../../assets/offers_rights_productprofile.png)

   >[!NOTE]
   >
   >Vous pouvez avoir autant de profils de produit que vous le souhaitez, correspondant aux différents rôles que vous souhaitez configurer pour votre organisation.

1. Indiquez le nom et la description du profil de produit, puis cliquez sur **[!UICONTROL Suivant]**.

   ![](../../assets/create-product-profile.png)

   <!--To access the product profile’s permissions, select the **[!UICONTROL Permissions]** line.-->

1. Sélectionnez les services à activer pour le profil de produit. Par défaut, tous les services sont sélectionnés, ce qui est recommandé pour s&#39;assurer que toutes les fonctionnalités d&#39;Experience Platform sont disponibles.

   ![](../../assets/enable-services.png)

1. Dans la section **[!UICONTROL Gestion des décisions]**, cliquez sur le bouton **+** pour attribuer des autorisations au profil de produit, puis cliquez sur **[!UICONTROL Enregistrer]**.

   ![](../../assets/configure-profile.png)

   Les autorisations disponibles sont les suivantes :

   **[!UICONTROL Gérer les activités de prise de décision]** :

   * Lecture, écriture, suppression d&#39;offres
   * Lecture, écriture, suppression de décisions (précédemment appelées activités d&#39;offre)
   * Lecture, écriture, suppression d&#39;emplacements

   **[!UICONTROL Exécuter les activités de prise de décision]** :

   * Lecture d&#39;offres
   * Lecture de décisions
   * Lecture d&#39;emplacements

   **[!UICONTROL Gérer les options de prise de décision]** :

   * Lecture, écriture, suppression d&#39;offres
   * Lecture de décisions
   * Lecture, écriture, suppression d&#39;emplacements



1. Un résumé des autorisations du profil de produit s&#39;affiche. Vous pouvez maintenant affecter des utilisateurs au profil de produit afin qu&#39;ils puissent accéder à ces autorisations.

   ![](../../assets/product-profile-created.png)

>[!NOTE]
>
>Pour plus d&#39;informations sur la gestion des autorisations des utilisateurs, consultez la [documentation de l‘Admin Console](https://helpx.adobe.com/enterprise/managing/user-guide.html){target=&quot;_blank&quot;}.

