---
title: Questions fréquentes sur la prise de décision
description: Obtenez des réponses aux questions courantes sur les fonctionnalités de prise de décision
feature: Decisioning
topic: Integrations
role: User
level: Intermediate
version: Journey Orchestration
hide: true
hidefromtoc: true
source-git-commit: 7205017785283e3db4d64ed595ac8f187f43307b
workflow-type: tm+mt
source-wordcount: '785'
ht-degree: 0%

---

# Questions fréquentes sur la prise de décision {#decisioning-faq}

Cette page fournit des réponses aux questions fréquentes sur les fonctionnalités de prise de décision dans Adobe Journey Optimizer.

## Règles de limitation {#capping-rules}

+++**Que se passe-t-il lorsque plusieurs règles de limitation sont appliquées à une seule offre ?**

Une offre est plafonnée dès qu’**une seule condition est remplie**. Lorsqu’il existe plusieurs règles de limitation, l’offre cesse d’être affichée une fois qu’une règle atteint son seuil.

**Exemple:**
Si vous définissez deux règles de limitation pour une offre :
* 5 fois par profil par semaine
* 100 fois le total pour tous les utilisateurs

L’offre ne s’affichera plus pour un utilisateur ou une utilisatrice une fois qu’il ou elle l’aura vue 5 fois par semaine, même si la limite totale de 100 n’a pas encore été atteinte. De même, une fois que 100 impressions totales sont atteintes, l’offre cesse d’être affichée pour tous les utilisateurs.

