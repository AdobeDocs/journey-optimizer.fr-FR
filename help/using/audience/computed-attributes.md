---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser des attributs calculés
description: Découvrez comment utiliser des attributs calculés.
feature: Audiences, Profiles
role: User
level: Intermediate
exl-id: 5402a179-263f-46a7-bddf-5b7017cf0f82
TQID: https://experienceleague.adobe.com/bH8UDdjWsh1Kle1ltVP2ltgXcNJDfVIdTuFdGWSZv6Y
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2: id: f42b4d14-fe8a-428b-b62e-e7995eaab1b3id: b32bb433-f8c6-4931-8e52-e657230a3bf2id: e95b6013-acbe-46e9-a3b5-b80e14088d7d
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: e0eb8757-182f-49f3-94a4-1587d16f5094id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1012
ht-degree: 51%

---

# Utiliser des attributs calculés {#computed-attributes}

>[!BEGINSHADEBOX]

**Sur cette page :** Découvrez comment créer des attributs calculés qui agrègent les événements comportementaux en attributs de profil et les utiliser pour la segmentation, la personnalisation et la logique de parcours dans Adobe Journey Optimizer.

>[!ENDSHADEBOX]

Les attributs calculés résument les événements comportementaux individuels en attributs de profil calculés disponibles dans Adobe Experience Platform. Ces attributs sont basés sur des jeux de données d’événements d’expérience compatibles avec les profils, ingérés dans Adobe Experience Platform, et servent de points de données agrégés stockés dans les profils clients.

Chaque attribut calculé est un attribut de profil que vous pouvez exploiter pour la segmentation, la personnalisation et l’activation dans les parcours et les campagnes. Cette simplification permet à vos clientes et clients d’offrir des expériences personnalisées pertinentes et opportunes.


![](../rn/assets/do-not-localize/computed-attributes.gif)


>[!NOTE]
>
>Pour accéder aux attributs calculés, assurez-vous de disposer des autorisations appropriées (**Afficher les attributs calculés** et **Gérer les attributs calculés**).

## Créer des attributs calculés {#manage}

Pour créer des attributs calculés, accédez à l’onglet **[!UICONTROL Attributs calculés]** dans le menu **[!UICONTROL Profils]** situé à gauche.

Dans cet écran, vous pouvez créer des attributs calculés en créant des règles qui combinent des attributs d’événement, des fonctions d’agrégat, ainsi qu’une période de recherche en amont spécifiée. Par exemple, vous pouvez calculer la somme des achats effectués au cours des trois derniers mois, identifier l’article le plus récent consulté par un profil qui n’a effectué aucun achat au cours de la dernière semaine ou calculer le total des points de récompense cumulés par chaque profil.

![](assets/computed-attributes.png)

Une fois votre règle prête, publiez l’attribut calculé pour le rendre disponible dans d’autres services en aval, y compris dans Journey Optimizer.

