---
title: Création de simulations
description: Découvrez comment créer des simulations
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: da9e898b-8e5d-43da-9226-5c9ccb78e174
source-git-commit: 39b52f39ec19c185d2cd95634a60e37f62a66f83
workflow-type: tm+mt
source-wordcount: '502'
ht-degree: 94%

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
   >Par défaut, tous les indicateurs de déduplication sont activés pour la simulation, ce qui signifie que le moteur de décision autorise les doublons et peut donc faire la même proposition dans plusieurs décisions/emplacements. Pour en savoir plus sur les propriétés des demandes de l’API [!DNL Decisions], consultez [cette section](../api-reference/decisions-api/deliver-offers.md). <!--Deduplication note TO REMOVE WHEN SIMULATIONS V2 is on PROD-->

<!--SIMULATIONS V2

## Define simulation settings {#define-simulation-settings}

To edit the default settings for your simulations, follow the steps below.

1. Click **[!UICONTROL Settings]**.

    ![](../../assets/offers_simulation-settings.png)

1. In the **[!UICONTROL Deduplication]** section, you can choose to allow duplicate offers accross decisions and/or placements. It means that multiple decisions/placements may get assigned the same offer.

    ![](../../assets/offers_simulation-settings-deduplication.png)

    >[!NOTE]
    >
    >By default, all Deduplication flags are enabled for simulation, which means that the decision engine allows duplicates and thus can make the same proposition accross multiple decisions/placements. Learn more on the [!DNL Decisions] API request properties in [this section](../api-reference/decisions-api/deliver-offers.md).