En savoir plus sur les [&#x200B; règles de limitation &#x200B;](items.md#capping).

+++

## Formules de classement {#ranking-formulas}

+++**Quel est le rôle des audiences dans les modèles d’IA ?**

Lors de la configuration de [modèles d’optimisation personnalisés](ranking/personalized-optimization-model.md), les jeux de données et les audiences ont des objectifs distincts :

* **Jeux de données** : capturez les événements de conversion (clics, commandes, chiffre d’affaires) qui servent de cibles d’optimisation pour le modèle.
* **Audiences** : fonctionnent comme des variables de prédicteur qui permettent au modèle de personnaliser les recommandations en fonction de l’appartenance à un segment client.

Les audiences ne limitent ni n’étendent la portée du modèle. Au lieu de cela, ils fournissent des attributs contextuels qui améliorent la capacité du modèle à effectuer des prédictions personnalisées sur différents segments de clients.

Les deux composants sont nécessaires pour optimiser les performances des modèles d’optimisation personnalisés. En savoir plus sur les [modèles d’IA](ranking/ai-models.md).

+++

+++**Comment les modifications apportées aux collections d’offres affectent-elles les modèles d’IA si vous utilisez des modèles d’optimisation automatique ou personnalisés ?**

Les deux modèles dirigeront le trafic vers la meilleure offre disponible suivante en fonction des données de trafic des 30 derniers jours.

Lorsque plusieurs offres sont supprimées simultanément et que les offres restantes contiennent des données de trafic minimales dans la fenêtre de 30 jours, le modèle peut présenter un comportement sous-optimal, notamment :
* Modèles de distribution aléatoire
* Biais en faveur des offres avec des taux de conversion plus élevés en fonction de données d’impression limitées

**Bonne pratique** : lorsque vous modifiez considérablement des collections d’offres, vérifiez que les offres restantes disposent de données de performances historiques suffisantes pour maintenir l’efficacité du modèle.

+++

+++**À quelle vitesse les modèles d’IA intègrent-ils les nouvelles offres ?**

Les modèles d’IA identifient et commencent à tester les nouvelles offres disponibles lors de leur prochain cycle de formation :

* **Optimisation automatique** : exécutions de formation quotidiennes
* **Optimisation personnalisée** : cycles de formation hebdomadaires

Une fois identifiés, les deux modèles commenceront à proposer immédiatement les nouvelles offres à certains visiteurs afin de tester leurs performances et de collecter des données sur leur efficacité.

En savoir plus sur les modèles [optimisation automatique](ranking/auto-optimization-model.md) et [optimisation personnalisée](ranking/personalized-optimization-model.md).

+++

+++**Comment les modèles d’IA s’optimisent-ils sans population témoin ?**

Les modèles d’optimisation automatique et d’optimisation personnalisée utilisent tous deux une stratégie d’exploration-exploitation qui élimine le besoin de populations témoins dédiées :

* **Phase initiale** : les modèles commencent par une exploration à 100 %, qui teste différentes offres pour établir des données de performances de base.
* **Optimisation adaptative** : à mesure que les événements comportementaux s’accumulent et que la précision des prédictions s’améliore, les modèles équilibrent automatiquement l’exploration et l’exploitation.
* **Apprentissage continu** : le système affecte progressivement davantage de trafic aux offres hautement performantes tout en continuant à tester les alternatives.

Cela garantit un apprentissage et une optimisation continus de tout le trafic sans nécessiter de populations témoins distinctes.

+++

+++**Quelles sont les exigences minimales en matière de trafic pour des performances optimales du modèle d’IA ?**

Adobe recommande les seuils minimaux suivants pour garantir des performances de modèle efficaces :

**Minimums recommandés (par semaine) :**
* 1 000 impressions par offre/article
* 100 événements de conversion par offre/article

<!--**Absolute minimums (per 30 days):**
* At least **250 impressions** per offer/item  
* At least **25 conversion events** per offer/item-->

Par défaut, le système ne tente pas de créer des modèles personnalisés pour les offres/articles comportant moins de 1 000 impressions ou 50 événements de conversion.

>[!NOTE]
>
>Dans les environnements de production avec des catalogues d’offres volumineux (environ 300 offres) et des règles commerciales restrictives, certaines offres peuvent approcher des seuils absolus inférieurs (250 impressions et 25 conversions par période de 30 jours). Ils représentent les exigences minimales en matière de données pour la formation des modèles, mais peuvent ne pas garantir des performances optimales.

En savoir plus sur les [exigences de collecte de données](data-collection/data-collection.md).

+++

+++**En quoi la similarité des offres affecte-t-elle les performances du modèle d’IA ?**

Les modèles d’IA génèrent des avantages de personnalisation supérieurs lorsque les offres s’adressent à des segments de clientèle distincts. Lorsque les offres sont très similaires, deux résultats sont typiques :

* **Performances équivalentes** : les offres ont des performances identiques et reçoivent une distribution du trafic à peu près égale.
* **Offre dominante** : en raison de différences mineures, une offre est plus performante que les autres sur tous les segments, capturant la majorité du trafic.

>[!NOTE]
>
>La différenciation des offres ne garantit pas une répartition équilibrée du trafic. Les offres avec des propositions de valeur objectivement supérieures (par exemple, 100 euros de remise contre 50 euros de remise) domineront généralement tous les segments de clientèle, quels que soient les efforts de personnalisation.

**Bonne pratique** : concevez des offres avec une différenciation significative qui s’alignent sur les préférences de segment client distinctes afin d’optimiser l’efficacité du modèle d’IA.

+++

+++**Comment les anomalies de trafic affectent-elles les performances du modèle d’IA ?**

Les anomalies de trafic sont intégrées au modèle proportionnellement dans la fenêtre glissante de 30 jours.

**Analyse d&#39;impact :**
Un pic de trafic temporaire (par exemple, 2 fois le trafic quotidien) a un effet minimal sur les performances globales du modèle, car le trafic anormal représente une petite fraction du jeu de données de 30 jours.

**insight clé** : la fenêtre dynamique de données de 30 jours offre une stabilité de modèle pendant les fluctuations temporaires du trafic. Les pics ou les baisses à court terme ne perturbent pas de manière significative les prédictions ou les performances du modèle.

+++
