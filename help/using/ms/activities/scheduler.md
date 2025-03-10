---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Planificateur
description: Découvrez comment utiliser l’activité Planificateur dans une campagne à plusieurs étapes
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '547'
ht-degree: 35%

---

# Planificateur {#scheduler}


>[!CONTEXTUALHELP]
>id="ajo_orchestration_scheduler"
>title="Activité Planificateur"
>abstract="L’activité **Planificateur** vous permet de planifier le démarrage de la campagne à plusieurs étapes. Cette activité est à considérer comme un démarrage planifié. Elle ne peut être utilisée que comme première activité de la campagne à plusieurs étapes."


L’activité **Planificateur** est une activité de **contrôle de flux**. Elle vous permet de planifier le démarrage de la campagne à plusieurs étapes. Cette activité est à considérer comme un démarrage planifié. Elle ne peut être utilisée que comme première activité de la campagne à plusieurs étapes.

## Bonnes pratiques{#scheduler-best-practices}

* Ne planifiez pas une campagne à plusieurs étapes pour qu’elle s’exécute plus de toutes les 15 minutes, car cela peut nuire aux performances générales du système et créer des blocs dans la base de données.
* Si vous souhaitez envoyer une diffusion unique dans votre campagne à plusieurs étapes, vous pouvez ajouter une activité de planificateur et la définir pour qu’elle s’exécute **Une fois**. Vous pouvez également définir le **Planning** dans les paramètres de la diffusion.
* Si vous souhaitez envoyer une diffusion récurrente dans votre campagne à plusieurs étapes, vous devez utiliser une activité **Planificateur** et définir la fréquence d’exécution. L’activité de diffusion récurrente ne permet pas de définir de planning.

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

1. Ajoutez une activité **Planificateur** à votre campagne à plusieurs étapes.

1. Configurez la **Fréquence d’exécution** :

   * **Une fois** : la campagne à plusieurs étapes est exécutée une seule fois.

   * **Quotidien** : la campagne à plusieurs étapes est exécutée à une heure spécifique, une fois par jour.

   * **Plusieurs fois par jour :** la campagne à plusieurs étapes est régulièrement exécutée plusieurs fois par jour. Vous pouvez configurer des exécutions à des heures et dates spécifiques ou périodiquement.

   * **Hebdomadaire** : la campagne à plusieurs étapes est exécutée à un moment spécifié, une ou plusieurs fois par semaine.

   * **Mensuel** : la campagne à plusieurs étapes est exécutée à un moment précis, une ou plusieurs fois par mois. Vous pouvez sélectionner les mois, lorsque vous avez besoin que la campagne à plusieurs étapes soit exécutée. Vous pouvez également configurer des exécutions un jour de semaine spécifié du mois, comme le deuxième mardi du mois.

1. Définissez les détails de l’exécution en fonction de la fréquence sélectionnée. Les champs de détail peuvent varier en fonction de la fréquence d’utilisation (heure, fréquence de répétition, jours spécifiques, etc.).

1. Cliquez sur **Prévisualiser les heures de lancement** pour vérifier le planning des dix prochaines exécutions de votre campagne à plusieurs étapes.

1. Définissez la période de validité du planificateur :

   * **Permanent (n’expire jamais)** : la campagne à plusieurs étapes est exécutée, selon la fréquence spécifiée, sans limite de délai ni de nombre d’itérations.

   * **Période de validité** : la campagne multi-étapes est exécutée selon la fréquence spécifiée, jusqu’à une date spécifique. Vous devez spécifier les dates de début et de fin.

>[!NOTE]
>
>Si vous souhaitez démarrer immédiatement la campagne à plusieurs étapes, vous pouvez cliquer sur le bouton **Exécuter la tâche en attente** dans la barre d&#39;actions supérieure du planificateur. Ce bouton n’est disponible que lorsque vous avez démarré la campagne à plusieurs étapes.

## Exemple{#scheduler-example}

Dans l’exemple suivant, l’activité est configurée de sorte que la campagne à plusieurs étapes s’exécute plusieurs fois par jour à 9 h et 12 h, tous les jours de la semaine du 1er octobre 2025 au 1er janvier 2026.

![](../assets/workflow-scheduler2.png)
