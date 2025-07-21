---
solution: Journey Optimizer
product: journey optimizer
title: Planifier la campagne d’action
description: Découvrez comment planifier la campagne d’action.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: créer, optimizer, campagne, surface, messages
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '272'
ht-degree: 32%

---


# Planifier la campagne d’action {#action-campaign-schedule}

Utilisez l&#39;onglet **[!UICONTROL Planning]** pour définir le planning de la campagne.

Par défaut, les campagnes d’action démarrent une fois qu’elles sont activées manuellement et se terminent dès que le message a été envoyé une fois. Si vous ne souhaitez pas exécuter votre campagne juste après son activation, vous pouvez spécifier la date et l’heure auxquelles le message doit être envoyé à l’aide de l’option **[!UICONTROL Début de campagne]**.

L’option **[!UICONTROL Fin de campagne]** vous permet de spécifier le moment où une campagne doit cesser d’être exécutée. En dehors des dates spécifiées, la campagne ne sera pas exécutée.

![](assets/create-campaign-schedule.png)

>[!NOTE]
>
>Lors de la planification de campagnes dans [!DNL Adobe Journey Optimizer], assurez-vous que la date/l’heure de début correspond à la première diffusion souhaitée. Pour les campagnes récurrentes, si l’heure planifiée initiale est déjà dépassée, les campagnes sont reportées au prochain créneau horaire disponible en fonction de leurs règles de périodicité.

D&#39;autres options de planification sont disponibles en fonction du canal de la campagne :

* **Fréquence** (e-mail, SMS, action Push)

  Vous pouvez définir la fréquence d’envoi du message de la campagne. Pour ce faire, utilisez la méthode **[!UICONTROL Déclencheurs d’action]** dans l’écran de création de la campagne pour indiquer si la campagne doit être exécutée tous les jours, toutes les semaines ou tous les mois.

* **Activation du plan de préchauffage d’adresses IP** (e-mail)

  Pour les campagnes par e-mail, vous pouvez créer des campagnes d’activation de plan de préchauffage d’adresses IP spécifiques. Le planning de la campagne sera piloté par le plan de préchauffage d’adresses IP auquel il sera associé, ce qui signifie que le planning n’est plus défini dans la campagne elle-même. [Découvrez comment créer des campagnes de préchauffage d’adresses IP](../configuration/ip-warmup-campaign.md).

## Étapes suivantes {#next}

Une fois que le planning de votre campagne est prêt, vous pouvez vérifier et activer la campagne. [En savoir plus](review-activate-campaign.md)
