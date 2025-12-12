---
solution: Journey Optimizer
product: journey optimizer
title: Pris een main de Journey Optimizer pour les responsables marketing
description: En tant qu’utilisateur ou utilisatrice de parcours, découvrez comment utiliser Journey Optimizer.
level: Beginner
feature: Get Started
Role: User
exl-id: 34304142-3ee8-4081-94b9-e914968c75ba
source-git-commit: 5ff7987c00afda3263cb97654967c5b698f726c2
workflow-type: tm+mt
source-wordcount: '1192'
ht-degree: 6%

---

# Prise en main pour les responsables marketing {#get-started-marketers}

En tant que **responsable marketing** ou **utilisateur ou utilisatrice de parcours**, vous êtes responsable de la création des offres et des parcours, ainsi que de la conception du contenu. Vous pouvez commencer à utiliser [!DNL Adobe Journey Optimizer] une fois que l’[administrateur système](administrator.md) et l’[ingénieur de données](data-engineer.md) vous ont accordé l’accès et ont préparé votre environnement.

## Prise en main de l’essentiel

Journey Optimizer vous permet de créer des expériences client connectées et personnalisées par e-mail, SMS, notification push, in-app, web, cartes de contenu, etc. Contactez vos [administrateurs](administrator.md) pour obtenir l’accès et les [ingénieurs de données](data-engineer.md) pour configurer des audiences et des données.

Pour commencer à créer des expériences, procédez comme suit :

1. **Créer des audiences** Créez des audiences par le biais de définitions de segment, chargez des fichiers CSV ou utilisez la composition d’audience. Journey Optimizer offre plusieurs façons de cibler les bons clients. En savoir plus sur les [audiences](../../audience/about-audiences.md) et [la création de définitions de segment](../../audience/creating-a-segment-definition.md).

1. **Conception du contenu**. Créez des messages attrayants sur plusieurs canaux :
   * Utilisez l’**assistant AI** pour générer le contenu, les objets et les images des e-mails en fonction des directives de votre marque. [En savoir plus sur la génération de contenu IA](../../content-management/gs-generative.md)
   * **Personnalisez les messages** avec des données client, du contenu dynamique et une logique conditionnelle. [En savoir plus sur la personnalisation](../../personalization/personalize.md)
   * **Effectuez une itération sur les données contextuelles** pour afficher des listes dynamiques à partir d’événements, d’actions personnalisées et de recherches de jeux de données. [En savoir plus sur l’itération des données contextuelles](../../personalization/iterate-contextual-data.md)
   * Créez des **modèles de contenu** et des **fragments** réutilisables pour maintenir la cohérence de la marque. [Utiliser des modèles](../../content-management/content-templates.md)
   * Gérez les ressources avec l’intégration **Adobe Experience Manager Assets**. [En savoir plus sur les ressources ](../../integrations/assets.md)

   ![](../assets/perso_ee2.png)

1. **Ajouter des offres et une prise de décision**. Proposez la meilleure offre à chaque client au bon moment à l’aide de la prise de décision optimisée par l’IA. Découvrez [Gestion des décisions](../../offers/get-started/starting-offer-decisioning.md) et [Experience Decisioning](../../experience-decisioning/gs-experience-decisioning.md).

   ![](../assets/offers-e2e-offers-displayed.png)

1. **Tester et valider**. Prévisualiser et tester le contenu avant l’envoi :
   * Utilisez des **profils de test** pour prévisualiser la personnalisation et vérifier le rendu sur tous les appareils
   * Tester avec des **exemples de données** provenant de fichiers CSV/JSON
   * Prévisualiser **rendu des e-mails** sur les principaux clients de messagerie
   * Configurer des **workflows de validation** pour les campagnes et les parcours (une licence supplémentaire est requise)

   Découvrez comment [tester et valider des messages](../../content-management/preview-test.md).

1. **Créer des parcours client**. Créez des expériences personnalisées en temps réel à l’aide de la zone de travail de parcours :

   * Déclenchez des parcours avec **événements** (actions client) ou **audiences** (envois par lots).
   * Ajoutez des **conditions** pour créer des chemins personnalisés en fonction des données client
   * Utilisez des **activités d’attente** pour créer un timing parfait entre les messages
   * Envoyer des messages sur **plusieurs canaux** dans un seul parcours
   * Appliquez des tests **A/B** pour optimiser l’efficacité des parcours.
   * Utilisez **recherche de jeu de données** pour enrichir les parcours avec des données en temps réel de Adobe Experience Platform. [En savoir plus sur la recherche de jeux de données](../../building-journeys/dataset-lookup.md)
   * Utilisez des **identifiants supplémentaires** pour permettre au même profil de saisir plusieurs instances de parcours (par exemple, différentes commandes ou réservations). [En savoir plus sur les identifiants supplémentaires](../../building-journeys/supplemental-identifier.md)

   ![](../assets/journey-design.png)

   Découvrez comment [concevoir et exécuter des parcours ](../../building-journeys/journey-gs.md) et explorez des [cas d’utilisation de parcours ](../../building-journeys/jo-use-cases.md). Comprenez [ critères d’entrée/sortie ](../../building-journeys/entry-exit-criteria-guide.md) pour contrôler le flux du profil.

