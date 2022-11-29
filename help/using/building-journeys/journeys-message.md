---
solution: Journey Optimizer
product: journey optimizer
title: Ajouter un message dans un parcours
description: Découvrez comment ajouter un message dans un parcours
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 4db07a9e-c3dd-4873-8bd9-ac34c860694c
source-git-commit: 0b19af568b33d29f4b35deeab6def17919cfe824
workflow-type: tm+mt
source-wordcount: '223'
ht-degree: 73%

---

# E-mail, SMS, Push{#add-a-message-in-a-journey}

[!DNL Journey Optimizer] est fourni avec des fonctionnalités de message intégrées. Vous pouvez simplement ajouter, dans votre parcours, une activité de message push, SMS ou e-mail et [définir les paramètres et le contenu](../messages/messages-in-journeys.md). Elle est ensuite exécutée et envoyée dans le contexte du parcours..

Vous pouvez également configurer des actions spécifiques pour vous envoyer des messages :

* Si vous utilisez un système tiers pour envoyer vos messages, vous pouvez créer une action personnalisée. En savoir plus dans cette [section](../action/action.md).

* Si vous utilisez Campaign et Journey Optimizer, reportez-vous aux sections suivantes :

   * [[!DNL Journey Optimizer] et Campaign Classic v7 / Campaign v8](../action/acc-action.md)
   * [[!DNL Journey Optimizer] et Campaign Standard](../action/acs-action.md)

Pour ajouter un message dans un parcours, procédez comme suit :

1. Débutez votre parcours avec une activité [Événement](general-events.md) ou [Lecture de segment](read-segment.md).

1. Dans la section **Actions** de la palette, effectuez un glisser-déposer d’une activité **E-mail**, **SMS** ou **Push** dans la zone de travail.

   ![](../messages/assets/add-a-message.png)


   Toutes les étapes de paramétrage du message et de définition de son contenu sont présentées dans [cette section](../messages/get-started-content.md).

## Mettre à jour le contenu en direct{#update-live-content}

Vous pouvez mettre à jour le contenu d’un message (email, sms, push) dans un parcours en direct.

Pour ce faire, ouvrez votre parcours en direct, sélectionnez l’activité de message et cliquez sur **Modifier le contenu**.

![](assets/add-a-message2.png)

Cependant, vous ne pouvez pas modifier les attributs utilisés dans la personnalisation, qu’il s’agisse d’attributs de profil ou de données contextuelles (à partir des propriétés d’événement ou de parcours).
