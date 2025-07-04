---
title: Règles de décision
description: Découvrez comment utiliser les règles de décision.
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
exl-id: 033a11b8-c848-4e4a-b6f0-62fa0a2152bf
source-git-commit: ebefeb59a19e831ec7f86cee690a35fe71e14554
workflow-type: tm+mt
source-wordcount: '515'
ht-degree: 89%

---

# Règles de décision {#rules}

>[!CONTEXTUALHELP]
>id="ajo_exd_config_rules"
>title="Créer des règles de décision"
>abstract="Les règles de décision vous permettent de définir l’audience des éléments de décision en appliquant des contraintes, directement au niveau de l’élément de décision ou dans une stratégie de sélection spécifique. Vous pouvez ainsi contrôler précisément quels éléments doivent être présentés à qui."

## À propos des règles de décision {#about}

Les règles de décision vous permettent de définir l’audience des éléments de décision en appliquant des contraintes, directement au niveau de l’élément de décision ou dans une stratégie de sélection spécifique. Vous pouvez ainsi contrôler précisément quels éléments doivent être présentés à qui.

Prenons l’exemple d’un scénario dans lequel vous avez des éléments de décision concernant des produits liés au yoga et conçus pour les femmes. Avec les règles de décision, vous pouvez spécifier que ces éléments ne doivent être affichés que pour les profils dont le genre est « Femme », et qui ont indiqué un « Point ciblé » dans « Yoga ».

>[!NOTE]
>
>Outre les règles de décision relatives aux éléments et à la stratégie de sélection, vous pouvez définir l’audience prévue au niveau de la campagne. [En savoir plus](../campaigns/create-campaign.md#audience)

La liste des règles de décision est accessible dans le menu **[!UICONTROL Configuration de la stratégie]**.

![](assets/decision-rules-list.png)

## Créer une règle de décision {#create}

Pour créer cette règle de décision, procédez comme suit :

1. Accédez à **[!UICONTROL Configuration de la stratégie]** / **[!UICONTROL Règles de décision]**, puis cliquez sur le bouton **[!UICONTROL Créer une règle]**.

   >[!NOTE]
   >
   >Vous pouvez également utiliser les données de Adobe Experience Platform pour enrichir votre logique de décision avec des données externes. Cela s’avère particulièrement utile pour les attributs qui changent fréquemment, tels que la disponibilité des produits ou la tarification en temps réel. Cette fonctionnalité est actuellement disponible en version Beta publique pour l’ensemble des clientes et clients. Contactez votre représentant de compte si vous souhaitez y accéder. [Découvrez comment utiliser les données Adobe Experience Platform pour la prise de décision](../experience-decisioning/aep-data-exd.md)

1. L’écran de création des règles de décision s’affiche. Nommez votre règle et fournissez une description.

1. Créez la règle de décision en fonction de vos besoins à l’aide du créateur de segments d’Adobe Experience Platform. Pour ce faire, vous pouvez utiliser différentes sources de données telles que :
   * Attributs de profil et attributs des éléments de décision
   * Audiences
   * Données contextuelles provenant d’Adobe Experience Platform [Découvrir comment utiliser les données contextuelles](context-data.md)

   ![](assets/decision-rules-build.png)

   >[!NOTE]
   >
   >Le Créateur de segments fourni pour créer des règles de décision présente certaines spécificités par rapport à celui utilisé avec le service de segmentation d’Adobe Experience Platform. Cependant, le processus global décrit dans la documentation est toujours valide pour créer des règles de décision. [Découvrir comment créer des définitions de segment](../audience/creating-a-segment-definition.md)

1. À mesure que vous ajoutez et configurez de nouveaux champs dans l’espace de travail, le volet **[!UICONTROL Propriétés de l’audience]** affiche des informations sur l’estimation des profils appartenant à l’audience. Cliquez sur **[!UICONTROL Actualiser l’estimation]** pour mettre à jour les données.

   >[!NOTE]
   >
   >Les estimations de profil ne sont pas disponibles lorsque les paramètres de règle incluent des données qui ne figurent pas dans le profil, telles que des données contextuelles.

1. Une fois votre règle de décision prête, cliquez sur **[!UICONTROL Enregistrer]**. La règle apparaît dans la liste et peut être utilisée dans les éléments de décision et les stratégies de sélection pour régir la présentation des éléments de décision aux profils.

   >[!NOTE]
   >
   >La profondeur d’imbrication dans une règle d’éligibilité est limitée à 30 niveaux. Celle-ci est mesurée en comptant les parenthèses fermantes `)` dans la chaîne PQL. La taille d’une chaîne de règle est de 15 Ko maximum pour les caractères codés en UTF-8. Cela équivaut à 15 000 caractères ASCII (1 octet chacun) ou 3 750 à 7 500 caractères non ASCII (2 à 4 octets chacun). [En savoir plus sur les mécanismes de sécurisation et sur les limitations de la prise de décisions](gs-experience-decisioning.md#guardrails)
