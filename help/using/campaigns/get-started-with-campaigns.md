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
source-git-commit: 4bd3e202935cfc971990faa7d1dd2f3d0d7cdc6d
workflow-type: tm+mt
source-wordcount: '879'
ht-degree: 100%

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
>title="Contrôle des taux"
>abstract="Définissez le contrôle des taux pour votre campagne en spécifiant les limites de taux souhaitées. Cette fonctionnalité est particulièrement utile pour éviter la surcharge sur les systèmes en aval, tels que les pages de destination ou les plateformes d’assistance clientèle."

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
>abstract="Sélectionnez le type de la campagne. Les canaux disponibles varient en fonction du type sélectionné. <br>**Campagnes planifiées** (campagnes d’action) : idéales pour les communications par lots, simples et ponctuelles, que vous pouvez planifier pour qu’elles s’exécutent à une heure spécifique.<br>**Campagnes déclenchées par API** : activées par le biais d’un appel API, elles permettent d’envoyer des messages automatisés et basés sur un événement, directement depuis des systèmes externes.<br>**Campagnes orchestrées** : fournissent une zone de travail visuelle par glisser-déposer pour concevoir et automatiser des workflows marketing complexes et à plusieurs étapes, depuis la segmentation d’audience jusqu’à la diffusion de messages personnalisés sur plusieurs canaux."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_orchestration"
>title="Campagnes"
>abstract="Créez votre flux de segmentation, concevez vos messages cross-canal et planifiez vos campagnes. Canaux pris en charge : e-mail, SMS, notification push."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_marketing"
>title="Campagnes"
>abstract="Effectuez des diffusions sortantes uniques ou récurrentes ou des actions entrantes continues."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_scheduled_transactional"
>title="Campagnes"
>abstract="Envoyez des actions transactionnelles sortantes uniques ou récurrentes."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_marketing"
>title="Campagnes"
>abstract="Diffusez des communications marketing personnalisées aux audiences ciblées. Canaux pris en charge : e-mail, SMS, notifications push."

>[!CONTEXTUALHELP]
>id="ajo_campaigns_create_api_transactional"
>title="Campagnes"
>abstract="Diffusez des communications transactionnelles à des profils individuels ou à des ensembles de profils. Canaux pris en charge : e-mail, SMS, notifications push."

Utilisez les campagnes de Journey Optimizer pour diffuser du contenu ponctuel sur une audience spécifique à l’aide de divers canaux. Lors de l’utilisation de parcours, les actions sont exécutées à la suite. Avec les campagnes, les actions sont exécutées simultanément, immédiatement ou selon un planning spécifié.

![](assets/gs-campaigns.png)

Vous pouvez créer différents types de campagnes dans Journey Optimizer. Les canaux pris en charge et les cas d’utilisation varient en fonction du type de campagne. Ces types sont répertoriés ci-dessous.

* **Campagnes d’action**

  Les campagnes d’action (ou campagnes planifiées) permettent des communications par lots ad hoc simples pour des cas d’utilisation marketing tels que des offres promotionnelles, des campagnes d’engagement, des annonces, des mentions légales ou des mises à jour de politiques. Pour en savoir plus sur les fonctionnalités des campagnes d’action, les cas d’utilisation et les canaux pris en charge, consultez [cette page](create-campaign.md).

* **Campagnes déclenchées par API**

  Les campagnes déclenchées par API permettent aux communications marketing d’atteindre une audience au moment opportun ou aux messages transactionnels/opérationnels (comme la réinitialisation d’un mot de passe) d’être envoyés à un individu. Elles sont utilisées quand une personnalisation de ces campagnes est nécessaire en utilisant non seulement l’attribut de profil, mais aussi les données contextuelles en temps réel du déclencheur, qui est une payload d’API REST. Pour en savoir plus sur les fonctionnalités des campagnes déclenchées par API, les cas d’utilisation et les canaux pris en charge, consultez [cette page](api-triggered-campaigns.md).

