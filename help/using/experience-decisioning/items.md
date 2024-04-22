---
title: Éléments de décision
description: Découvrez comment utiliser les éléments de décision.
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Version Beta"
exl-id: 5c866814-d79a-4a49-bfcb-7a767d802e90
source-git-commit: 50d3be8fb8ae04e1cab747f6ba4b1024c5e3ec97
workflow-type: tm+mt
source-wordcount: '1039'
ht-degree: 97%

---

# Éléments de décision {#items}

>[!CONTEXTUALHELP]
>id="ajo_exd_items"
>title="Gérer les éléments de décision"
>abstract="Journey Optimizer vous permet de créer des offres marketing, appelées éléments de décision, que vous pouvez créer et organiser dans un catalogue et des collections centralisés. Actuellement, tous les éléments de décision créés sont consolidés dans un seul catalogue « Offres ». Depuis cet écran, vous pouvez également accéder au schéma du catalogue à l’aide du bouton **Modifier le schéma** et créer des attributs personnalisés pour vos éléments de décision."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/decision-items/catalogs.html?lang=fr" text="Configurer le catalogue d’éléments"

>[!BEGINSHADEBOX « Ce guide couvre les sujets suivants »]

* [Commencer avec la prise de décision basée sur l’expérience](gs-experience-decisioning.md)
* Gérer les éléments de décision : [Configurer le catalogue d’éléments](catalogs.md) – **[Créer des éléments de décision](items.md)** – [Gérer des collections d’éléments](collections.md)
* Configurer la sélection des éléments : [Créer des règles de décision](rules.md) – [Créer des méthodes de classement](ranking.md)
* [Créer des stratégies de sélection](selection-strategies.md)
* [Créer des politiques de décision](create-decision.md)

>[!ENDSHADEBOX]

Journey Optimizer vous permet de créer des offres marketing, appelées éléments de décision, que vous pouvez créer et organiser dans un catalogue et des collections centralisés. Ils sont composés d’attributs standard et personnalisés, conçus précisément pour répondre à vos besoins. En outre, ils intègrent des contraintes de profil qui vous permettent de définir pour qui un élément de décision peut être affiché.

Avant de créer un élément de décision, veillez à créer une **règle de décision** si vous souhaitez définir des conditions pour déterminer pour qui l’élément de décision peut être affiché. [Découvrez comment créer des règles de décision](rules.md).

## Créer votre premier élément de décision

>[!CONTEXTUALHELP]
>id="ajo_exd_item_priority"
>title="Définir la priorité de l’élément de décision"
>abstract="Si un profil est admissible pour plusieurs éléments, la priorité permet de comparer cet élément de décision à d’autres. Une priorité plus élevée confère à l’élément une préséance sur les autres."

>[!CONTEXTUALHELP]
>id="ajo_exd_item_custom_attributes"
>title="Définir les attributs personnalisés"
>abstract="Les attributs personnalisés sont des attributs spécifiques, adaptés à vos besoins, que vous pouvez affecter à un élément de décision. Ils sont créés dans le schéma de catalogue des éléments de décision. Cette section s’affiche uniquement si vous avez ajouté au moins un attribut personnalisé au schéma de catalogue."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/decision-items/catalogs.html?lang=fr" text="Configurer le catalogue d’éléments"

>[!CONTEXTUALHELP]
>id="ajo_exd_item_constraints"
>title="Ajouter des audiences ou des règles de décision"
>abstract="Par défaut, tous les profils seront éligibles pour recevoir l’élément de décision; Vous pouvez toutefois utiliser des audiences ou des règles pour limiter l’élément à des profils spécifiques uniquement."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/audiences-profiles-identities/audiences/about-audiences.html?lang=fr" text="Utiliser des audiences"
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/experience-decisioning/selection/rules.html?lang=fr" text="Utiliser des règles de décision"

Pour créer un élément de décision, procédez comme suit :

1. Accédez à **[!UICONTROL Prise de décision basée sur l’expérience]** > **[!UICONTROL Éléments]**.

