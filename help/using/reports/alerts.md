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
source-git-commit: 78085934a00f4e365b49012b426e57a218bf48ba
workflow-type: tm+mt
source-wordcount: '461'
ht-degree: 14%

---

# Prise en main des alertes {#alerts}

## Fonctionnalités des alertes {#alerting-capabilities}

Vous pouvez accéder aux alertes système par le biais de l’interface utilisateur ou recevoir un courrier électronique en cas d’échec. Dans la **Alertes** , vous pouvez afficher les alertes disponibles et vous abonner à celles-ci. Lorsqu’un certain ensemble de conditions de vos opérations est atteint (par exemple, un problème potentiel lorsque le système enfreint un seuil), des messages d’alerte sont envoyés à tous les utilisateurs de votre organisation qui s’y sont abonnés.

<!--These messages can repeat over a pre-defined time interval until the alert has been resolved.-->

En savoir plus sur les alertes dans Adobe Experience Platform [Documentation Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/overview.html?lang=fr){target="_blank"}.

Dans le menu de gauche, sous **Administration**, cliquez sur **Alertes**. Deux alertes préconfigurées pour Journey Optimizer sont disponibles : [Échec de l’action personnalisée parcours](#alert-custom-actions) et la variable [Lecture du déclencheur de segment infructueuse](#alert-read-audiences) alerte Ces alertes sont détaillées ci-dessous.

Vous pouvez vous abonner individuellement à chaque alerte depuis l’interface utilisateur en sélectionnant l’option **Abonner** de l’option **Alertes** tableau de bord. Utilisez la même méthode pour vous désabonner.

![](assets/alert-subscribe.png)

Vous pouvez également vous abonner aux alertes par le biais de [Notifications d’événements d’E/S](https://experienceleague.adobe.com/docs/experience-platform/observability/alerts/subscribe.html?lang=fr){target="_blank"}. Les règles d’alerte sont organisées en différents packages d’abonnement. Les abonnements aux événements correspondant aux alertes Journey Optimizer spécifiques sont présentés ci-dessous.

Si un comportement inattendu se produit, une notification d’alerte est envoyée aux abonnés. Selon les préférences de l’utilisateur, les alertes sont envoyées par courrier électronique ou directement dans le centre de notification Journey Optimizer, dans le coin supérieur droit de l’interface utilisateur.

Lorsqu’une alerte est résolue, les abonnés reçoivent une notification &quot;Résolue&quot;.

>[!CAUTION]
>
>Les alertes spécifiques à Adobe Journey Optimizer s’appliquent uniquement à **live** parcours. Les alertes ne sont pas déclenchées pour les parcours en mode test.

## Échec de l’action personnalisée parcours {#alert-custom-actions}

Cette alerte vous avertit si une action personnalisée échoue. Nous considérons qu’il existe un échec quand plus de 1 % d’erreurs sont commises sur une action personnalisée spécifique au cours des 5 dernières minutes. Ces données sont évaluées toutes les 30 secondes.

![](assets/alerts-custom-action.png)

Les alertes relatives aux actions personnalisées sont résolues lorsque, au cours des 5 dernières minutes :

* il n&#39;y a pas eu d&#39;erreur sur cette action personnalisée (ou d&#39;erreur sous le seuil de 1 %),

* ou, aucun profil n’a atteint cette action personnalisée.

Le nom d’abonnement à l’événement d’E/S correspondant à l’alerte d’action personnalisée est **Échec de l’action personnalisée parcours**.

## Lecture du déclencheur de segment infructueuse {#alert-read-audiences}

Cette alerte vous avertit si une **Lecture d’audience** l’activité n’a traité aucun profil 10 minutes après l’heure planifiée de l’exécution. Cet échec peut être dû à des problèmes techniques ou parce que l’audience est vide.

![](assets/alerts1.png)

Alertes sur **Lecture d’audience** Les activités ne s’appliquent qu’aux parcours récurrents. **Lecture d’audience** activités dans des parcours actifs dont l’exécution est planifiée **Une fois** ou **Dès que possible** sont ignorées.

Alertes sur **Lecture d’audience** sont résolus lorsqu’un profil entre dans la variable **Lecture d’audience** noeud .

Nom de l’abonnement à l’événement I/O correspondant à la variable **Lecture du déclencheur de segment infructueuse** alerte **Lecture par parcours des segments Retards, échecs et erreurs**.
