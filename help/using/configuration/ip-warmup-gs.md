---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main des plans de chauffage des adresses IP
description: Découvrez comment mettre en oeuvre un plan de chauffage par IP
feature: Application Settings
topic: Administration
role: Admin
level: Experienced
keywords: IP, délivrabilité
hide: true
hidefromtoc: true
source-git-commit: b3e5a825b881736516b3bcd1d368843c3a601100
workflow-type: tm+mt
source-wordcount: '295'
ht-degree: 25%

---

# Prise en main des plans de chauffage des adresses IP {#ip-warmup-gs}

<!--
>[!CONTEXTUALHELP]
>id="ajo_admin_ip_warmup_plan"
>title="Define your IP warmup plan"
>abstract="You can perform IP warmup workflows directly from the Journey Optimizer interface in a standardized and efficient way that follows the best practices for optimal deliverability."
-->

>[!BEGINSHADEBOX]

Ce guide vous apportera la documentation suivante :

* **[Prise en main du réchauffement des adresses IP](ip-warmup-gs.md)**
* [Créer des campagnes de réchauffement des adresses IP](ip-warmup-campaign.md)
* [Créer une formule de chauffage des adresses IP](ip-warmup-plan.md)
* [Exécution de la formule de chauffage par IP](ip-warmup-execution.md)

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>La fonctionnalité de réchauffement des adresses IP est actuellement disponible en version bêta pour sélectionner uniquement les utilisateurs. Pour rejoindre le programme Beta, contactez l’assistance clientèle d’Adobe.

Avec [!DNL Journey Optimizer], vous pouvez facilement exécuter des workflows de chauffage des adresses IP directement à partir de l’interface utilisateur d’une manière normalisée et efficace, en respectant les bonnes pratiques pour une délivrabilité optimale.

>[!CAUTION]
>
>Cette fonctionnalité s&#39;applique uniquement au canal e-mail.

Lorsque vous envoyez des emails à l&#39;aide d&#39;une nouvelle plateforme, rien n&#39;est plus suspect pour un FAI (fournisseur d&#39;accès internet) que les adresses IP qui ne sont pas reconnues. Si des emails sont subitement envoyés en masse, le FAI les range souvent dans le courrier indésirable.

Pour éviter que les emails soient marqués comme spam, vous pouvez augmenter progressivement le volume envoyé à l’aide de la fonctionnalité de plan de réchauffement des adresses IP . Cette nouvelle option dans la variable **[!UICONTROL Administration]** vous permet de le faire plus facilement de manière consolidée au lieu de créer des parcours quotidiens complexes. Cela devrait garantir un développement fluide de la phase de démarrage et vous permettre de réduire le taux global d&#39;adresses invalides.

>[!NOTE]
>
>En savoir plus sur l’amélioration de la réputation de vos emails grâce au réchauffement des adresses IP dans la section [Guide des bonnes pratiques de délivrabilité](https://experienceleague.adobe.com/docs/deliverability-learn/deliverability-best-practice-guide/additional-resources/generic-resources/increase-reputation-with-ip-warming.html?lang=fr).

<!--
Benefits

* Standardization on Campaign which will be easy for practitioners too > why?

* No more pain of creating queries, audiences and testing those as system will create the audiences. 

* Ease of excluding domains and changing the plan with help of simple toggles to exclude OR by editing numbers inline or create new phases or reupload plan if drastic change. No more pain of editing audience definitions, journey conditions

* There is an expectation that with this, it will ease around 30% of effort and will be much better experience for consultant/partner/practitioner - right from planning to execution to reporting
-->

Les étapes clés de la mise en oeuvre d’un plan de chauffage par IP sont les suivantes :

1. Vous devez d’abord créer une ou plusieurs campagnes pour lesquelles l’option de réchauffement des adresses IP est activée. [En savoir plus](ip-warmup-campaign.md)

1. Créer un plan de chauffage par IP dans [!DNL Journey Optimizer] et téléchargez la feuille Excel préparée avec l’aide de votre consultant en délivrabilité. [En savoir plus](ip-warmup-plan.md)

1. Sélectionnez une opération pour chaque phase de votre plan et activez les exécutions correspondantes. [En savoir plus](ip-warmup-execution.md)
