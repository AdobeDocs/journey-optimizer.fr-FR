---
solution: Journey Optimizer
product: journey optimizer
title: Création d’une expérience de contenu
description: Découvrez comment créer une expérience de contenu dans vos campagnes
feature: A/B Testing
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: bd35ae19-8713-4571-80bc-5f40e642d121
source-git-commit: ef838945e0c3595de8ad920203b278bb51671d16
workflow-type: tm+mt
source-wordcount: '949'
ht-degree: 0%

---

# Création d’une expérience de contenu {#content-experiment}

>[!CONTEXTUALHELP]
>id="ajo_campaigns_content_experiment"
>title="Expérience de contenu"
>abstract="Vous pouvez choisir de varier le contenu, l&#39;objet ou l&#39;expéditeur de la diffusion afin de définir plusieurs traitements de diffusion et déterminer la meilleure combinaison pour vos audiences."

>[!AVAILABILITY]
>
>Le **Expérience de contenu** Cette fonctionnalité est actuellement disponible uniquement pour un ensemble d’organisations (disponibilité limitée). Pour plus d’informations, contactez votre représentant Adobe.

Utilisez l’expérience de contenu de Journey Optimizer pour définir plusieurs traitements de diffusion. L’audience ciblée est attribuée de manière aléatoire à chaque traitement afin de déterminer lequel est le plus performant par rapport à la mesure d’intérêt. Vous pouvez choisir de varier le contenu, l&#39;objet ou l&#39;expéditeur de la diffusion.

>[!NOTE]
>
>Avant de commencer l’expérience de contenu, assurez-vous que votre configuration de création de rapports est définie pour vos jeux de données personnalisés. En savoir plus dans [cette section](reporting-configuration.md).

Dans l&#39;exemple ci-dessous, la cible de la diffusion a été divisée en deux groupes, représentant chacun 45 % de la population ciblée, et un groupe d&#39;exclusion de 10 %, qui ne recevra pas la diffusion.

Chaque personne de l’audience ciblée recevra une version d’un email, avec un objet qui est l’un des deux suivants :

* une promotion directe d&#39;une offre de 10 % sur la nouvelle collection et une image.
* l’autre ne fait de la publicité que pour une offre spéciale sans spécifier les 10 % de réduction sans image.

L&#39;objectif ici est de voir si les destinataires interagissent avec l&#39;email en fonction de l&#39;expérience reçue. Nous choisirons donc **[!UICONTROL Email Opens]** comme mesure d’objectif principale de cette expérience de contenu.

![](assets/content_experiment.png)

## Créer votre campagne {#campaign-experiment}

1. Dans la **[!UICONTROL Campaigns]** page, cliquez sur **[!UICONTROL Create campaign]**.

   ![](assets/content_experiment_1.png)

1. Sélectionnez votre canal, puis le **[!UICONTROL Surface]** vous souhaitez utiliser pour cette diffusion. Voir à ce sujet la section [Surfaces des canaux](../configuration/channel-surfaces.md) page.

   ![](assets/content_experiment_2.png)

1. Cliquez sur **[!UICONTROL Create]**.

1. Configurez les **[!UICONTROL Properties]** de votre diffusion :
   * **[!UICONTROL Title]**
   * **[!UICONTROL Description]**
   * **[!UICONTROL Category]**: **[!UICONTROL Marketing]** / **[!UICONTROL Transactional]**

1. Pour lancer votre expérience de contenu, activez la fonction **[!UICONTROL Content experiment]** . Le **[!UICONTROL Content experiment]** s’affiche.

   ![](assets/content_experiment_3.png)

