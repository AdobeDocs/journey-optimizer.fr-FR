---
solution: Journey Optimizer
product: journey optimizer
title: Questions fréquentes sur les campagnes orchestrées
description: Questions fréquentes sur les campagnes orchestrées Journey Optimizer
hide: true
hidefromtoc: true
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
source-git-commit: a6a8521254005159b410790f88877d0591a16d15
workflow-type: tm+mt
source-wordcount: '1091'
ht-degree: 7%

---

# Questions fréquentes {#faq-oc}

Vous trouverez ci-dessous les questions fréquentes sur les campagnes orchestrées Adobe Journey Optimizer.

Vous avez besoin de plus d’informations ? Utilisez les options de commentaires au bas de cette page pour soulever votre question.

## Qu’est-ce que l’orchestration des campagnes ? {#what-are-oc}

L’orchestration des campagnes est une fonctionnalité de Journey Optimizer qui prend en charge les workflows en une ou plusieurs étapes qui utilisent le magasin de données relationnelles pour créer et segmenter les audiences dans le but d’un engagement par lots.

Journey Optimizer intègre un nouveau type de campagnes : **Campagnes orchestrées**. Les campagnes orchestrées aident les marques à exécuter des campagnes marketing complexes de type « un à plusieurs » à grande échelle. Ils sont conçus pour l’engagement initié par la marque, tel que les promotions, les campagnes saisonnières ou les communications basées sur un compte.

Par rapport aux campagnes à envoi unique/action, elles apportent l’**orchestration et le séquencement** au marketing sortant : les audiences passent par un workflow à plusieurs étapes ensemble, plutôt que de recevoir une seule opération.

## Que puis-je faire avec une campagne orchestrée ? {#what-can-i-do}

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

## Comment accéder à l&#39;orchestration des campagnes ? {#access-oc}

Pour accéder à l’orchestration de campagne, votre licence doit inclure le package **Journey Optimizer - Campagnes et parcours** ou **Journey Optimizer - Campagnes**. Contactez votre représentant ou représentante Adobe pour confirmer votre licence et effectuer une mise à jour si nécessaire.


## Quels canaux sont pris en charge ? {#channels}

Vous pouvez créer des campagnes orchestrées pour envoyer des **e-mails**, **SMS** et **notifications push**.


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

## Qu’est-ce que la segmentation d’entités multiples ? {#multi-entity}

Dans Adobe Journey Optimizer, l’orchestration de Campaign utilise une base de données relationnelle. Ce type de modèle de données comporte des schémas de données distincts connectés par le biais de relations 1:1 ou 1:many. Cela permet aux utilisateurs et utilisatrices de démarrer une requête sur n’importe quel schéma, pas seulement au niveau du destinataire, puis de basculer entre les schémas associés, tels que les achats, les produits, les réservations ou les détails du destinataire, offrant ainsi une grande flexibilité dans la manière dont les segments et les audiences peuvent être créés et
raffiné.

>[!BEGINSHADEBOX]

**Exemple** - Ciblez tous les destinataires dont les abonnements expirent au cours des 30 prochains jours. Dans Campaign Orchestration, la requête peut commencer par le schéma Abonnements , rechercher uniquement la colonne Date d’expiration de ce schéma et renvoyer tous les abonnements dont l’expiration est prévue, puis cumuler les données des destinataires liées à ces identifiants d’abonnements spécifiques et renvoyer les résultats plus rapidement et plus efficacement que les modèles de données qui lancent chaque requête au niveau du destinataire.

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

Oui. Dans Campaign Orchestration, un profil de destinataire appelé « Entité de personnes » peut être mis à jour et ces données sont utilisées pour la personnalisation. En outre, les données enrichies des entités liées dans la base de données relationnelle peuvent également être utilisées pour la personnalisation. Vous pouvez utiliser les profils client ainsi que les données liées (comme les achats ou les abonnements) pour personnaliser le contenu sur tous les canaux pris en charge.

>[!BEGINSHADEBOX]

**Recommandations**

* Utilisez des **données transactionnelles et comportementales** pour rendre les offres pertinentes.
* Combinez les **attributs statiques** (par exemple, le niveau de fidélité) avec les **attributs dynamiques** (par exemple, la date de dernier achat).
* Personnalisation concise : surcharger les messages avec des données peut nuire à la lisibilité.

>[!ENDSHADEBOX]


## S’intègre-t-il à d’autres solutions Adobe ? {#integrations}

Oui. L’orchestration des campagnes est intégrée nativement à :

* **Customer Journey Analytics** : les rapports d&#39;orchestration de Campaign sont disponibles.
* **Real-Time CDP** : les audiences créées dans les campagnes peuvent être lues dans Real-Time CDP.
* **Composition d’audience fédérée (FAC)** : disponible sous la forme d’un module complémentaire.

## Qu’en est-il des autorisations et du consentement ? {#permissions}

Les autorisations et le consentement pour les campagnes et les parcours orchestrés sont gérés de manière centralisée dans Adobe Experience Platform. Ces paramètres sont appliqués aux deux solutions pour chaque destinataire avant l’envoi.

>[!BEGINSHADEBOX]

**Bonnes pratiques**

* Appliquez la **gouvernance centralisée** évitez de gérer le consentement séparément au niveau de la campagne.
* Contrôlez régulièrement les données de consentement pour détecter les incohérences.
* Respectez les **désinscriptions spécifiques à un canal** — ne supposez pas que le consentement global couvre tous les canaux.

>[!ENDSHADEBOX]

## Puis-je effectuer une segmentation ad hoc ? {#ad-hoc}

Dans l’orchestration de Campaign, nous appelons la segmentation ad hoc « segmentation en direct », où vous pouvez accéder à toutes les données disponibles dans la boutique relationnelle en temps réel, créer une requête complexe par-dessus et obtenir le résultat pour une activation instantanée via les canaux sortants (par exemple : e-mail + SMS).

>[!BEGINSHADEBOX]

**Conseils**

* Utilisez la segmentation ad hoc pour les **besoins urgents** (par exemple, les promotions Flash).
* Enregistrez et documentez les requêtes utiles afin qu’elles puissent être réutilisées dans les prochaines campagnes.
* Validez le nombre d’audiences avant l’activation pour éviter un envoi insuffisant ou excessif.

>[!ENDSHADEBOX]


## Cela permet-il de prendre des décisions ? {#decisioning}

Actuellement, la prise de décision n’utilise pas les données relationnelles des campagnes orchestrées.

## Comment fonctionne le déploiement dans les environnements ? {#deployment}

Les objets créés dans des campagnes orchestrées (audiences, workflows, etc.) sont liés au sandbox dans lequel ils sont créés. Les workflows de package et de déploiement standard dans les environnements (de développement, d’évaluation et de production) ne sont actuellement pas disponibles pour les campagnes orchestrées.

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



>[!MORELIKETHIS]
>
>* [Mécanismes de sécurisation et limitations des campagnes orchestrées](../orchestrated/guardrails.md)
>* [Prise en main des schémas et des jeux de données dans les campagnes orchestrées](../orchestrated/gs-schemas.md)
>* [Créer votre première campagne orchestrée](../orchestrated/gs-campaign-creation.md)
>* Description du produit [Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
