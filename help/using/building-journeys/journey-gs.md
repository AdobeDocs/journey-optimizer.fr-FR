---
solution: Journey Optimizer
product: journey optimizer
title: Créer votre premier parcours
description: Étapes clés de création de votre premier parcours avec  [!DNL Adobe Journey Optimizer]
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: parcours, premier, commencer, démarrage rapide, audience, événement, action
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/7zNDOi2SUTyttgR6I1iOYQb61ejxpqLYznweU8alnPw
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: b15c7c2e-788c-4eb7-86a8-390565b0d2c9
  - id: a6c67b0d-bd3e-4d5d-95a8-882e3709d632
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: aa2f3246-cb95-4b30-8899-fdf7d73550cc
  - id: b5520579-b31f-4df7-9281-f0d9f91e2edc
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: d00e9f03-e50b-4162-b143-0c0817c937c2
  - id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 2097
ht-degree: 30%

---

# Créer votre premier parcours {#jo-quick-start}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez les principales étapes de création de votre premier parcours dans Adobe Journey Optimizer, depuis la définition de l’audience ou de l’événement d’entrée jusqu’à l’ajout d’actions et sa publication en direct.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="Créer des parcours"
>abstract="**[!DNL Adobe Journey Optimizer]** crée des cas d’utilisation d’orchestration en temps réel à l’aide de données contextuelles stockées dans des événements ou des sources de données."

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Parcours"
>abstract="Les parcours clients offrent des expériences contextuelles personnalisées. Journey Optimizer vous permet de créer des cas d’utilisation d’orchestration en temps réel avec des données contextuelles stockées dans des événements ou des sources de données. L’onglet **Vue d’ensemble** affiche un tableau de bord avec les mesures clés liées à vos parcours : L’onglet **Parcourir** affiche la liste des parcours existants."

[!DNL Adobe Journey Optimizer] comprend une zone de travail d’orchestration omnicanal qui permet aux marketeurs d’harmoniser la portée marketing avec l’engagement client individuel. L’interface utilisateur vous permet de faire glisser facilement des activités de la palette vers la zone de travail pour créer votre parcours. L’interface d’utilisation du parcours est présentée sur [cette page](journey-ui.md).

![exemple de zone de travail de parcours](assets/journey38.png)

Les étapes principales de la création d’un parcours sont détaillées sur cette page. Les voici :

![étapes de création de parcours : création, conception, test et publication](assets/journey-creation-process.png)

Dans ce guide, vous allez :

* Définir un point d’entrée de parcours : un segment d’audience ou un événement en temps réel
* Ajoutez des actions de message sur plusieurs canaux (e-mail, notification push, SMS, in-app, web, expérience basée sur le code, carte de contenu, etc.). [Voir canaux pris en charge](journey-action.md)
* Tester votre parcours avec des profils de test avant l’activation
* Publiez votre parcours et surveillez ses performances

Créez des parcours clients à plusieurs étapes pour démarrer une séquence d’interactions, d’offres et de messages sur plusieurs canaux en temps réel. Cette approche garantit que les clientes et clients interagissent aux moments optimaux en fonction de leurs actions et des signaux commerciaux pertinents.

<!--
>[!TIP]
>
>Not sure whether to use a journey or a campaign? [Learn how to choose the right approach](../start/journeys-vs-campaigns.md).
-->

## Avant de commencer {#prerequisites}

Ce que vous devez configurer avant de créer dépend de la manière dont votre parcours est déclenché. La plupart des parcours partent de l’un de ces deux points d’entrée :

* **Entrée basée sur l’audience** — Le parcours s’exécute pour un ensemble défini de profils à une heure planifiée. [Créez une audience](../audience/about-audiences.md) dans Adobe Experience Platform avant de créer votre parcours. Il s’agit du point de départ recommandé si vous découvrez Journey Optimizer.

* **Entrée basée sur un événement** — Le parcours est déclenché en temps réel lorsqu&#39;une personne effectue une action, comme un achat ou une inscription. [Configurer un événement](../event/about-events.md) pour définir le déclencheur et les données qu’il transporte.

**Vous ne savez pas quel point d’entrée utiliser ?** Le tableau ci-dessous met en correspondance les cas d’utilisation les plus courants avec l’activité de départ appropriée.

