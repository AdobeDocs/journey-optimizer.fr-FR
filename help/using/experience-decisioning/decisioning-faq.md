---
title: Questions fréquentes sur la prise de décision
description: Obtenez des réponses aux questions fréquentes sur les fonctionnalités de prise de décision
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
version: Journey Orchestration
exl-id: 7bb72527-d4e1-49f8-b2c3-c943d65903f2
source-git-commit: d7d9c371f4b0d8b4ea51e1f23eb9a2f665711fce
workflow-type: tm+mt
source-wordcount: '845'
ht-degree: 100%

---

# Questions fréquentes sur la prise de décision {#decisioning-faq}

Cette page fournit des réponses aux questions fréquentes sur les fonctionnalités de prise de décision dans Adobe Journey Optimizer.

## Règles de limitation {#capping-rules}

+++**Que se passe-t-il lorsque plusieurs règles de limitation sont appliquées à une seule offre ?**

Une offre est limitée dès qu’**une seule condition est remplie**. Lorsqu’il existe plusieurs règles de limitation, l’offre cesse d’être affichée une fois qu’une règle atteint son seuil.

**Exemple :**
Si vous définissez deux règles de limitation pour une offre :
* 5 fois par profil et par semaine
* 100 fois au total pour les utilisateurs et utilisatrices

L’offre ne s’affichera plus pour une personne une fois qu’elle l’aura vue 5 fois dans une semaine, même si la limite totale de 100 n’a pas encore été atteinte. De même, une fois qu’un total de 100 impressions est atteint, l’offre cesse d’être affichée pour l’ensemble des utilisateurs et des utilisatrices.

