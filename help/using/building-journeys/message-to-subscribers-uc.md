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
  - id: df64005d-8f9a-422e-ba4d-c6f6dc3454b4
subfeature_v2: []
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 924
ht-degree: 38%

---

# Envoyer un message aux abonnés d’une liste {#send-a-message-to-the-subscribers-of-a-list}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment créer un parcours qui envoie un message aux abonnés d’une liste à l’aide du groupe de champs Détails du consentement et des préférences .

>[!ENDSHADEBOX]

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

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page montre comment créer un parcours qui envoie un e-mail aux abonnés d’une liste en remplaçant le paramètre d’adresse e-mail par défaut à l’aide d’une expression qui lit les adresses des abonnés à partir d’un champ de mappage de consentement.

**Intentions:**

* Créez un parcours qui cible les abonnés d’une liste spécifique à l’aide d’une activité Lecture d’audience
* Remplacez l’adresse électronique par défaut dans une activité d’action E-mail à l’aide de l’éditeur d’expression
* Utilisez les fonctions `entry` et `firstEntryKey` pour récupérer les adresses électroniques des abonnés à partir d’une carte de consentement
* Référencez le groupe de champs Détails du consentement et des préférences pour accéder aux données de la liste d’abonnements

**Glossaire:**

* **Remplacement de l’adresse e-mail (remplacement du paramètre)** : paramètre d’activité E-mail de parcours qui remplace l’adresse e-mail de profil par défaut par une expression personnalisée, utilisée dans certains cas, tels que le ciblage des listes d’abonnements. *(spécifique au produit)*
* **Groupe de champs Détails du consentement et des préférences** : groupe de champs de schéma Adobe Experience Platform contenant des données d’abonnement et de consentement, y compris le mappage de `subscriptions` utilisé pour stocker les adresses e-mail des abonnés. *(spécifique au produit)*
* **`entry`fonction** : fonction d’expression qui fait référence à un élément de mappage par sa clé d’espace de noms ; utilisée ici pour faire référence à une liste d’abonnements spécifique (par exemple, `daily-email`). *(spécifique au produit)*
* Fonction **`firstEntryKey`:** fonction d’expression qui récupère la première clé d’un mappage ; utilisée ici pour récupérer la première adresse e-mail du mappage des abonnés d’une liste d’abonnements. *(spécifique au produit)*

**Mécanismes de sécurisation :**

* Le remplacement des adresses e-mail ne doit être utilisé que pour des cas d’utilisation spécifiques, tels que le ciblage des listes d’abonnements. Dans la plupart des cas, l’adresse principale définie dans les Champs d’exécution doit être utilisée
* Le groupe de champs Détails du consentement et des préférences doit être présent dans le schéma pour que ce cas d’utilisation fonctionne
* Le nom de la liste d’abonnements utilisé dans l’expression (par exemple, `daily-email`) doit correspondre exactement au nom configuré dans les données

**Terminologie:**

* Nom canonique : écrasement d’adresse électronique — Acronyme : none — variantes : écrasement de paramètre, écrasement de paramètre d’adresse électronique
* Synonymes : « liste d’abonnements » = « liste d’abonnés »
* Ne pas confondre : « email address override » ≠ « primary email address » — L&#39;adresse e-mail principale est l&#39;adresse par défaut utilisée dans tous les parcours ; le remplacement est une expression par activité utilisée uniquement pour des cas spéciaux, tels que l&#39;envoi de listes d&#39;abonnements

**FAQ:**

* **Q : Comment envoyer un e-mail aux abonnés d’une liste d’abonnements plutôt qu’aux adresses e-mail de profil ?** — Activez le remplacement du paramètre dans le champ Adresse de l&#39;activité E-mail et saisissez une expression à l&#39;aide des fonctions `entry` et `firstEntryKey` pour récupérer les adresses du mappage des abonnés de la liste d&#39;abonnements cible.
* **Q : Quel groupe de champs est requis pour ce cas d’utilisation ?** — Le groupe de champs Détails du consentement et des préférences de Adobe Experience Platform, qui contient la structure de mappage `subscriptions` utilisée pour stocker les adresses électroniques des abonnés.
* **Q : Dois-je toujours utiliser la substitution d’adresse e-mail lors du ciblage des abonnés ?** — Non ; le remplacement de l’adresse e-mail est réservé à des cas d’utilisation spécifiques. Dans la plupart des parcours, l’adresse principale définie dans les Champs d’exécution doit être utilisée.
* **Q : Que fait la fonction `firstEntryKey` dans ce contexte ?** — Il récupère la première clé d&#39;adresse e-mail de la carte `subscribers` associée à une liste d&#39;abonnements spécifique, ce qui permet au parcours d&#39;adresser des abonnés individuels.

+++
