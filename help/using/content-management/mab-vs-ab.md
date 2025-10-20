---
title: Calculs statistiques utilisés dans le rapport d’expérience
description: En savoir plus sur les tests A/B et le bandit manchot
feature: A/B Testing, Experimentation
role: User
level: Experienced
exl-id: 1f7b74d2-77c3-4113-8e6a-1e2a95117748
source-git-commit: a659f596c0d37f4b91ec41e52c02c8385f6ae16b
workflow-type: ht
source-wordcount: '607'
ht-degree: 100%

---

# Expériences A/B et bandit manchot {#mab-vs-ab}

>[!CONTEXTUALHELP]
>id="ajo_ab_test_mab"
>title="Type d’expérience"
>abstract="Le type d’expérience détermine la manière dont le trafic est réparti entre les traitements pendant le test. Choisissez la méthode qui correspond le mieux à vos objectifs :</br><b>Expérience A/B</b> : partage le trafic au fur et à mesure que vous définissez entre les traitements et les mesures de performances jusqu’à ce que les résultats soient statistiquement significatifs. Idéal pour savoir quel traitement est le plus performant dans une comparaison contrôlée.</br><b>Bandit manchot</b> : déplace le trafic vers des traitements plus performants lors de la collecte de données, en équilibrant la vitesse et l’optimisation. Utile lorsque vous souhaitez maximiser les conversions pendant l’expérience.</br><b>Utilisez votre propre bandit manchot</b> : utilisez votre propre algorithme pour décider de l’affectation du trafic, ce qui vous offre plus de flexibilité si vous disposez d’un modèle ou d’une stratégie personnalisé."

Cette page présente une comparaison détaillée des expériences **A/B** et **bandit manchot**, en expliquant leurs forces, leurs limites respectives et les scénarios dans lesquels chaque approche est la plus efficace.


## A/B {#ab-test}

L’expérience A/B traditionnelle implique la répartition égale du trafic entre les traitements et le maintien de cette attribution jusqu’à la fin de l’expérience. Une fois la signification statistique atteinte, le traitement gagnant est identifié et mis à l’échelle.

### Avantages

Les principaux points forts des expériences A/B traditionnelles sont les suivants :

* **Rigueur statistique**

  La conception fixe fournit des taux d’erreur et des intervalles de confiance bien définis.

  Les cadres de test des hypothèses, par exemple le degré de confiance de 95 %, sont plus faciles à appliquer et à interpréter.

  Des expériences correctement optimisées réduisent la probabilité de faux positifs.

* **Simplicité**

  La méthodologie est simple à concevoir et à exécuter.

  Les résultats peuvent être communiqués clairement aux parties prenantes ne possédant pas de compétences techniques.

* **Collecte exhaustive des données**

  Chaque traitement reçoit une exposition adéquate, ce qui permet d’analyser non seulement la variante gagnante, mais également les alternatives peu performantes.

  Ces informations supplémentaires peuvent éclairer les décisions stratégiques à long terme.

* **Contrôle de biais**

  L’affectation fixe réduit la vulnérabilité aux biais tels que la « malédiction du gagnant » ou la régression vers la moyenne.

### Limites

Les principales limites des expériences A/B traditionnelles sont les suivantes :

* **Coût de l’opportunité**

  Une proportion importante du trafic est dirigée vers des traitements inférieurs, ce qui peut réduire les conversions ou le revenu pendant le test.

  Le traitement gagnant ne peut pas être mis en œuvre avant la fin de l’expérience.

* **Exigence de durée fixe**

  Les tests doivent généralement être effectués pour leur horizon prédéfini, même si les conditions externes, par exemple la saisonnalité, les fluctuations du marché, changent à mi-parcours.

  L’adaptation au cours de l’expérience est limitée.

## Bandit manchot {#mab-experiment}

Les algorithmes du bandit manchot utilisent l’affectation adaptative : à mesure que les preuves s’accumulent, un trafic plus important est dirigé vers des traitements plus performants. L’objectif est de maximiser la récompense cumulée au cours de l’expérience plutôt que de se concentrer uniquement sur le résultat final.

### Avantages

Les principales forces des méthodes de bandit manchot sont les suivantes :

* **Optimisation plus rapide**

  Les traitements prometteurs sont prioritaires plus tôt, ce qui améliore les performances globales pendant le test.

* **Adaptation**

  Les affectations sont mises à jour en continu à mesure que les données sont collectées, faisant du bandit manchot une méthode adaptée aux environnements dynamiques.

* **Coût d’opportunité réduit**

  Les mauvais traitements sont rapidement éliminés, ce qui réduit le trafic gaspillé.

* **Aptitude aux tests continus**

  Efficace pour les expériences en cours ou les contextes où le trafic est coûteux.

### Limites

Les principales limites des méthodes de bandit manchot sont les suivantes :

* **Des garanties statistiques plus faibles**

  Les tests d’hypothèse traditionnels sont plus difficiles à appliquer et les règles d’arrêt sont moins claires.

* **Transparence Réduite**

  L’affectation adaptative peut être difficile à expliquer aux parties prenantes.

* **Informations limitées sur les traitements moins performants**

  Les traitements faibles sont peu exposés, ce qui limite la richesse de l’information diagnostique.

* **Complexité de l’implémentation**

  Nécessite des algorithmes et une infrastructure avancés, avec un plus grand risque de mauvaise configuration.

## Quand utiliser A/B ou le bandit manchot

| Scénario | Méthode recommandée |
|-|-|
| Vous exécutez des tests exploratoires ou axés sur la recherche. | A/B |
| Vous exécutez des campagnes permanentes, par exemple des annonces publicitaires, des recommandations. | Bandit manchot |
| Vous souhaitez maximiser les conversions pendant le test. | Bandit manchot |
| Vous voulez des informations claires et fiables. | A/B |
| Vous devez vous adapter rapidement, par exemple, à cause de changements saisonniers. | Bandit manchot |
| Le trafic est limité et vous souhaitez optimiser rapidement le retour sur investissement. | Bandit manchot |
| Le trafic est élevé et vous pouvez vous permettre un apprentissage plus lent. | A/B |
| Les parties prenantes ont besoin de points de décision clairs. | A/B |
