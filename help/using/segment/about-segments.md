---
title: À propos des segments Adobe Experience Platform
description: Découvrez comment configurer un segment Adobe Experience Platform
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 10d2de34-23c1-4a5e-b868-700b462312eb
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '386'
ht-degree: 100%

---

# Commencer avec les segments d’Adobe Experience Platform {#about-segments}

[!DNL Journey Optimizer]  vous permet de créer des segments Adobe Experience Platform à l’aide des données de profil client en temps réel directement à partir du menu **[!UICONTROL Segments]** et d’exploiter ces segments dans vos parcours.

Notez que les segments peuvent également être créés à partir du service de segmentation lui-même. Pour en savoir plus, consultez la [documentation du service de segmentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=fr).

Vous pouvez exploiter les segments dans les parcours de différentes manières :

* Utilisez une activité d’orchestration **Lecture de segment** pour que tous les individus appartenant au segment spécifié rejoignent le parcours. Les messages inclus dans votre parcours sont envoyés aux individus appartenant au segment. Supposons que vous ayez un segment « client Silver ». Avec cette activité, vous pouvez faire en sorte que tous les clients Silver rejoignent un parcours et leur envoyer une série de messages personnalisés.

   Pour plus d’informations sur l’utilisation de l’activité **[!UICONTROL Lecture de segment]**, consultez [cette section](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Utilisez l’activité d’événement **Qualification du segment** pour faire en sorte que des individus rejoignent un parcours ou y progressent en fonction des entrées et des sorties de segments Adobe Experience Platform. Par exemple, vous pouvez faire en sorte que tous les nouveaux clients Silver rejoignent un parcours et leur envoyer des messages. Pour plus d’informations sur l’utilisation de cette activité, consultez [cette section](../building-journeys/segment-qualification-events.md).

* Créez des **conditions complexes** dans vos parcours à l’aide de l’éditeur d’expression simple ou avancé. En savoir plus dans [cette section](../building-journeys/condition-activity.md#using-a-segment).

## Méthode d’évaluation dans Adobe Journey Optimizer {#evaluation-method-in-journey-optimizer}

Dans Adobe Journey Optimizer, les audiences sont générées à partir des définitions de segment à l’aide de l’une des méthodes d’évaluation suivantes :

* Segmentation par flux : la liste des audiences du segment est actualisée en temps réel pendant que de nouvelles données affluent dans le système.
* Segmentation par lots : la liste des audiences du segment est mise à jour toutes les heures, en fonction des données arrivées au cours de la dernière heure.

Le système détermine la segmentation par lots et la segmentation par flux pour chaque définition de segment, en fonction de la complexité et du coût de l’évaluation de la règle de segment.

Vous pouvez afficher la méthode d’évaluation pour chaque segment dans la colonne **[!UICONTROL Méthode d’évaluation]** de la liste des segments.

Une fois que vous avez défini un segment pour la première fois, les profils sont ajoutés à l’audience lorsqu’ils remplissent les critères.

Le renvoi de l’audience à partir de données antérieures peut prendre jusqu’à 24 heures. Une fois l’audience renvoyée, elle est constamment tenue à jour et toujours prête pour le ciblage.
