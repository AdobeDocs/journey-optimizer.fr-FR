---
title: Créer des simulations
description: Découvrez comment simuler les offres qui seront diffusées pour un emplacement donné afin de valider votre logique de prise de décision
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: da9e898b-8e5d-43da-9226-5c9ccb78e174
source-git-commit: f50617dc5ea07d01d1f7ec1ab3f9790557dcd957
workflow-type: tm+mt
source-wordcount: '807'
ht-degree: 0%

---

# Créer des simulations {#create-simulations}

## A propos de la simulation {#about-simulation}

Pour valider votre logique de prise de décision, vous pouvez simuler les offres qui seront diffusées à un profil de test pour un emplacement donné.

<!--Simulation allows you to view the results of offer decisions as a selected profile.-->

Vous pouvez ainsi tester et affiner différentes versions de vos offres sans aucun impact sur les destinataires ciblés.

>[!NOTE]
>
>Cette fonctionnalité simule une requête unique à la fonction [!DNL Decisioning] API. En savoir plus sur [Diffuser des offres à l’aide de l’API de prise de décision](../api-reference/offer-delivery-api/decisioning-api.md).

Pour accéder à cette fonctionnalité, sélectionnez la **[!UICONTROL Simulation]** à partir de l’onglet **[!UICONTROL Decision management]** > **[!UICONTROL Offers]** .

![](../assets/offers_simulation-tab.png)

