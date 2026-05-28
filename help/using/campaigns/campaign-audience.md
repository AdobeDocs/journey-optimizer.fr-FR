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
TQID: https://experienceleague.adobe.com/3lWwW0Lru2D5D83QqHl48Gsxv7JVKjX8ZBmZAiMFiB0
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a653cc2e-bc85-4353-a306-399e5b247978
subfeature_v2:
  - id: f7479fa1-474b-479d-8c98-f6cee5865a38
  - id: ee67bd4a-25ee-4cdd-9eab-0d7549fde0c6
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: f4e6943a-c91a-4134-a2c7-f4f20cfff2f0
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 210
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
