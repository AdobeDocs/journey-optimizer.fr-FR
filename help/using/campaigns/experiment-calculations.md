---
solution: Journey Optimizer
product: journey optimizer
title: Calculs statistiques utilisés par l’expérience Adobe Journey Optimizer
description: En savoir plus sur les calculs statistiques utilisés lors de l’exécution d’expériences
feature: A/B Testing
topic: Content Management
role: User
level: Experienced
keywords: contenu, expérience, statistique, calcul
hide: true
hidefromtoc: true
exl-id: 60a1a488-a119-475b-8f80-3c6f43c80ec9
badge: label="Beta" type="Informative"
source-git-commit: 160e4ce03d3be975157c30fbe511875a85b00551
workflow-type: tm+mt
source-wordcount: '909'
ht-degree: 100%

---

# Présentation des calculs statistiques {#experiment-calculations}

>[!BEGINSHADEBOX]

Cette documentation couvre les sujets suivants :

* [Prise en main de l’expérience de contenu](get-started-experiment.md)
* [Créer une expérience de contenu](content-experiment.md)
* **[Présentation des calculs statistiques](experiment-calculations.md)**
* [Configurer des rapports d’expérience](reporting-configuration.md)
* [Calculs statistiques dans le rapport d’expérience](experiment-report-calculations.md)

>[!ENDSHADEBOX]

Cet article décrit les calculs statistiques utilisés lors de l’exécution d’expériences dans Adobe Journey Optimizer.

L’expérimentation utilise des méthodes statistiques avancées pour calculer les **Séquences de confiance** et les **degrés de confiance**, qui vous permettent d’exécuter vos expériences aussi longtemps que nécessaire, et de surveiller vos résultats en continu.

Cet article décrit le fonctionnement de l’expérience et fournit une introduction intuitive aux **Séquences de confiance valides à tout moment** d’Adobe.

Pour les personnes expertes, les détails techniques et les références sont présentés sur [cette page](../campaigns/assets/confidence_sequence_technical_details.pdf).

## Tests statistiques et erreurs de contrôle {#statistical-testing}

![](assets/technote_1.png)

Comme illustré dans le tableau ci-dessus, de nombreuses méthodologies d’inférence statistique sont conçues pour contrôler deux types d’erreurs :

* **Faux positifs (erreurs de type I)** : est un rejet incorrect de l’hypothèse nulle, alors qu’en fait elle est vraie. Dans le contexte des expériences en ligne, cela signifie que nous concluons faussement que la mesure des résultats est différente entre chaque traitement, bien qu’elle ait été la même.
   </br>Nous sélectionnons généralement un seuil avant de lancer l’expérience`\alpha`. Une fois l’expérience terminée, la variable `p-value` est calculée, et nous rejetons la valeur `null if p < \alpha`. Un seuil couramment utilisé est : `\alpha = 0.05`, ce qui signifie qu’à long terme, nous nous attendons à ce que 5 expériences sur 100 soient des faux positifs.

* **Faux négatifs (erreurs de type II)** : signifie que nous ne parvenons pas à rejeter l’hypothèse nulle bien qu’elle soit fausse. Pour les expériences, cela signifie que nous ne rejetons pas l’hypothèse nulle, alors qu’en fait elle est différente. Pour contrôler ce type d’erreur, nous avons généralement besoin d’un nombre suffisant d’utilisateurs dans notre expérience pour garantir une certaine force, définie comme `1 - \beta`(soit 1 moins la probabilité d’erreur de type II).

La plupart des techniques d’inférence statistique nécessitent que vous fixiez préalablement la taille de l’échantillon, en fonction de la taille de l’effet que vous souhaitez déterminer, ainsi que votre tolérance d’erreur (`\alpha` et `\beta`) tout cela à l’avance. Toutefois, la méthodologie d’Adobe Journey Optimizer est conçue pour vous permettre d’examiner en permanence vos résultats, quelle que soit la taille de l’échantillon.

## Méthodologie statistique d’Adobe : séquences de confiance valides à tout moment

