---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec les plans de préchauffage d’adresses IP
description: Découvrez comment mettre en œuvre un plan de préchauffage d’adresses IP.
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, délivrabilité
exl-id: 393f051d-b86d-4b4f-b564-7a9ae3a5d4b8
TQID: https://experienceleague.adobe.com/xjJKrCXUmQY5sZu2w-B09agQh-tb4qkSXM0Vh2-TDnc
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: c343082f-e963-4f57-a96b-b64d27f8118e
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
  - id: e30b0a1a-b594-47b8-af94-1e3a2be6df11
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
topic_v2:
  - id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
  - id: c1579802-ddd4-4214-8a91-97b2066abe11
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 459
ht-degree: 100%

---

# Commencer avec les plans de préchauffage d’adresses IP {#ip-warmup-gs}

Avec [!DNL Journey Optimizer], vous pouvez facilement exécuter des workflows de préchauffage d’adresses IP directement à partir de l’interface d’utilisation, et ce d’une manière normalisée et efficace qui respecte les bonnes pratiques pour une délivrabilité optimale. Lorsque vous envoyez des e-mails à l’aide d’une nouvelle plateforme, rien n’est plus suspect pour un FAI (fournisseur d’accès internet) que les adresses IP qui ne sont pas reconnues. Si des e-mails sont subitement envoyés en masse, le FAI les range souvent dans le courrier indésirable.

Pour éviter que les e-mails soient marqués comme spam, vous pouvez augmenter progressivement le volume envoyé à l’aide de la fonctionnalité du plan de préchauffage d’adresses IP. Cette nouvelle option du menu **[!UICONTROL Administration]** permet d’automatiser la gestion des volumes et de simplifier le processus de préchauffage sans configurations de parcours complexes.

>[!NOTE]
>
>Avant de mettre en œuvre votre plan de préchauffage d’adresses IP, découvrez les principes de base de la délivrabilité, la création de la réputation et les bonnes pratiques dans ce [guide de délivrabilité sur le préchauffage d’adresses IP](ip-warmup-deliverability-guide.md).

➡️ [Découvrez comment créer et exécuter un plan de préchauffage d’adresses IP dans cette vidéo](#video).

>[!AVAILABILITY]
>
>Cette fonctionnalité ne peut être activée que sur les sandbox de type production.

<!--
Benefits

* Standardization on Campaign which will be easy for practitioners too > why?

* No more pain of creating queries, audiences and testing those as system will create the audiences. 

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

Les étapes clés de la mise en œuvre d’un plan de préchauffage d’adresses IP sont les suivantes :

1. Vous devez d’abord créer une ou plusieurs campagnes pour lesquelles l’option de préchauffage d’adresses IP est activée. [En savoir plus](ip-warmup-campaign.md)

1. Créez un plan de préchauffage d’adresses IP dans [!DNL Journey Optimizer] et téléchargez la feuille Excel préparée avec l’aide de votre consultant ou consultante en délivrabilité. [En savoir plus](ip-warmup-plan.md)

1. Sélectionnez une campagne pour chaque phase de votre plan et activez les exécutions correspondantes. [En savoir plus](ip-warmup-execution.md)

## Vidéo pratique {#video}

Découvrez comment créer et exécuter un plan de préchauffage des adresses IP.

>[!VIDEO](https://video.tv.adobe.com/v/3432637/?learn=on)

>[!NOTE]
>
>Apprenez-en plus sur la façon d’accroître la réputation de vos e-mails grâce au préchauffage dʼadresses IP dans la section [Guide des bonnes pratiques en matière de délivrabilité](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=fr).

## Ressources supplémentaires {#additional-resources}

Consultez les articles de blog suivants afin d’obtenir des instructions plus détaillées pour le préchauffage des adresses IP :

* [Guide de délivrabilité d’Adobe Journey Optimizer : d’expéditeur inconnu à champion des boîtes de réception](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950) : guide complet qui aborde les principes de base de la réputation, les calendriers de préchauffage, la surveillance et les bonnes pratiques en matière de résolution des problèmes.

* [Comprendre comment configurer le préchauffage d’adresses IP](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warmup-understanding-how-to-set-up-the-ip-warmup/ba-p/761949) : découvrez les principes de base de la configuration des plans de préchauffage d’adresses IP et les bonnes pratiques pour une implémentation réussie.

* [Fonctionnalités avancées dans les plans de préchauffage d’adresses IP](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/advanced-features-in-ajo-ip-warm-up-plans-granular-controls-for/ba-p/761958) : découvrez les fonctionnalités avancées et les contrôles précis vous permettant d’optimiser votre stratégie de préchauffage d’adresses IP.

* [Résolution des problèmes de préchauffage d’adresses IP](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warm-up-troubleshooting-audience-delays-and-smart-retry/ba-p/761952) : trouvez des solutions aux problèmes les plus courants tels que les retards d’audience, et découvrez les mécanismes de reprise intelligente.
