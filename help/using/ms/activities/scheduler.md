---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Planificateur
description: Découvrez comment utiliser l’activité Planificateur dans une campagne orchestrée
hide: true
hidefromtoc: true
exl-id: da77a0bf-7b17-40fc-b2cb-2f0940152e64
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 35%

---

# Planificateur {#scheduler}


>[!CONTEXTUALHELP]
>id="ajo_orchestration_scheduler"
>title="Activité Planificateur"
>abstract="L’activité **Planificateur** vous permet de planifier le démarrage de la campagne orchestrée. Cette activité est à considérer comme un démarrage planifié. Elle ne peut être utilisée que comme première activité de la campagne orchestrée."


L’activité **Planificateur** est une activité de **contrôle de flux**. Elle permet de planifier le démarrage de la campagne orchestrée. Cette activité est à considérer comme un démarrage planifié. Elle ne peut être utilisée que comme première activité de la campagne orchestrée.

## Bonnes pratiques{#scheduler-best-practices}

* Ne planifiez pas l’exécution d’une campagne orchestrée à une fréquence supérieure à toutes les 15 minutes, car cela peut nuire aux performances générales du système et créer des blocs dans la base de données.
* Si vous souhaitez envoyer une diffusion unique dans votre campagne orchestrée, vous pouvez ajouter une activité de planificateur et la définir pour qu’elle s’exécute **Une fois**. Vous pouvez également définir le **Planning** dans les paramètres de la diffusion.
* Si vous souhaitez envoyer une diffusion récurrente dans votre campagne orchestrée, vous devez utiliser une activité **Planificateur** et définir la fréquence d’exécution. L’activité de diffusion récurrente ne permet pas de définir de planning.

## Configurer l’activité Planificateur {#scheduler-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_validity"
>title="Validité du planificateur"
>abstract="Vous pouvez définir une période de validité pour le planificateur. Elle peut être permanente (par défaut) ou valide jusqu’à une date spécifique."


>[!CONTEXTUALHELP]
>id="ajo_orchestration_schedule_options"
>title="Options du planificateur"
>abstract="Définissez la fréquence du planificateur. Il peut être exécuté à un moment précis, ou encore une ou plusieurs fois par jour, semaine ou mois."

Pour configurer l’activité **Planificateur**, procédez comme suit :

![](../assets/workflow-scheduler.png)

1. Ajoutez une activité **Planificateur** à votre campagne orchestrée.

1. Configurez la **Fréquence d’exécution** :

   * **Une fois** : la campagne orchestrée est exécutée une seule fois.

   * **Quotidien** : la campagne orchestrée est exécutée à une heure spécifique, une fois par jour.

   * **Plusieurs fois par jour :** la campagne orchestrée est régulièrement exécutée plusieurs fois par jour. Vous pouvez configurer des exécutions à des heures et dates spécifiques ou périodiquement.

   * **Hebdomadaire** : la campagne orchestrée est exécutée à un moment précis, une ou plusieurs fois par semaine.

   * **Mensuel** : la campagne orchestrée est exécutée à un moment précis, une ou plusieurs fois par mois. Vous pouvez sélectionner les mois pendant lesquels la campagne orchestrée doit être exécutée. Vous pouvez également configurer des exécutions un jour de semaine spécifié du mois, comme le deuxième mardi du mois.

1. Définissez les détails de l’exécution en fonction de la fréquence sélectionnée. Les champs de détail peuvent varier en fonction de la fréquence d’utilisation (heure, fréquence de répétition, jours spécifiques, etc.).

1. Cliquez sur **Prévisualiser les heures de lancement** pour vérifier le planning des dix prochaines exécutions de votre campagne orchestrée.

1. Définissez la période de validité du planificateur :

   * **Permanent (n’expire jamais)** : la campagne orchestrée est exécutée, selon la fréquence spécifiée, sans limite de durée ni de nombre d’itérations.

   * **Période de validité** : la campagne orchestrée est exécutée selon la fréquence spécifiée, jusqu&#39;à une date spécifique. Vous devez spécifier les dates de début et de fin.

>[!NOTE]
>
>Si vous souhaitez démarrer immédiatement la campagne orchestrée, vous pouvez cliquer sur le bouton **Tâche d&#39;exécution en attente** dans la barre d&#39;actions supérieure du planificateur. Ce bouton n’est disponible que lorsque vous avez démarré la campagne orchestrée.

## Exemple{#scheduler-example}

Dans l’exemple suivant, l’activité est configurée de sorte que la campagne orchestrée s’exécute plusieurs fois par jour à 9 h et 12 h, tous les jours de la semaine du 1er octobre 2025 au 1er janvier 2026.

![](../assets/workflow-scheduler2.png)
