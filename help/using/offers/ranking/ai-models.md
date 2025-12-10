---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Prise en main des modèles d’IA
description: En savoir plus sur les modèles d’IA qui permettent de classer les offres
badge: label="Hérité" type="Informative"
feature: Ranking, Decision Management
topic: Artificial Intelligence
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
version: Journey Orchestration
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '396'
ht-degree: 100%

---

# Prise en main des modèles d’IA {#ai-models}

[!DNL Journey Optimizer] vous permet d&#39;utiliser un système de modèles formés pour classer les offres à afficher pour un profil donné.

Cette fonctionnalité permet de créer différents **modèles d’IA** en fonction des objectifs de votre entreprise. En appliquant ces différentes stratégies basées sur les objectifs à une décision, le système de modèles entraînés vous permet de comprendre l’impact des différents modèles d’IA sur vos objectifs.

Vous pouvez par exemple sélectionner un modèle d’IA pour le canal e-mail et un autre pour le canal push. Pour chaque canal, le système de modèles entraînés exploite différents points de données pour déterminer l’offre qui doit être présentée en premier pour un emplacement donné, plutôt que de prendre en compte les scores de priorité des offres ou une [formule de classement](create-ranking-formulas.md).

>[!IMPORTANT]
>
>Pour l’instant, les modèles d’IA ne sont pas pris en charge dans les canaux créés par Journey Optimizer.

➡️ [Découvrez cette fonctionnalité en vidéo.](#video)

## Types de modèles d’IA {#ai-model-types}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_ai_model_type"
>title="Choisir le type de modèle"
>abstract="Sélectionnez le type de modèle d’IA à créer : **Optimisation automatique** optimise les offres en fonction des performances des offres antérieures, tandis qu’**Optimisation personnalisée** optimise et personnalise les offres en fonction des audiences et des performances des offres."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/decisioning/offer-decisioning/rankings/ai-models/create-ranking-strategies#create-ranking-strategy" text="Créer un modèle d’IA"

Deux types de modèles d’IA sont disponibles dans [!DNL Journey Optimizer] :

* Les **modèles d’optimisation automatique** visent à proposer des offres qui optimisent le retour (KPI) défini par les clients commerciaux. Ces KPI peuvent prendre la forme de taux de conversion, de chiffres dʼaffaires, etc. À ce stade, l’optimisation automatique cherche à optimiser les clics sur les offres, avec comme cible la conversion de lʼoffre. L’optimisation automatique n’est pas personnalisée et s’optimise en fonction des performances « globales » des offres. [En savoir plus](auto-optimization-model.md)

* **Les modèles d’optimisation personnalisés** vous permettent de définir des objectifs métier et d’utiliser les données client pour entraîner des modèles orientés métier afin de diffuser des offres personnalisées et d’optimiser les KPI. [En savoir plus](personalized-optimization-model.md).

## Créer un modèle d’IA {#create-ai-model}

Les principales étapes pour créer et utiliser des modèles d’IA sont les suivantes :

1. Créez un jeu de données dans lequel les événements de conversion et d’impression seront collectés. [En savoir plus](../data-collection/create-dataset.md)

1. Créez un modèle d’IA qui exploite les événements du jeu de données pour classer les offres. [En savoir plus](create-ranking-strategies.md)

1. Configurez votre schéma d’offre pour capturer automatiquement les événements. [En savoir plus](../data-collection/schema-requirement.md)

   >[!IMPORTANT]
   >
   >Les modèles d’IA exigent que des événements de retour soient envoyés en tant qu’événements d’expérience afin d’être collectés. [En savoir plus sur la collecte de données de la gestion des décisions](../data-collection/data-collection.md)

1. Affectez le modèle d’IA à un emplacement dans une décision de classement des offres éligibles. [En savoir plus](../offer-activities/configure-offer-selection.md)

## Vidéo pratique {#video}

Découvrez comment créer un modèle d’IA pour Offer Decisioning et comment l’appliquer à une décision.

>[!VIDEO](https://video.tv.adobe.com/v/3419959?quality=12)
