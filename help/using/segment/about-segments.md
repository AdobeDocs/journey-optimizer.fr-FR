---
solution: Journey Optimizer
product: journey optimizer
title: À propos des segments Adobe Experience Platform
description: Découvrez comment configurer un segment Adobe Experience Platform
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: bfd262db2fd12afbb7df6c73c68b29d18a1abf98
workflow-type: tm+mt
source-wordcount: '452'
ht-degree: 0%

---

# Prise en main des segments Adobe Experience Platform {#about-segments}

[!DNL Journey Optimizer]  vous permet de créer des segments Adobe Experience Platform à l’aide de données Real-time Customer Profile directement à partir de la variable **[!UICONTROL Segments]** et exploitez-les dans vos parcours.

Notez que les segments peuvent également être créés à partir du service Segmentation lui-même. En savoir plus dans la section [Documentation d’Adobe Experience Platform Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html).

Vous pouvez exploiter les segments dans les parcours de différentes manières :

* Utilisez une **Lecture de segment** activité d’orchestration pour faire entrer dans le parcours toutes les personnes appartenant au segment spécifié. Les messages inclus dans votre parcours sont envoyés aux individus appartenant au segment. Supposons que vous ayez un segment &quot;client Silver&quot;. Avec cette activité, vous pouvez faire entrer tous les clients Silver dans un parcours et leur envoyer une série de messages personnalisés.

   Pour plus d’informations sur l’utilisation de la variable **[!UICONTROL Read segment]** activité, voir [cette section](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Utilisez la variable **Qualification du segment** activité d’événement pour faire entrer ou avancer des individus dans un parcours en fonction des entrées et des sorties de segments Adobe Experience Platform. Par exemple, vous pouvez faire entrer tous les nouveaux clients Silver dans un parcours et leur envoyer des messages. Pour plus d&#39;informations sur l&#39;utilisation de cette activité, reportez-vous à la section [cette section](../building-journeys/segment-qualification-events.md).

* Build **conditions complexes** dans vos parcours à l’aide de l’éditeur d’expression simple ou avancé. En savoir plus dans [cette section](../building-journeys/condition-activity.md#using-a-segment).

## Méthodes d’évaluation d’audience{#evaluation-method-in-journey-optimizer}

Dans Adobe Journey Optimizer, les audiences sont générées à partir de définitions de segment à l’aide de l’une des méthodes d’évaluation suivantes :

* Segmentation par flux : la liste des audiences du segment est actualisée en temps réel pendant que de nouvelles données s’enchaînent dans le système. La segmentation par flux est un processus continu de sélection des données qui met à jour vos segments en réponse à l’activité des utilisateurs. Une fois qu’un segment a été créé et enregistré, la définition de segment est appliquée aux données entrantes dans Journey Optimizer. Les ajouts et les suppressions de segments sont traités régulièrement, ce qui garantit que votre audience cible reste pertinente.

* Segmentation par lots : la liste des audiences du segment est évaluée toutes les 24 heures. Au lieu d’un processus continu de sélection de données, la segmentation par lots déplace toutes les données de profil à la fois par le biais de définitions de segment afin de produire les audiences correspondantes. Une fois créé, ce segment est enregistré et stocké afin que vous puissiez l’exporter pour l’utiliser.

Le système détermine la segmentation par lots et la segmentation par flux pour chaque définition de segment, en fonction de la complexité et du coût de l’évaluation de la règle de segment.

Vous pouvez afficher la méthode d’évaluation pour chaque segment dans la variable **[!UICONTROL Evaluation method]** de la liste des segments.

Une fois que vous avez défini un segment pour la première fois, les profils sont ajoutés à l’audience lorsqu’ils remplissent les critères.

Le renvoi de l’audience à partir de données antérieures peut prendre jusqu’à 24 heures. Une fois l’audience dépassée, elle est constamment tenue à jour et toujours prête pour le ciblage.
