---
solution: Journey Optimizer
product: journey optimizer
title: Utilisation d’un segment dans un parcours
description: Découvrez comment utiliser un segment dans un parcours
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 7b27d42e-3bfe-45ab-8a37-c55b231052ee
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '1260'
ht-degree: 0%

---

# Utilisation d’un segment dans un parcours {#segment-trigger-activity}

## Ajout d’une activité Lecture de segment {#about-segment-trigger-actvitiy}

>[!CONTEXTUALHELP]
>id="ajo_journey_read_segment"
>title="Activité Lecture de segment"
>abstract="L’activité Lecture de segment vous permet de faire entrer dans un parcours toutes les personnes appartenant à un segment Adobe Experience Platform. L’entrée dans un parcours peut être effectuée une seule fois ou régulièrement."

Utilisez la variable **Lecture de segment** pour faire entrer toutes les personnes d’un segment dans le parcours. L’entrée dans un parcours peut être effectuée une seule fois ou régulièrement.

Prenons comme exemple le segment &quot;Ouverture et passage en caisse de l’application Luma&quot; créé dans la variable [Création de segments](../segment/about-segments.md) cas d’utilisation. Avec l’activité Lecture de segment , vous pouvez faire en sorte que toutes les personnes appartenant à ce segment entrent dans un parcours et se dirigent vers des parcours personnalisés qui exploiteront toutes les fonctionnalités du parcours : conditions, minuteurs, événements, actions.

>[!NOTE]
>
>Pour les parcours qui utilisent une activité Lecture de segment , un nombre maximum de parcours peuvent démarrer exactement en même temps. Les reprises seront effectuées par le système, mais évitez d’avoir plus de cinq parcours (avec Lecture de segment, planifiés ou démarrés &quot;dès que possible&quot;) commençant exactement au même moment en les répartissant dans le temps, par exemple entre 5 et 10 minutes d’intervalle.
>
>Les groupes de champs d’événement d’expérience ne peuvent pas être utilisés dans les parcours commençant par un segment de lecture, une qualification de segment ou une activité d’événement commercial.

### Configuration de l’activité {#configuring-segment-trigger-activity}

Les étapes de configuration de l’activité Lecture de segment sont les suivantes :

1. Développez l’objet **[!UICONTROL Orchestration]** catégorie et déposer une **[!UICONTROL Read Segment]** dans votre zone de travail.

   L’activité doit être positionnée comme première étape d’un parcours.

1. Ajouter un **[!UICONTROL Label]** à l’activité (facultatif).

