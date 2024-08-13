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
source-git-commit: 34c1180e3ba5b6b39287e70651c45351fa71e6b1
workflow-type: tm+mt
source-wordcount: '240'
ht-degree: 70%

---

# Prise en main des plans de préchauffage d’adresses IP {#ip-warmup-gs}

Avec [!DNL Journey Optimizer], vous pouvez facilement exécuter des workflows de chauffage des adresses IP directement à partir de l’interface utilisateur d’une manière normalisée et efficace, en respectant les bonnes pratiques pour une délivrabilité optimale. Lorsque vous envoyez des e-mails à l&#39;aide d&#39;une nouvelle plateforme, rien n&#39;est plus suspect pour un FAI (fournisseur d&#39;accès internet) que les adresses IP qui ne sont pas reconnues. Si des e-mails sont subitement envoyés en masse, le FAI les marque souvent comme spam.

Pour éviter que les e-mails soient marqués comme spam, vous pouvez augmenter progressivement le volume envoyé à l’aide de la fonctionnalité du plan de préchauffage d’adresses IP. Cette nouvelle option dans le menu **[!UICONTROL Administration]** vous permet de le faire plus facilement de manière consolidée au lieu de créer des parcours quotidiens complexes.

<!--➡️ [Learn how to create and execute an IP warmup plan in this video](#video)-->

>[!AVAILABILITY]
>
>Cette fonctionnalité ne peut être activée que sur les environnements de test de type production.
>
>Elle n’est pas disponible pour les organisations qui ont acheté les modules complémentaires **Bouclier de santé** ou **Bouclier de protection et de confidentialité** de l’Adobe.



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

<!--Old UI
## How-to video {#video}

Learn how to create and execute an IP warmup plan.

>[!VIDEO](https://video.tv.adobe.com/v/3425965/?quality=12&learn=on)
-->


>[!NOTE]
>
>Pour en savoir plus sur l&#39;amélioration de la réputation de vos emails grâce au réchauffement des adresses IP, consultez le [guide des bonnes pratiques de délivrabilité](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=fr).
