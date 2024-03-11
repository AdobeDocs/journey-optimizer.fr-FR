---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser la zone de travail de composition
description: Découvrez comment utiliser la zone de travail de composition
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: 3eb9466e-9d88-4470-a22f-5e24a29923ae
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: ht
source-wordcount: '1521'
ht-degree: 100%

---

# Utiliser la zone de travail de composition {#composition-canvas}

>[!BEGINSHADEBOX]

Cette documentation fournit des informations détaillées sur l’utilisation de la composition de l’audience dans Adobe Journey Optimizer. Si vous n’utilisez pas Adobe Journey Optimizer, [cliquez ici](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=fr){target="_blank"}.

>[!ENDSHADEBOX]

La composition de l’audience met à votre disposition une zone de travail visuelle qui vous permet de créer des audiences et d’utiliser plusieurs activités (partage, enrichissement, etc.).

Pour composer une audience dans la zone de travail, procédez comme suit :

1. [Définir votre/vos audience(s) de départ](#starting-audience)
1. [Ajouter une ou plusieurs activités](#action-activities)
1. [Enregistrer les résultats dans une nouvelle audience](#save)

## Sélectionner l’audience de départ {#starting-audience}

La première étape pour créer une composition consiste à sélectionner une ou plusieurs audiences existantes comme base de votre composition.

1. Sélectionnez l’activité **[!UICONTROL Audience]**, puis fournissez un libellé pour l’activité.

1. Choisissez l’audience à cibler :

   * Cliquez sur le bouton **[!UICONTROL Ajouter une audience]** pour sélectionner une ou plusieurs audiences existantes,
   * Cliquez sur le bouton **[!UICONTROL Créer une règle]** pour créer une définition d’audience à l’aide du [service de segmentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=fr).

   ![](assets/audiences-choose-audience.png)

1. Si vous sélectionnez plusieurs audiences, indiquez comment les profils de ces audiences doivent être fusionnés :

* **[!UICONTROL Union]** : inclure tous les profils des audiences sélectionnées,
* **[!UICONTROL Intersection]** : inclure des profils communs à toutes les audiences sélectionnées,
* **[!UICONTROL Exclure le chevauchement]** : inclure des profils qui appartiennent à l’une des audiences uniquement. Les profils appartenant à plusieurs audiences ne seront pas inclus.

Dans cet exemple, nous allons cibler tous les profils appartenant aux audiences Gold et Silver.

![](assets/audiences-starting-audience.png)

Une fois les audiences sélectionnées, le nombre estimé de profils s’affiche au bas de l’activité.

## Ajouter des activités {#action-activities}

Ajoutez des activités après avoir sélectionné l’audience de départ afin d’affiner votre sélection.

Pour cela, cliquez sur le bouton + du chemin de composition, puis sélectionnez l’activité souhaitée. Le volet de droite s’ouvre et vous permet de configurer l’activité que vous venez d’ajouter.

![](assets/audiences-select-activity.png)

Les activités disponibles sont les suivantes :

* [Audience](#audience) : inclure des profils supplémentaires appartenant à une ou plusieurs audiences existantes,
* [Exclure](#exclude) : exclure les profils appartenant à une audience existante ou exclure les profils en fonction d’attributs spécifiques,
* [Enrichir](#enrich) : enrichissez votre audience avec des attributs supplémentaires issus des jeux de données d’Adobe Experience Platform,
* [Classement](#rank) : classer les profils en fonction d’un attribut spécifique, spécifier le nombre de profils à conserver et les inclure dans votre composition,
* [Partager](#split) : diviser votre composition en plusieurs chemins d’accès en fonction de pourcentages aléatoires ou d’attributs.

Vous pouvez ajouter autant d’activités **[!UICONTROL Audience]** et **[!UICONTROL Exclure]** que vous le souhaitez à votre composition. Toutefois, aucune activité supplémentaire ne peut être ajoutée après les activités **[!UICONTROL Classement]** et **[!UICONTROL Partager]**.

Vous pouvez à tout moment supprimer une activité de la zone de travail en cliquant sur le bouton Supprimer dans le volet de droite.  Si l’activité que vous souhaitez supprimer est parente d’autres activités de la composition, un message s’affiche et vous permet d’indiquer si vous souhaitez supprimer uniquement l’activité sélectionnée ou toutes les activités enfants.

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

  >[!NOTE]
  >
  >Une seule valeur d’exclusion peut être spécifiée.

  ![](assets/audiences-exclude-attribute.png)

### Activité Enrichir {#enrich}

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich"
>title="Activité Enrichir"
>abstract="Utilisez l’activité Enrichir pour enrichir votre audience avec des attributs supplémentaires provenant de jeux de données d’Adobe Experience Platform. Par exemple, vous pouvez ajouter des informations sur le produit acheté (comme le nom, le prix ou l’identifiant de fabricant) afin de personnaliser les diffusions envoyées à l’audience."

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_dataset"
>title="Jeu de données d’enrichissement"
>abstract="Sélectionnez le jeu de données d’enrichissement contenant les données à associer à l’audience."

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_criteria"
>title="Critères d’enrichissement"
>abstract="Sélectionnez les champs à utiliser comme clé de réconciliation entre le jeu de données source (l’audience) et le jeu de données d’enrichissement."

>[!CONTEXTUALHELP]
>id="ajo_ao_enrich_attributes"
>title="Attributs d’enrichissement"
>abstract="Sélectionnez un ou plusieurs attributs du jeu de données d’enrichissement à associer à l’audience. Une fois la composition publiée, ces attributs sont associés à l’audience. Ils peuvent ensuite être utilisés dans les campagnes Journey Optimizer pour personnaliser les diffusions."

L’activité **[!UICONTROL Enrichir]** vous permet d’enrichir votre audience avec des attributs supplémentaires provenant de jeux de données d’Adobe Experience Platform. Par exemple, vous pouvez ajouter des informations sur le produit acheté (comme le nom, le prix ou l’identifiant de fabricant) afin de personnaliser les diffusions envoyées à l’audience.

Notez les limitations suivantes lorsque vous utilisez l’activité **[!UICONTROL Enrichir]** :

* Les **Jeux de données** pour l’enrichissement doivent être de type enregistrement (contrairement à un type d’événement) et il ne peut pas s’agir d’un jeu de données système ni être marqué pour le profil. Ils doivent être inférieurs à 1 Go.
* **L’enrichissement prend en charge une jointure 1:1**. Cela signifie que si les clés de jointure comportent plusieurs correspondances sur le jeu de données d’enrichissement, le système sélectionne l’une des correspondances et l’utilise pour la jointure 1:1.
* **Les audiences peuvent être activées dans les destinations RTCDP**, mais pas leurs attributs d’enrichissement, le cas échéant.
* Les attributs d’enrichissement ne sont pas encore intégrés au service d’application des politiques. Par conséquent, les libellés d’utilisation des données que vous appliquez à vos attributs d’enrichissement ne sont pas implémentés dans les campagnes et les parcours Journey Optimizer.

Pour configurer l’activité, procédez comme suit :

1. Sélectionnez le **[!UICONTROL Jeu de données d’enrichissement]** contenant les données que vous souhaitez associer à l’audience.

1. Dans la section **[!UICONTROL Critères d’enrichissement]**, sélectionnez les champs à utiliser comme clé de réconciliation entre le jeu de données source (l’audience) et le jeu de données d’enrichissement. Dans cet exemple, la clé de réconciliation est l’identifiant du produit acheté.

1. Cliquez sur le bouton **[!UICONTROL Ajouter des attributs]**, puis sélectionnez un ou plusieurs attributs du jeu de données d’enrichissement à associer à l’audience.

   ![](assets/audiences-enrich-activity.png)

Une fois la composition publiée, les attributs sélectionnés sont associés à l’audience et peuvent être utilisés dans les campagnes pour personnaliser les diffusions.

### Activité Classement {#rank}

>[!CONTEXTUALHELP]
>id="ajo_ao_ranking"
>title="Activité Classement"
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

<!-- [!CONTEXTUALHELP]
>id="ajo_ao_control_group_text"
>title="Control Group"
>abstract="Use control groups to isolate a portion of the profiles. This allows you to measure the impact of a marketing activity and make a comparison with the behavior of the rest of the population."-->

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

* **[!UICONTROL Partage en pourcentage]** : il s’agit de partager les profils de manière aléatoire en deux ou plusieurs chemins d’accès. Par exemple, vous pouvez partager les profils en 2 chemins distincts de 50 % chacun. <!--and add an additional path for control group.-->

  ![](assets/audiences-split-percentage.png)

* **[!UICONTROL Partage d’attributs]** : il s’agit de partager les profils en fonction d’un attribut spécifique. Dans cet exemple, nous partagerons les profils en fonction de leurs préférences de type de chambre.

  ![](assets/audiences-split.png)

  Pour configurer une activité de partage basée sur des attributs, procédez comme suit :

   1. Cliquez sur le bouton situé en regard du champ **[!UICONTROL Attribut]** pour sélectionner l’attribut à utiliser comme critère de partage.
   1. Ajoutez autant de chemins que nécessaire. Pour chaque chemin, fournissez un libellé et spécifiez la valeur qui sera utilisée pour déterminer les profils à inclure dans ce chemin spécifique.

      >[!NOTE]
      >
      >Une seule valeur peut être spécifiée pour chaque chemin.

   1. L’option **[!UICONTROL Autres profils]** vous permet de créer un chemin d’accès supplémentaire avec les profils restants qui ne correspondent à aucune des conditions spécifiées dans les autres chemins d’accès.

## Enregistrer vos audiences {#save}

Configurez les audiences qui seront enregistrées dans Adobe Experience Platform.

Pour ce faire, sélectionnez l’activité **[!UICONTROL Enregistrer l’audience]** à la fin de chaque chemin d’accès, puis spécifiez le nom de la nouvelle audience à créer.

![](assets/audiences-publish.png)

Une fois votre composition prête, vous pouvez la publier. [Découvrez comment créer des compositions.](create-compositions.md)
