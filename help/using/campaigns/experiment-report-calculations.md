---
title: Calculs statistiques utilisés dans le rapport d’expérience
description: En savoir plus sur les calculs statistiques utilisés lors de l’exécution des rapports d’expérience
feature: A/B Testing
topic: Content Management
role: User
level: Experienced
hide: true
hidefromtoc: true
source-git-commit: f4068450dde5f85652096c09e7f817dbab40a3d8
workflow-type: tm+mt
source-wordcount: '931'
ht-degree: 1%

---

# Calculs statistiques dans le rapport d’expérience {#experiment-report-calculations}

Cette page présente les calculs statistiques détaillés utilisés dans le rapport d’expérience pour les campagnes dans Adobe Journey Optimizer.

Notez que cette page est destinée aux utilisateurs techniques.

## Taux de conversion

Le taux de conversion ou **mean**, μ<sub>ν</sub> pour chaque traitement `ν` dans une expérience est défini comme un ratio de la somme de la mesure par rapport au nombre de profils affectés à cette mesure, N<sub>ν</sub>:

![](assets/statistical_1.png){width="125" align="center"}

Ici, Y<sub>iν</sub> est la valeur de la mesure d’objectif pour chaque profil ; `i`, qui a été affecté à une variante donnée *ν*. Lorsque la mesure de l’objectif est une mesure &quot;unique&quot;, c’est-à-dire qu’il s’agit d’un décompte du nombre de profils effectuant une action particulière, il s’affiche sous forme de taux de conversion et est formaté en pourcentage. Lorsque la mesure est une mesure &quot;count&quot; ou &quot;valeur totale&quot; (par exemple, ouvertures de courriers électroniques, recettes, respectivement), l’estimation moyenne de la mesure s’affiche sous la forme &quot;Comptage par profil&quot; ou &quot;Valeur par profil&quot;.

Si nécessaire, l’écart-type d’exemple est utilisé avec l’expression :

![](assets/statistical_2.png){width="225" align="center"}

## Effet élévateur {#lift}

Effet élévateur entre une variante  *ν* et la variante de contrôle  *ν<sub>0</sub>* est le &quot;delta&quot; relatif dans les taux de conversion, défini comme le calcul ci-dessous où les taux de conversion individuels sont tels que définis ci-dessus. Ce pourcentage est affiché.

![](assets/statistical_3.png){width="125" align="center"}

</br>

## Intervalles de confiance valides pour chaque traitement individuel

Le panneau Expérience de Parcours affiche des intervalles de confiance (séquences de confiance) &quot;tout moment&quot; valides pour chaque traitement d’une expérience.

