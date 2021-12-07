---
title: Créer une liste d’abonnements
description: Découvrez comment configurer une liste d’abonnements dans Journey Optimizer
feature: Landing Pages
topic: Content Management
role: User
level: Beginner
hidefromtoc: true
hide: true
exl-id: 5e5419a0-5121-4aa7-a975-b1f08e2918c9
source-git-commit: 88b037e079a46e10f7ee4715e78e5edc5a34a6ce
workflow-type: tm+mt
source-wordcount: '363'
ht-degree: 1%

---

# Listes d&#39;abonnements {#create-subscription-list}

## Qu&#39;est-ce qu&#39;une liste d&#39;abonnements ?

Un service d’abonnement se rapporte aux produits et services marketing fournis aux clients qui ont choisi de recevoir des communications sur un sujet/événement/intérêt/etc. spécifique. sur une base continue. Dans [!DNL Journey Optimizer], ces clients inscrits sont regroupés dans une liste d’abonnements.

Un service d&#39;abonnement peut être :

* une newsletter, par exemple : &quot;Série en cours&quot;
* un événement, par exemple : &quot;Summit 2021&quot;
* un webinaire, par exemple : &quot;En savoir plus sur le crypto&quot;
* un intérêt sur un produit/un sport/un service/etc., par exemple : &quot;Intéressé à acheter une maison dans les 12 prochains mois&quot;
* une préférence sur le mode de notification, par exemple : &quot;Recevez de nouvelles notifications de chanson par email&quot;

Les profils peuvent être ajoutés à une liste d’abonnements au moyen d’un [landing page](create-lp.md). Un exemple est présenté dans la section [cette section](lp-use-cases.md#subscription-to-a-service).

## Définition d’une liste d’abonnements {#define-subscription-list}

Pour créer une liste d&#39;abonnements, procédez comme suit.

1. Pour accéder aux listes d&#39;abonnements, sélectionnez **[!UICONTROL Client]** > **[!UICONTROL Liste d&#39;abonnements]**.

   ![](../assets/lp_subscription-lists.png)

1. Sélectionnez la **[!UICONTROL Créer une liste d’abonnements]** bouton .

   ![](../assets/lp_create-subscription-list.png)

1. Ajoutez un nom et une description. Ces champs sont obligatoires.

1. Vous pouvez définir une date de début et une date de fin.

   ![](../assets/lp_subscription-list-dates.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

La liste affiche toutes les listes d&#39;abonnements créées. Vous pouvez les filtrer selon la date de création ou de modification, et leur état.

![](../assets/lp_subscription-filters.png)

Les statuts possibles sont les suivants :

* **[!UICONTROL Pas démarré]**: Vous avez défini une date de début postérieure à la date du jour en cours. Les profils abonnés ne recevront pas encore de communications relatives à cette liste d&#39;abonnements.
* **[!UICONTROL En direct]**: Le jour en cours se compose de la date de début et de fin de la liste d’abonnements ou vous n’avez pas défini de date de fin/début, ce qui signifie que la liste d’abonnements est toujours active.
* **[!UICONTROL Expiré]**: La date de fin est dépassée, la liste d&#39;abonnements n&#39;est donc plus valide. Aucun profil abonné ne recevra aucune communication relative à cette liste d’abonnements.

Une fois la liste d&#39;abonnements créée, vous pouvez l&#39;utiliser dans une landing page. Les profils qui se connectent par le biais du formulaire de landing page seront ajoutés à la liste. [En savoir plus](design-lp.md)

Vous pouvez également utiliser des listes d’abonnements comme segments lorsque [parcours de création](../building-journeys/journey-gs.md#jo-build) et l’ajout de la personnalisation.

>[!NOTE]
>
>Vous pouvez surveiller les impacts de votre liste d’abonnements par le biais de rapports spécifiques. [En savoir plus](subscription-report.md)

<!--

**Questions**

* Can't see the newly created subscription list in UI because their name included spacing > bug - to follow up (should be fixed for Dec. release)

* Can you update the subscription list in a way other than through a LP? Not in UI but with APIs > to follow up with Fred

-->
