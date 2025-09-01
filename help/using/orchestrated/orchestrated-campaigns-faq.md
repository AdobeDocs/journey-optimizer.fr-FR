---
solution: Journey Optimizer
product: journey optimizer
title: Questions fréquentes sur les campagnes orchestrées
description: Questions fréquentes sur les campagnes orchestrées Journey Optimizer
hide: true
hidefromtoc: true
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
source-git-commit: 13bc5f91e0e47bf36b9b9921fa926f8a5e2a50d6
workflow-type: tm+mt
source-wordcount: '765'
ht-degree: 4%

---

# Questions fréquentes {#faq-oc}

Vous trouverez ci-dessous les questions fréquentes sur les campagnes orchestrées par Adobe Journey Optimizer.

Vous avez besoin de plus d’informations ? Utilisez les options de commentaires au bas de cette page pour soulever votre question.

## Que sont les campagnes orchestrées ? {#what-are-oc}

Les campagnes orchestrées dans Adobe Journey Optimizer aident les marques à exécuter des campagnes marketing complexes de type « un à plusieurs » à grande échelle. Ils sont conçus pour l’engagement initié par la marque, tel que les promotions, les campagnes saisonnières ou les communications basées sur un compte.

Par rapport aux campagnes à envoi unique, elles intègrent l’**orchestration et le séquencement** au marketing sortant : les audiences passent par un workflow à plusieurs étapes ensemble, plutôt que de recevoir une seule opération.

## Que puis-je faire avec les campagnes orchestrées ? {#what-can-i-do}

Les fonctionnalités principales sont les suivantes :

* **Audiences à la demande** : créez et affinez instantanément des groupes cibles à l’aide de requêtes relationnelles.
* **Segmentation d’entités multiples** : créez des audiences précises en connectant les données client à des entités associées (par exemple, comptes, achats, réservations).
* **Visibilité de pré-envoi** : consultez un nombre précis d’audiences avant le lancement pour optimiser le ciblage.
* **Workflows à plusieurs étapes** : exécutez des campagnes séquencées telles que des promotions saisonnières, des lancements de produits ou des offres de fidélité.

>[!BEGINSHADEBOX]

**Bonnes pratiques**

* Définissez un **objectif de campagne clair** avant de concevoir des workflows.
* Commencez avec une **audience pilote** pour valider les nombres et la logique avant la mise à l’échelle.
* Conservez des règles de segmentation **aussi simples que possible** pour optimiser les performances et la transparence.
* Utilisez des **conventions de nommage cohérentes** pour les audiences et les campagnes afin de faciliter la gestion.

>[!ENDSHADEBOX]


## Quels canaux sont pris en charge ? {#channels}

Les campagnes orchestrées prennent en charge **e-mails, SMS et notifications push**.

>[!BEGINSHADEBOX]

**Recommandations**

* Faites correspondre le canal à la **nature de votre message** (par exemple, urgent = SMS, offres personnalisées = e-mail, contextuel = notification push).
* Validez toujours les préférences de consentement et d’abonnement avant d’activer un canal.
* Testez le rendu des messages sur plusieurs appareils et clients pour garantir une expérience cohérente.

>[!ENDSHADEBOX]

## En quoi les campagnes orchestrées sont-elles différentes des Parcours ? {#oc-vs-journeys}

* **Campagnes orchestrées** : idéal pour les campagnes **par lots, de type « un à plusieurs »**. Des audiences entières se déplacent à travers la zone de travail de campagne.
* **Parcours** : idéal pour l’engagement **en temps réel, individuel**. Chaque client ou cliente passe par le parcours à son propre rythme, déclenché par un comportement ou des événements.

>[!BEGINSHADEBOX]

**Conseil** - De nombreuses entreprises utilisent **les deux ensemble** : des Parcours pour les expériences déclenchées et réactives, ainsi que des campagnes orchestrées pour les initiatives planifiées basées sur un calendrier.

>[!ENDSHADEBOX]

## Comment fonctionne le modèle de données ? {#data-model}

Les campagnes utilisent une **base de données relationnelle**. Vous pouvez ainsi interroger différents jeux de données (par exemple, clients, produits, abonnements) et les connecter de manière flexible pour une segmentation avancée.

>[!BEGINSHADEBOX]

**Bonnes pratiques**

