---
title: Calculs statistiques utilisés dans le rapport d’expérience
description: En savoir plus sur les tests AB par rapport au bandit manchot
feature: A/B Testing, Experimentation
role: User
level: Experienced
source-git-commit: 397fad9c95e0c11c0496ab5c9adfb6f8169de4f6
workflow-type: tm+mt
source-wordcount: '506'
ht-degree: 4%

---

# Expériences A/B contre le bandit manchot {#mab-vs-ab}

<!--
>[!CONTEXTUALHELP]
>id="ajo_ab_test_mab"
>title="Experiment type"
>abstract="Experiment type determines how traffic is allocated between treatments during your test. Choose the method that best aligns with your goals:</br>
>
>* **A/B Experiment**: Splits traffic as you define between treatments and measures performance until results are statistically significant. Best for learning which treatment performs better in a controlled comparison.
>
>* **Multi-armed Bandit**: Shifts traffic toward higher-performing treatments as data is collected, balancing speed and optimization. Useful when you want to maximize conversions during the experiment.
>
>* **Bring your own Multi-armed Bandit**: Use your own algorithm to decide traffic allocation, giving you flexibility if you have a custom model or strategy."
-->

Cette page présente une comparaison détaillée des expériences **A/B** et **bandit manchot**, en expliquant leurs forces, leurs limites respectives et les scénarios dans lesquels chaque approche est la plus efficace.

## A/B {#ab-test}

L’expérience A/B traditionnelle implique le partage égal du trafic entre les traitements et le maintien de cette attribution jusqu’à la fin de l’expérience. Une fois la signification statistique atteinte, le traitement gagnant est identifié et mis à l’échelle.

### Avantages

Les principaux points forts des expériences A/B traditionnelles sont les suivants :

* **Rigueur statistique**

  La conception fixe fournit des taux d’erreur et des intervalles de confiance bien définis.

  Les cadres de test des hypothèses, par exemple le degré de confiance de 95 %, sont plus faciles à appliquer et à interpréter.

  Des expériences correctement optimisées réduisent la probabilité de faux positifs.

* **Simplicité**

  La méthodologie est simple à concevoir et à exécuter.

  Les résultats peuvent être communiqués clairement aux parties prenantes non techniques.

* **Collecte de données complète**

  Chaque traitement reçoit une exposition adéquate, ce qui permet d’analyser non seulement la variante gagnante, mais également les alternatives peu performantes.

  Ces informations supplémentaires peuvent éclairer les décisions stratégiques à long terme.

* **Contrôle de biais**

  L&#39;allocation fixe réduit la vulnérabilité aux biais tels que la « malédiction du gagnant » ou la régression à la moyenne.

### Limites

Les principales limites des expériences A/B traditionnelles sont les suivantes :

* **Coût d’opportunité**

  Une proportion importante du trafic est dirigée vers des traitements inférieurs, ce qui peut réduire les conversions ou les recettes pendant le test.

  Le traitement gagnant ne peut pas être mis en œuvre avant la fin de l&#39;expérience.

* **Exigence de durée fixe**

  Les tests doivent généralement être effectués pour leur horizon prédéfini, même si les conditions externes, par exemple la saisonnalité, les fluctuations du marché, changent à mi-parcours.

  L’adaptation au cours de l’expérience est limitée.

## Bandit manchot {#mab-experiment}

Les algorithmes du bandit manchot utilisent l’allocation adaptative : à mesure que les preuves s’accumulent, un trafic plus important est dirigé vers des traitements plus performants. L’objectif est de maximiser la récompense cumulée au cours de l’expérience plutôt que de se concentrer uniquement sur le résultat final.

### Avantages

Les principales forces des méthodes de bandit manchot sont les suivantes :

* **Optimisation plus rapide**

  Les traitements prometteurs sont prioritaires plus tôt, ce qui améliore les performances globales pendant le test.

* **Adaptivité**

  Les allocations sont mises à jour en continu à mesure que les données sont collectées, ce qui rend le bandit manchot adapté aux environnements dynamiques.

* **Coût d’opportunité réduit**

  Les mauvais traitements sont rapidement éliminés, ce qui réduit le trafic gaspillé.

* **Aptitude aux tests continus**

  Efficace pour les expériences en cours ou les contextes où le trafic est coûteux.

### Limites

Les principales limites des méthodes de bandit manchot sont les suivantes :

* **Des garanties statistiques plus faibles**

  Les tests d’hypothèse traditionnels sont plus difficiles à appliquer et les règles d’arrêt sont moins claires.

* **Transparence Réduite**

  L’allocation adaptative peut être difficile à expliquer aux parties prenantes.

* **Informations limitées sur les traitements sous-performants**

  Les traitements faibles sont peu exposés, ce qui limite l&#39;insight diagnostique.

* **Complexité de l’implémentation**

  Nécessite des algorithmes et une infrastructure avancés, avec un plus grand risque de mauvaise configuration.

## Quand utiliser A/B ou le bandit manchot

| Scénario | Méthode recommandée |
|-|-|
| Vous exécutez des tests exploratoires ou axés sur la recherche | A/B |
| Vous exécutez des campagnes permanentes, par exemple des annonces publicitaires, des recommandations | Bandit Manchot |
| Vous souhaitez maximiser les conversions pendant le test. | Bandit Manchot |
| Vous voulez des informations claires et fiables | A/B |
| Il faut s&#39;adapter rapidement, par exemple, aux changements saisonniers | Bandit Manchot |
| Le trafic est limité et vous souhaitez optimiser rapidement le retour sur investissement | Bandit Manchot |
| Le trafic est élevé et vous pouvez vous permettre un apprentissage plus lent | A/B |
| Les parties prenantes ont besoin de points de décision clairs | A/B |

