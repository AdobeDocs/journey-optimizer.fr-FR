---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité d’attente dans des campagnes à plusieurs étapes
description: Découvrez comment utiliser l’activité d’attente dans des campagnes à plusieurs étapes
hide: true
hidefromtoc: true
exl-id: 11ef095b-77ec-4e2e-ab4d-49a248354f08
source-git-commit: 323472ef9d6203cbbadc44ceb17ddcc7f6207323
workflow-type: tm+mt
source-wordcount: '168'
ht-degree: 85%

---

# Attente {#wait}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_wait"
>title="Activité Attente"
>abstract="L’activité **Attente** est utilisée pour retarder la transition d’une activité à une autre."

L’activité d’**attente** est une activité de **contrôle de flux**. Elle est utilisée pour permettre qu’un certain temps s’écoule entre l’exécution de deux activités. Par exemple, elle permet d’attendre plusieurs jours après une activité de diffusion e-mail puis d’analyser les ouvertures et les clics générés pendant ce laps de temps avant d’appliquer d’autres traitements (e-mail de rappel, création d’audience, etc.).

## Configuration{#wait-configuration}

Pour configurer l’activité d’**attente**, procédez comme suit :

1. Ajoutez une activité **Attente** dans votre campagne à plusieurs étapes.

1. Spécifiez la **durée** de l’attente entre les transitions entrante et sortante.

1. Sélectionnez l’unité de temps dans le champ **Périodes** : secondes, minutes, heures, jours.

## Exemple{#wait-example}

L’exemple suivant illustre l’activité **Attente** dans un cas typique. Un e-mail d’invitation à un événement est envoyé. 24 heures après son envoi, une diffusion SMS est envoyée à la même population.

![](../assets/workflow-wait-example.png)