>[!NOTE]
>
>Comme la simulation ne génère aucun événement de décision, la variable [capping](../offer-library/creating-personalized-offers.md#capping) n’est pas affecté.

<!--
➡️ [Discover this feature in video](#video)
-->

## Sélection de profils de test {#select-test-profiles}

>[!CONTEXTUALHELP]
>id="ajo_decisioning_simulation_test_profile"
>title="Ajout de profils de test"
>abstract="Vous pouvez ajouter un profil de test en sélectionnant un espace de noms d’identité et une valeur d’identité correspondante. Vous devez disposer de profils de test déjà disponibles pour pouvoir les utiliser en simulation."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/segment/profiles/creating-test-profiles.html" text="Créer des profils de test"

Vous devez d&#39;abord sélectionner les profils de test que vous allez utiliser pour la simulation.

>[!CAUTION]
>
>Vous devez disposer de profils de test pour simuler les offres qui leur seront diffusées. Découvrez comment [créer des profils de test](../../segment/creating-test-profiles.md).

1. Cliquez sur **[!UICONTROL Manage profile]**.

   ![](../assets/offers_simulation-manage-profile.png)

1. Sélectionnez l’espace de noms d’identité à utiliser pour identifier les profils de test. Dans cet exemple, nous utiliserons la variable **Email** espace de noms.

   >[!NOTE]
   >
   >Un espace de noms d’identité définit le contexte d’un identifiant, tel qu’une adresse électronique ou un identifiant CRM. En savoir plus sur les espaces de noms d’identité Adobe Experience Platform [dans cette section](../../segment/get-started-identity.md){target=&quot;_blank&quot;}.

1. Saisissez la valeur d’identité et cliquez sur **[!UICONTROL View]** pour répertorier les profils disponibles.

   ![](../assets/offers_simulation-add-profile.png)

1. Ajoutez d’autres profils si vous souhaitez tester différentes données de profil et enregistrez votre sélection.

   ![](../assets/offers_simulation-save-profiles.png)

1. Une fois ajoutés, tous les profils sont répertoriés dans la liste déroulante sous **[!UICONTROL Test profile]**. Vous pouvez basculer entre les profils de test enregistrés pour afficher les résultats pour chaque profil sélectionné.

   ![](../assets/offers_simulation-saved-profiles.png)

   >[!NOTE]
   >
   >Les profils sélectionnés restent répertoriés en tant que profils de test dans la variable **[!UICONTROL Simulation]** d’une session à l’autre jusqu’à ce qu’elles soient supprimées à l’aide de **[!UICONTROL Manage profile]**.

1. Vous pouvez cliquer sur le bouton **[!UICONTROL Profile details]** lien pour afficher les données de profil sélectionnées.

<!--Learn more on [selecting test profiles](messages/preview.md#select-test-profiles)-->

## Ajout de portées de décision {#add-decision-scopes}

Sélectionnez maintenant les décisions d’offre que vous souhaitez simuler sur vos profils de test.

1. Sélectionner **[!UICONTROL Add decision scope]**.

   ![](../assets/offers_simulation-add-decision.png)

1. Sélectionnez un emplacement dans la liste.

   ![](../assets/offers_simulation-add-decision-scope.png)

1. Les décisions disponibles s’affichent.

   * Vous pouvez utiliser le champ de recherche pour affiner la sélection.
   * Vous pouvez cliquer sur le bouton **[!UICONTROL Open offer decisions]** pour ouvrir la liste de toutes les décisions que vous avez créées. En savoir plus sur [décisions](create-offer-activities.md).

   Sélectionnez la décision de votre choix et cliquez sur **[!UICONTROL Add]**.

   ![](../assets/offers_simulation-add-decision-scope-add.png)

1. La portée de décision que vous venez de définir s’affiche dans l’espace de travail principal.

   Vous pouvez ajuster le nombre d’offres que vous souhaitez demander. Par exemple, si vous sélectionnez 2, les 2 meilleures offres s’afficheront pour cette portée de décision.

   ![](../assets/offers_simulation-request-offer.png)

   >[!NOTE]
   >
   >Vous pouvez demander jusqu’à 30 offres.

1. Répétez les étapes ci-dessus pour ajouter autant de décisions que nécessaire.

   ![](../assets/offers_simulation-add-more-decisions.png)

   >[!NOTE]
   >
   >Même si vous définissez plusieurs portées de décision, une seule requête API est simulée.

## Définition des paramètres de simulation {#define-simulation-settings}

Pour modifier les paramètres par défaut de vos simulations, procédez comme suit.

1. Cliquez sur **[!UICONTROL Settings]**.

   ![](../assets/offers_simulation-settings.png)

1. Dans le **[!UICONTROL Deduplication]** , vous pouvez choisir d’autoriser les offres en double pour les décisions et/ou les emplacements. Cela signifie que plusieurs décisions/emplacements peuvent se voir attribuer la même offre.

   ![](../assets/offers_simulation-settings-deduplication.png)

   >[!NOTE]
   >
   >Par défaut, tous les indicateurs de déduplication sont activés pour la simulation, ce qui signifie que le moteur de décision autorise les doublons et peut donc faire la même proposition dans plusieurs décisions/emplacements. En savoir plus sur la [!DNL Decisioning] Propriétés de requête d’API dans [cette section](../api-reference/offer-delivery-api/decisioning-api.md).

1. Dans le **[!UICONTROL Response format]** vous pouvez choisir d’inclure des métadonnées dans la vue de code. Cochez l’option correspondante, puis sélectionnez les métadonnées de votre choix. Elles s’affichent dans les payloads de requête et de réponse lors de la sélection de **[!UICONTROL View code]**. En savoir plus dans la section [Affichage des résultats de la simulation](#simulation-results) .

   ![](../assets/offers_simulation-settings-response-format.png)

   >[!NOTE]
   >
   >Lorsque l’option est activée, tous les éléments sont sélectionnés par défaut.

1. Cliquez sur **[!UICONTROL Save]**.

>[!NOTE]
>
>Actuellement, pour les données de simulation, vous pouvez uniquement utiliser la variable **[!UICONTROL Hub]** API.

<!--
In the **[!UICONTROL API for simulation]** section, select the API you want to use: **[!UICONTROL Hub]** or **[!UICONTROL Edge]**.
Hub and Edge are two different end points for simulation data.

In the **[!UICONTROL Context data]** section, you can add as many elements as needed.

    >[!NOTE]
    >
    >This section is hidden if you select Edge API in the section above. Hub allows the use of Context data, Edge does not.

Context data allows the user to add contextual data that could affect the simulation score.
For instance, let's say the customer has an offer for a discount on ice cream. In the rules for that offer, it can have logic that would rank it higher when the temperature is above 80 degrees. In simulation, the user could add context data: temperature=65 and that offer would rank lower, of they could add temperature=95 and that would rank higher.
-->

## Affichage des résultats de la simulation {#simulation-results}

Une fois que vous avez ajouté une portée de décision et sélectionné un profil de test, vous pouvez afficher les résultats.

1. Cliquez sur **[!UICONTROL View results]**.

   ![](../assets/offers_simulation-view-results.png)

1. Les meilleures offres disponibles s’affichent en fonction du profil sélectionné pour chaque décision.

   Sélectionnez une offre pour afficher ses détails.

   ![](../assets/offers_simulation-offer-details.png)

1. Cliquez sur **[!UICONTROL View code]** pour afficher les payloads de requête et de réponse. [En savoir plus](#view-code)

1. Sélectionnez un autre profil dans la liste pour afficher les résultats des décisions d’offre pour un autre profil de test.

1. Vous pouvez ajouter, supprimer ou mettre à jour les portées de décision autant de fois que nécessaire.

>[!NOTE]
>
>Chaque fois que vous modifiez des profils ou mettez à jour des portées de décision, vous devez actualiser les résultats à l’aide de la variable **[!UICONTROL View results]** bouton .

## Afficher le code {#view-code}

1. Utilisez la variable **[!UICONTROL View code]** pour afficher les payloads de requête et de réponse.

   ![](../assets/offers_simulation-view-code.png)

   L’affichage du code affiche les informations sur le développeur pour l’utilisateur actuel. Par défaut, la variable **[!UICONTROL Response payload]** s’affiche.

   ![](../assets/offers_simulation-request-payload.png)

1. Cliquez sur **[!UICONTROL Response payload]** ou **[!UICONTROL Request payload]** pour naviguer entre les deux onglets.

   ![](../assets/offers_simulation-response-payload.png)

1. Pour utiliser le payload de requête en dehors de [!DNL Journey Optimizer] - à des fins de dépannage, par exemple, copiez-le à l’aide de la fonction **[!UICONTROL Copy to clipboard]** en haut de l’affichage du code.

   ![](../assets/offers_simulation-copy-payload.png)

   <!--You cannot copy the response payload. ACTUALLY YES YOU CAN > to confirm with PM/dev? -->

   >[!NOTE]
   >
   >Lors de la copie des payloads de requête ou de réponse dans votre propre code, veillez à remplacer {USER_TOKEN} et {API_KEY} par des valeurs valides. Découvrez comment récupérer ces valeurs dans la variable [API Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/landing/platform-apis/api-authentication.html)Documentation {target=&quot;_blank&quot;}.

