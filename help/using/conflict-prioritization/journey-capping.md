---
title: Limitation et arbitrage des parcours
description: Découvrez comment créer des règles de limitation pour vos parcours et comment arbitrer une entrée de parcours.
role: User
level: Beginner
exl-id: 4c0ee178-81fb-41ae-b7f5-22da995e6fc6
source-git-commit: b8d56578aae90383092978446cb3614a4a033f80
workflow-type: tm+mt
source-wordcount: '944'
ht-degree: 100%

---

# Limitation et arbitrage des parcours {#journey-capping}

La limitation des parcours permet de limiter le nombre de parcours dans lesquels un profil peut être inscrit, ce qui évite la surcharge de communication. Dans Journey Optimizer, vous pouvez définir deux types de règles de limitation :

* La **limitation des entrées** limite le nombre d’entrées de parcours sur une période donnée pour un profil.
* La **limitation de simultanéité** limite le nombre de parcours dans lesquels un profil peut être inscrit simultanément.

Les deux types de limitation de parcours utilisent des scores de priorité pour arbitrer les entrées.

➡️ [Découvrez cette fonctionnalité en vidéo.](#video)

## Création d’une règle de limitation de parcours {#create-rule}

>[!CONTEXTUALHELP]
>id="ajo_rule_set_concurrency_prioritization"
>title="Avenir de la priorité"
>abstract=" Si un parcours de priorité plus élevée est planifié dans la période spécifiée ici, le client ou la cliente ne pourra pas entrer dans ce parcours. Dans les cas où vous souhaitez que les parcours soient accessibles sur la base du premier arrivé, premier servi, nous vous suggérons de choisir la période d’anticipation quotidienne et de vous assurer que le score de priorité de tout autre parcours ce jour-là est inférieur au score de priorité du parcours. Un score de priorité de 100 à un parcours garantirait également son accessibilité."

>[!CONTEXTUALHELP]
>id="ajo_rule_set_rule_type"
>title="Type de règle"
>abstract="Spécifiez le type de limitation de la règle. La **[!UICONTROL limite d’entrée dans le parcours]** limite le nombre d’entrées dans le parcours sur une période donnée pour un profil, tandis que la **[!UICONTROL limite de simultanéité du parcours]** limite le nombre de parcours auxquels un profil peut être inscrit simultanément."

Pour créer une règle de limitation de parcours, procédez comme suit :

1. Accédez au menu **[!UICONTROL Règles métier]** pour consulter l’inventaire des jeux de règles.

1. Sélectionnez le jeu de règles dans lequel vous souhaitez ajouter la règle de limitation ou créez un nouveau jeu de règles :

   * Pour utiliser un jeu de règles existant, sélectionnez-le dans la liste. Les règles de limitation de parcours ne peuvent être ajoutées qu’aux jeux de règles avec le domaine « parcours ». Vous pouvez vérifier ces informations dans les listes des jeux de règles, dans la colonne **[!UICONTROL Domaine]**.

     ![](assets/journey-capping-list.png)

   * Pour créer la règle de limitation dans un nouveau jeu de règles, cliquez sur **[!UICONTROL Créer un jeu de règles]**, spécifiez un nom unique pour le jeu de règles, sélectionnez « Parcours » dans la liste déroulante **[!UICONTROL Domaine du jeu de règles]**, puis cliquez sur **[!UICONTROL Enregistrer]**.

     ![](assets/journey-capping-rule-set.png)

1. Dans l’écran de définition des règles, cliquez sur le bouton **[!UICONTROL Ajouter une règle]**, puis attribuez un nom unique à la règle.

1. Dans la liste déroulante **[!UICONTROL Type de règle]**, spécifiez le type de limitation de la règle.

   * **[!UICONTROL Limite des entrées de parcours]** : limite le nombre d’entrées dans le parcours sur une période donnée pour un profil.
   * **[!UICONTROL Limite de simultanéité des parcours]** : limite le nombre de parcours dans lesquels un profil peut être inscrit simultanément.

   ![](assets/journey-capping-concurrency.png)

1. Développez les sections ci-dessous pour découvrir comment configurer chaque type de limitation :

   +++Configurer une règle de limitation d’entrée de parcours

   1. Dans le champ **[!UICONTROL Limitation]**, définissez le nombre maximal de parcours qu’un profil peut rejoindre.
   1. Dans le champ **[!UICONTROL Durée]**, définissez la période à prendre en compte. Veuillez noter que la durée est basée sur le fuseau horaire UTC. Par exemple, la limite quotidienne est réinitialisée à minuit UTC.

   Dans cet exemple, nous voulons limiter à 5 le nombre de parcours par mois que les profils peuvent rejoindre.

   ![](assets/journey-capping-entry-example.png)

   >[!NOTE]
   >
   >Le système prendra en compte la priorité des parcours planifiés à venir auxquels cette même règle est appliquée.
   >
   >Dans cet exemple, si la personne spécialiste marketing a déjà rejoint 4 parcours et qu’il y a un autre parcours planifié à venir ce mois-ci avec une priorité plus élevée, les personnes clientes seront alors supprimées de l’entrée au parcours de priorité plus faible.

   +++

   +++Configurer une règle de limitation de simultanéité de parcours 

   1. Dans le champ **[!UICONTROL Limitation]**, définissez le nombre maximal de parcours dans lesquels un profil peut être inscrit simultanément.

   1. Utilisez le champ **[!UICONTROL Durée de la priorité]** pour arbitrer les entrées de parcours en fonction des scores de priorité sur une période donnée (par exemple, 1 jour, 7 jours, 30 jours).

      Cette option analyse les parcours de lecture d’audience à venir planifiés pour le reste de la semaine afin de déterminer si le profil doit être supprimé de l’entrée dans le parcours en raison d’un parcours de priorité plus élevée à venir. Cela permet de donner la priorité à l’entrée dans des parcours à plus forte valeur si un profil est éligible à plusieurs parcours.

   Dans cet exemple, nous voulons empêcher les profils de rejoindre le parcours s’ils sont déjà inscrits dans un autre parcours contenant le même jeu de règles. Si un autre parcours dans les 7 jours à venir a un score de priorité plus élevé, le profil ne rejoint pas ce parcours.

   ![](assets/journey-capping-concurrency-example.png){width="50%" zommable="yes"}

   +++

1. Répétez les étapes ci-dessus pour ajouter autant de règles que nécessaire au jeu de règles.

1. Lorsque la règle de limitation est prête à être appliquée aux parcours, activez la règle et le jeu de règles auquel elle a été ajoutée. [Découvrir comment activer les jeux de règles](../conflict-prioritization/rule-sets.md#Create)

## Application de règles de limitation aux parcours {#apply-capping}

>[!CONTEXTUALHELP]
>id="ajo_journey_capping_rule"
>title="Appliquer un jeu de règles aux parcours"
>abstract="Appliquez un jeu de règles pour exclure ce parcours d’une partie de votre audience en fonction des règles de capping de la fréquence."

Pour appliquer une règle de limitation à un parcours, accédez au parcours et ouvrez ses propriétés. Dans la liste déroulante **[!UICONTROL Règles de limitation]**, sélectionnez le jeu de règles approprié. Une fois le parcours activé, les règles de limitation définies dans le jeu de règles prennent effet.

![](assets/journey-capping-apply.png)

>[!NOTE]
>
>Si un parcours est activé immédiatement, cela peut prendre jusqu’à 10 minutes pour que le système puisse commencer à supprimer la clientèle. Par conséquent, un message s’affiche si vous tentez de publier un parcours avec une heure de début inférieure à dix minutes.

## Surveiller les exclusions de jeux de règles {#monitor}

Une fois un parcours actif, vous pouvez vérifier dans le rapport de parcours si le jeu de règles a entraîné des exclusions du parcours, dans le tableau **[!UICONTROL Exclusions du parcours]**. Le tableau Exclusions du parcours comprend des répartitions détaillées des exclusions par jeu de règles et nom de règle, ce qui permet de comprendre pourquoi certains profils ont été écartés. [Découvrir comment utiliser les rapports de parcours](../reports/journey-global-report-cja.md)

![](assets/journey-report.png)

En outre, vous pouvez également utiliser le [service de requête Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/query/api/getting-started.html?lang=fr){target="_blank"} pour créer des requêtes permettant d’identifier quelle règle a empêché un profil de rejoindre un parcours donné. Un exemple de requête est disponible dans [cette section](../reports/query-examples.md#common-queries).

## Vidéo pratique {#video}

>[!VIDEO](https://video.tv.adobe.com/v/3435530?quality=12)