1. Définissez les attributs standard de l’élément de décision :

   1. Saisissez un nom et une description.
   1. Spécifiez les dates de début et de fin. L’élément sera pris en compte par le moteur de prise de décision dans cette plage de dates.
   1. Définissez la **[!UICONTROL Priorité]** de l’élément de décision par rapport aux autres, si un profil est qualifié pour plusieurs éléments. Une priorité plus élevée confère à l’élément une préséance sur les autres.
   1. La variable **Balises** vous permet d’affecter des balises unifiées Adobe Experience Platform à vos éléments de décision. Vous pouvez ainsi facilement les classer et améliorer la recherche. [Découvrir comment utiliser les balises](../start/search-filter-categorize.md#tags)

   ![](assets/item-attributes.png)

   >[!NOTE]
   >
   >La priorité est un type de données Entier. Tous les attributs qui sont des types de données Entier doivent contenir des valeurs entières (pas de décimales).

1. Les attributs personnalisés sont des attributs spécifiques, adaptés à vos besoins, que vous pouvez affecter à un élément de décision. Ils sont définis dans le schéma de catalogue des éléments de décision. [Découvrez comment utiliser les catalogues](catalogs.md).

1. Une fois les attributs de l’élément de décision définis, cliquez sur **[!UICONTROL Suivant]** pour définir les contraintes de profil de l’élément.

   Par défaut, tous les profils seront éligibles pour recevoir l’élément de décision; Vous pouvez toutefois utiliser des audiences ou des règles pour limiter l’élément à des profils spécifiques uniquement ; les deux solutions correspondant à différents usages. Pour plus d’informations, développez la section ci-dessous :

   +++Utiliser les audiences par rapport aux règles de décision

   Pour faire simple, la sortie d’une audience est une liste de profils, tandis qu’une règle de décision est une fonction exécutée à la demande sur un seul profil pendant le processus de prise de décision.

   * **Audiences** : d’un côté, les audiences sont un groupe de profils Adobe Experience Platform qui correspondent à une certaine logique basée sur les attributs de profil et les événements d’expérience. Cependant, la gestion des offres ne recalcule pas l’audience, qui peut ne pas être à jour lors de la présentation de l’offre.

   * **Règles de décision** : d’un autre côté, une règle de décision est basée sur les données disponibles dans Adobe Experience Platform et détermine à qui une offre peut être montrée. Une fois sélectionnée dans une offre ou une décision pour un emplacement donné, la règle est exécutée chaque fois qu’une décision est prise, ce qui garantit que chaque profil obtient la dernière et la meilleure offre.

+++

   ![](assets/item-constraints.png)

   * Pour limiter la présentation de l’élément de décision aux membres d’une ou de plusieurs audiences Adobe Experience Platform, sélectionnez l’option **[!UICONTROL Visiteurs et visiteuses appartenant à une ou plusieurs audiences]**, puis ajoutez une ou plusieurs audiences depuis le volet de gauche et combinez-les à l’aide des opérateurs logiques **[!UICONTROL Et]**/**[!UICONTROL Ou]**. [En savoir plus sur les audiences](../audience/about-audiences.md).

   * Pour associer une règle de décision spécifique à l’élément de décision, sélectionnez **[!UICONTROL Par règle]**, puis faites glisser la règle de votre choix depuis le volet de gauche vers la zone centrale. [En savoir plus sur les règles de décision](rules.md).

   Lorsque vous sélectionnez des audiences ou des règles de décision, vous pouvez afficher des informations sur les profils qualifiés estimés. Cliquez sur **[!UICONTROL Actualiser]** pour mettre à jour les données.

   >[!NOTE]
   >
   >Les estimations de profil ne sont pas disponibles lorsque les paramètres de règle incluent des données qui ne figurent pas dans le profil, telles que des données contextuelles. Par exemple, une règle d’éligibilité qui exige que la météo actuelle soit de ≥80 degrés.

1. Une fois les contraintes de l’élément de décision définies, cliquez sur **[!UICONTROL Suivant]** pour vérifier l’élément et l’enregistrer.

1. L’élément de décision apparaît désormais dans la liste, avec le statut **[!UICONTROL Brouillon]**. Lorsqu’il est prêt à être présenté aux profils, cliquez sur le bouton représentant des points de suspension et sélectionnez **[!UICONTROL Approuver]**.

   ![](assets/item-approve.png)

## Gérer les éléments de décision

Dans la liste des éléments de décision, vous pouvez modifier un élément de décision, modifier son statut (**Brouillon**, **Approuvé**, **Archivé**), le dupliquer ou le supprimer.

Pour modifier un élément de décision, ouvrez-le, apportez vos modifications et enregistrez-le.

Sélectionner un élément de décision ou cliquer sur le bouton représentant des points de suspension active les actions décrites ci-dessous.

* **[!UICONTROL Approuver]** : définit l’état de l’élément de décision sur Approuvé.
* **[!UICONTROL Annuler l’approbation]** : redéfinit le statut de l’élément de décision sur **[!UICONTROL Brouillon]**.
* **[!UICONTROL Dupliquer]** : crée un élément de décision avec des attributs et des contraintes identiques. Par défaut, le nouvel élément a le statut **[!UICONTROL Brouillon]**.
* **[!UICONTROL Supprimer]** : supprime l’élément de décision de la liste.

  >[!IMPORTANT]
  >
  >Une fois supprimés, l’élément de décision et son contenu ne sont plus accessibles. Cette action ne peut pas être annulée. Si l’élément de décision est utilisé dans une collection ou une décision, il ne peut pas être supprimé. Vous devez d’abord supprimer l’élément de décision de tous les objets.

* **[!UICONTROL Archiver]** : définit le statut de l’élément de décision sur **[!UICONTROL Archivé]**. L’élément de décision est toujours disponible dans la liste, mais vous ne pouvez pas redéfinir son statut sur **[!UICONTROL Brouillon]** ou sur **[!UICONTROL Approuvé]**. Vous pouvez uniquement le dupliquer ou le supprimer.
