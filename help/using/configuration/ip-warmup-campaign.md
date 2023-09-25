---
solution: Journey Optimizer
product: journey optimizer
title: Créer des campagnes de réchauffement des adresses IP
description: Découvrez comment créer une campagne de réchauffement des adresses IP
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
keywords: IP, pools, délivrabilité
hide: true
hidefromtoc: true
source-git-commit: b3e5a825b881736516b3bcd1d368843c3a601100
workflow-type: tm+mt
source-wordcount: '348'
ht-degree: 6%

---

# Créer des campagnes de réchauffement des adresses IP {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="Activez l’option Formule de chauffage par IP ."
>abstract="Lorsque vous sélectionnez cette option, la campagne peut être utilisée dans un forfait de chauffage par IP. Le planning de la campagne sera ensuite piloté par le plan de chaleur IP auquel il est associé."

>[!BEGINSHADEBOX]

Ce guide vous apportera la documentation suivante :

* [Prise en main du réchauffement des adresses IP](ip-warmup-gs.md)
* **[Créer des campagnes de réchauffement des adresses IP](ip-warmup-campaign.md)**
* [Créer une formule de chauffage des adresses IP](ip-warmup-plan.md)
* [Exécution de la formule de chauffage par IP](ip-warmup-execution.md)

>[!ENDSHADEBOX]

Avant de créer le plan de chauffage par IP dans [!DNL Journey Optimizer], vous devez d’abord créer une ou plusieurs campagnes avec l’option dédiée activée afin qu’elles puissent être utilisées dans un forfait de chaleur d’IP.

Pour créer une campagne de réchauffement des adresses IP, procédez comme suit.

1. Créez un [email](../email/email-settings.md) channel [surface](channel-surfaces.md) pour le domaine et les adresses IP que vous avez identifiées pour votre plan de chaleur.

   >[!NOTE]
   >
   >Découvrez comment sélectionner le domaine et les adresses IP à utiliser dans une surface d’email dans [cette section](../email/email-settings.md#subdomains-and-ip-pools).
   >
   >Contactez votre conseiller en délivrabilité pour identifier le domaine et les adresses IP à utiliser pour votre plan de chauffage des adresses IP.<!--TBC-->

1. Créez un [campaign](../campaigns/create-campaign.md) et sélectionnez la variable [Email](../email/create-email.md#create-email-journey-campaign) action.

1. Sélectionnez la surface que vous avez créée pour le réchauffement des adresses IP.

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Cliquez sur **[!UICONTROL Créer]**.

1. Dans la **[!UICONTROL Planification]** , sélectionnez **[!UICONTROL Activation du plan de chauffage par IP]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   La campagne [planning](../campaigns/create-campaign.md#schedule) sera piloté par le plan de chaleur IP auquel il sera associé, ce qui signifie que le planning n’est plus défini dans la campagne elle-même.

1. Suivez les étapes de création d’une campagne par e-mail, telles que la définition des propriétés de la campagne, [audience](../audience/about-audiences.md)<!--best practices for IP warmup in terms of audience?-->, et [content](../email/get-started-email-design.md#key-steps).

   >[!NOTE]
   >
   >Pour plus d’informations sur la configuration d’une campagne, consultez cette [page](../campaigns/get-started-with-campaigns.md).

1. [Activer](../campaigns/review-activate-campaign.md) la campagne.

   >[!NOTE]
   >
   >Pour une campagne en direct avec le plan de chauffage par IP activé, la variable **[!UICONTROL Supprimer]** est disponible jusqu’à ce qu’il soit associé à un plan de chauffage par IP. Une fois utilisée dans un plan, la campagne ne peut plus être supprimée.

1. La campagne s’affiche dans la variable **[!UICONTROL Campagnes]** liste. Pour récupérer facilement toutes les campagnes de chaleur d’IP créées sur l’environnement de test actuel, vous pouvez filtrer sur **[!UICONTROL Réchauffement des adresses IP]** option de campagne.

   ![](assets/ip-warmup-campaign-filter.png)

Une fois active, la campagne est prête à être utilisée dans un plan de chauffage par IP. [En savoir plus](ip-warmup-plan.md)

<!--Any recommendations when defining an audience? i.e do you have to include all your database or a limited number or according to your Excel file?-->

