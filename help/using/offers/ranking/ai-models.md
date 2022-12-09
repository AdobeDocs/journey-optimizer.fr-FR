---
product: experience platform
solution: Experience Platform
title: Prise en main des modèles AI
description: En savoir plus sur les modèles AI qui permettent de classer les offres
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: 12bc2373ac5c391764df3880c5c87666a19e99b2
workflow-type: tm+mt
source-wordcount: '310'
ht-degree: 0%

---

# Prise en main des modèles AI {#ai-models}

[!DNL Journey Optimizer] vous permet d’utiliser un système de modèles formé qui classe les offres à afficher pour un profil donné.

Cette fonctionnalité vous permet de créer différents **Modèles AI** en fonction des objectifs de votre entreprise. En utilisant ces différentes stratégies basées sur des objectifs dans une décision, le système de modèles formé vous aidera à comprendre comment les différents modèles d’IA affectent vos objectifs.

Par exemple, vous pouvez sélectionner un modèle d’IA pour le canal email et un autre pour le canal push. Pour chaque canal, le système de modèle formé exploite plusieurs points de données pour déterminer l’offre qui doit être présentée en premier pour un emplacement donné, plutôt que de prendre en compte les scores de priorité des offres ou une [formule de classement](create-ranking-formulas.md).

## Types de modèle AI {#ai-model-types}

Deux types de modèles d’IA sont disponibles dans [!DNL Journey Optimizer]:

* **Modèles d’optimisation automatique** visent à diffuser des offres qui optimisent le retour (IPC) défini par les clients commerciaux. Ces indicateurs clés de performance peuvent prendre la forme de taux de conversion, de recettes, etc. À ce stade, l’optimisation automatique se concentre sur l’optimisation des clics sur les offres, avec pour cible la conversion des offres. L’optimisation automatique n’est pas personnalisée et s’optimise en fonction des performances &quot;globales&quot; des offres. [En savoir plus](auto-optimization-model.md)

* **Modèles de personnalisation** vous permettent de définir des objectifs commerciaux et d’utiliser les données client pour former des modèles orientés vers l’entreprise afin de diffuser des offres personnalisées et d’optimiser les indicateurs de performance clés. [En savoir plus](personalized-optimization-model.md)

   >[!CAUTION]
   >
   >L’utilisation des modèles d’optimisation personnalisée est actuellement disponible en accès anticipé pour certains utilisateurs uniquement.

## Création d’un modèle AI {#create-ai-model}

Les principales étapes pour créer et utiliser des modèles AI sont les suivantes :

1. Créez un jeu de données dans lequel les événements de conversion et d’impression seront collectés. [En savoir plus](create-dataset.md)
1. Créez un modèle d’IA qui exploite les événements du jeu de données pour classer les offres. [En savoir plus](create-ranking-strategies.md)
1. Configurez votre schéma d’offre pour capturer automatiquement les événements. [En savoir plus](schema-requirement.md)
1. Affectez le modèle AI à un emplacement dans une décision de classement des offres éligibles. [En savoir plus](../offer-activities/configure-offer-selection.md)