| Point d&#39;entrée | À utiliser lorsque... | Entrées de profils |
|---|---|---|
| **[Lecture d’audience](read-audience.md)** | Vous souhaitez envoyer un message planifié ou récurrent à un ensemble défini de profils (newsletters, promotions, séries d’intégration). | Tous les profils d’une audience par lots, à la fois ou selon un planning. |
| **[Qualification d’audience](audience-qualification-events.md)** | Vous devez réagir en temps réel lorsqu’un profil entre ou quitte une audience (mise à niveau du niveau de fidélité, indicateur de risque d’attrition). | Un profil à la fois, dès qu’ils remplissent les critères d’une audience de diffusion en continu. |
| **Événement unitaire** | Une action de profil déclenche une réponse immédiate (confirmation d’achat, envoi de formulaire, connexion à l’application). | Profil par profil, en temps réel. |
| **[Événement métier](../event/about-creating-business.md)** | Un événement sans profil affecte plusieurs personnes à la fois (annulation de vol, réapprovisionnement des stocks, alerte de dernière minute). | Tous les profils associés à l’événement, via une étape automatique Lecture d’audience . |

Les éléments suivants sont facultatifs, mais peuvent être requis selon votre cas d’utilisation :

* **Source de données** — Pour enrichir les conditions du parcours ou la personnalisation avec des données provenant d&#39;un système externe, configurez une [source de données](../datasource/about-data-sources.md).

* **Action personnalisée** — Si vous diffusez des messages par l&#39;intermédiaire d&#39;un système tiers plutôt que par les canaux intégrés, configurez une [action personnalisée](../action/action.md).

>[!NOTE]
>
>* Si vous êtes un ingénieur de données responsable de la configuration technique (événements, sources de données et actions), consultez [cette section](../configuration/about-data-sources-events-actions.md).
>
>* Les mécanismes de sécurisation et limitations du parcours sont détaillés sur [cette page](../start/guardrails.md).

## Créer un parcours {#jo-build}

Pour créer un parcours à plusieurs étapes, procédez comme suit :

1. Dans la section du menu GESTION DES PARCOURS, cliquez sur **[!UICONTROL Parcours]**.

1. Cliquez sur le bouton **[!UICONTROL Créer un parcours]** pour créer un parcours.

