---
title: Règles de décision
description: Découvrez comment utiliser les règles de décision.
feature: Experience Decisioning
topic: Integrations
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Version Beta"
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: f92e3882d3b5e515e672a4af8e787813d4d939ce
workflow-type: tm+mt
source-wordcount: '323'
ht-degree: 100%

---

# Règles de décision {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="Créer des règles de décision"
>abstract="Les règles de décision vous permettent de définir l’audience des éléments de décision en appliquant des contraintes, directement au niveau de l’élément de décision ou dans une stratégie de sélection spécifique. Vous pouvez ainsi contrôler précisément quels éléments doivent être présentés à qui."

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
* [Créer des politiques de décision](create-decision.md)

>[!ENDSHADEBOX]

Les règles de décision vous permettent de définir l’audience des éléments de décision en appliquant des contraintes, directement au niveau de l’élément de décision ou dans une stratégie de sélection spécifique. Vous pouvez ainsi contrôler précisément quels éléments doivent être présentés à qui.

Prenons l’exemple d’un scénario dans lequel vous avez des éléments de décision concernant des produits liés au yoga et conçus pour les femmes. Avec les règles de décision, vous pouvez spécifier que ces éléments ne doivent être affichés que pour les profils dont le genre est « Femme », et qui ont indiqué un « Point ciblé » dans « Yoga ».

>[!NOTE]
>
>Outre les règles de décision relatives aux éléments et à la stratégie de sélection, vous pouvez définir l’audience prévue au niveau de la campagne. [En savoir plus](../campaigns/create-campaign.md#audience)


La liste des règles de décision est accessible dans le menu **[!UICONTROL Configuration]**/**[!UICONTROL Régles de décisions]**.

<!--![](assets/decision-rules-list.png)-->

>[!IMPORTANT]
>
>Pour l’instant, les règles de décision sont gérées à l’aide du menu **Gestion des décisions** de Journey Optimizer. Par conséquent, la liste **[!UICONTROL Règles de décision]** dans la prise de décision basée sur l’expérience englobe les règles créées à partir des menus **[!UICONTROL Gestion des décisions]** ou **[!UICONTROL Prise de décision basée sur l’expérience]** de Journey Optimizer.

Pour créer une règle, procédez comme suit :

1. Accédez à **[!UICONTROL Configuration]**/**[!UICONTROL Règles de décision]**.
1. L’interface utilisateur de la gestion des décisions de Journey Optimizer s’affiche dans la zone centrale. Suivez les étapes présentées dans la [documentation sur la gestion des décisions](../offers/offer-library/creating-decision-rules.md) pour créer votre règle en fonction de vos besoins.

1. Une fois créée, la règle apparaît dans la liste et peut être utilisée dans les éléments de décision et les stratégies de sélection pour régir la présentation des éléments de décision aux profils.
