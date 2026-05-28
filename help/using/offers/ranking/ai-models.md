---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Commencer avec les modèles d’IA
description: En savoir plus sur les modèles d’IA qui permettent de classer les offres
badge: label="Hérité" type="Informative"
feature: Ranking, Decision Management
topic: Artificial Intelligence
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Ya5F8s8gr9dM-surRM-0K4VaM9GSs8jIZNVZ9b7pdIM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a4cb03e1-327e-499d-9de8-e0c0db8a63a2
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
  - id: d3cdead0-685a-4489-9250-4bb709942f66
subfeature_v2:
  - id: a7a194a0-75e2-4913-8a83-14714fbf68e6
  - id: eb547372-2a95-4d13-b0fd-f720c9895880
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
source-git-commit: ee6e1c0a2d86736e51257315fa41c4796286579f
workflow-type: tm+mt
source-wordcount: 440
ht-degree: 93%

---

# Commencer avec les modèles d’IA {#ai-models}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../../experience-decisioning/gs-experience-decisioning.md)

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

* Les **modèles d’optimisation automatique** visent à proposer des offres qui optimisent le retour (KPI) défini par les clients commerciaux. Ces indicateurs de performance clés peuvent prendre la forme de taux de conversion, de revenus, etc. À ce stade, l’optimisation automatique se concentre sur l’optimisation des clics sur les offres avec la conversion d’offres comme cible. L’optimisation automatique n’est pas personnalisée et s’optimise en fonction des performances « globales » des offres. [En savoir plus](auto-optimization-model.md)

* **Les modèles d’optimisation personnalisés** vous permettent de définir des objectifs métier et d’utiliser les données client pour entraîner des modèles orientés métier afin de diffuser des offres personnalisées et d’optimiser les KPI. [En savoir plus](personalized-optimization-model.md)

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
