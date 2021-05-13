---
title: Commencer avec les événements de gestion des décisions
description: Découvrez comment créer des rapports Gestion des décisions dans Adobe Experience Platform.
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '175'
ht-degree: 46%

---

# Commencez avec les événements de gestion des décisions {#monitor-offer-events}

Chaque fois que la Gestion des décisions prend une décision pour un profil donné, les informations relatives à ces événements sont automatiquement envoyées à Adobe Experience Platform.

Vous pouvez ainsi exporter ces données pour les analyser dans votre propre système de rapports. Vous pouvez également utiliser [Query Service](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=fr) d’Adobe Experience Platform en combinaison avec d’autres outils pour améliorer l’analyse et les rapports.

Les jeux de données contenant les événements de gestion de la décision sont accessibles à partir du menu Adobe Experience Platform **[!UICONTROL Datasets]**. Un jeu de données est automatiquement créé lors de l&#39;approvisionnement de chacune de vos instances.

![](../../assets/events-datasets-list.png)

Ces jeux de données sont basés sur le schéma **[!UICONTROL ODE DecisionEvents]**, qui contient tous les champs XDM requis pour envoyer des informations de la gestion des décisions à Adobe Experience Platform.

>[!NOTE]
>
>Notez que les jeux de données ODE DecisionEvents sont **des jeux de données ne concernant pas les profils**, ce qui signifie qu’ils ne peuvent pas être ingérés dans Experience Platform pour être utilisés par le profil client en temps réel.

**Rubriques connexes :**

* [Informations clés des événements de gestion des décisions](../reports/key-information.md)
* [Accès aux champs XDM des événements](../reports/xdm-fields.md)
