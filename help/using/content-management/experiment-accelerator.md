---
solution: Journey Optimizer
product: journey optimizer
title: Experimentation Accelerator
description: Améliorer votre capacité à mener des expériences efficacement et à générer des informations
feature: Experimentation
topic: Content Management
role: User
level: Beginner
keywords: contenu, expérience, multiple, audience, traitement
hide: true
hidefromtoc: true
source-git-commit: b52a0206e336185a8c630b7a6eace1fed14b1b66
workflow-type: tm+mt
source-wordcount: '964'
ht-degree: 2%

---

# Prise en main d’Experimentation Accelerator {#content-experiment}

>[!BEGINSHADEBOX]

* **[Prise en main d’Experimentation Accelerator](experiment-accelerator.md)**
* [Onglet Expériences](experiment-accelerator-monitor.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
> Experimentation Accelerator est actuellement en version bêta et ses fonctionnalités sont déployées progressivement.

**Experimentation Accelerator** est un outil puissant conçu pour rationaliser et améliorer le processus d’expérimentation. En s’intégrant à Adobe Target et Adobe Journey Optimizer, il fournit une plateforme centralisée pour gérer, analyser et optimiser les expériences. En exploitant les informations basées sur l’IA et les tests adaptatifs, l’Experimentation Accelerator vous permet de prendre des décisions basées sur les données, d’améliorer les stratégies marketing et de générer des résultats mesurables.

Les principaux avantages sont les suivants :

* **Expérimentation plus rapide** : exécutez des tests adaptatifs permanents avec des modèles qui s’ajustent au fil du temps.

* **Plateforme unifiée** : gérez toutes les expériences d’Adobe Target et de Journey Optimizer au même endroit.

* **Informations basées sur l’IA** : découvrez automatiquement les résultats clés, les facteurs de performance et les nouvelles opportunités.

* **Ciblage plus intelligent** : utilisez des données comportementales et de contenu pour donner la priorité aux expériences à fort impact.

* **Surveillance des KPI** : suivez les mesures telles que l’effet élévateur, le chiffre d’affaires et la confiance dans toutes les expériences.

* **Collaboration transparent** : partagez facilement les résultats et gérez les rôles d’équipe avec des alertes en temps réel.

Après avoir [créé et configuré votre expérience](content-experiment.md) et envoyé vos campagnes ou parcours à vos profils, vous pouvez accéder à **[!UICONTROL Experimentation Accelerator]** pour mieux comprendre les performances de votre expérience.

Pour accéder à **[!UICONTROL Experimentation Accelerator]** :

* Dans le menu de gauche, sélectionnez **[!UICONTROL Experimentation Accelerator]** dans le menu déroulant **[!UICONTROL Expérimentation]**.

* Vous pouvez également sélectionner **[!UICONTROL Experimentation Accelerator]** dans le sélecteur d’applications.

Notez que les utilisateurs disposant uniquement d’une licence Target peuvent y accéder uniquement par le biais du sélecteur d’applications.

<!--
<table style="table-layout:fixed"><tr style="border: 0;">
<td><img alt="Overview" href="experiment-accelerator-overview.md" src="assets/do-not-localize/experiments-2.jpeg">
<div align="center"><p><strong><a href="experiment-accelerator-overview.md">Overview</a></strong></p></div></td>
<td><img alt="Experiments" href="experiment-accelerator-monitor.md" src="assets/do-not-localize/experiment-overview.jpeg">
<div align="center"><p><strong><a href="experiment-accelerator-monitor.md">Experiments</a></strong></p></div></td>
<td><img alt="Metrics" href="experiment-accelerator-metrics.md" src="assets/do-not-localize/experiment-metrics.png">
<div align="center"><p><strong><a href="experiment-accelerator-metrics.md">Metrics</a></strong></p></div></td>
</tr></table>
-->

## Qu’Est-Ce Qu’Un Test A/B ?

Les tests A/B sont le processus consistant à comparer plusieurs versions d’un élément afin de déterminer laquelle est la plus performante par rapport à un objectif défini.

Les participants sont affectés de manière aléatoire à une version, connue sous le nom de variante, et leur comportement est suivi. Les résultats montrent si une version est statistiquement plus performante que les autres.

## Terminologie Clé

| Terme | Définition |
|-|-|
| Commande | Version d’origine utilisée comme référence pour la comparaison. |
| Variante ou traitement | Une nouvelle version créée pour tester le contrôle. |
| Hypothèse | Une prédiction sur les changements qui produiront un meilleur résultat, et pourquoi. |
| Taille de l’échantillon | Nombre d’individus ou de sessions inclus dans le test. |
| Signification statistique | Mesure de confiance indiquant que les résultats ne sont pas dus à un hasard. |
| Effet élévateur | Pourcentage d’amélioration ou de déclin d’une variante par rapport au contrôle. |
| Mesure principale | Principale mesure utilisée pour déterminer la réussite du test. |
| Mesures Secondaire | Les mesures de prise en charge qui proposent des insight supplémentaires ou permettent de surveiller les effets inattendus. |
| Intervalle de confiance | Plage estimée à l’intérieur de laquelle l’effet réel est susceptible de se produire. |
| Segment | Un sous-ensemble spécifique de l’audience analysé indépendamment (par exemple, les nouveaux utilisateurs, les visiteurs mobiles). |

## Bonnes pratiques pour l’exécution d’expériences

* **Commencez par une hypothèse claire**

  Une hypothèse solide inclut ce que vous êtes en train de changer, ce que vous vous attendez à voir se produire et pourquoi.
Exemple : _Nous pensons que la modification de X augmentera Y en raison de Z._

* **Définir une mesure de succès significative**

  Choisissez une mesure qui correspond à vos objectifs généraux. Évitez les mesures « de redirection » qui ont bonne apparence, mais qui ne reflètent pas un impact réel.

* **Tester une modification à la fois (lorsque cela est possible)**

  L’isolation des variables facilite l’interprétation précise des résultats. Si vous testez plusieurs modifications à la fois, vous ne saurez peut-être pas ce qui a provoqué l’effet.

* **Laissez le test s’exécuter suffisamment longtemps**

  Les conclusions prématurées peuvent être trompeuses. Attendez que la taille de l’échantillon soit statistiquement significative avant d’agir.

* **Tenez compte des facteurs externes**

  La saisonnalité, les vacances et d&#39;autres changements dans votre environnement peuvent fausser les résultats. Documentez tout ce qui peut influencer le comportement pendant votre test.

* **Utilisez la segmentation avec soin**

  La répartition des résultats par segment d’audience peut révéler des modèles masqués, mais évite de surinterpréter les petites tailles d’échantillon.

* **Documenter et partager les apprentissages**

  Conservez un enregistrement clair de ce qui a été testé, des raisons et de ce que vous avez appris. Cela permet de renforcer les connaissances institutionnelles et d&#39;éviter les erreurs répétées.

## Mesures courantes et ce qu’elles indiquent

| Mesure | Ce Qu’Il Mesure | Quand l’utiliser |
|-|-|-|
| Taux de conversion | Pourcentage d’utilisateurs et d’utilisatrices qui effectuent l’action souhaitée | Utile pour le suivi du succès d’une expérience axée sur des objectifs |
| Taux de clic publicitaire (CTR) | Pourcentage d’utilisateurs et d’utilisatrices qui cliquent sur un élément spécifique | Indique le caractère attrayant de l’expérience |
| Taux d’engagement | Niveau d’interaction des utilisateurs et utilisatrices avec l’expérience | Bon pour mesurer l&#39;intérêt ou l&#39;attention |
| Taux de bounces | Pourcentage d’utilisateurs et d’utilisatrices qui quittent rapidement sans agir | Peut indiquer une mauvaise adaptation ou une expérience confuse |
| Temps passé sur la page | Temps que les utilisateurs et utilisatrices passent sur une partie spécifique de l’expérience | Peut refléter la profondeur de l’intérêt ou la complexité |
| Chiffre d’affaires par visiteur (RPV) | Chiffre d’affaires moyen par utilisateur | Souvent utilisé dans des expériences axées sur le commerce |
| Taux de rétention | Pourcentage d’utilisateurs et d’utilisatrices qui reviennent ou restent engagés au fil du temps | Utile pour les évaluations de valeur à long terme |

## Qu’est-ce qui fait une bonne expérience ?

Une bonne expérience ne produit pas seulement une victoire, elle produit un apprentissage clair et exploitable.
Voici ce qu’il faut rechercher :

&amp;check; **Confiance statistique** : il est peu probable que la différence entre les variantes soit due au hasard.
&amp;check; **Alignement avec les objectifs** : la mesure principale reflète une progression significative vers un objectif commercial.
&amp;check; **Impact Secondaire** : aucun effet secondaire négatif significatif sur les mesures associées.
&amp;check; **Évolutivité** : le résultat peut éclairer les décisions futures ou être généralisé à d’autres domaines.
&amp;check; **Clarté** : la cause du résultat est raisonnablement isolée et comprise.

L’expérimentation ne consiste pas seulement à trouver la « meilleure » version, mais également à acquérir des connaissances par le biais de tests et d’itérations. Lorsqu’elles sont bien menées, les expériences révèlent des informations qui permettent de prendre des décisions plus intelligentes, d’offrir de meilleures expériences utilisateur et de meilleurs résultats.

>[!BEGINSHADEBOX]

**Exemple :**

* **Entreprise** : Chaîne hôtelière
* **Hypothèse** : si nous utilisons un langage plus urgent sur la page d&#39;accueil, cela entraînera davantage de réservations.
   * **Control** : Version originale
   * **Variante** : ajout d’une nouvelle version avec urgence.
   * **Mesure Principal** : Taux de réservation
   * **Mesures Secondaire** : Taux de rebond, temps passé sur le site
* **Résultat** : la variante a entraîné une augmentation de 14 % du taux de réservation, sans changement négatif dans les autres mesures.
* **Action** : envisagez de déployer la variante et d’exécuter des expériences de suivi pour tester des approches similaires dans d’autres domaines.

>[!ENDSHADEBOX]
