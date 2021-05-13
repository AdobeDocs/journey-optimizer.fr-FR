---
title: Configuration d’un événement métier
description: Découvrez comment créer un événement d'entreprise
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '837'
ht-degree: 50%

---

# Configurer un événement métier {#configure-a-business-event}

![](../assets/do-not-localize/badge.png)

Contrairement aux événements unitaires, les événements d&#39;entreprise ne sont pas liés à un profil spécifique. Le type d’ID de événement est toujours basé sur des règles. Pour en savoir plus sur les événements d&#39;affaires, consultez [cette section](../event/about-events.md).

Les parcours basés sur les segments de lecture peuvent être déclenchés par un seul coup, par un Planificateur régulièrement ou par un événement d’activité, lorsque le événement se produit.

Les événements d&#39;affaires peuvent être &quot;un produit est de retour en stock&quot;, &quot;le prix des actions d&#39;une société atteint une certaine valeur&quot;, etc.

## Remarques importantes

* Le schéma du événement doit contenir une Principale identité.
* Les événements d&#39;entreprise ne peuvent être ignorés que comme première étape d&#39;un parcours.
* Lorsque vous supprimez un événement d&#39;entreprise comme première étape d&#39;un parcours, le type de Planificateur du parcours est &quot;événement d&#39;entreprise&quot;.
* Seule une activité de segment en lecture peut être supprimée après un événement métier. Elle est automatiquement ajoutée comme étape suivante.
* Les événements métier ne peuvent pas être déclenchés plus fréquemment qu’une heure.
* Une fois qu’un événement métier est déclenché, l’exportation du segment de 15 minutes à une heure est retardée.
* Lors du test d&#39;un événement d&#39;entreprise, vous devez transmettre les paramètres du événement et l&#39;identifiant du profil de test qui va entrer le parcours dans le test. En outre, lorsque vous testez un parcours basé sur un événement d’entreprise, vous ne pouvez déclencher qu’une seule entrée de profil. Consultez [cette section](../building-journeys/testing-the-journey.md#test-business). En mode test, aucun mode &quot;vue de code&quot; n’est disponible.
* Qu&#39;advient-il des personnes qui se trouvent actuellement sur le parcours si un nouveau événement d&#39;entreprise arrive ? Il se comporte de la même manière que lorsque des individus sont toujours dans un parcours récurrent lorsqu&#39;une nouvelle répétition se produit. Leur chemin est terminé. En conséquence, les spécialistes du marketing doivent veiller à ne pas créer trop de parcours s&#39;ils s&#39;attendent à des événements d&#39;affaires fréquents.

## Commencer avec les événements métier

Voici les premières étapes de configuration d’un événement d’entreprise :

1. Dans le menu de gauche, cliquez sur l’icône **[!UICONTROL Administration]**, puis sur **[!UICONTROL Événements]**. La liste des événements s’affiche.

   ![](../assets/jo-event1.png)

1. Cliquez sur le bouton **[!UICONTROL Ajouter]** pour créer un événement. Le volet de configuration d’événement s’ouvre dans la partie droite de l’écran.

   ![](../assets/jo-event2.png)

1. Saisissez le nom de votre événement. Vous pouvez également ajouter une description.

   ![](../assets/jo-event3-business.png)

   >[!NOTE]
   >
   >N’utilisez ni espaces ni caractères spéciaux. Utilisez 30 caractères au maximum.

1. Dans le champ **[!UICONTROL Type]**, choisissez **Entreprise**.

   ![](../assets/jo-event3bis-business.png)

1. Le nombre de parcours qui font appel à cet événement apparaît dans le champ **[!UICONTROL Utilisé(e) dans]**. Vous pouvez cliquer sur l’icône **[!UICONTROL Afficher les parcours]** pour faire apparaître la liste des parcours utilisant cet événement.

