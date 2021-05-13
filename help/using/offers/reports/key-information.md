---
title: Informations clés des événements de gestion des décisions
description: En savoir plus sur les informations clés envoyées avec chaque événement de gestion des décisions.
translation-type: tm+mt
source-git-commit: db7fd318b14d01a0369c934a3e01c6e368d7658d
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 75%

---

# Informations clés des événements de gestion des décisions {#events-key-information}

Chaque événement envoyé lorsqu’une décision est prise contient quatre points de données clés que vous pouvez exploiter à des fins d’analyse et de création de rapports.

![](../../assets/events-dataset-preview.png)

* **[!UICONTROL Fallback]** : Nom et ID de l’offre de secours, si aucune offre personnalisée n’a été sélectionnée,
* **[!UICONTROL Placement]** : Nom, ID et canal du placement utilisé pour diffuser l’offre,
* **[!UICONTROL Selections]** : Nom et ID de l’offre sélectionnée pour le profil,
* **[!UICONTROL Activité]** : Nom et ID de la décision (précédemment connue sous le nom d&#39;activité d&#39;offre).

En outre, vous pouvez également utiliser les champs **[!UICONTROL identityMap]** et **[!UICONTROL Timestamp]** pour récupérer des informations sur le profil et le moment où l’offre a été diffusée.

Pour plus d’informations sur tous les champs XDM envoyés avec chaque décision, consultez [cette section](xdm-fields.md).
