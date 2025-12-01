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
source-git-commit: 59e85eb7a14f88d95b2ef97e3ace11a65f115b75
workflow-type: tm+mt
source-wordcount: '979'
ht-degree: 1%

---

# Questions fréquentes sur la prise de décision {#decisioning-faq}

Cette page fournit des réponses aux questions fréquentes sur les fonctionnalités de prise de décision dans Adobe Journey Optimizer.

## Règles de limitation {#capping-rules}

+++**Que se passe-t-il lorsque vous créez plusieurs règles de limitation pour une offre ? Allons-nous arrêter d’afficher l’offre lorsque nous répondons à l’une des règles de limitation, ou à toutes les règles ?**

L&#39;offre est plafonnée dès qu&#39;**une condition est remplie**. Cela signifie que l’une des règles de limitation empêche l’affichage de l’offre une fois son seuil atteint.

Par exemple, si vous avez deux règles de limitation :
* 5 fois par profil par semaine
* 100 fois le total pour tous les utilisateurs

L’offre ne s’affichera plus pour un utilisateur ou une utilisatrice une fois qu’il ou elle l’aura vue 5 fois par semaine, même si la limite totale de 100 n’a pas encore été atteinte. De même, une fois que 100 impressions totales sont atteintes, l’offre cesse d’être affichée pour tous les utilisateurs.

