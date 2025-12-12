---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main des plans de préchauffage d’adresses IP
description: Découvrez comment mettre en œuvre un plan de préchauffage d’adresses IP.
feature: IP Warmup Plans
topic: Administration
role: Admin
level: Experienced
keywords: IP, délivrabilité
exl-id: 393f051d-b86d-4b4f-b564-7a9ae3a5d4b8
source-git-commit: b1b9b34aec305d6690d93e68238aed852ef689b7
workflow-type: tm+mt
source-wordcount: '367'
ht-degree: 63%

---

# Prise en main des plans de préchauffage d’adresses IP {#ip-warmup-gs}

Avec [!DNL Journey Optimizer], vous pouvez facilement exécuter des workflows de préchauffage d’adresses IP directement à partir de l’interface d’utilisation, et ce d’une manière normalisée et efficace qui respecte les bonnes pratiques pour une délivrabilité optimale. Lorsque vous envoyez des e-mails à l&#39;aide d&#39;une nouvelle plateforme, rien n&#39;est plus suspect pour un FAI (fournisseur d&#39;accès internet) que les adresses IP qui ne sont pas reconnues. Si des e-mails sont subitement envoyés en masse, le FAI les marque souvent comme spam.

Pour éviter que les e-mails soient marqués comme spam, vous pouvez augmenter progressivement le volume envoyé à l’aide de la fonctionnalité du plan de préchauffage d’adresses IP. Cette nouvelle option dans le menu **[!UICONTROL Administration]** vous permet de le faire plus facilement de manière consolidée au lieu de créer des parcours quotidiens complexes.

>[!NOTE]
>
>Avant de mettre en œuvre votre plan de préchauffage d’adresses IP, découvrez les principes fondamentaux de la délivrabilité, la création de réputation et les bonnes pratiques dans ce [guide de délivrabilité du préchauffage d’adresses IP](ip-warmup-deliverability-guide.md).

➡️ [Découvrez comment créer et exécuter un plan de préchauffage d’adresses IP dans cette vidéo](#video)

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

Consultez ces articles de blog utiles pour obtenir des conseils plus détaillés sur le préchauffage des adresses IP :

* [Guide de délivrabilité de Adobe Journey Optimizer : de la réputation zéro à la boîte de réception hero ](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/adobe-journey-optimizer-deliverability-guide-from-zero/ba-p/761950) - Guide complet couvrant les principes de base de la réputation, les calendriers de préchauffage, la surveillance et les bonnes pratiques de dépannage.

* [Comprendre comment configurer le préchauffage d’adresses IP](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warmup-understanding-how-to-set-up-the-ip-warmup/ba-p/761949) - Découvrez les principes de base de la configuration des plans de préchauffage d’adresses IP et les bonnes pratiques pour une implémentation réussie.

* [Fonctionnalités avancées dans les plans de préchauffage d’adresses IP](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/advanced-features-in-ajo-ip-warm-up-plans-granular-controls-for/ba-p/761958) - Découvrez les fonctionnalités avancées et les commandes granulaires pour optimiser votre stratégie de préchauffage d’adresses IP.

* [Résolution des problèmes de préchauffage d’IP](https://experienceleaguecommunities.adobe.com/t5/journey-optimizer-blogs/ajo-ip-warm-up-troubleshooting-audience-delays-and-smart-retry/ba-p/761952) - Trouvez des solutions aux problèmes courants tels que les retards d’audience et découvrez les mécanismes de reprise intelligente.
