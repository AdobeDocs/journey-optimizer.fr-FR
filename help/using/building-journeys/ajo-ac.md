---
solution: Journey Optimizer
product: journey optimizer
title: Envoyer un message à l'aide de Campaign v7/v8
description: Découvrez comment envoyer un message à l'aide de Campaign v7/v8
feature: Actions
topic: Administration
role: Admin
level: Intermediate
exl-id: b07feb98-b2ae-476c-8fcb-873b308176f0
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '394'
ht-degree: 0%

---

# Cas pratique : envoyer un message à l&#39;aide de Campaign v7/v8 ; {#campaign-classic-use-case}

Ce cas pratique présente toutes les étapes nécessaires pour envoyer un email à l&#39;aide de l&#39;intégration avec Adobe Campaign Classic v7 et Adobe Campaign v8.

Nous allons tout d’abord créer un modèle d’email transactionnel dans Campaign. Ensuite, dans Journey Optimizer, nous allons créer l’événement, l’action et concevoir le parcours.

Pour en savoir plus sur l&#39;intégration de Campaign, consultez les pages suivantes :

* [Création d’une action de campagne](../action/acc-action.md)
* [Utilisation de l’action dans un parcours](../building-journeys/using-adobe-campaign-classic.md).

**Adobe Campaign**

Votre instance Campaign doit être configurée pour cette intégration. La fonctionnalité de messagerie transactionnelle doit être configurée.

1. Connectez-vous à votre instance de pilotage Campaign.

1. Sous **Administration** > **Plateforme** > **Enumérations**, sélectionnez la variable **Type d’événement** Enumération (eventType). Créez un type d’événement (&quot;journey-event&quot;, dans notre exemple). Vous devrez utiliser le nom interne du type d’événement lors de l’écriture ultérieure du fichier JSON.

   ![](assets/accintegration-uc-1.png)

1. Déconnectez-vous et reconnectez-vous à l’instance pour que la création soit effective.

1. Sous **Message Center** > **Modèles de messages transactionnels**, créez un modèle d&#39;email en fonction du type d&#39;événement précédemment créé.

   ![](assets/accintegration-uc-2.png)

1. Concevez votre modèle. Dans cet exemple, nous utilisons la personnalisation sur le prénom et le numéro de commande du profil. Le prénom se trouve dans la source de données Adobe Experience Platform et le numéro de commande est un champ de notre événement Journey Optimizer. Veillez à utiliser les noms de champ corrects dans Campaign.

   ![](assets/accintegration-uc-3.png)

1. Publiez votre modèle transactionnel.

   ![](assets/accintegration-uc-4.png)

1. Vous devez maintenant écrire la charge utile JSON correspondant au modèle.

```
{
     "channel": "email",
     "eventType": "journey-event",
     "email": "Email address",
     "ctx": {
          "firstName": "First name", "purchaseOrderNumber": "Purchase order number"
     }
}
```

* Pour le canal, vous devez saisir &quot;email&quot;.
* Pour eventType, utilisez le nom interne du type d’événement créé précédemment.
* L’adresse électronique est une variable. Vous pouvez donc saisir n’importe quel libellé.
* Sous ctx, les champs de personnalisation sont également des variables.

**Journey Optimizer**

1. Tout d’abord, vous devez créer un événement. Veillez à inclure le champ &quot;purchaseOrderNumber&quot;.

   ![](assets/accintegration-uc-5.png)

1. Vous devez ensuite créer, dans Journey Optimizer, une action correspondant à votre modèle de campagne. Dans le **Type d’action** menu déroulant, sélectionnez **Adobe Campaign Classic**.

   ![](assets/accintegration-uc-6.png)

1. Cliquez sur le bouton **Champ de payload** et collez le fichier JSON créé précédemment.

   ![](assets/accintegration-uc-7.png)

1. Pour l’adresse email et les deux champs de personnalisation, modifiez **Constante** to **Variable**.

   ![](assets/accintegration-uc-8.png)

1. Créez maintenant un parcours et commencez par l’événement précédemment créé.

   ![](assets/accintegration-uc-9.png)

1. Ajoutez l’action et mappez chaque champ au champ approprié dans Journey Optimizer.

   ![](assets/accintegration-uc-10.png)

1. Testez votre parcours.

   ![](assets/accintegration-uc-11.png)

1. Vous pouvez maintenant publier votre parcours.