En savoir plus sur les [&#x200B; règles de limitation &#x200B;](items.md#capping).

+++

## Formules de classement {#ranking-formulas}

+++**Pourquoi ajouter une audience à un modèle d’IA ? Quel est l’avantage d’ajouter des audiences par rapport à un jeu de données complet ? Le modèle sera-t-il restreint ou élargi?**

Lorsque vous utilisez des modèles d’IA (en particulier [modèles d’optimisation personnalisés](ranking/personalized-optimization-model.md)) :

* Les **jeux de données** sont ajoutés pour collecter vos événements de conversion (clics, commandes, chiffre d’affaires). Ce sont les résultats pour lesquels le modèle tente d’optimiser.
* Des **audiences** sont ajoutées pour être utilisées comme variables prédictrices dans le modèle. Ils permettent de personnaliser les prédictions pour essayer de prévoir les clics, les commandes ou les recettes de différents segments de clientèle.

Les jeux de données et les audiences sont nécessaires au fonctionnement efficace du modèle d’optimisation personnalisé. Les audiences **ne limitent ni n’étendent** le modèle, mais fournissent un contexte supplémentaire qui aide le modèle à prendre de meilleures décisions personnalisées.

En savoir plus sur les [modèles d’IA](ranking/ai-models.md).

+++

+++**L’ajout ou la suppression d’offres à une collection aura-t-il un impact sur le modèle si j’utilise des modèles d’optimisation automatique ou d’optimisation personnalisée ?**

Les deux modèles dirigeront le trafic vers la meilleure offre disponible suivante en fonction des données de trafic des 30 derniers jours.

Si plusieurs offres sont supprimées à la fois et que les offres restantes ont reçu très peu de trafic au cours des 30 derniers jours, la distribution des offres peut se comporter de manière inattendue. Cela peut entraîner une répartition aléatoire ou un biais en faveur de certaines offres qui ont un taux de conversion plus élevé basé sur seulement quelques impressions.

**Bonne pratique** : lorsque vous apportez des modifications importantes aux collections d’offres, assurez-vous que les offres restantes disposent de données de performances historiques suffisantes pour maintenir des performances de modèle optimales.

+++

+++**Combien de temps faut-il aux modèles d’IA pour comprendre qu’un nouveau contenu a été ajouté et commencer à l’ajouter au mix ?**

Les deux modèles d’IA identifieront les offres nouvellement disponibles lors de la prochaine exécution de formation :

* **Optimisation automatique** : exécutions de formation quotidiennes
* **Optimisation personnalisée** : cycles de formation hebdomadaires

Une fois identifiés, les deux modèles commenceront à proposer immédiatement les nouvelles offres à certains visiteurs afin de tester leurs performances et de collecter des données sur leur efficacité.

En savoir plus sur les modèles [optimisation automatique](ranking/auto-optimization-model.md) et [optimisation personnalisée](ranking/personalized-optimization-model.md).

+++

+++**Si nous n’avons pas de populations témoins dans les modèles d’IA, apprenons-nous et optimisons-nous l’ensemble du trafic en même temps ?**

Oui. Les deux modèles d’IA (optimisation automatique et optimisation personnalisée) utilisent une approche « explorer et exploiter » :

* Au départ, les deux modèles sont **exploration à 100 %**, ce qui signifie qu’ils testent différentes offres pour collecter des données de performances.
* Au fil du temps, les modèles **gèrent automatiquement le compromis explorer/exploiter** à mesure que les événements comportementaux sont collectés et que les prédictions s’améliorent.
* Les modèles déplacent progressivement davantage de trafic vers des offres plus performantes tout en continuant à explorer et à tester d’autres options.

Cela garantit un apprentissage et une optimisation continus de tout le trafic sans nécessiter de populations témoins distinctes.

+++

+++**De combien d’événements d’optimisation avons-nous besoin pour être statistiquement significatifs ? Existe-t-il un seuil de trafic minimal pour une surface ?**

Pour optimiser les performances des modèles, Adobe recommande les minimums suivants :

**Minimums recommandés (par semaine) :**
* Au moins 1 000 impressions **&#x200B;**&#x200B;par offre/article
* Au moins **100 événements de conversion** par offre/article

<!--**Absolute minimums (per 30 days):**
* At least **250 impressions** per offer/item  
* At least **25 conversion events** per offer/item-->

Par défaut, le système ne tente pas de créer des modèles personnalisés pour les offres/articles comportant moins de 1 000 impressions ou 50 événements de conversion.

**Important** : dans la pratique, certains clients ont de nombreuses offres (~300) dans un seul modèle et certaines offres peuvent avoir des règles commerciales très restrictives. Les minimums absolus (250 impressions/25 conversions par période de 30 jours) représentent le seuil le plus bas que le système peut prendre en charge pour les modèles de construction.

En savoir plus sur les [exigences de collecte de données](data-collection/data-collection.md).

+++

+++**Le contenu des offres doit-il être clairement différencié pour que les modèles d’IA fonctionnent correctement ? Que se passe-t-il si j’ai plusieurs offres trop similaires les unes aux autres ?**

D’une manière générale, le modèle d’IA est plus susceptible de générer des avantages liés à la personnalisation lorsque les **offres sont adaptées aux différents types de clients**.

Lorsque les offres sont très similaires, l’un des deux résultats est probable :

* **Performances similaires** : les offres ont des performances identiques et reçoivent une part relativement égale du trafic.
* **Dominance** : de petites différences peuvent faire en sorte qu’une offre domine les autres pour tous les types de clients et elles recevront l’essentiel du trafic.

>[!NOTE]
>
>Les différences d’offres ne garantissent pas qu’une offre ne dominera pas les autres. Par exemple, une offre de réduction de 100 euros surpasse presque toujours une offre de réduction de 50 euros pour tous les types de clients, quelle que soit la personnalisation.

**Bonne pratique** : assurez-vous que vos offres offrent une différenciation significative qui peut plaire à différents segments de clientèle pour des performances optimales du modèle d’IA.

+++

+++**Qu’advient-il du modèle en cas d’anomalie de trafic, comme un pic de trafic énorme ? Cela provoquera-t-il des problèmes ou soulèvera-t-il l’étrangeté ?**

Un pic de trafic serait inclus dans la modélisation proportionnellement au trafic des 30 derniers jours.

Par exemple, un pic de trafic quotidien multiplié par 2 aura un effet relativement modeste sur le modèle global, car il y a 29 jours de trafic normal qui représentent nettement plus de données comportementales globales.

**Point clé** : la fenêtre dynamique de 30 jours permet au modèle de maintenir la stabilité lors d’anomalies de trafic temporaires. Les pointes ou les creux à court terme ne perturbent pas considérablement les performances du modèle.

+++

## Rubriques connexes {#related-topics}

<!--* [Get started with Decisioning](gs-experience-decisioning.md)-->
* [Créer des éléments de décision](items.md)
* [Présentation des modèles d’IA](ranking/ai-models.md)
* [Mécanismes de sécurisation et limitations de la prise de décisions](decisioning-guardrails.md)

