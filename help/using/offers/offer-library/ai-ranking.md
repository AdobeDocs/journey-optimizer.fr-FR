---
product: experience platform
solution: Experience Platform
title: À propos des modèles AI
description: En savoir plus sur les modèles AI qui permettent de classer les offres
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 4f7f7d1d-a12a-4ff6-b0ff-1a1c3d305a9d
source-git-commit: a7483965e3154d0ad34cfb56b6458bb63b46a26c
workflow-type: tm+mt
source-wordcount: '1530'
ht-degree: 4%

---

# Modèles AI {#ai-models}

## Prise en main des modèles AI {#get-started-with-ai-rankings}

Vous pouvez utiliser un système de modèles formé qui classe les offres à afficher pour un profil donné.

>[!CAUTION]
>
>L’utilisation des modèles AI est actuellement disponible en accès anticipé pour certains utilisateurs uniquement.

Cette fonctionnalité vous permet de créer différents **Modèles AI** en fonction des objectifs de votre entreprise. En utilisant ces différentes stratégies basées sur des objectifs dans une décision, le système de modèles formé vous aidera à comprendre comment les différents modèles d’IA affectent vos objectifs.

Par exemple, vous pouvez sélectionner un modèle d’IA pour le canal email et un autre pour le canal push. Pour chaque canal, le système de modèles formés exploite différents points de données pour déterminer l&#39;offre qui doit être présentée en premier pour un emplacement donné, plutôt que de prendre en compte les scores de priorité des offres ou une [formule de classement](create-ranking-formulas.md).

Une fois qu’un modèle AI a été créé, affectez-le à un emplacement dans une décision. En savoir plus dans la section [Configurer la sélection des offres dans les décisions](../offer-activities/configure-offer-selection.md).

>[!NOTE]
>
>Actuellement, le seul type de modèle pris en charge pour le classement par lʼIA dans [!DNL Journey Optimizer] est lʼ&#x200B;**optimisation automatique**.

## Modèle dʼoptimisation automatique {#auto-optimization}

Un modèle d’optimisation automatique vise à proposer des offres qui optimisent le retour (IPC) défini par les clients commerciaux. Ces indicateurs clés de performance peuvent prendre la forme de taux de conversion, de recettes, etc. À ce stade, l’optimisation automatique se concentre sur l’optimisation des clics sur les offres, avec pour cible la conversion des offres. L’optimisation automatique n’est pas personnalisée et s’optimise en fonction des performances &quot;globales&quot; des offres.

### Terminologie

Les termes suivants sont utiles pour aborder l’optimisation automatique :

