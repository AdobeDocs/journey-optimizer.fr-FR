---
solution: Journey Optimizer
product: journey optimizer
title: Utilisation de fragments visuels
description: Découvrez comment utiliser des fragments visuels lors de la création d’emails dans des campagnes et des parcours Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: dd463d36550b53faaffca90691550278498c862a
workflow-type: tm+mt
source-wordcount: '445'
ht-degree: 72%

---

# Ajout de fragments visuels à vos emails {#use-visual-fragments}

Vous pouvez utiliser un fragment visuel dans une [email](get-started-email-design.md) dans un parcours ou une campagne, ou dans un [modèle de contenu](../content-management/content-templates.md).

>[!NOTE]
>
>Découvrez comment créer et gérer des fragments dans [cette section](../content-management/fragments.md).

➡️ [Découvrez comment gérer, créer et utiliser des fragments dans cette vidéo](../content-management/fragments.md#video-fragments)

## Utilisation d’un fragment {#use-fragment}

1. Ouvrez le contenu d’un e-mail ou d’un modèle à l’aide du [Concepteur d’e-mail](get-started-email-design.md).

1. Sélectionnez l’icône **[!UICONTROL Fragments]** dans le rail de gauche.

   ![](assets/fragments-in-designer.png)

1. La liste de tous les fragments visuels créés sur l’environnement de test actuel s’affiche. Vous pouvez :

   * Rechercher un fragment spécifique en commençant à saisir son libellé.
   * Trier les fragments par ordre croissant ou décroissant.
   * Modifier l’affichage des fragments (vue Cartes ou Liste).

   >[!NOTE]
   >
   >Les fragments sont triés par date de création : les fragments visuels récemment ajoutés sont affichés en premier dans la liste.

1. Vous pouvez rechercher et actualiser la liste.

   >[!NOTE]
   >
   >Si certains fragments ont été modifiés ou ajoutés pendant que vous modifiez votre contenu, la liste est mise à jour avec les dernières modifications.

1. Faites glisser un fragment de la liste et déposez-le dans la zone où vous souhaitez l’insérer.

   ![](assets/fragment-insert.png)

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

Lorsque vous modifiez un fragment visuel, les modifications sont synchronisées. Elles sont automatiquement propagées à tous les **[!UICONTROL brouillons]** de parcours/campagnes et modèles de contenu contenant ce fragment.

>[!NOTE]
>
>Les modifications ne sont pas propagées aux e-mails utilisés dans les parcours ou campagnes **[!UICONTROL dynamiques]**.

Lorsqu’ils sont ajoutés à un e-mail ou à un modèle de contenu, les fragments sont synchronisés par défaut.

Vous pouvez toutefois rompre l’héritage du fragment d’origine. Dans ce cas, le contenu du fragment est copié dans la conception actuelle et les modifications ne sont plus synchronisées.

Pour rompre l’héritage, procédez comme suit :

1. Sélectionnez le fragment.

1. Cliquez sur l’icône Déverrouiller dans la barre d’outils contextuelle.

   ![](assets/fragment-break-inheritance.png)

1. Ce fragment devient alors un élément autonome qui n’est plus lié au fragment d’origine. Modifiez-le comme tout autre composant de votre contenu. [En savoir plus](content-components.md).

