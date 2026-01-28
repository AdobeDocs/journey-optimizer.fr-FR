---
solution: Journey Optimizer
product: journey optimizer
title: Création de rapports
description: Commencer avec les rapports
feature: Reporting
topic: Content Management
role: User
level: Intermediate
exl-id: d2ff175a-8bca-4b62-931c-a909cfd9308d
source-git-commit: 47280460f7b47412c348ccc75ca9afca50c34e7e
workflow-type: tm+mt
source-wordcount: '1327'
ht-degree: 100%

---

# Gérer vos rapports {#channel-cja-manage}

## Analyser dans Customer Journey Analytics {#analyze}

>[!AVAILABILITY]
>
> La fonctionnalité **Analyser dans CJA** est disponible exclusivement pour les utilisateurs et utilisatrices disposant d’une licence [!DNL Customer Journey Analytics].

![](assets/cja-analyze.png)

Améliorez votre expérience d’analyse des données avec votre licence **[!DNL Customer Journey Analytics]** en tirant parti de la fonction **[!UICONTROL Analyser dans CJA]** disponible dans tous les rapports.

Cette puissante option vous redirige aisément vers votre environnement **[!DNL Customer Journey Analytics]**, ce qui vous permet de personnaliser abondamment vos rapports. Intégrez des mesures avancées de Customer Journey Analytics dans vos widgets pour enrichir vos informations et les rendre encore plus pertinentes.

[En savoir plus sur l’interface de Customer Journey Analytics.](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-overview/cja-getting-started)

## Définir la période d’un rapport {#report-period}

![](assets/cja-time-period.png)

En accédant à un rapport, vous pouvez appliquer un filtre de période situé dans le coin supérieur droit de ce dernier.

Par défaut, la période de filtrage d’une campagne ou d’un parcours est définie sur ses dates de début et de fin. En l’absence de date de fin, le filtre est défini par défaut sur la date actuelle.

Pour modifier le filtre, vous pouvez sélectionner une date de début et une durée personnalisées ou choisir parmi des options prédéfinies telles que « la semaine dernière » ou « il y a deux mois ».

Le rapport est automatiquement mis à jour une fois le filtre appliqué ou modifié.

## Exporter vos rapports {#export-reports}

Vous pouvez facilement exporter vos différents rapports au format PDF ou CSV, ce qui vous permet de les partager ou de les imprimer. Les étapes d’export des rapports sont présentées dans les onglets ci-dessous.

>[!BEGINTABS]

>[!TAB Exporter votre rapport au format CSV]

1. Dans votre rapport, cliquez sur **[!UICONTROL Partager]** et sélectionnez **[!UICONTROL Télécharger le CSV]** pour générer un fichier CSV au niveau du rapport global.

   ![](assets/export_cja_csv.png)

1. Votre fichier est automatiquement téléchargé et peut se trouver dans vos fichiers locaux.

   Si vous avez généré le fichier au niveau du rapport, il contient des informations détaillées pour chaque widget, notamment son titre et ses données.

>[!TAB Exporter votre rapport au format PDF]

1. Dans votre rapport, cliquez sur **[!UICONTROL Partager]** et sélectionnez **[!UICONTROL Télécharger le PDF]**.

   ![](assets/export_cja_pdf.png)

1. Une fois le téléchargement demandé, cliquez sur **[!UICONTROL Télécharger]**.

   ![](assets/export_cja_pdf_2.png)

1. Votre fichier s’ouvre automatiquement dans votre navigateur.

Vous pouvez maintenant consulter, télécharger ou partager votre rapport en fichier PDF.

>[!ENDTABS]


## Planifier les exports {#schedule-export}

La fonction **Planifier les exports** permet d’automatiser la remise de 10 rapports au maximum à des intervalles hebdomadaires, mensuels ou annuels. Vous pouvez également facilement gérer vos rapports planifiés avec des options permettant de mettre à jour, modifier, annuler ou supprimer l’un de vos exports planifiés.

1. Dans votre rapport, cliquez sur **[!UICONTROL Partager]** et sélectionnez **[!UICONTROL Planifier l’export]**.

   ![](assets/export-schedule-1.png)

1. Choisissez le **[!UICONTROL type de fichier]** (CSV ou PDF).

1. Si nécessaire, vous pouvez ajouter une **[!UICONTROL Description]** à votre export.

1. Saisissez le nom des destinataires qui recevront cette diffusion automatisée.

   ![](assets/export-schedule-2.png)

1. Choisissez la **[!UICONTROL fréquence]**.

1. En fonction de la fréquence sélectionnée, fournissez les détails de planification pertinents, tels que les suivants :

   * Dates de début et de fin

   * Intervalle (toutes les quelques semaines, par exemple)

   * Jour spécifique de la semaine

   * Semaine du mois

   * Jour du mois

   * Mois de l’année

