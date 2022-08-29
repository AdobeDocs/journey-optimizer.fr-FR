---
title: Prise en main des campagnes
description: En savoir plus sur les campagnes dans [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: d747cc9a4d065ea9110cb8065c113326959e2a41
workflow-type: tm+mt
source-wordcount: '518'
ht-degree: 32%

---

# Prise en main des campagnes {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagnes"
>abstract="Créez des campagnes pour diffuser du contenu ponctuel sur un segment spécifique sur différents canaux. Avant de créer votre campagne, assurez-vous d’avoir une surface de canal (c’est-à-dire un paramètre prédéfini de message) et un segment Adobe Experience Platform prêt à l’emploi."

Utilisez les campagnes Journey Optimizer pour diffuser du contenu ponctuel sur un segment spécifique à l’aide de divers canaux. Lors de l’utilisation de parcours, les actions sont conçues pour être exécutées en séquence. Avec les campagnes, les actions sont exécutées simultanément, immédiatement ou selon un planning spécifié.

Créez des campagnes pour envoyer des communications par lots ad hoc simples pour des cas d’utilisation marketing tels que des offres promotionnelles, des campagnes d’engagement, des annonces, des avis juridiques ou des mises à jour de stratégie.

➡️ [Découvrez cette fonctionnalité en vidéo](#video)

<!--You can create two types of campaigns:

* **Scheduled campaigns** allow for simple ad-hoc batch communications for marketing use cases like promotional offers, engagement campaigns, announcements, legal notices, or policy updates.
* **API Triggered Campaigns** allow for simple transactional/operational messages with REST APIs (password reset, card abandonment, etc.), where the need may involve personalization using profile attributes and contextual data from payload.-->

## Avant de commencer {#campaign-prerequisites}

Vérifiez les conditions préalables suivantes avant de commencer la création de votre première campagne dans Journey Optimizer :

1. **Vous avez besoin d’autorisations appropriées**. Les campagnes ne sont disponibles que pour les utilisateurs ayant accès à une campagne associée **[!UICONTROL Profil de produit]** par exemple, administrateur de Campaign, approbateur de Campaign, responsable de Campaign et/ou visionneuse de Campaign. Si vous ne pouvez pas accéder aux campagnes, vos autorisations doivent être étendues. Si vous avez accès à [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;} pour votre organisation, procédez comme suit. Si ce n’est pas le cas, contactez votre administrateur Journey Optimizer.

+++Découvrez comment attribuer des autorisations de campagne

Pour affecter la variable **[!UICONTROL Profil de produit]** à vos utilisateurs :

1. Dans la [!DNL Admin console], sélectionnez la variable [!DNL Adobe Experience Platform] produit.

1. Dans la **[!UICONTROL Profil de produit]** , sélectionnez l’un des onglets intégrés de Campaign **[!UICONTROL Profil de produit]**: Administrateur de Campaign, approbateur de Campaign, responsable de Campaign ou visionneuse de Campaign.

   Pour plus d’informations sur la campagne Journey Optimizer **[!UICONTROL Profils de produit]** et **[!UICONTROL Autorisations]**, [voir cette page](../administration/ootb-product-profiles.md).

   ![](assets/do-not-localize/admin_1.png)

1. Cliquez sur **[!UICONTROL Ajouter un utilisateur]** pour affecter à votre utilisateur le **[!UICONTROL Profil de produit]**.

   ![](assets/do-not-localize/admin_2.png)

1. Saisissez le nom, le groupe ou l’adresse électronique de votre utilisateur, puis cliquez sur **[!UICONTROL Enregistrer]**.

Votre utilisateur pourra désormais accéder à **[!UICONTROL Campagnes]**.

+++

1. **Vous avez besoin d’une audience**. Les segments d’audience doivent être disponibles avant de créer la campagne. En savoir plus sur la création d’audiences [dans cette page](../segment/about-segments.md).
1. **Vous avez besoin d’une surface de canal**. Pour pouvoir sélectionner un canal, la surface correspondante doit être créée et disponible. En savoir plus sur les surfaces des canaux (c’est-à-dire les paramètres prédéfinis) [dans cette page](../configuration/channel-surfaces.md)

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
