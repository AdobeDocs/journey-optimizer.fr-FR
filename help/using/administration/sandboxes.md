---
solution: Journey Optimizer
product: journey optimizer
title: Gestion des environnements de test
description: Découvrez comment gérer les environnements de test
feature: Sandboxes
topic: Administration
role: Admin
level: Intermediate
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '345'
ht-degree: 0%

---

# Gestion des environnements de test {#sandboxes}

## Utilisation des environnements de test {#using-sandbox}

[!DNL Journey Optimizer] vous permet de partitionner votre instance en environnements virtuels séparés appelés environnements de test.
Les environnements de test sont attribués via les profils de produit dans Admin Console. [Découvrez comment affecter des environnements de test](permissions.md#create-product-profile).

[!DNL Journey Optimizer] reflète les environnements Sandbox Adobe Experience Platform qui ont été créés pour une organisation donnée.
Les environnements de test Adobe Experience Platform peuvent être créés ou réinitialisés à partir de votre instance Adobe Experience Platform. [En savoir plus dans le guide d’utilisation de Sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html){target=&quot;_blank&quot;}.

Le sélecteur d’environnement de test se trouve dans le coin supérieur droit de votre écran en regard du nom de votre organisation. Pour passer d’un environnement de test à un autre, cliquez sur l’environnement de test actuellement actif dans le sélecteur et sélectionnez un autre environnement de test dans la liste déroulante.

![](assets/sandbox_5.png)

➡️ [En savoir plus sur les environnements de test dans cette vidéo](#video)

## Attribution d’environnements de test {#assign-sandboxes}

>[!IMPORTANT]
>
> La gestion des environnements de test ne peut être effectuée que par un **[!UICONTROL Product]** ou **[!UICONTROL System]** administrateur. Voir à ce sujet la section [Documentation de la console d’administration](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html){target=&quot;_blank&quot;}.

Vous pouvez choisir d’affecter différents environnements de test à des environnements prêts à l’emploi ou personnalisés. **[!UICONTROL Product profiles]**.

Pour affecter des environnements de test :

1. Dans le [!DNL Admin Console], de la fonction **[!UICONTROL Products]** , sélectionnez la variable **[!UICONTROL Adobe Experience Platform Apps]** produit.

1. Sélectionnez une **[!UICONTROL Product profile]**.

   ![](assets/sandbox_1.png)

1. Sélectionnez la **[!UICONTROL Permissions]** .

1. Sélectionnez la **[!UICONTROL Sandboxes]** fonctionnalité.

   ![](assets/sandbox_2.png)

1. Sous **[!UICONTROL Available Permissions Items]**, cliquez sur l’icône plus (+) pour attribuer des environnements de test à votre profil. [En savoir plus sur les environnements de test](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html){target=&quot;_blank&quot;}.

   ![](assets/sandbox_3.png)

1. Si nécessaire, sous **[!UICONTROL Included Permission Items]**, cliquez sur l’icône X en regard de pour supprimer l’accès aux environnements de test à votre **[!UICONTROL Product profile]**.

   ![](assets/sandbox_4.png)

1. Cliquez sur **[!UICONTROL Save]**.

## Accès au contenu {#content-access}

Pour configurer l’accessibilité du contenu, vous devez affecter un dossier de contenu partagé à chacun de vos environnements de test. Vous pouvez créer et configurer votre dossier partagé dans le **[!UICONTROL Storage]** affiché dans l’onglet [!DNL Admin Console] pour les administrateurs. Si vous avez accès au [!DNL Admin Console] en tant qu’administrateur système, vous pouvez créer des dossiers partagés et ajouter des délégués avec un niveau d’accès différent à vos dossiers partagés.

![](assets/do-not-localize/content_access.png)

Notez que pour que votre contenu soit synchronisé avec l’environnement de test correct, vous devez suivre la même syntaxe que l’environnement de test ; par exemple, si votre environnement de test est appelé développement, votre dossier partagé doit porter le même nom.

[Découvrez comment gérer les dossiers partagés](https://helpx.adobe.com/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target=&quot;_blank&quot;}.

## Vidéo pratique{#video}

Découvrez ce que sont les environnements de test et comment faire la distinction entre les environnements de test de développement et de production. Découvrez comment créer, réinitialiser et supprimer des environnements de test.

>[!VIDEO](https://video.tv.adobe.com/v/334355?quality=12)
