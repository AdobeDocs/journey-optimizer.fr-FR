---
solution: Journey Optimizer
product: journey optimizer
title: Créer des fragments
description: Découvrez comment créer des fragments pour réutiliser du contenu dans des campagnes et des parcours Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
source-git-commit: 251c145eb69fe8227a99655346e6e37f59a42bea
workflow-type: tm+mt
source-wordcount: '1431'
ht-degree: 6%

---


# Utilisation de fragments {#fragments}

Un fragment est un composant réutilisable pouvant être référencé dans un ou plusieurs emails au sein de [!DNL Journey Optimizer] campagnes et parcours.

Cette fonctionnalité permet de précréer plusieurs blocs de contenu personnalisés qui peuvent être utilisés par des utilisateurs marketing non techniques pour assembler rapidement les contenus d’email dans un processus de conception amélioré.

<!--
➡️ [Learn how to create and use templates in this video](#video-templates)-->

>[!CAUTION]
>
>Pour créer, modifier et archiver des fragments, vous devez disposer de la variable **[!DNL Manage Library Items]** autorisation incluse dans la variable **[!DNL Content Library Manager]** profil de produit. [En savoir plus](../administration/ootb-product-profiles.md#content-library-manager).

Pour optimiser l’utilisation des fragments :

* Créez vos propres fragments. Voir [Créer des fragments](#create-fragments)
* Utilisez-les autant de fois que nécessaire dans vos emails. Voir [Utilisation de fragments](#use-fragments)

>[!NOTE]
>
>Actuellement, cette fonctionnalité n’est disponible que pour les emails.

## Accès et gestion des fragments {#access-manage-fragments}

Pour accéder à la liste des fragments, sélectionnez **[!UICONTROL Gestion de contenu]** > **[!UICONTROL Fragments]** dans le menu de gauche.

![](assets/fragment-list.png)

Tous les fragments qui ont été créés sur l’environnement de test actuel, soit à partir du **[!UICONTROL Fragments]** à l’aide de la fonction [Enregistrer en tant que fragment](#save-as-fragment) option : s’affichent.

Vous pouvez filtrer les fragments selon la date de création ou de modification. Vous pouvez choisir d’afficher tous les fragments ou uniquement les éléments créés ou modifiés par l’utilisateur actuel. Vous pouvez également afficher la variable **[!UICONTROL Archivé]** fragments. [En savoir plus](#archive-fragments).

![](assets/fragment-list-filters.png)

Dans la **[!UICONTROL Autres actions]** en regard de chaque fragment, vous pouvez effectuer les opérations suivantes :

* Dupliquez un fragment.

* Utilisez la variable **[!UICONTROL Exploration des références]** pour afficher les parcours, les campagnes ou les modèles dans lesquels ils sont utilisés. [En savoir plus](#explore-references).

* Archivez un fragment. [En savoir plus](#archive-fragments).

![](assets/fragment-list-more-actions.png)

### Modification de fragments {#edit-fragments}

Pour modifier un fragment, procédez comme suit.

1. Cliquez sur l’élément de votre choix dans la **[!UICONTROL Fragment]** liste.
1. À partir des propriétés du fragment, vous pouvez [explorer les références](#explore-references), [gérer son accès](../administration/object-based-access.md) et mettre à jour les détails du fragment.

   ![](assets/fragment-edit-content.png)

1. Sélectionnez le bouton correspondant pour modifier le contenu comme vous le feriez lors de la création d’un fragment à partir de zéro. [En savoir plus](#create-from-scratch).


>[!NOTE]
>
>Lorsque vous modifiez un fragment, les modifications sont automatiquement propagées à tous les emails ou modèles contenant ce fragment, à l’exception des emails utilisés dans **[!UICONTROL En direct]** parcours ou campagnes. Vous pouvez également rompre l’héritage du fragment d’origine. [En savoir plus](#break-inheritance).

<!--Changes made to a fragment are not propagated to live journeys or campaigns where it is used.-->

<!--When added to an email, if you want to modify a fragment for a specific email, you can break the synchronization with the original fragment. The fragment becomes part of the email content and the changes will not be synchronized anymore. [Learn more](#break-inheritance)-->

### Exploration des références {#explore-references}

Vous pouvez afficher la liste des parcours, campagnes et modèles de contenu qui utilisent actuellement un fragment.

Pour ce faire, sélectionnez **[!UICONTROL Exploration des références]** soit à partir de **[!UICONTROL Autres actions]** dans la liste des fragments ou dans l’écran des propriétés du fragment.

![](assets/fragment-explore-references.png)

Sélectionnez un onglet pour basculer entre les parcours, les campagnes et les modèles. Vous pouvez voir leur état et cliquer sur un nom pour le rediriger vers l’élément correspondant où le fragment est référencé.

![](assets/fragment-usage-screen.png)

>[!NOTE]
>
>Si le fragment est utilisé dans un parcours, une campagne ou un modèle dont le libellé vous empêche d’y accéder, un message d’alerte s’affiche en haut de l’onglet sélectionné. [En savoir plus sur le contrôle d’accès au niveau de l’objet (OLAC)](../administration/object-based-access.md)

### Archiver des fragments {#archive-fragments}

Vous pouvez supprimer la liste des fragments des éléments qui ne sont plus pertinents pour votre marque.

Pour ce faire, cliquez sur le bouton **[!UICONTROL Autres actions]** en regard du fragment souhaité, puis sélectionnez **[!UICONTROL Archiver]**. Il disparaîtra de la liste des fragments, ce qui empêche les utilisateurs de l’utiliser dans les futurs emails ou modèles.

![](assets/fragment-list-archive.png)

>[!NOTE]
>
>Si vous archivez un fragment utilisé dans un email ou dans un modèle de contenu, <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->l’email ou le modèle ne sera pas affecté.

Pour désarchiver un fragment, filtrez selon la variable **[!UICONTROL Archivé]** éléments et sélectionnez **[!UICONTROL Désarchiver]** de la **[!UICONTROL Autres actions]** . Il est à nouveau accessible à partir de la liste des fragments et peut être utilisé dans n’importe quel email ou modèle.

![](assets/fragment-list-unarchive.png)

## Créer des fragments {#create-fragments}

Vous pouvez créer des fragments de deux manières différentes :

* Créez un fragment à partir de zéro, à l’aide de la fonction **[!UICONTROL Fragments]** menu dédié. [Voici comment procéder.](#create-template-from-scratch)

* Lors de la conception d’un email ou d’un modèle de contenu, enregistrez une partie de votre contenu en tant que fragment. [Voici comment procéder.](#save-as-template)

Une fois enregistré, votre fragment peut être utilisé dans un parcours, une campagne ou un modèle. Que ce fragment soit créé de A à Z ou à partir d’un contenu existant, vous pouvez désormais l’utiliser lors de la création d’une [email](get-started-email-design.md) ou [modèle de contenu](content-templates.md) dans [!DNL Journey Optimizer]. [En savoir plus](#use-fragments).

### Créer à partir de zéro {#create-from-scratch}

>[!CONTEXTUALHELP]
>id="ajo_create_fragment"
>title="Définition de votre propre fragment"
>abstract="Créez un fragment autonome de A à Z pour rendre votre contenu réutilisable sur plusieurs parcours et campagnes."

Pour créer un fragment à partir de zéro, procédez comme suit.

1. Accédez à la liste des fragments via le **[!UICONTROL Gestion de contenu]** > **[!UICONTROL Fragments]** menu de gauche.

1. Sélectionner **[!UICONTROL Créer un fragment]**.

1. Renseignez les détails du fragment, c’est-à-dire le nom et la description (si nécessaire).

   ![](assets/fragment-details.png)

   >[!NOTE]
   >
   >Actuellement, seule la variable **[!UICONTROL Fragment visuel]** et la variable **Email** sont pris en charge.

1. Pour attribuer des libellés d’utilisation de données personnalisés ou de base au fragment, sélectionnez **[!UICONTROL Gérer l’accès]**. [En savoir plus sur le contrôle d’accès au niveau de l’objet (OLAC)](../administration/object-based-access.md).

1. Cliquez sur **[!UICONTROL Créer]**.

1. Le [Concepteur d’e-mail](get-started-email-design.md) s’affiche. Modifiez votre contenu selon vos besoins, de la même manière que pour tout email contenu dans un parcours ou une campagne.

   >[!NOTE]
   >
   >Vous pouvez ajouter des champs de personnalisation et du contenu dynamique, mais les attributs contextuels ne sont pas pris en charge dans les fragments.

   ![](assets/fragment-designer.png)

1. Une fois votre fragment prêt, cliquez sur **[!UICONTROL Enregistrer]**.

1. Si nécessaire, cliquez sur la flèche en regard du nom du fragment pour revenir au **[!UICONTROL Détails]** et modifiez-la.

   ![](assets/fragment-designer-back.png)

Ce fragment est maintenant prêt à être utilisé lors de la création d’un [email](get-started-email-design.md) ou [modèle de contenu](content-templates.md) dans [!DNL Journey Optimizer]. [Voici comment procéder.](#use-fragments)

### Enregistrer en tant que fragment {#save-as-fragment}

Lors de la conception d’une [modèle de contenu](content-templates.md) ou [email](get-started-email-design.md) dans une campagne ou un parcours, vous pouvez enregistrer une partie de votre contenu en tant que fragment pour une réutilisation ultérieure. Pour ce faire, suivez les étapes ci-après.

1. Dans le [Concepteur d&#39;email](get-started-email-design.md), cliquez sur les points de suspension en haut à droite de l’écran.

1. Sélectionner **[!UICONTROL Enregistrer en tant que fragment]** dans le menu déroulant.

   ![](assets/fragment-save-as.png)

1. Le **[!UICONTROL Enregistrer en tant que fragment]** s’affiche. Sélectionnez ensuite les éléments que vous souhaitez inclure dans votre fragment, notamment les champs de personnalisation et le contenu dynamique. Notez que les attributs contextuels ne sont pas pris en charge dans les fragments.

   >[!CAUTION]
   >
   >Vous ne pouvez sélectionner que les sections adjacentes. Vous ne pouvez pas sélectionner une structure vide ou un autre fragment.

   ![](assets/fragment-save-as-screen.png)

1. Cliquez sur **[!UICONTROL Créer]**. Renseignez les détails du fragment, c’est-à-dire le nom et la description (si nécessaire).

   ![](assets/fragment-details.png)

   >[!NOTE]
   >
   >Actuellement, seule la variable **[!UICONTROL Fragment visuel]** et la variable **Email** sont pris en charge.

1. Pour attribuer des libellés d’utilisation de données personnalisés ou de base au fragment, sélectionnez **[!UICONTROL Gérer l’accès]**. [En savoir plus sur le contrôle d’accès au niveau de l’objet (OLAC)](../administration/object-based-access.md).

1. Cliquez sur **[!UICONTROL Créer]** encore une fois. Le fragment est enregistré dans la variable **[!UICONTROL Fragments]** accessible à partir de la liste [!DNL Journey Optimizer] menu dédié.

   Il devient un fragment autonome qui peut être [accessible](#access-manage-fragments), [modifié](#edit-fragments) et [archivé](#archive-fragments) comme tout autre élément de cette liste.

Vous pouvez désormais utiliser ce fragment lors de la création d’un [email](get-started-email-design.md) ou [modèle de contenu](content-templates.md) dans [!DNL Journey Optimizer]. [Voici comment procéder.](#use-fragments)

>[!NOTE]
>
>Toute modification apportée à ce nouveau fragment n’est pas propagée dans l’email ou le modèle d’origine. De même, lorsque le contenu d’origine est modifié dans cet email ou ce modèle, le nouveau fragment n’est pas modifié.

## Utilisation de fragments {#use-fragments}

Vous pouvez utiliser un fragment dans une [email](get-started-email-design.md) dans un parcours ou une campagne, ou dans un [modèle de contenu](content-templates.md).

1. Ouvrez un contenu d’email ou de modèle à l’aide de la méthode [Concepteur d&#39;email](get-started-email-design.md).

1. Sélectionnez la **[!UICONTROL Fragments]** dans le rail de gauche.

   ![](assets/fragments-in-designer.png)

1. La liste de tous les fragments créés sur l’environnement de test actuel s’affiche. Vous pouvez :

   * Recherchez un fragment spécifique en commençant à saisir son libellé.
   * Triez les fragments par ordre croissant ou décroissant.
   * Modifiez l’affichage des fragments (mode Carte ou Liste).

1. Vous pouvez également actualiser la liste.

   >[!NOTE]
   >
   >Si certains fragments ont été modifiés ou ajoutés pendant que vous modifiez votre contenu, la liste est mise à jour avec les dernières modifications.

1. Faites glisser un fragment de la liste et déposez-le dans la zone où vous souhaitez l’insérer.

   ![](assets/fragment-insert.png)

1. Comme tout autre composant, vous pouvez déplacer le fragment dans votre contenu.

1. Sélectionnez le fragment à afficher dans le volet correspondant à droite. De là, vous pouvez supprimer le fragment de votre contenu ou le dupliquer. Vous pouvez également effectuer ces actions directement à partir du menu contextuel qui s’affiche au-dessus du fragment.

   ![](assets/fragment-right-pane.png)

1. Dans la **[!UICONTROL Paramètres]** vous pouvez :

   * Sélectionnez les appareils sur lesquels vous souhaitez que le fragment s’affiche.
   * Ouvrez le fragment dans un nouvel onglet pour le modifier, si nécessaire. [En savoir plus](#edit-fragments).
   * Explorez les références. [En savoir plus](#explore-references).

1. Vous pouvez personnaliser davantage votre fragment à l’aide du **[!UICONTROL Styles]** .

1. Si nécessaire, vous pouvez rompre l’héritage avec le fragment d’origine. [En savoir plus](#break-inheritance).

1. Ajoutez autant de fragments que vous le souhaitez et **[!UICONTROL Enregistrer]** vos modifications.

### Rompre l’héritage {#break-inheritance}

Lorsque vous modifiez un fragment, les modifications sont synchronisées. Ils sont automatiquement propagés à tous **[!UICONTROL Version préliminaire]** parcours/campagnes et modèles de contenu contenant ce fragment.

>[!NOTE]
>
>Les modifications ne sont pas propagées aux emails utilisés dans **[!UICONTROL En direct]** parcours ou campagnes.

Lorsqu&#39;ils sont ajoutés à un email ou à un modèle de contenu, les fragments sont synchronisés par défaut.

Vous pouvez toutefois rompre l’héritage du fragment d’origine. Dans ce cas, le contenu du fragment est copié dans la conception actuelle et les modifications ne seront plus synchronisées.

Pour rompre l’héritage, procédez comme suit :

1. Sélectionnez le fragment.

1. Cliquez sur l’icône de déverrouillage dans la barre d’outils contextuelle.

   ![](assets/fragment-break-inheritance.png)

1. Ce fragment devient un élément autonome qui n’est plus lié au fragment d’origine. Modifiez-le comme tout autre composant de contenu de votre contenu. [En savoir plus](content-components.md).

<!--

## How-to video {#video-templates}

Learn how to create, edit, and use fragments in [!DNL Journey Optimizer].

>[!VIDEO](https://video.tv.adobe.com/v/3413743/?quality=12)

-->
