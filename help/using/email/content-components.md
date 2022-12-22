---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser les composants de contenu du Concepteur d’email
description: Découvrez comment utiliser les composants de contenu dans vos e-mails
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: a4aaa814-3fd4-439e-8f34-faf97208378a
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: ht
source-wordcount: '1380'
ht-degree: 100%

---

# Utilisez les composants de contenu du concepteur d’e-mail. {#content-components}

>[!CONTEXTUALHELP]
>id="ac_content_components_email"
>title="À propos des composants de contenu"
>abstract="Les composants de contenu sont des espaces réservés de contenu vides que vous pouvez utiliser pour créer la disposition d&#39;un email."

>[!CONTEXTUALHELP]
>id="ac_content_components_landing_page"
>title="À propos des composants de contenu"
>abstract="Les composants de contenu sont des espaces réservés de contenu vides que vous pouvez utiliser pour créer la disposition d’une page de destination."

>[!CONTEXTUALHELP]
>id="ac_content_components_fragment"
>title="À propos des composants de contenu"
>abstract="Les composants de contenu sont des espaces réservés de contenu vides que vous pouvez utiliser pour créer la disposition d’un fragment."

>[!CONTEXTUALHELP]
>id="ac_content_components_template"
>title="À propos des composants de contenu"
>abstract="Les composants de contenu sont des espaces réservés de contenu vides que vous pouvez utiliser pour créer la disposition d’un modèle."

Lorsque vous créez le contenu de votre e-mail, la section **[!UICONTROL Composants de contenu]** vous permet de personnaliser davantage votre e-mail à l’aide des composants bruts que vous pouvez modifier une fois placés dans un e-mail.

Vous pouvez ajouter autant de composants de contenu que nécessaire dans un ou plusieurs composants de structure, ce qui permet de définir la disposition de votre e-mail.

## Ajouter des composants de contenu {#add-content-components}

Pour ajouter des composants de contenu à votre e-mail et les ajuster selon vos besoins, suivez les étapes ci-dessous.

1. Dans le concepteur d’e-mail, utilisez un contenu existant ou faites glisser et déposez la section **[!UICONTROL Composants de structure]** dans votre contenu vide pour définir la disposition de votre e-mail. [Voici comment procéder](content-from-scratch.md)

1. Pour accéder à la section **[!UICONTROL Composants de contenu]**, sélectionnez le bouton correspondant dans le volet gauche du concepteur d’e-mail.

   ![](assets/email_designer_content_components.png)

1. Faites glisser et déposez les composants de contenu de votre choix dans les composants de structure appropriés.

   ![](assets/email_designer_add_content_components.png)

   >[!NOTE]
   >
   >Vous pouvez ajouter plusieurs composants dans un seul composant de structure et dans chaque colonne d’un composant de structure.

1. Ajustez les attributs de style de chaque composant à l’aide du volet **[!UICONTROL Paramètres des composants]** sur la droite. Par exemple, vous pouvez changer le style de texte, la marge intérieure ou la marge de chaque composant. [En savoir plus sur l’alignement et la marge intérieure](alignment-and-padding.md)

   ![](assets/email_designer_content_components_settings.png)

## Conteneur {#container}

Vous pouvez ajouter un conteneur simple à l’intérieur duquel vous pourrez ajouter un autre composant de contenu. Vous pouvez ainsi appliquer un style spécifique au conteneur, qui sera différent du composant utilisé à l’intérieur.