1. Définissez les champs schéma et charge utile : c’est là que vous sélectionnez les informations de événement (généralement appelées données utiles) que les parcours attendent de recevoir. Vous pourrez alors utiliser ces informations dans votre parcours. Consultez [cette section](../event/about-creating-business.md#define-the-payload-fields).

   ![](../assets/jo-event5-business.png)

   Seuls les schémas de série chronologique sont disponibles. Les schémas des Événements d’expérience, des Événements de décision et des Événements d’étape de Parcours ne sont pas disponibles. Le schéma du événement doit contenir une Principale identité.

   ![](../assets/test-profiles-4.png)

1. Cliquez à l’intérieur du champ **[!UICONTROL Condition de l’identifiant d’événement]**. À l’aide de l’éditeur d’expression simple, définissez la condition qui sera utilisée par le système pour identifier les événements qui déclencheront votre parcours.
   ![](../assets/jo-event6-business.png)

   Dans notre exemple, nous avons écrit une condition basée sur l’identifiant du produit. Cela signifie que chaque fois que le système reçoit un événement correspondant à cette condition, il le transmet aux parcours.

1. Cliquez sur **[!UICONTROL Enregistrer]**.

   ![](../assets/journey7-business.png)

   L’événement est maintenant configuré et prêt à être déposé dans un parcours. Des étapes de configuration supplémentaires sont requises pour la réception d’événements. Voir [cette page](../event/additional-steps-to-send-events-to-journey-orchestration.md).

## Définition des champs de charge utile {#define-the-payload-fields}

La définition de la payload vous permet de choisir les informations que le système s’attend à recevoir de l’événement dans votre parcours, ainsi que la clé permettant d’identifier la personne associée à l’événement. La payload est basée sur la définition de champ XDM d’Experience Cloud. Pour plus d’informations sur XDM, consultez [cette page](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr).

1. Sélectionnez un schéma XDM dans la liste et cliquez ensuite sur le champ **[!UICONTROL Payload]** ou sur l’icône **[!UICONTROL Modifier]**.

   ![](../assets/journey8-business.png)

   Tous les champs définis dans le schéma sont affichés. La liste des champs varie d’un schéma à l’autre. Vous pouvez rechercher un champ spécifique, ou utiliser les filtres pour afficher l’ensemble des nœuds et des champs ou uniquement les champs sélectionnés. En fonction de la définition du schéma, certains champs peuvent être obligatoires et présélectionnés. Vous ne pouvez pas les désélectionner. Tous les champs obligatoires pour que le événement soit correctement reçu par les parcours sont sélectionnés par défaut.

   ![](../assets/journey9-business.png)

1. Sélectionnez les champs que vous prévoyez de recevoir de l’événement. Il s’agit des champs que l’utilisateur chargé de la conception de parcours exploitera dans le parcours.

   ![](../assets/journey10-business.png)

1. Une fois la sélection des champs nécessaires terminée, cliquez sur **[!UICONTROL Enregistrer]** ou appuyez sur la touche **[!UICONTROL Entrée]**.

   Le nombre de champs sélectionnés s’affiche dans le champ **[!UICONTROL Payload]**.

   ![](../assets/journey12-business.png)

## Prévisualisation de la charge utile {#preview-the-payload}

Cet aperçu vous permet de valider la définition de la payload.

1. Cliquez sur l’icône **[!UICONTROL Afficher la payload]** pour prévisualiser la payload attendue par le système.

   ![](../assets/journey13-business.png)

   Vous remarquerez que les champs sélectionnés sont affichés.

   ![](../assets/journey14-business.png)

1. Vérifiez l’aperçu pour valider la définition de la payload.

1. Vous pouvez ensuite partager l’aperçu de la payload avec la personne responsable de l’envoi de l’événement. Cette payload peut l’aider à concevoir la configuration d’un envoi d’événement vers [!DNL Journey Optimizer]. Voir [cette page](../event/additional-steps-to-send-events-to-journey-orchestration.md).
