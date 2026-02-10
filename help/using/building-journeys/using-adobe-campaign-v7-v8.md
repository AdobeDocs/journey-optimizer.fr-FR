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
source-git-commit: 339285cbc82d5b30b221feb235ed8425a66f8802
workflow-type: tm+mt
source-wordcount: '296'
ht-degree: 46%

---

# Actions [!DNL Adobe Campaign] v7/v8 {#using_campaign_v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom_acc"
>title="Actions personnalisées"
>abstract="Une intégration est disponible si vous disposez de [!DNL Adobe Campaign] v7 ou v8. Il vous permet d’envoyer des e-mails, des notifications push et des SMS à l’aide des fonctionnalités de messagerie transactionnelle [!DNL Adobe Campaign]."

Une intégration est disponible si vous disposez de [!DNL Adobe Campaign] v7 ou v8. Il vous permet d’envoyer des e-mails, des notifications push et des SMS à l’aide des fonctionnalités de messagerie transactionnelle [!DNL Adobe Campaign].

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
>* Les actions de Campaign v7/v8 peuvent être utilisées avec les actions de canal natives dans le même parcours. Cela ne s’applique pas aux actions Campaign Standard. Voir [ Mécanismes de sécurisation de l’activité Campaign](../start/guardrails.md#ac-g).
>* Les actions Campaign v7/v8 ne peuvent pas être utilisées avec les activités Lecture d’audience ou Qualification d’audience . Consultez les mécanismes de sécurisation Lecture d’audience et Qualification d’audience dans la page Mécanismes de sécurisation .

![[!DNL Adobe Campaign] paramètres d’intégration et de configuration des actions v7/v8](assets/accintegration2.png)
