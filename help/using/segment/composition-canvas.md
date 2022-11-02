---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser la zone de travail de composition
description: Découvrez comment utiliser la zone de travail de composition
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: af59c7ed83f18932fe13791b50713eabfba3b549
workflow-type: tm+mt
source-wordcount: '1040'
ht-degree: 92%

---

# Utiliser la zone de travail de composition {#composition-canvas}

La zone de travail de composition est une zone de travail visuelle qui vous permet de créer des compositions en exploitant les audiences et les activités (partager, exclure..).

Les étapes de configuration d’une composition dans la zone de travail de composition sont les suivantes :

1. [Définir votre/vos audience(s) de départ](#starting-audience)
1. [Ajouter une ou plusieurs activités](#action-activities)
1. [Enregistrer les résultats dans une nouvelle audience](#save)

## Sélectionner l’audience de départ {#starting-audience}

La première étape pour créer une composition consiste à sélectionner une ou plusieurs audiences existantes comme base de votre composition.

1. Sélectionnez la **[!UICONTROL Audience]** puis fournissez un libellé pour l’activité.

1. Choisissez l&#39;audience à cibler :

   * Cliquez sur le bouton **[!UICONTROL Ajouter une audience]** pour sélectionner une ou plusieurs audiences existantes,
   * Cliquez sur le bouton **[!UICONTROL Créer une règle]** pour créer une définition de segment à l’aide du bouton [Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=fr).

   ![](assets/audiences-choose-audience.png)

1. Si plusieurs audiences sont sélectionnées, indiquez comment les profils de ces audiences doivent être fusionnés :

* **[!UICONTROL Union]** : inclure tous les profils des audiences sélectionnées,
* **[!UICONTROL Intersection]** : inclure des profils communs à toutes les audiences sélectionnées,
* **[!UICONTROL Exclure le chevauchement]** : inclure des profils qui appartiennent à l’une des audiences uniquement. Les profils appartenant à plusieurs audiences ne seront pas inclus.

Dans cet exemple, nous allons cibler tous les profils appartenant aux audiences Gold et Silver.

![](assets/audiences-starting-audience.png)

Une fois les audiences sélectionnées, le nombre estimé de profils s’affiche au bas de l’activité.

## Ajouter des activités {#action-activities}

Ajoutez des activités après avoir sélectionné l’audience de départ afin d’affiner votre sélection.

Pour cela, cliquez sur le bouton + du chemin de composition, puis sélectionnez l’activité souhaitée. Le volet de droite s’ouvre, vous permettant de configurer l’activité.

![](assets/audiences-select-activity.png)

>[!NOTE]
>
>Vous pouvez ajouter autant d’activités **[!UICONTROL Audience]** et **[!UICONTROL Exclure]** que vous le souhaitez à votre composition. Toutefois, aucune activité supplémentaire ne peut être ajoutée après les activités **[!UICONTROL Classement]** et **[!UICONTROL Partager]**.

Vous pouvez à tout moment supprimer une activité de la zone de travail en cliquant sur le bouton Supprimer dans le volet de droite. Toutes les activités ajoutées après cette activité seront également supprimées de la zone de travail.

Les activités disponibles sont les suivantes :

* [Audience](#audience) : inclure des profils supplémentaires appartenant à une ou plusieurs audiences existantes,
* [Exclure](#exclude) : exclure les profils appartenant à une audience existante ou exclure les profils en fonction d’attributs spécifiques,
* [Classement](#rank) : classer les profils en fonction d’un attribut spécifique, spécifier le nombre de profils à conserver et les inclure dans votre composition,
* [Partager](#split) : diviser votre composition en plusieurs chemins d’accès en fonction de pourcentages aléatoires ou d’attributs.

### Activité Audience {#audience}

>[!CONTEXTUALHELP]
>id="ajo_ao_audience"
>title="Activité Audience"
>abstract="L’activité Audience permet d’inclure dans votre composition des profils supplémentaires appartenant à une audience existante."

>[!CONTEXTUALHELP]
>id="ajo_ao_merge_types"
>title="Types de fusion"
>abstract="Indiquez le mode de fusion des profils des audiences sélectionnées."

L’activité **[!UICONTROL Audience]** vous permet d’inclure dans votre composition des profils supplémentaires appartenant à une audience existante.

La configuration de cette activité est identique à celle de l’[activité Audience](#starting-audience) de départ.

### Exclure l’activité {#exclude}

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude_type"
>title="Type d’exclusion"
>abstract="Utilisez le type Exclure l’audience pour exclure les profils appartenant à une audience existante. Le type Exclure en utilisant l’attribut permet d’exclure des profils en fonction d’un attribut spécifique."

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude"
>title="Exclure l’activité"
>abstract="L’activité Exclure permet d’exclure des profils de votre composition en sélectionnant une audience existante ou en utilisant une règle."

L’activité **[!UICONTROL Exclure]** vous permet d’exclure des profils de votre composition. Deux types d’exclusions sont disponibles :

* **[!UICONTROL Exclure l’audience]** : exclure les profils appartenant à une audience existante.

   Cliquez sur le bouton **[!UICONTROL Ajouter une audience]** puis sélectionnez l’audience à exclure.

   ![](assets/audiences-exclude-audience.png)

* **[!UICONTROL Exclure en utilisant l’attribut]** : exclure des profils en fonction d’un attribut spécifique.

   Sélectionnez l’attribut à rechercher, puis spécifiez la valeur à exclure. Dans cet exemple, nous excluons des profils de composition dont l’adresse de domicile est au Japon.

   ![](assets/audiences-exclude-attribute.png)

### Activité Classement {#rank}

>[!CONTEXTUALHELP]
>id="ajo_ao_ranking"
>title="Activité de classement"
>abstract="L’activité Classement vous permet de classer les profils en fonction d’un attribut spécifique et de les inclure dans votre composition. Par exemple, incluez les 50 profils présentant le plus grand nombre de points de fidélité."

>[!CONTEXTUALHELP]
>id="ajo_ao_rank_profilelimit_text"
>title="Ajouter une limite de profil"
>abstract="Activez cette option pour spécifier un nombre maximum de profils à inclure dans la composition."

L’activité **[!UICONTROL Classement]** vous permet de classer les profils en fonction d’un attribut spécifique et de les inclure dans votre composition. Vous pouvez, par exemple, inclure les 50 profils présentant le plus grand nombre de points de fidélité.

1. Sélectionnez l’attribut que vous souhaitez rechercher et indiquez un ordre de classement (ascendant ou descendant).

   >[!NOTE]
   >
   >Vous pouvez sélectionner des attributs avec les types de données suivants : entiers, nombres, courts <!--(other?)-->

1. Activez l’option **[!UICONTROL Ajouter une limite de profil]** et indiquez un nombre maximum de profils à inclure dans la composition.

   ![](assets/audiences-rank.png)

### Activité Partage {#split}

>[!CONTEXTUALHELP]
>id="ajo_ao_control_group_text"
>title="Population témoin"
>abstract="Utilisez les populations témoins pour isoler une partie des profils. Vous pouvez ainsi mesurer l’impact d’une activité de marketing et faire une comparaison avec le comportement du reste de la population."

>[!CONTEXTUALHELP]
>id="ajo_ao_split"
>title="Activité Partage"
>abstract="L’activité Partage permet de diviser votre composition en plusieurs chemins d’accès. Lors de la publication de la composition, une audience est enregistrée dans Adobe Experience Platform pour chaque chemin d’accès."

>[!CONTEXTUALHELP]
>id="ajo_ao_split_type"
>title="Type Partage"
>abstract="Utilisez le type Partage en pourcentage pour partager les profils de manière aléatoire en plusieurs chemins d’accès. Le type de partage des attributs permet de partager les profils en fonction d’un attribut spécifique."

>[!CONTEXTUALHELP]
>id="ajo_ao_split_otherprofiles_text"
>title="Autres profils"
>abstract="Activez cette option pour créer un chemin d’accès supplémentaire avec les profils restants qui ne correspondent à aucune des conditions spécifiées dans les autres chemins d’accès."

L’activité **[!UICONTROL Partage]** vous permet de diviser votre composition en plusieurs chemins d’accès.

Cette opération ajoute automatiquement une activité **[!UICONTROL Enregistrer]** à la fin de chaque chemin d’accès. Lors de la publication de la composition, une audience est enregistrée dans Adobe Experience Platform pour chaque chemin d’accès.

Deux types d’opérations de partage sont disponibles :

* **[!UICONTROL Partage en pourcentage]** : il s’agit de partager les profils de manière aléatoire en deux ou plusieurs chemins d’accès. Par exemple, vous pouvez partager les profils en 2 chemins d’accès distincts de 45 % chacun, et ajouter un chemin d’accès supplémentaire pour la population témoin.

   ![](assets/audiences-split-percentage.png)

* **[!UICONTROL Partage d’attributs]** : il s’agit de partager les profils en fonction d’un attribut spécifique. Dans cet exemple, nous partagerons les profils en fonction de leurs préférences de type de chambre.

   ![](assets/audiences-split.png)

   >[!NOTE]
   >
   >L’option **[!UICONTROL Autres profils]** vous permet de créer un chemin d’accès supplémentaire avec les profils restants qui ne correspondent à aucune des conditions spécifiées dans les autres chemins d’accès.

## Enregistrer vos audiences {#save}

Configurez les audiences qui seront enregistrées dans Adobe Experience Platform.

Pour ce faire, sélectionnez l’activité **[!UICONTROL Enregistrer l’audience]** à la fin de chaque chemin d’accès, puis spécifiez le nom de la nouvelle audience à créer.

![](assets/audiences-publish.png)

Une fois votre composition prête, vous pouvez la publier. [Découvrez comment créer des compositions.](create-compositions.md)

En savoir plus :

* [Prise en main de la composition des audiences](get-started-audience-orchestration.md)
* [Créer des workflows de composition](create-compositions.md)
* [Accéder aux audiences et les gérer](access-audiences.md)
