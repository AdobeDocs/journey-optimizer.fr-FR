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
source-git-commit: 3be1b238962fa5d0e2f47b64f6fa5ab4337272a5
workflow-type: tm+mt
source-wordcount: '620'
ht-degree: 69%

---

# Commencer avec les campagnes {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule"
>title="Planning de la campagne"
>abstract="Par défaut, les campagnes démarrent via une activation manuelle et se terminent immédiatement après un seul envoi du message. Vous avez la possibilité de définir une date et une heure spécifiques pour l’envoi du message. De plus, vous pouvez spécifier une date de fin pour les campagnes d’action récurrentes. Dans les déclencheurs d’action, vous pouvez également configurer la fréquence d’envoi des messages en fonction de vos préférences."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_start"
>title="Début de campagne"
>abstract="Indiquez la date et l’heure auxquelles le message doit être envoyé."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_end"
>title="Fin de campagne"
>abstract="Indiquez à quel moment une campagne récurrente doit cesser d’être exécutée."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_schedule_triggers"
>title="Déclencheurs d’action de campagne"
>abstract="Vous pouvez définir la fréquence d’envoi du message de la campagne."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_throttling"
>title="Contrôle du taux de ralentissement"
>abstract="Contrôle du taux de ralentissement"

>[!CONTEXTUALHELP]
>id="ajo_homepage_card3"
>title="Créer des campagnes"
>abstract="Utilisez **Adobe Journey Optimizer** pour diffuser du contenu ponctuel sur une audience spécifique à l’aide de divers canaux. Lors de l’utilisation de parcours, les actions sont exécutées à la suite. Avec les campagnes, les actions sont exécutées simultanément, immédiatement ou selon un planning spécifié."

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagnes"
>abstract="Créez des campagnes pour diffuser du contenu ponctuel à une audience spécifique sur différents canaux. Avant de créer votre campagne, assurez-vous de disposer d’une configuration de canal et d’une audience Adobe Experience Platform prête à l’emploi."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_campaign_type"
>title="Type de campagne"
>abstract="Les **campagnes planifiées** sont exécutées immédiatement ou à une date spécifiée et sont destinées à envoyer des messages de type marketing. Les campagnes **déclenchées par API** sont exécutées à l’aide d’un appel API. Elles sont destinées à envoyer soit des messages marketing (messages promotionnels nécessitant le consentement de la personne), soit des messages transactionnels (messages non commerciaux, qui peuvent également être envoyés à des profils désabonnés dans des contextes spécifiques)."

Utilisez les campagnes de Journey Optimizer pour diffuser du contenu ponctuel sur une audience spécifique à l’aide de divers canaux. Lors de l’utilisation de parcours, les actions sont exécutées à la suite. Avec les campagnes, les actions sont exécutées simultanément, immédiatement ou selon un planning spécifié.

![](assets/gs-campaigns.png)

Vous pouvez créer différents types de campagnes dans Journey Optimizer :

* **Campagnes d’action**

  Les campagnes d’action (ou campagnes planifiées) permettent des communications par lots ad hoc simples pour des cas d’utilisation marketing tels que des offres promotionnelles, des campagnes d’engagement, des annonces, des informations juridiques ou des mises à jour de politiques.

* **Campagnes déclenchées par l’API**

  Les campagnes déclenchées par API permettent aux communications marketing d’atteindre une audience au bon moment ou aux messages transactionnels/opérationnels d’être envoyés à une personne, comme la réinitialisation d’un mot de passe. La personnalisation de ces campagnes inclut l’attribut de profil, mais aussi les données contextuelles en temps réel dans le déclencheur, qui est une payload de l’API REST.

<!--* **Orchestrated campaigns**

    Campaign Orchestration in Adobe Journey Optimizer powers sophisticated, brand-initiated marketing campaigns across channels, helping you drive engagement, revenue, and customer loyalty at scale.

    While cross-channel marketing is essential, Orchestrated campaigns make it seamless. With a visual, drag-and-drop interface, you can design and automate complex marketing workflows, from segmentation to message delivery, across multiple channels. Everything happens in one intuitive environment, built for speed, control, and efficiency.-->

## Avant de commencer {#campaign-prerequisites}

Vérifiez les conditions préalables suivantes avant de commencer à créer votre première campagne dans [!DNL Journey Optimizer] :

1. **Il vous faut les autorisations appropriées**. Les campagnes ne sont disponibles que pour les utilisateurs ayant accès à une campagne liée **[!UICONTROL profil de produit]** telle que l’administrateur de la campagne, l’approbateur de la campagne, le responsable de la campagne et/ou l’observateur de la campagne. Si vous ne pouvez pas accéder aux campagnes, vos autorisations doivent être étendues.

   +++Découvrir comment attribuer un rôle lié à la campagne

   1. Pour attribuer un rôle à un utilisateur ou une utilisatrice dans le produit [!DNL Permissions], accédez à l’onglet **[!UICONTROL Rôles]** et sélectionnez l’un des **[!UICONTROL Rôles]** liés à la campagne intégrés : administrateur ou administratrice de campagne, approbateur ou approbatrice de campagne, personne responsable de la gestion de campagne, ou observateur ou observatrice de campagne.

   1. Dans l’onglet **[!UICONTROL Utilisateurs]**, cliquez sur **[!UICONTROL Ajouter un utilisateur]**.

   1. Saisissez le nom ou l’adresse e-mail de votre utilisateur ou utilisatrice, ou sélectionnez l’utilisateur ou l’utilisatrice dans la liste, puis cliquez sur **[!UICONTROL Enregistrer]**.

      Si le profil de l’utilisateur ou de l’utilisatrice n’a pas été créé auparavant, consultez la [documentation relative à l’ajout d’utilisateurs et d’utilisatrices](https://experienceleague.adobe.com/fr/docs/experience-platform/access-control/ui/users).

   La personne doit alors recevoir un e-mail la redirigeant vers votre instance.

+++

1. **Vous avez besoin d’une audience**. Les audiences doivent être disponibles avant de créer la campagne. [Prise en main des audiences](../audience/about-audiences.md).

1. **Il vous faut une configuration de canal**. Pour pouvoir sélectionner un canal, la configuration de canal correspondante (c’est-à-dire le paramètre prédéfini) doit être créée et disponible. [Découvrez comment configurer les canaux](../configuration/channel-surfaces.md).

## Explorons plus en détail

Maintenant que vous connaissez les campagnes dans [!DNL Journey Optimizer], il est temps d’examiner plus en détail ces sections de documentation pour commencer à créer vos premières campagnes.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img alt="campagnes d’action" src="assets/do-not-localize/gs-action-campaign.png" width="50%"></a><br/><a href="create-campaign.md">Campagnes d’action</a></td>
<td><a href="api-triggered-campaigns.md"><img alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png" width="50%"></a><br/><a href="api-triggered-campaigns.md">Campagnes déclenchées par l’API</a></td>
</tr></table>

<!--
<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img alt="action campaigns" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Action campaigns</a></td>
<td><a href="api-triggered-campaigns.md"><img alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">API triggered campaigns</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img alt="push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Orchestrated campaigns</a></td>
</tr></table>-->
