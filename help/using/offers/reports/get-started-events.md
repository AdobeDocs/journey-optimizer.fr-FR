---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Utiliser les événements de gestion des décisions
description: Découvrez comment créer des rapports de gestion des décisions dans Adobe Experience Platform.
badge: label="Hérité" type="Informative"
feature: Decision Management, Datasets
topic: Integrations
role: User, Developer
level: Intermediate
exl-id: 51830c63-fa88-47e7-8605-192297fcf6b8
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/r3bOKyWcAT-sqI7KXA3J-Yi5TUax9KGi-8JY62QD6tA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79id: edbd1a0e-46c8-49da-8c10-dba9ec80bba9
feature_v2: id: c132d929-fa62-4271-803e-b823be07b914id: c20d46e7-1c7d-476c-a50e-3961d4dce35fid: ed0d8d0e-04b9-4326-be72-a0fbca265377id: fe338112-e2ce-4876-8989-fc4d497613f1id: fe96aceb-8194-4a8a-a6b0-75302d02804d
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 321
ht-degree: 100%

---

# Commencer avec les événements de gestion des décisions {#monitor-offer-events}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../../experience-decisioning/gs-experience-decisioning.md)

Chaque fois que la gestion des décisions prend une décision pour un profil donné, les informations relatives à ces événements sont automatiquement envoyées à Adobe Experience Platform.

Cela vous permet d’obtenir des informations sur vos décisions, notamment pour savoir quelle offre a été présentée à un profil donné. Vous pouvez exporter ces données pour les analyser dans votre propre système de rapports ou utiliser le [service de requête](https://experienceleague.adobe.com/docs/experience-platform/query/home.html?lang=fr) Adobe Experience Platform en association avec d’autres outils à des fins d’analyse et de création de rapports améliorées.

## Informations clés disponibles dans les jeux de données {#key-information}

Chaque événement envoyé lorsqu’une décision est prise contient quatre points de données clés que vous pouvez exploiter à des fins d’analyse et de création de rapports :

![](../assets/events-dataset-preview.png)

* **[!UICONTROL Fallback]** : Nom et ID de l&#39;offre de secours, si aucune offre personnalisée n&#39;a été sélectionnée,
* **[!UICONTROL Emplacement]** : Nom, ID et canal du placement utilisé pour diffuser l&#39;offre,
* **[!UICONTROL Selections]** : Nom et ID de l&#39;offre sélectionnée pour le profil,
* **[!UICONTROL Activité]** : Nom et identifiant de la décision.

En outre, vous pouvez également utiliser les champs **[!UICONTROL identityMap]** et **[!UICONTROL Timestamp]** pour récupérer des informations sur le profil et le moment où l&#39;offre a été diffusée.

Pour plus d&#39;informations sur tous les champs XDM envoyés avec chaque décision, consultez [cette section](xdm-fields.md).

## Accéder aux jeux de données {#access-datasets}

Les jeux de données contenant des événements de gestion des décisions sont accessibles à partir du menu **[!UICONTROL Jeux de données]** d’Adobe Experience Platform. Un jeu de données est automatiquement créé lors de l&#39;approvisionnement de chacune de vos instances.

![](../assets/events-datasets-list.png)

Ces jeux de données sont basés sur le schéma **[!UICONTROL ODE DecisionEvents]**, qui contient tous les champs XDM requis pour envoyer des informations de la gestion de décision à Adobe Experience Platform.

>[!NOTE]
>
>Notez que les jeux de données ODE DecisionEvents sont **des jeux de données ne concernant pas les profils**, ce qui signifie qu’ils ne peuvent pas être ingérés dans Experience Platform pour être utilisés par le profil client en temps réel.
