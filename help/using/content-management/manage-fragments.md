---
solution: Journey Optimizer
product: journey optimizer
title: Gérer les fragments
description: Découvrir comment gérer vos fragments de contenu
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: 1fc708e1-a993-4a2a-809c-c5dc08a4bae1
source-git-commit: d93ef15df4a25e7a6d6fab3df1f9838a0c3d31df
workflow-type: ht
source-wordcount: '979'
ht-degree: 100%

---

# Gérer les fragments {#manage-fragments}

Pour gérer vos fragments, accédez à la liste des fragments à partir du menu de gauche **[!UICONTROL Gestion de contenu]** > **[!UICONTROL Fragments]**.

Tous les fragments qui ont été créés sur le sandbox actuel, soit [à partir du menu **[!UICONTROL Fragments]**](#create-fragments), soit à l’aide de l’option [Enregistrer en tant que fragment](#save-as-fragment), s’affichent.

![](assets/fragment-list-filters.png)

Vous pouvez filtrer les fragments selon leur :

* Statut (Brouillon ou Actif)
* Type (visuel ou d’expression)
* Date de création ou de modification
* État (archivé ou non)
* Balises

Vous pouvez choisir d’afficher tous les fragments ou uniquement les éléments créés ou modifiés par la personne y ayant accès.

Cliquez sur le bouton **[!UICONTROL Plus d’actions]** en regard de chaque fragment pour effectuer les opérations suivantes :

* Dupliquer un fragment.
* Utilisez l’option **[!UICONTROL Explorer les références]** pour afficher les parcours, les campagnes ou les modèles dans lesquels ils sont utilisés. [En savoir plus](#explore-references).
* Archiver un fragment. [En savoir plus](#archive-fragments).
* Modifier les balises d’un fragment [Découvrez comment utiliser les balises unifiées](../start/search-filter-categorize.md#tags).

![](assets/fragment-list-more-actions.png)

## Statuts des fragments

>[!CONTEXTUALHELP]
>id="ajo_fragment_statuses"
>title="Nouveaux statuts de fragments"
>abstract="Depuis que les status **Brouillon** et **Actif** ont été introduits avec la version de juin de Journey Optimizer, tous les fragments créés avant cette version ont le statut « Brouillon », même s’ils sont utilisés dans un parcours ou une campagne. Si vous apportez des modifications à ces fragments, vous devez les publier pour les rendre « Actif » et propager les modifications aux campagnes et parcours associés. Vous devez également créer une version de parcours/campagne et la publier. <br/>La publication requiert l’autorisation utilisateur <a href="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manage">Publier un fragment</a>."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/access-control/privacy/ootb-product-profiles#content-library-manager" text="En savoir plus sur les autorisations des fragments de contenu"

Les fragments peuvent avoir plusieurs statuts :

* **[!UICONTROL Brouillon]** : le fragment est en cours de modification et n’a pas été approuvé.

* **[!UICONTROL Actif]** : le fragment a été approuvé et est actif. [Découvrir comment publier un fragment](../content-management/create-fragments.md#publish)

  Lorsqu’un fragment actif est en cours de modification, une icône spécifique s’affiche à côté de son statut. Cliquez sur cette icône pour ouvrir la version brouillon du fragment.

* **[!UICONTROL Publication]** : le fragment a été approuvé et est en cours de publication.
* **[!UICONTROL Archivé]** : le fragment a été archivé. [Découvrir comment archiver des fragments](#archive-fragments)

>[!CAUTION]
>
>Depuis que les status **Brouillon** et **Actif** ont été introduits avec la version de juin de Journey Optimizer, tous les fragments créés avant cette version ont le statut « Brouillon », même s’ils sont utilisés dans un parcours ou une campagne. Si vous apportez des modifications à ces fragments, vous devez les publier pour les rendre « Actif » et propager les modifications aux campagnes et parcours associés. Vous devez également créer une version de parcours/campagne et la publier. La publication requiert l’autorisation utilisateur [Publier un fragment](../administration/ootb-product-profiles.md#content-library-manager).

## Modifier des fragments {#edit-fragments}

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_campaigns"
>title="Mise à jour des fragments dans les campagnes"
>abstract="Cette campagne ne sera pas mise à jour si vous publiez des modifications dans le fragment. Une nouvelle version doit être publiée afin que la fonctionnalité de mise à jour des fragments puisse être prise en charge."

>[!CONTEXTUALHELP]
>id="ajo_fragments_update_journeys"
>title="Mise à jour des fragments dans les parcours"
>abstract="Ce parcours ne sera pas mis à jour si vous publiez des modifications dans le fragment. Une nouvelle version doit être publiée afin que la fonctionnalité de mise à jour des fragments puisse être prise en charge."

Pour modifier un fragment, procédez comme suit.

1. Cliquez sur le fragment de votre choix dans la liste **[!UICONTROL Fragments]**.

1. Les propriétés du fragment s’ouvrent avec un aperçu de son contenu.

1. Si le fragment en cours de modification a le statut **Actif**, cliquez sur le bouton **Modifier** pour créer une version brouillon du fragment. La version actuelle du fragment reste active jusqu’à ce que vous publiiez la version brouillon.

1. Apportez les modifications souhaitées au fragment. Pour modifier son contenu, cliquez sur le bouton **Modifier** puis modifiez votre contenu comme vous le feriez lors de la création d’un fragment à partir de zéro. [Découvrir comment créer un fragment](#create-from-scratch)

   >[!NOTE]
   >
   >Lors de la modification d’un fragment, vous pouvez supprimer n’importe quel champ de personnalisation, mais vous ne pouvez pas en ajouter de nouveaux au contenu du fragment. Si vous souhaitez ajouter des champs de personnalisation, dupliquez le fragment afin d’en créer un .

   Vous pouvez également vérifier la liste des parcours, campagnes et modèles de contenu dans lesquels le fragment est actuellement utilisé en sélectionnant l’option **Explorer les références**. [En savoir plus](#explore-references)

   ![](assets/fragment-edit.png)

1. Une fois vos modifications prêtes, cliquez sur le bouton **Publier** pour rendre vos modifications actives.

Lorsque vous apportez des modifications à un fragment, celles-ci sont automatiquement répercutées sur tous les contenus utilisant ce fragment, y compris les parcours et campagnes actifs, sauf pour les contenus dont l’héritage du fragment original a été rompu. Découvrez comment rompre l’héritage dans les sections [Ajouter des fragments visuels à vos e-mails](../email/use-visual-fragments.md#break-inheritance) et [Utiliser des fragments d’expression](../personalization/use-expression-fragments.md#break-inheritance).

## Explorer les références {#explore-references}

Vous pouvez afficher la liste des parcours, des campagnes et des modèles de contenu qui utilisent actuellement un fragment. Pour ce faire, sélectionnez **[!UICONTROL Explorer les références]**, soit à partir du menu **[!UICONTROL Autres actions]** dans la liste des fragments ou dans l’écran des propriétés du fragment.

![](assets/fragment-explore-references.png)

Sélectionnez un onglet pour basculer entre les parcours, les campagnes, les modèles et les fragments. Vous pouvez voir leur statut et cliquer sur un nom pour le rediriger vers l’élément correspondant où le fragment est référencé.

![](assets/fragment-usage-screen.png)

>[!NOTE]
>
>Si le fragment est utilisé dans un parcours, une campagne ou un modèle dont le libellé vous empêche l’accès, un message d’alerte s’affiche en haut de l’onglet sélectionné. [En savoir plus sur le contrôle d’accès au niveau de l’objet (OLAC)](../administration/object-based-access.md)

## Archiver des fragments {#archive-fragments}

Vous pouvez supprimer de la liste des fragments des éléments qui ne sont plus pertinents pour votre marque.

Pour ce faire, cliquez sur l’icône **[!UICONTROL Plus d’actions]** en regard du fragment souhaité, puis sélectionnez **[!UICONTROL Archiver]**. Il disparaîtra de la liste des fragments, ce qui empêche leur utilisation dans les futurs e-mails ou modèles.

![](assets/fragment-list-archive.png)

>[!NOTE]
>
>Si vous archivez un fragment utilisé dans un contenu, <!--it will remain in the email or template, but you won't be able to select it from the fragment list to edit it-->ce contenu ne sera pas affecté.

Pour désarchiver un fragment, filtrez sur les éléments **[!UICONTROL archivés]** et sélectionnez **[!UICONTROL Désarchiver]** dans le menu **[!UICONTROL Autres actions]**. Le fragment est à nouveau accessible à partir de la liste des fragments et peut être utilisé dans n’importe quel e-mail ou modèle.

![](assets/fragment-list-unarchive.png)

## Exporter des fragments vers un autre sandbox {#export}

Journey Optimizer vous permet de copier un fragment d’un sandbox à un autre. Par exemple, vous pouvez copier un fragment de votre sandbox d’évaluation vers votre sandbox de production.

Le processus de copie est réalisé via un **import et un export de package** entre les sandbox source et cible. Des informations détaillées sur l’export d’objets et leur import dans un sandbox cible sont disponibles dans cette section : [Copier des objets vers un autre sandbox](../configuration/copy-objects-to-sandbox.md).
