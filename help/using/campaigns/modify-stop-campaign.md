---
solution: Journey Optimizer
product: journey optimizer
title: Modifier ou arrêter une campagne
description: Découvrez comment modifier, arrêter ou dupliquer des campagnes dynamiques dans Journey Optimizer.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: gérer les campagnes, statut, planification, accès, optimizer
exl-id: 1b88c84e-9d92-4cc1-b9bf-27a2f1d29569
source-git-commit: 1ad534b7877f0ac6c1f50e29f41af708e83b34c9
workflow-type: tm+mt
source-wordcount: '868'
ht-degree: 66%

---

# Gestion des campagnes {#modify-stop-campaign}

Une fois qu’une campagne a été activée, vous pouvez la modifier ou l’arrêter à tout moment. Ces opérations sont disponibles pour les campagnes dont l’exécution est récurrente uniquement.

De plus, vous pouvez dupliquer des campagnes dynamiques (exécutées une fois ou de manière récurrente) pour en créer de nouvelles et archiver les campagnes terminées ou arrêtées.

## Accéder aux campagnes {#access}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_view"
>title="Vues Liste et Calendrier des campagnes"
>abstract="Outre la liste des campagnes, [!DNL Journey Optimizer] fournit une vue Calendrier de vos campagnes, ce qui apporte une représentation visuelle claire de leurs plannings. Vous pouvez basculer entre les vues Liste et Calendrier à tout moment à l’aide de ces boutons."

Les campagnes sont accessibles à partir du menu **[!UICONTROL Campagnes]**.

Par défaut, toutes les campagnes dont le statut est **[!UICONTROL Brouillon]**, **[!UICONTROL Planifié]** et **[!UICONTROL Actif]** sont répertoriées. Pour afficher les campagnes arrêtées, terminées et archivées, vous devez supprimer le filtre.

![](assets/create-campaign-list.png)

