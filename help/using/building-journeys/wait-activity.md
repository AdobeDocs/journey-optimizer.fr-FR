---
solution: Journey Optimizer
product: journey optimizer
title: Activité d'attente
description: Découvrez comment configurer l’activité d’attente
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: attente, activité, parcours, suivant, zone de travail
exl-id: 7268489a-38c1-44da-b043-f57aaa12d7d5
source-git-commit: 505a418819b7a8ac9883d78a4f3d05a78cf5aa31
workflow-type: tm+mt
source-wordcount: '535'
ht-degree: 37%

---

# Activité d&#39;attente {#wait-activity}

>[!CONTEXTUALHELP]
>id="ajo_journey_wait"
>title="Activité d&#39;attente"
>abstract="Si vous souhaitez observer un temps d&#39;attente avant d&#39;exécuter l&#39;activité suivante dans le chemin, vous pouvez utiliser une activité Attente. Cela vous permet de définir le moment d&#39;exécution de l&#39;activité suivante. Deux options sont disponibles : durée et personnalisation."

Vous pouvez utiliser une **[!UICONTROL Attente]** pour définir une durée avant d’exécuter l’activité suivante. Les options disponibles sont les suivantes :

* [Durée](#duration)
* [Valeur](#custom) personnalisée

<!--
* [Email send time optimization](#email_send_time_optimization)
* [Fixed date](#fixed_date) 
-->

## À propos de l&#39;activité d&#39;attente {#about_wait}

La durée d&#39;attente maximale est de 29 jours. En mode test, le paramètre **[!UICONTROL Temps d&#39;attente en test]** vous permet de définir la durée de chaque activité d&#39;attente. La valeur par défaut est de 10 secondes. Vous obtiendrez ainsi rapidement les résultats du test. En savoir plus sur [cette page](../building-journeys/testing-the-journey.md).

Soyez prudent lorsque vous utilisez plusieurs **Attente** activités dans un parcours, car le délai d’expiration du parcours global est de 30 jours, ce qui signifie qu’un profil abandonnera toujours le parcours maximum 30 jours après son entrée. En savoir plus sur [cette page](../building-journeys/journey-gs.md#global_timeout).

Un individu peut saisir une **Attente** activité uniquement s’il leur reste suffisamment de temps dans le parcours pour terminer la durée d’attente avant le délai d’parcours de 30 jours. Par exemple, si vous ajoutez deux **Attente** est définie sur 20 jours, le système détecte que la seconde variable **Attente** l’activité se termine après le délai d’attente de 30 jours. La seconde **Attente** L’activité sera donc ignorée et l’individu quittera le parcours avant de le démarrer. Dans cet exemple, la cliente ou le client restera 20 jours au total dans le parcours.

Une bonne pratique pour ne pas utiliser **Attente** activités pour bloquer la rentrée. Utilisez plutôt l’option **Autoriser la reprise** au niveau des propriétés du parcours. En savoir plus sur [cette page](../building-journeys/journey-gs.md#entrance).

## Durée de l&#39;attente {#duration}

Sélectionnez la durée d&#39;attente avant l&#39;exécution de l&#39;activité suivante. La durée maximale est de 29 jours.

![Définition de la durée d’attente](assets/journey55.png)

<!--
## Fixed date wait{#fixed_date}

Select the date for the execution of the next activity.

![](assets/journey56.png)

-->

## Attente personnalisée {#custom}

Utilisez la variable **Personnalisé** saisissez pour définir une date personnalisée à l’aide d’une expression avancée basée sur un champ provenant d’un événement ou d’une réponse d’action personnalisée. Vous ne pouvez pas définir directement une durée relative, par exemple, 7 jours, mais vous pouvez utiliser des fonctions pour la calculer si nécessaire (par exemple, 2 jours après l’achat).

![Définition d’une attente personnalisée avec une expression](assets/journey57.png)

L’expression de l’éditeur doit fournir une `dateTimeOnly` format. Consultez [cette page](expression/expressionadvanced.md). Pour plus d’informations sur le format dateTimeOnly, reportez-vous à la section [cette page](expression/data-types.md).

Il est recommandé d’utiliser des dates personnalisées spécifiques à vos profils et d’éviter d’utiliser la même date pour tous. Par exemple, ne définissez pas `toDateTimeOnly('2024-01-01T01:11:00Z')` mais `toDateTimeOnly(@event{Event.productDeliveryDate})` qui est spécifique à chaque profil. Gardez à l’esprit que l’utilisation de dates fixes peut entraîner des problèmes d’exécution de votre parcours.


>[!NOTE]
>
>Vous pouvez utiliser une `dateTimeOnly` expression ou utilisation d’une fonction pour effectuer une conversion en `dateTimeOnly`. Par exemple : `toDateTimeOnly(@event{Event.offerOpened.activity.endTime})`, le champ de l’événement correspondant au formulaire 2023-08-12T09:46:06Z.
>
>La définition du **fuseau horaire** est attendue dans les propriétés de votre parcours. Par conséquent, à partir de l’interface utilisateur, il n’est pas possible de pointer directement vers un horodatage ISO-8601 complet associant l’heure et le décalage du fuseau horaire comme 2023-08-12T09:46:06.982-05 [En savoir plus](../building-journeys/timezone-management.md).


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
