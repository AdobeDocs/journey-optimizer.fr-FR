---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’expérimentation dans l’optimisation des messages
description: Découvrez comment utiliser des expériences de contenu pour tester plusieurs versions de contenu et déterminer celle qui fonctionne le mieux.
role: User
level: Intermediate
keywords: expérimentation, optimisation, tests A/B, expérience de contenu, traitements
exl-id: 4e8537c4-944f-4a39-be2b-af8ebfb6e099
TQID: https://experienceleague.adobe.com/2ponHAr61o0hTMYuG5l9mQuh79-WeQz9eRuCF7dZjdA
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: []
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: cdd65e7e-8839-44a2-bc21-0e03623b5dd1id: e1e0219c-f879-479f-8427-888ed2a6e9c2
subfeature_v2: id: f29a52db-c90c-4345-902e-b586d1406d8d
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 294
ht-degree: 72%

---

# Utiliser l’expérimentation {#experimentation}

>[!NOTE]
>
>Cette page présente un aperçu de l’utilisation de l’expérimentation dans le cadre de l’optimisation du contenu. Pour plus d’informations sur les expériences de contenu, y compris les options de configuration, les mesures et l’analyse, consultez la [documentation sur les expériences de contenu](../content-management/get-started-experiment.md).

L’expérimentation permet de tester plusieurs versions d’un contenu afin de déterminer celle qui offre les meilleures performances en fonction de mesures de succès prédéfinies.

Pour configurer l’expérimentation, suivez les étapes ci-dessous.

Supposons que vous vouliez tester les messages promotionnels suivants dans une campagne :

* **Traitement A** : « 20 % de réduction sur votre prochain achat »
* **Traitement B** : « Livraison gratuite sur les commandes de plus de 50 $ »
* **Traitement C** : « Obtenez votre carte-cadeau de 10 $ »

Pour configurer l’expérimentation et déterminer le message qui génère le plus d’achats, procédez comme suit.

1. Créez un [parcours](../building-journeys/journey-gs.md#jo-build) ou une [campagne](../campaigns/create-campaign.md).

   >[!NOTE]
   >
   >Si vous vous trouvez dans un parcours, ajoutez une activité **[!UICONTROL Action]**, choisissez une activité de canal et sélectionnez **[!UICONTROL Configurer l’action]**. [En savoir plus](../building-journeys/journey-action.md#add-action)

1. Dans l’onglet **[!UICONTROL Actions]**, sélectionnez au moins deux actions entrantes, par exemple [expérience basée sur du code](../code-based/get-started-code-based.md) et [in-app](../../rp_landing_pages/in-app-landing-page.md).

1. Dans la section **[!UICONTROL Optimisation]**, sélectionnez **[!UICONTROL Créer une expérience]**.

   ![](../campaigns/assets/msg-optimization-select-experiment.png){width=85%}

1. Concevez et configurez votre expérience de contenu selon vos besoins. [Voici comment procéder](../content-management/content-experiment.md)

   ![](../campaigns/assets/msg-optimization-create-experiment.png){width=85%}

   Une fois l’expérience définie, elle s’applique à toutes les actions insérées dans la campagne ou par le biais de l’activité **[!UICONTROL Action]** du parcours, ce qui signifie que les mêmes clients et clientes voient les mêmes offres sur l’ensemble des surfaces.

   >[!NOTE]
   >
   >Vous pouvez sélectionner d’autres actions : l’expérimentation s’applique à toutes les actions ajoutées à la campagne ou au parcours [Activité d’action](../building-journeys/journey-action.md).

1. [Activez](../campaigns/review-activate-campaign.md) votre parcours ou campagne.

Une fois la campagne ou le parcours actif, les utilisateurs et utilisatrices se voient attribuer aléatoirement les différentes variations de contenu. [!DNL Journey Optimizer] suit la variation qui génère le plus d’achats et fournit des informations exploitables.

Suivez le succès de votre campagne avec les rapports de [parcours](../reports/journey-global-report-cja.md) et de [campagne](../reports/campaign-global-report-cja-experimentation.md). <!--Link to Experimentation journey reportis missing-->
