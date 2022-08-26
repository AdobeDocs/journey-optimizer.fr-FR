---
title: Prise en main des campagnes
description: En savoir plus sur les campagnes dans [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 8d8586a6c70b6fc01dbd1c2a8833079f422c93f7
workflow-type: tm+mt
source-wordcount: '403'
ht-degree: 59%

---

# Prise en main des campagnes {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagnes"
>abstract="Les campagnes vous permettent de diffuser un contenu unique à un segment spécifique, et ce sur plusieurs canaux. Avant de créer une campagne, assurez-vous de disposer d’une surface de canal (c’est-à-dire un préréglage de message) et d’un segment Adobe Experience Platform prêt à l’emploi."

## À propos des campagnes {#about}

Les campagnes vous permettent de diffuser un contenu unique à un segment spécifique sur plusieurs canaux. À la différence des parcours, où les actions sont conçues pour être exécutées l’une après l’autre, les campagnes exécutent des actions simultanément, immédiatement ou selon un planning précis.

Cela vous permet d’envoyer des communications par lots ad hoc simples pour des cas d’utilisation marketing tels que des offres promotionnelles, des campagnes d’engagement, des annonces, des avis juridiques ou des mises à jour de stratégie.

➡️ [Découvrez cette fonctionnalité en vidéo](#video)

<!--You can create two types of campaigns:

* **Scheduled campaigns** allow for simple ad-hoc batch communications for marketing use cases like promotional offers, engagement campaigns, announcements, legal notices, or policy updates.
* **API Triggered Campaigns** allow for simple transactional/operational messages with REST APIs (password reset, card abandonment, etc.), where the need may involve personalization using profile attributes and contextual data from payload.-->

## Conditions préalables {#campaign-prerequisites}

Campaign n&#39;est disponible que pour les utilisateurs ayant accès à une campagne associée **[!UICONTROL Profil de produit]** par exemple, administrateur de Campaign, approbateur de Campaign, responsable de Campaign et/ou visionneuse de Campaign.

Pour affecter la variable **[!UICONTROL Profil de produit]** à vos utilisateurs :

1. Dans la [!DNL Admin console], sélectionnez la variable [!DNL Adobe Experience Platform] produit.

1. Dans la **[!UICONTROL Profil de produit]** , sélectionnez l’un des onglets intégrés de Campaign **[!UICONTROL Profil de produit]**: Administrateur de Campaign, approbateur de Campaign, responsable de Campaign ou visionneuse de Campaign.

   Pour plus d’informations sur Campaign **[!UICONTROL Profils de produit]** et **[!UICONTROL Autorisations]**, voir à ce sujet [page](../administration/ootb-product-profiles.md).

   ![](assets/do-not-localize/admin_1.png)

1. Cliquez sur **[!UICONTROL Ajouter un utilisateur]** pour affecter à votre utilisateur le **[!UICONTROL Profil de produit]**.

   ![](assets/do-not-localize/admin_2.png)

1. Saisissez le nom, le groupe ou l’adresse électronique de votre utilisateur, puis cliquez sur **[!UICONTROL Enregistrer]**.

Votre utilisateur pourra désormais accéder à **[!UICONTROL Campagnes]**.

## Accès aux campagnes {#access}

Les campagnes sont accessibles à partir du menu **[!UICONTROL Campagnes]**.

Par défaut, toutes les campagnes dont le statut est **[!UICONTROL Brouillon]**, **[!UICONTROL Planifié]** et **[!UICONTROL Actif]** sont répertoriées. Pour afficher les campagnes arrêtées, terminées et archivées, vous devez supprimer le filtre.

![](assets/create-campaign-list.png)

## Statuts des campagnes {#statuses}

Les campagnes peuvent avoir plusieurs statuts :

* **[!UICONTROL Brouillon]** : la campagne est en cours de modification et n’est pas active.
* **[!UICONTROL Activation]** : la campagne est en cours d’activation.
* **[!UICONTROL Actif]** : la campagne est active.
* **[!UICONTROL Planifié]** : la campagne a été configurée pour être activée à une date spécifique.
* **[!UICONTROL Arrêté]** : la campagne a été arrêtée manuellement. Vous ne pouvez plus l’activer ou la réutiliser (consultez la section [Arrêter une campagne](modify-stop-campaign.md#stop)).
* **[!UICONTROL Terminé]** : la campagne est terminée. Ce statut est automatiquement attribué 3 jours après l&#39;activation d&#39;une campagne, ou à la date de fin de la campagne si son exécution est récurrente.
* **[!UICONTROL Archivé]** : la campagne a été archivée.

>[!NOTE]
>
>L’icône « Ouvrir le brouillon » en regard d’un statut **[!UICONTROL Actif]** ou **[!UICONTROL Planifié]** indique qu’une nouvelle version de la campagne a été créée et n’a pas encore été activée (consultez la section [Modifier une campagne](modify-stop-campaign.md#modify)).

## Vidéo pratique {#video}

Découvrez comment créer votre première campagne.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
