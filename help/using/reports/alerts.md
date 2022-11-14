---
solution: Journey Optimizer
product: journey optimizer
title: Alertes
description: Découvrez comment gérer les alertes.
feature: Alerts
topic: Administration
role: Admin
level: Intermediate
exl-id: 0855ca5b-c7af-41c4-ad51-bed820ae5ecf
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '275'
ht-degree: 84%

---

# Prise en main des alertes {#alerts}

Journey Optimizer exploite les fonctionnalités d’alerte d’Adobe Experience Platform. Vous pouvez ainsi accéder aux alertes système à travers l’interface utilisateur. Vous pouvez afficher les alertes disponibles et vous y abonner. Lorsqu’un certain ensemble de conditions de vos opérations est atteint (par exemple, un problème potentiel lorsque le système dépasse un certain seuil), des messages d’alerte sont envoyés à tous les utilisateurs de votre organisation qui se sont abonnés à ces messages. Ces messages peuvent se répéter pendant un intervalle prédéfini jusqu’à ce que l’alerte ait été résolue.

En savoir plus sur les alertes dans la [documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=fr) d’Adobe Experience Platform.
Pour découvrir comment vous abonner à des alertes et les configurer, reportez-vous à cette [page](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html?lang=fr).

Dans le menu de gauche, sous **Administration**, cliquez sur **Alertes**. Une alerte préconfigurée pour Journey Optimizer est disponible. Cette alerte vous avertit si un nœud de segment lu n’a traité aucun profil pendant la période définie.

![](assets/alerts1.png)

Si un tel comportement inattendu se produit, une notification d’alerte est envoyée aux abonnés de l’alerte par courrier électronique, dans le coin supérieur droit de l’interface.

![](assets/alerts2.png)

When [affichage des règles d’alerte dans l’interface utilisateur de Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html), vous pouvez vous abonner à chaque règle individuellement. Toutefois, lorsque vous vous abonnez à des alertes par le biais des [Notifications d’événements I/O](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html?lang=fr), les règles d’alerte sont organisées en différents packages d’abonnement. Le nom d’abonnement à l’événement d’E/S correspondant à l’alerte Lecture de segment est le suivant : « Retards, échecs et erreurs dans les segments de lecture par parcours ».

>[!WARNING]
>
>Ces alertes s’appliquent uniquement aux parcours dynamiques. Les alertes ne seront pas déclenchées pour les parcours en mode test.