Par exemple, ajoutez un composant **[!UICONTROL Conteneur]**, puis ajoutez un composant [Bouton](#button) à l’intérieur de ce conteneur. Vous pouvez utiliser un arrière-plan spécifique pour le conteneur et un autre pour le bouton.

![](assets/email_designer_container_component.png)

## Bouton {#button}

Utilisez le composant **[!UICONTROL Bouton]** pour insérer un ou plusieurs boutons dans votre e-mail et rediriger votre audience d’e-mail vers une autre page.

1. À partir de la section **[!UICONTROL Composants de contenu]**, faites glisser et déposez le composant **[!UICONTROL Bouton]** dans un **[!UICONTROL composant de structure]**.

1. Cliquez sur votre bouton nouvellement ajouté pour personnaliser le texte et accéder aux **[!UICONTROL Paramètres des composants]** dans le volet droit du Concepteur d’e-mail.

   ![](assets/email_designer_button_component.png)

1. Dans le champ **[!UICONTROL Lien]**, ajoutez l’URL vers laquelle vous souhaitez rediriger lors d’un clic sur le bouton.

1. Choisissez comment votre audience sera redirigée avec la liste déroulante **[!UICONTROL Cible]** :

   * **[!UICONTROL Aucune]** : ouvre le lien dans le même cadre que celui sur lequel l’utilisateur a cliqué (par défaut).
   * **[!UICONTROL Vierge]** : ouvre le lien dans une nouvelle fenêtre ou un nouvel onglet.
   * **[!UICONTROL Self]** : ouvre le lien dans le même cadre que celui sur lequel l’utilisateur a cliqué.
   * **[!UICONTROL Parent]** : ouvre le lien dans le cadre parent.
   * **[!UICONTROL Haut]** : ouvre le lien dans le corps complet de la fenêtre.

   ![](assets/email_designer_button_link.png)

1. Vous pouvez personnaliser davantage votre bouton en modifiant les attributs de style, tels que la **[!UICONTROL bordure]**, la **[!UICONTROL taille]**, la **[!UICONTROL marge]**, etc. à partir du volet **[!UICONTROL Paramètres des composants]**.

## Texte {#text}

Utilisez le composant **[!UICONTROL Texte]** pour insérer du texte dans votre e-mail et ajuster le style (bordure, taille, marge intérieure, etc.) en utilisant le volet **[!UICONTROL Paramètres des composants]**.

![](assets/email_designer_text_component.png)

1. À partir des **[!UICONTROL composants de contenu]**, faites glisser et déposez le composant de **[!UICONTROL texte]** dans un **[!UICONTROL composant de structure]**.

1. Cliquez sur votre composant nouvellement ajouté pour personnaliser le texte et accéder aux **[!UICONTROL paramètres des composants]** dans le volet droit du concepteur d’e-mail.

1. Modifiez votre texte à l’aide des options suivantes disponibles dans la barre d’outils :

   ![](assets/email_designer_27.png)

   * **[!UICONTROL Modifier le style de texte]** : appliquez des caractères gras, italiques, soulignés ou barrés à votre texte.
   * **Modifier l&#39;alignement** : choisissez entre l’alignement à gauche, à droite, centré ou justifié pour votre texte.
   * **[!UICONTROL Créer une liste]** : ajoutez une puce ou une liste numérique à votre texte.
   * **[!UICONTROL Définir le titre]** : ajoutez jusqu&#39;à six niveaux d&#39;en-tête à votre texte.
   * **Taille de police** : sélectionnez la taille de police de votre texte en pixels.
   * **[!UICONTROL Modifier l&#39;image]** : ajoutez une image ou une ressource à votre composant de texte. [En savoir plus sur la gestion des ressources](assets-essentials.md)
   * **[!UICONTROL Afficher le code source]** : affichez le code source de votre texte. Ceci ne peut pas être modifié.
   * **[!UICONTROL Dupliquer]** : ajoutez une copie de votre composant de texte.
   * **[!UICONTROL Supprimer]** : supprimez le composant de texte sélectionné de votre e-mail.
   * **[!UICONTROL Ajouter une personnalisation]** : ajoutez des champs de personnalisation pour personnaliser le contenu à partir des données de vos profils. [En savoir plus sur la personnalisation de contenu](../personalization/personalize.md)
   * **[!UICONTROL Activer le contenu conditionnel]** : ajoutez du contenu conditionnel pour adapter le contenu du composant aux profils ciblés. [En savoir plus sur le contenu dynamique](../personalization/get-started-dynamic-content.md)

1. Ajustez les autres attributs de style, tels que la couleur du texte, la famille de polices, la bordure, la marge intérieure, la marge, etc. à partir du volet **[!UICONTROL Paramètres des composants]**.

## Diviseur {#divider}

Utilisez le composant **[!UICONTROL Diviseur]** pour insérer une ligne de séparation afin d’organiser la disposition et le contenu de votre e-mail.

Vous pouvez ajuster les attributs de style, tels que la couleur, le style et la hauteur des lignes à partir du volet **[!UICONTROL Paramètres des composants]**.

![](assets/email_designer_divider.png)

## HTML {#HTML}

Utilisez le composant **[!UICONTROL HTML]** pour copier-coller les différentes parties de votre code HTML existant. Vous pouvez ainsi créer des composants HTML modulaires autonomes afin de réutiliser du contenu externe.

1. À partir de **[!UICONTROL Composants de contenu]**, faites glisser le composant **[!UICONTROL HTML]** et déposez-le dans un **[!UICONTROL composant de structure]**.

1. Cliquez sur votre nouveau composant ajouté, puis sélectionnez **[!UICONTROL Afficher le code source]** dans la barre d’outils contextuelle pour ajouter votre code HTML.

   ![](assets/email_designer_html_component.png)

1. Copiez-collez le code HTML à ajouter à votre e-mail et cliquez sur **[!UICONTROL Enregistrer]**.

   ![](assets/email_designer_html_content.png)

>[!NOTE]
>
>Pour rendre un contenu externe compatible avec le Concepteur d’e-mail, Adobe recommande de créer entièrement un message et de copier le contenu de votre e-mail existant dans des composants.

## Image {#image}

Utilisez le composant **[!UICONTROL Image]** pour insérer un fichier image de votre ordinateur dans le corps de votre e-mail.

1. À partir de **[!UICONTROL Composants de contenu]**, faites glisser le composant **[!UICONTROL Image]** et déposez-le dans un **[!UICONTROL composant de structure]**.

1. Cliquez sur **[!UICONTROL Parcourir]** pour choisir un fichier image dans vos ressources.

   Pour en savoir plus sur [!DNL Assets Essentials], consultez la [documentation Adobe Experience Manager Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/introduction.html?lang=fr){target=&quot;_blank&quot;}.

1. Cliquez sur le nouveau composant ajouté et configurez les propriétés de votre image à l’aide du volet **[!UICONTROL Paramètres des composants]** :

   * **[!UICONTROL Titre d’image]** vous permet de définir un titre pour votre image.
   * **[!UICONTROL Text alt]** vous permet de définir la légende liée à votre image. Cela correspond à l’attribut alt en HTML.

   ![](assets/email_designer_10.png)

1. Ajustez les autres attributs de style tels que la marge, la bordure, etc. ou ajoutez un lien pour rediriger votre audience vers un autre contenu à partir du volet **[!UICONTROL Paramètres des composants]**.

## Vidéo {#Video}

>[!CONTEXTUALHELP]
>id="ac_edition_video_email"
>title="Paramètres vidéo"
>abstract="Utilisez ce composant pour insérer une vidéo dans votre email. Notez que les vidéos ne fonctionnent pas sur tous les clients de messagerie. Nous vous conseillons de définir une image de remplacement."

>[!CONTEXTUALHELP]
>id="ac_edition_video_landing_page"
>title="Paramètres vidéo"
>abstract="Utilisez ce composant pour insérer une vidéo dans votre page de destination. Notez que les vidéos ne fonctionnent pas sur tous les clients de messagerie. Nous vous conseillons de définir une image de remplacement."

>[!CONTEXTUALHELP]
>id="ac_edition_video_fragment"
>title="Paramètres vidéo"
>abstract="Utilisez ce composant pour insérer une vidéo dans votre fragment. Notez que les vidéos ne fonctionnent pas sur tous les clients de messagerie. Nous vous conseillons de définir une image de remplacement."

>[!CONTEXTUALHELP]
>id="ac_edition_video_template"
>title="Paramètres vidéo"
>abstract="Utilisez ce composant pour insérer une vidéo dans votre modèle. Notez que les vidéos ne fonctionnent pas sur tous les clients de messagerie. Nous vous conseillons de définir une image de remplacement."

Utilisez le composant **[!UICONTROL Vidéo]** pour insérer une vidéo dans le corps de votre e-mail via un lien URL.

1. À partir de **[!UICONTROL Composants de contenu]**, faites glisser le composant **[!UICONTROL Vidéo]** et déposez-le dans un **[!UICONTROL composant de structure]**.

   ![](assets/email_designer_17.png)

1. Cliquez sur le composant que vous venez d’ajouter.

1. Dans le champ **[!UICONTROL Lien vidéo]** du volet **[!UICONTROL Paramètres des composants]**, ajoutez l’URL de votre vidéo.

   ![](assets/email_designer_18.png)

1. Vous pouvez ajouter une **[!UICONTROL image d’affichage]** à votre vidéo pour spécifier une image à afficher jusqu’à ce que votre audience clique sur le bouton de lecture.

1. Ajustez les autres attributs de style tels que le style, la marge, la bordure, etc. à partir du volet **[!UICONTROL Paramètres des composants]**.

## Social {#social}

Utilisez le composant **[!UICONTROL Social]** pour insérer des liens vers des pages de réseaux sociaux dans le corps de votre e-mail.

1. À partir de **[!UICONTROL Composants de contenu]**, faites glisser le composant **[!UICONTROL Social]** et déposez-le dans un **[!UICONTROL composant de structure]**.

1. Cliquez sur le composant que vous venez d’ajouter.

1. Dans le champ **[!UICONTROL Social]** du volet **[!UICONTROL Paramètres des composants]**, sélectionnez le réseau social que vous souhaitez ajouter ou supprimer.

   ![](assets/email_designer_20.png)

1. Sélectionnez la taille de vos icônes dans le champ dédié.

1. Cliquez sur chacune des icônes de vos réseaux sociaux pour configurer l’**[!UICONTROL URL]** vers laquelle votre audience sera redirigée.

   ![](assets/email_designer_21.png)

1. Vous pouvez également modifier les icônes de chacun de vos réseaux sociaux si nécessaire dans le champ **[!UICONTROL Image]**.

1. Ajustez les autres attributs de style tels que le style, la marge, la bordure, etc. à partir du volet **[!UICONTROL Paramètres des composants]**.

## Décision d’offre {#offer-decision}

Utilisez le composant **[!UICONTROL Décision d’offre]** pour insérer des offres dans vos messages. Le moteur [Gestion des décisions](../offers/get-started/starting-offer-decisioning.md) choisira la meilleure offre à proposer à votre clientèle.

Découvrez comment ajouter des offres personnalisées dans un e-mail dans [cette section](add-offers-email.md).

