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
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: c2beecbb-b93e-4ae3-baa9-72adcdc06781
  - id: cfba2953-2ce9-4b00-a00c-71cd338ae63f
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 299
ht-degree: 63%

---

# Actions [!DNL Adobe Campaign] v7/v8 {#using_campaign_v7-v8}

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
