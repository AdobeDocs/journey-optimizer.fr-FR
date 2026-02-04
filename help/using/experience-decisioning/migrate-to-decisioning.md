---
title: Avantages de la migration vers Decisioning
description: Découvrez les avantages de la migration de la gestion des décisions vers la prise de décision
feature: Decisioning
topic: Integrations
role: User
level: Experienced
source-git-commit: d336684656c75af682a72b0acab071df15a79004
workflow-type: tm+mt
source-wordcount: '1243'
ht-degree: 3%

---

# Avantages de la migration vers Decisioning {#migrate-to-decisioning}

## Qu’est-ce que Decisioning ? {#what-is-decisioning}

La prise de décision Journey Optimizer est une extension de la fonctionnalité de prise de décision qui jette les bases de la prise de décision sur d’autres objets (tels que des parcours) à l’avenir. Cette nouvelle fonctionnalité unifie les concepts clés des workflows pour rationaliser la création et la gestion, introduit l’expérimentation dans la prise de décision et déplace les éléments de prise de décision vers une approche basée sur un schéma pour le rendu dynamique des éléments.

La structure de prise de décision de nouvelle génération et l’ensemble des fonctionnalités de Adobe Journey Optimizer permettent aux marques d’utiliser les données disponibles, l’intelligence et le contexte d’un client afin de déterminer la meilleure expérience pour chaque client et d’optimiser la valeur commerciale. [En savoir plus](gs-experience-decisioning.md)

## Pourquoi migrer vers Decisioning ? {#why-migrate}

Decisioning offre des fonctionnalités et des avantages significatifs par rapport à l’ancien cadre de gestion des décisions :

### Fonctionnalités d’IA et de machine learning

