---
product: experience platform
solution: Experience Platform
title: Prise en main des modèles d’IA
description: En savoir plus sur les modèles d’IA qui permettent de classer les offres
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 3188bc97b8103d2a01101a23d8c242a3e2924f76
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 80%

---

# Prise en main des modèles d’IA {#ai-models}

[!DNL Journey Optimizer] vous permet d&#39;utiliser un système de modèles formés pour classer les offres à afficher pour un profil donné.

Cette fonctionnalité permet de créer différents **modèles d’IA** en fonction des objectifs de votre entreprise. En appliquant ces différentes stratégies basées sur les objectifs à une décision, le système de modèles entraînés vous permet de comprendre l’impact des différents modèles d’IA sur vos objectifs.

Vous pouvez par exemple sélectionner un modèle d’IA pour le canal e-mail et un autre pour le canal push. Pour chaque canal, le système de modèles entraînés exploite différents points de données pour déterminer l’offre qui doit être présentée en premier pour un emplacement donné, plutôt que de prendre en compte les scores de priorité des offres ou une [formule de classement](create-ranking-formulas.md).

## Types de modèles d’IA {#ai-model-types}

Deux types de modèles d’IA sont disponibles dans [!DNL Journey Optimizer]:

* **Modèles d’optimisation automatique** visent à diffuser des offres qui optimisent le retour (IPC) défini par les clients commerciaux. Ces KPI peuvent prendre la forme de taux de conversion, de chiffres dʼaffaires, etc. À ce stade, l’optimisation automatique cherche à optimiser les clics sur les offres, avec comme cible la conversion de lʼoffre. L’optimisation automatique n’est pas personnalisée et s’optimise en fonction des performances « globales » des offres. [En savoir plus](auto-optimization-model.md)

* **Modèles de personnalisation** vous permettent de définir des objectifs commerciaux et d’utiliser les données client pour former des modèles orientés vers l’entreprise afin de diffuser des offres personnalisées et d’optimiser les indicateurs de performance clés. [En savoir plus](personalized-optimization-model.md)

>[!CAUTION]
>
>L’utilisation des modèles d’optimisation personnalisée est actuellement disponible en accès anticipé pour certains utilisateurs uniquement.

## Créer un modèle d’IA {#create-ai-model}

Les principales étapes pour créer et utiliser des modèles d’IA sont les suivantes :

1. Créez un jeu de données dans lequel les événements de conversion et d’impression seront collectés. [En savoir plus](create-dataset.md)
1. Créez un modèle d’IA qui exploite les événements du jeu de données pour classer les offres. [En savoir plus](create-ranking-strategies.md)
1. Configurez votre schéma d’offre pour capturer automatiquement les événements. [En savoir plus](schema-requirement.md)
1. Affectez le modèle d’IA à un emplacement dans une décision de classement des offres éligibles. [En savoir plus](../offer-activities/configure-offer-selection.md)
