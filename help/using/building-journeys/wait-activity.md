---
solution: Journey Optimizer
product: journey optimizer
title: Activité Attente
description: Découvrir comment configurer l’activité Attente
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: attente, activité, parcours, suivant, zone de travail
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: 846c601c02a28119dddb3029e5273cfccf141a2c
workflow-type: ht
source-wordcount: '567'
ht-degree: 100%

---

# Activité Attente {#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Activité Attente"
>abstract="Si vous souhaitez observer un temps d&#39;attente avant d&#39;exécuter l&#39;activité suivante dans le chemin, vous pouvez utiliser une activité Attente. Cela vous permet de définir le moment d&#39;exécution de l&#39;activité suivante. Deux options sont disponibles : durée et personnalisation."

Vous pouvez utiliser une activité **[!UICONTROL Attente]** pour définir une durée avant l’exécution de l’activité suivante.  La durée d’attente maximale est de **29 jours**.

Vous pouvez définir deux types d’activité **Attente** :

* Attente en fonction d’une durée relative. [En savoir plus](#duration)
* Date personnalisée, avec des fonctions pour la calculer. [En savoir plus](#custom)

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## Recommandations {#wait-recommendations}

### Activités Attente multiples {#multiple-wait-activities}

Lorsque vous utilisez plusieurs activités **Attente** dans un parcours, gardez à l’esprit que le délai d’expiration global du parcours est de 30 jours, ce qui signifie qu’un profil quittera toujours le parcours au maximum 30 jours après y être entré. En savoir plus sur [cette page](../building-journeys/journey-gs.md#global_timeout).

Une personne ne peut entrer dans une activité **Attente** que si elle dispose de suffisamment de temps restant dans le parcours pour compléter la durée d’attente avant le délai d’expiration de 30 jours du parcours. Par exemple, si vous ajoutez deux activités **Attente** définies sur 20 jours chacune, le système détecte que la seconde activité **Attente** se termine après le délai d’expiration de 30 jours. La seconde activité **Attente** est donc ignorée et la personne quitte le parcours avant de la commencer. Dans cet exemple, la personne restera 20 jours au total dans le parcours.

### Attente et reprise {#wait-re-entrance}

La bonne pratique est de ne pas utiliser d’activités **Attente** pour bloquer une reprise. Utilisez plutôt l’option **Autoriser la reprise** au niveau des propriétés du parcours. En savoir plus sur [cette page](../building-journeys/journey-gs.md#entrance).

### Attente et mode test {#wait-test-modd}

En mode test, le paramètre **[!UICONTROL Durée d’attente en test]** vous permet de définir la durée de chaque activité **Attente**. La valeur par défaut est de 10 secondes. Vous obtiendrez ainsi rapidement les résultats du test. En savoir plus sur [cette page](../building-journeys/testing-the-journey.md).

## Configuration {#wait-configuration}

### Durée de l’attente {#duration}

Sélectionnez le type de **Durée** pour définir la durée relative de l’attente avant l’exécution de l’activité suivante. La durée maximum est de **29 jours**.

![Définition de la durée d’attente](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

### Attente personnalisée {#custom}

Sélectionnez le type **Personnalisée** pour définir une date personnalisée à l’aide d’une expression avancée basée sur un champ provenant d’un événement ou d’une réponse d’action personnalisée. Vous ne pouvez pas définir directement une durée relative (par exemple, 7 jours) mais vous pouvez utiliser des fonctions pour la calculer si nécessaire (par exemple, 2 jours après l’achat).

![Définition d’une attente personnalisée avec une expression](assets/journey57.png)

L’expression figurant dans l’éditeur doit fournir un format `dateTimeOnly`. Consultez [cette page](expression/expressionadvanced.md). Pour plus d’informations sur le format dateTimeOnly, consultez [cette page](expression/data-types.md).

La bonne pratique consiste à utiliser des dates personnalisées spécifiques à vos profils, et d’éviter d’utiliser la même date pour tous les profils. Par exemple, ne définissez pas `toDateTimeOnly('2024-01-01T01:11:00Z')`, mais plutôt `toDateTimeOnly(@event{Event.productDeliveryDate})`, qui est spécifique à chaque profil. Gardez à l’esprit que l’utilisation de dates fixes peut entraîner des problèmes d’exécution de votre parcours.


>[!NOTE]
>
>Vous pouvez tirer parti d’une expression `dateTimeOnly` ou utiliser une fonction pour effectuer une conversion vers le format `dateTimeOnly`. Par exemple : `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`, le champ de l’événement se présentant sous la forme 2023-08-12T09:46:06Z.
>
>La définition du **fuseau horaire** est attendue dans les propriétés de votre parcours. Par conséquent, à partir de l’interface d’utilisation, il n’est actuellement pas possible de pointer directement vers un horodatage ISO-8601 complet associant l’heure et le fuseau horaire, tel que 2023-08-12T09:46:06.982-05. [En savoir plus](../building-journeys/timezone-management.md).


Pour vérifier que l’activité d’attente fonctionne comme prévu, vous pouvez utiliser des événements d’étape. [En savoir plus](../reports/query-examples.md#common-queries).

<!--## Email send time optimization{#email_send_time_optimization}

This type of wait uses a score calculated in Adobe Experience Platform. The score calculates the propensity to click or open an email in the future based on past behavior. Note that the algorithm calculating the score needs a certain amount of data to work. As a result, when it does not have enough data, the default wait time will apply. At publication time, you'll be notified that the default time applies.

>[!NOTE]
>
>The first event of your journey must have a namespace.
>
>This capability is only available after an **[!UICONTROL Email]** activity. You need to have Adobe Campaign Standard.

1. In the **[!UICONTROL Amount of time]** field, define the number of hours to consider to optimize email sending.
1. In the **[!UICONTROL Optimization type]** field, choose if the optimization should increase clicks or opens.
1. In the **[!UICONTROL Default time]** field, define the default time to wait if the predictive send time score is not available.

    >[!NOTE]
    >
    >Note that the send time score can be unavailable because there is not enough data to perform the calculation. In this case, you will be informed, at publication time, that the default time applies.

![](assets/journey57bis.png)-->
