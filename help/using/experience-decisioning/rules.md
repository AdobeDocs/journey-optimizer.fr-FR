---
title: Règles de décision
description: Découvrez comment utiliser les règles de décision
feature: Offers
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Version Beta"
source-git-commit: 69a2ef17b6f5ccd40c08858f7b434029964d544d
workflow-type: tm+mt
source-wordcount: '257'
ht-degree: 8%

---

# Règles de décision {#rules}

>[!BEGINSHADEBOX]

Ce guide vous apportera la documentation suivante :

* [Prise en main d’Experience Decisioning](gs-experience-decisioning.md)
* Gestion des éléments de décision
   * [Configuration du catalogue d’éléments](catalogs.md)
   * [Création d’éléments de décision](items.md)
   * [Gestion des collections d’éléments](collections.md)
* Configuration de la sélection d’éléments
   * **[Créer des règles de décision](rules.md)**
   * [Création de méthodes de classement](ranking.md)
* [Créer des stratégies de sélection](selection-strategies.md)
* [Création de stratégies de décision](create-decision.md)

>[!ENDSHADEBOX]

Les règles de décision vous permettent de définir l’audience des éléments de décision en appliquant des contraintes, directement au niveau de l’élément de décision ou dans une stratégie de sélection spécifique. Vous pouvez ainsi contrôler précisément quels éléments doivent être présentés à qui.

Par exemple, imaginons un scénario où des éléments de décision avec des produits liés au yoga sont conçus pour les femmes. Avec les règles de décision, vous pouvez spécifier que ces éléments ne doivent être affichés que pour les profils dont le genre est &quot;Femme&quot; et qui ont indiqué un &quot;Point ciblé&quot; dans &quot;Yoga&quot;.

La liste des règles de décision est accessible dans la variable **[!UICONTROL Configuration]** / **[!UICONTROL Règles de décision]** .

<!--![](assets/decision-rules-list.png)-->

>[!IMPORTANT]
>
>Pour l’instant, les règles de décision sont gérées à l’aide du Journey Optimizer **Gestion des décisions** . Par conséquent, la variable **[!UICONTROL Règles de décision]** La liste dans Experience Decisioning englobe les règles créées à partir des deux Journey Optimizer **[!UICONTROL Gestion des décisions]** ou **[!UICONTROL Experience Decisioning]** menus.

Pour créer une collection, procédez comme suit :

1. Accédez à **[!UICONTROL Configuration]** / **[!UICONTROL Règles de décision]**.
1. L’interface utilisateur de la gestion des décisions de Journey Optimizer s’affiche dans la zone centrale. Suivez les étapes présentées dans la section [Documentation sur la gestion des décisions](../offers/offer-library/creating-decision-rules.md) pour créer votre règle en fonction de vos besoins.

1. Une fois créée, la règle apparaît dans la liste et peut être utilisée dans les éléments de décision et les stratégies de sélection pour régir la présentation des éléments de décision aux profils.
