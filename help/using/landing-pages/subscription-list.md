---
title: Création d’une liste dʼabonnements
description: Découvrez comment configurer une liste dʼabonnements dans Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 100%

---

# Listes dʼabonnements {#create-subscription-list}

## Qu’est-ce qu’une liste dʼabonnements ? {#subscription-list-definition}

Un service d’abonnement fait référence aux produits et services marketing fournis aux clients qui ont choisi de recevoir des communications sur un sujet/événement/intérêt spécifique etc. de manière régulière. Dans [!DNL Journey Optimizer], ces clients inscrits sont regroupés dans une liste d’abonnements.

Voici quelques exemples de services dʼabonnement :

* une newsletter, par exemple : « Série de courses »
* un événement, par exemple : « Sommet 2021 »
* un webinaire, par exemple : « En savoir plus sur la crypto »
* un intérêt pour un produit/sport/service etc., par exemple : « Souhaite acheter une maison dans les 12 prochains mois »
* une préférence en matière de notification, par exemple : « Recevoir les notifications de nouvelles chansons par e-mail »

Les profils peuvent être ajoutés à une liste dʼabonnements au moyen dʼune [page de destination](create-lp.md). Retrouvez un exemple dans [cette section](lp-use-cases.md#subscription-to-a-service).

## Définition d’une liste dʼabonnements {#define-subscription-list}

Pour créer une liste dʼabonnements, procédez comme suit :

1. Pour accéder aux listes dʼabonnements, sélectionnez **[!UICONTROL Client]** > **[!UICONTROL Liste dʼabonnements]**.

   ![](assets/lp_subscription-lists.png)

1. Cliquez sur le bouton **[!UICONTROL Créer une liste dʼabonnements]**.

   ![](assets/lp_create-subscription-list.png)

1. Donnez-lui un nom et une description. Ces champs sont obligatoires.

1. Vous pouvez définir une date de début et de fin.

   ![](assets/lp_subscription-list-dates.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

La liste reprend toutes les listes dʼabonnements créées. Vous pouvez les filtrer en fonction de leur date de création ou de modification et de leur statut.

![](assets/lp_subscription-filters.png)

Voici les statuts possibles :

* **[!UICONTROL Non démarrée]** : vous avez défini une date de début postérieure à la date du jour en cours. Les profils abonnés ne recevront pas encore les communications relatives à cette liste dʼabonnements.
* **[!UICONTROL En direct]** : le jour en cours est compris entre les dates de début et de fin de la liste d’abonnements, ou vous n’avez pas défini de dates de fin/début, ce qui signifie que la liste d’abonnements est toujours active.
* **[!UICONTROL Expirée]** : la date de fin est dépassée, la liste dʼabonnements nʼest donc plus valide. Tout profil abonné ne recevra plus de communications relatives à cette liste dʼabonnements.

Une fois la liste dʼabonnements créée, vous pouvez lʼutiliser dans une page de destination. Les profils inscrits par le biais du formulaire de la page de destination seront ajoutés à la liste. [En savoir plus](design-lp.md)

Vous pouvez également utiliser les listes d’abonnements comme des segments lorsque vous [créez des parcours](../building-journeys/journey-gs.md#jo-build) et ajoutez de la personnalisation.

>[!NOTE]
>
>Vous pouvez surveiller lʼimpact de votre liste d’abonnements grâce à des rapports spécifiques. [En savoir plus](subscription-report.md)

<!--

**Questions**

* Can't see the newly created subscription list in UI because their name included spacing > bug - to follow up (should be fixed for Dec. release)

* Can you update the subscription list in a way other than through a LP? Not in UI but with APIs > to follow up with Fred

-->
