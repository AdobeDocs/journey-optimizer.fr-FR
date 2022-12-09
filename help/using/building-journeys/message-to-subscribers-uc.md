---
solution: Journey Optimizer
product: journey optimizer
title: Envoyer un message aux abonnés
description: Découvrez comment créer un parcours pour envoyer un message aux abonnés d’une liste
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '256'
ht-degree: 0%

---

# Cas pratique : envoyer un message aux abonnés d&#39;une liste ;{#send-a-message-to-the-subscribers-of-a-list}

Ce cas pratique a pour but de créer un parcours pour envoyer un message aux abonnés d’une liste.

Dans cet exemple, la variable **[!UICONTROL Consent and Preference Details]** groupe de champs de [!DNL Adobe Experience Platform] est utilisée. Pour trouver ce groupe de champs, à partir du **[!UICONTROL Data Management]** menu, choisissez **[!UICONTROL Schemas]**. Sur le **[!UICONTROL Field groups]** , saisissez le nom du groupe de champs dans le champ de recherche.

![Ce groupe de champs comprend l’élément abonnements](assets/consent-and-preference-details-field-group.png)

Pour configurer ce parcours, procédez comme suit :

1. Créez un parcours commençant par un **[!UICONTROL Read]** activité. [En savoir plus](journey-gs.md).
1. Ajoutez un **[!UICONTROL Email]** activité d’action dans le parcours. [En savoir plus](journeys-message.md).
1. Dans le **[!UICONTROL Email parameters]** de la section **[!UICONTROL Email]** paramètres d’activité, remplacez l’adresse électronique par défaut (`PersonalEmail.adress`) avec l&#39;adresse email des abonnés à la liste :

   1. Cliquez sur le bouton **[!UICONTROL Enable parameter override]** à droite de l’icône **[!UICONTROL Address]** , puis cliquez sur le champ **[!UICONTROL Edit]** icône .

      ![](assets/message-to-subscribers-uc-1.png)

   1. Dans l&#39;éditeur d&#39;expression, saisissez l&#39;expression permettant de récupérer les adresses email des abonnés. [En savoir plus](expression/expressionadvanced.md).

      Cet exemple illustre une expression qui comprend des références aux champs de mappage :

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      Dans cet exemple, les fonctions suivantes sont utilisées :

      | Fonction | Description | Exemple |
      | --- | --- | --- |
      | `entry` | Reportez-vous à un élément map en fonction de l’espace de noms sélectionné. | Reportez-vous à une liste d’abonnements spécifique |
      | `firstEntryKey` | Récupération de la première clé d’entrée d’une carte | Récupérer la première adresse email des abonnés |

      Dans cet exemple, la liste des abonnements est nommée `daily-email`. Les adresses électroniques sont définies comme clés dans la variable `subscribers` map, qui est liée à la carte de la liste d’abonnements.

      En savoir plus sur [références aux champs](expression/field-references.md) dans les expressions.

      ![](assets/message-to-subscribers-uc-2.png)

   1. Dans le **[!UICONTROL Add an expression]** boîte de dialogue, cliquez sur **[!UICONTROL Ok]**.