1. Définissez l’audience à cibler. Pour ce faire, cliquez sur le bouton **[!UICONTROL Select audience]** pour afficher la liste des segments Adobe Experience Platform disponibles. [En savoir plus sur les segments](../segment/about-segments.md)

   Dans le **[!UICONTROL Identity namespace]** , choisissez l’espace de noms à utiliser pour identifier les individus du segment sélectionné. [En savoir plus](get-started-experiment.md#content-experiment-work)

1. Pour exécuter votre campagne à une date spécifique ou à une fréquence récurrente, configurez la section Planning . [En savoir plus](create-campaign.md)

1. Cliquez sur **[!UICONTROL Edit content]** pour commencer à personnaliser vos **[!UICONTROL Treatments]**.

   ![](assets/content_experiment_4.png)

## Créer vos traitements {#treatment-experiment}

1. Dans la **[!UICONTROL Edit content]** , commencez à personnaliser votre traitement A.

   Pour ce traitement, nous allons définir l&#39;offre spéciale directement dans la ligne d&#39;objet.

   ![](assets/content_experiment_5.png)

1. Après avoir conçu votre premier traitement, à partir de la **[!UICONTROL More actions]** bouton, cliquez **[!UICONTROL Duplicate]**.

   Vous pouvez également choisir de commencer un nouveau traitement à partir de zéro en cliquant sur le bouton **[!UICONTROL Content experiment]** button ![](assets/content_experiment_16.png) pour accéder aux options avancées, puis **[!UICONTROL Add treatment]**.

   ![](assets/content_experiment_7.png)

1. Modifiez la variable **[!UICONTROL Title]** de votre traitement pour mieux les différencier.

   ![](assets/content_experiment_8.png)

1. Personnalisez votre second traitement selon vos besoins.

   Ici, nous choisissons de ne pas spécifier l’offre dans le **[!UICONTROL Subject line]**.

   ![](assets/content_experiment_9.png)

Une fois vos traitements personnalisés, vous pouvez commencer à configurer votre expérience de contenu.

## Configuration de votre expérience de contenu {#configure-experiment}

1. Lorsque les deux diffusions sont personnalisées, à partir de la **[!UICONTROL Edit content]** fenêtre, sélectionnez **[!UICONTROL Configure content experiment]**.

   ![](assets/content_experiment_10.png)

1. Sélectionnez les objectifs que vous souhaitez définir pour votre expérience.

   Pour notre expérience, nous sélectionnons **[!UICONTROL Email open]** pour tester si les destinataires ouvriront leurs emails si le code promotion se trouve dans la ligne d’objet.

   ![](assets/content_experiment_11.png)

1. Choisissez d’ajouter une **[!UICONTROL Holdout]** à votre diffusion. Ce groupe ne recevra aucun contenu de cette campagne.

   Le fait de basculer sur la barre de bascule représentera automatiquement 10 % de votre population. Vous pouvez ajuster ce pourcentage si nécessaire.

   ![](assets/content_experiment_12.png)

1. Vous pouvez ensuite choisir d’attribuer un pourcentage précis à chaque **[!UICONTROL Treatment]** ou simplement activer la fonction **[!UICONTROL Distribute evenly]** la barre de bascule.

   ![](assets/content_experiment_13.png)

1. Cliquez sur **[!UICONTROL Save]** lorsque votre configuration est définie.

1. Lorsque votre expérience de contenu est prête, vous pouvez cliquer sur **[!UICONTROL Review to activate]** pour afficher un résumé de l&#39;opération. Les alertes s’affichent si un paramètre est incorrect ou manquant.

   ![](assets/content_experiment_15.png)

1. Vérifiez que votre campagne est correctement configurée, puis cliquez sur **[!UICONTROL Activate]** pour le lancer.

   ![](assets/content_experiment_14.png)

Après avoir paramétré votre expérimentation et votre campagne, vous pouvez suivre le succès de votre diffusion avec le rapport Campagne .

## Rapport Objectifs {#objectives-global}

>[!AVAILABILITY]
>
>Actuellement, la fonctionnalité d’expérience de contenu n’est disponible que pour un ensemble d’organisations (disponibilité limitée). Pour plus d’informations, contactez votre représentant Adobe.

![](assets/performance_report.gif)

Le **[!UICONTROL Objectives]** de votre rapport Campagne , qui vous permet d’affiner davantage les rapports de vos diffusions en ciblant une mesure spécifique.

Le **[!UICONTROL Objectives]** répertoriés sont liés à **[!UICONTROL Datasets]** qui définissent une connexion à un système afin de récupérer des informations supplémentaires. Liste des éléments intégrés **[!UICONTROL Objectives]** est disponible, mais vous pouvez ajouter le vôtre en ajoutant un nouveau **[!UICONTROL Dataset]**. Voir à ce sujet la procédure détaillée [section](reporting-configuration.md).

Après avoir sélectionné les objectifs que vous souhaitez cibler, les deux **[!UICONTROL Performance overview]** et **[!UICONTROL Campaign objective]** Les widgets fournissent un résumé détaillé des performances de votre diffusion.

Avec le **[!UICONTROL Campaign objective]** vous pouvez également choisir de comparer votre objectif principal à une autre mesure.

Notez que chaque widget peut être redimensionné et supprimé si nécessaire. Voir à ce sujet la section [section](../reports/global-report.md#modify-dashboard).

## Rapport d’expérience {#experimentation-global}

>[!AVAILABILITY]
>
>Actuellement, la fonctionnalité d’expérience de contenu n’est disponible que pour un ensemble d’organisations (disponibilité limitée). Pour plus d’informations, contactez votre représentant Adobe.

![](assets/experimentation_report_3.png)

Depuis votre campagne **[!UICONTROL Global report]**, la variable **[!UICONTROL Experimentation]** l’onglet détaille les informations principales relatives aux performances de chaque variante et s’il y a un meilleur résultat.

Notez que la définition du meilleur performant peut prendre un certain temps, elle sera représentée par cette icône . ![](assets/experimentation_report_1.png).

Le **[!UICONTROL Experiment result]** décrit les performances de chaque variante. Vous pouvez modifier votre ligne de base en sélectionnant l’un des traitements de la **[!UICONTROL Baseline]** la liste déroulante. Le meilleur traitement sera représenté par une icône en forme d’étoile.

Le tableau présente les mesures suivantes :

* **[!UICONTROL Profiles]**: Nombre de profils ciblés pour ce traitement.

* **[!UICONTROL Unique outbound clicks]**: Nombre total de clics sur les canaux sortants.

* **[!UICONTROL Count per profile]**: Valeur totale de la mesure de l’objectif de l’expérience divisée par le nombre de profils.

* **[!UICONTROL Confidence interval]**: Différence en pourcentage de performance entre la ligne de base et le traitement le plus performant. [En savoir plus](../campaigns/experiment-calculations.md#confidence-intervals).

* **[!UICONTROL Average lift]**: Pourcentage d’amélioration du taux de conversion d’un traitement donné par rapport à la ligne de base. [En savoir plus](../campaigns/experiment-calculations.md#understand-lift)

* **[!UICONTROL Confidence]**: Preuves qu&#39;un traitement donné est le même que le traitement de base. [En savoir plus](../campaigns/experiment-calculations.md#understand-confidence)

Pour un examen approfondi de ces résultats et de leur interprétation, reportez-vous à la section [cette page](../campaigns/get-started-experiment.md#interpret-results).
