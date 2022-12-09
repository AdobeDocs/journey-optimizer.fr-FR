---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser les composants de contenu du Concepteur d'email
description: Découvrez comment utiliser des composants de contenu dans vos emails
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: a4aaa814-3fd4-439e-8f34-faf97208378a
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '1256'
ht-degree: 0%

---

# Utilisation des composants de contenu du Concepteur d&#39;email {#content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components_email"
>title="À propos des composants de contenu"
>abstract="Les composants de contenu sont des espaces réservés de contenu vides que vous pouvez utiliser pour créer la mise en page d’un email."

>[!CONTEXTUALHELP]
>id="ac_content_components_landing_page"
>title="À propos des composants de contenu"
>abstract="Les composants de contenu sont des espaces réservés de contenu vides que vous pouvez utiliser pour créer la mise en page d’une landing page."

>[!CONTEXTUALHELP]
>id="ac_content_components_fragment"
>title="À propos des composants de contenu"
>abstract="Les composants de contenu sont des espaces réservés de contenu vides que vous pouvez utiliser pour créer la mise en page d’un fragment."

>[!CONTEXTUALHELP]
>id="ac_content_components_template"
>title="À propos des composants de contenu"
>abstract="Les composants de contenu sont des espaces réservés de contenu vides que vous pouvez utiliser pour créer la mise en page d’un modèle."

Lors de la création du contenu de votre email, **[!UICONTROL Content components]** vous permet de personnaliser davantage votre email avec des composants bruts que vous pouvez éditer une fois qu&#39;il a été placé dans un email.

Vous pouvez ajouter autant de composants de contenu que nécessaire dans un ou plusieurs composants de structure, qui définissent la disposition de votre email.

## Ajout de composants de contenu {#add-content-components}

Pour ajouter des composants de contenu à votre email et les ajuster à vos besoins, procédez comme suit.

1. Dans le Concepteur d&#39;email, utilisez un contenu existant ou effectuez un glisser-déposer. **[!UICONTROL Structure components]** dans votre contenu vide pour définir la mise en page de votre email. [Découvrez comment](content-from-scratch.md)

1. Pour accéder au **[!UICONTROL Content components]** , sélectionnez le bouton correspondant dans le volet de gauche du Concepteur d&#39;email.

   ![](assets/email_designer_content_components.png)

1. Faites glisser et déposez les composants de contenu de votre choix dans les composants de structure appropriés.

   ![](assets/email_designer_add_content_components.png)

   >[!NOTE]
   >
   >Vous pouvez ajouter plusieurs composants dans un seul composant de structure et dans chaque colonne d’un composant de structure.

1. Ajustez les attributs de style de chaque composant à l’aide de la fonction **[!UICONTROL Component settings]** sur la droite. Par exemple, vous pouvez modifier le style de texte, la marge ou la marge intérieure de chaque composant. [En savoir plus sur l’alignement et la marge intérieure](alignment-and-padding.md)

   ![](assets/email_designer_content_components_settings.png)

## Conteneur {#container}

Vous pouvez ajouter un conteneur simple à l’intérieur duquel vous pourrez ajouter un autre composant de contenu. Vous pouvez ainsi appliquer un style spécifique au conteneur, qui sera différent du composant utilisé à l’intérieur.

