---
solution: Journey Optimizer
product: Journey Optimizer
title: Commencer avec les modèles d’IA
description: En savoir plus sur les modèles d’IA qui permettent de classer les offres
feature: Ranking, Decisioning
topic: Artificial Intelligence
role: User
level: Intermediate
exl-id: 07679823-2288-4528-b09a-12fd76a69482
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sWJEr5Pm1wl83Q-2HVb-7mqy7hasQ1ffqRDmJsOFomw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 338
ht-degree: 89%

---

# Commencer avec les modèles d’IA {#ai-models}

[!DNL Journey Optimizer] vous permet d&#39;utiliser un système de modèles formés pour classer les offres à afficher pour un profil donné.

Cette fonctionnalité permet de créer différents **modèles d’IA** en fonction des objectifs de votre entreprise. En appliquant ces différentes stratégies basées sur les objectifs à une décision, le système de modèles entraînés vous permet de comprendre l’impact des différents modèles d’IA sur vos objectifs.

<!--
For example, you can select an AI model for the email channel and another one for the push channel. For each channel, the trained model system will leverage multiple data points to determine which offer should be presented first for a given decision policy?, rather than taking into account the offers' priority scores or a [ranking formula](create-ranking-formulas.md).

>[!IMPORTANT]
>
>For now, ranking models are not supported in Journey Optimizer authored channels.
-->

## Types de modèles d’IA {#ai-model-types}

>[!CONTEXTUALHELP]
>id="ajo_exd_ai_model_type"
>title="Choisir le type de modèle"
>abstract="Sélectionnez le type de modèle d’IA à créer : **Optimisation automatique** optimise les offres en fonction des performances des offres antérieures, tandis qu’**Optimisation personnalisée** optimise et personnalise les offres en fonction des audiences et des performances des offres."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/decisioning/offer-decisioning/rankings/ai-models/create-ranking-strategies#create-ranking-strategy" text="Créer un modèle d’IA"

Deux types de modèles d’IA sont disponibles dans [!DNL Journey Optimizer] :

* Les **modèles d’optimisation automatique** visent à proposer des offres qui optimisent le retour (KPI) défini par les clients commerciaux. Ces indicateurs de performance clés peuvent prendre la forme de taux de conversion, de revenus, etc. À ce stade, l’optimisation automatique se concentre sur l’optimisation des clics sur les offres avec la conversion d’offres comme cible. L’optimisation automatique n’est pas personnalisée et s’optimise en fonction des performances « globales » des offres. [En savoir plus](auto-optimization-model.md)

* **Les modèles d’optimisation personnalisés** vous permettent de définir des objectifs métier et d’utiliser les données client pour entraîner des modèles orientés métier afin de diffuser des offres personnalisées et d’optimiser les KPI. [En savoir plus](personalized-optimization-model.md)

## Créer un modèle d’IA {#create-ai-model}

Les principales étapes pour créer et utiliser des modèles d’IA sont les suivantes :

1. Créez un jeu de données dans lequel les événements de conversion et d’impression seront collectés. [En savoir plus](../data-collection/create-dataset.md)

1. Créez un modèle d’IA qui exploite les événements du jeu de données pour classer les offres. [En savoir plus](create-ai-models.md)

1. Configurez votre schéma d’offre pour capturer automatiquement les événements. [En savoir plus](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >Les modèles de classement exigent que des événements de commentaires soient envoyés en tant qu’événements d’expérience afin d’être collectés. [En savoir plus sur la collecte de données de prise de décision](../data-collection/data-collection.md).

1. Affectez le modèle d’IA à une stratégie de sélection pour classer les offres éligibles. [En savoir plus](../selection-strategies.md#select-ranking-method)

1. Surveillez le statut et les performances d’entraînement de votre modèle d’IA. [En savoir plus](ai-model-observability.md)
