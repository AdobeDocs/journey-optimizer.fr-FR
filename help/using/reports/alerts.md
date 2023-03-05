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
source-git-commit: 1832f3395b07580e62f32c886a0a4256267b2970
workflow-type: ht
source-wordcount: '258'
ht-degree: 100%

---

# Prise en main des alertes {#alerts}

Journey Optimizer exploite les fonctionnalités d’alerte d’Adobe Experience Platform. Vous pouvez ainsi accéder aux alertes système à travers l’interface utilisateur. Vous pouvez afficher les alertes disponibles et vous y abonner.

Lorsqu’un certain ensemble de conditions de vos opérations est atteint (par exemple, un problème potentiel lorsque le système dépasse un certain seuil), des messages d’alerte sont envoyés à tous les utilisateurs de votre organisation qui se sont abonnés à ces messages. Ces messages peuvent se répéter pendant un intervalle prédéfini jusqu’à ce que l’alerte ait été résolue.

En savoir plus sur les alertes dans la [documentation](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=fr) d’Adobe Experience Platform.
Pour découvrir comment vous abonner à des alertes et les configurer, reportez-vous à cette [page](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html?lang=fr).

>[!AVAILABILITY]
>
>Certaines modifications de conception sont en cours pour l’alerte « Échec du déclenchement de la lecture de segment ». Par conséquent, cette alerte est suspendue pour l’instant et a été temporairement supprimée de l’IU. Une fois ces modifications publiées, l’alerte sera de nouveau disponible et vous pourrez vous y abonner.

Dans le menu de gauche, sous **Administration**, cliquez sur **Alertes**.

<!--A pre-configured alert for Journey Optimizer is available. This alert will warn you if a read segment node has not processed any profile during the defined time frame.

![](assets/alerts1.png)-->

Si un comportement inattendu se produit, une notification d’alerte est envoyée aux abonnés de l’alerte par e-mail, dans le coin supérieur droit de l’interface.

<!--![](assets/alerts2.png)-->


Lors de l’[affichage des règles d’alerte dans l’interface utilisateur d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/ui.html?lang=fr), vous pouvez vous abonner à chaque règle. Toutefois, lorsque vous vous abonnez à des alertes par le biais des [Notifications d’événements I/O](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html?lang=fr), les règles d’alerte sont organisées en différents packages d’abonnement.

<!--The I/O event subscription name corresponding to the Read segment alert is: "Journey read segment Delays, Failures and Errors".

>[!WARNING]
>
>These alerts apply only to live journeys. Alerts will not be triggered for journeys in test mode.-->
