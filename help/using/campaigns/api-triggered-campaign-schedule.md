---
solution: Journey Optimizer
product: journey optimizer
title: Planifier une campagne déclenchée par API
description: Découvrez comment planifier une campagne déclenchée par API.
feature: Campaigns, API
topic: Content Management
role: Developer
level: Experienced
keywords: campagnes, déclenchement par API, REST, optimizer, messages
exl-id: e04b0d38-6b3d-4086-a0f0-c1b8f6d9634f
source-git-commit: 3aa3203ae7763d81288cb70a2984d017b0006bb3
workflow-type: tm+mt
source-wordcount: '226'
ht-degree: 64%

---

# Planifier la campagne déclenchée par API {#api-schedule}

Utilisez l’onglet **[!UICONTROL Planifier]** pour définir le planning de la campagne.

## Définir les dates de début et de fin

Par défaut, les campagnes déclenchées par API démarrent après avoir été déclenchées et se terminent dès que le message a été envoyé une fois. Si vous ne souhaitez pas exécuter votre campagne juste après son déclenchement, vous pouvez spécifier la date et l’heure auxquelles le message doit être envoyé à l’aide de l’option **[!UICONTROL Début de campagne]**.

L’option **[!UICONTROL Fin de la campagne]** vous permet de spécifier le moment où une campagne doit arrêter son exécution. En dehors des dates spécifiées, la campagne ne sera pas exécutée.

![](assets/api-triggered-schedule.png)

>[!NOTE]
>
>Lors de la planification de campagnes dans [!DNL Adobe Journey Optimizer], vérifiez que la date/l’heure de début correspond à la première diffusion souhaitée.

## Régler le contrôle des taux

[!DNL Journey Optimizer] vous permet d’activer le contrôle des taux pour les actions sortantes (e-mails, SMS, notifications push).

Cette fonctionnalité est particulièrement utile pour éviter la surcharge sur les systèmes en aval, tels que les pages de destination ou les plateformes d’assistance clientèle. Par exemple, vous pouvez définir une limite de débit de 165 messages par seconde pour garantir une diffusion régulière sans surcharger les systèmes en aval.

Pour définir le contrôle des taux, activez l’option **[!UICONTROL Ralentir la diffusion]** dans la section **[!UICONTROL Paramètres de diffusion]** et spécifiez le **[!UICONTROL Taux de diffusion]** souhaité.

![](assets/throttling-rate-control.png)

## Étapes suivantes {#next}

Une fois la configuration et le contenu de votre campagne prêts, vous pouvez les vérifier, puis les activer. [En savoir plus](review-activate-campaign.md)
