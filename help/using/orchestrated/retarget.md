---
solution: Journey Optimizer
product: journey optimizer
title: Démarrer et surveiller les campagnes orchestrées avec Adobe Journey Optimizer
description: Découvrez comment démarrer et surveiller des campagnes orchestrées avec Adobe Journey Optimizer.
feature: Monitoring
exl-id: 3c1cad30-3ed7-4df1-a46a-60394a834e79
version: Campaign Orchestration
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '657'
ht-degree: 100%

---


# Créer des requêtes de reciblage {#retarget}

Le reciblage permet de relancer les destinataires en fonction de leur réaction à une campagne orchestrée précédente. Par exemple, il est possible d’envoyer un deuxième e-mail aux destinataires qui ont reçu, mais n’ont pas cliqué sur le premier.

**[!UICONTROL Campagne orchestrée]** fournit deux attributs principaux à cet effet :

* **[!UICONTROL Retour sur les messages]** : capture les événements liés à la diffusion, par exemple message envoyé, ouvert, rejeté, etc.
* **[!UICONTROL Suivi des e-mails]** : capture les actions de l’utilisateur ou de l’utilisatrice, par exemple clics et ouvertures.

![](assets/do-not-localize/retarget-schema.png){zoomable="yes"}


## Créer une règle de reciblage basée sur le retour {#feedback-retarget}

La règle de reciblage basée sur le retour permet de recibler les destinataires en fonction des événements de diffusion des messages capturés dans l’attribut **[!UICONTROL Retour sur les messages]**. Ces événements incluent des résultats tels que l’envoi, l’ouverture, le rejet ou le marquage des messages comme indésirables.

À l’aide de ces données, il est possible de définir des règles pour identifier les destinataires ayant reçu un message précédent, ce qui permet d’assurer une communication de suivi fondée sur des statuts de diffusion spécifiques.

1. Créer une nouvelle **[!UICONTROL campagne orchestrée]**.

1. Ajoutez une activité **[!UICONTROL Créer une audience]** et définissez la dimension de ciblage sur **[!UICONTROL Destinataire (caas)]**.

1. Dans le **[!UICONTROL Créateur de règles]**, cliquez sur **[!UICONTROL Ajouter une condition]** et sélectionnez **[!UICONTROL Retour sur les messages]** dans le **[!UICONTROL Sélecteur d’attributs]**. Cliquez sur **[!UICONTROL Confirmer]** pour créer une condition **Retour sur les messages existants**.

   ![](assets/retarget_1.png){zoomable="yes"}

1. Choisissez l’attribut **[!UICONTROL Statut du retour]** pour cibler les événements de diffusion des messages.

   +++ Guide détaillé

   1. Ajoutez une autre condition liée à l’attribut **[!UICONTROL Retour sur les messages]**.

   1. Recherchez l’attribut **[!UICONTROL Statut du retour]** et cliquez sur **[!UICONTROL Confirmer]**.

      ![](assets/retarget_3.png){zoomable="yes"}

   1. Dans le menu **[!UICONTROL Condition personnalisée]**, choisissez le statut de diffusion à suivre dans la liste déroulante **[!UICONTROL Valeur]**.

      ![](assets/retarget_4.png){zoomable="yes"}

   +++

1. Choisissez l’attribut **[!UICONTROL Nom de la campagne orchestrée]** pour cibler une campagne orchestrée spécifique.

   +++ Guide détaillé

   1. Ajoutez une autre condition liée à l’attribut **[!UICONTROL Retour sur les messages]**, recherchez **[!UICONTROL Entité]** et accédez à :

      `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign entity`.

   1. Sélectionnez **[!UICONTROL Nom de la campagne orchestrée]**.

      ![](assets/retarget_5.png){zoomable="yes"}

   1. Dans le menu **[!UICONTROL Condition personnalisée]**, indiquez le nom de la campagne dans le champ **[!UICONTROL Valeur]**.

   +++