Vous pouvez également filtrer la liste en fonction du type et du canal de la campagne, ou des balises qui ont été affectées aux campagnes lors de leur création. [Découvrir comment attribuer des balises à une campagne](create-campaign.md#create)

## Calendrier des campagnes {#calendar}

Outre la liste des campagnes, [!DNL Journey Optimizer] fournit une vue Calendrier de vos campagnes, offrant une représentation visuelle claire de leurs plannings.

>[!AVAILABILITY]
>
>La vue Calendrier n’est actuellement disponible que pour un ensemble d’organisations (disponibilité limitée). Pour demander l’accès, utilisez [ce formulaire](https://forms.cloud.microsoft/r/FC49afuJVi){target=”_blank”}.
>
>Cette fonctionnalité est en développement actif. Vos commentaires et demandes sont les bienvenus à l’aide du bouton **[!UICONTROL Commentaires Beta]** situé dans le menu supérieur.

Le calendrier affiche toutes les campagnes planifiées pour la semaine en cours. Utilisez les boutons fléchés situés au-dessus du calendrier pour naviguer entre les semaines.

![vue calendrier affichant les campagnes actives](assets/campaigns-timeline.png)

Représentation des campagnes :

* Par défaut, la grille de calendrier affiche toutes les campagnes actives et planifiées pour la semaine sélectionnée. D’autres options de filtre peuvent afficher les activations terminées, arrêtées et terminées ou les activations d’un certain type ou d’un certain canal.
* Les brouillons de campagne ne s’affichent pas.
* Les campagnes s’étendant sur plusieurs jours s’affichent en haut de la grille du calendrier.
* Si aucune heure de début n’est spécifiée, l’heure d’activation manuelle la plus proche est utilisée pour la positionner dans le calendrier.
* Les campagnes s’affichent sous la forme de périodes d’une heure, mais cela ne reflète pas l’heure d’envoi ou d’achèvement réelle.

Pour plus d’informations sur une campagne, cliquez sur son bloc visuel afin d’afficher les détails correspondants.

Pour afficher les détails d’une campagne spécifique, sélectionnez-la dans la liste. Un volet d’informations s’ouvre avec diverses informations sur la campagne, telles que son type, l’accès aux rapports ou les balises qui ont été affectées.

![liste des campagnes avec le volet d’informations ouvert](assets/campaign-rail.png)

## Statuts et alertes des campagnes {#statuses}

Les campagnes peuvent avoir plusieurs statuts :

* **[!UICONTROL Brouillon]** : la campagne est en cours de modification et n’est pas active.
* **[!UICONTROL Activation]** : la campagne est en cours d’activation.
* **[!UICONTROL Traitement]** *(campagnes par e-mail uniquement)* : l’export de l’audience est terminé, la campagne est en cours de publication.
* **[!UICONTROL Actif]** : la campagne est active.
* **[!UICONTROL Planifié]** : la campagne a été configurée pour être activée à une date de début spécifique.
* **[!UICONTROL Arrêté]** : la campagne a été arrêtée manuellement. Vous ne pouvez plus l’activer ni la réutiliser. [Découvrez comment arrêter une campagne.](modify-stop-campaign.md#stop)
* **[!UICONTROL Terminé]** : la campagne est terminée. Ce statut est automatiquement attribué 3 jours après l’activation d’une campagne, ou à la date de fin de la campagne si son exécution est récurrente.
* **[!UICONTROL Archivé]** : la campagne a été archivée. [Découvrez comment archiver des campagnes.](modify-stop-campaign.md#archive)

>[!NOTE]
>
>L’icône « Ouvrir le brouillon » en regard d’un statut **[!UICONTROL Actif]** ou **[!UICONTROL Planifié]** indique qu’une nouvelle version de la campagne a été créée et n’a pas encore été activée. [En savoir plus](modify-stop-campaign.md#modify).

Lorsqu’une erreur se produit dans l’une de vos campagnes, une icône d’avertissement s’affiche avec le statut de la campagne. Cliquez dessus pour afficher les informations relatives à l’alerte. Ces alertes peuvent se produire dans différentes situations, par exemple lorsque le message de la campagne n’a pas été publié ou si la configuration choisie est incorrecte.

![](assets/campaign-alerts.png)

## Modification d’une campagne récurrente {#modify}

Pour modifier et créer une nouvelle version d’une campagne récurrente, procédez comme suit :

1. Ouvrez la campagne, puis cliquez sur le bouton **[!UICONTROL Modifier la campagne]**.

1. Une nouvelle version de la campagne est créée. Vous pouvez vérifier la version active en cliquant sur **[!UICONTROL Ouvrir la version active]**.

   ![](assets/create-campaign-draft.png)

   Dans la liste des campagnes, les campagnes activées avec un brouillon en cours s’affichent avec une icône spécifique dans la colonne **[!UICONTROL Statut]**. Cliquez sur cette icône pour ouvrir le brouillon de la campagne.

   ![](assets/create-campaign-edit-list.png)

1. Une fois vos modifications prêtes, vous pouvez activer la nouvelle version de la campagne (voir [Vérification et activation d’une campagne](create-campaign.md#review-activate)).

   >[!IMPORTANT]
   >
   >L’activation du brouillon remplacera la version active de la campagne.

## Arrêt d’une campagne récurrente {#stop}

Pour arrêter une campagne récurrente, ouvrez-la, puis cliquez sur le bouton **[!UICONTROL Arrêter la campagne]**.

![](assets/create-campaign-stop.png)

>[!IMPORTANT]
>
>L’arrêt d’une campagne n’arrête pas un envoi continu, mais elle arrête un envoi planifié ou les occurrences suivantes si l’envoi est déjà en cours.

<!-- inbound campaign (inapp): can stop and resume -->

## Duplication d’une campagne {#duplicate}

Vous pouvez dupliquer une campagne active pour en créer une nouvelle. Pour ce faire, ouvrez la campagne, puis cliquez sur **[!UICONTROL Dupliquer]**.

![](assets/create-campaign-duplicate.png)

## Archivage d’une campagne {#archive}

Avec le temps, la liste des campagnes ne cesse d’augmenter et il devient plus difficile de parcourir les campagnes terminées et arrêtées.

Pour éviter cela, vous pouvez archiver les campagnes terminées et arrêtées dont vous n’avez plus besoin. Pour ce faire, cliquez sur le bouton représentant des points de suspension, puis sélectionnez **[!UICONTROL Archiver]**.

![](assets/create-campaign-archive.png)

Les campagnes archivées peuvent ensuite être récupérées à l’aide du filtre dédié dans la liste. [Découvrez comment accéder à des campagnes](get-started-with-campaigns.md#access)
