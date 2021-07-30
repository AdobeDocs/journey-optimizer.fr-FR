---
title: Informations clés des événements de gestion de décision
description: En savoir plus sur les informations clés envoyées avec chaque événement de gestion de décision.
feature: Offres
topic: Intégrations
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '141'
ht-degree: 100%

---

# Informations clés des événements de gestion de décision {#events-key-information}

Chaque événement envoyé lorsqu&#39;une décision est prise contient quatre points de données clés que vous pouvez exploiter à des fins d&#39;analyse et de création de rapports.

![](../../assets/events-dataset-preview.png)

* **[!UICONTROL Fallback]** : Nom et ID de l&#39;offre de secours, si aucune offre personnalisée n&#39;a été sélectionnée,
* **[!UICONTROL Emplacement]** : Nom, ID et canal du placement utilisé pour diffuser l&#39;offre,
* **[!UICONTROL Selections]** : Nom et ID de l&#39;offre sélectionnée pour le profil,
* **[!UICONTROL Activité]** : Nom et identifiant de la décision (précédemment appelée activité d&#39;offre).

En outre, vous pouvez également utiliser les champs **[!UICONTROL identityMap]** et **[!UICONTROL Timestamp]** pour récupérer des informations sur le profil et le moment où l&#39;offre a été diffusée.

Pour plus d&#39;informations sur tous les champs XDM envoyés avec chaque décision, consultez [cette section](xdm-fields.md).
