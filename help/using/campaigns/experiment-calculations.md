---
title: Calculs statistiques utilisés par l’expérience
description: En savoir plus sur les calculs statistiques utilisés lors de l’exécution d’expériences
feature: Overview
topic: Content Management
role: User
level: advanced
hide: true
hidefromtoc: true
exl-id: 60a1a488-a119-475b-8f80-3c6f43c80ec9
source-git-commit: 0fb54571ea7620c981e746f8ac240b675e2f0d64
workflow-type: tm+mt
source-wordcount: '905'
ht-degree: 0%

---

# Présentation des calculs statistiques {#experiment-calculations}

>[!AVAILABILITY]
>
>Actuellement, la fonctionnalité d’expérience de contenu n’est disponible que pour un ensemble d’organisations (disponibilité limitée). Pour en savoir plus, contactez votre représentant Adobe.

Cet article décrit les calculs statistiques utilisés lors de l’exécution d’expériences dans Adobe Journey Optimizer. L’expérience utilise des méthodes statistiques avancées pour calculer **Séquences de confiance** et **Confiance**, qui vous permettent d’exécuter vos expériences aussi longtemps que nécessaire, et de surveiller vos résultats en continu.

Cet article décrit le fonctionnement de l’expérience et présente de manière intuitive le fonctionnement de l’Adobe. **Tout moment de séquence de confiance valide**.

Pour les utilisateurs experts, les détails techniques et les références sont présentés dans la section [cette page](https://experienceleague.adobe.com/docs/journey-optimizer/assets/confidence_sequence_technical_details.pdf?lang=en).

## Erreurs de test et de contrôle statistiques {#statistical-testing}

![](assets/technote_1.png)

Comme illustré dans le tableau ci-dessus, de nombreuses méthodologies d’référencement statistique sont conçues pour contrôler deux types d’erreurs :

* **Faux positifs (erreurs de type I)**: est un rejet incorrect de l’hypothèse nulle, alors qu’en fait elle est vraie. Dans le contexte des expériences en ligne, cela signifie que nous concluons faussement que la mesure des résultats est différente entre chaque traitement, bien qu’elle ait été la même.
   </br>Avant de lancer l&#39;expérience, nous sélectionnons généralement un seuil `$\alpha$`. Une fois l’expérience terminée, la variable `$p$-value` est calculé, et nous rejetons la variable `null if $p < \alpha$`. Un seuil couramment utilisé est : `$\alpha = 0.05$`, ce qui signifie qu&#39;à long terme, nous nous attendons à ce que 5 expériences sur 100 soient des faux positifs.

* **Faux négatifs (erreurs de type II)**: signifie que nous ne parvenons pas à rejeter l’hypothèse nulle bien qu’elle soit fausse. Pour les expériences, cela signifie que nous ne rejetons pas l’hypothèse nulle, alors qu’en fait elle est différente. Pour contrôler ce type d&#39;erreur, nous avons généralement besoin d&#39;un nombre suffisant d&#39;utilisateurs dans notre expérience pour garantir un certain pouvoir, défini comme `$1 - \beta$`(soit moins la probabilité d’une erreur de type II).

La plupart des techniques d’inférencement statistique nécessitent que vous fixiez à l’avance la taille de l’échantillon, en fonction de la taille de l’effet que vous souhaitez déterminer, ainsi que votre tolérance d’erreur (`$\alpha$` et `$\beta$`) en avance. Toutefois, la méthodologie de Adobe Journey Optimizer est conçue pour vous permettre d’examiner en permanence vos résultats, quelle que soit la taille de l’échantillon.

## Méthodologie statistique de l’Adobe : Tout moment de séquence de confiance valide

A **Séquence de confiance** est l’analogique séquentiel d’un événement **Intervalle de confiance**, par exemple, si vous répétez vos expériences cent fois, et calculez une estimation de la mesure moyenne et de sa séquence de confiance de 95 % associée pour chaque nouvel utilisateur qui entre dans l’expérience. Une séquence de confiance de 95 % inclut la valeur réelle de la mesure dans 95 des 100 expériences que vous avez exécutées. Un intervalle de confiance de 95 % ne pouvait être calculé qu&#39;une seule fois par expérience afin de garantir la même garantie de couverture de 95 % ; pas avec chaque nouvel utilisateur. Les séquences de confiance vous permettent donc de surveiller en permanence les expériences, sans augmenter les taux d’erreur False Positive.

La différence entre les séquences de confiance et les intervalles de confiance pour une seule expérience est illustrée dans l’animation ci-dessous :

![](assets/technote_2.gif)

**Séquences de confiance** déplacer le focus des expériences vers l’estimation plutôt que vers les tests d’hypothèse, c’est-à-dire se concentrer sur une estimation précise de la différence de moyens entre les traitements, plutôt que de rejeter ou non une hypothèse nulle basée sur un seuil de signification statistique.

Toutefois, de la même manière que la relation entre `$p$-values`ou **Confiance**, et **Intervalles de confiance**, il existe également une relation entre **Séquences de confiance** et tout moment valide `$p$-values`, ou tout autre degré de confiance valide. Étant donné la familiarité de quantités comme le degré de confiance, l&#39;Adobe fournit à la fois les **Séquences de confiance** et tout moment de fiabilité dans ses rapports.

Les fondements théoriques de **Séquences de confiance** proviennent de l&#39;étude de séquences de variables aléatoires connues sous le nom de martingales. Voici quelques-uns des principaux résultats pour les lecteurs experts, mais les interprétations des praticiens sont claires :

    Les séquences de confiance peuvent être interprétées comme des analogies séquentielles sécurisées d’intervalles de confiance. Vous pouvez consulter et interpréter les données de vos expériences à tout moment et les arrêter en toute sécurité ou continuer des expériences. L’attribut Any Valid Confidence, ou `$p$-value` correspondant, peut également être interprété en toute sécurité.

Il est important de noter que, puisque les séquences de confiance sont &quot;valides à tout moment&quot;, elles seront plus conservatrices qu’une méthodologie d’horizon fixe utilisée à la même taille d’échantillon. Les limites de la séquence de confiance sont généralement plus larges qu’un calcul d’intervalle de confiance, tandis que le degré de confiance valide à tout moment sera plus petit qu’un calcul de confiance d’horizon fixe. L&#39;avantage de ce conservatisme est que vous pouvez interpréter vos résultats en toute sécurité et à tout moment.

## Déclaration finale d’une expérience

![](assets/experimentation_report_2.png)

Chaque fois que vous consultez le rapport d’expérimentation, Adobe analyse les données accumulées jusqu’à présent dans l’expérience et déclare une expérience &quot;concluante&quot; lorsque la confiance valide franchit un seuil de 95 % pour au moins un des traitements.

À ce stade, le traitement qui présente les meilleures performances (en fonction du taux de conversion ou de la valeur de mesure normalisée par le profil) est mis en surbrillance dans la partie supérieure de l’écran du rapport et indiqué par une étoile dans le rapport tabulaire. Seuls les traitements dont la confiance est supérieure à 95 %, ainsi que la référence, sont pris en compte dans cette détermination.

Lorsqu’il existe plus de deux traitements, le lien de correction Bonferroni est utilisé pour corriger les problèmes de comparaison multiples et contrôle le taux d’erreur par famille. Dans ce scénario, il est également possible qu’il existe plusieurs traitements dont la confiance est supérieure à 95 % et dont les intervalles de confiance se chevauchent. Dans ce cas, l’Adobe déclarera celui qui a le taux de conversion le plus élevé (ou la valeur de mesure normalisée par le profil) comme le plus performant.
