---
solution: Journey Optimizer
product: journey optimizer
title: Verrouiller le contenu dans les modèles d’e-mail
description: Découvrez comment verrouiller le contenu dans vos modèles d’e-mail.
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: f64fe1c4-3e30-4b74-80f8-b801a5f1d4c4
source-git-commit: dcbb83e72377838281e1762bb99230e7fe52ab4c
workflow-type: tm+mt
source-wordcount: '1273'
ht-degree: 100%

---

# Verrouiller le contenu dans les modèles d’e-mail {#lock-content-email-templates}

>[!CONTEXTUALHELP]
>id="ajo_locking_governance"
>title="Gouvernance"
>abstract="Activez la gouvernance pour verrouiller le contenu dans le modèle, en verrouillant soit l’ensemble du modèle, soit des structures et composants spécifiques. Cela vous permet d’éviter les modifications ou suppressions involontaires, de mieux contrôler la personnalisation des modèles et d’améliorer l’efficacité et la fiabilité de vos campagnes par e-mail."

>[!CONTEXTUALHELP]
>id="ajo_locking_mode"
>title="Mode"
>abstract="Sélectionnez le mode de verrouillage souhaité pour le modèle. Le **Verrouillage du contenu** vous permet de verrouiller des sections spécifiques de contenu dans le modèle. La **Lecture seule** vous permet de verrouiller l’intégralité du contenu du modèle, empêchant toute modification."

>[!CONTEXTUALHELP]
>id="ajo_locking_content_addition"
>title="Activer l’ajout de contenu"
>abstract="Activez cette option pour définir plus précisément comment les personnes peuvent interagir avec le modèle. Sélectionnez **Autoriser l’ajout de structures et de contenu** pour permettre aux utilisateurs et aux utilisatrices d’insérer de nouvelles structures entre celles déjà en place et d’ajouter des composants ou fragments de contenu dans les structures modifiables. **Autoriser l’ajout de contenu uniquement** permet aux utilisateurs et aux utilisatrices d’ajouter des composants ou fragments de contenu dans des structures modifiables, sans possibilité d’ajouter ou de dupliquer des structures."

>[!CONTEXTUALHELP]
>id="ajo_email_locking_activated"
>title="Gouvernance activée"
>abstract="Le verrouillage du contenu est activé et empêche les modifications."

>[!CONTEXTUALHELP]
>id="ajo_email_locking_read_only"
>title="Lecture seule"
>abstract="Ce contenu est en lecture seule et ne peut pas être modifié."

Journey Optimizer vous permet de verrouiller le contenu dans les modèles d’e-mail, en verrouillant l’intégralité du modèle ou des structures et composants spécifiques. Cela vous permet d’éviter des modifications ou suppressions involontaires, de mieux contrôler la personnalisation des modèles et d’améliorer l’efficacité et la fiabilité de vos campagnes par e-mail.

>[!IMPORTANT]
>
>Le verrouillage du contenu est une fonctionnalité au niveau de l’éditeur pour les personnes chargées de la création et ne garantit pas que le contenu ne sera pas modifié s’il est importé ou créé via une API.

Le verrouillage du contenu peut être appliqué au niveau de la **structure** ou au niveau du **composant**. Voici les principaux principes qui s’appliquent au niveau de la structure et au niveau du composant lors du verrouillage du contenu dans votre modèle :

* Lorsqu’une structure est verrouillée :

   * Tout le contenu de cette structure est également verrouillé par défaut.
   * Aucun contenu ne peut être ajouté à la structure.
   * Par défaut, vous ne pouvez pas supprimer la structure. Vous pouvez contourner cette restriction en activant l’option « Autoriser la suppression ».
   * Les composants de contenu individuels dans la structure verrouillée peuvent être définis comme modifiables.

* Lorsqu’une structure est modifiable (structure non verrouillée) :

   * Les composants de contenu individuels peuvent être verrouillés dans cette structure.
   * Par défaut, vous ne pouvez pas supprimer un composant s’il est verrouillé ou si l’option « Verrouillage de contenu modifiable uniquement » est sélectionnée. Vous pouvez contourner cette restriction en activant l’option « Autoriser la suppression ».

>[!AVAILABILITY]
>
>Les utilisateurs et les utilisatrices autorisés à créer des modèles de contenu peuvent activer le verrouillage de contenu.