1. In the **[!UICONTROL Response format]** section, you can choose to include metadata in the code view. Check the corresponding option, and select the metadata of your choice. They will be displayed in the request and response payloads when selecting **[!UICONTROL View code]**. Learn more in the [View simulation results](#simulation-results) section.

    ![](../../assets/offers_simulation-settings-response-format.png)

    >[!NOTE]
    >
    >When turning on the option, all items are selected by default.

1. Click **[!UICONTROL Save]**.-->

<!--NOT FOR SIMULATIONS V2

In the **[!UICONTROL API for simulation]** section, select the API you want to use: **[!UICONTROL Hub]** or **[!UICONTROL Edge]**.
Hub and Edge are two different end points for simulation data.

In the **[!UICONTROL Context data]** section, you can add as many elements as needed.

    >[!NOTE]
    >
    >This section is hidden if you select Edge API in the section above. Hub allows the use of Context Data, Edge does not.

Context data allows the user to add contextual data that could affect the simulation score.
For instance, let's say the customer has an offer for a discount on ice cream. In the rules for that offer, it can have logic that would rank it higher when the temperature is above 80 degrees. In simulation, the user could add context data: temperature=65 and that offer would rank lower, of they could add temperature=95 and that would rank higher.
-->

## Afficher les résultats de la simulation {#simulation-results}

Une fois que vous avez ajouté une portée de décision et sélectionné un profil de test, vous pouvez afficher les résultats. 

1. Cliquez sur **[!UICONTROL Afficher les résultats]**.

   ![](../../assets/offers_simulation-view-results.png)

1. La ou les meilleures offres disponibles sont affichées en fonction du profil sélectionné pour chaque décision. 

   Sélectionnez une offre pour afficher ses détails. 

   ![](../../assets/offers_simulation-offer-details.png)

   <!--
    SIMULATIONS V2
    1. Click **[!UICONTROL View code]** to display the request and response payloads. [Learn more](#view-code)-->

1. Sélectionnez un autre profil dans la liste pour afficher les résultats des décisions d’offre pour un autre profil de test. 

1. Vous pouvez ajouter, supprimer ou mettre à jour les portées de décision autant de fois que nécessaire. 

>[!NOTE]
>
>Chaque fois que vous modifiez des profils ou mettez à jour des portées de décision, vous devez actualiser les résultats à l’aide du bouton **[!UICONTROL Afficher les résultats]**. 

<!--
SIMULATIONS V2

## View code {#view-code}

To use the request payload outside of [!DNL Journey Optimizer] - for troubleshooting purpose for example, you can copy it by clicking the corresponding button on top of the code view.
    
>[!NOTE]
>
>You cannot copy the response payload.

Below is an example of code view:

    ```
    curl -X POST \
    'https://platform.adobe.io/data/core/ode/{CONTAINER_ID}/decisions' \
    -H 'Accept: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-response;version=1.0"' \
    -H 'Content-Type: application/vnd.adobe.xdm+json; schema="https://ns.adobe.com/experience/offer-management/decision-request;version=1.0"' \
    -H 'Authorization: Bearer eyJhbGciOiJSUzI1NiIsIng1dSI6Imltc19uYTEtc3RnMS1rZXktMS5jZXIifQ.eyJpZCI6IjE2NDMxMzg3NDMxODlfOTIzY2ZjZjgtOWVkYy00MjE1LWJjODgtYmEyYTY2ZGIyYmMyX3VlMSIsInR5cGUiOiJhY2Nlc3NfdG9rZW4iLCJjbGllbnRfaWQiOiJhY3BfdWlfcGxhdGZvcm0iLCJ1c2VyX2lkIjoiNDhENTc0N0E2MDc3NkRERTBBNDk0MDFEQEFkb2JlSUQiLCJzdGF0ZSI6IntcInNlc3Npb25cIjpcImh0dHBzOi8vaW1zLW5hMS1zdGcxLmFkb2JlbG9naW4uY29tL2ltcy9zZXNzaW9uL3YxL1l6azNNakE0TXpNdFpXVTVaUzAwTVdOaExUZ3pNamd0TmpFM1pqZ3lOak5qTmpSakxTMDBPRVExTnpRM1FUWXdOemMyUkVSRk1FRTBPVFF3TVVSQVFXUnZZbVZKUkFcIn0iLCJhcyI6Imltcy1uYTEtc3RnMSIsImFhX2lkIjoiNDhENTc0N0E2MDc3NkRERTBBNDk0MDFEQEFkb2JlSUQiLCJjdHAiOjAsImZnIjoiV0VQQTNUSUY0UjRaQTZEWlBDUk1BMklBQ1U9PT09PT0iLCJzaWQiOiIxNjQzMDYwMDg0NzI2XzYzNGJkNDEzLWMwYTktNDA0NS1iNTM3LWRmMzgzYzU5ZGIxY191ZTEiLCJydGlkIjoiMTY0MzEzODc0MzE4OV9lYWMxOWY5Yi00ZjhhLTQ1NWMtOWVmMi1mNjYwNmQ0ODY4N2ZfdWUxIiwibW9pIjoiYmVjOTQzYzIiLCJwYmEiOiIiLCJvYyI6InJlbmdhKm5hMXItc3RnMSoxN2U5MmIzNzYzNCo2MEJEVjBGUlhOMFlRMkdHSkRON0E5Tk1HOCIsInJ0ZWEiOiIxNjQ0MzQ4MzQzMTg5IiwiZXhwaXJlc19pbiI6Ijg2NDAwMDAwIiwic2NvcGUiOiJvcGVuaWQsc2Vzc2lvbixyZWFkX29yZ2FuaXphdGlvbnMsYWRkaXRpb25hbF9pbmZvLnByb2plY3RlZFByb2R1Y3RDb250ZXh0LGFkZGl0aW9uYWxfaW5mby5yb2xlcyxhdWRpZW5jZW1hbmFnZXJfYXBpLEFkb2JlSUQiLCJjcmVhdGVkX2F0IjoiMTY0MzEzODc0MzE4OSJ9.TgZ998KHA4Zeoyq7b_NbPv8aPHb2cs9GgP3uJKrTbzosylKKRYqLpj_8HkloI-bFVQFCBCOWbCwtJtkcRIvFlQFruTr5bpMatPV8izEUVutO6smkYBFoGFYyEGuN5Xe97uOJZEHzFSWguGZtgttSrNhXr-j0hFloofjXDJXPB_911dzXALp5s15sd3HLH9XWTwwlqF_a5SMNDXaSj1800RxsB9bJ8_YL0x4pqQwjYJxRGMhiy7Y9IOpwogSBEiqCQitlKYgaO7yaJzFwhfyisnqM7_MWX2ETn-kGFEOoBHxXDTx9P2OPojzb8ChWQgmGf7Expyvtc1ke3nJkppzrxg' \
    -H 'x-api-key: {API_KEY}' \
    -H 'x-gw-ims-org-id: 5D1328435BF324E90A49402A@AdobeOrg' \
    -H 'x-sandbox-name: prod' \
    -D '{
      "xdm:propositionRequests": [
            {
                  "xdm:placementId": "xcore:offer-placement:1416f4109d9d292c",
                  "xdm:activityId": "xcore:offer-activity:1416f4aad9fd99d7",
                  "xdm:itemCount": 2
            }
      ],
      "xdm:profiles": [
            {
                  "xdm:identityMap": {
                        "email": [
                              {
                                    "xdm:id": "poyfair@adobe.com"
                              }
                        ]
                  }
            }
      ],
      "xdm:allowDuplicatePropositions": {
            "xdm:acrossActivities": true,
            "xdm:acrossPlacements": true
      },
      "xdm:responseFormat": {
            "xdm:includeMetadata": {
                  "xdm:activity": [],
                  "xdm:option": [],
                  "xdm:placement": []
            }
      }
    }'
    ```

>[!NOTE]
>
>When copying the request payload into your own code, make sure you replace CONTAINER_ID and API_KEY with your own values.-->

