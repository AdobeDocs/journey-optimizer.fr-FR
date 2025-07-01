---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser des fragments visuels
description: Découvrez comment utiliser des fragments visuels lors de la création d’e-mails dans des campagnes et des parcours Journey Optimizer.
feature: Email Design, Fragments
topic: Content Management
role: User
level: Beginner
exl-id: 25a00f74-ed08-479c-9a5d-4185b5f3c684
source-git-commit: 7a8a0c133318b0bfc33b0fdb294e5b9ef53de9a5
workflow-type: tm+mt
source-wordcount: '715'
ht-degree: 91%

---

# Ajouter des fragments visuels à vos e-mails {#use-visual-fragments}

Un fragment est un composant réutilisable pouvant être référencé dans un ou plusieurs e-mails dans des campagnes, des parcours ou des modèles de contenu de Journey Optimizer. Cette fonctionnalité permet de créer en avance plusieurs blocs de contenu personnalisés qui peuvent être utilisés par des personnes chargées du marketing pour assembler rapidement les contenus d’e-mail dans un processus de conception amélioré. [Découvrez comment créer et gérer des fragments](../content-management/fragments.md).

➡️ [Découvrez comment gérer, créer et utiliser des fragments dans cette vidéo](../content-management/fragments.md#video-fragments)

## Utiliser un fragment {#use-fragment}

Pour utiliser un fragment dans un email, procédez comme suit :

>[!NOTE]
>
>Vous pouvez ajouter jusqu’à 30 fragments pour une diffusion donnée. Les fragments ne peuvent être imbriqués que jusqu’à un seul niveau.


1. Ouvrez le contenu d’un e-mail ou d’un modèle à l’aide du [concepteur d’e-mail](get-started-email-design.md).

1. Sélectionnez l’icône **[!UICONTROL Fragments]** dans le rail de gauche.

   ![](assets/fragments-in-designer.png)

1. La liste de tous les fragments visuels créés dans le sandbox actuel s’affiche. Les fragments sont triés par date de création : les fragments visuels récemment ajoutés sont affichés en premier dans la liste. Vous pouvez :

   * Rechercher un fragment spécifique en commençant à saisir son libellé.
   * Trier les fragments par ordre croissant ou décroissant.
   * Modifier l’affichage des fragments (vue Cartes ou Liste).
   * Actualiser la liste.

   >[!NOTE]
   >
   >Si certains fragments sont modifiés ou ajoutés pendant que vous modifiez votre contenu, la liste se met à jour en tenant compte des dernières modifications.

1. Faites glisser un fragment de la liste et déposez-le dans la zone où vous souhaitez l’insérer.

   ![](assets/fragment-insert.png)

   >[!CAUTION]
   >
   >Vous pouvez ajouter n’importe quel fragment ayant un statut **Brouillon** ou **Actif** à votre contenu. Cependant, vous ne pouvez pas activer votre parcours ou votre campagne si un fragment ayant le statut de brouillon est utilisé dans ce parcours ou cette campagne. Lors de la publication du parcours ou de la campagne, les fragments de brouillon affichent une erreur et vous devez les approuver pour pouvoir les publier.

1. Comme tout autre composant, vous pouvez déplacer le fragment dans votre contenu.

1. Sélectionnez le fragment pour afficher le volet correspondant à droite. De là, vous pouvez supprimer le fragment de votre contenu ou le dupliquer. Vous pouvez également effectuer ces actions directement à partir du menu contextuel qui s’affiche au-dessus du fragment.

   ![](assets/fragment-right-pane.png)

1. À partir de l’onglet **[!UICONTROL Paramètres]**, vous pouvez :

   * Sélectionner les appareils sur lesquels afficher le fragment.
   * Ouvrir le fragment dans un nouvel onglet pour le modifier, si nécessaire. [En savoir plus](../content-management/fragments.md#edit-fragments).
   * Explorer les références. [En savoir plus](../content-management/fragments.md#explore-references).

1. Vous pouvez personnaliser davantage votre fragment à l’aide de l’onglet **[!UICONTROL Styles]**.

1. Si nécessaire, vous pouvez rompre l’héritage avec le fragment d’origine. [En savoir plus](#break-inheritance).

1. Ajoutez autant de fragments que vous le souhaitez. Vous pouvez ensuite **[!UICONTROL enregistrer]** vos modifications.

## Utiliser des variables implicites {#implicit-variables-in-fragments}

Les variables implicites améliorent la fonctionnalité de fragment existante afin d’optimiser l’efficacité pour la réutilisation du contenu et les cas d’utilisation de script. Les fragments peuvent utiliser des variables d’entrée et créer des variables de sortie utilisables dans le contenu des campagnes et des parcours.

Découvrez comment utiliser les variables implicites dans [cette section](../personalization/use-expression-fragments.md#implicit-variables).

## Personnaliser des champs modifiables {#customize-fields}

Si certaines parties du fragment sélectionné ont été rendues modifiables, vous pouvez remplacer leur valeur par défaut après l’ajout du fragment dans votre contenu. [Découvrir comment rendre personnalisables vos fragments](../content-management/customizable-fragments.md)

Pour personnaliser les champs modifiables dans un fragment, procédez comme suit :

1. Ajoutez le fragment à votre contenu.

1. Sélectionnez-le pour ouvrir le volet Propriétés sur le côté droit.

   Tous les champs modifiables du fragment sont affichés dans l’onglet **Paramètres** sous la section **Fragment**.

1. Lorsque vous sélectionnez un champ modifiable dans le volet de droite, il est mis en surbrillance en vert dans le volet d’aperçu central, ce qui facilite l’identification de son emplacement dans votre contenu.

   Dans l’exemple ci-dessous, l’image **source** et le **texte alternatif** peuvent être modifiés, ainsi que l’**URL** du bouton « Cliquez ici ».

   ![](assets/fragment-editable.png)

## Rompre l’héritage {#break-inheritance}

Lorsque vous modifiez un fragment visuel, les modifications sont synchronisées. Elles sont automatiquement propagées à tous les parcours/campagnes et modèles de contenu, brouillons ou actifs, qui contiennent ce fragment.

Lorsqu’ils sont ajoutés à un e-mail ou à un modèle de contenu, les fragments sont synchronisés par défaut. Vous pouvez toutefois rompre l’héritage du fragment d’origine. Dans ce cas, le contenu du fragment est copié dans la conception actuelle et les modifications ne sont plus synchronisées.

Pour rompre l’héritage, procédez comme suit :

1. Sélectionnez le fragment.

1. Cliquez sur l’icône Déverrouiller dans la barre d’outils contextuelle.

   ![](assets/fragment-break-inheritance.png)

1. Ce fragment devient alors un élément autonome qui n’est plus lié au fragment d’origine. Modifiez-le comme tout autre composant de votre contenu. [En savoir plus](content-components.md).
