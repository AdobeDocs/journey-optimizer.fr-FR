---
title: Concevoir des cartes de contenu
description: Découvrez comment concevoir du contenu de cartes de contenu
topic: Content Management
role: User
level: Beginner
badge: label="Disponibilité limitée" type="Informative"
hide: true
hidefromtoc: true
source-git-commit: 8a902298bbbac5689b4f84266dd9c9027e45fad5
workflow-type: tm+mt
source-wordcount: '560'
ht-degree: 18%

---

# Concevoir le contenu des cartes de contenu {#design-content-card}

>[!BEGINSHADEBOX]

**Table des matières**

* [Prise en main des cartes de contenu](get-started-content-card.md)
* [Prérequis pour les cartes de contenu](content-card-configuration-prereq.md)
* [Configuration du canal de cartes de contenu dans Journey Optimizer](content-card-configuration.md)
* [Création de cartes de contenu](create-content-card.md)
* **Concevoir des cartes de contenu**
* [Rapport sur les cartes de contenu](content-card-report.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Actuellement, les cartes de contenu ne sont disponibles que pour un ensemble d’organisations (disponibilité limitée). Pour en bénéficier, contactez votre représentant ou représentante Adobe.

Le concept de création de cartes offre une expérience de création basée sur des formulaires qui fournit aux marketeurs des entrées de base qui peuvent être utilisées pour le rendu par le développeur.

Une fois votre contenu défini et personnalisé, vous pouvez le consulter et l’activer. Votre campagne sera envoyée selon le planning défini. [En savoir plus dans cette page](../campaigns/review-activate-campaign.md).

## Onglet Contenu {#content-tab}

Dans l&#39;onglet **[!UICONTROL Contenu]** , vous pouvez personnaliser vos cartes de contenu en définissant à la fois leur contenu et la conception du bouton **[!UICONTROL Fermer]** . De plus, vous pouvez améliorer votre contenu avec les médias et ajouter des boutons d’action directement à partir de cet onglet.

### Bouton Fermer {#close-button}

![](assets/content-card-design-1.png)

Sélectionnez le **[!UICONTROL Style]** de votre **[!UICONTROL bouton Fermer]** pour personnaliser son aspect.

Vous pouvez sélectionner l’un des styles suivants :

* **[!UICONTROL None]**
* **[!UICONTROL Simple]**
* **[!UICONTROL Cercle]**

### Contenu {#title-body}

Pour composer votre message, saisissez votre texte dans les champs **[!UICONTROL Titre]** et **[!UICONTROL Corps]** .

![](assets/content-card-design-2.png)

+++Plus d’options avec Formatage avancé

Si le **[!UICONTROL Mode de formatage avancé]** est activé, vous pouvez choisir les éléments suivants pour votre **[!UICONTROL En-tête]** et votre **[!UICONTROL Corps]** :

* la **[!UICONTROL Police]**
* la **[!UICONTROL Taille du point]**
* la **[!UICONTROL Couleur de la police]**
* l’**[!UICONTROL Alignement]**
+++

Si vous souhaitez personnaliser davantage votre message, utilisez l’icône **[!UICONTROL Personalization]** pour ajouter des éléments personnalisés. Pour obtenir des instructions détaillées sur l&#39;utilisation des fonctionnalités de personnalisation, reportez-vous à [cette section](../personalization/personalize.md).

### Média {#add-media}

Le champ **[!UICONTROL Média]** vous permet d’améliorer vos cartes de contenu en ajoutant des supports, ce qui peut rendre votre présentation plus attrayante pour les utilisateurs finaux.

![](assets/content-card-design-3.png)

Pour inclure un média, saisissez l’URL du média à utiliser ou cliquez sur l’icône **[!UICONTROL Sélectionner Assets]** pour choisir parmi les ressources stockées dans votre bibliothèque Assets. [En savoir plus sur la gestion des ressources](../content-management/assets.md).

+++Plus d’options avec Formatage avancé

Si le **[!UICONTROL mode de formatage avancé]** est activé, vous pouvez ajouter un **[!UICONTROL texte de remplacement]** pour les applications de lecture d’écran et un autre actif dans le champ **[!UICONTROL URL de média en mode sombre]**.

+++

### Boutons {#add-buttons}

Ajoutez des boutons pour que les utilisateurs puissent interagir avec vos cartes de contenu.

![](assets/content-card-design-4.png)

1. Cliquez sur **[!UICONTROL Ajouter un bouton]** pour créer un bouton d’action.

1. Editez le champ **[!UICONTROL Titre]** du bouton pour spécifier le libellé qui s&#39;affichera sur le bouton.

1. Sélectionnez un **[!UICONTROL événement Interact]** pour définir l’action qui sera déclenchée lorsque les utilisateurs cliqueront ou interagiront avec le bouton.

1. Dans le champ **[!UICONTROL Target]** , saisissez l’URL web ou le lien profond vers lequel les utilisateurs seront redirigés après avoir interagi avec le bouton.

+++Plus d’options avec Formatage avancé

Si le **[!UICONTROL Mode de formatage avancé]** est activé, vous pouvez choisir les éléments suivants pour vos **[!UICONTROL Boutons]** :

* la **[!UICONTROL Police]**
* la **[!UICONTROL Taille du point]**
* la **[!UICONTROL Couleur de la police]**
* l’**[!UICONTROL Alignement]**

+++

### Comportement en cas de clic

![](assets/content-card-design-5.png)

Dans le champ **[!UICONTROL URL cible]** , saisissez l’URL web ou le lien profond qui redirigera les utilisateurs vers la destination souhaitée une fois qu’ils auront interagi avec votre carte de contenu. Il peut s’agir d’un site web externe, d’une page spécifique au sein de l’application ou de tout autre emplacement sur lequel vous souhaitez que les utilisateurs soient amenés en fonction de leur interaction.

## Onglet Données

## Données personnalisées {#custom-data}

![](assets/content-card-design-6.png)

Dans la section **[!UICONTROL Données personnalisées]** , cliquez sur **[!UICONTROL Ajouter une paire clé/valeur]** pour inclure des variables personnalisées dans la payload. Ces paires clé/valeur vous permettent de transmettre des données supplémentaires, selon votre configuration spécifique. Vous pouvez ainsi ajouter du contenu personnalisé ou dynamique, des informations de suivi ou toute autre donnée pertinente pour votre configuration.
