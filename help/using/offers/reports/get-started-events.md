---
title: Prise en main des événements de gestion de décision
description: Découvrez comment créer des rapports de gestion de décision dans Adobe Experience Platform.
feature: Offers
topic: Integrations
role: User
level: Beginner
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 100%

---

# Guide du développeur de l&#39;API de gestion des décisions {#monitor-offer-events}

Chaque fois que la gestion de décision prend une décision pour un profil donné, les informations relatives à ces événements sont automatiquement envoyées à Adobe Experience Platform.

Vous pouvez ainsi exporter ces données pour les analyser dans votre propre système de rapports. Vous pouvez également utiliser [Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=fr) d’Adobe Experience Platform en combinaison avec d’autres outils pour améliorer l’analyse et les rapports.

Les jeux de données contenant des événements de gestion de décision sont accessibles à partir du menu **[!UICONTROL Jeux de données]** d’Adobe Experience Platform. Un jeu de données est automatiquement créé lors de l&#39;approvisionnement de chacune de vos instances.

![](../assets/events-datasets-list.png)

Ces jeux de données sont basés sur le schéma **[!UICONTROL ODE DecisionEvents]**, qui contient tous les champs XDM requis pour envoyer des informations de la gestion de décision à Adobe Experience Platform.

>[!NOTE]
>
>Notez que les jeux de données ODE DecisionEvents sont **des jeux de données ne concernant pas les profils**, ce qui signifie qu’ils ne peuvent pas être ingérés dans Experience Platform pour être utilisés par le profil client en temps réel.

**Rubriques connexes :**

* [Informations clés sur les événements de gestion de décision](../reports/key-information.md)
* [Accès aux champs XDM des événements](../reports/xdm-fields.md)
