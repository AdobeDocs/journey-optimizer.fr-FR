---
title: Informations clés sur les événements de gestion de décision
description: En savoir plus sur les informations clés envoyées avec chaque événement de gestion de la décision.
feature: Offers
topic: Integrations
role: User
level: Intermediate
exl-id: 07be59e8-e994-4854-8089-25614d005dbe
source-git-commit: 882b99d9b49e1ae6d0f97872a74dc5a8a4639050
workflow-type: tm+mt
source-wordcount: '128'
ht-degree: 0%

---

# Informations clés sur les événements de gestion de décision {#events-key-information}

Chaque événement envoyé lorsqu’une décision est prise contient quatre points de données clés que vous pouvez exploiter à des fins d’analyse et de création de rapports.

![](../assets/events-dataset-preview.png)

* **[!UICONTROL Fallback]**: Nom et identifiant de l’offre de secours, si aucune offre personnalisée n’a été sélectionnée,
* **[!UICONTROL Placement]**: Nom, identifiant et canal de l&#39;emplacement utilisé pour diffuser l&#39;offre,
* **[!UICONTROL Selections]**: Nom et identifiant de l&#39;offre sélectionnée pour le profil,
* **[!UICONTROL Activity]**: Nom et ID de la décision.

De plus, vous pouvez également utiliser la variable **[!UICONTROL identityMap]** et **[!UICONTROL Timestamp]** pour récupérer des informations sur le profil et l’heure à laquelle l’offre a été diffusée.

Pour plus d’informations sur tous les champs XDM envoyés avec chaque décision, reportez-vous à la section [cette section](xdm-fields.md).
