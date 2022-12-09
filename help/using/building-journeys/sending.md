---
solution: Journey Optimizer
product: journey optimizer
title: Démarrage de l’exécution du parcours
description: Découvrez comment démarrer votre parcours et envoyer des messages
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 0%

---


# Exécution du parcours {#message-execution}

## Tester votre parcours

Vous pouvez tester votre parcours à l’aide de profils de test. Cette étape est recommandée pour valider vos paramètres et messages.

En savoir plus à ce sujet [section](testing-the-journey.md).

## Activation du parcours

Vous devez publier votre parcours pour l’activer.

![](assets/jo-journeyuc2_32bis.png)

En savoir plus à ce sujet [section](publishing-the-journey.md).


Une fois le parcours publié, vous pouvez le surveiller à l’aide d’outils de reporting dédiés afin de mesurer son efficacité.

![](assets/jo-dynamic_report_journey_12.png)

[En savoir plus sur les rapports](../reports/live-report.md)

## Envoyer les messages {#send-messages}

Lorsque le contenu de votre message est défini, il est prêt à être envoyé via un [parcours](journey.md).

Une fois un message envoyé, vous pouvez en contrôler l&#39;exécution via plusieurs indicateurs. [En savoir plus sur les rapports](../global-report.md).

## Planification des messages {#schedule-messages}

Les messages peuvent être planifiés via la variable **[!UICONTROL Read Segment]** une activité dans une [parcours](journey.md). Vous pouvez indiquer le moment où le segment va entrer dans le parcours. [En savoir plus sur l’activité Lecture de segment](read-segment.md).

Pour ce faire, procédez comme suit :

1. Modification d’un parcours, glisser-déposer d’un **[!UICONTROL Read Segment]** et commencez à la configurer. [En savoir plus sur la configuration de l’activité Lecture de segment](read-segment.md#configuring-segment-trigger-activity).

1. Cliquez sur le bouton **[!UICONTROL Edit journey schedule]** pour accéder aux propriétés du parcours.

   ![](assets/message-read-segment-schedule.png)

1. Configurez la variable **[!UICONTROL Scheduler type]** field : sélectionnez la valeur souhaitée dans la liste pour que le segment entre dans le parcours à une date/heure spécifique ou de manière récurrente.

   >[!NOTE]
   >
   >Le **[!UICONTROL Schedule]** n’est disponible que lorsqu’une **[!UICONTROL Read Segment]** l’activité a été déposée dans la zone de travail.

   ![](assets/message-read-segment-scheduler.png)

1. Si vous sélectionnez **[!UICONTROL Once]**, définissez une date et une heure spécifiques auxquelles le segment rejoindra le parcours.

   ![](assets/message-read-segment-scheduler-once.png)

1. Si vous sélectionnez une méthode récurrente, modifiez la date et l’heure de début. Vous pouvez également définir une date et une heure de fin facultatives.

   ![](assets/message-read-segment-scheduler-daily.png)

   >[!NOTE]
   >
   >Par défaut, les segments rejoignent le parcours **[!UICONTROL As soon as possible]**, c’est-à-dire 1 heure après la publication du parcours.

1. Cliquez sur **[!UICONTROL OK]** pour enregistrer vos modifications.

<!--Unitary messages that are triggered by an event within a journey cannot be scheduled.-->
