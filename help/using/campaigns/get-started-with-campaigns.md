---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec les campagnes
description: Apprenez en plus sur les campagnes dans Journey Optimizer.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: campagne, guide, commencer, optimizer
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 0ec43a204f5fcf0bddf38cfd381f0ea496c7de70
workflow-type: tm+mt
source-wordcount: '955'
ht-degree: 59%

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

Utilisez des campagnes [!DNL Journey Optimizer] pour diffuser du contenu unique à une audience spécifique sur plusieurs canaux. Contrairement aux parcours qui exécutent des actions étape par étape, les campagnes exécutent des actions simultanément, immédiatement ou selon un planning défini.

![](assets/gs-campaigns.png)

## Types de campagne

[!DNL Journey Optimizer] prend en charge trois types de campagnes. Chaque type correspond à différents cas d’utilisation et prend en charge différents canaux.

![](assets/campaign-modal.png)

>[!BEGINTABS]

>[!TAB Campagnes orchestrées]

**Campagnes orchestrées** alimentez des campagnes marketing sophistiquées et lancées par la marque sur l’ensemble des canaux, ce qui vous permet de stimuler l’engagement, le chiffre d’affaires et la fidélisation de la clientèle à grande échelle.

Bien que le marketing cross-canal soit essentiel, les campagnes orchestrées le rendent transparent. Grâce à une interface visuelle par glisser-déposer, vous pouvez concevoir et automatiser des workflows marketing complexes, depuis la segmentation jusqu’à la diffusion des messages, sur plusieurs canaux. Tout se passe dans un environnement intuitif, conçu pour assurer vitesse, contrôle et efficacité.

➡️ [Découvrez comment utiliser des campagnes orchestrées](../orchestrated/gs-orchestrated-campaigns.md).

>[!TAB Campagnes d’action (ou campagnes planifiées)]

Les **campagnes d’action** également appelées campagnes planifiées, permettent des communications par lots ad hoc simples.

* **Planifié - Marketing** - Pour les cas d’utilisation marketing tels que les offres promotionnelles, les campagnes d’engagement, les annonces, les informations juridiques ou les mises à jour de politiques. Nécessite que les destinataires soient inscrits.
* **Planifié - Transactionnel** - Contrairement aux campagnes marketing, les campagnes transactionnelles ne nécessitent pas que les destinataires soient inscrits. Utilisez cette catégorie pour les communications liées aux perturbations, aux urgences et aux annulations. Canaux pris en charge : email, SMS, notification push.

➡️ [Découvrez comment utiliser les campagnes d’action](create-campaign.md)

>[!TAB Campagnes déclenchées par API]

**Campagnes déclenchées par API** vous permettent de déclencher l’exécution de la campagne à l’aide d’un appel API. Ces communications peuvent être envoyées là où le besoin implique une personnalisation non seulement de l’utilisation d’attributs de profil tels que la réinitialisation du mot de passe, mais également des données contextuelles en temps réel dans le déclencheur, qui est une payload de l’API REST.

* **Déclenché par API - Marketing** - Envoyez des communications marketing personnalisées aux audiences ciblées.
* **Déclenché par API - Transactionnel** - Envoyez des messages à la suite d’une action effectuée par une personne, telle qu’une demande de réinitialisation de mot de passe, un achat au panier, etc.

➡️ [Découvrez comment utiliser des campagnes déclenchées par API](api-triggered-campaigns.md)


>[!ENDTABS]

## Canaux pris en charge par type de campagne {#channels}

Le tableau ci-dessous indique la disponibilité de chaque canal pour différents types de campagne, en indiquant où ils sont pris en charge.