1. Dans le **[!UICONTROL Segment]** , sélectionnez le segment Adobe Experience Platform qui va entrer dans le parcours, puis cliquez sur **[!UICONTROL Save]**.

   Notez que vous pouvez personnaliser les colonnes affichées dans la liste et les trier.

   >[!NOTE]
   >
   >Seuls les individus dotés de la fonction **Réalisé** et **Existant** les états de participation au segment entrent dans le parcours. Pour plus d’informations sur l’évaluation d’un segment, reportez-vous à la section [Documentation de Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html#interpret-segment-results){target=&quot;_blank&quot;}.

   ![](assets/read-segment-selection.png)

   Une fois le segment ajouté, la variable **[!UICONTROL Copy]** permet de copier son nom et son identifiant :

   `{"name":"Luma app opening and checkout",”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](assets/read-segment-copy.png)

1. Dans le **[!UICONTROL Namespace]** , choisissez l’espace de noms à utiliser pour identifier les individus. [En savoir plus sur les espaces de noms](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >Les personnes appartenant à un segment qui n’a pas l’identité sélectionnée (espace de noms) parmi leurs différentes identités ne peuvent pas entrer dans le parcours.

1. Définissez la variable **[!UICONTROL Throttling rate]** à la limite de débit de l’activité de lecture de segment.

   Cette valeur est stockée dans la payload de la version du parcours. La valeur par défaut est de 20 000 messages par seconde. Vous pouvez modifier cette valeur de 500 à 20 000 messages par seconde.

   >[!NOTE]
   >
   >Le taux de ralentissement global par environnement de test est défini sur 20 000 messages par seconde. Par conséquent, le taux de ralentissement de tous les segments lus qui s’exécutent simultanément dans le même environnement de test s’élève à 20 000 messages par seconde au maximum. Vous ne pouvez pas modifier cette limite.

1. Le **[!UICONTROL Read Segment]** activité vous permet de spécifier l’heure à laquelle le segment va entrer dans le parcours. Pour ce faire, cliquez sur le bouton **[!UICONTROL Edit journey schedule]** pour accéder aux propriétés du parcours, puis configurez la variable **[!UICONTROL Scheduler type]** champ .

   ![](assets/read-segment-schedule.png)

   Par défaut, les segments rejoignent le parcours **[!UICONTROL As soon as possible]**. Si vous souhaitez que le segment entre dans le parcours à une date/heure spécifique ou de manière récurrente, sélectionnez la valeur souhaitée dans la liste.

   >[!NOTE]
   >
   >Notez que la variable **[!UICONTROL Schedule]** n’est disponible que lorsqu’une **[!UICONTROL Read Segment]** l’activité a été déposée dans la zone de travail.

   ![](assets/read-segment-schedule-list.png)

   **Lecture incrémentale** option : lorsqu’un parcours avec un événement récurrent **Lecture de segment** s’exécute pour la première fois, tous les profils du segment entrent dans le parcours. Cette option permet de cibler, après la première occurrence, uniquement les individus entrés dans le segment depuis la dernière exécution du parcours.

   **Force une réentrée sur une période récurrente**: cette option vous permet de faire en sorte que tous les profils toujours présents dans le parcours le quittent automatiquement lors de la prochaine exécution. Par exemple, si vous avez 2 jours d’attente dans un parcours récurrent quotidien, en activant cette option, les profils seront toujours déplacés lors de la prochaine exécution du parcours (donc le jour suivant), qu’ils se trouvent dans la prochaine audience d’exécution ou non. Si la durée de vie de vos profils dans ce parcours peut être supérieure à la fréquence de périodicité, n’activez pas cette option pour vous assurer que les profils peuvent terminer leur parcours.

<!--

### Segment filters {#segment-filters}

[!CONTEXTUALHELP]
>id="jo_segment_filters"
>title="About segment filters"
>abstract="You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week."

You can choose to target only the individuals who entered or exited a specific segment during a specific time window. For example, you can decide to only retrieve all the customers who entered the VIP segment since last week. Only the new VIP customers will be targeted. All the customers who were already part of the VIP segment before will be excluded.

To activate this mode, click the **Segment Filters** toggle. Two fields are displayed:

**Segment membership**: choose whether you want to listen to segment entrances or exits. 

**Lookback window**: define when you want to start to listen to entrances or exits. This lookback window is expressed in hours, starting from the moment the journey is triggered.  If you set this duration to 0, the journey will target all members of the segment. For recurring journeys, it will take into account all entrances/exits since the last time the journey was triggered.

-->

>[!NOTE]
>
>Les parcours de lecture en une seule fois de segment passent à l’état Terminé 30 jours après l’exécution du parcours. Pour les segments de lecture planifiés, il s’agit de 30 jours après l’exécution de la dernière occurrence.

### Test et publication du parcours {#testing-publishing}

Le **[!UICONTROL Read Segment]** l’activité vous permet de tester le parcours sur un profil unitaire ou sur 100 profils de test aléatoires sélectionnés parmi les profils qualifiés pour le segment.

Pour ce faire, activez le mode test, puis sélectionnez l’option de votre choix dans le volet de gauche.

![](assets/read-segment-test-mode.png)

Vous pouvez ensuite configurer et exécuter le mode test comme vous le faites habituellement. [Découvrez comment tester un parcours](testing-the-journey.md).

Une fois le test en cours d’exécution, la variable **[!UICONTROL Show logs]** vous permet d’afficher les résultats du test en fonction de l’option de test sélectionnée :

* **[!UICONTROL Single profile at a time]**: les journaux de test affichent les mêmes informations que lors de l’utilisation du mode test unitaire. Voir à ce sujet la section [cette section](testing-the-journey.md#viewing_logs)

* **[!UICONTROL Up to 100 profiles at once]**: les journaux de test vous permettent de suivre l’avancement de l’exportation de segments à partir d’Adobe Experience Platform, ainsi que la progression individuelle de toutes les personnes qui sont entrées dans le parcours.

   Notez que tester le parcours en utilisant jusqu’à 100 profils à la fois ne vous permet pas de suivre la progression des individus dans le parcours à l’aide du flux visuel.

   ![](assets/read-segment-log.png)

Une fois les tests réussis, vous pouvez publier votre parcours (voir [Publication du parcours](publishing-the-journey.md)). Les personnes appartenant au segment rejoindront le parcours à la date/heure spécifiée dans les propriétés du parcours. **[!UICONTROL Scheduler]** .

>[!NOTE]
>
>Pour les parcours récurrents basés sur des segments, le parcours se ferme automatiquement une fois sa dernière occurrence exécutée. Si aucune date/heure de fin n’a été spécifiée, vous devrez fermer manuellement le parcours vers de nouvelles entrées pour le terminer.

## Ciblage d’audience dans les parcours basés sur des segments

Les parcours basés sur des segments commencent toujours par un **Lecture de segment** pour récupérer les individus appartenant à un segment Adobe Experience Platform.

L’audience appartenant au segment est récupérée une fois ou de manière régulière.

Après avoir rejoint le parcours, vous pouvez créer des cas d’utilisation d’orchestration de l’audience, ce qui fait que les individus du segment initial se déplacent dans différentes branches du parcours.

**Segmentation**

Vous pouvez utiliser des conditions pour effectuer une segmentation à l’aide de la variable **Condition** activité. Par exemple, vous pouvez faire en sorte que les personnes VIP empruntent un chemin particulier et que le flux non VIP emprunte un autre chemin.

La segmentation peut être basée sur :

* données de source de données
* le contexte des événements faisant partie des données de parcours, par exemple : une personne a-t-elle cliqué sur le message reçu il y a une heure ?
* une date, par exemple : sommes-nous en juin lorsqu&#39;une personne fait le voyage ?
* une heure, par exemple : est-ce le matin dans le fuseau horaire de la personne ?
* un algorithme fractionnant l’audience qui participe au parcours en fonction d’un pourcentage, par exemple : 90 à 10 % pour exclure une population témoin

![](assets/read-segment-audience1.png)

**Exclusion**

Identique **Condition** l’activité utilisée pour la segmentation (voir ci-dessus) permet également d’exclure une partie de la population. Par exemple, vous pouvez exclure les personnes VIP en les faisant entrer dans une branche avec une étape de fin juste après.

Cette exclusion peut survenir juste après la récupération des segments, à des fins de comptage de population ou au cours d’un parcours à plusieurs étapes.

![](assets/read-segment-audience2.png)

**Union**

Les parcours vous permettent de créer N branches et de les associer après une segmentation.

Par conséquent, vous pouvez faire en sorte que deux audiences reviennent à une expérience commune.

Par exemple, après avoir suivi une expérience différente pendant dix jours dans un parcours, les clients VIP et non VIP peuvent revenir au même chemin.

Après une union, vous pouvez diviser à nouveau l’audience en effectuant une segmentation ou une exclusion.

![](assets/read-segment-audience3.png)
