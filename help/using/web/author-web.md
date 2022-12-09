---
title: Création de pages web
description: Découvrez comment créer une page web et modifier son contenu dans Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 3847ac1d-2c0a-4f80-8df9-e8e304faf261
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1045'
ht-degree: 0%

---

# Création de pages web {#author-web}

>[!AVAILABILITY]
>
>La fonctionnalité de canal web est actuellement disponible en version bêta pour sélectionner uniquement les utilisateurs.

Dans [!DNL Journey Optimizer] la création web est optimisée par l’extension de navigateur Adobe Experience Cloud Visual Helper chrome. [En savoir plus](visual-editing-helper.md)

Pour accéder à des pages web et les créer dans le [!DNL Journey Optimizer] , suivez les conditions préalables répertoriées dans [cette section](create-web.md#prerequesites).

## Modifier le contenu d’une page web {#edit-web-content}

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_surface"
>title="Saisissez l’URL à modifier."
>abstract="Saisissez l&#39;URL d&#39;une page web spécifique à utiliser pour l&#39;édition du contenu qui sera appliqué sur la surface web définie ci-dessus. La page web doit être mise en oeuvre à l’aide du SDK Web d’Adobe Experience Platform."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html" text="En savoir plus"

>[!CONTEXTUALHELP]
>id="ajo_web_url_to_edit_rule"
>title="Saisissez l’URL à modifier."
>abstract="Saisissez l’URL d’une page web spécifique à utiliser pour l’édition du contenu qui sera appliqué à toutes les pages correspondant à la règle. La page web doit être mise en oeuvre à l’aide du SDK Web d’Adobe Experience Platform."
>additional-url="https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html" text="En savoir plus"

<!--Confirm the URL to use for authoring content on the surface. Typically the Authoring URL will be the surface URL itself, but you may include extra parameters if required. The page must include the Adobe Experience Platform Web SDK.-->

Une fois que vous avez créé une action web à partir de la campagne, vous pouvez éditer votre contenu à l&#39;aide du concepteur web. Pour ce faire, procédez comme suit.

>[!CAUTION]
>
>Pour y accéder : [!DNL Journey Optimizer], votre page web doit être implémentée à l’aide de la fonction [SDK Web d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target=&quot;_blank&quot;}.

1. Dans la **[!UICONTROL Action]** de l&#39;opération, sélectionnez **[!UICONTROL Edit content]** pour commencer à créer votre campagne web.

1. Si vous avez créé une règle de correspondance de pages, vous devez saisir toute URL correspondant à cette règle. Les modifications seront appliquées à toutes les pages correspondant à la règle.

   >[!NOTE]
   >
   >Si vous avez saisi une seule URL comme surface web, l’URL à personnaliser est déjà renseignée.

   ![](assets/web-edit-enter-url.png)

1. Le contenu de la page s’affiche.

   >[!CAUTION]
   >
   >La page web doit inclure la variable [SDK Web d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/platform-learn/implement-web-sdk/overview.html){target=&quot;_blank&quot;}.

1. Cliquez sur **[!UICONTROL Open web designer]** pour la modifier. [En savoir plus](author-web.md)

   ![](assets/web-open-designer.png)

1. Le concepteur web s’affiche.

   ![](assets/web-designer.png)

1. Sélectionnez un élément dans la zone de travail, tel qu’une image, un bouton, un paragraphe, un texte, un conteneur, un en-tête, un lien, etc. et utilisez :

   * Le menu contextuel permettant d&#39;éditer son contenu, sa mise en page, insérer des liens ou la personnalisation, etc.

      ![](assets/web-designer-contextual-bar.png)

   * Les icônes situées en haut du panneau de droite permettent de modifier, dupliquer, supprimer ou masquer chaque élément.

      ![](assets/web-designer-right-panel-icons.png)

   * Panneau de droite qui change dynamiquement en fonction de l’élément sélectionné. Vous pouvez, par exemple, modifier l’arrière-plan, la typographie, la bordure, la taille, la position, l’espacement, les effets ou les styles intégrés d’un élément.

      ![](assets/web-designer-right-panel.png)

## Utilisation des composants de contenu {#content-components}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_components"
>title="Ajout de composants de contenu à une page web"
>abstract="Vous pouvez ajouter plusieurs composants à votre page web et les modifier selon vos besoins."

1. Dans la **[!UICONTROL Components]** dans le volet de gauche, vous pouvez ajouter les composants suivants à votre page web et les modifier selon vos besoins :

   * [Diviseur](../email/content-components.md#divider)
   * [HTML](../email/content-components.md#HTML)
   * [Image](../email/content-components.md#image)
   * En-tête : l’utilisation de ce composant est similaire à l’utilisation de la fonction **[!UICONTROL Text]** dans le concepteur d’email. [En savoir plus](../email/content-components.md#text)
   * Paragraphe : l’utilisation de ce composant est similaire à l’utilisation de la propriété **[!UICONTROL Text]** dans le concepteur d’email. [En savoir plus](../email/content-components.md#text)
   * Lien - Découvrez comment définir le style du lien dans [cette section](../email/styling-links.md)
   * [Décision sur l’offre](../email/add-offers-email.md)

   ![](assets/web-designer-components.png)

1. Passez la souris sur la page, puis cliquez sur l’icône **[!UICONTROL Insert before]** ou **[!UICONTROL Insert after]** pour ajouter le composant à un élément existant sur la page.

   ![](assets/web-designer-insert-components.png)

1. Dans le conteneur qui s’affiche pour ce composant, modifiez le contenu du composant selon les besoins.

   ![](assets/web-designer-edit-html.png)

1. Ajustez les styles qui s’affichent à partir du **[!UICONTROL Container]** le volet de droite, comme l’arrière-plan, la couleur du texte, la bordure, la taille, la position, etc. ; selon le composant sélectionné.

   ![](assets/web-designer-html-style.png)

## Navigation dans le concepteur web

### Utilisation des chemins de navigation

1. Sélectionnez un élément dans la zone de travail.

1. Cliquez sur le bouton **[!UICONTROL Expand/Collapse Breadcrumbs]** dans le coin inférieur gauche de l’écran pour afficher rapidement les informations sur l’élément sélectionné.

   ![](assets/web-designer-breadcrumbs.png)

1. Lorsque vous passez la souris sur le chemin de navigation, l’élément correspondant est mis en surbrillance dans l’éditeur.

1. Vous pouvez facilement y accéder à n’importe quel élément parent, frère ou enfant dans l’éditeur visuel.

### Basculer vers le mode de navigation {#browse-mode}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_browse"
>title="Utilisation du mode de navigation"
>abstract="Dans ce mode, vous pouvez accéder à la page exacte à partir de la surface sélectionnée à personnaliser."

Vous pouvez passer de la valeur par défaut **[!UICONTROL Design]** en mode **[!UICONTROL Browse]** à l’aide du bouton dédié.

![](assets/web-designer-browse-mode.png)

Dans la **[!UICONTROL Browse]** , vous pouvez accéder à la page exacte à partir de la surface sélectionnée à personnaliser.

Elle est particulièrement utile lorsque vous traitez des pages qui se trouvent derrière l’authentification ou qui ne sont pas disponibles depuis le début à une certaine URL. Par exemple, vous pourrez vous authentifier, accéder à la page de votre compte ou à la page de votre panier, puis revenir à **[!UICONTROL Design]** pour effectuer les modifications sur la page souhaitée.

### Modification de la taille de l’appareil

Vous pouvez définir la taille de l’appareil sur une taille prédéfinie, telle que **[!UICONTROL Tablet]** ou **[!UICONTROL Mobile landscape]** ou définir une taille personnalisée. Saisissez le nombre de pixels souhaité pour définir une taille personnalisée.

Vous pouvez également modifier la mise au point du zoom, de 25 % à 400 %.

![](assets/web-designer-device.png)

## Gestion des modifications {#manage-modifications}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_modifications"
>title="Gérer facilement toutes vos modifications"
>abstract="Ce volet vous permet de parcourir et de gérer tous les réglages et styles ajoutés à votre page web."

Vous pouvez facilement gérer tous les composants, réglages et styles que vous avez ajoutés à votre page web.

1. Sélectionnez la **[!UICONTROL Modifications]** pour afficher le volet correspondant à gauche.

   ![](assets/web-designer-modifications-pane.png)

1. Vous pouvez passer en revue chacune des modifications que vous avez apportées à la page.

1. Sélectionnez une modification indésirable et cliquez sur l’icône de suppression pour la supprimer.

   ![](assets/web-designer-modifications-delete.png)

   >[!CAUTION]
   >
   >Procédez avec précaution lors de la suppression d’une action, car elle peut avoir un impact sur les actions suivantes.

1. Vous pouvez également annuler et rétablir des actions à l’aide de la variable **[!UICONTROL Undo/Redo]** en haut à droite de l’écran.

   ![](assets/web-designer-undo-redo.png)

   Cliquez sur le bouton et maintenez-le enfoncé pour passer de la **[!UICONTROL Undo]** et **[!UICONTROL Redo]** options. Cliquez ensuite sur le bouton lui-même pour appliquer l’action souhaitée.

## Ajout d’offres et de personnalisation

Pour ajouter de la personnalisation, sélectionnez un conteneur et l&#39;icône de personnalisation dans la barre de menus contextuelle qui s&#39;affiche. Ajoutez vos modifications à l&#39;aide de l&#39;éditeur d&#39;expression. [En savoir plus](../personalization/personalization-build-expressions.md)

![](assets/web-designer-personalization.png)

Utilisez la variable **[!UICONTROL Offer decision]** composant à insérer [offres](../offers/get-started/starting-offer-decisioning.md) dans vos pages web. Le processus est le même que lorsque [ajout d’une offre à un email](../email/add-offers-email.md). Elle tire parti de la gestion de la décision pour sélectionner la meilleure offre à fournir à vos clients.

![](assets/web-designer-offer.png)

## Tester la campagne web {#test-web-campaign}

>[!CONTEXTUALHELP]
>id="ajo_web_designer_preview"
>title="Prévisualiser votre expérience web"
>abstract="Effectuez une simulation de votre expérience web."

Pour afficher un aperçu de votre expérience web modifiée, procédez comme suit.

>[!CAUTION]
>
>Vous devez disposer de profils de test pour simuler les offres qui leur seront diffusées. Découvrez comment [créer des profils de test](../segment/creating-test-profiles.md).

1. À partir de **[!UICONTROL Edit content]** ou le concepteur web, sélectionnez **[!UICONTROL Simulate content]**.

   ![](assets/web-designer-simulate.png)

1. Cliquez sur **[!UICONTROL Manage test profiles]** pour sélectionner un ou plusieurs profils de test.
1. Un aperçu de la page web modifiée s’affiche.

   ![](assets/web-designer-preview.png)

1. Vous pouvez également copier l’URL de test pour la coller dans n’importe quel navigateur ou l’ouvrir dans le navigateur par défaut.
