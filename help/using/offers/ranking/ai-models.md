---
product: experience platform
solution: Experience Platform
title: Prise en main des modèles d’IA
description: En savoir plus sur les modèles d’IA qui permettent de classer les offres
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 12b01cb9de84399e5ede987866609acc10b64c5f
workflow-type: tm+mt
source-wordcount: '232'
ht-degree: 59%

---

# Prise en main des modèles d’IA {#ai-models}

[!DNL Journey Optimizer] vous permet d&#39;utiliser un système de modèles formés pour classer les offres à afficher pour un profil donné.

Cette fonctionnalité permet de créer différents **modèles d’IA** en fonction des objectifs de votre entreprise. En appliquant ces différentes stratégies basées sur les objectifs à une décision, le système de modèles entraînés vous permet de comprendre l’impact des différents modèles d’IA sur vos objectifs.

Vous pouvez par exemple sélectionner un modèle d’IA pour le canal e-mail et un autre pour le canal push. Pour chaque canal, le système de modèles entraînés exploite différents points de données pour déterminer l’offre qui doit être présentée en premier pour un emplacement donné, plutôt que de prendre en compte les scores de priorité des offres ou une [formule de classement](create-ranking-formulas.md).

## Types de modèle AI {#ai-model-types}

Pour l’instant, [!DNL Journey Optimizer]** fournit un modèle d’IA, **Optimisation automatique**, qui optimise les offres en fonction des performances des offres antérieures. Des informations détaillées sur ce type de modèle d’IA sont disponibles dans la section [cette section](auto-optimization-model.md).

## Création d’un modèle AI {#create-ai-model}

Les principales étapes pour créer et utiliser des modèles AI sont les suivantes :

1. Créez un jeu de données dans lequel les événements de conversion et d’impression seront collectés. [En savoir plus](create-dataset.md)
1. Créez un modèle d’IA qui exploite les événements du jeu de données pour classer les offres. [En savoir plus](create-ranking-strategies.md)
1. Configurez votre schéma d’offre pour capturer automatiquement les événements. [En savoir plus](schema-requirement.md)
1. Affectez le modèle AI à un emplacement dans une décision de classement des offres éligibles. [En savoir plus](../offer-activities/configure-offer-selection.md)
