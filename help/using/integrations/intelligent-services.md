---
solution: Journey Optimizer
product: journey optimizer
title: Intégration aux services intelligents
description: Découvrez comment tirer parti des services intelligents Adobe et des prédictions de l’IA dédiée aux clients dans Journey Optimizer
feature: Journeys, Integrations
topic: Artificial Intelligence
role: User
level: Intermediate
keywords: artificiel, IA, intelligent, parcours, service
exl-id: 20da09e1-0611-4d27-a589-30552011e06c
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/rTKcWHwfwleQtD68fcdeqYK2AMQHVaknKtsNDFsOldI
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: bbbea26f-9621-49eb-9ab8-e06fb3bbce8c
  - id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377
  - id: eb30f47f-d87a-400f-8f78-63ce7979ff56
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 669
ht-degree: 16%

---

# Intégration aux services intelligents {#ai-overview}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment intégrer les services intelligents Adobe et les prédictions de l’IA dédiée aux clients avec Journey Optimizer afin d’utiliser les scores d’attrition et de conversion comme attributs de profil pour la prise de décision, les actions et la création de segments.

>[!ENDSHADEBOX]

L’intégration à **[!DNL Adobe Intelligent Services]** vous permet de tirer parti de l’intelligence artificielle et du machine learning dans des cas d’utilisation liés à l’expérience client. Elle permet aux analystes marketing de configurer des prédictions adaptées aux besoins spécifiques d’une entreprise à l’aide de configurations métier, sans nécessiter d’expertise en science des données.

[!DNL Intelligent Services], qui repose sur [!DNL Adobe Experience Platform], fournit une IA en tant que service pour les équipes chargées de l’expérience client. Il permet de prédire le comportement des clients, de mesurer l’impact de la campagne et d’améliorer le retour sur investissement. Pour plus d’informations, consultez la [[!DNL Adobe Experience Platform] documentation](https://experienceleague.adobe.com/docs/experience-platform/intelligent-services/home.html?lang=fr){target="_blank"}.

L&#39;intégration entre [!DNL Journey Optimizer] et [!DNL Intelligent Services] vous permet de tirer parti des prédictions de la clientèle.

L’IA dédiée aux clients, un composant de [!DNL Adobe Intelligent Services], prédit les actions probables de la clientèle. Reportez-vous à la [[!DNL Adobe Experience Platform] documentation](https://experienceleague.adobe.com/docs/experience-platform/intelligent-services/customer-ai/overview.html?lang=fr){target="_blank"}.

L’IA dédiée aux clients permet aux marques de créer des scores d’attrition ou à de conversion, basés sur le machine learning. Ces scores sont disponibles en tant qu’attributs de profil dans les profils [!DNL Adobe Experience Platform] (profil client en temps réel).

Par conséquent, ces attributs peuvent être utilisés comme n’importe quel autre attribut de profil dans Journey Optimizer. Utilisez-les dans des conditions pour la prise de décision, les actions ou la création de segments.

![Intégration de l’IA dédiée aux clients et clientes affichant des scores de propension et des prédictions](assets/customer-ai.png)

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

- **TL;DR:** Cette page explique comment Journey Optimizer s’intègre aux services intelligents d’Adobe, en particulier à l’IA dédiée aux clients, pour exploiter les scores de propension basés sur le machine learning en tant qu’attributs de profil dans les parcours.

**Intentions:**
- Comprendre comment Adobe Intelligent Services s’intègre à Journey Optimizer
- Utiliser les scores de propension de Customer AI comme attributs de profil dans des conditions ou des actions de parcours
- Activer les prédictions pilotées par l’IA pour l’attrition ou la conversion sans avoir besoin d’expertise en science des données
- Appliquer des scores de machine learning à la création de segments dans Journey Optimizer

**Glossaire:**
- **Adobe Intelligent Services** : suite de services d’IA/ML reposant sur Adobe Experience Platform qui permet de prédire l’expérience client sans avoir besoin d’expertise en science des données *(spécifique au produit)*
- **IA dédiée aux clients** : composant d’Adobe Intelligent Services qui génère des scores de propension à l’attrition ou à la conversion basés sur le machine learning pour les profils clients *(spécifiques au produit)*
- **Score de propension** : score basé sur le machine learning, qui représente la probabilité qu’un client effectue une action spécifique (par exemple, l’attrition ou la conversion), stocké en tant qu’attribut de profil *(spécifique au produit)*

**Mécanismes de sécurisation :**
- Aucune expertise en science des données n’est requise, mais la configuration au niveau de l’entreprise doit être effectuée par les analystes marketing
- Les scores de l’IA dédiée aux clients doivent d’abord être configurés dans Adobe Experience Platform avant d’être disponibles en tant qu’attributs de profil dans Journey Optimizer

**Terminologie:**
- Nom canonique : Adobe Intelligent Services — Acronyme : none — variantes : Intelligent Services, services d’IA
- Nom canonique : Customer AI — Acronyme : aucun — variantes : scores d’IA dédiée aux clients, scores de propension
- Synonymes : « score de résiliation » = « propension à la résiliation » ; « score de conversion » = « propension à la conversion »
- Ne les confondez pas : « Adobe Intelligent Services » ≠ « AI Assistant » (Intelligent Services est une plateforme ML prédictive ; AI Assistant est une interface de conversation)

**FAQ:**
- **Q : Qu’est-ce que l’IA dédiée aux clients dans le cadre de Journey Optimizer ?** — L’IA dédiée aux clients est un composant des services intelligents d’Adobe qui crée des scores d’attrition ou de conversion basés sur le machine learning, qui deviennent disponibles en tant qu’attributs de profil utilisables dans des conditions, des actions et la création de segments Journey Optimizer.
- **Q : Ai-je besoin de compétences en science des données pour utiliser les services intelligents d’Adobe ?** non, les analystes marketing peuvent configurer des prédictions à l&#39;aide de paramètres au niveau de l&#39;entreprise sans avoir besoin d&#39;expertise en science des données.
- **Q : Où les scores de l’IA dédiée aux clients sont-ils stockés ?** — Ils sont stockés en tant qu&#39;attributs de profil dans le profil client en temps réel de Adobe Experience Platform, ce qui les rend accessibles comme tout autre attribut de profil dans Journey Optimizer.
- **Q : Comment utiliser les scores de l’IA dédiée aux clients dans un parcours ?** — Une fois disponibles en tant qu’attributs de profil, les scores peuvent être utilisés dans des conditions pour la prise de décision, dans des configurations d’action ou pour créer des segments d’audience.

+++