Par exemple, ajoutez une **[!UICONTROL Container]** , puis ajoutez une [Bouton](#button) à l’intérieur de ce conteneur. Vous pouvez utiliser un arrière-plan spécifique pour le conteneur et un autre pour le bouton.

![](assets/email_designer_container_component.png)

## Bouton {#button}

Utilisez la variable **[!UICONTROL Button]** pour insérer un ou plusieurs boutons dans votre email et rediriger votre audience de courrier électronique vers une autre page.

1. De **[!UICONTROL Content components]**, effectuez un glisser-déposer de la variable **[!UICONTROL Button]** dans un composant **[!UICONTROL Structure component]**.

1. Cliquez sur le bouton que vous venez d’ajouter pour personnaliser le texte et avoir accès au **[!UICONTROL Components settings]** dans le volet de droite du Concepteur d’email .

   ![](assets/email_designer_button_component.png)

1. Dans le **[!UICONTROL Link]** ajoutez l’URL vers laquelle vous souhaitez rediriger lorsque vous cliquez sur le bouton.

1. Choisissez la manière dont votre audience sera redirigée avec la variable **[!UICONTROL Target]** liste déroulante :

   * **[!UICONTROL None]**: ouvre le lien dans le même cadre que celui sur lequel l’utilisateur a cliqué (par défaut).
   * **[!UICONTROL Blank]**: ouvre le lien dans une nouvelle fenêtre ou un nouvel onglet.
   * **[!UICONTROL Self]**: ouvre le lien dans le même cadre que celui sur lequel l’utilisateur a cliqué.
   * **[!UICONTROL Parent]**: ouvre le lien dans le cadre parent.
   * **[!UICONTROL Top]**: ouvre le lien dans le corps complet de la fenêtre.

   ![](assets/email_designer_button_link.png)

1. Vous pouvez personnaliser davantage votre bouton en modifiant les attributs de style, tels que **[!UICONTROL Border]**, **[!UICONTROL Size]**, **[!UICONTROL Margin]**, etc. de la **[!UICONTROL Component settings]** volet.

## Texte {#text}

Utilisez la variable **[!UICONTROL Text]** pour insérer du texte dans votre email et ajuster le style (bordure, taille, remplissage, etc.) en utilisant la variable **[!UICONTROL Component settings]** volet.

![](assets/email_designer_text_component.png)

1. De **[!UICONTROL Content components]**, effectuez un glisser-déposer de la variable **[!UICONTROL Text]** dans un composant **[!UICONTROL Structure component]**.

1. Cliquez sur le composant que vous venez d’ajouter pour personnaliser le texte et accéder à la fonction **[!UICONTROL Components Settings]** dans le volet droit du Concepteur d’email.

1. Modifiez votre texte avec les options suivantes disponibles dans la barre d’outils :

   ![](assets/email_designer_27.png)

   * **[!UICONTROL Change text style]**: appliquez le style gras, italique, souligné ou faites passer le pointeur de la souris sur votre texte.
   * **Modifier l’alignement**: sélectionnez l’alignement gauche, droite, centré ou justifié de votre texte.
   * **[!UICONTROL Create list]**: ajoutez une liste à puces ou de nombres à votre texte.
   * **[!UICONTROL Set heading]**: ajoutez jusqu’à six niveaux d’en-tête à votre texte.
   * **Taille de police**: sélectionnez la taille de police de votre texte en pixels.
   * **[!UICONTROL Edit image]**: ajoutez une image ou une ressource à votre composant de texte. [En savoir plus sur la gestion des ressources](assets-essentials.md)
   * **[!UICONTROL Show the source code]**: afficher le code source de votre texte. Il ne peut pas être modifié.
   * **[!UICONTROL Duplicate]**: ajoutez une copie de votre composant de texte.
   * **[!UICONTROL Delete]**: supprimez le composant de texte sélectionné de votre email.
   * **[!UICONTROL Add personalization]**: ajoutez des champs de personnalisation pour personnaliser le contenu des données de vos profils. [En savoir plus sur la personnalisation du contenu](../personalization/personalize.md)
   * **[!UICONTROL Enable conditional content]**: ajoutez du contenu conditionnel pour adapter le contenu du composant aux profils ciblés. [En savoir plus sur le contenu dynamique](../personalization/get-started-dynamic-content.md)

1. Ajustez les autres attributs de style tels que la couleur du texte, la famille de polices, la bordure, la marge intérieure, la marge, etc. de la **[!UICONTROL Component settings]** volet.

## Diviseur {#divider}

Utilisez la variable **[!UICONTROL Divider]** pour insérer une ligne de séparation afin d&#39;organiser la mise en page et le contenu de votre email.

Vous pouvez ajuster les attributs de style, tels que la couleur de la ligne, le style et la hauteur, à partir du **[!UICONTROL Component settings]** volet.

![](assets/email_designer_divider.png)

## HTML {#HTML}

Utilisez la variable **[!UICONTROL HTML]** pour copier-coller les différentes parties du code HTML existant. Vous pouvez ainsi créer des composants HTML modulaires gratuits pour réutiliser du contenu externe.

1. De **[!UICONTROL Content Components]**, effectuez un glisser-déposer de la variable **[!UICONTROL HTML]** dans un composant **[!UICONTROL Structure component]**.

1. Cliquez sur le composant que vous venez d’ajouter, puis sélectionnez **[!UICONTROL Show the source code]** dans la barre d’outils contextuelle pour ajouter votre code HTML.

   ![](assets/email_designer_html_component.png)

1. Copiez-collez le code HTML à ajouter à votre email, puis cliquez sur **[!UICONTROL Save]**.

   ![](assets/email_designer_html_content.png)

>[!NOTE]
>
>Pour simplement rendre un contenu externe compatible avec le Concepteur d&#39;email, Adobe recommande de créer entièrement un message et de copier le contenu de votre email existant dans des composants.

## Image {#image}

Utilisez la variable **[!UICONTROL Image]** pour insérer un fichier image de votre ordinateur dans le contenu de votre email.

1. De **[!UICONTROL Content components]**, effectuez un glisser-déposer de la variable **[!UICONTROL Image]** dans un composant **[!UICONTROL Structure component]**.

1. Cliquez sur **[!UICONTROL Browse]** pour choisir un fichier image parmi vos ressources.

   Pour en savoir plus sur [!DNL Assets Essentials], voir [Documentation sur Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html){target=&quot;_blank&quot;}.

1. Cliquez sur le composant que vous venez d’ajouter et configurez vos propriétés d’image à l’aide de la fonction **[!UICONTROL Components settings]** Volet :

   * **[!UICONTROL Image title]** vous permet de définir un titre pour votre image.
   * **[!UICONTROL Alt text]** permet de définir la légende associée à votre image. Cela correspond à l’attribut HTML alt.

   ![](assets/email_designer_10.png)

1. Ajustez les autres attributs de style tels que la marge, la bordure, etc. ou ajouter un lien pour rediriger votre audience vers un autre contenu de la **[!UICONTROL Component settings]** volet.

## Vidéo {#Video}

>[!CONTEXTUALHELP]
>id="ac_edition_video_email"
>title="Paramètres vidéo"
>abstract="Utilisez ce composant pour insérer une vidéo dans votre email. Notez que les vidéos ne fonctionnent pas sur tous les clients de messagerie. Nous vous conseillons de définir une image de secours."

>[!CONTEXTUALHELP]
>id="ac_edition_video_landing_page"
>title="Paramètres vidéo"
>abstract="Utilisez ce composant pour insérer une vidéo dans votre landing page. Notez que les vidéos ne fonctionnent pas sur tous les clients de messagerie. Nous vous conseillons de définir une image de secours."

>[!CONTEXTUALHELP]
>id="ac_edition_video_fragment"
>title="Paramètres vidéo"
>abstract="Utilisez ce composant pour insérer une vidéo dans votre fragment. Notez que les vidéos ne fonctionnent pas sur tous les clients de messagerie. Nous vous conseillons de définir une image de secours."

>[!CONTEXTUALHELP]
>id="ac_edition_video_template"
>title="Paramètres vidéo"
>abstract="Utilisez ce composant pour insérer une vidéo dans votre modèle. Notez que les vidéos ne fonctionnent pas sur tous les clients de messagerie. Nous vous conseillons de définir une image de secours."

Utilisez la variable **[!UICONTROL Video]** pour insérer une vidéo dans le contenu de votre email par le biais d’un lien URL.

1. De **[!UICONTROL Content Components]**, effectuez un glisser-déposer de la variable **[!UICONTROL Video]** dans une **[!UICONTROL Structure component]**.

   ![](assets/email_designer_17.png)

1. Cliquez sur le composant que vous venez d’ajouter.

1. Dans le **[!UICONTROL Video link]** du champ **[!UICONTROL Components settings]** ajoutez l’URL de la vidéo.

   ![](assets/email_designer_18.png)

1. Vous pouvez ajouter une **[!UICONTROL Poster image]** à votre vidéo afin de spécifier une image à afficher jusqu’à ce que votre audience clique sur le bouton de lecture .

1. Ajustez les autres attributs de style tels que le style, la marge, la bordure, etc. de la **[!UICONTROL Component settings]** volet.

## Social {#social}

Utilisez la variable **[!UICONTROL Social]** pour insérer des liens vers des pages de médias sociaux dans le contenu de votre email.

1. De **[!UICONTROL Content Components]**, effectuez un glisser-déposer de la variable **[!UICONTROL Social]** dans un composant **[!UICONTROL Structure component]**.

1. Cliquez sur le composant que vous venez d’ajouter.

1. Dans le **[!UICONTROL Social]** du champ **[!UICONTROL Components settings]** , sélectionnez les médias sociaux à ajouter ou à supprimer.

   ![](assets/email_designer_20.png)

1. Sélectionnez la taille de vos icônes dans le champ dédié.

1. Cliquez sur chacune de vos icônes de médias sociaux pour configurer la variable **[!UICONTROL URL]** vers laquelle votre audience sera redirigée.

   ![](assets/email_designer_21.png)

1. Vous pouvez également modifier les icônes de chacun de vos médias sociaux si nécessaire dans la variable **[!UICONTROL Image]** champ .

1. Ajustez les autres attributs de style tels que le style, la marge, la bordure, etc. de la **[!UICONTROL Component settings]** volet.

## Décision sur l’offre {#offer-decision}

Utilisez la variable **[!UICONTROL Offer decision]** pour insérer des offres dans vos messages. Le [gestion des décisions](../offers/get-started/starting-offer-decisioning.md) Le moteur choisira la meilleure offre à diffuser à vos clients.

Découvrez comment ajouter des offres personnalisées dans un email dans [cette section](add-offers-email.md).

