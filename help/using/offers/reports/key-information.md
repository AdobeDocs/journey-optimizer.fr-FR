---
title: Informations clés des événements de gestion des décisions
description: En savoir plus sur les informations clés envoyées avec chaque événement de gestion des décisions.
translation-type: tm+mt
source-git-commit: 4ff255b6b57823a1a4622dbc62b4b8886fd956a0
workflow-type: tm+mt
source-wordcount: '139'
ht-degree: 0%

---

# Informations clés des événements de gestion des décisions {#events-key-information}

Chaque événement envoyé lorsqu&#39;une décision est prise contient quatre points de données clés que vous pouvez exploiter à des fins d&#39;analyse et de rapports.

![](../assets/events-dataset-preview.png)

* **[!UICONTROL Retour arrière]** : Nom et ID de l’offre de secours, si aucune offre personnalisée n’a été sélectionnée,
* **[!UICONTROL Emplacement]** : Nom, ID et canal du placement utilisé pour livrer l&#39;offre,
* **[!UICONTROL Sélections]** : Nom et ID de l&#39;offre sélectionnée pour le profil,
* **[!UICONTROL Activité]** : Nom et ID de la décision (précédemment connue sous le nom d&#39;activité d&#39;offre).

De plus, vous pouvez également utiliser les champs **[!UICONTROL identityMap]** et **[!UICONTROL Timestamp]** pour récupérer des informations sur le profil et le moment où l’offre a été livrée.

Pour plus d&#39;informations sur tous les champs XDM envoyés avec chaque décision, consultez [cette section](xdm-fields.md).
