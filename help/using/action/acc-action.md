---
solution: Journey Optimizer
product: journey optimizer
title: Intégration à Adobe Campaign v7/v8
description: Découvrez comment intégrer avec Adobe Campaign v7/v8
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '494'
ht-degree: 0%

---

# Intégration à Adobe Campaign v7/v8 {#integrating-with-adobe-campaign-classic}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Actions Adobe Campaign v7/v8"
>abstract="Cette intégration est disponible pour Adobe Campaign Classic v7 et v8. Il vous permet d’envoyer des emails, des notifications push et des SMS à l’aide des fonctionnalités de messagerie transactionnelle d’Adobe Campaign. La connexion entre les instances Journey Optimizer et Campaign est configurée par Adobe au moment de la mise en service."

Cette intégration est disponible pour Adobe Campaign Classic v7 à partir de la version 7.1 et Adobe Campaign v8. Il vous permet d’envoyer des emails, des notifications push et des SMS à l’aide des fonctionnalités de messagerie transactionnelle d’Adobe Campaign.

La connexion entre les instances Journey Optimizer et Campaign est configurée par Adobe au moment de la mise en service.

Ce cas pratique de bout en bout est présenté dans la section [section](../building-journeys/ajo-ac.md).

Pour chaque action configurée, une activité d’action est disponible dans la palette du concepteur de parcours. Consultez cette section [section](../building-journeys/using-adobe-campaign-classic.md).

## Remarques importantes {#important-notes}

* Il n’y a pas de limitation des messages. Le système limite à 4 000 le nombre de messages pouvant être envoyés par 5 minutes, en fonction du contrat SLA Campaign actuel. C’est pourquoi Journey Optimizer ne doit être utilisé que dans des cas d’utilisation unitaire (événements individuels, et non segments).

* Vous devez configurer une action sur la zone de travail par modèle que vous souhaitez utiliser. Vous devez configurer une action dans Journey Optimizer pour chaque modèle que vous souhaitez utiliser à partir d’Adobe Campaign.

* Nous vous recommandons d’utiliser une instance Message Center dédiée qui est hébergée pour cette intégration afin d’éviter toute incidence sur les autres opérations Campaign que vous avez peut-être effectuées. Le serveur marketing peut être hébergé ou on-premise. La version requise est 21.1 ou supérieure.

* Il n’existe aucune validation indiquant que la payload ou le message Campaign est correct.

* Vous ne pouvez pas utiliser une action Campaign avec un événement de qualification de segment.

## Conditions préalables {#prerequisites}

Dans Campaign, vous devez créer et publier un message transactionnel et son événement associé. Reportez-vous à la section [Documentation Adobe Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html#transactional-messaging){target=&quot;_blank&quot;}.

Vous pouvez créer la charge utile JSON correspondant à chaque message selon le modèle ci-dessous. Vous collez ensuite cette payload lors de la configuration de l’action dans Journey Optimizer (voir ci-dessous).

Voici un exemple :

```
{
    "channel": "email",
    "eventType": "welcome",
    "email": "Email address",
    "ctx": {
        "firstName": "First name"
    }
}
```

* **channel**: le canal défini pour votre modèle transactionnel Campaign
* **eventType**: le nom interne de votre événement Campaign
* **ctx**: en fonction de la personnalisation de votre message.

## Configuration de l’action {#configure-action}

Dans Journey Optimizer, vous devez configurer une action par message transactionnel. Procédez comme suit :

1. Créez une action. Consultez cette section [section](../action/action.md).
1. Saisissez un nom et une description.
1. Dans le **Type d’action** champ, sélectionnez **Adobe Campaign Classic**.
1. Cliquez sur dans le **Payload** et collez un exemple de payload JSON correspondant au message Campaign. Contactez Adobe pour obtenir cette payload.
1. Ajustez les différents champs de sorte qu’ils soient statiques ou variables selon que vous souhaitez les mapper sur la zone de travail du parcours. Certains champs, tels que les paramètres de canal pour l’adresse électronique et les champs de personnalisation (ctx), doivent probablement être définis comme des variables pour le mappage dans le contexte du parcours.
1. Cliquez sur **Enregistrer**.

![](assets/accintegration1.png)
