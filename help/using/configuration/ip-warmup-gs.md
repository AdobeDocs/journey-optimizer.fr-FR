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
hide: true
hidefromtoc: true
badge: label="Version Beta"
exl-id: 393f051d-b86d-4b4f-b564-7a9ae3a5d4b8
source-git-commit: 9d48213d8367fdc6c0fae62b73d1706bc4983d9d
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 91%

---

# Prise en main des plans de préchauffage d’adresses IP {#ip-warmup-gs}

>[!BEGINSHADEBOX]

Ce guide couvre les sujets suivants :

* **[Prise en main du préchauffage d’adresses IP](ip-warmup-gs.md)**
* [Créer des campagnes de préchauffage d’adresses IP](ip-warmup-campaign.md)
* [Créer un plan de préchauffage d’adresses IP](ip-warmup-plan.md)
* [Exécuter le plan de préchauffage d’adresses IP](ip-warmup-execution.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>La fonctionnalité de préchauffage d’adresses IP est actuellement disponible en version bêta pour certains utilisateurs ou utilisatrices uniquement. Pour rejoindre le programme Beta, contactez l’assistance clientèle d’Adobe.

Avec [!DNL Journey Optimizer], vous pouvez facilement exécuter des workflows de préchauffage d’adresses IP directement à partir de l’interface utilisateur d’une manière normalisée et efficace, en respectant les bonnes pratiques pour une délivrabilité optimale.

➡️ [Découvrez comment créer et exécuter un plan de chauffage par IP dans cette vidéo](#video)

>[!CAUTION]
>
>Cette fonctionnalité s&#39;applique uniquement au canal e-mail.

Lorsque vous envoyez des e-mails à l&#39;aide d&#39;une nouvelle plateforme, rien n&#39;est plus suspect pour un FAI (fournisseur d&#39;accès internet) que les adresses IP qui ne sont pas reconnues. Si des e-mails sont subitement envoyés en masse, le FAI les marque souvent comme spam.

Pour éviter que les e-mails soient marqués comme spam, vous pouvez augmenter progressivement le volume envoyé à l’aide de la fonctionnalité du plan de préchauffage d’adresses IP. Cette nouvelle option dans le menu **[!UICONTROL Administration]** vous permet de le faire plus facilement de manière consolidée au lieu de créer des parcours quotidiens complexes.

>[!NOTE]
>
>Apprenez-en plus sur la façon d’accroître la réputation de vos e-mails grâce au préchauffage dʼadresses IP dans la section [Guide des bonnes pratiques en matière de délivrabilité](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=fr).

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

Découvrez comment créer et exécuter un plan de chauffage par IP.

>[!VIDEO](https://video.tv.adobe.com/v/3425965/?quality=12&learn=on)