1. Modifiez le volet de configuration du parcours pour définir le nom du parcours et ses propriétés. Découvrez comment définir les propriétés de votre parcours sur [cette page](journey-properties.md).

   >[!TIP]
   >
   >**Quel type de parcours dois-je choisir ?** Si vous découvrez Journey Optimizer, commencez avec un parcours basé sur les audiences à l’aide d’une activité **[!UICONTROL Lecture d’audience]**. Il ne nécessite aucune configuration d’événement préalable et est le moyen le plus simple de vous familiariser avec la zone de travail. Pour les expériences déclenchées par un événement en temps réel (par exemple, en réaction à un achat ou à un envoi de formulaire), configurez d’abord un événement et utilisez une entrée basée sur un événement. Prêt à aller plus loin ? [Découvrez tous les types de parcours et leurs règles d’entrée](entry-management.md#types-of-journeys).

   ![Panneau des propriétés du parcours avec les paramètres et les options de configuration](assets/jo-properties.png)

Vous pouvez ensuite commencer à concevoir votre parcours.

## Concevoir le parcours {#jo-design}

Le concepteur de parcours vous permet de créer des parcours à plusieurs étapes à l’aide d’une interface intuitive par glisser-déposer. Les activités de la palette de gauche sont organisées en trois catégories : **Événements**, **Orchestration** et **Actions**. Pour une présentation complète de la zone de travail et de ses commandes, reportez-vous à [cette page](using-the-journey-designer.md).

![Interface du concepteur de parcours avec la palette d’activités et la zone de travail](assets/journey38.png)

Pour concevoir votre parcours, procédez comme suit :

1. **Ajouter un point d’entrée** — Faites glisser un événement ou une activité **[!UICONTROL Lecture d’audience]** de la palette vers la zone de travail. Cela définit la manière dont les profils rejoignent le parcours : individuellement en temps réel (en fonction de l’événement) ou tous en même temps à partir d’une audience définie (en fonction de l’audience).

   ![Configuration de l’activité Lecture d’audience pour sélectionner une audience cible](assets/read-segment.png)

1. **Ajouter des actions de message** — Dans la section **[!UICONTROL Actions]** de la palette, faites glisser une action de canal sur la zone de travail pour envoyer des messages aux profils qui traversent le parcours. Les actions sont disponibles pour les e-mails, les notifications push, les SMS, etc.

1. **Ajouter des activités d’orchestration** — Utilisez une activité **[!UICONTROL Condition]** pour diviser le parcours en plusieurs chemins d’accès en fonction des attributs de profil ou du comportement. Utilisez une activité **[!UICONTROL Attente]** pour introduire un délai entre les étapes.

>[!TIP]
>
>Pour les parcours comportant plusieurs phases ou plusieurs points de contact, pensez à diviser le flux de bout en bout en sous-parcours plus petits liés à l’activité **[!UICONTROL Saut]**. Cela réduit la complexité et facilite le test indépendant de chaque sous-parcours. En savoir plus dans [Stratégie de conception : sous-parcours de petite taille](jump.md#jump-strategy).

## Tester le parcours {#jo-test}

Une fois que vous avez créé votre parcours, testez-le avant de le publier. Journey Optimizer propose un **mode de test** pour afficher les profils de test au fur et à mesure de leur progression dans le parcours et ainsi détecter les erreurs potentielles avant l’activation. L’exécution de tests rapides vous permet de vérifier que les parcours fonctionnent correctement afin de pouvoir les publier en toute confiance. Découvrez comment tester votre parcours dans [cette section](testing-the-journey.md).

Vous pouvez également exécuter votre parcours en mode **test à blanc**. Le test à blanc de parcours est un mode de publication de parcours spécial dans Adobe Journey Optimizer qui permet aux concepteurs et conceptrices de tester un parcours à l’aide de données de production réelles sans contacter les clients et clientes ni mettre à jour les informations de profil. Cette fonctionnalité permet aux concepteurs et conceptrices de parcours d’avoir confiance dans leur conception de parcours et leur ciblage d’audience avant de publier un parcours en ligne. Découvrez comment publier un parcours en mode Test à blanc dans [cette section](journey-dry-run.md).

## Publiez le parcours. {#jo-pub}

Vous devez publier un parcours pour l’activer et le rendre disponible pour que de nouveaux profils puissent le rejoindre. Avant de publier votre parcours, vérifiez qu’il est valide et qu’il ne comporte aucune erreur. Vous ne pouvez pas publier un parcours comportant des erreurs. En savoir plus sur la publication des parcours dans cette [section](publish-journey.md).

![Flux de parcours complet avec l’audience, les conditions et les actions](assets/jo-journeyuc2_32bis.png)

Une fois publié, vous pouvez surveiller votre parcours à l’aide des outils de rapports dédiés afin de mesurer l’efficacité de votre parcours.

![Rapport d’analyse du parcours montrant les mesures et statistiques de performance](assets/jo-dynamic_report_journey_12.png)

En savoir plus sur les rapports de parcours dans [cette section](../reports/live-report.md).

## Cas d’utilisation courants {#use-cases}

Vous ne savez pas par où commencer ? Voici trois scénarios typiques dans lesquels les parcours offrent la plus grande valeur :

<table style="table-layout:fixed">
  <tr style="border: 0;">
    <td>
      <a href="https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding" target="_blank">
        <img src="../assets/do-not-localize/icon-quick-start.svg" width="35px">
      </a>
      <div><strong>Série de bienvenue</strong><br/>Intégrez automatiquement les nouveaux utilisateurs avec une séquence de messages après leur inscription, les guidant tout au long de votre produit ou service.</div>
    </td>
    <td>
      <a href="https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart" target="_blank">
        <img src="../assets/do-not-localize/icon-campaign.svg" width="35px">
      </a>
      <div><strong>Abandon de panier</strong><br/>Réengagez les clients qui ont quitté le produit sans effectuer d’achat en envoyant un rappel opportun avec du contenu personnalisé.</div>
    </td>
    <td>
      <a href="jo-use-cases.md">
        <img src="../assets/do-not-localize/icon-content.svg" width="35px">
      </a>
      <div><strong>Réengagement</strong><br/>Récupérez les utilisateurs inactifs avec des offres ou des mises à jour ciblées en fonction de leur dernier comportement connu.</div>
    </td>
  </tr>
  <tr style="border: 0;">
    <td align="center"><a href="https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/use-cases/customer-onboarding" target="_blank"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/use-cases/abandoned-cart" target="_blank"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
    <td align="center"><a href="jo-use-cases.md"><img src="../assets/do-not-localize/learn-more-button.svg"></a></td>
  </tr>
</table>

## Ressources supplémentaires

* **[types de Parcours et entrée de profil](entry-management.md)** - Comprenez tous les types de parcours (événement unitaire, événement métier, lecture d’audience, qualification de l’audience) et la manière dont les profils entrent, rentrent à nouveau et circulent dans les parcours.
* **[Présentation du concepteur de parcours](using-the-journey-designer.md)** : maîtrisez l’interface de zone de travail du parcours pour concevoir et orchestrer des parcours client.
* **[Activités de parcours](about-journey-activities.md)** : découvrez toutes les activités disponibles, y compris les événements, les actions et les composants d’orchestration.
* **[Test des parcours](testing-the-journey.md)** : découvrez comment tester vos parcours à l’aide du mode test avant de les publier en production.
* **[Publication de parcours](publish-journey.md)** : découvrez le processus de publication des parcours et comment gérer les parcours en direct.
* **[Rapports de parcours](report-journey.md)** : suivez et analysez les performances du parcours avec des mesures et des informations détaillées.
* **[Dépannage des parcours](troubleshooting.md)** : trouvez des solutions aux problèmes courants du parcours et consultez les bonnes pratiques de débogage.
* **[Tutoriels sur les parcours](https://experienceleague.adobe.com/fr/docs/journey-optimizer-learn/tutorials/journeys/introduction-to-building-a-journey){target="_blank"}** : consultez des tutoriels vidéo détaillés sur la création de parcours et les bonnes pratiques.

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page décrit les quatre étapes clés de la création d’un premier parcours dans Adobe Journey Optimizer (définition d’un point d’entrée, conception de la zone de travail, test en mode test ou Exécution d’essai et publication), ainsi que des conseils sur le choix du type d’entrée approprié.

**Intentions:**
* Créez un parcours et configurez ses propriétés dans le menu Gestion des Parcours .
* Choisissez le point d’entrée correct (Lecture d’audience, Qualification d’audience, événement unitaire ou événement métier) pour un cas d’utilisation donné
* Créez un parcours à plusieurs étapes en faisant glisser et en déposant des événements, des activités d’orchestration et des actions de canal sur la zone de travail
* Tester un parcours en mode Test avec des profils de test synthétiques avant la publication
* Exécutez une Exécution d’essai pour valider le ciblage des audiences avec des données de production réelles sans contacter les clients.
* Publiez un parcours pour le rendre actif et surveiller ses performances à l’aide d’outils de création de rapports

**Glossaire:**
* **Lecture d’audience** : activité d’entrée qui traite tous les profils d’une audience par lots à la fois ou selon un *planifié (spécifique au produit)*
* **Qualification d’audience** : activité d’entrée déclenchée en temps réel lorsqu’un profil entre ou sort d’un *d’audience de diffusion en continu (spécifique à un produit)*
* **Événement unitaire** : déclencheur en temps réel qui entre un profil à la fois dans un parcours lorsqu’une action spécifique se produit *(spécifique au produit)*
* **Événement métier** : événement sans profil (par exemple, annulation de vol, réapprovisionnement de stock) qui déclenche un parcours pour plusieurs profils simultanément via une étape automatique Lecture d’audience *(spécifique au produit)*
* **Mode test** : mode de validation qui utilise des profils de test synthétiques pour simuler l’exécution du parcours sans activer les *de communication en direct (spécifiques au produit)*
* **Exécution d’essai** : mode de publication spécial qui utilise des données de production réelles pour valider la logique de parcours sans contacter les clients réels ou mettre à jour les profils *(spécifiques au produit)*

**Mécanismes de sécurisation :**
* Un parcours ne peut pas être publié s’il contient des erreurs ; toutes les erreurs doivent d’abord être résolues
* La configuration de l’événement (pour l’entrée basée sur un événement) doit être effectuée par un ingénieur de données avant que le parcours ne puisse être créé
* Les mécanismes de sécurisation et limitations du parcours sont documentés séparément et doivent être examinés avant la conception à grande échelle
* La création d’audiences dans Adobe Experience Platform est une condition préalable aux parcours basés sur les audiences

**Terminologie:**
* Nom canonique : Parcours — Acronyme : none — variantes : parcours client, flux d’orchestration
* Synonymes : « Mode test » = « Test de parcours » ; « Exécution d’essai » = « Mode Exécution d’essai »
* Ne les confondez pas : « Mode test » ≠ « Exécution d’essai » - Le mode test utilise des profils synthétiques ; l’exécution d’essai utilise des données de production réelles sans contacter les clients.

**FAQ:**
* **Q : Quelle est la première chose que je dois faire avant de créer un parcours déclenché par un événement ?** — Configurez l&#39;événement avec un ingénieur de données pour définir le déclencheur et les données qu&#39;il transporte ; référencez ensuite l&#39;événement comme point d&#39;entrée du parcours.
* **Q : Quel point d’entrée est recommandé pour une personne qui découvre Journey Optimizer ?** — Commencez par un parcours basé sur une audience à l’aide d’une activité Lecture d’audience : il ne nécessite aucune configuration d’événement préalable et est le moyen le plus simple de se familiariser avec la zone de travail.
* **Q : Puis-je tester mon parcours avant qu’il ne soit mis en ligne ?** — Oui ; utilisez le mode Test avec des profils de test synthétiques pour parcourir le parcours, ou utilisez l’exécution d’essai pour exécuter des données de production réelles sans envoyer de communications.
* **Q : Que se passe-t-il si mon parcours comporte des erreurs lorsque j’essaie de publier ?** — Vous ne pouvez pas publier un parcours comportant des erreurs ; toutes les erreurs de configuration doivent être résolues avant la publication.
* **Q : Comment puis-je diviser un parcours complexe avec de nombreuses étapes ?** utilisez l&#39;activité Saut pour connecter des sous-parcours plus petits, ce qui réduit la complexité et facilite les tests indépendants de chaque sous-parcours.

+++
