---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser des attributs calculés
description: Découvrez comment utiliser des attributs calculés.
feature: Profiles
role: User
level: Beginner
exl-id: 5402a179-263f-46a7-bddf-5b7017cf0f82
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 6%

---

# Utiliser des attributs calculés {#computed-attributes}

Les attributs calculés vous permettent de résumer des événements comportementaux individuels en attributs de profil calculés disponibles sur Adobe Experience Platform. Ces attributs calculés sont basés sur des jeux de données d’événement d’expérience activés pour le profil ingérés dans Adobe Experience Platform et servent de points de données agrégés stockés dans les profils client.

Chaque attribut calculé est un attribut de profil que vous pouvez exploiter pour la segmentation, la personnalisation et l’activation dans les parcours et les campagnes. Cette simplification permet à vos clients d’offrir des expériences personnalisées pertinentes et opportunes.

>[!NOTE]
>
>Pour accéder aux attributs calculés, vous devez disposer des autorisations appropriées (**Affichage des attributs calculés** et **Gestion des attributs calculés**).

## Création d’attributs calculés {#manage}

Pour créer des attributs calculés, accédez au **[!UICONTROL Attributs calculés]** dans le **[!UICONTROL Profils]** situé sur le côté gauche.

Dans cet écran, vous pouvez créer des attributs calculés en créant des règles qui combinent des attributs d’événement, des fonctions d’agrégat, au cours d’une période de recherche en amont spécifiée. Par exemple, vous pouvez calculer la somme des achats effectués au cours des trois derniers mois, identifier l’article le plus récent consulté par un profil qui n’a effectué aucun achat au cours de la dernière semaine ou calculer le total des points de récompense cumulés par chaque profil.

![](assets/computed-attributes.png)

Une fois votre règle prête, publiez l’attribut calculé pour le rendre disponible dans d’autres services en aval, y compris Journey Optimizer.

Des informations détaillées sur la création et la gestion des attributs calculés sont disponibles dans la section [Documentation sur les attributs calculés](https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html?lang=fr)

## Ajout d’attributs calculés à la source de données Adobe Experience Platform {#source}

Pour pouvoir exploiter les attributs calculés dans Journey Optimizer, vous devez d’abord les ajouter à Journey Optimizer. **Experience Platform** source de données.

La source de données Adobe Experience Platform définit la connexion au profil client en temps réel d’Adobe. Cette source de données est conçue pour récupérer les données de profil et les données d’événements d’expérience du service de profil client en temps réel.

Pour ajouter des attributs calculés à la source de données, procédez comme suit :

1. Accédez au **[!UICONTROL Configurations]** dans le menu de gauche, puis cliquez sur le bouton **[!UICONTROL Sources de données]** carte.

1. Sélectionnez la variable **[!UICONTROL Experience Platform]** source de données.

   ![](assets/computed-attributes-add.png)

1. Ajoutez la variable **[!UICONTROL SystemComputedAttributes]** groupe de champs contenant tous les attributs calculés créés.

   ![](assets/computed-attributes-fieldgroup.png)

Les attributs calculés peuvent désormais être utilisés dans Journey Optimizer. [Découvrez comment utiliser les attributs calculés dans Journey Optimizer](#use)

Vous trouverez des informations détaillées sur l’ajout de groupes de champs à la source de données Adobe Experience Platform dans la section [cette section](../datasource/adobe-experience-platform-data-source.md).

## Utilisation d’attributs calculés dans Journey Optimizer {#use}

>[!NOTE]
>
>Avant de commencer, assurez-vous d’avoir ajouté vos attributs calculés dans la source de données Adobe Experience Platform. [Découvrez comment dans cette section](#source).

Les attributs calculés offrent un ensemble polyvalent de fonctionnalités dans l’optimiseur de Parcours. Vous pouvez les utiliser à diverses fins, par exemple pour personnaliser le contenu d’un message, créer de nouvelles audiences ou diviser les parcours en fonction d’un attribut calculé spécifique. Par exemple, vous pouvez fractionner le chemin d’un parcours en fonction du total des achats d’un profil au cours des trois dernières semaines, en ajoutant un seul attribut calculé dans une activité Condition . Vous pouvez également personnaliser un email en affichant l’article le plus récemment consulté pour chaque profil.

Puisque les attributs calculés sont des champs d’attribut de profil créés sur votre schéma d’union de profil, vous pouvez y accéder à partir de l’éditeur d’expression dans la variable **SystemComputedAttributes** groupe de champs. À partir de là, vous pouvez ajouter un attribut calculé dans vos expressions, en les traitant comme tout autre attribut de profil pour effectuer les opérations souhaitées.

![](assets/computed-attributes-ajo.png)
