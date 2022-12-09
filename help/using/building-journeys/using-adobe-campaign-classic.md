---
solution: Journey Optimizer
product: journey optimizer
title: Actions Adobe Campaign v7/v8
description: En savoir plus sur les actions Adobe Campaign v7/v8
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 3da712e7-0e08-4585-8ca4-b6ff79df0b68
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '163'
ht-degree: 0%

---

# Actions Adobe Campaign v7/v8 {#using_campaign_classic}

Une intégration est disponible si vous disposez d&#39;Adobe Campaign v7 ou v8. Il vous permettra d’envoyer des emails, des notifications push et des SMS à l’aide des fonctionnalités des messages transactionnels d’Adobe Campaign.

La connexion entre les instances Journey Optimizer et Campaign est configurée par Adobe au moment de la mise en service. Contactez Adobe.

Pour que cela fonctionne, vous devez configurer une action dédiée. Consultez cette section [section](../action/acc-action.md).

Ce cas pratique de bout en bout est présenté dans la section [section](../building-journeys/ajo-ac.md).

1. Concevez votre parcours, en commençant par un événement. Voir [section](../building-journeys/journey.md).
1. Dans le **Action** dans la palette, sélectionnez une action Campaign et ajoutez-la à votre parcours.
1. Dans le **Paramètres d’action**, tous les champs attendus dans la payload du message s’affichent. Vous devez associer chacun de ces champs au champ que vous souhaitez utiliser, depuis l’événement ou la source de données. Cela est similaire aux actions personnalisées. Consultez cette section [section](../building-journeys/using-custom-actions.md).

![](assets/accintegration2.png)
