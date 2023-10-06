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
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: 4b23f9fa2d6d7d12988f3c590d6e835637c05bea
workflow-type: tm+mt
source-wordcount: '280'
ht-degree: 17%

---

# Règles de décision {#rules}

>[!BEGINSHADEBOX]

Ce guide couvre les sujets suivants :

* [Prise en main de la prise de décision basée sur l’expérience](gs-experience-decisioning.md)
* Gérer les éléments de décision
   * [Configurer le catalogue d’éléments](catalogs.md)
   * [Créer des éléments de décision](items.md)
   * [Gérer des collections d’éléments](collections.md)
* Configurer la sélection d’éléments
   * **[Créer des règles de décision](rules.md)**
   * [Créer des méthodes de classement](ranking.md)
* [Créer des stratégies de sélection](selection-strategies.md)
* [Créer des stratégies de décision](create-decision.md)

>[!ENDSHADEBOX]

Les règles de décision vous permettent de définir l’audience des éléments de décision en appliquant des contraintes, directement au niveau de l’élément de décision ou dans une stratégie de sélection spécifique. Vous pouvez ainsi contrôler précisément quels éléments doivent être présentés à qui.

Par exemple, imaginons un scénario où des éléments de décision avec des produits liés au yoga sont conçus pour les femmes. Avec les règles de décision, vous pouvez spécifier que ces éléments ne doivent être affichés que pour les profils dont le genre est &quot;Femme&quot; et qui ont indiqué un &quot;Point ciblé&quot; dans &quot;Yoga&quot;.

>[!NOTE]
>
>Outre les règles de décision relatives aux éléments et à la stratégie de sélection, vous pouvez définir l’audience prévue au niveau de la campagne. [En savoir plus](../campaigns/create-campaign.md#audience)


La liste des règles de décision est accessible dans la variable **[!UICONTROL Configuration]** / **[!UICONTROL Règles de décision]** .

<!--![](assets/decision-rules-list.png)-->

>[!IMPORTANT]
>
>Pour l’instant, les règles de décision sont gérées à l’aide du Journey Optimizer **Gestion des décisions** . Par conséquent, la variable **[!UICONTROL Règles de décision]** La liste dans Experience Decisioning englobe les règles créées à partir des deux Journey Optimizer **[!UICONTROL Gestion des décisions]** ou **[!UICONTROL Experience Decisioning]** menus.

Pour créer une règle, procédez comme suit :

1. Accédez à **[!UICONTROL Configuration]** / **[!UICONTROL Règles de décision]**.
1. L’interface utilisateur de la gestion des décisions de Journey Optimizer s’affiche dans la zone centrale. Suivez les étapes présentées dans la section [Documentation sur la gestion des décisions](../offers/offer-library/creating-decision-rules.md) pour créer votre règle en fonction de vos besoins.

1. Une fois créée, la règle apparaît dans la liste et peut être utilisée dans les éléments de décision et les stratégies de sélection pour régir la présentation des éléments de décision aux profils.