1. Cliquez sur **[!UICONTROL Envoyer selon le planning]**.

1. Pour modifier l’export planifié créé précédemment, cliquez sur **[!UICONTROL Partager]** et sélectionnez **[!UICONTROL Gérer les plannings]**.

   ![](assets/export-schedule-3.png)

1. Dans la liste des exports planifiés, choisissez celui que vous souhaitez mettre à jour et apportez les modifications nécessaires.

1. Pour supprimer un rapport planifié, sélectionnez-le dans la liste des plannings gérés et cliquez sur **[!UICONTROL Supprimer]**.

   ![](assets/export-schedule-4.png)


## Créer une mesure simple {#create-simple-metric}

Vous pouvez créer des mesures calculées personnalisées directement dans vos rapports. Vous pouvez générer des informations plus personnalisées et mieux analyser vos données en combinant deux mesures existantes en fonction de vos besoins de création de rapports spécifiques.

1. Commencez par accéder au rapport dans lequel vous souhaitez ajouter une nouvelle mesure.

1. Dans le tableau de votre rapport, sélectionnez les mesures souhaitées en maintenant les touches `Shift` ou `CTRL/CMD` enfoncées tout en cliquant dessus. Cliquez ensuite avec le bouton droit et sélectionnez **[!UICONTROL Créer une mesure d’après la sélection]**.

   Si vous sélectionnez plus de deux mesures, seules les deux premières sont utilisées dans le créateur de mesures.

   ![](assets/cja-create-metric_2.png)

