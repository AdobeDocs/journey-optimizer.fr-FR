---
solution: Journey Optimizer
product: journey optimizer
title: Envoyer un message aux personnes abonnées
description: Découvrez comment créer un parcours pour envoyer un message aux abonnés d’une liste.
feature: Journeys, Use Cases, Subscriptions
topic: Content Management
role: User, Developer
level: Intermediate, Experienced
keywords: parcours, cas d’utilisation, message, abonnés, liste, lecture
exl-id: 2540938f-8ac7-43fa-83ff-fed59f6bc417
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/sDhncesYlIjsj2zjB-QmjWqP--0KDyp-5x5-UGLSjRc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2: []
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 355
ht-degree: 100%

---

# Envoyer un message aux abonnés d’une liste {#send-a-message-to-the-subscribers-of-a-list}

Ce cas d’utilisation a pour but de créer un parcours pour envoyer un message aux abonnés d’une liste.

Dans cet exemple, le groupe de champs **[!UICONTROL Détails du consentement et des préférences]** de [!DNL Adobe Experience Platform] est utilisé. Pour trouver ce groupe de champs, à partir du menu **[!UICONTROL Gestion des données]**, choisissez **[!UICONTROL Schémas]**. Dans l’onglet **[!UICONTROL Groupes de champs]**, saisissez le nom du groupe de champs dans le champ de recherche.

![Ce groupe de champs comprend l’élément abonnements](assets/consent-and-preference-details-field-group.png).

Pour configurer ce parcours, procédez comme suit:

1. Créez un parcours commençant par une activité **[!UICONTROL Lecture]**. Obtenez des informations supplémentaires dans [Créer votre premier parcours](journey-gs.md)
1. Ajoutez une activité d’action **[!UICONTROL E-mail]** au parcours. Découvrez comment [utiliser les actions de canal](journey-action.md).
1. Dans la section **[!UICONTROL Paramètres de l’e-mail]** des paramètres d’activité **[!UICONTROL E-mail]**, remplacez l’adresse e-mail par défaut (`PersonalEmail.adress`) par l’adresse e-mail des abonnés à la liste :

   1. Cliquez sur le bouton **[!UICONTROL Activer le remplacement de paramètre]** à droite du champ **[!UICONTROL Adresse]**, puis cliquez sur l’icône **[!UICONTROL Modifier]**.

      ![Flux du parcours avec Lecture d’audience pour le ciblage des listes des personnes abonnées](assets/message-to-subscribers-uc-1.png)

   1. Dans l’éditeur d’expression, saisissez l’expression permettant de récupérer les adresses e-mail des abonnés. [En savoir plus](expression/expressionadvanced.md).

      Cet exemple illustre une expression qui comprend des références aux champs de mappage :

      ```json
      #{ExperiencePlatform.Subscriptions.profile.consents.marketing.email.subscriptions.entry('daily-email').subscribers.firstEntryKey()}
      ```

      Dans cet exemple, les fonctions suivantes sont utilisées :

      | Fonction | Description | Exemple |
      | --- | --- | --- |
      | `entry` | Renvoie à un élément de mappage selon l’espace de noms sélectionné. | Renvoyer à une liste d’abonnements spécifique |
      | `firstEntryKey` | Récupère la première clé d’entrée d’un mappage. | Récupérer la première adresse e-mail des abonnés |

      Dans cet exemple, la liste d’abonnements est nommée `daily-email`. Les adresses e-mail sont définies comme des clés dans le mappage `subscribers`, qui est lié au mappage de la liste d’abonnements.

      En savoir plus sur les [références aux champs](expression/field-references.md) dans les expressions.

      ![Configuration du canal e-mail avec du contenu personnalisé pour les personnes abonnées](assets/message-to-subscribers-uc-2.png)

   1. Dans la boîte de dialogue **[!UICONTROL Ajouter une expression]**, cliquez sur **[!UICONTROL OK]**.

>[!CAUTION]
>
>Le remplacement de l’adresse e-mail ne doit être utilisé que pour des cas d’utilisation spécifiques. La plupart du temps, il n’est pas nécessaire de modifier l’adresse e-mail, car la valeur définie comme adresse principale dans les **[!UICONTROL Champs d&#39;exécution]** est celle qui doit être utilisée. [En savoir plus](../configuration/primary-email-addresses.md)
