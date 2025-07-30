---
solution: Journey Optimizer
product: journey optimizer
title: Définir l’audience d’une campagne d’action
description: Découvrez comment définir l’audience d’une campagne d’action.
feature: Campaigns
topic: Content Management
role: User
level: Beginner
mini-toc-levels: 1
keywords: créer, optimizer, campagne, surface, messages
exl-id: 5635ef04-c69d-4397-9762-7a6f1265d453
source-git-commit: 45c95d5682b35c8afb161b75c88942c010b36d1c
workflow-type: ht
source-wordcount: '196'
ht-degree: 100%

---

# Définir l’audience d’une campagne d’action {#action-campaign-audience}

Utilisez l’onglet **[!UICONTROL Audience]** pour définir l’audience de la campagne.

![](assets/campaign-audience.png)

1. **Sélectionner l’audience**

   Pour les campagnes marketing, cliquez sur le bouton **[!UICONTROL Sélectionner une audience]** pour afficher la liste des audiences Adobe Experience Platform disponibles. [En savoir plus sur les audiences](../audience/about-audiences.md).

   >[!IMPORTANT]
   >
   >L’utilisation d’audiences et d’attributs de la [composition d’audiences](../audience/get-started-audience-orchestration.md) est actuellement indisponible avec Healthcare Shield ou Privacy and Security Shield.

1. **Sélectionner le type d’identité**

   Dans le champ **[!UICONTROL Type d’identité]**, choisissez le type de clé à utiliser pour identifier les personnes dans l’audience sélectionnée. Vous pouvez soit utiliser un type d’identité existant, soit en créer un nouveau à l’aide du service d’identités Adobe Experience Platform. Les espaces de noms d’identité standard sont répertoriés dans [cette page](https://experienceleague.adobe.com/fr/docs/experience-platform/identity/features/namespaces#standard){target="_blank"}.

   Un seul type d’identité est autorisé par campagne. Les personnes appartenant à un segment qui ne dispose pas du type d’identité sélectionné parmi leurs différentes identités ne seront pas ciblées par la campagne. Pour en savoir plus sur les types d’identité et les espaces de noms, consultez la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html?lang=fr){target="_blank"}.

## Étapes suivantes {#next}

Une fois l’audience de votre campagne d’action prête, vous pouvez planifier la campagne. [En savoir plus](campaign-schedule.md)
