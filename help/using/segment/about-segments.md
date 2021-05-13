---
title: À propos des segments Adobe Experience Platform
description: Découvrez comment configurer un segment Adobe Experience Platform
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '227'
ht-degree: 22%

---

# À propos des segments Adobe Experience Platform {#about-segments}

![](../assets/do-not-localize/badge.png)

Journey Optimizer vous permet de créer des segments Adobe Experience Platform à l’aide des données du Profil client en temps réel directement à partir du menu **[!UICONTROL Segments]** et de les exploiter dans vos parcours.

Notez que les segments peuvent également être créés à partir du service de segmentation lui-même. Pour en savoir plus, consultez la [documentation de Adobe Experience Platform Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=fr).

Vous pouvez exploiter les segments de différentes manières dans les parcours :

* Utilisez une activité d&#39;orchestration **Read segment** pour faire entrer dans le parcours toutes les personnes appartenant au segment spécifié. Les messages inclus dans votre parcours sont envoyés aux personnes appartenant au segment. Supposons que vous ayez un segment « client Silver ». Avec cette activité, vous pouvez faire entrer tous les clients argentés dans un parcours et leur envoyer une série de messages personnalisés.

   Pour plus d&#39;informations sur l&#39;utilisation de l&#39;activité **[!UICONTROL Lire le segment]**, consultez [cette section](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Utilisez l&#39;activité de événement **Qualification de segment** pour faire entrer ou avancer des individus dans un parcours en fonction des entrées et sorties de segments Adobe Experience Platform. Par exemple, vous pouvez faire entrer tous les nouveaux clients argentés dans un parcours et leur envoyer des messages. Pour plus d’informations sur l’utilisation de cette activité, consultez [cette section](../building-journeys/segment-qualification-events.md).

* Créez des **conditions complexes** dans vos parcours à l’aide de l’éditeur d’expressions simple ou avancé. En savoir plus dans [cette section](../building-journeys/condition-activity.md#using-a-segment).