Des informations détaillées sur la création et la gestion des attributs calculés sont disponibles dans la [documentation sur les attributs calculés](https://experienceleague.adobe.com/docs/experience-platform/profile/computed-attributes/overview.html?lang=fr).

## Ajouter des attributs calculés à la source de données Adobe Experience Platform {#source}

Pour utiliser les attributs calculés dans Journey Optimizer, ajoutez-les à la source de données **Experience Platform** de Journey Optimizer.

La source de données Adobe Experience Platform définit la connexion au profil client en temps réel d’Adobe. Cette source de données récupère les données de profil et les données d’événements d’expérience à partir du service de profil client en temps réel.

Pour ajouter des attributs calculés à la source de données, procédez comme suit :

1. Accédez au menu de gauche **[!UICONTROL Configurations]**, puis cliquez sur la vignette **[!UICONTROL Sources de données]**.

1. Sélectionnez la source de données **[!UICONTROL Experience Platform]**.

   ![](assets/computed-attributes-add.png)

1. Ajoutez le groupe de champs **[!UICONTROL Attributs calculés sytème]** contenant tous les attributs calculés créés.

   ![](assets/computed-attributes-fieldgroup.png)

Les attributs calculés peuvent désormais être utilisés dans Journey Optimizer. [Découvrez comment utiliser les attributs calculés dans Journey Optimizer.](#use)

Des informations détaillées sur l’ajout de groupes de champs à la source de données Adobe Experience Platform sont disponibles dans [cette section](../datasource/adobe-experience-platform-data-source.md).

## Utiliser les attributs calculés dans Journey Optimizer {#use}

>[!NOTE]
>
>Avant de commencer, assurez-vous d’avoir ajouté vos attributs calculés à la source de données Adobe Experience Platform. [Découvrez comment dans cette section](#source).

Les attributs calculés offrent des fonctionnalités polyvalentes dans Journey Optimizer. Utilisez-les à diverses fins, comme personnaliser le contenu des messages, créer de nouvelles audiences, ou partager les parcours selon un attribut calculé spécifique. Par exemple, partagez le chemin d’un parcours en fonction du nombre total d’achats d’un profil au cours des trois dernières semaines en ajoutant un seul attribut calculé dans une activité Condition. Vous pouvez également personnaliser un e-mail en affichant l’article le plus récemment consulté pour chaque profil.

Puisque les attributs calculés sont des champs d’attribut de profil créés sur votre schéma d’union des profils, accédez-y depuis l’éditeur de personnalisation dans le groupe de champs **SystemComputedAttributes**. À partir de là, ajoutez les attributs calculés à vos expressions, en les traitant comme n’importe quel autre attribut de profil, afin d’effectuer les opérations souhaitées.

![](assets/computed-attributes-ajo.png)

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

- **TL;DR:** Découvrez comment créer des attributs calculés sur Adobe Experience Platform et les exploiter dans Journey Optimizer pour la segmentation, la personnalisation et la logique de parcours.

**Intentions:**
- Découvrez ce que sont les attributs calculés et en quoi ils diffèrent des attributs de profil standard
- Créez des attributs calculés en combinant des attributs d’événement, des fonctions d’agrégat et une période de recherche en amont
- Ajoutez le groupe de champs SystemComputedAttributes à la source de données Experience Platform dans AJO
- Utilisez des attributs calculés dans les conditions de parcours, la création d’audiences et la personnalisation des messages

**Glossaire:**
- **Attribut calculé** : attribut de profil dérivé de données d’événement comportemental agrégées, stocké dans les profils client *(spécifiques au produit)*
- **Période de recherche en amont** : période appliquée lors du calcul de la règle d’agrégation d’un attribut calculé (par exemple, « 3 derniers mois ») *(spécifique au produit)*
- **Groupe de champs SystemComputedAttributes** : groupe de champs de la source de données AJO Experience Platform qui expose tous les attributs calculés publiés à utiliser dans les parcours et les *de personnalisation (spécifiques au produit)*
- **Schéma d’union des profils** : schéma fusionné qui combine tous les fragments de profil pour une identité donnée, où sont stockés les attributs calculés

**Mécanismes de sécurisation :**
- Nécessite des autorisations **Afficher les attributs calculés** et **Gérer les attributs calculés** pour accéder à la fonctionnalité
- Les attributs calculés doivent être **publiés** dans AEP avant d’être disponibles en aval dans Journey Optimizer
- Les attributs calculés doivent être explicitement ajoutés à la source de données **** dans AJO avant de pouvoir être utilisés dans les parcours ou la personnalisation
- Les attributs calculés sont basés sur des jeux de données d’événements d’expérience activés pour Profile ingérés dans Adobe Experience Platform

**Terminologie:**
- Nom canonique : Adobe Journey Optimizer — Acronyme : AJO — Variantes : Journey Optimizer, A-JO
- Nom canonique : Adobe Experience Platform — Acronyme : AEP
- Synonymes : « attributs calculés » = « attributs de profil calculés »
- Ne les confondez pas : « attributs calculés » (fonctionnalité agrégée spécifique à AEP/AJO) ≠ « attributs de profil » génériques

**FAQ:**
- **Q : Que sont les attributs calculés ?** : données comportementales agrégées relatives aux événements (par exemple, total des achats, dernier élément consulté) stockées en tant qu’attributs de profil sur AEP et utilisables dans AJO.
- **Q : Ai-je besoin d’autorisations spéciales ?** — Oui : les options « Afficher les attributs calculés » et « Gérer les attributs calculés » sont toutes deux requises.
- **Q : Comment rendre les attributs calculés disponibles dans Journey Optimizer ?** — Ajoutez le groupe de champs `SystemComputedAttributes` à la source de données Experience Platform sous Configurations > Sources de données.
- **Q : Où puis-je utiliser les attributs calculés dans AJO ?** : dans les activités Condition (fractionnement de parcours), la création d’audiences et l’éditeur de personnalisation.
- **Q : Qu’est-ce qu’une période de recherche en amont ?** — Fenêtre temporelle utilisée pour définir la règle d’agrégation, par exemple « somme des achats au cours des 3 dernières semaines ».
- **Q : Puis-je utiliser des attributs calculés dans les parcours en temps réel ?** — Oui, une fois publiés et ajoutés à la source de données, ils sont accessibles comme tout autre attribut de profil.

+++
