---
title: Créer des applications d’une seule page
description: Découvrez comment créer des SPA et appliquer des modifications à différentes vues dans Journey Optimizer
feature: Web Channel
topic: Content Management
role: User
level: Beginner
exl-id: b33e4bca-d2e9-4610-9f04-008d47f686d0
source-git-commit: a2d67bbcf9b90c427ea3f755d80e465a3d7b10ec
workflow-type: tm+mt
source-wordcount: '464'
ht-degree: 8%

---

# Créer des applications d’une seule page {#web-author-spas}

## À propos des vues {#about-views}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications_views"
>title="Appliquer les modifications aux vues sélectionnées"
>abstract="Les modifications seront appliquées uniquement pour les vues sélectionnées. Les vues peuvent être découvertes à l’aide de la variable **Parcourir** et accédez-y. Vous ne trouvez pas la vue que vous recherchez ?"
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html?lang=fr" text="En savoir plus"

**Applications d’une seule page** (SPA) peut désormais être créé dans l’éditeur visuel du concepteur web. Vous pouvez ainsi sélectionner la variable spécifique **views** vous souhaitez appliquer vos modifications de page web à .

[Découvrez comment créer des applications monopage dans cette vidéo](#video)

Une vue peut être définie comme un site entier ou un groupe d’éléments visuels sur un site, tels que la page d’accueil, l’ensemble du site de produits ou les préférences de livraison, encadrés sur toutes les pages de passage en caisse.

Une configuration de développeur unique est nécessaire pour définir les vues dans l’implémentation du SDK Web de Adobe Experience Platform. Vous pouvez ainsi créer et exécuter des campagnes web Adobe Journey Optimizer sur SPA.

## Définition des vues dans l’implémentation du SDK Web {#define-views}

Les vues XDM peuvent être exploitées dans Adobe [!DNL Journey Optimizer] pour permettre aux marketeurs d’exécuter des campagnes de personnalisation et d’expérimentation web sur SPA via l’éditeur visuel web. [En savoir plus](web-spa-implementation.md)

Pour pouvoir accéder aux vues et les créer dans le [!DNL Journey Optimizer] dans l’interface utilisateur, veillez à suivre les étapes répertoriées dans [cette section](web-spa-implementation.md#implement-xdm-views).

## Découvrez les vues dans le concepteur web {#discover-views}

Une fois SPA configuration effectuée dans l’implémentation du SDK Web de Adobe Experience Platform, vous devez parcourir toutes les vues de votre site web auxquelles vous souhaitez appliquer des modifications. Suivez les étapes ci-dessous.

1. [Créer une campagne web](create-web.md) et accédez au [web designer](edit-web-content.md).

   La vue dans laquelle vous vous trouvez actuellement s’affiche en haut à gauche.

   ![](assets/web-designer-view-home.png)

1. Basculer vers **[!UICONTROL Parcourir]** mode . [En savoir plus](../web/edit-web-content.md#browse-mode)

   ![](assets/web-designer-view-browse.png)

1. Naviguez entre les différentes pages du site web pour toutes les découvrir. Le nom d’affichage affiché en haut change lorsque vous accédez à une autre page.

   ![](assets/web-designer-other-view.png)

## Application de modifications à d’autres vues {#apply-modifications-views}

Une fois que vous avez ajouté une modification alors que vous vous trouvez dans une vue spécifique, vous pouvez l’appliquer à d’autres vues sélectionnées. Suivez les étapes ci-dessous.

>[!CAUTION]
>
>Si vous n’avez pas découvert de vues à l’aide de la variable **[!UICONTROL Parcourir]** , vous ne pourrez pas les sélectionner pour appliquer vos modifications. [En savoir plus](#discover-views)

1. Sélectionnez l’icône **[!UICONTROL Modifications]** pour afficher le volet correspondant à gauche.

   ![](assets/web-designer-view-modifications-pane.png)

1. Sélectionnez une modification et cliquez sur le bouton **[!UICONTROL Autres actions]** en regard. Sélectionner **[!UICONTROL Appliquer à d’autres vues]**.

   ![](assets/web-designer-modifications-more-actions.png)

1. Sélectionnez les vues auxquelles vous souhaitez appliquer vos modifications.

   ![](assets/web-designer-modifications-apply-to.png)

1. Cliquez sur **[!UICONTROL Appliquer]**.

1. Basculer vers **[!UICONTROL Parcourir]** pour vérifier que les modifications sont appliquées sur les pages souhaitées.

   ![](assets/web-designer-modifications-applied-view.png)

## Vidéo pratique{#video}

Cette vidéo explique comment :

* Découvrez SPA vues à l’aide de **[!UICONTROL Parcourir]** mode
* Effectuer la création dans la vue actuelle
* Application des modifications de site web à plusieurs vues ou à toutes les vues découvertes
* Actions en bloc sur les modifications

>[!VIDEO](https://video.tv.adobe.com/v/3424536/?quality=12&learn=on)
