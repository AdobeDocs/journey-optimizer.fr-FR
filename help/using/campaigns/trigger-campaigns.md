---
solution: Journey Optimizer
product: journey optimizer
title: Examiner et activer une campagne
description: Découvrez comment vérifier et activer des campagnes dans Journey Optimizer.
feature: Campaigns
topic: Content Management
role: User
level: Intermediate
keywords: campagne, vérification, validation, activation, activer, optimizer
exl-id: 86f35987-f0b7-406e-9ae6-0e4a2e651610
source-git-commit: 1d3638499a9e8261a5f1b09744b82642198a5d5d
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 100%

---


# Exécuter une campagne déclenchée par API {#execute}

Une fois votre campagne activée, vous devez récupérer l’exemple de requête cURL généré et l’utiliser dans l’API pour créer votre payload et déclencher la campagne.

## À lire impérativement {#must-read}

* **Dates de début/de fin de la campagne** : si vous avez configuré une date de début et/ou de fin spécifique lors de la création de la campagne, elle ne sera pas exécutée en dehors de ces dates et les appels API échoueront.

* **Délai d’expiration de l’appel** : le délai d’expiration de l’appel de l’API REST Interactive Message Execution est de 60 secondes. Cependant, de nouvelles tentatives internes d’appel sont implémentées en cas de délais dépassés inattendus pour garantir la diffusion.

## Déclencher la campagne {#trigger}

1. Ouvrez la campagne, puis copiez-collez la requête de payload depuis la section **[!UICONTROL requête cURL]**. Cette payload inclut toutes les variables de personnalisation (profil et contexte) utilisées dans le message. Elle est disponible une fois la campagne activée.

   ![](assets/api-triggered-curl.png)

1. Utilisez cette requête cURL dans les API pour créer votre payload et déclencher la campagne. Pour plus d’informations, consultez la [documentation de l’API d’exécution de message interactif](https://developer.adobe.com/journey-optimizer-apis/references/messaging/#tag/execution).

   Des exemples d’appels API sont également disponibles sur [cette page](https://developer.adobe.com/journey-optimizer-apis/references/messaging-samples/).
