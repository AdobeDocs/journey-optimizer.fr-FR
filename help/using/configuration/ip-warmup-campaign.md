---
solution: Journey Optimizer
product: journey optimizer
title: Créer des campagnes de réchauffement des adresses IP
description: Découvrez comment créer une campagne de réchauffement des adresses IP
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, pools, groupes, sous-domaines, délivrabilité
hide: true
hidefromtoc: true
source-git-commit: ea86d44f7c9309ff69877e01cea6a13e7907a039
workflow-type: tm+mt
source-wordcount: '251'
ht-degree: 8%

---

# Créer des campagnes de réchauffement des adresses IP {#create-ip-warmup-campaign}

>[!CONTEXTUALHELP]
>id="ajo_campaign_ip_warmup"
>title="Activez l’option Formule de chauffage par IP ."
>abstract="Sélectionnez l’option d’activation du plan de chaleur IP. Une fois la campagne activée, elle peut être associée à un plan de chauffage par IP."

>[!BEGINSHADEBOX]

Ce guide vous apportera la documentation suivante :

* [Prise en main du réchauffement des adresses IP](ip-warmup-gs.md)
* **[Créer des campagnes de réchauffement des adresses IP](ip-warmup-campaign.md)**
* [Créer une formule de chauffage des adresses IP](ip-warmup-plan.md)
* [Exécution de la formule de chauffage des adresses IP](ip-warmup-running.md)

>[!ENDSHADEBOX]

Vous devez créer une ou plusieurs campagnes avec une option spécifique activée afin qu’elles puissent être utilisées dans un plan de réchauffement des adresses IP.

Pour créer une campagne de réchauffement des adresses IP, procédez comme suit.

1. Créer un email [surface](channel-surfaces.md) pour le domaine et les adresses IP que vous avez identifiées pour votre plan de chaleur.<!--how do you identify these or who does it at the customer level?-->

   >[!NOTE]
   >
   >Découvrez comment sélectionner le domaine et les adresses IP à utiliser dans une surface d’email dans [cette section](../email/email-settings.md#subdomains-and-ip-pools).

1. Créez un [campaign](../campaigns/create-campaign.md) et sélectionnez la variable [Email](../email/create-email.md#create-email-journey-campaign) action.

1. Sélectionnez la surface que vous avez créée pour le réchauffement des adresses IP.

   ![](assets/ip-warmup-campaign-surface.png)

   <!--You must use the same surface as the one that will be used for the asociated IP warmup plan. [Learn how to create an IP warmup plan](#create-ip-warmup-plan)-->

1. Cliquez sur **[!UICONTROL Créer]**.

1. Dans la **[!UICONTROL Planification]** , sélectionnez **[!UICONTROL Activation du plan de chauffage par IP]**.

   ![](assets/ip-warmup-campaign-plan-activation.png)

   La campagne [planning](../campaigns/create-campaign.md#schedule) sera piloté par la variable [formule de chauffage par IP](ip-warmup-plan.md) il sera associé à , ce qui signifie que le planning n&#39;est plus défini dans l&#39;opération elle-même.

1. [Activer](../campaigns/review-activate-campaign.md) la campagne. Une fois en ligne, elle est prête à être utilisée dans un plan de chauffage par IP.

>[!NOTE]
>
>Pour une campagne en direct avec le plan de chauffage par IP activé, la variable **[!UICONTROL Supprimer]** est disponible jusqu’à ce qu’il soit associé à un plan de chauffage par IP.

Pour plus d’informations sur la configuration d’une campagne, consultez cette [page](../campaigns/get-started-with-campaigns.md).

<!--Any recommendations when defining an audience? i.e do you have to include all your database or a limited number or according to your Excel file?-->
