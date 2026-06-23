---
solution: Journey Optimizer
product: journey optimizer
title: Actions d’Adobe Campaign v7/v8
description: En savoir plus sur les actions Adobe Campaign v7/v8
feature: Journeys, Actions, Custom Actions
topic: Administration
role: User
level: Intermediate
keywords: parcours, intégration, campaign, v7, v8
exl-id: 3da712e7-0e08-4585-8ca4-b6ff79df0b68
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/Saqu6Kkm1Rdym10IuwLF88Fj-hT2crAwENajyKBeY5w
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: b5d14f7b40933f110ff666db858e976e5de711db
workflow-type: tm+mt
source-wordcount: 761
ht-degree: 24%

---

# Actions [!DNL Adobe Campaign] v7/v8 {#using_campaign_v7-v8}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment utiliser l’intégration Adobe Campaign v7 et v8 pour envoyer des e-mails, des notifications push et des SMS à partir de vos parcours via les messages transactionnels de Campaign.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acc"
>title="Actions personnalisées"
>abstract="Une intégration est disponible si vous disposez d’[!DNL Adobe Campaign] v7 ou v8. Elle permet d’envoyer des e-mails, des notifications push et des SMS à l’aide des fonctionnalités de messagerie transactionnelle d’[!DNL Adobe Campaign]."

Une intégration est disponible si vous disposez d’[!DNL Adobe Campaign] v7 ou v8. Elle permet d’envoyer des e-mails, des notifications push et des SMS à l’aide des fonctionnalités de messagerie transactionnelle d’[!DNL Adobe Campaign].

La connexion entre les instances Journey Optimizer et Campaign est configurée par Adobe au moment de l’approvisionnement. Contactez Adobe.

**Utilisation :** utilisez des actions Campaign v7/v8 lorsque votre messagerie repose sur des modèles transactionnels Campaign, des modèles de données spécifiques à Campaign ou des workflows de diffusion Campaign existants.

**Conditions préalables**

* Votre instance [!DNL Adobe Campaign] v7/v8 est configurée et connectée à Journey Optimizer par Adobe.
* Vous avez accès aux messages transactionnels de Campaign et disposez des autorisations requises.

Pour que cela fonctionne, vous devez configurer une action dédiée. Reportez-vous à cette [section](../action/acc-action.md).

Un cas d&#39;utilisation complet est présenté dans cette [section](../building-journeys/ajo-ac.md).

1. Concevez votre parcours en commençant par un événement. Consultez cette [section](../building-journeys/journey.md).
1. Dans la section **Action** de la palette, sélectionnez une action Campaign et ajoutez-la à votre parcours.
1. Dans les **paramètres d’action**, tous les champs attendus dans la payload du message s’affichent. Vous devez faire correspondre chacun de ces champs avec celui que vous souhaitez utiliser, et ce, depuis l’événement ou la source de données. Cette opération est similaire aux actions personnalisées. Reportez-vous à cette [section](../building-journeys/using-custom-actions.md).

>[!NOTE]
>
>* Les actions de Campaign v7/v8 peuvent être utilisées avec les actions de canal natives dans le même parcours. Cela ne s’applique pas aux actions Campaign Standard. Voir [&#x200B; Mécanismes de sécurisation de l’activité Campaign](../start/guardrails.md#ac-g).
>* Les actions Campaign v7/v8 ne peuvent pas être utilisées avec les activités Lecture d’audience ou Qualification d’audience . Consultez les mécanismes de sécurisation Lecture d’audience et Qualification d’audience dans la page Mécanismes de sécurisation .

![[!DNL Adobe Campaign] paramètres d’intégration et de configuration des actions v7/v8](assets/accintegration2.png)

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page explique comment utiliser Adobe Campaign v7/v8 comme action dans les parcours Journey Optimizer pour envoyer des e-mails, des notifications push et des SMS via les messages transactionnels de Campaign.

**Intentions:**

* Ajouter une action Campaign v7/v8 à un parcours pour envoyer des messages transactionnels
* Mappez les champs d’événement de parcours ou de source de données aux paramètres de payload des messages Campaign.
* Combinez des actions Campaign v7/v8 avec des actions de canal Journey Optimizer natives dans le même parcours
* Configurez l’action dédiée requise pour l’intégration de Campaign v7/v8

**Glossaire:**

* **Messagerie transactionnelle de Campaign** : fonctionnalité d&#39;Adobe Campaign v7/v8 pour envoyer des messages déclenchés (email, SMS, push) via une action dédiée intégrée à Journey Optimizer *(spécifique au produit)*
* **Paramètres d’action** : champs du volet Activité de parcours qui mappent les données de parcours à la *de payload de message Campaign attendue (spécifique au produit)*

**Mécanismes de sécurisation :**

* La connexion entre Journey Optimizer et l’instance Campaign est configurée par Adobe au moment de l’approvisionnement. Contactez Adobe pour l’activer.
* Une action dédiée doit être configurée avant que les actions de Campaign v7/v8 ne soient disponibles dans la palette de parcours.
* Les actions Campaign v7/v8 ne peuvent pas être utilisées avec les activités Lecture d’audience ou Qualification d’audience .
* L&#39;accès aux messages transactionnels de Campaign et les autorisations requises dans Campaign sont des conditions préalables.

**Terminologie:**

* Nom canonique : Adobe Campaign v7/v8 — Acronyme : ACC — variantes : Campaign v7, Campaign v8, Campaign Classic
* Ne les confondez pas : « Actions de Campaign v7/v8 » (peuvent être utilisées avec des actions natives) ≠ « Actions de Campaign Standard » (ne peuvent pas être combinées avec des actions natives dans le même parcours)

**FAQ:**

* **Q : Qui configure la connexion entre Journey Optimizer et Campaign v7/v8 ?** — Adobe configure la connexion au moment de l&#39;approvisionnement ; vous devez contacter Adobe pour la configurer.
* **Q : Les actions de Campaign v7/v8 peuvent-elles être combinées avec les actions de canal Journey Optimizer natives dans le même parcours ?** — Oui, les actions de Campaign v7/v8 peuvent être utilisées avec les actions de canal natives ; ce n’est pas le cas pour les actions de Campaign Standard.
* **Q : Les actions Campaign v7/v8 peuvent-elles être utilisées avec les activités Lecture d’audience ou Qualification d’audience ?** — Non, les actions Campaign v7/v8 ne peuvent pas être utilisées avec les activités Lecture d’audience ou Qualification d’audience.
* **Q : Comment mapper les données de parcours à la payload du message Campaign ?** — Dans le volet Paramètres d&#39;action , mappez chaque champ de payload attendu au champ correspondant de l&#39;événement de parcours ou de la source de données, de la même manière que les actions personnalisées.

+++
