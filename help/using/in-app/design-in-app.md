---
title: Concevoir le contenu in-app
description: Découvrez comment concevoir du contenu In-App dans Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: 7d7aa721-96aa-4ebc-a51c-e693f893f34f
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '772'
ht-degree: 0%

---

# Concevoir le contenu in-app {#design-content}

Vous pouvez modifier le contenu in-app pour configurer les options d’expérience, notamment la disposition et l’affichage du message, le texte et les options de bouton.

Pour configurer le contenu du message, cliquez sur le bouton **[!UICONTROL Edit content]** et utilisez les options de la section droite de l&#39;écran pour concevoir le contenu de votre message in-app.

![](assets/edit-in-app-content.png)

Le **[!UICONTROL Advanced formatting]** activer/désactiver active des options supplémentaires pour personnaliser l’expérience.

Une fois votre message in-app créé et son contenu défini et personnalisé, vous pouvez le consulter et l’activer. Les notifications seront alors envoyées conformément au planning de la campagne. En savoir plus dans [cette page](create-in-app.md#in-app-send).

## Disposition des messages {#message-layout}

Dans la **[!UICONTROL Message Layout]** sélectionnez l’une des quatre options de mise en page différentes en fonction de vos besoins en matière de messagerie.

![](assets/in_app_content_1.png)

* **[!UICONTROL Fullscreen]**: Ce type de disposition couvre tout l’écran des appareils de votre audience.

   Il prend en charge les composants média (image, vidéo), texte et bouton.

* **[!UICONTROL Modal]**: Cette disposition apparaît dans une grande fenêtre de style alerte. Votre application est toujours visible en arrière-plan.

   Il prend en charge les composants média (image, vidéo), texte et bouton.

* **[!UICONTROL Banner]**: Ce type de disposition apparaît comme message d’alerte du système d’exploitation natif.

   Vous pouvez uniquement ajouter une **[!UICONTROL Header]** et un **[!UICONTROL Body]** à votre message.

* **[!UICONTROL Custom]**: Le mode Message personnalisé vous permet d&#39;importer et d&#39;éditer directement l&#39;un de vos messages HTML préconfigurés.

   * Sélectionner **[!UICONTROL Compose]** pour saisir ou coller votre code HTML brut.

      Utilisez le volet de gauche pour tirer parti des fonctionnalités de personnalisation de Journey Optimizer. Voir à ce sujet la section [cette section](../personalization/personalize.md).

   * Sélectionner **[!UICONTROL Import]** pour importer le fichier HTML ou .zip contenant votre contenu HTML.

## Onglet Contenu {#content-tab}

Dans la **Contenu** vous pouvez définir et personnaliser les éléments suivants : le contenu de la notification et le style de la **Fermer** bouton . Vous pouvez également ajouter un média à votre notification in-app et ajouter des boutons d’action depuis cet onglet.

### Bouton Fermer {#close-button}

![](assets/in_app_content_2.png)

Choisissez la **[!UICONTROL Style]** de votre **[!UICONTROL Close button]**.

Les styles disponibles sont les suivants :

* **[!UICONTROL Simple]**
* **[!UICONTROL Circle]**
* **[!UICONTROL Custom image]** à partir d’une URL de média ou de vos ressources.

+++ Plus d’options avec mise en forme avancée

Si la variable **[!UICONTROL Advanced formatting mode]** est activé, vous pouvez vérifier la variable **[!UICONTROL Color]** pour choisir la couleur et l’opacité de votre bouton.

+++

### Média {#add-media}

Le **[!UICONTROL Media]** vous permet d’ajouter des médias à votre message in-app afin de créer une expérience utilisateur unique.

![](assets/in_app_content_3.png)

Saisissez votre URL de média ou cliquez sur le bouton **[!UICONTROL Select Assets]** pour ajouter directement des ressources stockées dans votre bibliothèque de ressources à votre message in-app. [En savoir plus sur la gestion des ressources](../email/assets-essentials.md).
Vous pouvez également ajouter une **[!UICONTROL Alternative text]** pour les applications de lecture d’écran.

+++ Plus d’options avec mise en forme avancée

Si la variable **[!UICONTROL Advanced formatting mode]** est activé, vous pouvez personnaliser la variable **[!UICONTROL Max height]** et **[!UICONTROL Max width]** de vos médias.

+++

### En-tête et corps {#title-body}

Pour composer votre message, saisissez le contenu dans le champ **[!UICONTROL Header]** et **[!UICONTROL Body]** champs.

![](assets/in_app_content_4.png)

Utilisez la variable **[!UICONTROL Personalization]** pour ajouter de la personnalisation. En savoir plus sur la personnalisation dans Adobe Journey Optimizer Expression Editor [dans cette section](../personalization/personalize.md).

+++ Plus d’options avec mise en forme avancée

Si la variable **[!UICONTROL Advanced formatting mode]** est activé, vous pouvez choisir pour votre **[!UICONTROL Header]** et **[!UICONTROL Body]**:

* la valeur **[!UICONTROL Font]**
* la valeur **[!UICONTROL Pt size]**
* la valeur **[!UICONTROL Font Color]**
* la valeur **[!UICONTROL Alignment]**
+++

### Boutons {#add-buttons}

Ajoutez des boutons pour que les utilisateurs puissent interagir avec votre message in-app.

![](assets/in_app_content_5.png)

Pour personnaliser votre bouton :

1. Editez le champ Texte #1 bouton (principal) . Vous pouvez également utiliser la variable **[!UICONTROL Personalization]** pour définir le contenu et les données de personnalisation.

1. Choisissez votre **[!UICONTROL Interact event]** qui définit l’action du bouton une fois que les utilisateurs ont interagi avec celui-ci.

1. Entrez votre URL web ou votre lien profond dans la **[!UICONTROL Target]** champ .

1. Pour ajouter plusieurs boutons, cliquez sur **[!UICONTROL Add button]**.

+++ Plus d’options avec mise en forme avancée

Si la variable **[!UICONTROL Advanced formatting mode]** est activé, vous pouvez choisir pour votre **[!UICONTROL Buttons]**:

* la valeur **[!UICONTROL Font]**
* la valeur **[!UICONTROL Pt size]**
* la valeur **[!UICONTROL Font Color]**
* la valeur **[!UICONTROL Alignment]**
* la valeur **[!UICONTROL Button style]**
* la valeur **[!UICONTROL Radius]**
* la valeur **[!UICONTROL Button color]**

+++

## Onglet Paramètres {#settings-tab}

Dans la **Paramètres** vous pouvez définir la mise en page du message et prévisualiser le message in-app. Vous pouvez également accéder à des options de mise en forme avancées.

### Aperçu {#preview-tab}

![](assets/in_app_content_6.png)

Le **[!UICONTROL App Preview]** vous permet d’ajouter un arrière-plan derrière votre message in-app :

* Un média provenant d’un lien URL.

* Ressource de votre bibliothèque Assets.

* Couleur d’arrière-plan.

### Disposition {#layout-options}

![](assets/in_app_content_7.png)

Le **[!UICONTROL Background image]** vous permet d’ajouter un arrière-plan à votre message in-app :

* Un média provenant d’un lien URL.

* Couleur d’arrière-plan.

### Message {#message-tab}

![](assets/in_app_content_8.png)

L’option de prise de contrôle de l’interface utilisateur, activée par défaut, vous permet d’assombrir l’arrière-plan de votre message in-app pour mettre l’accent sur votre contenu.

+++ Plus d’options avec mise en forme avancée

Si la variable **[!UICONTROL Advanced formatting mode]** est activé, vous pouvez personnaliser davantage votre message à l’aide des options suivantes :

* **[!UICONTROL Customize gestures]**: vous permet de personnaliser l’interaction de glissement de l’utilisateur. Si l’option Ignorer est sélectionnée, vous pouvez ajouter un événement d’interaction personnalisé et/ou une destination cible.

* **[!UICONTROL Customize UI takeover]**: permet de sélectionner une couleur à afficher en arrière-plan et son opacité.

* **[!UICONTROL Customize size]**: vous permet d’ajuster la largeur et la hauteur de votre notification in-app.

* **[!UICONTROL Customize position]**: vous permet de personnaliser la position de vos messages in-app sur l’écran de vos utilisateurs. Vous pouvez modifier les alignements vertical et horizontal.

* **[!UICONTROL Customize animation]**: vous permet de personnaliser vos animations d’affichage et d’affichage, par exemple si votre notification in-app apparaît depuis la gauche ou la partie supérieure de l’appareil de votre utilisateur.

* **[!UICONTROL Message round corner]**: vous permet d’ajouter un coin rond à votre notification in-app en modifiant la variable **[!UICONTROL Corner radius]**.

+++

**Rubriques connexes :**

* [Créer un message in-app](create-in-app.md)
* [Rapport in-app](inapp-report.md)
* [Configuration In-App](inapp-configuration.md)
