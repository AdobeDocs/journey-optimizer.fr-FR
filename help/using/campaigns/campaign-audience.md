---
solution: Journey Optimizer
product: journey optimizer
title: Définir l’audience de la campagne d’action
description: Découvrez comment définir l’audience de la campagne d’action.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: créer, optimizer, campagne, surface, messages
source-git-commit: 1bdba8c5c1a9238d351b159551f6d3924935b339
workflow-type: tm+mt
source-wordcount: '196'
ht-degree: 53%

---


# Définir l’audience de la campagne d’action {#action-campaign-audience}

Utilisez l’onglet **[!UICONTROL Audience]** pour définir l’audience de la campagne.

![](assets/campaign-audience.png)

1. **Sélectionnner l’audience**

   Pour les campagnes marketing, cliquez sur le bouton **[!UICONTROL Sélectionner une audience]** pour afficher la liste des audiences Adobe Experience Platform disponibles. [En savoir plus sur les audiences](../audience/about-audiences.md).

   >[!IMPORTANT]
   >
   >L’utilisation des audiences et des attributs de la [composition d’audiences](../audience/get-started-audience-orchestration.md) est actuellement indisponible avec Healthcare Shield ou Privacy and Security Shield.

1. **Sélectionner le type d’identité**

   Dans le champ **[!UICONTROL Type d’identité]**, choisissez le type de clé à utiliser pour identifier les personnes dans l’audience sélectionnée. Vous pouvez soit utiliser un type d’identité existant, soit en créer un nouveau à l’aide du service d’identités Adobe Experience Platform. Les espaces de noms d’identité standard sont répertoriés dans [cette page](https://experienceleague.adobe.com/fr/docs/experience-platform/identity/features/namespaces#standard){target="_blank"}.

   Un seul type d’identité est autorisé par campagne. Les individus appartenant à un segment qui n’a pas le type d’identité sélectionné parmi leurs différentes identités ne peuvent pas être ciblés par la campagne. Pour en savoir plus sur les types d’identité et les espaces de noms, consultez la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=fr){target="_blank"}.

## Étapes suivantes {#next}

Une fois l’audience de votre campagne d’action prête, vous pouvez planifier la campagne. [En savoir plus](campaign-schedule.md)
