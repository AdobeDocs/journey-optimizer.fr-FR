---
title: Utilisation du canevas de composition
description: Découvrez comment utiliser le canevas de composition
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: a51b41ddbb562137dc1f6cf15160ce326cc0564a
workflow-type: tm+mt
source-wordcount: '945'
ht-degree: 0%

---

# Utilisation du canevas de composition {#composition-canvas}

Le canevas de composition est un canevas visuel qui vous permet de créer des compositions en exploitant les audiences et les activités (fractionner, exclure..).

Les étapes de configuration d’une composition dans la zone de travail de composition sont les suivantes :

1. [Définition des audiences de départ](#starting-audience)
1. [Ajouter une ou plusieurs activités](#action-activities)
1. [Enregistrer les résultats dans une nouvelle audience](#save)

## Sélectionner l’audience de départ {#starting-audience}

>[!CONTEXTUALHELP]
>id="ajo_ao_merge_types"
>title="Types de fusion"
>abstract="Indiquez le mode de fusion des profils des audiences sélectionnées."

La première étape pour créer une composition consiste à sélectionner une ou plusieurs audiences existantes comme base de votre composition.

Sélectionnez la **[!UICONTROL Audience]** puis cliquez sur l’activité **[!UICONTROL Ajouter une audience]** puis sélectionnez une ou plusieurs audiences.

Dans cet exemple, nous allons cibler tous les profils appartenant aux audiences Or et Argent.

![](assets/audiences-starting-audience.png)

Si vous sélectionnez plusieurs audiences, indiquez comment les profils de ces audiences doivent être fusionnés :

* **[!UICONTROL Union]**: inclure tous les profils des audiences sélectionnées,
* **[!UICONTROL Intersection]**: inclure des profils communs à toutes les audiences sélectionnées,
* **[!UICONTROL Exclure le chevauchement]**: incluent des profils qui appartiennent à l’une des audiences uniquement. Les profils appartenant à plusieurs audiences ne seront pas inclus.

## Ajouter des activités {#action-activities}

Ajoutez des activités après avoir sélectionné l’audience de départ afin d’affiner votre sélection.

Pour cela, cliquez sur le bouton + du chemin de composition, puis sélectionnez l’activité souhaitée. Le volet de droite s’ouvre, vous permettant de configurer l’activité.

![](assets/audiences-select-activity.png)

>[!NOTE]
>
>Vous pouvez ajouter autant de **[!UICONTROL Audience]** et **[!UICONTROL Exclure]** activités selon les besoins dans votre composition. Toutefois, aucune activité supplémentaire ne peut être ajoutée après **[!UICONTROL Classement]** et **[!UICONTROL Partage]** activités.

Vous pouvez à tout moment supprimer une activité de la zone de travail en cliquant sur le bouton de suppression dans le volet de droite. Toutes les activités ajoutées après cette activité seront également supprimées de la zone de travail.

Les activités disponibles sont les suivantes :

* [Audience](#audience): inclure des profils supplémentaires appartenant à une ou plusieurs audiences existantes,
* [Exclure](#exclude): exclure les profils appartenant à une audience existante ou exclure les profils en fonction d&#39;attributs spécifiques,
* [Classement](#rank): classer les profils en fonction d’un attribut spécifique, spécifier le nombre de profils à conserver et les inclure dans votre composition,
* [Partage](#split): divisez votre composition en plusieurs chemins d’accès en fonction de pourcentages aléatoires ou d’attributs.

### Activité Audience {#audience}

>[!CONTEXTUALHELP]
>id="ajo_ao_audience"
>title="Activité Audience"
>abstract="L&#39;activité Audience permet d&#39;inclure dans votre composition des profils supplémentaires appartenant à une audience existante."

Le **[!UICONTROL Audience]** activité vous permet d’inclure dans votre composition des profils supplémentaires appartenant à une audience existante.

Le paramétrage de cette activité est identique à celui du début [Activité Audience](#starting-audience).

### Exclure l’activité {#exclude}

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude_type"
>title="Type d’exclusion"
>abstract="Utilisez le type Exclure l&#39;audience pour exclure les profils appartenant à une audience existante. Le type d’attribut Exclure à l’aide permet d’exclure des profils en fonction d’un attribut spécifique."

>[!CONTEXTUALHELP]
>id="ajo_ao_exclude"
>title="Exclure l’activité"
>abstract="L&#39;activité Exclure permet d&#39;exclure des profils de votre composition en sélectionnant une audience existante ou en utilisant une règle."

Le **[!UICONTROL Exclure]** L’activité vous permet d’exclure des profils de votre composition. Deux types d’exclusion sont disponibles :

* **[!UICONTROL Exclure l’audience]**: Exclure les profils appartenant à une audience existante.

   Cliquez sur le bouton **[!UICONTROL Ajouter une audience]** puis sélectionnez l’audience à exclure.

   ![](assets/audiences-exclude-audience.png)

* **[!UICONTROL Exclure à l’aide d’un attribut]**: Exclure des profils en fonction d’un attribut spécifique.

   Sélectionnez l’attribut à rechercher, puis spécifiez la valeur à exclure. Dans cet exemple, nous excluons des profils de composition dont l’adresse de domicile est au Japon.

   ![](assets/audiences-exclude-attribute.png)

### Activité de classement a {#rank}

>[!CONTEXTUALHELP]
>id="ajo_ao_ranking"
>title="Activité de classement"
>abstract="L&#39;activité Classement permet de classer les profils en fonction d&#39;un attribut spécifique et de les inclure dans votre composition. Par exemple, incluez les 50 profils présentant le plus grand nombre de points de fidélité."

Le **[!UICONTROL Classement]** L’activité vous permet de classer les profils en fonction d’un attribut spécifique et de les inclure dans votre composition. Vous pouvez, par exemple, inclure les 50 profils présentant le plus grand nombre de points de fidélité.

1. Sélectionnez l’attribut que vous souhaitez rechercher et indiquez un ordre de classement (ascendant ou descendant).

   >[REMARQUE]
   >
   >Vous pouvez sélectionner des attributs avec les types de données suivants : entier, nombres, court <!--(other?)-->

1. Activez/désactivez la variable **[!UICONTROL Ajouter une limite de profil]** sur et indiquez un nombre maximum de profils à inclure dans la composition.

   ![](assets/audiences-rank.png)

### Activité Partage {#split}

>[!CONTEXTUALHELP]
>id="ajo_ao_control_group_text"
>title="Le groupe de contrôle doit être"
>abstract="Utilisez les populations témoins pour isoler une partie des profils. Vous pouvez ainsi mesurer l’impact d’une activité marketing et faire une comparaison avec le comportement du reste de la population."

>[!CONTEXTUALHELP]
>id="ajo_ao_split"
>title="Activité Partage"
>abstract="L&#39;activité Partage permet de diviser votre composition en plusieurs chemins. Lors de la publication de la composition, une audience est enregistrée dans Adobe Experience Platform pour chaque chemin."

>[!CONTEXTUALHELP]
>id="ajo_ao_split_type"
>title="Type de partage"
>abstract="Utilisez le type Division en pourcentage pour fractionner les profils de manière aléatoire en plusieurs chemins. Le type de partage Attribut permet de fractionner les profils en fonction d’un attribut spécifique."

Le **[!UICONTROL Partage]** L’activité vous permet de diviser votre composition en plusieurs chemins.

Cette opération ajoute automatiquement une **[!UICONTROL Enregistrer]** à la fin de chaque chemin. Lors de la publication de la composition, une audience est enregistrée dans Adobe Experience Platform pour chaque chemin.

Deux types d’opérations de partage sont disponibles :

* **[!UICONTROL Division en pourcentage]**: fractionner les profils de manière aléatoire en deux chemins ou plus. Par exemple, vous pouvez fractionner les profils en 2 chemins distincts de 45 % chacun, et ajouter un chemin supplémentaire pour la population témoin.

   ![](assets/audiences-split-percentage.png)

* **[!UICONTROL Partage d’attributs]**: fractionner les profils en fonction d’un attribut spécifique. Dans cet exemple, nous partitionnons les profils en fonction de leurs préférences de type de chambre.

   ![](assets/audiences-split.png)

   >[!NOTE]
   >
   >Le **[!UICONTROL Autres profils]** vous permet de créer un chemin d’accès supplémentaire avec les profils restants qui ne correspondent à aucune des conditions spécifiées dans les autres chemins.

## Enregistrement de vos audiences {#save}

Configurez les audiences qui seront enregistrées dans Adobe Experience Platform.

Pour ce faire, sélectionnez la variable **[!UICONTROL Sauvegarde d’audience]** à la fin de chaque chemin, puis spécifiez le nom de la nouvelle audience à créer.

![](assets/audiences-publish.png)

Une fois votre composition prête, vous pouvez la publier. [Découvrez comment créer des compositions](create-compositions.md)

En savoir plus:

* [Prise en main de la composition de l’audience](get-started-audience-orchestration.md)
* [Création de workflows de composition](create-compositions.md)
* [Accès et gestion des audiences](access-audiences.md)
