---
title: Création de simulations
description: Découvrez comment créer des simulations
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: da9e898b-8e5d-43da-9226-5c9ccb78e174
source-git-commit: 65bae1eae9fe425ce7f7c6ce43c6dd978d23570f
workflow-type: tm+mt
source-wordcount: '501'
ht-degree: 100%

---

# Création de simulations

## À propos de la simulation

Pour valider votre logique de prise de décision, vous pouvez simuler les offres qui seront diffusées à un profil de test pour un emplacement donné. 

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

Vous pouvez ainsi tester et affiner différentes versions de vos offres sans aucun impact sur les destinataires ciblés. 

>[!NOTE]
>
>Cette fonctionnalité simule une demande unique à l’API [!DNL Decisions]. Pour en savoir plus, consultez la section [Diffuser des offres à l’aide de l’API Decisions](../api-reference/decisions-api/deliver-offers.md).

Pour accéder à cette fonctionnalité, sélectionnez l’onglet **[!UICONTROL Simulation]** dans le menu **[!UICONTROL Gestion des décisions]**/**[!UICONTROL Offres]**. 

![](../../assets/offers_simulation-tab.png)

<!--
➡️ [Discover this feature in video](#video)
-->

## Sélectionner des profils de test

Vous devez d’abord sélectionner les profils de test que vous allez utiliser pour la simulation. 

1. Cliquez sur **[!UICONTROL Gérer le profil]**.

   ![](../../assets/offers_simulation-manage-profile.png)

1. Sélectionnez l’espace de noms d’identité à utiliser pour identifier les profils de test. Dans cet exemple, nous utiliserons l’espace de noms **E-mail**. 

   >[!NOTE]
   >
   >Un espace de noms d’identité définit le contexte d’un identifiant, tel qu’une adresse e-mail ou un identifiant CRM. Apprenez-en davantage sur les espaces de noms d’identité d’Adobe Experience Platform [dans cette section](../../get-started-identity.md){target=&quot;_blank&quot;}.

1. Saisissez la valeur d’identité et cliquez sur **[!UICONTROL Affichage]** pour répertorier les profils disponibles. 

   ![](../../assets/offers_simulation-add-profile.png)

1. Ajoutez d’autres profils si vous souhaitez tester différentes données de profil et enregistrez votre sélection. 

   ![](../../assets/offers_simulation-save-profiles.png)

1. Une fois ajoutés, tous les profils sont répertoriés dans la liste déroulante sous **[!UICONTROL Profil de test]**. Vous pouvez basculer entre les profils de test enregistrés pour afficher les résultats de chaque profil sélectionné. 

   ![](../../assets/offers_simulation-saved-profiles.png)

1. Vous pouvez cliquer sur le lien **[!UICONTROL Détails du profil]** pour afficher les données de profil sélectionnées. 

<!--Learn more on [selecting test profiles](preview.md#select-test-profiles)-->

## Ajout de portée de décision

Sélectionnez maintenant les décisions d’offre que vous souhaitez simuler sur vos profils de test. 

1. Sélectionnez **[!UICONTROL Ajouter une portée de décision]**.

   ![](../../assets/offers_simulation-add-decision.png)

1. Sélectionnez un emplacement dans la liste. 

   ![](../../assets/offers_simulation-add-decision-scope.png)

1. Les décisions disponibles s’affichent. 

   * Vous pouvez utiliser le champ de recherche pour affiner la sélection. 
   * Vous pouvez cliquer sur le lien **[!UICONTROL Ouvrir les décisions d’offre]** pour ouvrir la liste de toutes les décisions que vous avez créées. En savoir plus sur les [décisions](create-offer-activities.md).

   Sélectionnez la décision de votre choix et cliquez sur **[!UICONTROL Ajouter]**.

   ![](../../assets/offers_simulation-add-decision-scope-add.png)

1. La portée de décision que vous venez de définir s’affiche dans l’espace de travail principal. 

   Vous pouvez ajuster le nombre d’offres que vous souhaitez demander. Par exemple, si vous sélectionnez 2, les 2 meilleures offres s’afficheront pour cette portée de décision. 

   ![](../../assets/offers_simulation-request-offer.png)

   >[!NOTE]
   >
   >Vous pouvez demander jusqu’à 30 offres. 

1. Répétez les étapes ci-dessus pour ajouter autant de décisions que nécessaire. 

   ![](../../assets/offers_simulation-add-more-decisions.png)

   >[!NOTE]
   >
   >Même si vous définissez plusieurs portées de décision, une seule demande d’API est simulée.  
   >
   >Tous les indicateurs de déduplication sont activés par défaut pour la simulation, ce qui signifie que le moteur de décision autorise les doublons et peut donc faire la même proposition dans plusieurs décisions. Pour en savoir plus sur les propriétés des demandes de l’API [!DNL Decisions], consultez [cette section](../api-reference/decisions-api/deliver-offers.md). 

## Afficher les résultats de la simulation

Une fois que vous avez ajouté une portée de décision et sélectionné un profil de test, vous pouvez afficher les résultats. 

1. Cliquez sur **[!UICONTROL Afficher les résultats]**.

   ![](../../assets/offers_simulation-view-results.png)

1. La ou les meilleures offres disponibles sont affichées en fonction du profil sélectionné pour chaque décision. 

   Sélectionnez une offre pour afficher ses détails. 

   ![](../../assets/offers_simulation-offer-details.png)

1. Sélectionnez un autre profil dans la liste pour afficher les résultats des décisions d’offre pour un autre profil de test. 

1. Vous pouvez ajouter, supprimer ou mettre à jour les portées de décision autant de fois que nécessaire. 

>[!NOTE]
>
>Chaque fois que vous modifiez des profils ou mettez à jour des portées de décision, vous devez actualiser les résultats à l’aide du bouton **[!UICONTROL Afficher les résultats]**. 

<!--Questions

* Is it recommended to first select profiles or first add decision scopes?
* What does Request offer changes?
* Nothing displays when I click View results? Can't see any score...
* What's the typical example? i.e. how many decisions do you select, and how do you compare scores?
* What do you learn from simulation? i.e. if I selected 2 decisions and I compare the scores, which one is better or should I use for my customers?
* Is there a way to create relevant test profiles?
* Error on Profile details link.
* Is there a tutorial planned to be released?
* Why still a big red frame when no profile is found?

## Tutorial video {#video}

>[!NOTE]
>
>This video applies to the Offer Decisioning application service built on Adobe Experience Platform. However, it provides generic guidance to use Offer in the context of Journey Optimizer.

>[!VIDEO](https://video.tv.adobe.com/v/329606?quality=12)
-->