En savoir plus sur les [règles de limitation](items.md#capping).

+++

## Formules de classement {#ranking-formulas}

+++**Quel est le rôle des audiences par rapport à un jeu de données complet dans les modèles d’IA ?**

Lors de la configuration de [modèles d’IA](ranking/ai-models.md), les jeux de données et les audiences ont des objectifs distincts.

* **Jeux de données** : capturent les événements de conversion (clics, commandes, chiffre d’affaires) qui servent de cibles d’optimisation pour le modèle.
* **Audiences** : fonctionnent comme des variables de prédicteur qui permettent au modèle de personnaliser les recommandations en fonction de l’appartenance à un segment client.

Les audiences ne limitent ni n’étendent la portée du modèle. Au lieu de cela, elles fournissent des attributs contextuels qui améliorent la capacité du modèle à effectuer des prédictions personnalisées sur différents segments clients.

Les deux composants sont requis pour des performances de modèle et des [modèles d’optimisation personnalisés](ranking/personalized-optimization-model.md) efficaces.

+++

+++**Comment les modifications apportées aux collections d’offres affectent-elles l’optimisation automatique ou les modèles d’optimisation personnalisés ?**

Le modèle d’optimisation automatique diffuse le trafic vers la meilleure offre disponible suivante en fonction des données de trafic des 14 derniers jours, que le modèle d’optimisation personnalisé utilise ou non les données de trafic des 30 derniers jours.

Lorsque plusieurs offres sont supprimées simultanément et que les offres restantes contiennent des données de trafic minimales dans la fenêtre de 14 ou 30 jours, le modèle peut présenter un comportement sous-optimal, notamment des modèles de distribution aléatoire ou un biais en faveur des offres avec des taux de conversion plus élevés en fonction de données d’impression limitées.

**Bonne pratique** : lorsque vous modifiez considérablement des collections d’offres, vérifiez que les offres restantes disposent de données de performances historiques suffisantes pour maintenir l’efficacité du modèle.

+++

+++**À quelle vitesse les modèles d’IA intègrent-ils les nouvelles offres ?**

Les modèles d’IA identifient et commencent à tester les nouvelles offres disponibles lors de leur prochain cycle d’entraînement :

* L’**optimisation automatique** identifie et commence à tester de nouvelles offres lors de son prochain cycle d’entraînement. L’entraînement de l’optimisation automatique a lieu 3 à 4 fois par jour, environ toutes les 6 heures.
* L’**optimisation personnalisée** identifie et commence à tester les nouvelles offres au fur et à mesure qu’elles sont ajoutées à la stratégie d’offre. Elles seront incluses dans le trafic d’exploration aléatoire. Ensuite, ces offres seront personnalisées dans le prochain cycle d’entraînement du modèle, sur une base hebdomadaire.

Une fois identifiés, les deux modèles commenceront à proposer immédiatement les nouvelles offres à certains visiteurs et visiteuses afin de tester leurs performances et de collecter des données sur leur efficacité.

En savoir plus sur les modèles d’[optimisation automatique](ranking/auto-optimization-model.md) et d’[optimisation personnalisée](ranking/personalized-optimization-model.md).

+++

+++**Comment les modèles d’IA s’optimisent-ils sans population témoin ?**

Les modèles d’optimisation automatique et d’optimisation personnalisée utilisent tous deux une stratégie d’« exploration-exploitation » qui élimine le besoin de populations témoins dédiées.

* **Phase initiale** : les modèles commencent par une exploration à 100 %, qui teste différentes offres pour établir des données de performances de base.
* **Optimisation adaptative** : à mesure que les événements comportementaux s’accumulent et que la précision des prédictions s’améliore, les modèles équilibrent automatiquement exploration et exploitation.
* **Apprentissage continu** : le système affecte progressivement davantage de trafic aux offres hautement performantes tout en continuant à tester les alternatives.

Cela garantit un apprentissage et une optimisation continus sur l’ensemble du trafic sans nécessiter de populations témoins distinctes.

+++

+++**Quelles sont les exigences minimales en matière de trafic pour des performances optimales du modèle d’IA ?**

Adobe recommande les seuils minimaux suivants pour garantir des performances de modèle efficaces :
* 1 000 impressions par offre/élément par semaine
* 100 événements de conversion par offre/élément par semaine

<!--
**Absolute minimums (per 30 days):**
* At least **250 impressions** per offer/item  
* At least **25 conversion events** per offer/item
-->

Par défaut, le système ne tente pas de créer des modèles personnalisés pour les offres/éléments comportant moins de 1 000 impressions ou 50 événements de conversion.

>[!NOTE]
>
>Dans les environnements de production avec des catalogues d’offres volumineux (environ 300 offres) et des règles métier restrictives, certaines offres peuvent approcher des seuils absolus inférieurs (250 impressions et 25 conversions par période de 30 jours). Ces valeurs représentent les exigences minimales en matière de données pour l’entraînement des modèles, mais peuvent ne pas garantir des performances optimales.

En savoir plus sur les [exigences en matière de collecte de données](data-collection/data-collection.md).

+++

+++**Comment des offres similaires affectent-elles les performances du modèle d’IA ?**

Les modèles d’IA génèrent des avantages de personnalisation supérieurs lorsque les offres s’adressent à des segments clients distincts. Lorsque les offres sont très similaires, on observe généralement deux résultats :

* **Performances équivalentes** : les offres ont des performances identiques et reçoivent une répartition du trafic à peu près égale.
* **Offre dominante** : en raison de différences mineures, une offre est plus performante que les autres sur tous les segments, capturant ainsi la majorité du trafic.

>[!NOTE]
>
>La différenciation des offres ne garantit pas une répartition équilibrée du trafic. Les offres avec des propositions de valeur objectivement supérieures (par exemple, 100 euros de remise contre 50 euros de remise) domineront généralement tous les segments clients, quels que soient les efforts de personnalisation.

**Bonne pratique** : concevez des offres qui se démarquent de manière significative et qui correspondent aux préférences distinctes des segments clients afin d’optimiser l’efficacité du modèle d’IA.

+++

+++**Comment les anomalies de trafic affectent-elles les performances du modèle d’IA ?**

Les anomalies de trafic sont incorporées au modèle proportionnellement dans la fenêtre glissante de 30 jours, ce qui fournit une stabilité du modèle pendant les fluctuations temporaires de trafic. Les pics ou les baisses à court terme ne perturbent pas de manière significative les prédictions ou les performances du modèle.

Un pic de trafic temporaire (par exemple, le double du trafic quotidien) a un effet minimal sur les performances globales du modèle, car le trafic anormal représente une petite fraction du jeu de données de 30 jours.

+++
