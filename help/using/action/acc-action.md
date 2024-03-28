---
solution: Journey Optimizer
product: journey optimizer
title: Intégration avec Adobe Campaign v7/v8
description: Découvrez comment intégrer Journey Optimizer à Adobe Campaign v7/v8.
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: campaign, acc, intégration
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: f8d62a702824bcfca4221c857acf1d1294427543
workflow-type: tm+mt
source-wordcount: '496'
ht-degree: 96%

---

# Intégration à Adobe Campaign v7/v8 {#integrating-with-adobe-campaign-v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Actions d&#39;Adobe Campaign v7/v8"
>abstract="Cette intégration est disponible pour Adobe Campaign v7 et v8. Elle permet d&#39;envoyer des e-mails, des notifications push et des SMS à l&#39;aide des fonctionnalités de messagerie transactionnelle d&#39;Adobe Campaign. La connexion entre les instances Journey Optimizer et Campaign est configurée par Adobe au moment de l’approvisionnement."

Cette intégration est disponible pour Adobe Campaign v7/v8 à compter de la version 7.1 et Adobe Campaign v8. Elle permet d&#39;envoyer des e-mails, des notifications push et des SMS à l&#39;aide des fonctionnalités de messagerie transactionnelle d&#39;Adobe Campaign.

La connexion entre les instances Journey Optimizer et Campaign est configurée par Adobe au moment de l’approvisionnement.

Un cas d’utilisation complet est présenté dans cette [section](../building-journeys/ajo-ac.md).

Pour chaque action configurée, une activité d’action est disponible dans la palette du concepteur de parcours. Reportez-vous à cette [section](../building-journeys/using-adobe-campaign-v7-v8.md).

## Remarques importantes {#important-notes}

* Il n’y a pas de limitation des messages. Le système limite à 4 000 le nombre de messages pouvant être envoyés touttes les 5 minutes, en fonction du contrat SLA Campaign actuel. C’est la raison pour laquelle Journey Optimizer ne devrait être utilisé que dans des cas d’utilisation unitaires (événements individuels, pas d’audiences).

* Vous devez configurer une action sur la zone de travail pour chaque modèle à utiliser. Vous devez configurer une action dans Journey Optimizer pour chaque modèle que vous souhaitez utiliser dans Adobe Campaign.

* Nous vous recommandons d’utiliser une instance Message Center dédiée et hébergée pour cette intégration afin d’éviter d’impacter les autres opérations de Campaign en cours. Le serveur marketing peut être hébergé ou On-Premise. Le build requis est la version 21.1 Release Candidate ou ultérieure.

* Il n’existe aucune validation indiquant le caractère correct du message Campaign ou de la payload.

* Vous ne pouvez pas utiliser une action de campagne avec un événement de qualification d’audience.

## Conditions préalables {#prerequisites}

Dans Campaign, vous devez créer et publier un message transactionnel et son événement associé. Reportez-vous à la [documentation d’Adobe Campaign](https://experienceleague.adobe.com/docs/campaign-classic/using/transactional-messaging/introduction/about-transactional-messaging.html?lang=fr#transactional-messaging){target="_blank"}.

Vous pouvez créer la payload JSON correspondant à chaque message selon le modèle ci-dessous. Il vous faudra ensuite coller cette payload lors de la configuration de l’&#39;action dans Journey Optimizer (voir ci-dessous)

Voici un exemple :

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

* **channel** : le canal défini pour votre modèle transactionnel Campaign
* **eventType** : le nom interne de votre événement Campaign
* **ctx** : variable basée sur la personnalisation de votre message.

## Configuration de l’action {#configure-action}

Dans Journey Optimizer, vous devez configurer une action par message transactionnel. Procédez de la façon suivante :

1. Créez une nouvelle action. Reportez-vous à cette [section](../action/action.md).
1. Entrez un nom et une description.
1. Dans le champ **Type d’action**, sélectionnez **Adobe Campaign Classic**.
1. Cliquez dans le champ **Payload** et collez un exemple de payload JSON correspondant au message Campaign Contactez Adobe pour obtenir cette payload.
1. Ajustez les différents champs de sorte qu’ils soient statiques ou variables selon que vous souhaitez les mapper ou non sur la zone de travail des parcours. Certains champs, tels que les paramètres de canal pour l’adresse e-mail et les champs de personnalisation (ctx), doivent probablement être définis comme des variables pour le mappage dans le contexte du parcours.
1. Cliquez sur **Enregistrer**.

![](assets/accintegration1.png)