1. Dans le créateur de mesures calculées, nommez votre nouvelle mesure en saisissant dans le champ **[!UICONTROL Titre]**. Vous pouvez également ajouter une **[!UICONTROL description]**.

   >[!NOTE]
   >
   >Si vous possédez Customer Journey Analytics, vous pouvez personnaliser davantage vos mesures à l’aide d’options supplémentaires. [En savoir plus](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-components/cja-calcmetrics/cm-workflow/cm-build-metrics#areas-of-the-calculated-metrics-builder)

1. Sélectionnez le **[!UICONTROL Nombre de décimales après la virgule]** approprié et choisissez un **[!UICONTROL format]** (décimale, heure, pourcentage ou devise) en fonction de la manière dont votre mesure doit être affichée.

1. Sélectionnez l’opérateur, tel que l’addition, la soustraction, la multiplication ou la division, qui déterminera le mode de calcul de la mesure.

   ![](assets/cja-create-metric.png)

1. Vous pouvez réorganiser les composants si nécessaire.

1. Lorsque vos paramètres vous conviennent, cliquez sur **[!UICONTROL Appliquer]** pour finaliser votre nouvelle mesure.

1. Votre nouvelle mesure s’affiche en regard des mesures d’origine dans votre rapport.

   ![](assets/cja-create-metric_3.png)

La mesure que vous venez de créer sera incluse lorsque vous exportez le rapport au format PDF ou CSV. Cependant, elle sera supprimée du rapport une fois que vous l’aurez quitté.

## Explorer les données à l’aide du Générateur d’aperçu {#exploratory}

Utilisez l’outil Générateur d’aperçu pour créer facilement des tableaux et des visualisations à partir des **[!UICONTROL dimensions]** et des **[!UICONTROL mesures]** sélectionnées. Cet outil simplifie l’exploration des données, ce qui vous permet de personnaliser et d’analyser automatiquement et facilement les informations. Apprenez-en davantage en consultant [cette documentation](https://experienceleague.adobe.com/fr/docs/analytics/analyze/analysis-workspace/panels/quickinsight).

1. Commencez par accéder au rapport dans lequel vous souhaitez utiliser le Générateur d’aperçu.

1. Sélectionnez le menu Générateur d’aperçu dans le menu du rail de gauche.

   ![](assets/exploratory_analysis_1.png)

1. Créez une requête en choisissant une **[!UICONTROL dimension]** et une **[!UICONTROL mesure]** à l’aide des menus déroulants. Vous pouvez également sélectionner un **[!UICONTROL segment]** si nécessaire.

   ![](assets/exploratory_analysis_2.png)

1. Définissez la période de votre analyse afin de spécifier la période sur laquelle vous souhaitez vous concentrer. Par défaut, la période est définie sur celle utilisée dans le panneau du rapport.

1. Utilisez les options **[!UICONTROL Ajouter une répartition]** ou **[!UICONTROL Ajouter une mesure]** pour inclure des dimensions supplémentaires, ce qui permet une répartition des données plus détaillée.

   Notez que vous ne pouvez ajouter que trois **[!UICONTROL dimensions]**, **[!UICONTROL mesures]** et **[!UICONTROL segments]**.

Vous pouvez désormais analyser vos données à l’aide de vos outils de visualisation et de tableau personnalisés.

<!--## Create a down-funnel metric {#down-funnel}

1. Create a new journey or open an existing one. [Learn more about journey creation](../building-journeys/journey-gs.md)

1. On the canvas editor, select the option to "add a metric".

c. In the metric selector, choose whichever conversion metric seems appropriate and publish your journey

d. Open the report for the journey that you added the metric to and ensure that the metric has been added to the table alongside all the other pre-configured metrics.
-->

## Créer une audience à partir de données de rapport {#create-audience}

>[!IMPORTANT]
>
>Chaque organisation est limitée à la publication de 25 audiences. En outre, les utilisateurs et utilisatrices peuvent publier un maximum de 5 audiences par heure et 20 par jour.
> Les audiences ponctuelles ont une durée de vie de 48 heures. Par conséquent, si 25 audiences sont publiées au cours de ce délai, les audiences supplémentaires ne peuvent être publiées qu’une fois la période de 48 heures écoulée.

Vous pouvez désormais sélectionner des données spécifiques dans le tableau et créer directement une audience à partir de ces sélections, en rationalisant et en simplifiant le processus de création d’audience.

1. Accédez tout d’abord au tableau du rapport qui contient les données que vous souhaitez transformer en audience.

1. Cliquez avec le bouton droit sur la cellule de votre choix et sélectionnez **[!UICONTROL Créer une audience]**.

   Vous pouvez également lancer la création d’audience à partir du widget **[!UICONTROL Zone de travail du parcours]** en sélectionnant un nœud et en cliquant dessus avec le bouton droit de la souris.

1. Dans la fenêtre **[!UICONTROL Créer une audience]**, saisissez un **[!UICONTROL nom]** et définissez une **[!UICONTROL période unique]** pour l’audience que vous prévoyez de publier.

   >[!NOTE]
   >
   >Si vous possédez Customer Journey Analytics, vous pouvez personnaliser davantage vos mesures à l’aide d’options supplémentaires. [En savoir plus](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-components/audiences/publish)

   ![](assets/audience_1.png)

1. Cliquez sur le bouton **[!UICONTROL Créer]** pour finaliser la création de l’audience. Notez que ce processus peut nécessiter un certain temps.

Vous pouvez maintenant utiliser l’audience nouvellement créée avec un parcours ou une campagne.

## Gérer les modèles {#cja-template}

Vous avez désormais la possibilité d’améliorer vos rapports Journey Optimizer à l’aide de modèles Customer Journey Analytics. [En savoir plus sur le modèle Customer Journey Analytics](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-workspace/templates/use-templates#use-reports)

Lors de l’accès aux rapports, vous pouvez choisir entre deux types de modèles dans le menu déroulant **[!UICONTROL Sélectionner un modèle]** :

* Modèle par défaut fourni par Adobe
* Modèles générés par la clientèle

![](assets/cja_template_5.png)

Si aucun modèle n’a été créé, la liste déroulante **[!UICONTROL Sélectionner un modèle]** n’apparaît pas dans votre interface de création de rapports.

Pour créer un modèle, procédez comme suit :

1. Dans [!DNL Customer Journey Analytics], accédez au menu **[!UICONTROL Workspace]** et sélectionnez **[!UICONTROL Modèles Adobe]**. [En savoir plus sur les modèles disponibles](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-workspace/templates/use-templates#available-templates)

1. Parcourez les modèles préconfigurés disponibles et cliquez sur **[!UICONTROL Utiliser le modèle]** pour en sélectionner un.

   ![](assets/cja_template_1.png)

1. Ajustez votre rapport en fonction de vos besoins. Consultez la documentation [Customer Journey Analytics](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-workspace/home).

1. Une fois le modèle personnalisé terminé, accédez au menu **[!UICONTROL Projet]** et sélectionnez **[!UICONTROL Enregistrer en tant que modèle]**.

   ![](assets/cja_template_2.png)

1. Fournissez les détails nécessaires pour votre modèle. Consultez la documentation [Customer Journey Analytics](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/cja-workspace/templates/create-templates#edit-or-delete-a-template) pour plus d’informations.

   >[!IMPORTANT]
   >
   > Veillez à choisir **Journey Optimizer** sous **[!UICONTROL Cas d’utilisation]** et à spécifier le type d’activité et l’**activité** **Journey Optimizer** correspondants. Ainsi, votre rapport apparaîtra dans Journey Optimizer.

   ![](assets/cja_template_3.png)

1. Dans [!DNL Journey Optimizer], à partir de votre rapport, accédez au rapport et choisissez le modèle précédemment créé dans le menu déroulant **[!UICONTROL Sélectionner un modèle]**.

   ![](assets/cja_template_4.png)

Pour créer directement un modèle à partir de votre rapport Journey Optimizer, il vous suffit d’accéder à votre campagne ou à votre rapport de parcours, de sélectionner **[!UICONTROL Analyser dans CJA]** et de personnaliser le modèle par défaut en suivant les étapes décrites ci-dessus.
