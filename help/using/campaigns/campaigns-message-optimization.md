---
solution: Journey Optimizer
product: journey optimizer
title: Optimisation des messages
description: Tirez parti de l’optimisation des messages pour créer des campagnes marketing personnalisées et optimisées.
role: User
level: Intermediate
keywords: optimisation des campagnes, expérimentation, ciblage, tests A/B
source-git-commit: edbe25e0cb341c08e440eb0663fb9b253273f48a
workflow-type: tm+mt
source-wordcount: '918'
ht-degree: 1%

---

# Optimisation des campagnes {#message-optimization}

L’optimisation vous fournit les outils nécessaires pour diffuser du contenu personnalisé et optimisé à l’audience de vos campagnes, <!--based on marketer-defined advanced decision configurations. This ensures that the right message reaches the right audience at the right time in order to maximize the effectiveness of your campaigns. (Removed for now as Decisioning is not yet supported)-->en garantissant un engagement et une réussite maximaux pour créer des campagnes hautement <!--customized and --> efficaces.

Avec l’optimisation, vous pouvez :

* Utilisation [ règles de ciblage ](#targeting)
* Exécuter [expériences de contenu](#experimentation)
* Utilisez des [combinaisons avancées](#combination) d’expérimentation et de ciblage dans une seule campagne

Une fois la campagne active, les profils sont évalués en fonction des critères définis. Ensuite, en fonction des critères correspondants, ils sont diffusés avec l’expérience ou le contenu approprié de la campagne.

La différence entre les expériences et le ciblage peut être décrite comme suit :

* L’expérimentation consiste en une répartition aléatoire dans la diffusion du contenu en fonction de l’affectation du trafic&#x200B;.
* Le ciblage utilise des techniques déterministes pour diffuser du contenu en fonction du profil utilisateur, de l’appartenance à l’audience ou des règles contextuelles.

![](assets/msg-optimization-experiment-vs-targeting.png){width="110%" zoomable="yes"}

## Utiliser le ciblage {#targeting}

Le ciblage fournit du contenu personnalisé à des segments d’audience spécifiques en fonction d’attributs de profil utilisateur ou d’attributs contextuels.

Contrairement à l’expérimentation, qui consiste en une affectation aléatoire du contenu d’un message, le ciblage est déterministe en termes de diffusion du contenu à la bonne audience.

Avec le ciblage, des règles spécifiques peuvent être définies en fonction des éléments suivants :

* **Attributs de profil utilisateur** tels que l’emplacement (par exemple, le géociblage), l’âge ou les préférences. Par exemple, aux États-Unis, les utilisateurs voient une promotion « Golden Gate », tandis qu’en France, ils voient une promotion « Tour Eiffel ».

* **Données contextuelles** telles que le type d’appareil (par exemple, ciblage de l’appareil), l’heure de la journée ou les détails de la session. Par exemple, les utilisateurs d’ordinateurs de bureau reçoivent du contenu optimisé pour les ordinateurs de bureau, tandis que les utilisateurs mobiles reçoivent du contenu optimisé pour les appareils mobiles.

* **Audiences** qui peuvent être utilisées pour inclure ou exclure les profils ayant une appartenance à une audience particulière.

Pour configurer le ciblage dans une campagne, procédez comme suit.

1. Création d’une campagne. [En savoir plus](../campaigns/create-campaign.md) <!--Add link to API triggered?-->

1. Dans l’onglet **[!UICONTROL Actions]**, sélectionnez au moins une action.

1. Dans la section **[!UICONTROL Optimisation des messages]**, sélectionnez **[!UICONTROL Ciblage]**.

   ![](assets/msg-optimization-select-targeting.png){width=85%}

1. Utilisez le créateur de règles pour définir vos critères. Par exemple, définissez une règle pour les résidents des États-Unis, une règle pour les résidents de la France et une règle pour les résidents de l’Inde.

   ![](assets/msg-optimization-create-targeting.png){width=85%}

1. Sélectionnez l’option **[!UICONTROL Activer le contenu de secours]** selon vos besoins. Le contenu de secours permet à votre audience de recevoir un contenu par défaut lorsqu’aucune règle de ciblage n’est qualifiée. Si vous ne sélectionnez pas cette option, toute audience qui ne remplit pas les critères d’une règle de ciblage définie ci-dessus ne recevra pas de contenu.

1. Enregistrez les paramètres de votre règle de ciblage.

1. De retour dans l’onglet Campagne **[!UICONTROL Actions]**, sélectionnez **[!UICONTROL Modifier le contenu]**.

1. Concevez le contenu approprié pour chaque groupe défini par les paramètres de vos règles de ciblage.

   ![](assets/msg-optimization-targeting-design.png){width=85%}

   Dans cet exemple, concevez un contenu spécifique pour les résidents américains, un contenu différent pour les résidents français et un autre pour les résidents indiens.

1. [ Activer ](review-activate-campaign.md) votre campagne.

Une fois la campagne en ligne, le contenu adapté à chaque cible est envoyé afin que les résidents américains reçoivent un message spécifique, les résidents français un message différent, etc.

<!--Default content:

* If no targeting rules match, default content can be delivered.

* If default content is not enabled, passthrough behavior ensures lower-priority campaigns are evaluated.-->

## Utiliser l’expérimentation {#experimentation}

L’expérimentation vous permet de tester plusieurs versions de contenu afin de déterminer celle qui fonctionne le mieux en fonction de mesures de succès prédéfinies.

Pour configurer l’expérimentation dans une campagne, procédez comme suit.

Supposons que vous souhaitiez tester les messages promotionnels suivants dans une campagne :

* **Traitement A** : « 20 % de réduction sur votre prochain achat »
* **Traitement B** : « Livraison gratuite sur les commandes de plus de 50 $ »
* **Traitement C** : « Obtenez votre carte-cadeau de 10 $ »

Pour configurer l’expérimentation et déterminer le message qui génère le plus d’achats, procédez comme suit.

1. Création d’une campagne. [En savoir plus](../campaigns/create-campaign.md) <!--Add link to API triggered?-->

1. Dans l’onglet **[!UICONTROL Actions]**, sélectionnez au moins deux actions entrantes, par exemple [expérience basée sur du code](../code-based/get-started-code-based.md) et [In-app](../in-app/get-started-in-app.md).

1. Dans la section **[!UICONTROL Optimisation des messages]**, sélectionnez **[!UICONTROL Expérimentation]**.

   ![](assets/msg-optimization-select-experiment.png){width=85%}

1. Concevez et configurez votre expérience de contenu selon vos besoins. [Voici comment procéder](../content-management/content-experiment.md)

   ![](assets/msg-optimization-create-experiment.png){width=85%}

   Une fois l’expérience définie, elle s’applique à toutes les actions insérées dans cette campagne, ce qui signifie que les mêmes clients voient les mêmes offres sur toutes les surfaces.

   >[!NOTE]
   >
   >Vous pouvez sélectionner d’autres actions : l’expérimentation s’applique à toutes les actions ajoutées à la campagne.

1. [ Activer ](review-activate-campaign.md) votre campagne.

Une fois la campagne activée, les utilisateurs sont affectés de manière aléatoire aux différentes variations de contenu. [!DNL Journey Optimizer] permet de suivre les variations qui génèrent le plus d’achats et fournit des informations exploitables.

Suivez le succès de votre campagne avec le [rapport de campagne d’expérimentation](../reports/campaign-global-report-cja-experimentation.md).

## Combiner ciblage et expérimentation {#combination}

Journey Optimizer vous permet également de combiner le ciblage et les expériences au sein d’une même campagne afin de créer des stratégies plus sophistiquées.

En effet, vous pouvez utiliser le ciblage pour créer plusieurs variantes et, pour chaque variante, utiliser l’expérimentation pour optimiser davantage chaque contenu. Cela permet de s’assurer que les expériences sont spécifiques à chaque règle de ciblage et ne s’étendent pas sur plusieurs variantes dans la campagne.

Par exemple, vous pouvez tester une « promotion de 50 % » par rapport à une « carte cadeau de 50 $ » pour les clients situés aux États-Unis et exécuter un test différent pour les clients en Europe, tel que « livraison gratuite sur les commandes de plus de 50 € » par rapport à « 20 % de réduction sur leur prochain achat ».

Pour combiner le ciblage et les expériences dans une campagne, procédez comme suit.

1. Créez une opération dans laquelle vous définissez plusieurs règles de ciblage. [Voici comment procéder](#targeting)

   ![](assets/msg-optimization-create-targeting.png){width=85%}

1. Créez une expérience pour la première règle de ciblage.

1. Concevez et configurez votre expérience de contenu selon vos besoins. [Voici comment procéder](../content-management/content-experiment.md)

   ![](assets/msg-optimization-targeting-with-experiment.png){width=85%}

   Une fois l’expérimentation définie, elle s’applique uniquement à la première règle de ciblage.

1. De retour dans l’onglet Campagne **[!UICONTROL Actions]**, sélectionnez **[!UICONTROL Modifier le contenu]**.

1. Pour le groupe défini par votre première règle de ciblage, vous pouvez définir un contenu spécifique pour chaque variante de votre expérience.

   Si vous avez ajouté plusieurs actions entrantes à votre campagne, la même combinaison de ciblage et d’expérience s’applique à chaque action. Cependant, vous devez définir un contenu spécifique pour chaque variante de chaque action.

   ![](assets/msg-optimization-targeting-experiment-design.png){width=85%}

1. Procédez de la même manière pour les autres règles de ciblage et concevez le contenu correspondant pour chaque variante.

1. Enregistrez vos modifications et [activez](review-activate-campaign.md) votre campagne.

Une fois la campagne activée, les utilisateurs de chaque groupe ciblé se voient attribuer de manière aléatoire les différentes variations de contenu définies pour le groupe auquel ils appartiennent.

<!--
## Reporting on Message optimization

E.g. explaining how a marketer can look at the report to determine which treatment (e.g. which message content) is performing the best for the targeting audience
-->

