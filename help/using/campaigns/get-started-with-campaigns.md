---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec les campagnes
description: Apprenez en plus sur les campagnes dans Journey Optimizer.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
keywords: campagne, guide, commencer, optimizer
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: d4ecfecdc74c26890658d68d352c36b75f7c9039
workflow-type: tm+mt
source-wordcount: '467'
ht-degree: 100%

---

# Commencer avec les campagnes {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card3"
>title="Créer des campagnes"
>abstract="Utilisez **Adobe Journey Optimizer** pour diffuser du contenu ponctuel sur une audience spécifique à l’aide de divers canaux. Lors de l’utilisation de parcours, les actions sont exécutées à la suite. Avec les campagnes, les actions sont exécutées simultanément, immédiatement ou selon un planning spécifié."


>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagnes"
>abstract="Créez des campagnes pour diffuser du contenu ponctuel à une audience spécifique sur différents canaux. Avant de créer une campagne, assurez-vous de disposer d’une surface de canal (c’est-à-dire un préréglage de message) et d’une audience Adobe Experience Platform prête à l’emploi."

Utilisez les campagnes de Journey Optimizer pour diffuser du contenu ponctuel sur une audience spécifique à l’aide de divers canaux. Lors de l’utilisation de parcours, les actions sont exécutées à la suite. Avec les campagnes, les actions sont exécutées simultanément, immédiatement ou selon un planning spécifié.

Vous pouvez créer deux types de campagnes :

* **Les campagnes planifiées** permettent des communications par lots ad hoc simples pour des cas d’utilisation marketing tels que des offres promotionnelles, des campagnes d’engagement, des avis juridiques ou des mises à jour de politique.
* Les **campagnes déclenchées par API** visent à permettre aux communications marketing d’atteindre une audience au moment opportun ou aux messages transactionnels/opérationnels d’être envoyés à une personne, comme la réinitialisation d’un mot de passe. La personnalisation de ces campagnes inclut l’attribut de profil, mais aussi les données contextuelles en temps réel dans le déclencheur, qui est une payload de l’API REST.

Suivez les étapes de création dʼune campagne décrites ci-après :

![](assets/create-campaign-process.png)

➡️ [Découvrez cette fonctionnalité en vidéo](#video)

## Avant de commencer {#campaign-prerequisites}

Vérifiez les conditions préalables suivantes avant de commencer la création de votre première campagne dans Journey Optimizer :

1. **Il vous faut les autorisations appropriées**. Les campagnes ne sont disponibles que pour les utilisateurs ayant accès à un **[!UICONTROL profil de produit]** associé à une campagne, tels que l’administrateur de la campagne, l’approbateur de la campagne, le responsable de la campagne et/ou l’observateur de la campagne.

   Si vous ne pouvez pas accéder aux campagnes, vos autorisations doivent être étendues. Si vous avez accès à [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"} pour votre organisation, procédez comme suit. Si ce n’est pas le cas, contactez votre administrateur Journey Optimizer.

   +++Découvrez comment attribuer des autorisations de campagne

   Pour attribuer le **[!UICONTROL profil de produit]** correspondant à vos utilisateurs :

   1. Depuis [Adobe Admin Console](https://adminconsole.adobe.com/){target="_blank"}, sélectionnez le produit [!DNL Adobe Experience Platform].

   1. Accédez à l’onglet **[!UICONTROL Profil de produit]** , sélectionnez l’un des **[!UICONTROL profils de produit]** intégrés liés à la campagne : l’administrateur de la campagne, l’approbateur de la campagne, le responsable de la campagne ou l’observateur de la campagne.

      Pour plus d’informations sur les **[!UICONTROL Profils de produit]** et **[!UICONTROL Autorisations]** de la campagne Journey Optimizer, [consultez cette page](../administration/ootb-product-profiles.md).

      ![](assets/do-not-localize/admin_1.png)

   1. Cliquez sur **[!UICONTROL Ajouter un utilisateur]** pour attribuer à votre utilisateur le **[!UICONTROL profil de produit]** sélectionné.

      ![](assets/do-not-localize/admin_2.png)

   1. Saisissez le nom, le groupe ou l’adresse e-mail de votre utilisateur, puis cliquez sur **[!UICONTROL Enregistrer]**.

   Votre utilisateur peut désormais accéder aux **[!UICONTROL Campagnes]**.

+++

1. **Vous avez besoin d’une audience**. Les audiences doivent être disponibles avant de créer la campagne. Pour en savoir plus sur les audiences, consultez [cette page](../audience/about-audiences.md).
1. **Vous avez besoin d’une surface de canal**. Pour pouvoir sélectionner un canal, la surface de canal correspondante (c’est-à-dire le préréglage) doit être créée et disponible. Pour en savoir plus sur les surface de canal, consultez cette [page](../configuration/channel-surfaces.md).

## Vidéo pratique {#video}

Découvrez comment créer votre première campagne.

>[!VIDEO](https://video.tv.adobe.com/v/346680?quality=12)