1. **Surveiller et optimiser**. Suivez les performances et améliorez les résultats au fil du temps :
   * Surveillez **parcours en direct** les performances et identifiez les goulots d’étranglement
   * Analyse **diffusion des messages** taux et mesures d’engagement
   * Utilisation de **tableaux de bord de rapports** avec l’intégration de Customer Journey Analytics
   * Suivi **conversion** et de l’impact commercial

   Découvrez comment [ surveiller les performances ](../../reports/report-gs-cja.md).

## Tirer parti des dernières fonctionnalités

Journey Optimizer évolue en permanence avec de nouvelles fonctionnalités pour améliorer votre efficacité marketing :

* **Cartes de contenu** : diffusez des messages persistants et non intrusifs dans les applications mobiles et les sites web, avec lesquels les utilisateurs peuvent interagir à leur guise. Contrairement aux notifications push, les cartes de contenu restent visibles jusqu’à leur rejet. [En savoir plus sur les cartes de contenu ](../../content-card/get-started-content-card.md)

* **Gestion des conflits et hiérarchisation** : contrôlez la fréquence des messages et empêchez la surcommunication avec des règles de limitation avancées. Définissez des scores de priorité pour vous assurer que les messages les plus importants atteignent d’abord les clients. [En savoir plus sur la gestion des conflits ](../../conflict-prioritization/gs-conflict-prioritization.md)

* **Optimisation de l’heure d’envoi optimisée par l’IA** : laissez l’IA prédire l’heure d’envoi optimale pour chaque client en fonction de ses modèles d’engagement historiques, en augmentant les taux d’ouverture et de clic jusqu’à 10 %. [Découvrez l’optimisation de l’heure d’envoi](../../building-journeys/send-time-optimization.md)

* **Expérimentation de bandit manchot** : attribuez automatiquement plus de trafic aux variations gagnantes en temps réel lors des tests, en maximisant les résultats sans attendre la fin du test. [En savoir plus sur l’expérimentation](../../content-management/content-experiment.md)

* **Workflows d’approbation** : implémentez des processus de révision pour les campagnes et les parcours avant leur activation (disponible avec une licence supplémentaire). [En savoir plus sur les validations](../../test-approve/gs-approval.md)

## Bonnes pratiques pour réussir

### Création de contenu

* **Prise en main des modèles** : utilisez des modèles et des fragments de contenu préconfigurés pour accélérer la création et maintenir la cohérence.
* **Tester tôt, tester souvent** : prévisualisez toujours le contenu sur les différents appareils et utilisez des profils de test pour valider la personnalisation
* **Exploiter l’IA à bon escient** : utilisez l’assistant AI pour les brouillons initiaux et les variations, mais examinez et affinez toujours pour la voix de votre marque
* **Restez simple** : des messages clairs et concis avec de forts appels à l’action ont de meilleurs résultats que des mises en page complexes

### Parcours design

* **Définir des objectifs clairs** : établir des mesures de succès avant de créer votre parcours
* **Mapper l’expérience client** : visualiser l’ensemble du parcours avant l’implémentation
* **Utiliser les activités d’attente de manière stratégique** : donnez aux clients le temps d’interagir avant d’envoyer des suivis
* **Planifier les stratégies de sortie** : définir quand et pourquoi les clients doivent quitter le parcours
* **Test en mode brouillon** : validez la logique de parcours avec l’essai avant l’activation.

