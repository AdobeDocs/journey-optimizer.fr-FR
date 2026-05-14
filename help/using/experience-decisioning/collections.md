---
title: Collections
description: Découvrir comment utiliser les collections
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 099d1439-34f7-47fe-9181-0e9ce2032a01
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/prHnL1lwDR5YZrYfB94Gp0-VH9pOf4kK2NJiUu1mLIU
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 533
ht-degree: 100%

---

# Collections {#collections}

>[!CONTEXTUALHELP]
>id="ajo_exd_item_collections"
>title="Créer des collections"
>abstract="Les collections vous permettent de classer et de regrouper vos éléments de décision en fonction de vos préférences. Ces catégories sont créées en élaborant des règles qui utilisent les attributs des éléments de décision."

>[!CONTEXTUALHELP]
>id="ajo_exd_item_collection_rules"
>title="Définir des règles pour votre collection"
>abstract="Ajoutez une ou plusieurs règles pour déterminer les éléments à inclure dans la collection. Sélectionnez un attribut d’élément à utiliser comme critère. Sélectionnez l’opérateur souhaité et saisissez la valeur sur laquelle filtrer les données. Ajoutez autant de règles que nécessaire."

>[!CONTEXTUALHELP]
>id="ajo_exd_strategy_collection"
>title="Choisir une collection"
>abstract="Sélectionnez la collection qui contient les offres à prendre en compte. Cette étape est obligatoire lors de la création d’une stratégie de sélection. Les collections vous permettent de classer et de regrouper vos éléments de décision en fonction de vos préférences. Par exemple, vous pouvez créer une collection qui inclut tous les éléments de décision avec la valeur « Yoga » dans l’attribut personnalisé « Catégorie »."

Les collections vous permettent de classer et de regrouper vos éléments de décision en fonction de vos préférences. Ces catégories sont créées en élaborant des règles qui utilisent les attributs des éléments de décision.

Supposons, par exemple, que vous ayez ajouté un attribut personnalisé « Catégorie » au schéma de catalogue de vos éléments de décision. Vous pouvez ainsi créer une collection qui inclut tous les éléments de décision avec la valeur « Yoga » dans l’attribut « Categorie ».

La liste des collections est accessible à partir du menu **[!UICONTROL Catalogues]**.

Pour créer une collection, procédez comme suit :

1. Accédez à **[!UICONTROL Catalogues]** > **[!UICONTROL Collections]** et cliquez sur **[!UICONTROL Créer une collection]**.
1. Fournissez un nom et une description pour la collection.
1. Ajoutez une ou plusieurs règles pour déterminer les éléments à inclure dans la collection. Pour ce faire :

   1. Sélectionnez un attribut d’élément à utiliser comme critère. La liste d’attributs comprend tous les attributs standard et personnalisés définis dans le schéma de catalogue. [En savoir plus sur le catalogue des éléments](catalogs.md)
   1. Sélectionnez l’opérateur de votre choix et saisissez la valeur sur laquelle effectuer le filtrage. Spécifiez explicitement chaque nom d’offre ou créez et attribuez une balise « luma-summer » à chaque offre.

      >[!NOTE]
      >
      >L’opérateur **CONTIENT** ne prend pas en charge les correspondances partielles ou avec des caractères génériques. Il fonctionne comme un opérateur **DANS**, ce qui signifie que vous devez fournir une série de valeurs exactes pour l’attribut.
      >
      >Supposons, par exemple, que vous souhaitiez inclure plusieurs offres d’été dans une collection : *« luma-summer-yoga »*, *« luma-summer-fitness »* et *« luma-summer-running »*. Pour inclure ces éléments, vous devez définir une règle telle que « Nom de l’offre » CONTIENT « luma-summer-yoga », « luma-summer-fitness », « luma-summer-running ». Cette règle renvoie uniquement les offres qui correspondent exactement à l’un des noms présents dans la liste.
      >
      >Si vous avez besoin d’une correspondance partielle (par exemple, toutes les offres contenant *« luma-summer »*), cette fonctionnalité n’est actuellement pas prise en charge. Vous devez spécifier explicitement le nom de chaque offre ou attribuer une balise *« luma-summer »* à chaque offre et utiliser cette balise dans votre règle.

   1. Répétez ces étapes pour ajouter autant de règles que nécessaire. Lorsque plusieurs règles sont ajoutées, vous pouvez choisir parmi les opérateurs **Et** et **Ou** pour les combiner. Pour cela, cliquez sur le badge de l’opérateur pour basculer entre les deux choix.
   1. Cliquez sur le bouton **[!UICONTROL Prévisualiser la collection]** pour afficher les éléments qui respectent les règles que vous avez définies.

   ![](assets/collection-create.png)

1. Une fois les règles de collection définies, cliquez sur **[!UICONTROL Créer]**. La collection s’affiche désormais dans la liste.

>[!NOTE]
>
>Chaque collection d’éléments peut contenir jusqu’à 500 éléments d’offre. [En savoir plus sur les mécanismes de sécurisation et sur les limitations de la prise de décisions](gs-experience-decisioning.md#guardrails)
