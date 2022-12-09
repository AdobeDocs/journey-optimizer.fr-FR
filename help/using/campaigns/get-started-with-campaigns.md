---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main des campagnes
description: En savoir plus sur les campagnes dans [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '385'
ht-degree: 0%

---

# Prise en main des campagnes {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagnes"
>abstract="Créez des campagnes pour diffuser du contenu ponctuel sur un segment spécifique sur différents canaux. Avant de créer votre campagne, assurez-vous d’avoir une surface de canal (c’est-à-dire un paramètre prédéfini de message) et un segment Adobe Experience Platform prêt à l’emploi."

Utilisez les campagnes Journey Optimizer pour diffuser du contenu ponctuel sur un segment spécifique à l’aide de divers canaux. Lors de l’utilisation de parcours, les actions sont exécutées de manière séquentielle. Avec les campagnes, les actions sont exécutées simultanément, immédiatement ou selon un planning spécifié.

Vous pouvez créer deux types de campagnes :

* **Campagnes planifiées** autorisez des communications par lots ad hoc simples pour des cas d’utilisation marketing tels que des offres promotionnelles, des campagnes d’engagement, des annonces, des avis juridiques ou des mises à jour de stratégie.
* **Campagnes déclenchées par l’API** autorisez des messages transactionnels/opérationnels simples avec des API REST (réinitialisation de mot de passe, abandon de carte, etc.), où le besoin peut impliquer une personnalisation à l’aide d’attributs de profil et de données contextuelles issues de la payload.

Les étapes principales pour créer une opération sont les suivantes :

![](assets/create-campaign-process.png)

➡️ [Découvrez cette fonctionnalité en vidéo](#video)

## Avant de commencer {#campaign-prerequisites}

Vérifiez les conditions préalables suivantes avant de commencer la création de votre première campagne dans Journey Optimizer :

1. **Vous avez besoin d’autorisations appropriées**. Les campagnes ne sont disponibles que pour les utilisateurs ayant accès à une campagne associée **[!UICONTROL Product profile]** par exemple, administrateur de Campaign, approbateur de Campaign, responsable de Campaign et/ou visionneuse de Campaign.

   Si vous ne pouvez pas accéder aux campagnes, vos autorisations doivent être étendues. Si vous avez accès à [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;} pour votre organisation, procédez comme suit. Si ce n’est pas le cas, contactez votre administrateur Journey Optimizer.

   +++Découvrez comment attribuer des autorisations de campagne

   Pour affecter la variable **[!UICONTROL Product profile]** à vos utilisateurs :

   1. De [Adobe Admin Console](https://adminconsole.adobe.com/){target=&quot;_blank&quot;}, sélectionnez la variable [!DNL Adobe Experience Platform] produit.

   1. Accédez au **[!UICONTROL Product profile]** , sélectionnez l’une des campagnes intégrées liées **[!UICONTROL Product profile]**: Administrateur de Campaign, approbateur de Campaign, responsable de Campaign ou visionneuse de Campaign.

      Pour plus d’informations sur la campagne Journey Optimizer **[!UICONTROL Product profiles]** et **[!UICONTROL Permissions]**, [voir cette page](../administration/ootb-product-profiles.md).

      ![](assets/do-not-localize/admin_1.png)

   1. Cliquez sur **[!UICONTROL Add user]** pour affecter à votre utilisateur le **[!UICONTROL Product profile]**.

      ![](assets/do-not-localize/admin_2.png)

   1. Saisissez le nom, le groupe ou l’adresse électronique de votre utilisateur, puis cliquez sur **[!UICONTROL Save]**.
   Votre utilisateur peut désormais accéder à **[!UICONTROL Campaigns]**.

+++

1. **Vous avez besoin d’une audience**. Les segments d’audience doivent être disponibles avant de créer la campagne. En savoir plus sur la création d’audiences [dans cette page](../segment/about-segments.md).
1. **Vous avez besoin d’une surface de canal**. Pour pouvoir sélectionner un canal, la surface du canal correspondante (c’est-à-dire le paramètre prédéfini) doit être créée et disponible. En savoir plus sur les surfaces des canaux [dans cette page](../configuration/channel-surfaces.md).

## Vidéo pratique {#video}

Découvrez comment créer votre première campagne.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