| Canal | Action (Marketing) | Action (transactionnelle) | Déclenché par l’API (marketing) | Déclenché par l’API (transactionnel) | Orchestré |
|----------------------|---------------------|-------------------------|----------------------------|--------------------------------|--------------|
| E-mail | ✅ | ✅ | ✅ | ✅ | ✅ |
| SMS | ✅ | ✅ | ✅ | ✅ | ✅ |
| Notification push | ✅ | ✅ | ✅ | ✅ | ✅ |
| In-app | ✅ | — | — | — | — |
| Courrier | ✅ | — | — | — | — |
| Web | ✅ | — | — | — | — |
| Exp. basée sur le code | ✅ | — | — | — | — |
| Cartes de contenu | ✅ | — | — | — | — |
| WhatsApp | ✅ | — | — | — | — |
| Ligne | ✅ | — | — | — | — |

## Conditions préalables {#prerequisites}

Avant d’utiliser des campagnes, vérifiez les conditions préalables ci-dessous.

* **Audiences** Les audiences doivent être disponibles avant de créer la campagne. [Commencer avec les audiences](../audience/about-audiences.md).

* **Configurations de canal** - Pour pouvoir sélectionner un canal, vous devez avoir créé et disponible la configuration de canal correspondante (c’est-à-dire le préréglage). [Découvrez comment configurer des canaux](../configuration/channel-surfaces.md).

* **Autorisations** - Les campagnes ne sont disponibles que pour les utilisateurs disposant des autorisations appropriées répertoriées ci-dessous. Si vous ne parvenez pas à accéder aux fonctionnalités de Campaign, contactez votre administrateur pour demander les autorisations nécessaires. [En savoir plus sur les rôles intégrés de Journey Optimizer](../administration/ootb-product-profiles.md)

  | Type de campagne | Autorisations |
  |----------------------------|----------------------------------------------------------------------------|
  | **Campagnes d’action** | Administrateur de campagne<br>Approbateur de campagne<br>Responsable de campagne<br>Observateur de campagne |
  | **Campagnes déclenchées par API** | Administrateur de campagne<br>Approbateur de campagne<br>Responsable de campagne<br>Observateur de campagne |
  | **Campagnes orchestrées** | Administrateur De Campagne Orchestré<br>Approbateur De Campagne Orchestré<br>Gestionnaire De Campagne Orchestré<br>Observateur De Campagne Orchestré |

  +++Découvrir comment attribuer un rôle lié à la campagne

   1. Pour attribuer un rôle à un utilisateur ou une utilisatrice dans le produit [!DNL Permissions], accédez à l’onglet **[!UICONTROL Rôles]** et sélectionnez l’un des **[!UICONTROL Rôles]** liés à la campagne intégrée précisés ci-dessous.

   1. Dans l’onglet **[!UICONTROL Utilisateurs]**, cliquez sur **[!UICONTROL Ajouter un utilisateur]**.

   1. Saisissez le nom ou l’adresse e-mail de l’utilisateur ou sélectionnez-le dans la liste, puis cliquez sur **[!UICONTROL Enregistrer]**.

      Si le profil de l’utilisateur ou de l’utilisatrice n’a pas été créé auparavant, consultez la [documentation relative à l’ajout d’utilisateurs et d’utilisatrices](https://experienceleague.adobe.com/fr/docs/experience-platform/access-control/ui/users).

  La personne doit alors recevoir un e-mail la redirigeant vers votre instance.

  +++

## Explorons plus en détail.

Maintenant que vous comprenez le principe des campagnes dans [!DNL Journey Optimizer], il est temps d’examiner plus en détail ces sections de la documentation pour commencer à créer vos premières campagnes.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;">
<td><a href="create-campaign.md"><img width="70%" alt="campagnes d’action" src="assets/do-not-localize/gs-action-campaign.png"></a><br/><a href="create-campaign.md">Campagnes d’action</a></td>
<td><a href="api-triggered-campaigns.md"><img width="70%" alt="sms" src="assets/do-not-localize/gs-api-triggered-campaign.png"></a><br/><a href="api-triggered-campaigns.md">Campagnes déclenchées par API</a></td>
<td><a href="../orchestrated/gs-orchestrated-campaigns.md"><img width="70%" alt="notification push" src="assets/do-not-localize/gs-orchestrated-campaign.png"></a><a href="../orchestrated/gs-orchestrated-campaigns.md">Campagnes orchestrées</a></td>
</tr></table>
