---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Branchement
description: Découvrez comment utiliser l’activité Branchement dans une campagne orchestrée.
exl-id: 52e8057b-dac1-45f5-9dd0-1b28a59adde9
version: Campaign Orchestration
TQID: https://experienceleague.adobe.com/b0FyVaM0LcSz1DLGd-UEhHqBqXMWcb0rbimJA6E7WOM
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: b423a773-0a58-4a77-b65d-3dd4ae6ef841
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 256
ht-degree: 54%

---

# Branchement {#fork}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork"
>title="Activité Branchement"
>abstract="L’activité **Branchement** permet de créer des transitions sortantes afin de lancer plusieurs activités en parallèle."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_fork_transitions"
>title="Transitions de l’activité Branchement"
>abstract="Par défaut, deux transitions sont créées avec une activité **Branchement**. Cliquez sur le bouton **Ajouter une transition** pour définir une transition sortante supplémentaire, puis renseignez son libellé."

L’activité **[!UICONTROL Branchement]** est un composant **[!UICONTROL Contrôle de flux]** qui permet de créer plusieurs transitions sortantes et d’exécuter plusieurs activités en parallèle.

## Configurer l’activité Branchement{#fork-configuration}

Pour configurer l’activité **[!UICONTROL Branchement]**, procédez comme suit :

![](../assets/workflow-fork.png)

1. Ajoutez une activité **[!UICONTROL Branchement]** à votre campagne orchestrée.

1. Définissez un **[!UICONTROL libellé]**.

1. Ajoutez un libellé à chaque transition sortante. Par défaut, deux transitions sont fournies.

1. Pour supprimer une transition, cliquez sur l’icône ![](../assets/do-not-localize/Smock_Delete_18_N.svg).

1. Si nécessaire, cliquez sur **[!UICONTROL Ajouter une transition]** pour ajouter une transition sortante supplémentaire.

## Exemples {#fork-examples}

Voici une utilisation type de l’activité **[!UICONTROL Branchement]** : cibler la même audience avec deux canaux e-mail différents (un marketing et un transactionnel) pour comparer le comportement de diffusion.

Une fois qu’une activité **[!UICONTROL Créer une audience]** sélectionne la population cible, un **[!UICONTROL Branchement]** crée deux branches parallèles :

* **Branche 1** se connecte à une activité de canal e-mail marketing. Les messages suivent les règles métier standard et sont envoyés uniquement aux profils inscrits.
* La **Branche 2** se connecte à une activité de canal e-mail transactionnel . Les messages contournent les règles métier et sont envoyés à tous les profils, quel que soit le statut d’opt-in.

![](../assets/workflow-fork.png)

Ce modèle est utile pour comprendre comment les paramètres de catégorie de canal affectent le comportement de la diffusion et pour envoyer différents types de messages à la même audience au cours d’une seule exécution de campagne.
