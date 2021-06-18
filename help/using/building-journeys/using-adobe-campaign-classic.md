---
title: Actions d’Adobe Campaign v7/v8
description: En savoir plus sur les actions Adobe Campaign v7/v8
feature: Actions
topic: Administration
role: Administrator
level: Intermediate
source-git-commit: 9ca747c4f46fd7eb24dbbf12350d7bbe409b1617
workflow-type: tm+mt
source-wordcount: '165'
ht-degree: 49%

---

# Actions d’Adobe Campaign v7/v8 {#using_campaign_classic}

Une intégration est disponible si vous disposez d’Adobe Campaign v7 ou v8. Il vous permettra d’envoyer des emails, des notifications push et des SMS à l’aide des fonctionnalités de messagerie transactionnelle Adobe Campaign.

La connexion entre les instances Journey Optimizer et Campaign est configurée par Adobe au moment de la mise en service. Contactez l’Adobe.

Pour que cela fonctionne, vous devez configurer une action dédiée. Reportez-vous à cette [section](../action/acc-action.md).

Un cas pratique de bout en bout est présenté dans cette [section](../building-journeys/campaign-classic-use-case.md).

1. Concevez votre parcours en commençant par un événement. Consultez cette [section](../building-journeys/journey.md).
1. Dans la section **Action** de la palette, sélectionnez une action Campaign et ajoutez-la à votre parcours.
1. Dans les **paramètres d’action**, tous les champs attendus dans la payload du message s’affichent. Vous devez faire correspondre chacun de ces champs avec celui que vous souhaitez utiliser, et ce, depuis l’événement ou la source de données. Cette opération est similaire aux actions personnalisées. Reportez-vous à cette [section](../building-journeys/using-custom-actions.md).

![](../assets/accintegration2.png)
