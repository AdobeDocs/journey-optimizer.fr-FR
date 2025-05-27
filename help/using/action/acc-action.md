---
solution: Journey Optimizer
product: journey optimizer
title: Intégration à Adobe Campaign v7/v8
description: Découvrez comment intégrer Journey Optimizer à Adobe Campaign v7/v8.
feature: Journeys, Actions, Custom Actions
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate
keywords: campaign, acc, intégration
exl-id: 109ba212-f04b-425f-9447-708c8e0b3f51
source-git-commit: bf4044bc23b0e7c0ef74e5b612d93cb45ec20242
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 67%

---

# Intégration à Adobe Campaign v7/v8 {#integrating-with-adobe-campaign-v7-v8}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_acc"
>title="Actions d&#39;Adobe Campaign v7/v8"
>abstract="Cette intégration est disponible pour Adobe Campaign v7 et v8. Elle permet d&#39;envoyer des e-mails, des notifications push et des SMS à l&#39;aide des fonctionnalités de messagerie transactionnelle d&#39;Adobe Campaign. La connexion entre les instances Journey Optimizer et Campaign est configurée par Adobe au moment de l’approvisionnement."

Si vous disposez de Adobe Campaign Classic v7 ou Campaign v8, une action personnalisée spécifique est disponible dans vos parcours pour intégrer Adobe Journey Optimizer et Adobe Campaign. Cette intégration vous permet d&#39;envoyer des e-mails, des notifications push et des SMS à l&#39;aide des fonctionnalités de messagerie transactionnelle Adobe Campaign. En savoir plus dans ce [cas d’utilisation complet](../building-journeys/ajo-ac.md).

Pour chaque action configurée, une [activité d&#39;action Campaign](../building-journeys/using-adobe-campaign-v7-v8.md) est disponible dans la palette du concepteur de parcours.

## Activation {#access}

Si nécessaire, la connexion entre les environnements Journey Optimizer et Adobe Campaign est configurée par Adobe au moment de l’approvisionnement. Si vous n’avez pas demandé de connexion au moment de la mise en service, contactez l’assistance Adobe Journey Optimizer pour demander l’activation. Vous devez fournir les informations suivantes :

>[!BEGINTABS]

>[!TAB Pour Adobe Journey Optimizer]

* ID d’organisation (OrgID Adobe)

* Nom du sandbox

>[!TAB Pour Adobe Campaign]

* URL du serveur Campaign

* URL du serveur en temps réel

* Version de Campaign

>[!ENDTABS]


## Remarques importantes {#important-notes}

* Il n’y a pas de limitation des messages. Le système limite à 4 000 le nombre de messages pouvant être envoyés touttes les 5 minutes, en fonction du contrat SLA Campaign actuel. C’est la raison pour laquelle Journey Optimizer ne devrait être utilisé que dans des cas d’utilisation unitaires (événements individuels, pas d’audiences).

* Vous devez configurer une action sur la zone de travail pour chaque modèle à utiliser. Vous devez configurer une action dans Journey Optimizer pour chaque modèle que vous souhaitez utiliser dans Adobe Campaign.

* Nous vous recommandons d’utiliser une instance Message Center dédiée et hébergée pour cette intégration afin d’éviter d’impacter les autres opérations de Campaign en cours. Le serveur marketing peut être hébergé ou On-Premise. Le build requis est la version 21.1 Release Candidate ou ultérieure.

* Il n’existe aucune validation indiquant le caractère correct du message Campaign ou de la payload.

* Vous ne pouvez pas utiliser une action de campagne avec un événement de qualification d’audience.

## Conditions préalables {#prerequisites}

Dans Adobe Campaign, vous devez créer et publier un message transactionnel et son événement associé. Reportez-vous à la [documentation d’Adobe Campaign ](https://experienceleague.adobe.com/fr/docs/campaign/campaign-v8/send/real-time/transactional){target="_blank"}.

Vous pouvez créer la payload JSON correspondant à chaque message selon le modèle ci-dessous. Vous allez ensuite coller cette payload lors de la configuration de l’action dans Journey Optimizer (voir ci-dessous).

Voici un exemple :

```JSON
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
* **ctx** : variable basée sur la personnalisation de votre message

## Configuration de l’action {#configure-action}

Dans Journey Optimizer, vous devez configurer une action par message transactionnel. Procédez de la façon suivante :

1. Créez une action. [En savoir plus sur les actions personnalisées](../action/action.md).
1. Saisissez un nom et une description.
1. Dans le champ **Type d’action**, sélectionnez **Adobe Campaign Classic**.
1. Cliquez dans le champ **Payload** et collez un exemple de payload JSON correspondant au message Campaign Contactez Adobe pour obtenir cette payload.
1. Ajustez les différents champs de sorte qu’ils soient statiques ou variables selon que vous souhaitez les mapper ou non sur la zone de travail des parcours. Certains champs, tels que les paramètres de canal pour l’adresse e-mail et les champs de personnalisation (ctx), doivent probablement être définis comme des variables pour le mappage dans le contexte du parcours.
1. Cliquez sur **Enregistrer**.

![](assets/accintegration1.png)