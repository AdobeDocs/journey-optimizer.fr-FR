---
title: À propos des segments Adobe Experience Platform
description: Découvrez comment configurer un segment Adobe Experience Platform
feature: Parcours
topic: Gestion de contenu
role: User
level: Intermediate
source-git-commit: 2d882b8d10cc642b04705dd924fd2b129f4f78ac
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 100%

---

# Prise en main des segments {#about-segments}

[!DNL Journey Optimizer] vous permet de créer des segments Adobe Experience Platform à l’aide des données de profil client en temps réel directement à partir du menu **[!UICONTROL Segments]** et de les exploiter dans vos parcours.

Notez que les segments peuvent également être créés à partir du service de segmentation lui-même. Pour en savoir plus, consultez la [documentation du service de segmentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=fr){target=&quot;_blank&quot;}.

Vous pouvez exploiter les segments dans les parcours de différentes manières :

* Utilisez une activité d’orchestration **Lecture de segment** pour que tous les individus appartenant au segment spécifié rejoignent le parcours. Les messages inclus dans votre parcours sont envoyés aux individus appartenant au segment. Supposons que vous ayez un segment « client Silver ». Avec cette activité, vous pouvez faire en sorte que tous les clients Silver rejoignent un parcours et leur envoyer une série de messages personnalisés.

   Pour plus d’informations sur l’utilisation de l’activité **[!UICONTROL Lecture de segment]**, consultez [cette section](../building-journeys/read-segment.md#configuring-segment-trigger-activity).

* Utilisez l’activité d’événement **Qualification du segment** pour faire en sorte que des individus rejoignent un parcours ou y progressent en fonction des entrées et des sorties de segments Adobe Experience Platform. Par exemple, vous pouvez faire en sorte que tous les nouveaux clients Silver rejoignent un parcours et leur envoyer des messages. Pour plus d’informations sur l’utilisation de cette activité, consultez [cette section](../building-journeys/segment-qualification-events.md).

* Créez des **conditions complexes** dans vos parcours à l’aide de l’éditeur d’expression simple ou avancé. En savoir plus dans [cette section](../building-journeys/condition-activity.md#using-a-segment).