* **Mesures personnalisées** : possibilité d’utiliser des mesures d’optimisation personnalisées pour les modèles d’IA. Cela permet une interopérabilité des rapports avec [Customer Journey Analytics](https://experienceleague.adobe.com/en/docs/analytics-platform/using/cja-overview/cja-overview){target="_blank"}, normalise les rapports sur les deux plateformes et améliore la cohérence et la fiabilité des données. L’intégration transparente offre une vue plus claire des mesures de performances et ajoute de nouvelles fonctionnalités telles que la création de mesures simples, la publication d’audiences, la pose de questions ad hoc à l’aide d’Insight Builder et la planification de rapports.

* **Mesure de l’effet élévateur** : capacité à visualiser le trafic d’exploration et d’exploitation dans les modèles d’IA. Cela permet aux spécialistes du marketing et aux spécialistes des données de quantifier la manière dont l’exploration de l’IA améliore les performances du modèle à long terme et la découvrabilité de nouvelles offres gagnantes. La transparence dans l’affectation du trafic renforce la confiance dans les décisions de l’IA et permet aux équipes d’optimiser l’apprentissage et les performances au fil du temps. [En savoir plus](ranking/auto-optimization-model.md#lift)

* **Créateur de formules d’IA** : possibilité d’appliquer les sorties de score du modèle d’IA aux fonctionnalités de formule existantes. Cela permet aux professionnels du marketing de combiner facilement les sorties d’IA avec des règles et des poids déterministes pour des stratégies d’optimisation plus nuancées, ce qui accroît le contrôle et la flexibilité tout en tirant parti de l’intelligence du machine learning. [En savoir plus](ranking/ranking-formulas.md)

### Expérimentation

Possibilité d’expérimenter sur les offres, les aspects d’une offre donnée et/ou les méthodes de classement. Cela permet aux professionnels du marketing d’exécuter des expériences contrôlées sur la logique de création, d’éligibilité et de classement afin d’identifier les variantes à hautes performances, d’accélérer les cycles d’apprentissage et d’optimiser en continu le système de prise de décision.

### Amélioration des rapports

Tableau de bord documentant les performances des éléments de décision et des stratégies de sélection par rapport aux éléments clés du funnel d’engagement. Un tableau de bord de prise de décision intuitif et prêt à l’emploi montre rapidement la valeur des performances des campagnes et des parcours pour les KPI clés dans la diffusion d’offres et de contenu, l’engagement d’affichage et de clic, les taux d’utilisation de secours et l’effet élévateur à partir de l’IA et des modèles de classement de machine learning. [En savoir plus](cja-reporting.md)

### Efficacité opérationnelle

* **Copie de sandbox** : possibilité de copier des objets entre des sandbox (par exemple, de développement à production). Cela simplifie le déploiement et les workflows de test en permettant une migration transparente de la logique de décision, des offres et des objets de configuration entre les environnements, ce qui réduit le temps de configuration et réduit les erreurs humaines. [En savoir plus](../configuration/copy-objects-to-sandbox.md)

* **Gestion de catalogue d’éléments basée sur un schéma** : possibilité de définir et de gérer des éléments de décision directement dans des jeux de données liés à un schéma, ce qui permet des mises à jour dynamiques et une gouvernance simplifiée. Cela simplifie la gestion des catalogues en synchronisant les éléments de décision avec les sources de données sous-jacentes, en assurant la précision du contenu, en permettant des mises à jour plus rapides et en prenant en charge la gouvernance à grande échelle. [En savoir plus](items.md)

* **Prise de décision indépendante de l’emplacement** : possibilité de rendre la logique de décision réutilisable dans tous les emplacements/emplacements, en découplant la sélection de décision de la diffusion. Cela favorise la réutilisation et l’efficacité en permettant à un modèle de décision unique d’alimenter plusieurs emplacements ou surfaces (par exemple, web, application, e-mail), en centralisant la logique et en accélérant les efforts de personnalisation cross-canal. [En savoir plus](placements.md)

* **Fragments de contenu réutilisables** : possibilité de définir des blocs de contenu JSON ou HTML (par exemple, titres, en-têtes, pieds de page, CTA) une seule fois et de les référencer dans plusieurs objets d’offre. Cela simplifie la création et la gouvernance de contenu en permettant aux composants partagés d’être gérés de manière centralisée et automatiquement mis à jour entre les offres. [En savoir plus](../content-management/fragments.md)

### Fonctionnalités à venir

* **Prise de décision du canal** : possibilité d’utiliser la logique de décision pour déterminer le meilleur canal pour l’engagement (par exemple, e-mail vs push vs web), plutôt que simplement la meilleure offre au sein d’un seul canal. Cela améliore l’expérience client en optimisant l’endroit où un message est diffusé, et pas seulement ce qui est diffusé.

* **Optimisation des messages** : possibilité d’utiliser l’IA ou des approches basées sur des règles pour optimiser le contenu des messages pour chaque profil, ce qui améliore les résultats d’engagement et de conversion. Cela permet aux spécialistes marketing de personnaliser dynamiquement le ton, l’imagerie et la mise en page en fonction des attributs d’audience et des données de performances.

* **Optimisation du chemin de Parcours** : possibilité de déterminer le chemin de parcours qu’un profil doit suivre, en fonction des résultats expérimentaux, du contexte en temps réel, des règles et/ou de la propension à la conversion. Cela permet aux équipes d’acheminer intelligemment les profils par le biais de la branche de parcours optimale, en assurant la cadence et le contenu appropriés pour chaque utilisateur.

* **Prise de décision de Parcours** : possibilité d’arbitrer entre plusieurs parcours lorsqu’un profil est admissible pour plusieurs profils, en s’assurant que le parcours le plus utile ou le plus pertinent est sélectionné. Cela évite les conflits de messages et la surmessagerie en classant et en sélectionnant le parcours ayant la priorité la plus élevée pour chaque profil.

### Fonctionnalités supplémentaires

* **Application des politiques** : autonomisation des utilisateurs professionnels pour l’utilisation de fonctionnalités telles que [Data Usage Labeling &amp; Enforcement (DULE)](https://experienceleague.adobe.com/fr/docs/experience-platform/data-governance/labels/overview){target="_blank"} et [Consentement](../action/consent.md) dans la prise de décision, ce qui permet d’activer la protection de Privacy Shield dans l’ensemble du workflow de prise de décision. Cela garantit que les décisions respectent automatiquement les politiques d’utilisation des données et les préférences de consentement du client.

* **Prise en charge native des canaux de messagerie** : messagerie et prise de décision intégrées dans un cadre unique sur plusieurs canaux ([Expérience basée sur le code](../code-based/get-started-code-based.md) et [E-mail](../email/get-started-email.md) actuellement disponibles, d’autres canaux seront disponibles au cours du premier semestre 2026). La prise en charge intuitive de l’interface utilisateur permet aux utilisateurs et utilisatrices d’insérer des composants de prise de décision directement dans les workflows de création de messages.

* **Recherche de jeu de données Experience Platform** : possibilité de charger et de référencer des [jeux de données Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/catalog/datasets/overview){target="_blank"} directement dans les règles de sélection d’offres, le classement et le contenu d’offre personnalisé. Vous bénéficiez ainsi d’une plus grande flexibilité en matière de personnalisation et de ciblage en permettant à la logique de décision d’utiliser des sources de données externes dynamiques. [En savoir plus](../data/lookup-aep-data.md)

* **Évolutivité et performances** : amélioration de l’architecture qui déplace le calcul de décision du hub vers la périphérie, réduisant considérablement la latence et améliorant le débit pour les cas d’utilisation à trafic élevé.

## Exemples de cas d’utilisation {#use-cases}

| Exemple d’utilisation | Gestion des décisions | Prise de décision |
|----------|---------------------|-------------|
| **Stratégie multi-emplacement** | Logique de décision liée à un emplacement spécifique (emplacement web ou e-mail, par exemple) | Une seule stratégie alimente la page d’accueil et l’application mobile |
| **Attributs d’offre cohérents** | Chaque offre gère manuellement ses propres attributs ; aucune cohérence au niveau du schéma | Un marketeur définit « discountType » et « offerValue » une seule fois ; chaque offre hérite automatiquement de ces champs |
| **Classement IA dynamique** | Les classements reposent uniquement sur la sortie du modèle ou les règles statiques | Un spécialiste marketing peut ajuster la pondération (par exemple, 60 % de score de conversion de l’IA + 40 % de marge bénéficiaire) pour équilibrer les objectifs de chiffre d’affaires et d’engagement |
| **Stratégies de test A/B** | Aucune prise en charge d’expérimentation intégrée | Une équipe peut tester A/B si « AI + règles métier » surpasse le « classement par priorité » |
| **Mesures IA personnalisées** | Optimise uniquement en fonction de la propension aux clics ; aucune visibilité sur l’exploration ou l’effet élévateur des modèles | Retailer entraîne un modèle de « probabilité d’achat » et surveille l’effet élévateur sur les produits nouveaux par rapport aux produits connus |
| **Réutilisation du contenu** | Chaque offre stocke le contenu complet indépendamment | La mise à jour d’un en-tête ou de CTA se propage automatiquement à des centaines d’offres |
| **Création intégrée** | Les prises de décision et la messagerie sont intégrées dans des structures distinctes avec une intégration limitée | Un marketeur insère des offres personnalisées dans un email sans quitter l&#39;éditeur de messages |
| **Respect de la confidentialité** | Nécessite une coordination manuelle avec les équipes d’ingénierie et de données pour l’application | Un spécialiste marketing crée une règle d’offre en sachant que les préférences de consentement excluent automatiquement certains profils |
| **Inventaire en temps réel** | Données statiques ; flexibilité limitée pour utiliser des jeux de données externes ou contextuels | Utilisez un jeu de données d’inventaire de produits pour supprimer en temps réel les offres pour les articles en rupture de stock |
| **Mise à l’échelle des performances** | Décisions prises dans le hub avec une latence plus élevée | Personnalisation en temps réel de millions de requêtes entrantes avec un temps de réponse inférieur à 100 ms |

## Outils de migration {#migration-tooling}

Un ensemble complet d’**API d’outils de migration** est disponible pour migrer les entités de gestion des décisions vers la prise de décision. Ces API permettent une migration transparente entre les sandbox avec des fonctionnalités automatisées de résolution des dépendances et de restauration.

Les API d’outils de migration vous permettent d’effectuer les opérations suivantes :

* **Analyser les dépendances** entre les sandbox source et cible
* **Migration à différentes portées** - sandbox, offre ou niveau de décision
* **Migrations de restauration** si des problèmes sont détectés

Pour consulter la documentation complète sur les API, y compris l’authentification, les points d’entrée, les exemples de requête/réponse et les workflows détaillés, consultez [cette page](decisioning-migration-api.md).

## Rubriques connexes {#related-topics}

* [Commencer avec la prise de décisions](gs-experience-decisioning.md)
* [Mécanismes de sécurisation et limitations des décisions](decisioning-guardrails.md)
* [FAQ sur Decisioning](decisioning-faq.md)

