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
source-git-commit: 893f7146b358da48153b1e6bc74b8f622028df76
workflow-type: tm+mt
source-wordcount: '612'
ht-degree: 57%

---

# Ajouter des fragments visuels à vos e-mails {#use-visual-fragments}

Un fragment est un composant réutilisable pouvant être référencé dans un ou plusieurs emails au sein de campagnes Journey Optimizer, de parcours ou de modèle de contenu. Cette fonctionnalité permet de précréer plusieurs blocs de contenu personnalisés qui peuvent être utilisés par les utilisateurs marketing pour assembler rapidement les contenus d’email dans un processus de conception amélioré. [Découvrez comment créer et gérer des fragments](../content-management/fragments.md).

➡️ [Découvrez comment gérer, créer et utiliser des fragments dans cette vidéo.](../content-management/fragments.md#video-fragments)

## Utiliser un fragment {#use-fragment}

Pour utiliser un fragment dans un email, procédez comme suit.

>[!NOTE]
>
>Vous pouvez ajouter jusqu’à 30 fragments dans une diffusion donnée. Les fragments ne peuvent être imbriqués qu’à un niveau maximum.


1. Ouvrez le contenu d’un e-mail ou d’un modèle à l’aide du [concepteur d’e-mail](get-started-email-design.md).

1. Sélectionnez l’icône **[!UICONTROL Fragments]** dans le rail de gauche.

   ![](assets/fragments-in-designer.png)

1. La liste de tous les fragments visuels créés dans le sandbox actuel s’affiche. Ils sont triés par date de création : les fragments visuels récemment ajoutés sont affichés en premier dans la liste. Vous pouvez :

   * Rechercher un fragment spécifique en commençant à saisir son libellé.
   * Trier les fragments par ordre croissant ou décroissant.
   * Modifier l’affichage des fragments (vue Cartes ou Liste).
   * Actualisez la liste.

   >[!NOTE]
   >
   >Si certains fragments ont été modifiés ou ajoutés pendant que vous modifiez votre contenu, la liste est mise à jour avec les dernières modifications.

1. Faites glisser un fragment de la liste et déposez-le dans la zone où vous souhaitez l’insérer.

   ![](assets/fragment-insert.png)

   >[!CAUTION]
   >
   >Vous pouvez ajouter n’importe quel **Version préliminaire** ou **En direct** fragment dans votre contenu. Cependant, vous ne pourrez pas activer votre parcours ou campagne si un fragment avec le statut En création y est utilisé. Lors de la publication parcours ou de la campagne, les fragments de brouillon affichent une erreur et vous devez les approuver pour pouvoir publier.
   >
   > Notez que les statuts des fragments sont déployés progressivement au cours des jours qui suivent la publication de Journey Optimizer en juin. Bien que certains utilisateurs disposent d’un accès immédiat, d’autres peuvent rencontrer un délai avant qu’il ne soit disponible dans leur environnement. Si cette amélioration n’est pas encore disponible dans votre environnement, veuillez noter que le fragment ne doit pas obligatoirement être **En direct** à utiliser dans vos parcours et campagnes.

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

## Rompre l’héritage {#break-inheritance}

Lorsque vous modifiez un fragment visuel, les modifications sont synchronisées. Ils sont automatiquement propagés à tous les parcours/campagnes en version préliminaire ou active et aux modèles de contenu contenant ce fragment.

Lorsqu&#39;ils sont ajoutés à un email ou à un modèle de contenu, les fragments sont synchronisés par défaut. Vous pouvez toutefois rompre l’héritage du fragment d’origine. Dans ce cas, le contenu du fragment est copié dans la conception actuelle et les modifications ne sont plus synchronisées.

Pour rompre l’héritage, procédez comme suit :

1. Sélectionnez le fragment.

1. Cliquez sur l’icône Déverrouiller dans la barre d’outils contextuelle.

   ![](assets/fragment-break-inheritance.png)

1. Ce fragment devient alors un élément autonome qui n’est plus lié au fragment d’origine. Modifiez-le comme tout autre composant de votre contenu. [En savoir plus](content-components.md).
