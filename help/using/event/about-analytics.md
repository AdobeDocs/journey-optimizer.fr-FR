---
title: À propos des données Adobe Analytics
description: Découvrez comment exploiter les données Adobe Analytics
feature: Événements
topic: Administration
role: Administrator
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '194'
ht-degree: 100%

---

# Utilisation des données Adobe Analytics{#analytics-data}

![](../assets/do-not-localize/badge.png)

>[!NOTE]
>
>Cette section s’applique uniquement aux événements basés sur des règles et aux clients qui doivent utiliser des données Adobe Analytics.

Vous pouvez exploiter toutes les données d’événement comportemental Adobe Analytics que vous capturez déjà et diffusez en continu dans Platform afin de déclencher des parcours et d’automatiser les expériences de vos clients.

Pour que cela fonctionne, vous devez activer, dans Adobe Experience Platform, la suite de rapports que vous souhaitez utiliser :

1. Dans Adobe Experience Platform, sélectionnez **[!UICONTROL Sources]**, puis **[!UICONTROL Ajouter des données]** dans la section Adobe Analytics. La liste des suites de rapports Adobe Analytics disponibles s’affiche.

1. Sélectionnez la suite de rapports à activer, cliquez sur **[!UICONTROL Suivant]** et sur **[!UICONTROL Terminer]**.

1. Partagez l’ID de données source avec votre point de contact de programme Bêta.

Cela active le connecteur source Analytics pour cette suite de rapports. Chaque fois que des données entrent, elles sont transformées en événement d’expérience et envoyées dans Adobe Experience Platform.

![](../assets/jo-event9.png)

Pour plus d’informations sur le connecteur source Adobe Analytics, consultez la [documentation]https://experienceleague.adobe.com/docs/experience-platform/sources/connectors/adobe-applications/analytics.html) et le [tutoriel](https://experienceleague.adobe.com/docs/experience-platform/sources/ui-tutorials/create/adobe-applications/analytics.html?lang=fr).
