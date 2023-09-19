---
title: Collections
description: Découvrez comment utiliser des collections
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Version Beta"
source-git-commit: 69a2ef17b6f5ccd40c08858f7b434029964d544d
workflow-type: tm+mt
source-wordcount: '262'
ht-degree: 8%

---

# Collections {#collections}

>[!BEGINSHADEBOX]

Ce guide vous apportera la documentation suivante :

* [Prise en main d’Experience Decisioning](gs-experience-decisioning.md)
* Gestion des éléments de décision
   * [Configuration du catalogue d’éléments](catalogs.md)
   * [Création d’éléments de décision](items.md)
   * **[Gestion des collections d’éléments](collections.md)**
* Configuration de la sélection d’éléments
   * [Créer des règles de décision](rules.md)
   * [Création de méthodes de classement](ranking.md)
* [Créer des stratégies de sélection](selection-strategies.md)
* [Création de stratégies de décision](create-decision.md)

>[!ENDSHADEBOX]

Les collections vous permettent de classer et de regrouper vos éléments de décision en fonction de vos préférences. Ces catégories sont créées en créant des règles qui tirent parti des attributs des éléments de décision.

Supposons, par exemple, que vous ayez ajouté un attribut personnalisé &quot;Catégorie&quot; au schéma de catalogue de vos éléments de décision. Vous pouvez ainsi créer une collection qui inclut tous les éléments de décision avec la valeur &quot;Yoga&quot; dans l’attribut &quot;Category&quot;.

La liste des collections est accessible à partir du **[!UICONTROL Éléments]** .

Pour créer une collection, procédez comme suit :

1. Accédez à **[!UICONTROL Éléments]** > **[!UICONTROL Collections]** et cliquez sur **[!UICONTROL Créer une collection]**.
1. Attribuez un nom et une description à la collection.
1. Ajoutez une ou plusieurs règles pour déterminer les éléments à inclure dans la collection. Pour ce faire :

   1. Sélectionnez un attribut d’élément à utiliser comme critère. La liste d’attributs comprend tous les attributs standard et personnalisés définis dans le schéma de catalogue. [En savoir plus sur le catalogue d’articles](catalogs.md)
   1. Sélectionnez l’opérateur désiré et saisissez la valeur sur laquelle filtrer les données.
   1. Répétez ces étapes pour ajouter autant de règles que nécessaire. Lorsque plusieurs règles sont ajoutées, vous pouvez choisir parmi les **Et** et **Ou** pour les combiner. Pour cela, cliquez sur le badge de l&#39;opérateur pour basculer entre les deux choix.

   ![](assets/collection-create.png)

1. Une fois les règles de collecte définies, cliquez sur **[!UICONTROL Créer]**. La collection s’affiche désormais dans la liste.