[Découvrir les bonnes pratiques relatives au parcours](../../building-journeys/entry-exit-criteria-guide.md#best-practices)

### Ciblage des audiences

* **Segmenter de manière réfléchie** : créez des segments ciblés spécifiques et exploitables selon des critères clairs
* **Actualiser régulièrement** : assurez-vous que les audiences restent à jour en définissant des plannings d’évaluation appropriés
* **Taille et précision de l’équilibre** : les audiences cibles sont suffisamment importantes pour avoir une signification statistique, mais suffisamment spécifiques pour être pertinentes
* **Utiliser des attributs d’enrichissement** : utilisez les attributs calculés et les données d’enrichissement pour une personnalisation plus approfondie

### Gestion des fréquences

* **Respecter les préférences du client** : respecter les désinscriptions et les préférences de communication
* **Définir des limites de fréquence** : utilisez des ensembles de règles pour éviter la fatigue des messages sur plusieurs canaux
* **Coordonner des campagnes** : utilisez la gestion des conflits pour vous assurer que les clients reçoivent le message approprié au bon moment.
* **Surveiller l&#39;engagement** : surveiller les signes de fatigue (baisse des taux d&#39;ouverture, augmentation des désabonnements)

[En savoir plus sur le capping de la fréquence](../../conflict-prioritization/channel-capping.md)

## Explorer les cas d’utilisation

Apprenez à partir d’exemples pratiques qui démontrent les fonctionnalités de Journey Optimizer :

**Cas d’utilisation courants :**

* **Série de bienvenue** : intégrez de nouveaux clients avec des parcours personnalisés à plusieurs étapes. [Afficher le cas d’utilisation](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding)
* **Récupération de panier abandonné** : réengagez les clients qui ont laissé des articles dans leur panier. [Afficher le cas d’utilisation](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart)
* **Campagnes de réengagement** : récupérez les clients inactifs avec des offres ciblées. [Afficher le cas d’utilisation](https://experienceleague.adobe.com/fr/docs/experience-platform/rtcdp/use-cases/personalization-insights-engagement/use-cases-luma)
* **Campagnes d’anniversaire** : envoyez des messages d’anniversaire personnalisés avec des offres spéciales
* **Recommandations de produits** : suggérez des produits pertinents en fonction de l’historique de navigation et d’achat
* **Messagerie pilotée par les événements** : répondez aux actions des clients en temps réel

**modèles de Parcours :**

* [Envoyer des messages aux abonnés](../../building-journeys/message-to-subscribers-uc.md) : cibler les listes d’abonnements avec du contenu personnalisé
* [Messagerie multicanal](../../building-journeys/journeys-uc.md) : combinez e-mail et notification push avec des événements de réaction
* [E-mails réservés à la semaine](../../building-journeys/weekday-email-uc.md) : planifier des communications à l’aide de conditions temporelles

Parcourez toute la bibliothèque de cas d’utilisation de [parcours ](../../building-journeys/jo-use-cases.md) pour découvrir d’autres modèles et implémentations.

## Collaborer avec d’autres rôles

Votre travail marketing se connecte à d’autres équipes :

* **Collaboration avec les [ingénieurs de données](data-engineer.md)** : demandez de nouveaux attributs calculés, fournissez des commentaires sur la qualité de l’audience et coordonnez les exigences en matière de données
* **Travailler avec [les développeurs](developer.md)** : alignement sur les déclencheurs d’événement, test des implémentations mobiles et validation du suivi
* **Travailler avec [Administrateurs](administrator.md)** : demander des configurations de canal, signaler les problèmes liés aux autorisations et se coordonner sur l’activation des nouvelles fonctionnalités

## Restez à jour

Suivez les dernières fonctionnalités de Journey Optimizer et de marketing :

* **[Notes de mise à jour](../../rn/release-notes.md)** : consultez les nouvelles fonctionnalités, les mises à jour de canal et les améliorations publiées chaque mois
* **[Mises à jour de la documentation](../../rn/documentation-updates.md)** : suivez les modifications récentes, y compris les nouveaux cas d’utilisation, les bonnes pratiques et la documentation sur les fonctionnalités
* **Notifications de produit** : activez les notifications dans votre profil [Adobe Experience Cloud](https://experience.adobe.com/preferences){target="_blank"} pour recevoir des alertes sur :
   * Nouveaux canaux et fonctionnalités disponibles
   * Lancements de fonctionnalités et programmes bêta à venir
   * Bonnes pratiques et opportunités de formation
   * Annonces importantes affectant vos campagnes

  Pour activer les notifications, cliquez sur l’icône de votre profil en haut à droite de Adobe Experience Cloud, accédez à **Préférences > Notifications**, puis configurez vos préférences de notification Journey Optimizer.

## Étapes suivantes

1. **Commencez petit** : créez un parcours de bienvenue simple ou une campagne à message unique pour apprendre à utiliser la plateforme
2. **Utiliser l’IA** : utilisez l’assistant d’IA pour poser des questions et accélérer la création de contenu
3. **Rejoindre la communauté** : entrez en contact avec d’autres utilisateurs Journey Optimizer de la [communauté Experience League](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer/ct-p/journey-optimizer){target="_blank"}
4. **Explorer les tutoriels** : regardez des vidéos détaillées sur [Experience League](https://experienceleague.adobe.com/docs/journey-optimizer-learn/tutorials/overview.html?lang=fr){target="_blank"}