* **Bandit à plusieurs bras**: A [bandit à plusieurs bras](https://en.wikipedia.org/wiki/Multi-armed_bandit)L’approche d’optimisation {target=&quot;_blank&quot;} équilibre l’apprentissage exploratoire et l’exploitation de cet apprentissage.

* **Tirage de Thomson**: l’échantillonnage de Thompson est un algorithme pour les problèmes de décision en ligne où les actions sont entreprises de manière séquentielle de manière à équilibrer entre l’exploitation de ce qui est connu pour maximiser les performances immédiates et l’investissement pour accumuler de nouvelles informations susceptibles d’améliorer les performances futures. [En savoir plus](#thompson-sampling)

* [**Distribution bêta**](https://en.wikipedia.org/wiki/Beta_distribution){target=&quot;_blank&quot;} : Jeu continu [distributions de probabilité](https://en.wikipedia.org/wiki/Probability_distribution){target=&quot;_blank&quot;} défini sur l’intervalle [0, 1] [paramétré](https://en.wikipedia.org/wiki/Statistical_parameter){target=&quot;_blank&quot;} par deux valeurs positives [paramètres de forme](https://en.wikipedia.org/wiki/Shape_parameter){target=&quot;_blank&quot;}.

### Échantillonnage de Thompson {#thompson-sampling}

L’algorithme qui sous-tend l’optimisation automatique est le suivant : **Échantillonnage de Thompson**. Dans cette section, nous abordons l’intuition sous-jacente à l’échantillonnage de Thompson.

[Échantillonnage de Thompson](https://en.wikipedia.org/wiki/Thompson_sampling){target=&quot;_blank&quot;}, ou bandits bayésiens, est une approche bayésienne du problème du bandit à plusieurs bras.  L&#39;idée de base est de traiter la récompense moyenne ?? de chaque offre en tant que **variable aléatoire** et utiliser les données que nous avons collectées jusqu&#39;à présent, pour mettre à jour notre &quot;croyance&quot; sur la récompense moyenne. Cette &quot;croyance&quot; est représentée mathématiquement par une **distribution des probabilités postérieures** - soit essentiellement une plage de valeurs pour la récompense moyenne, ainsi que la plausibilité (ou probabilité) que la récompense ait cette valeur pour chaque offre. Ensuite, pour chaque décision, nous **échantillonnage d’un point de chacune de ces distributions de récompense postérieures ;** et sélectionnez l&#39;offre dont la récompense échantillonnée a la valeur la plus élevée.

Ce processus est illustré dans la figure ci-dessous, où nous avons 3 offres différentes. Au départ, nous n&#39;avons aucune preuve des données et nous supposons que toutes les offres ont une distribution uniforme de récompense postérieur. Nous tirons un échantillon de la distribution de récompenses postérieures de chaque offre. L’exemple sélectionné dans la distribution de l’offre 2 a la valeur la plus élevée. Voici un exemple de **exploration**. Après avoir affiché l’offre 2, nous collectons toute récompense potentielle (par exemple, conversion/non-conversion) et mettons à jour la distribution postérieur de l’offre 2 à l’aide du théorème Bayes, comme expliqué ci-dessous.  Nous poursuivons ce processus et mettons à jour les répartitions postérieures chaque fois qu’une offre est affichée et que la récompense est collectée. Dans la seconde figure, l&#39;offre 3 est sélectionnée, bien que l&#39;offre 1 ait obtenu la récompense moyenne la plus élevée (sa distribution de récompense postérieur est la plus éloignée à droite), le processus d&#39;échantillonnage de chaque distribution nous a amenés à choisir une offre 3 apparemment sous-optimale. Ce faisant, nous nous donnons la possibilité d’en savoir plus sur la distribution de la vraie récompense d’Offer 3.

À mesure que davantage d’échantillons sont collectés, la confiance augmente et une estimation plus précise de la récompense possible est obtenue (correspondant à des distributions de récompense plus étroites). Ce processus de mise à jour de nos croyances au fur et à mesure que de nouvelles preuves deviennent disponibles est connu sous le nom **Inférence bayésienne**.

Finalement, si une offre (par exemple, l’offre 1) est un gagnant définitif, sa distribution de récompense supérieure sera séparée des autres. À ce stade, pour chaque décision, la récompense échantillonnée de l’offre 1 sera probablement la plus élevée, et nous la choisirons avec une probabilité plus élevée. Ceci est **exploitation** - nous sommes convaincus que l&#39;offre 1 est la meilleure et qu&#39;elle est donc choisie pour maximiser les récompenses.

![](../assets/ai-ranking-thompson-sampling.png)

**Figure 1**: *Pour chaque décision, nous prenons un point des distributions de récompense postérieures. L’offre avec la valeur d’échantillon la plus élevée (taux de conversion) sera choisie. Dans la phase initiale, toutes les offres ont une distribution uniforme puisque nous n’avons aucune preuve des taux de conversion des offres à partir des données. En collectant plus d&#39;échantillons, les distributions postérieures deviennent plus étroites et plus précises. En fin de compte, l’offre présentant le taux de conversion le plus élevé sera choisie à chaque fois.*

<!--
![](../assets/ai-ranking-thompson-sampling-initial.png)
![](../assets/ai-ranking-thompson-sampling-intermediate.png)
![](../assets/ai-ranking-thompson-sampling-ultimate.png)
-->

+++**Détails techniques**

Pour calculer/mettre à jour des distributions, nous utilisons **Le théorème de Bayes**. Pour chaque offre ***i***, nous allons calculer leur ***P(??i) | data)***, c’est-à-dire pour chaque offre ***i***, probabilité d’une valeur de récompense **??i** est, compte tenu des données que nous avons collectées jusqu’à présent pour cette offre.

De Bayes Theorem :

***Postérieur = Probabilité * Précédent***

Le **probabilité précédente** est l’estimation initiale de la probabilité de produire une sortie. La probabilité, une fois qu&#39;une preuve a été collectée, est connue sous le nom de **probabilité supérieure**. 

L’optimisation automatique est conçue pour prendre en compte les récompenses binaires (clic/non clic). Dans ce cas, la probabilité représente le nombre de succès provenant de N tests et est modélisée par une variable **Répartition binaire**. Pour certaines fonctions de probabilité, si vous choisissez un certain précédent, le postérieur se retrouve dans la même distribution que le précédent. Un tel préalable est alors appelé une **conjugate before**. Ce genre d&#39;avance rend le calcul de la distribution postérieur très simple. Le **Distribution bêta** est un conjugué avant la probabilité binaire (récompenses binaires). Il s’agit donc d’un choix pratique et judicieux pour les distributions de probabilité antérieures et postérieures. La distribution bêta prend deux paramètres, ***α*** et ***ß***. Ces paramètres peuvent être considérés comme le nombre de succès et d’échecs et la valeur moyenne donnée par :

![](../assets/ai-ranking-beta-distribution.png)

La fonction Probabilité comme nous l’avons expliqué ci-dessus est modélisée par une distribution binomiale, avec s réussites (conversions) et f échecs (aucune conversion) et q est une [variable aléatoire](https://en.wikipedia.org/wiki/Random_variable){target=&quot;_blank&quot;} avec une [distribution bêta](https://en.wikipedia.org/wiki/Beta_distribution){target=&quot;_blank&quot;}.

La distribution précédente est modélisée par la distribution bêta et la distribution postérieur se présente comme suit :

![](../assets/ai-ranking-posterior-distribution.svg)

Le postérieur est calculé simplement en ajoutant le nombre de succès et d&#39;échecs aux paramètres existants. ***α***, ***ß***.

Pour l’optimisation automatique, comme illustré dans l’exemple ci-dessus, nous commençons avec une distribution précédente. ***Beta(1, 1)*** (distribution uniforme) pour toutes les offres et après avoir obtenu ses succès et ses échecs pour une offre donnée, l’image de marque devient une distribution bêta avec des paramètres ***(s+, f+)*** pour cette offre.
+++

**Rubriques connexes**:

Pour une étude plus approfondie de l&#39;échantillonnage de Thompson, lisez les documents de recherche suivants :
* [Évaluation empirique de l’échantillonnage de Thompson](https://proceedings.neurips.cc/paper/2011/file/e53a0a2978c28872a4505bdb51db06dc-Paper.pdf){target=&quot;_blank&quot;}
* [Analyse de l’échantillonnage de Thompson pour le problème du bandit à plusieurs bras](http://proceedings.mlr.press/v23/agrawal12/agrawal12.pdf){target=&quot;_blank&quot;}

### Problème de démarrage à froid

Le problème de &quot;démarrage à froid&quot; se produit lorsqu’une nouvelle offre est ajoutée à une campagne et qu’aucune donnée n’est disponible sur le taux de conversion de la nouvelle offre. Au cours de cette période, nous devons définir une stratégie concernant la fréquence de sélection de cette nouvelle offre afin de minimiser la baisse de performance, tandis que nous collectons des informations sur le taux de conversion de cette nouvelle offre. Plusieurs solutions existent pour s&#39;attaquer à ce problème. La clé est de trouver un équilibre entre l&#39;exploration de cette nouvelle offre alors que nous ne sacrifions pas beaucoup l&#39;exploitation. Actuellement, nous utilisons la &quot;distribution uniforme&quot; comme estimation initiale du taux de conversion de la nouvelle offre (distribution précédente). En gros, nous donnons à toutes les valeurs de taux de conversion une probabilité d’occurrence égale.


![](../assets/ai-ranking-cold-start-strategies.png)

**Figure 2**: *Prenons l’exemple d’une campagne comportant trois offres. Pendant que la campagne est active, l’offre 4 est ajoutée à la campagne. Au départ, nous ne disposons pas de données sur le taux de conversion de l’offre 4 et nous devons résoudre le problème du démarrage à froid. Nous utilisons la distribution uniforme comme estimation initiale du taux de conversion de l’offre 4, tandis que nous collectons des données pour cette nouvelle offre. Comme expliqué dans la section [Échantillonnage de Thompson](#thompson-sampling) , pour choisir l’offre qui sera présentée à un utilisateur, nous échantillonnons les points des distributions de récompenses postérieures des offres et sélectionnons l’offre avec la valeur d’échantillon la plus élevée. Dans l&#39;exemple ci-dessus, l&#39;offre 4 est choisie puis basée sur la récompense collectée. La répartition postérieure de cette offre est mise à jour, comme expliqué dans la section [Échantillonnage de Thompson](#thompson-sampling) .*

### Mesure de l’effet élévateur

&quot;Effet élévateur&quot; est la mesure utilisée pour mesurer les performances de toute stratégie déployée dans le service de classement, par rapport à la stratégie de base (service des offres uniquement de manière aléatoire).

Par exemple, si nous voulons mesurer les performances d’une stratégie d’échantillonnage de Thompson (TS) utilisée dans le service de classement et que l’indicateur de performance clé est le taux de conversion (CVR), l’&quot;effet élévateur&quot; de la stratégie TS par rapport à la stratégie de base est défini comme suit :

![](../assets/ai-ranking-lift.png)
