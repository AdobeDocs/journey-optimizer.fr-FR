---
solution: Journey Optimizer
product: Journey Optimizer
title: Prise en main des modèles d’IA
description: En savoir plus sur les modèles d’IA qui permettent de classer les offres
feature: Ranking, Decision Management
role: User
level: Intermediate
exl-id: 07679823-2288-4528-b09a-12fd76a69482
version: Journey Orchestration
source-git-commit: 3fa90fa707b562ecf2160ec980520bc8bc267a21
workflow-type: ht
source-wordcount: '303'
ht-degree: 100%

---

# Prise en main des modèles d’IA {#ai-models}

[!DNL Journey Optimizer] vous permet d&#39;utiliser un système de modèles formés pour classer les offres à afficher pour un profil donné.

Cette fonctionnalité permet de créer différents **modèles d’IA** en fonction des objectifs de votre entreprise. En appliquant ces différentes stratégies basées sur les objectifs à une décision, le système de modèles entraînés vous permet de comprendre l’impact des différents modèles d’IA sur vos objectifs.

<!--For example, you can select an AI model for the email channel and another one for the push channel. For each channel, the trained model system will leverage multiple data points to determine which offer should be presented first for a given decision policy?, rather than taking into account the offers' priority scores or a [ranking formula](create-ranking-formulas.md).

>[!IMPORTANT]
>
>For now, ranking models are not supported in Journey Optimizer authored channels.-->

## Types de modèles d’IA {#ai-model-types}

>[!CONTEXTUALHELP]
>id="ajo_exd_ai_model_type"
>title="Choisir le type de modèle"
>abstract="Sélectionnez le type de modèle d’IA à créer : **Optimisation automatique** optimise les offres en fonction des performances des offres antérieures, tandis qu’**Optimisation personnalisée** optimise et personnalise les offres en fonction des audiences et des performances des offres."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/decisioning/offer-decisioning/rankings/ai-models/create-ranking-strategies#create-ranking-strategy" text="Créer un modèle d’IA"

Deux types de modèles d’IA sont disponibles dans [!DNL Journey Optimizer] :

* Les **modèles d’optimisation automatique** visent à proposer des offres qui optimisent le retour (KPI) défini par les clients commerciaux. Ces KPI peuvent prendre la forme de taux de conversion, de chiffres dʼaffaires, etc. À ce stade, l’optimisation automatique cherche à optimiser les clics sur les offres, avec comme cible la conversion de lʼoffre. L’optimisation automatique n’est pas personnalisée et s’optimise en fonction des performances « globales » des offres. [En savoir plus](auto-optimization-model.md)

* **Les modèles d’optimisation personnalisés** vous permettent de définir des objectifs métier et d’utiliser les données client pour entraîner des modèles orientés métier afin de diffuser des offres personnalisées et d’optimiser les KPI. [En savoir plus](personalized-optimization-model.md).

## Créer un modèle d’IA {#create-ai-model}

Les principales étapes pour créer et utiliser des modèles d’IA sont les suivantes :

1. Créez un jeu de données dans lequel les événements de conversion et d’impression seront collectés. [En savoir plus](../data-collection/create-dataset.md)

1. Créez un modèle d’IA qui exploite les événements du jeu de données pour classer les offres. [En savoir plus](create-ai-models.md)

1. Configurez votre schéma d’offre pour capturer automatiquement les événements. [En savoir plus](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >Les modèles de classement exigent que des événements de commentaires soient envoyés en tant qu’événements d’expérience afin d’être collectés. [En savoir plus sur la collecte de données de prise de décision](../data-collection/data-collection.md).

1. Affectez le modèle d’IA à une stratégie de sélection pour classer les offres éligibles. [En savoir plus](../selection-strategies.md#select-ranking-method)
