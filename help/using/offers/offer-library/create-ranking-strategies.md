---
product: experience platform
solution: Experience Platform
title: Création de stratégies de classement
description: Découvrez comment créer des modèles AI pour classer les offres.
feature: Ranking Formulas
role: User
level: Intermediate
exl-id: 81d07ec8-e808-4bc6-97b1-b9f7db2aec22
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '676'
ht-degree: 97%

---

# Création de modèles AI {#ai-rankings}

## Création d’une stratégie de classement {#create-ranking-strategy}

Pour créer une stratégie de classement, procédez comme suit :

1. Accédez au menu **[!UICONTROL Composants]**, puis sélectionnez l&#39;onglet **[!UICONTROL Classements par l&#39;IA]**.

   ![](../assets/ai-ranking-list.png)

   Toutes les stratégies de classement créées jusqu&#39;à présent y sont répertoriées.

1. Cliquez sur le bouton **[!UICONTROL Créer une stratégie]**.

1. Renseignez les champs suivants :

   ![](../assets/ai-ranking-fields.png)

   * **[!UICONTROL Nom]** : nom unique que vous devez fournir.

   * **[!UICONTROL Type de modèle]**: Actuellement dans [!DNL Journey Optimizer] le seul type de modèle pris en charge est **[!UICONTROL Optimisation automatique]**. [En savoir plus](ai-ranking.md#auto-optimization)

   * **[!UICONTROL Mesure d&#39;optimisation]** :

      cette option permet aux marketeurs de choisir comment le modèle d&#39;apprentissage automatique doit être créé et formé : selon les offres affichées, les offres ayant fait l&#39;objet d&#39;un clic dans un e-mail et/ou les offres ayant fait l&#39;objet d&#39;un clic sur le web.

      >[!NOTE]
      >
      >Si nécessaire, vous pouvez sélectionner tous les types de mesures.

      Il existe deux types de mesures d&#39;optimisation :
      * **[!UICONTROL Impression]** : actuellement, les événements d&#39;impression correspondent à toutes les offres affichées.
      * **[!UICONTROL Conversion]** : les événements de conversion correspondent à toutes les offres qui génèrent des clics par e-mail ou sur le web.

      Tous les événements d&#39;impression et/ou de conversion sélectionnés seront automatiquement capturés à l&#39;aide du SDK Web ou du SDK Mobile fourni. Pour en savoir plus à ce sujet, consultez la [présentation du SDK web Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/home.html?lang=fr).

   * **[!UICONTROL Identifiant du jeu de données]** : pour la conversion, vous devez fournir un jeu de données dans lequel les événements sont collectés en les sélectionnant dans la liste déroulante. Découvrez comment créer un jeu de données dans [cette section](#create-dataset). <!--This dataset needs to be associated with a schema that must have the **[!UICONTROL Proposition Interactions]** field group (previously known as mixin) associated with it.-->

   ![](../assets/ai-ranking-dataset-id.png)

   >[!CAUTION]
   >
   >Seuls les jeux de données créés à partir de schémas associés au groupe de champs **[!UICONTROL Événement d&#39;expérience - Interactions de propositions]** (précédemment appelé « mixin ») s&#39;affichent dans la liste déroulante.

1. Enregistrez et activez la stratégie de classement.

   ![](../assets/ai-ranking-save-activate.png)

Elle est maintenant prête à être utilisée dans une décision de classement des offres éligibles pour un emplacement. En savoir plus dans [cette section](../offer-activities/configure-offer-selection.md#use-ranking-strategy).<!--TBC?-->

## Création d’un jeu de données pour collecter des événements {#create-dataset}

Vous devez créer un jeu de données dans lequel les événements de conversion seront collectés. Commencez par créer le schéma qui sera utilisé dans votre jeu de données :

1. Dans le menu **[!UICONTROL Data Management]**, sélectionnez **[!UICONTROL Schéma]**, accédez à l&#39;onglet **[!UICONTROL Parcourir]** et cliquez sur **[!UICONTROL Créer un schéma]**.

   ![](../assets/ai-ranking-create-schema.png)

1. Sélectionnez **[!UICONTROL XDM ExperienceEvent]**.

   ![](../assets/ai-ranking-xdm-event.png)

   >[!NOTE]
   >
   >    Pour en savoir plus sur les schémas et les groupes de champs XDM, consultez la [documentation de présentation du système XDM](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr).


1. Dans le champ **[!UICONTROL Rechercher]**, saisissez « interaction de proposition » et sélectionnez le groupe de champs **[!UICONTROL Événement d&#39;expérience - Interactions de proposition]**.

   ![](../assets/ai-ranking-proposition-interactions.png)

   >[!CAUTION]
   >
   >    Le schéma qui sera utilisé dans votre jeu de données doit être associé au groupe de champs **[!UICONTROL Événement d&#39;expérience - Interactions de proposition]**. Sinon, vous ne pourrez pas l&#39;utiliser dans votre stratégie de classement.

1. Cliquez sur **[!UICONTROL Ajouter des groupes de champs]**.

   ![](../assets/ai-ranking-add-field-group.png)

   >[!NOTE]
   >Le groupe de champs était auparavant appelé « mixin ».

1. Saisissez un nom et enregistrez le schéma.<!--How do you edit the fields in this new schema? Examples?-->

>[!NOTE]
>
>    Pour en savoir plus sur la création de schémas, consultez la section [Principes de base de la composition des schémas](https://experienceleague.adobe.com/docs/experience-platform/xdm/schema/composition.html?lang=fr?lang=fr#Understanding-schemas).

Vous êtes maintenant prêt à créer un jeu de données à l&#39;aide de ce schéma. Pour ce faire, procédez comme suit :

1. Dans le menu **[!UICONTROL Data Management]**, sélectionnez **[!UICONTROL Jeux de données]**, accédez à l&#39;onglet **[!UICONTROL Parcourir]** et cliquez sur **[!UICONTROL Créer un jeu de données]**.

   ![](../assets/ai-ranking-create-dataset.png)

1. Sélectionnez **[!UICONTROL Créer un jeu de données à partir d&#39;un schéma]**.

   ![](../assets/ai-ranking-create-dataset-from-schema.png)

1. Sélectionnez le schéma que vous venez de créer dans la liste.

   ![](../assets/ai-ranking-dataset-select-schema.png)

1. Cliquez sur **[!UICONTROL Suivant]**.

1. Attribuez un nom unique au jeu de données dans le champ **[!UICONTROL Nom]** et cliquez sur **[!UICONTROL Terminer]**.

   ![](../assets/ai-ranking-dataset-name.png)

Le jeu de données est maintenant prêt à être sélectionné pour collecter les données dʼévénement lors de la [création dʼune stratégie de classement](#create-ranking-strategy).

## Exigences relatives au schéma de lʼoffre {#schema-requirements}

À ce stade, vous devez avoir :

* créé la stratégie de classement,
* défini le type dʼévénement à capturer : offre affichée (impression) et/ou offre ayant fait l’objet d’un clic (conversion)
* ainsi que le jeu de données dans lequel vous souhaitez collecter les données d’événement.

Désormais, chaque fois quʼune offre est affichée et/ou qu’un utilisateur clique dessus, vous souhaitez que lʼévénement correspondant soit automatiquement capturé par le groupe de champs **[!UICONTROL Événement dʼexpérience - Interactions de proposition]** à lʼaide du [SDK web Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/edge/web-sdk-faq.html?lang=fr#what-is-adobe-experience-platform-web-sdk%3F){target=&quot;_blank&quot;} ou du SDK mobile.

Pour envoyer des types d’événement (offre affichée ou offre ayant fait l’objet d’un clic), vous devez définir la valeur correcte pour chaque type d’événement dans un événement d’expérience qui est envoyé dans Adobe Experience Platform. Vous trouverez ci-dessous les exigences du schéma que vous devez implémenter dans votre code JavaScript :

### Scénario d’offre affichée

**Type d’événement :** `decisioning.propositionDisplay`
**Source :** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) ou ingestion par lots
+++**Exemple de payload :**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionDisplay",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4",
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5",
                }
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id - taken from experience event for “nextBestOffer”
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id - taken from experience event for “nextBestOffer”
        }
    ]
}
```

+++

### Scénario d’offre cliquée

**Type d’événement :** `decisioning.propositionInteract`
**Source :** Web.sdk/Alloy.js (`sendEvent command -> xdm : {eventType, interactionMixin}`) ou ingestion par lots
+++**Exemple de payload :**

```
{
    "@id": "a7864a96-1eac-4934-ab44-54ad037b4f2b",
    "xdm:timestamp": "2020-09-26T15:52:25+00:00",
    "xdm:eventType": "decisioning.propositionInteract",
    "https://ns.adobe.com/experience/decisioning/propositions":
    [
        {
            "xdm:items":
            [
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee4"
                },
                {
                    "xdm:id": "personalized-offer:f67bab756ed6ee5"
                },
            ],
            "xdm:id": "3cc33a7e-13ca-4b19-b25d-c816eff9a70a", //decision event id
            "xdm:scope": "scope:12cfc3fa94281acb", //decision scope id
        }
    ]
}
```

+++

<!--
## Using a ranking strategy {#using-ranking}

To use the ranking strategy you created above, follow the steps below:

Once a ranking strategy has been created, you can assign it to a placement in a decision. For more on this, see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md).

1. Create a decision.
1. Add a placement.
1. Add a collection.
1. Choose to rank offers by AI ranking (select it from the drop-down list).
1. Click Add ranking.
1. Select the ranking strategy that you created. All the details of the ranking strategy are displayed.
1. Click Next to confirm.
1. Save your decision.

It is now ready to be used in a decision to rank eligible offers for a placement (see [Configure offers selection in decisions](../offer-activities/configure-offer-selection.md)).
-->

