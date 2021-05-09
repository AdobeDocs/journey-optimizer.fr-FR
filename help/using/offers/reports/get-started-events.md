---
title: Commencer avec les événements de gestion des décisions
description: Découvrez comment créer des rapports Gestion des décisions dans Adobe Experience Platform.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 0%

---

# Commencez avec les événements de gestion des décisions {#monitor-offer-events}

Chaque fois que la Gestion des décisions prend une décision pour un profil donné, les informations relatives à ces événements sont automatiquement envoyées à Adobe Experience Platform.

Vous pouvez ainsi exporter ces données pour les analyser dans votre propre système de rapports. Vous pouvez également utiliser Adobe Experience Platform [Requête Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html) en combinaison avec d&#39;autres outils pour améliorer l&#39;analyse et les rapports.

Les jeux de données contenant les événements de gestion de la décision sont accessibles à partir du menu Adobe Experience Platform **[!UICONTROL Datasets]**. Un jeu de données est automatiquement créé lors de la mise en service de chacune de vos instances.

![](../assets/events-datasets-list.png)

Ces jeux de données sont basés sur le schéma **[!UICONTROL ODE DecisionEvents]**, qui contient tous les champs XDM requis pour envoyer des informations de la gestion des décisions à Adobe Experience Platform.

>[!NOTE]
>
>Notez que les jeux de données ODE DecisionEvents sont **des jeux de données non profils**, ce qui signifie qu&#39;ils ne peuvent pas être assimilés à des Experience Platform pour être utilisés par le Profil client en temps réel.

**Rubriques connexes :**

* [Informations clés des événements de gestion des décisions](../reports/key-information.md)
* [Champs XDM des événements d&#39;accès](../reports/xdm-fields.md)
