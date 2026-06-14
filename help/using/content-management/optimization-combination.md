---
solution: Journey Optimizer
product: journey optimizer
title: Combiner ciblage et expérimentation
description: Découvrez comment combiner le ciblage et les expériences dans un seul parcours ou une seule campagne afin de créer des stratégies d’optimisation sophistiquées.
role: User
level: Intermediate
keywords: optimisation, ciblage, expérimentation, combinaison, avancé
exl-id: dafcb4d3-e33c-40c5-a5c6-972822a23cc0
TQID: https://experienceleague.adobe.com/klXmy7KQLcIHm-T6BMS1RaMKrwzdCfzvK3KK6fUs7KU
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1
feature_v2: []
subfeature_v2: id: f29a52db-c90c-4345-902e-b586d1406d8d
source-git-commit: dc3ac795cd3cbfbd3dd3adfe6f220641d331081f
workflow-type: tm+mt
source-wordcount: 331
ht-degree: 85%

---

# Combiner ciblage et expérimentation {#combination}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment combiner le ciblage et l’expérimentation dans un seul parcours ou une seule campagne afin que les expériences restent spécifiques à chaque règle de ciblage.

>[!ENDSHADEBOX]

Journey Optimizer permet également de combiner le ciblage et les expériences au sein d’un seul parcours ou d’une seule campagne afin de créer des stratégies plus sophistiquées.

En effet, il est possible d’utiliser le ciblage pour créer plusieurs variantes et, pour chacune d’elles, de recourir à l’expérimentation afin d’optimiser davantage chaque contenu. Cela garantit que les expériences sont propres à chaque règle de ciblage et ne s’étendent pas aux variantes.

Par exemple, il est possible de tester une « promotion -50 % » par rapport à une « carte-cadeau de 50 $ » pour la clientèle américaine, et d’exécuter un test différent pour la clientèle européenne, comme « livraison gratuite pour toute commande supérieure à 50 € » par rapport à « 20 % de réduction sur l’achat suivant ».

Pour combiner le ciblage et les expériences dans un parcours ou une campagne, suivez les étapes ci-dessous.

1. Créez un parcours ou une campagne où plusieurs règles de ciblage sont définies. [Voici comment procéder](optimization-targeting.md)

   ![](../campaigns/assets/msg-optimization-create-targeting.png){width=85%}

1. Créez une expérience pour la première règle de ciblage.

1. Concevez et configurez votre expérience de contenu selon vos besoins. [Voici comment procéder](../content-management/content-experiment.md)

   ![](../campaigns/assets/msg-optimization-targeting-with-experiment.png){width=85%}

   Une fois l’expérience définie, elle s’applique uniquement à la première règle de ciblage.

1. De retour dans l’onglet **[!UICONTROL Actions]**, sélectionnez **[!UICONTROL Modifier le contenu]**.

1. Pour le groupe défini par la première règle de ciblage, il est possible de définir du contenu spécifique pour chaque variante de l’expérience.

   Si plusieurs actions entrantes sont ajoutées au parcours ou à la campagne, la même combinaison de ciblage et d’expérience s’applique à chaque action. Cependant, un contenu spécifique doit être défini pour chaque variante de chaque action.

   ![](../campaigns/assets/msg-optimization-targeting-experiment-design.png){width=85%}

1. Procédez de la même manière pour les autres règles de ciblage et concevez le contenu correspondant pour chaque variante.

1. Enregistrez vos modifications et [activez](../campaigns/review-activate-campaign.md) votre parcours ou campagne.

Une fois la campagne ou le parcours actif, les utilisateurs et utilisatrices de chaque groupe ciblé se voient attribuer aléatoirement les différentes variations de contenu définies pour leur groupe respectif.

<!--
## Reporting on Message optimization

E.g. explaining how a marketer can look at the report to determine which treatment (e.g. which message content) is performing the best for the targeting audience
-->