Une **Séquence de confiance** est l’analogie séquentielle d’un **Intervalle de confiance**, par exemple, si vous répétez vos expériences cent fois, et calculez une estimation de la mesure moyenne et de sa séquence de confiance de 95 % associée pour chaque nouvel utilisateur qui entre dans l’expérience, Une séquence de confiance de 95 % inclut la valeur réelle de la mesure dans 95 des 100 expériences exécutées. Un intervalle de confiance de 95 % ne pouvait être calculé qu’une seule fois par expérience afin de fournir la même garantie de couverture de 95 % ; et pas avec chaque nouvel utilisateur. Les séquences de confiance vous permettent donc de surveiller en permanence les expériences, sans augmenter les taux d’erreurs Faux Positifs.

La différence entre les séquences de confiance et les intervalles de confiance pour une seule expérience est illustrée dans l’animation ci-dessous :

![](assets/technote_2.gif)

Les **Séquences de confiance** réorientent l’objectif des expériences vers l’estimation plutôt que vers les tests d’hypothèse, c’est-à-dire qu’elles se concentrent sur une estimation précise de la différence de moyenne entre les traitements, plutôt que sur la nécessité de rejeter ou non une hypothèse nulle basée sur un seuil de signification statistique.

Toutefois, de la même manière qu’il existe une relation entre `p-values`, ou la **Confiance** et les **Intervalles de confiance**, il existe également une relation entre les **séquences de confiance** et les `p-values` valides à tout moment, ou la Confiance valide à tout moment. Étant donné la familiarité des quantités comme le degré de confiance, Adobe fournit dans ses rapports à la fois les **Séquences de confiance** et la Confiance valide à tout moment.

Les fondements théoriques des **Séquences de confiance** proviennent de l’étude de séquences de variables aléatoires connues sous le nom de martingales. Voici quelques-uns des principaux résultats pour les personnes expertes, mais les points essentiels à l’intention des praticiens et des praticiennes sont clairs :

>[!NOTE]
>
>Les séquences de confiance peuvent être interprétées comme des analogies séquentielles sécurisées d’intervalles de confiance. Vous pouvez consulter et interpréter les données de vos expériences quand vous voulez, puis arrêter ou continuer les expériences en toute sécurité. L’attribut Confiance valide à tout moment correspondant, ou `p-value`, peut également être interprété en toute sécurité.

Il est important de noter que, puisque les séquences de confiance sont « valides à tout moment », elles seront plus conservatrices qu’une méthodologie d’horizon fixe utilisée à la même taille d’échantillon. Les limites de la séquence de confiance sont généralement plus larges qu’un calcul d’intervalle de confiance, tandis que le degré de confiance valide à tout moment sera plus petit qu’un calcul de confiance à horizon fixe. L’avantage de ce conventionnalisme est que vous pouvez en toute sécurité interpréter vos résultats à tout moment.

## Déclaration d’une expérience comme étant concluante

![](assets/experimentation_report_2.png)

Chaque fois que vous consultez le rapport d’expérimentation, Adobe analyse les données accumulées jusqu’à présent dans l’expérience et déclare une expérience « concluante » lorsque le degré de confiance valide franchit un seuil de 95 % pour au moins un des traitements.

À ce stade, le traitement qui présente les meilleures performances (en fonction du taux de conversion ou de la valeur de mesure normalisée par le profil) est mis en surbrillance dans la partie supérieure de l’écran du rapport et signalé par une étoile dans le rapport tabulaire. Seuls les traitements dont le degré de confiance est supérieur à 95 %, ainsi que la ligne de base, sont pris en compte dans cette classification.

Lorsqu’il existe plus de deux traitements, le lien de correction Bonferroni est utilisé pour corriger les problèmes de comparaison multiples et contrôler le taux d’erreur par famille. Dans ce scénario, il est également possible qu’il existe plusieurs traitements dont le degré de confiance est supérieur à 95 % et dont les intervalles de confiance se chevauchent. Dans ce cas, Adobe Journey Optimizer déclarera celui qui a le taux de conversion le plus élevé (ou la valeur de mesure normalisée par le profil) comme le plus performant.
