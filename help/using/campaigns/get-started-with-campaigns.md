---
title: Prise en main des campagnes
description: En savoir plus sur les campagnes dans [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
exl-id: e2506a43-e4f5-48af-bd14-ab76c54b7c90
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '316'
ht-degree: 72%

---

# Prise en main des campagnes {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagnes"
>abstract="Les campagnes vous permettent de diffuser un contenu unique à un segment spécifique, et ce sur plusieurs canaux. Avant de créer une campagne, assurez-vous d’avoir une surface de canal (c’est-à-dire un paramètre prédéfini de message) et un segment Adobe Experience Platform prêt à l’emploi."

## À propos des campagnes {#about}

Les campagnes vous permettent de diffuser un contenu unique à un segment spécifique sur plusieurs canaux. À la différence des parcours, où les actions sont conçues pour être exécutées l’une après l’autre, les campagnes exécutent des actions simultanément, immédiatement ou selon un planning précis.

Vous pouvez créer deux types de campagnes :

* **Campagnes planifiées** autorisez des communications par lots ad hoc simples pour des cas d’utilisation marketing tels que des offres promotionnelles, des campagnes d’engagement, des annonces, des avis juridiques ou des mises à jour de stratégie.
* **Campagnes déclenchées par l’API** autorisez des messages transactionnels/opérationnels simples avec des API REST (réinitialisation de mot de passe, abandon de carte, etc.), où le besoin peut impliquer une personnalisation à l’aide d’attributs de profil et de données contextuelles issues de la payload.

Découvrez comment utiliser les campagnes :
* [Créer une campagne](create-campaign.md)
* [Création de campagnes déclenchées par l’API](api-triggered-campaigns.md)
* [Modifier ou arrêter une campagne](modify-stop-campaign.md)
* [Rapport dynamique de la campagne](campaign-live-report.md)
* [Rapport global de campagne](campaign-global-report.md)

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
* **[!UICONTROL Terminé]** : la campagne est terminée.
* **[!UICONTROL Archivé]** : la campagne a été archivée.

>[!NOTE]
>
>L’icône « Ouvrir le brouillon » en regard d’un statut **[!UICONTROL Actif]** ou **[!UICONTROL Planifié]** indique qu’une nouvelle version de la campagne a été créée et n’a pas encore été activée (consultez la section [Modifier une campagne](modify-stop-campaign.md#modify)).