* **Campagnes orchestrées**

  L’orchestration de campagne dans Adobe Journey Optimizer alimente des campagnes marketing sophistiquées et lancées par la marque sur l’ensemble des canaux, ce qui permet de renforcer l’engagement, le chiffre d’affaires et la fidélisation de la clientèle à grande échelle.

  Bien que le marketing cross-canal soit essentiel, les campagnes orchestrées le rendent transparent. Grâce à une interface visuelle par glisser-déposer, vous pouvez concevoir et automatiser des workflows marketing complexes, depuis la segmentation jusqu’à la diffusion des messages, sur plusieurs canaux. Tout se passe dans un environnement intuitif, conçu pour assurer vitesse, contrôle et efficacité. Pour en savoir plus sur les fonctionnalités des campagnes orchestrées, les cas d’utilisation et les canaux pris en charge, consultez [cette page](../orchestrated/gs-orchestrated-campaigns.md).

## Conditions préalables {#prerequisites}

Avant de créer votre campagne, vérifiez que vous avez examiné les conditions préalables ci-après.

### Autorisations

Les campagnes ne sont disponibles que pour les utilisateurs et utilisatrices disposant des autorisations appropriées répertoriées ci-dessous. [En savoir plus sur les rôles intégrés de Journey Optimizer](../administration/ootb-product-profiles.md)

>[!BEGINTABS]

>[!TAB Campagnes d’action]

Administrateur ou administratrice de Campaign
Approbateur ou approbatrice de Campagin
Responsable de Campaign
Observateur ou observatrice de Campaign

>[!TAB Campagnes déclenchées par API]

Administrateur ou administratrice de Campaign
Approbateur ou approbatrice de Campagin
Responsable de Campaign
Observateur ou observatrice de Campaign

>[!TAB Campagnes orchestrées]

Administrateur ou administratrice de campagnes orchestrées
Approbateur ou approbatrice de campagnes orchestrées
Responsable de campagnes orchestrées
Observateur ou observatrice de campagnes orchestrées

>[!ENDTABS]

Si vous ne parvenez pas à accéder aux fonctionnalités des campagnes, contactez votre équipe d’administration pour demander les autorisations nécessaires.

+++Découvrir comment attribuer un rôle lié à la campagne

1. Pour attribuer un rôle à un utilisateur ou une utilisatrice dans le produit [!DNL Permissions], accédez à l’onglet **[!UICONTROL Rôles]** et sélectionnez l’un des **[!UICONTROL Rôles]** liés à la campagne intégrée précisés ci-dessous.

1. Dans l’onglet **[!UICONTROL Utilisateurs]**, cliquez sur **[!UICONTROL Ajouter un utilisateur]**.

1. Saisissez le nom ou l’adresse e-mail de votre utilisateur ou utilisatrice, ou sélectionnez l’utilisateur ou l’utilisatrice dans la liste, puis cliquez sur **[!UICONTROL Enregistrer]**.

   Si le profil de l’utilisateur ou de l’utilisatrice n’a pas été créé auparavant, consultez la [documentation relative à l’ajout d’utilisateurs et d’utilisatrices](https://experienceleague.adobe.com/fr/docs/experience-platform/access-control/ui/users).

La personne doit alors recevoir un e-mail la redirigeant vers votre instance.

+++

### Audience

Les audiences doivent être disponibles avant de créer la campagne. [Commencer avec les audiences](../audience/about-audiences.md).

### Configuration des canaux

Pour pouvoir sélectionner un canal, la configuration de canal correspondante (c’est-à-dire le préréglage) doit être créée et disponible. [Découvrez comment configurer des canaux](../configuration/channel-surfaces.md).

## Explorons plus en détail.

Maintenant que vous comprenez le principe des campagnes dans [!DNL Journey Optimizer], il est temps d’examiner plus en détail ces sections de la documentation pour commencer à créer vos premières campagnes.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="campagnes d’action" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Campagnes d’action</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">Campagnes déclenchées par API</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="notification push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Campagnes orchestrées</a></td>
</tr></table>