Séquence de confiance pour une variante individuelle `ν` est au coeur de la méthodologie statistique utilisée par l’Adobe. Vous trouverez sa définition dans [cette page](https://doi.org/10.48550/arXiv.2103.06476) (reproduit à partir de [Waudby-Smith et al.]).

Si vous souhaitez estimer un paramètre cible `ψ` comme le taux de conversion d’une variante dans une expérience, la dichotomie entre une séquence d’intervalles de confiance (CI) à &quot;temps fixe&quot; et une séquence de confiance uniforme (CS) peut être résumée comme suit :

![](assets/statistical_4.png){width="500" align="center"}

Pour un intervalle de confiance régulier, la garantie probabiliste que le paramètre cible se trouve dans la plage des valeurs des<sub>n</sub> n’est valide qu’à une seule valeur fixe de `n` (où `n` est le nombre d’échantillons). Inversement, pour une séquence de confiance, il est garanti qu’à tout moment/toutes les valeurs de la taille de l’échantillon `t`, la valeur &quot;true&quot; du paramètre d’intérêt se trouve dans les limites.

Cela a quelques implications profondes qui sont très importantes pour les tests en ligne :

* Le CS peut éventuellement être mis à jour chaque fois que de nouvelles données sont disponibles.
* Les expériences peuvent être surveillées en permanence, stoppées de manière adaptative ou continues.
* L’erreur type-I est contrôlée à tous les temps d’arrêt, y compris aux heures dépendantes des données.

Adobe utilise des séquences de confiance asynchrones, qui, pour une variante individuelle avec une estimation moyenne. `μ` possède le formulaire suivant :

![](assets/statistical_5.png){width="300" align="center"}

où:

* `N` est le nombre d’unités pour cette variante.
* `σ` est un exemple d’estimation de l’écart type (défini ci-dessus).
* `α` est le niveau d’erreur type I souhaité (ou probabilité de méprise). Cette valeur est toujours définie sur 0,05.
* ρ<sup>2</sup> est une constante qui ajuste la taille d’échantillon à laquelle le CS est le plus serré. L&#39;Adobe a choisi une valeur universelle ρ<sup>2</sup> = 10<sup>-2.8</sup>, qui est approprié pour les types de taux de conversion observés dans les expériences en ligne.

## Degré de confiance {#confidence}

La confiance utilisée par l’Adobe est une confiance &quot;valide à tout moment&quot;, obtenue en inversant la séquence de confiance pour l’effet de traitement moyen.

Pour être précis, dans deux échantillons *t* test de la différence de moyens entre deux variantes, il existe un mappage 1:1 entre la variable *p*-value pour ce test et l’intervalle de confiance pour la différence de moyens. Par analogie, un *p*-value peut être obtenu en inversant la séquence de confiance (valide à tout moment) de l’estimateur d’effet de traitement moyen :

![](assets/statistical_6.png){width="200" align="center"}

Ici, *E* est une attente. L’estimateur utilisé est un estimateur de propension pondéré (IPW) inverse. N = N<sub>0</sub> +N<sub>1</sub> unités, affectations de variantes pour chaque unité `i` étiqueté par A<sub>i</sub>=0,1 si l&#39;unité est affectée à la variante `ν`=0,1. Si les utilisateurs sont affectés avec une probabilité fixe (propension)<sub>0</sub>, (1<sub>0</sub>), et leur mesure de résultat est Y<sub>i</sub>, l’estimateur de l’IPW pour l’effet de traitement moyen est :

![](assets/statistical_12.png){width="400" align="center"}

Constatant que *f* est la fonction d&#39;influence, Waudby-Smith et al. a montré que la séquence de confiance pour cet estimateur est :

![](assets/statistical_7.png){width="500" align="center"}

Remplacer la probabilité d’affectation par ses estimations empiriques : π<sub>0</sub> = N<sub>0</sub>/N, le terme de variance peut être exprimé en termes d’estimations moyennes individuelles μ<sub>0,1</sub> et les estimations d’écart type,<sub>0,1</sub> comme :

![](assets/statistical_8.png){width="500" align="center"}

Ensuite, rappelez-vous que pour un test d&#39;hypothèse normal avec la statistique de test z = (μ<sub>A</sub>-μ<sub>0</sub>/uler<sub>p</sub>) il existe une correspondance entre `p`-values et intervalles de confiance :

![](assets/statistical_9.png){width="500" align="center"}

where `Φ` est la distribution cumulée de la normale standard. Pour tout moment valide `p`-values, étant donné la séquence de confiance de l’effet de traitement moyen défini ci-dessus, nous pouvons inverser cette relation :

![](assets/statistical_10.png){width="600" align="center"}

Enfin, la **degré de confiance valide** est :

![](assets/statistical_11.png){width="200" align="center"}

## Déclaration d’une expérience comme étant concluante

Pour une expérience avec deux bras, le panneau Expérience Journey Optimizer affiche un message indiquant qu’une expérience est **concluant** lorsque le degré de confiance en cours de validité dépasse 95 % (c’est-à-dire lorsqu’il est valide `p`-value est inférieur à 5 %).

Lorsque plus de deux variantes sont présentes, la correction Bonferonni est appliquée pour contrôler le taux d&#39;erreur par famille. Pour une expérience avec `K` les traitements et un traitement de base unique (contrôle), il y a `K-1` tests d&#39;hypothèse indépendants. La correction de Bonferonni signifie que nous rejetons l&#39;hypothèse nulle que le contrôle et une variante donnée ont des moyens égaux, si le moment est valide `p`-value (définie ci-dessus) est inférieur à un seuil de `α/(K-1)`.

## bras le plus performant

Lorsqu’une expérience est déclarée concluante, le bras le plus performant s’affiche. Il s’agit du bras le plus performant (moyenne la plus élevée ou taux de conversion), parmi l’ensemble qui comprend la commande et tous les bras ayant une `p`-value qui est inférieure au seuil de Bonferonni.
