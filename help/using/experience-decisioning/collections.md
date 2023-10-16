---
title: Collections
description: Découvrir comment utiliser les collections
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Version Beta"
exl-id: 099d1439-34f7-47fe-9181-0e9ce2032a01
source-git-commit: c4ab97999d000d969f6f09f4d84be017d1288f94
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 100%

---

# Collections {#collections}

>[!BEGINSHADEBOX]

Ce guide couvre les sujets suivants :

* [Prise en main de la prise de décision basée sur l’expérience](gs-experience-decisioning.md)
* Gérer les éléments de décision
   * [Configurer le catalogue d’éléments](catalogs.md)
   * [Créer des éléments de décision](items.md)
   * **[Gérer des collections d’éléments](collections.md)**
* Configurer la sélection d’éléments
   * [Créer des règles de décision](rules.md)
   * [Créer des méthodes de classement](ranking.md)
* [Créer des stratégies de sélection](selection-strategies.md)
* [Créer des politiques de décision](create-decision.md)

>[!ENDSHADEBOX]

Les collections vous permettent de classer et de regrouper vos éléments de décision en fonction de vos préférences. Ces catégories sont créées en créant des règles qui utilisent les attributs des éléments de décision.

Supposons, par exemple, que vous ayez ajouté un attribut personnalisé « Catégorie » au schéma de catalogue de vos éléments de décision. Vous pouvez ainsi créer une collection qui inclut tous les éléments de décision avec la valeur « Yoga » dans l’attribut « Categorie ».

La liste des collections est accessible à partir du menu **[!UICONTROL Éléments]**.

Pour créer une collection, procédez comme suit :

1. Accédez à **[!UICONTROL Éléments]** > **[!UICONTROL Collections]** et cliquez sur **[!UICONTROL Créer une collection]**.
1. Fournissez un nom et une description pour la collection.
1. Ajoutez une ou plusieurs règles pour déterminer les éléments à inclure dans la collection. Pour ce faire :

   1. Sélectionnez un attribut d’élément à utiliser comme critère. La liste d’attributs comprend tous les attributs standard et personnalisés définis dans le schéma de catalogue. [En savoir plus sur le catalogue d’éléments](catalogs.md)
   1. Sélectionnez l’opérateur souhaité et saisissez la valeur sur laquelle filtrer les données.
   1. Répétez ces étapes pour ajouter autant de règles que nécessaire. Lorsque plusieurs règles sont ajoutées, vous pouvez choisir parmi les opérateurs **Et** et **Ou** pour les combiner. Pour cela, cliquez sur le badge de l’opérateur pour basculer entre les deux choix.

   ![](assets/collection-create.png)

1. Une fois les règles de collection définies, cliquez sur **[!UICONTROL Créer]**. La collection s’affiche désormais dans la liste.
