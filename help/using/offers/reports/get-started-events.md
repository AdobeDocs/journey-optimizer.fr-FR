---
title: Prise en main des événements de gestion de la décision
description: Découvrez comment créer des rapports de gestion de la décision dans Adobe Experience Platform.
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '167'
ht-degree: 0%

---

# Prise en main des événements de gestion de la décision {#monitor-offer-events}

Chaque fois que la gestion de la décision prend une décision pour un profil donné, les informations relatives à ces événements sont automatiquement envoyées à Adobe Experience Platform.

Vous pouvez ainsi exporter ces données pour les analyser dans votre propre système de création de rapports. Vous pouvez également tirer parti d’Adobe Experience Platform [Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html) en combinaison avec d’autres outils à des fins d’analyse et de création de rapports améliorées.

Les jeux de données contenant des événements de gestion de la décision sont accessibles à partir d’Adobe Experience Platform. **[!UICONTROL Datasets]** . Un jeu de données est automatiquement créé lors de la mise en service de chacune de vos instances.

![](../assets/events-datasets-list.png)

Ces jeux de données reposent sur la variable **[!UICONTROL ODE DecisionEvents]** schéma, qui contient tous les champs XDM requis pour envoyer des informations de la gestion de la décision à Adobe Experience Platform.

>[!NOTE]
>
>Notez que les jeux de données ODE DecisionEvents sont **jeux de données non liés au profil**, ce qui signifie qu’elles ne peuvent pas être ingérées dans Experience Platform pour être utilisées par Real-time Customer Profile.

**Rubriques connexes :**

* [Informations clés sur les événements de gestion de décision](../reports/key-information.md)
* [Accès aux champs XDM des événements](../reports/xdm-fields.md)