1. Sélectionnez l’attribut **[!UICONTROL Nom de l’action de campagne orchestrée]** pour cibler un message ou une activité spécifique dans une campagne orchestrée.

   +++ Guide détaillé

   1. Ajoutez une autre condition liée à l’attribut **[!UICONTROL Retour sur les messages]**, recherchez **[!UICONTROL Entité]** et accédez à :

      `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign entity`.

   1. Sélectionnez **[!UICONTROL Nom de l’action de campagne orchestrée]**.

      ![](assets/retarget_6.png){zoomable="yes"}

   1. Dans le menu **[!UICONTROL Condition personnalisée]**, indiquez le nom de l’action de campagne dans le champ **[!UICONTROL Valeur]**.

      Les noms d’action peuvent être consultés en cliquant sur ![icône d’information](assets/do-not-localize/info-icon.svg) située à côté du champ Libellé de votre activité.

   +++

1. Vous pouvez également filtrer par l’**[!UICONTROL identifiant de campagne]** (UUID), que vous trouverez dans les propriétés de la campagne.

Vous avez maintenant configuré une règle de reciblage basée sur le retour afin d’identifier les destinataires en fonction du statut de diffusion d’un message précédent, tel qu’envoyé, ouvert, rejeté ou marqué comme indésirable. Avec cette audience définie, vous pouvez soit ajouter un e-mail de suivi, soit affiner davantage le ciblage en [configurant une règle de reciblage basée sur le suivi](#tracking-based), qui exploite les données d’interaction des utilisateurs ou des utilisatrices.

![](assets/retarget_9.png){zoomable="yes"}


## Créer une règle de reciblage basée sur le suivi {#tracking-based}

La règle de reciblage basée sur le suivi cible les destinataires en fonction de leurs interactions avec un message, en utilisant les données de l’attribut **[!UICONTROL Suivi des e-mails]**. Elle capture les actions de l’utilisateur ou de l’utilisatrice, telles que les ouvertures d’e-mails et les clics sur les liens.

Pour recibler les destinataires en fonction des interactions sur les messages (par exemple ouverture ou clic), utilisez l’entité **[!UICONTROL Suivi des e-mails]** comme suit :

1. Créer une nouvelle **[!UICONTROL campagne orchestrée]**.

1. Ajoutez une activité **[!UICONTROL Créer une audience]** et définissez la dimension de ciblage sur **[!UICONTROL Destinataire]** afin de vous concentrer sur les destinataires des campagnes orchestrées précédentes.

1. Dans le **[!UICONTROL créateur de règles]**, cliquez sur **[!UICONTROL Ajouter une condition]** et sélectionnez **[!UICONTROL Suivi des e-mails]** dans le **[!UICONTROL sélecteur d’attributs]**.

   Cliquez sur **[!UICONTROL Confirmer]** pour créer une condition **Suivi des e-mails existant**.

   ![](assets/retarget_2.png){zoomable="yes"}

1. Pour cibler les interactions des destinataires avec un message, ajoutez une autre condition liée à l’attribut **[!UICONTROL Suivi des e-mails]** et recherchez l’attribut **[!UICONTROL Type d’interaction]**.

   ![](assets/retarget_7.png){zoomable="yes"}

1. Dans les options de condition personnalisée, utilisez **[!UICONTROL Inclus dans]** comme opérateur et sélectionnez une ou plusieurs valeurs selon le cas d’utilisation, par exemple **[!UICONTROL Message ouvert]** ou **[!UICONTROL Message avec lien ayant fait l’objet d’un clic]**.

   ![](assets/retarget_8.png){zoomable="yes"}

Vous avez maintenant configuré une règle de reciblage basée sur le suivi afin de cibler les destinataires en fonction de leurs interactions avec un message précédent, telles que les ouvertures d’e-mails ou les clics sur les liens, en utilisant les données de l’attribut **[!UICONTROL Suivi des e-mails]**. Une fois cette audience définie, vous pouvez soit ajouter une action de suivi, soit affiner davantage le ciblage en la combinant avec une [règle de reciblage basée sur le retour](#feedback-retarget) afin d’inclure des résultats de messages tels qu’envoyé, rejeté ou marqué comme indésirable.


![](assets/retarget_10.png){zoomable="yes"}