* Organisez les jeux de données de sorte que les **relations (jointures)** reflètent la logique commerciale.
* Évitez les jointures inutiles pour maintenir les performances des requêtes.
* Validez les exemples de résultats avant d’exécuter des extractions à grande échelle.

>[!ENDSHADEBOX]

## Puis-je personnaliser les messages avec ces données ? {#personalization}

Oui. Vous pouvez utiliser les profils client ainsi que les données liées (comme les achats ou les abonnements) pour personnaliser le contenu sur tous les canaux pris en charge.

>[!BEGINSHADEBOX]

**Recommandations**

* Utilisez des **données transactionnelles et comportementales** pour rendre les offres pertinentes.
* Combinez les **attributs statiques** (par exemple, le niveau de fidélité) avec les **attributs dynamiques** (par exemple, la date de dernier achat).
* Personnalisation concise : surcharger les messages avec des données peut nuire à la lisibilité.

>[!ENDSHADEBOX]


## S’intègre-t-il à d’autres solutions Adobe ? {#integrations}

* **Customer Journey Analytics** : les rapports d&#39;orchestration de Campaign sont disponibles.
* **Real-Time CDP** : les audiences créées dans les campagnes peuvent être lues dans CDP.
* **Composition d’audience fédérée (FAC)** : disponible sous la forme d’un module complémentaire.

## Qu’en est-il des autorisations et du consentement ? {#permissions}

Les autorisations et le consentement sont gérés de manière centralisée dans Adobe Experience Platform. Les mêmes règles s’appliquent à la fois aux Parcours et aux campagnes orchestrées afin d’assurer la conformité et une expérience client cohérente.

>[!BEGINSHADEBOX]

**Bonnes pratiques**

* Appliquez la **gouvernance centralisée** évitez de gérer le consentement séparément au niveau de la campagne.
* Contrôlez régulièrement les données de consentement pour détecter les incohérences.
* Respectez les **opt-outs spécifiques à un canal** sans supposer que le consentement global couvre tous les canaux.

>[!ENDSHADEBOX]

## Puis-je effectuer une segmentation ad hoc ? {#ad-hoc}

Oui. Avec la **Segmentation en direct**, vous pouvez créer des requêtes complexes sur place et les activer instantanément sur les canaux sortants.

>[!BEGINSHADEBOX]

**Conseils**

* Utilisez la segmentation ad hoc pour les **besoins urgents** (par exemple, les promotions Flash).
* Enregistrez et documentez les requêtes utiles afin qu’elles puissent être réutilisées dans les prochaines campagnes.
* Validez le nombre d’audiences avant l’activation pour éviter un envoi insuffisant ou excessif.

>[!ENDSHADEBOX]

## Cela permet-il de prendre des décisions ? {#decisioning}

Actuellement, la prise de décision n’utilise pas les données relationnelles des campagnes orchestrées.

## Comment fonctionne le déploiement dans les environnements ? {#deployment}

Les objets créés dans des campagnes orchestrées (par exemple, des audiences, des workflows) sont liés au sandbox dans lequel ils sont créés. Les workflows de package et de déploiement standard dans les environnements (de développement, d’évaluation et de production) ne sont actuellement pas disponibles pour les campagnes orchestrées.

>[!BEGINSHADEBOX]

**Bonnes pratiques**

* Conservez les **sandbox distincts** pour l’expérimentation, l’assurance qualité et la production.
* Documentez minutieusement les configurations pour activer la réplication manuelle si nécessaire.
* Alignez-vous sur les équipes de gouvernance pour réduire la dérive de configuration entre les environnements.

>[!ENDSHADEBOX]

## Existe-t-il des pratiques recommandées pour exécuter des campagnes à grande échelle ? {#scale}

Oui, suivez les bonnes pratiques ci-dessous :

* **Planifiez des campagnes autour des calendriers professionnels** (lancements de produits, pics saisonniers) pour aligner le volume et les ressources.
* Utilisez les **aperçus d’audience** avant l’envoi pour confirmer la taille attendue et éviter les surprises.
* Dans la mesure du possible, **échelonnez les délais d’envoi** pour éviter de surcharger les systèmes en aval (p. ex. centres d’appels, sites Web).
* Établissez une **routine de surveillance** : suivez les logs de diffusion, les taux d’erreur et les désinscriptions après chaque envoi.
* Exécutez **analyse post-campagne** dans Customer Journey Analytics pour affiner le ciblage et l’orchestration pour le cycle suivant.
