---
title: Concevoir votre contenu in-app
description: Découvrez comment concevoir votre contenu in-app dans Journey Optimizer.
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 7d7aa721-96aa-4ebc-a51c-e693f893f34f
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: ht
source-wordcount: '866'
ht-degree: 100%

---

# Concevoir votre contenu in-app {#design-content}

Vous pouvez modifier le contenu in-app pour configurer les options d’expérience, notamment la disposition et l’affichage du message, le texte et les options de bouton.

Pour configurer le contenu du message, cliquez sur le bouton **[!UICONTROL Modifier le contenu]** et utilisez les options de la section droite de l’écran pour concevoir le contenu de votre message in-app.

![](assets/edit-in-app-content.png)

Le bouton **[!UICONTROL Formatage avancé]** active des options supplémentaires pour personnaliser l’expérience.

Une fois votre message in-app créé et son contenu défini et personnalisé, vous pouvez le vérifier et l’activer. Les notifications seront alors envoyées conformément au planning de la campagne. En savoir plus sur [cette page](create-in-app.md#in-app-send).

## Disposition des messages {#message-layout}

Dans la section **[!UICONTROL Disposition des messages]**, sélectionnez l’une des quatre options de disposition différentes en fonction de vos besoins en matière de messagerie.

![](assets/in_app_content_1.png)

* **[!UICONTROL Plein écran]** : ce type de disposition couvre tout l’écran des appareils de votre audience.

   Elle prend en charge des composants multimédia (image, vidéo), texte et bouton.

* **[!UICONTROL Modal]** : cette disposition apparaît dans une grande fenêtre de style alerte. Votre application est toujours visible en arrière-plan.

   Elle prend en charge des composants multimédia (image, vidéo), texte et bouton.

* **[!UICONTROL Bannière]** : ce type de disposition apparaît comme message d’alerte natif du système d’exploitation.

   Vous pouvez uniquement ajouter un **[!UICONTROL En-tête]** et un **[!UICONTROL Corps]** à votre message.

* **[!UICONTROL Personnalisé]** : le mode message personnalisé permet d’importer et de modifier directement l’un de vos messages HTML préconfigurés.

   * Sélectionnez **[!UICONTROL Composer]** pour saisir ou coller votre code HTML brut.

      Utilisez le volet de gauche pour tirer parti des fonctionnalités de personnalisation de Journey Optimizer. Voir à ce propos [cette section](../personalization/personalize.md).

   * Sélectionnez **[!UICONTROL Importer]** pour importer le fichier HTML ou .zip contenant votre contenu HTML.

## Onglet Contenu {#content-tab}

Dans l’onglet **Contenu**, vous pouvez définir et personnaliser les éléments suivants : le contenu de la notification et le style du bouton **Fermer**. Vous pouvez également ajouter un média à votre notification in-app et ajouter des boutons d’action depuis cet onglet.

### Bouton Fermer {#close-button}

![](assets/in_app_content_2.png)

Choisissez le **[!UICONTROL Style]** de votre **[!UICONTROL Bouton Fermer]**.

Les styles disponibles sont les suivants :

* **[!UICONTROL Simple]**
* **[!UICONTROL Cercle]**
* **[!UICONTROL Image personnalisée]** à partir d’une URL de média ou de vos ressources.

+++Plus d’options avec Formatage avancé

Si le **[!UICONTROL Mode de formatage avancé]** est activé, vous pouvez vérifier l’option **[!UICONTROL Couleur]** pour choisir la couleur et l’opacité de votre bouton.

+++

### Média {#add-media}

Le champ **[!UICONTROL Média]** permet d’ajouter des médias à votre message in-app afin de créer une expérience attrayante pour l’utilisateur final.

![](assets/in_app_content_3.png)

Saisissez votre URL de média ou cliquez sur l’icône **[!UICONTROL Sélectionner les ressources]** pour ajouter directement des ressources stockées dans votre bibliothèque de ressources à votre message in-app. [En savoir plus sur la gestion des ressources](../design/assets-essentials.md).
Vous pouvez également ajouter un **[!UICONTROL Texte secondaire]** pour les applications de lecture d’écran.

+++Plus d’options avec Formatage avancé

Si le **[!UICONTROL Mode de formatage avancé]** est activé, vous pouvez personnaliser la **[!UICONTROL Hauteur maximale]** et la **[!UICONTROL Largeur maximale]** de vos médias.

+++

### En-tête et corps {#title-body}

Pour composer votre message, saisissez le contenu dans les champs **[!UICONTROL En-tête]** et **[!UICONTROL Corps]**.

![](assets/in_app_content_4.png)

Utilisez l’icône **[!UICONTROL Personnalisation]** pour ajouter de la personnalisation. En savoir plus sur la personnalisation avec l’éditeur d’expression d’Adobe Journey Optimizer [dans cette section](../personalization/personalize.md).

+++Plus d’options avec Formatage avancé

Si le **[!UICONTROL Mode de formatage avancé]** est activé, vous pouvez choisir les éléments suivants pour votre **[!UICONTROL En-tête]** et votre **[!UICONTROL Corps]** :

* la **[!UICONTROL Police]**
* la **[!UICONTROL Taille du point]**
* la **[!UICONTROL Couleur de la police]**
* l’**[!UICONTROL Alignement]**
+++

### Boutons {#add-buttons}

Ajoutez des boutons pour que les utilisateurs et utilisatrices puissent interagir avec votre message in-app.

![](assets/in_app_content_5.png)

Pour personnaliser votre bouton :

1. Modifiez le champ texte Bouton #1 (principal). Vous pouvez également utiliser l’icône **[!UICONTROL Personnalisation]** pour définir le contenu et les données de personnalisation.

1. Choisissez votre **[!UICONTROL Événement d’interaction]**, lequel définit l’action du bouton une fois que les utilisateurs et utilisatrices ont interagi avec celui-ci.

1. Entrez votre URL web ou votre lien profond dans le champ **[!UICONTROL Cible]**.

1. Pour ajouter plusieurs boutons, cliquez sur **[!UICONTROL Ajouter un bouton]**.

+++Plus d’options avec Formatage avancé

Si le **[!UICONTROL Mode de formatage avancé]** est activé, vous pouvez choisir les éléments suivants pour vos **[!UICONTROL Boutons]** :

* la **[!UICONTROL Police]**
* la **[!UICONTROL Taille du point]**
* la **[!UICONTROL Couleur de la police]**
* l’**[!UICONTROL Alignement]**
* le **[!UICONTROL Style de bouton]**
* le **[!UICONTROL Rayon]**
* la **[!UICONTROL Couleur du bouton]**

+++

## Paramètres  onglet {#settings-tab}

Dans l’onglet **Paramètres**, vous pouvez définir la disposition du message et prévisualiser votre message in-app. Vous pouvez également accéder à des options de formatage avancé.

### Prévisualisation {#preview-tab}

![](assets/in_app_content_6.png)

La **[!UICONTROL Prévisualisation de l’application]** vous permet d’ajouter un arrière-plan derrière votre message in-app :

* Un média provenant d’un lien URL.

* Une ressource de votre bibliothèque de ressources.

* Une couleur d’arrière-plan.

### Disposition {#layout-options}

![](assets/in_app_content_7.png)

Le champ **[!UICONTROL Image d’arrière-plan]** vous permet d’ajouter un arrière-plan à votre message in-app :

* Un média provenant d’un lien URL.

* Une couleur d’arrière-plan.

### Message {#message-tab}

![](assets/in_app_content_8.png)

L’option de prise de contrôle de l’interface utilisateur, activée par défaut, vous permet d’assombrir l’arrière-plan derrière votre message in-app pour mettre l’accent sur votre contenu.

+++Plus d’options avec Formatage avancé

Si le **[!UICONTROL Mode de formatage avancé]** est activé, vous pouvez personnaliser davantage votre message à l’aide des options suivantes :

* **[!UICONTROL Personnaliser les mouvements]** : vous permet de personnaliser l’interaction de balayage des utilisateurs et utilisatrices. Si l’option Ignorer est sélectionnée, vous pouvez ajouter un événement d’interaction personnalisé et/ou une destination cible.

* **[!UICONTROL Personnaliser la prise de contrôle de l’interface utilisateur]** : vous permet de sélectionner une couleur à afficher en arrière-plan et son opacité.

* **[!UICONTROL Personnaliser la taille]** : vous permet d’ajuster la largeur et la hauteur de votre notification in-app.

* **[!UICONTROL Personnaliser la position]** : vous permet de personnaliser la position de vos messages in-app sur l’écran des utilisateurs et utilisatrices. Vous pouvez modifier les alignements vertical et horizontal.

* **[!UICONTROL Personnaliser l’animation]** : vous permet de personnaliser vos animations d’affichage et d’ignorance, par exemple si votre notification in-app apparaît depuis la gauche ou la partie supérieure de l’appareil des utilisateurs et utilisatrices.

* **[!UICONTROL Coin arrondi du message]** : vous permet d’ajouter un coin arrondi à votre notification in-app en modifiant le **[!UICONTROL Rayon]**.

+++

**Rubriques connexes :**

* [Créer un message in-app](create-in-app.md)
* [Rapport in-app](inapp-report.md)
* [Configuration in-app](inapp-configuration.md)
