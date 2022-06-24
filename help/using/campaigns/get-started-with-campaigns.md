---
title: Prise en main des campagnes
description: En savoir plus sur les campagnes dans [!DNL Journey Optimizer]
feature: Overview
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: b9fa6bff926eb8cee476fa53feb38ed783e048fc
workflow-type: tm+mt
source-wordcount: '263'
ht-degree: 2%

---


# Prise en main des campagnes {#get-started-campaigns}

>[!CONTEXTUALHELP]
>id="campaigns_list"
>title="Campagnes"
>abstract="Grâce aux campagnes, vous pouvez diffuser du contenu unique sur un segment spécifique sur plusieurs canaux. Avant de créer une campagne, assurez-vous d’avoir un paramètre de message prédéfini et un segment Adobe Experience Platform prêt à l’emploi."

## A propos des campagnes {#about}

Les campagnes vous permettent de diffuser du contenu unique sur un segment spécifique à l’aide de plusieurs canaux.

Contrairement aux parcours, où les actions sont conçues pour être exécutées de manière séquentielle, les campagnes exécutent les actions simultanément, immédiatement ou selon un calendrier spécifié. Vous pouvez les utiliser, par exemple, pour diffuser des offres promotionnelles, des campagnes d’engagement, des annonces, des mentions légales ou des mises à jour de politique.

<!--Additionally, campaigns' content experiment feature allows you to test multiple variables of a delivery on populations samples, in order to define which treatment has the biggest impact on the targeted population.-->

Découvrez comment gérer les campagnes &lt;!>—and content expériences&lt;>:
* [Créer une campagne](create-campaign.md)
* [Modifier ou arrêter une campagne](modify-stop-campaign.md)
<!--* [Create a content experiment](content-experiment.md)-->

## Accès aux campagnes {#access}

Les campagnes sont accessibles à partir du **[!UICONTROL Campagnes]** .

Par défaut, la liste affiche toutes les campagnes avec la variable **[!UICONTROL Version préliminaire]**, **[!UICONTROL Planifié]**, et **[!UICONTROL En direct]** les états. Pour afficher les campagnes arrêtées, terminées et archivées, vous devez effacer le filtre.

![](assets/create-campaign-list.png)

## Statuts des campagnes {#statuses}

Les campagnes peuvent avoir plusieurs états :

* **[!UICONTROL Version préliminaire]**: La campagne est en édition, elle n&#39;a pas été activée.
* **[!UICONTROL Activation]**: La campagne est en cours d’activation.
* **[!UICONTROL En direct]**: La campagne a été activée.
* **[!UICONTROL Planifié]**: La campagne a été configurée pour être activée à une date de début spécifique.
* **[!UICONTROL Stoppé]**: La campagne a été arrêtée manuellement. Vous ne pouvez plus l’activer ou la réutiliser (voir [Arrêter une campagne](modify-stop-campaign.md#stop))
* **[!UICONTROL Terminé]**: La campagne est terminée.
* **[!UICONTROL Archivé]**: La campagne a été archivée.

>[!NOTE]
>
>L’icône &quot;Ouvrir la version préliminaire&quot; en regard d’un **[!UICONTROL En direct]** ou **[!UICONTROL Planifié]** le statut indique qu’une nouvelle version de la campagne a été créée et n’a pas encore été activée (voir [Modifier une campagne](modify-stop-campaign.md#modify)).