➡️ [Découvrez cette fonctionnalité en vidéo.](#video)

## Verrouillage d’un modèle d’e-mail {#define}

### Activation du verrouillage de contenu {#enable}

Vous pouvez activer le verrouillage de contenu pour un modèle d’e-mail directement dans le Concepteur d’e-mail que vous créiez un nouveau modèle ou que vous en modifiiez un existant. Procédez comme suit :

1. Ouvrez ou créez un modèle d’e-mail et accédez à l’écran de modification du contenu dans le Concepteur d’e-mail.

1. Dans le volet **[!UICONTROL Corps]** à droite, activez l’option **[!UICONTROL Gouvernance]**.

1. Dans la liste déroulante **[!UICONTROL Mode]**, sélectionnez le mode de verrouillage souhaité pour le modèle :

   * **[!UICONTROL Verrouillage de contenu]** : verrouillez des sections spécifiques du contenu dans le modèle. Par défaut, toutes les structures et tous les composants deviennent modifiables. Vous pouvez ensuite verrouiller de manière sélective des éléments individuels.
   * **[!UICONTROL Lecture seule]** : verrouillez le contenu complet du modèle, ce qui empêche toute modification.

   ![](assets/template-lock-enable.png)

1. Si vous avez sélectionné le mode **[!UICONTROL Verrouillage de contenu]**, vous pouvez définir plus précisément comment les personnes peuvent interagir avec le modèle. Activez l’option **[!UICONTROL Activer l’ajout de contenu]** et sélectionnez l’une des options suivantes :

   * **[!UICONTROL Autoriser l’ajout de structure et de contenu]** : les personnes peuvent ajouter des structures entre des structures existantes et ajouter des composants de contenu ou des fragments dans des structures modifiables.

   * **[!UICONTROL Autoriser l’ajout de contenu uniquement]** : les personnes peuvent ajouter des composants de contenu ou des fragments dans des structures modifiables, mais elles ne peuvent pas ajouter ni dupliquer des structures.

1. Après avoir sélectionné le mode de verrouillage, vous pouvez définir les structures et/ou les composants à verrouiller si vous avez sélectionné le mode **[!UICONTROL Verrouillage de contenu]** :

   * [Découvrir comment verrouiller des structures](#lock-structures)
   * [Découvrir comment verrouiller des composants](#lock-components)

   Si vous choisissez le mode **[!UICONTROL Lecture seule]**, vous pouvez terminer et enregistrer votre modèle de la manière habituelle.

Vous pouvez ajuster les paramètres de **[!UICONTROL gouvernance]** à tout moment lors de la conception de votre modèle en sélectionnant le corps du modèle. Pour ce faire, cliquez sur le lien **[!UICONTROL Corps]** dans le rail de navigation situé en haut du volet de droite.

![](assets/template-lock-body.png)

### Verrouiller des structures {#lock-structures}

>[!CONTEXTUALHELP]
>id="ajo_locking_structure"
>title="Verrouillage du contenu dans la structure"
>abstract="Pour verrouiller la structure dans le modèle, sélectionnez **Verrouillé** dans la liste déroulante **Type de verrouillage**. Par défaut, les personnes ne peuvent pas supprimer les structures verrouillées. Vous pouvez contourner cette restriction en activant l’option **[!UICONTROL Autoriser la suppression]**."

Pour verrouiller une structure dans votre modèle :

1. Sélectionnez la structure à verrouiller.

1. Dans la liste déroulante **[!UICONTROL Type de verrouillage]**, sélectionnez **[!UICONTROL Verrouillé]**.

   ![](assets/template-lock-structure.png)

   >[!NOTE]
   >
   >Par défaut, les personnes ne peuvent pas supprimer les structures verrouillées. Vous pouvez contourner cette restriction en activant l’option **[!UICONTROL Autoriser la suppression]**.

Après le verrouillage d’une structure, aucun autre composant de contenu ou fragment ne peut être dupliqué ou ajouté à l’intérieur. Tous les composants d’une structure verrouillée sont également verrouillés par défaut. Pour rendre un composant modifiable dans une structure verrouillée :

1. Sélectionnez le composant que vous souhaitez déverrouiller.

1. Activez l’option **[!UICONTROL Utiliser un verrouillage spécifique]**.

1. Dans la liste déroulante **[!UICONTROL Type de verrouillage]**, sélectionnez **[!UICONTROL Modifiable]**. Pour autoriser la modification du contenu tout en verrouillant les styles, sélectionnez **[!UICONTROL Contenu modifiable uniquement]**. [Découvrir comment verrouiller des composants](#lock-components)

   ![](assets/template-lock-editable-component.png)

### Verrouillage des composants {#lock-components}

>[!CONTEXTUALHELP]
>id="ajo_locking_component"
>title="Utiliser un verrouillage spécifique dans le composant"
>abstract="Pour verrouiller le composant dans le modèle, activez l’option **Utiliser le verrouillage spécifique**. Dans la liste déroulante **[!UICONTROL Type de verrouillage]**, sélectionnez l’option de verrouillage souhaitée : **Verrouillage de contenu modifiable uniquement** permet de verrouiller les styles du composant tout en autorisant la modification du contenu, tandis que **Verrouillé** verrouille entièrement le contenu et les styles du composant."

Pour verrouiller un composant spécifique dans une structure :

1. Sélectionnez le composant et activez l’option **[!UICONTROL Utiliser un verrouillage spécifique]** dans le volet de droite.

1. Dans la liste déroulante **[!UICONTROL Type de verrouillage]**, sélectionnez l’option de verrouillage de votre choix :

   ![](assets/template-lock-component.png)

   * **[!UICONTROL Contenu modifiable uniquement]** : verrouille les styles du composant, mais permet de modifier le contenu.
   * **[!UICONTROL Verrouillé]** : verrouille entièrement le contenu et les styles du composant.

   >[!NOTE]
   >
   >Le type de verrouillage **[!UICONTROL Modifiable]** permet aux personnes de modifier un composant, même dans une structure verrouillée. [Découvrir comment verrouiller des structures](#lock-structures)

1. Par défaut, les personnes ne peuvent pas supprimer les composants verrouillés. Vous pouvez activer la suppression en activant l’option **[!UICONTROL Autoriser la suppression]**.

### Identification du contenu verrouillé {#identify}

Pour identifier facilement les structures et les composants verrouillés dans votre modèle, utilisez l’**[!UICONTROL arborescence de navigation]** située dans le menu de gauche. Ce menu présente une vue d’ensemble visuelle de tous les éléments de modèle, en mettant en surbrillance les éléments verrouillés avec une icône de verrouillage et les éléments modifiables avec une icône en forme de crayon.

Dans l’exemple ci-dessous, la gouvernance est activée pour le corps du modèle. *La structure 2* est verrouillée avec le *composant 1* modifiable, tandis que la *structure 3* est entièrement verrouillée.

![](assets/template-lock-navigation.png)

## Utilisation des modèles avec du contenu verrouillé {#use}

>[!CONTEXTUALHELP]
>id="ajo_email_editable_areas"
>title="Mettre en surbrillance les zones modifiables"
>abstract="Selon le type de verrouillage appliqué au modèle, vous pouvez effectuer différentes actions sur les structures et composants du modèle. Pour identifier rapidement toutes les zones modifiables dans le modèle, activez l’option **[!UICONTROL Mettre en surbrillance les zones modifiables]**."

Lors de l’utilisation d’un modèle avec du contenu verrouillé, un message s’affiche dans le volet de droite.

Selon le type de verrouillage appliqué au modèle, vous pouvez effectuer différentes actions sur les structures et composants du modèle. Pour identifier rapidement toutes les zones modifiables dans le modèle, activez l’option **[!UICONTROL Mettre en surbrillance les zones modifiables]**.

Par exemple, dans le modèle ci-dessous, toutes les zones sont modifiables, à l’exception de l’image du haut qui a été verrouillée, ce qui signifie que vous ne pouvez pas la modifier ni la supprimer.

![](assets/template-lock-highlight.png)

Pour plus d’informations sur les différents types de verrouillage qui peuvent être appliqués, consultez les sections suivantes :

* [Verrouiller des structures](#lock-structures)
* [Verrouillage des composants](#lock-components)

Voici quelques exemples de modifications d’e-mails et de configurations de verrouillage de contenu associées qui ont été appliquées :

| Type de verrouillage de contenu | Configuration des modèles | Modification d’e-mails |
| ------- | ------- | ------- |
| Modèle de contenu en lecture seule | ![](assets/locking-sample-read-only-conf.png){zoomable="yes"} | ![](assets/locking-sample-read-only.png){zoomable="yes"} |
| Le contenu complet est modifiable, mais les personnes ne peuvent pas ajouter de structure ou de composant. | ![](assets/locking-sample-no-addition-conf.png){zoomable="yes"} | ![](assets/locking-sample-no-addition.png){zoomable="yes"} |
| Structure verrouillée qui ne peut pas être supprimée. | ![](assets/locking-sample-structure-locked-conf.png){zoomable="yes"} | ![](assets/locking-sample-structure-locked.png){zoomable="yes"} |
| Composant avec des styles verrouillés et qui ne peut pas être supprimé. Les personnes peuvent uniquement modifier le contenu. | ![](assets/locking-sample-content-only-conf.png){zoomable="yes"} | ![](assets/locking-sample-content-only.png){zoomable="yes"} |
| Composant modifiable dans une structure verrouillée. | ![](assets/locking-sample-editable-component-conf.png){zoomable="yes"} | ![](assets/locking-sample-editable-component.png){zoomable="yes"} |

## Vidéo pratique {#video}

Découvrez comment verrouiller le contenu dans vos modèles d’e-mail.

>[!VIDEO](https://video.tv.adobe.com/v/3451591?quality=12)
