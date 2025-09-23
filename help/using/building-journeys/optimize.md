---
solution: Journey Optimizer
product: journey optimizer
title: Activité Optimiser
description: En savoir plus sur l’activité d’optimisation
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: activité, condition, zone de travail, parcours, optimisation
badge: label="Disponibilité limitée" type="Informative"
exl-id: f6618de4-7861-488e-90c0-f299ef5897ca
version: Journey Orchestration
source-git-commit: c472ce00623b810dea60dd5d9e34ca4d516447ad
workflow-type: tm+mt
source-wordcount: '1298'
ht-degree: 38%

---

# Activité Optimiser {#journey-path-optimization}

>[!CONTEXTUALHELP]
>id="ajo_journey_optimize"
>title="Activité Optimiser"
>abstract="L’activité **Optimiser** vous permet de définir la progression des individus dans votre parcours en créant plusieurs chemins en fonction de critères spécifiques, y compris l’expérimentation, le ciblage et des conditions spécifiques."

>[!AVAILABILITY]
>
>Cette fonctionnalité est en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en obtenir l’accès.

L’activité **Optimiser** vous permet de définir la progression des individus dans votre parcours en créant plusieurs **chemins** en fonction de critères spécifiques, notamment l’expérimentation, le ciblage et des conditions spécifiques, garantissant ainsi un engagement et un succès optimaux pour créer des parcours hautement personnalisés et efficaces.

Un parcours **chemin** peut être constitué de l’un des éléments suivants : séquencement des communications, temps écoulé entre les deux, nombre de communications ou toute combinaison de ces trois variables.

Par exemple, un chemin peut contenir un e-mail, un autre peut contenir deux SMS et un troisième peut contenir un e-mail, un nœud Attente de deux heures, puis un SMS.

<!--With this feature, [!DNL Journey Optimizer] empowers you with the tools to deliver personalized and optimized paths to your audience, ensuring maximum engagement and success to create highly customized and effective journeys.-->

Grâce à l’activité **Optimiser**, vous pouvez effectuer les actions suivantes sur les chemins résultants :

* exécuter des [expériences de chemin](#experimentation) ;
* utiliser des règles de [ciblage](#targeting) dans chaque chemin de parcours ;
* appliquer des [conditions](#conditions) à vos chemins.

![](assets/journey-optimize.png)

Une fois le parcours actif, les profils sont évalués en fonction des critères définis. Puis, en fonction des critères correspondants, ils sont envoyés vers le chemin approprié du parcours.

## Utiliser l’expérimentation {#experimentation}

>[!CONTEXTUALHELP]
>id="ajo_path_experiment_success_metric"
>title="Mesure de succès"
>abstract="La mesure de succès permet de suivre et d’évaluer le traitement le plus performant dans une expérience."

L’expérimentation permet de tester plusieurs chemins selon un partage aléatoire afin de déterminer celui qui offre les meilleures performances en fonction de mesures de succès prédéfinies.

Pour configurer l’expérimentation de chemin dans un parcours, procédez comme suit.

Supposons que vous souhaitiez comparer trois chemins :

* Un chemin avec un e-mail
* un deuxième chemin avec un nœud **[!UICONTROL Wait]** de deux jours et un e-mail ;
* Un troisième chemin avec un e-mail, puis un SMS

1. Dans la section **[!UICONTROL Orchestration]**, faites glisser l’activité **[!UICONTROL Optimiser]** et déposez-la dans la zone de travail du parcours.

1. Ajoutez un libellé facultatif, ce qui peut s’avérer utile pour identifier l’activité dans les journaux de rapports et de mode test.

1. Sélectionnez **[!UICONTROL Expérience]** dans la liste déroulante **[!UICONTROL Méthode]**.

   ![](assets/journey-optimize-experiment.png){width=65%}

1. Cliquez sur **[!UICONTROL Créer une expérience]**.

1. Sélectionnez la **[!UICONTROL mesure de succès]** que vous souhaitez définir pour votre expérience. En savoir plus sur les mesures disponibles et sur la configuration de la liste dans [cette section](success-metrics.md).

   <!--Need to have the list of all default metrics + a description for each.
    Explain why the metric selection is important.
    Are there custom metrics? If so explain.
    If possible, add best practices and examples for each metrics (could even be a dedicated section).
    Consider adding an example in this step: For this example, select this metric to test xxx.
    -->

   ![](assets/journey-optimize-experiment-metrics.png){width=80%}

1. Vous pouvez choisir d’ajouter un groupe d’exclusion **[!UICONTROL à votre diffusion]** Ce groupe n’entre dans aucun chemin à partir de cette expérience.

   >[!NOTE]
   >
   >Activer la barre de bascule retirera automatiquement 10 % de votre population. Vous pouvez ajuster ce pourcentage si nécessaire.

   <!--
    DOES THIS APPLY TO PATH EXPERIMENT?
    IMPORTANT: When a holdout group is used in an action for path experimentation, the holdout assignment only applies to that specific action. After the action is completed, profiles in the holdout group will continue down the journey path and can receive messages from other actions. Therefore, ensure that any subsequent messages do not rely on the receipt of a message by a profile that might be in a holdout group. If they do, you may need to remove the holdout assignment.-->

1. Vous pouvez attribuer un pourcentage précis à chaque **[!UICONTROL Traitement]** ou simplement activer la barre de bascule **[!UICONTROL Répartir proportionnellement]**.

   ![](assets/journey-optimize-experiment-treatments.png){width=80%}

1. Cliquez sur **[!UICONTROL Créer]**.

1. Définissez les éléments souhaités pour chaque branche résultant de l’expérience, par exemple :

   * Effectuez un glisser-déposer d&#39;une activité [E-mail](../email/create-email.md) sur la première branche (**Traitement A**).

   * Effectuez un glisser-déposer d’une activité [Attente](wait-activity.md) de deux jours sur la première branche, suivie d’une activité [E-mail](../email/create-email.md) (**Traitement B**).

   * Effectuez un glisser-déposer d’une activité [E-mail](../email/create-email.md) sur la troisième branche, suivie d’une activité [SMS](../sms/create-sms.md) (**Traitement C**).

   ![](assets/journey-optimize-experiment-ex.png){width=100%}

1. Vous pouvez éventuellement utiliser l’**[!UICONTROL Ajouter un itinéraire alternatif en cas de temporisation ou d’erreur]** pour définir une action de remplacement. [En savoir plus](using-the-journey-designer.md#paths)

1. Sélectionnez une action de canal et utilisez le bouton **[!UICONTROL Modifier le contenu]** pour accéder aux outils de conception.

   ![](assets/journey-optimize-experiment-edit-content.png){width=70%}

1. À partir de là, dans le volet de gauche, vous pouvez naviguer entre les différents contenus de chaque action de votre expérience. Sélectionnez chaque contenu et concevez-le selon vos besoins.

   ![](assets/journey-optimize-experiment-content.png){width=100%}

1. [Publier](publishing-the-journey.md) votre parcours.

Une fois le parcours actif, les utilisateurs et utilisatrices sont affectés de manière aléatoire à différents chemins. [!DNL Journey Optimizer] permet de déterminer le chemin le plus performant et fournit des informations exploitables.

Suivez la réussite de votre parcours avec le rapport d’expérience de chemin de Parcours. [En savoir plus](../reports/journey-global-report-cja-experimentation.md)

### Cas d’utilisation d’expérience {#uc-experiment}

Les exemples suivants montrent comment utiliser l’activité **[!UICONTROL Optimiser]** avec la méthode **[!UICONTROL Expérience]** pour déterminer le chemin qui fonctionne le mieux globalement.

+++Efficacité des canaux

Testez si l’envoi du premier message par e-mail plutôt que par SMS génère un taux de conversion plus élevé.

➡️ Utilisez le taux de conversion comme mesure de succès (par exemple : achats, inscriptions).

![](assets/journey-optimize-experiment-uc-channel.png)

+++

+++Fréquence des messages

Exécutez une expérience pour vérifier si l’envoi d’un e-mail plutôt que de trois e-mails sur une semaine entraîne plus d’achats.

➡️ Utilisez les achats ou le taux de désabonnement comme mesure de succès.

![](assets/journey-optimize-experiment-uc-frequency.png)

+++

+++Temps d’attente entre les communications

Comparez une attente de 24 heures à une attente de 72 heures avant une relance afin de déterminer quel délai maximise l’engagement.

➡️ Utilisez le taux de clic publicitaire ou le chiffre d’affaires comme mesure de succès.

![](assets/journey-optimize-experiment-uc-wait.png)

+++

## Tirer profit du ciblage {#targeting}

>[!CONTEXTUALHELP]
>id="ajo_path_targeting_fallback"
>title="Qu’est-ce qu’un chemin de secours ?"
>abstract="Les chemins de secours permettent à l’audience d’entrer sur un autre chemin lorsqu’aucune règle de ciblage n’est applicable. </br>Si vous ne sélectionnez pas cette option, toute audience qui ne remplit pas les critères d’une règle de ciblage ne peut pas accéder au chemin de secours et quitter le parcours."

Les règles de ciblage vous permettent de déterminer les règles ou qualifications spécifiques qui doivent être remplies pour qu’un client soit éligible pour accéder à l’un des chemins de parcours, en fonction de segments d’audience spécifiques<!-- depending on profile attributes or contextual attributes-->.

Contrairement à l’expérimentation, qui est une affectation aléatoire d’un chemin donné, le ciblage est déterministe dans la mesure où il garantit que l’audience ou le profil approprié rejoint chemin spécifié.

<!--With targeting, specific rules can be defined based on:

* **User profile attributes** such as location (eg. geo-targeting), age, or preferences. For example, users in the US receive a "Golden Gate" promotion, while users in France receive an "Eiffel Tower" promotion.

* **Contextual data** such as device type (eg. device-targeting), time of day, or session details. For example, desktop users receive desktop-optimized content, while mobile users receive mobile-optimized content.

* **Audiences** which can be used to include or exclude profiles that have a particular audience membership.-->

Pour configurer le ciblage dans un parcours, suivez les étapes ci-dessous.

1. Dans la section **[!UICONTROL Orchestration]**, faites glisser l’activité **[!UICONTROL Optimiser]** et déposez-la dans la zone de travail du parcours.

1. Ajoutez un libellé facultatif, ce qui peut s’avérer utile pour identifier l’activité dans les journaux de rapports et de mode test.

1. Sélectionnez **[!UICONTROL Règle de ciblage]** dans la liste déroulante **[!UICONTROL Méthode]**.

   ![](assets/journey-optimize-targeting.png){width=60%}

1. Cliquez sur **[!UICONTROL Créer une règle de ciblage]**.

1. Utilisez le créateur de règles pour définir vos critères. Par exemple, définissez une règle pour les membres Gold du programme de fidélité (`loyalty.status.equals("Gold", false)`) et une règle pour les autres membres (`loyalty.status.notEqualTo("Gold", false)`).

   ![](assets/journey-targeting-rule.png)

1. Sélectionnez l’option **[!UICONTROL Activer le chemin de secours]** selon vos besoins. Cette action crée un chemin de secours pour l’audience qui ne répond à aucune des règles de ciblage définies ci-dessus.

   >[!NOTE]
   >
   >Si vous ne sélectionnez pas cette option, toute audience qui ne remplit pas les critères d’une règle de ciblage ne rejoint pas le chemin de secours et quitte le parcours.

1. Cliquez sur **[!UICONTROL Créer]** pour enregistrer les paramètres de votre règle de ciblage.

1. De retour dans le parcours, déposez des actions spécifiques pour personnaliser chaque chemin. Par exemple, créez un e-mail contenant des offres personnalisées pour les membres du programme de fidélité Gold et un rappel SMS pour tous les autres membres.

   ![](assets/journey-targeting-paths.png)

1. Si vous avez sélectionné l’option **[!UICONTROL Activer le contenu de secours]** lors de la définition des paramètres de la règle, définissez une ou plusieurs actions pour le chemin de secours qui a été automatiquement ajouté.

   ![](assets/journey-targeting-fallback.png){width=70%}

1. Vous pouvez éventuellement utiliser l’option **[!UICONTROL Ajouter un itinéraire alternatif en cas de temporisation ou d’erreur]** pour définir une autre action en cas de problème. [En savoir plus](using-the-journey-designer.md#paths)

1. Concevez le contenu approprié pour chaque action correspondant à chaque groupe défini par les paramètres de vos règles de ciblage. Vous pouvez naviguer facilement entre les différents contenus de chaque action.

   ![](assets/journey-targeting-design.png)

   Dans cet exemple, créez un e-mail contenant des offres spéciales pour les membres Gold et un rappel SMS pour les autres membres.

1. [Publier](publishing-the-journey.md) votre parcours.

Une fois le parcours actif, le chemin d’accès spécifié pour chaque segment est traité afin que les membres Gold rejoignent le chemin d’accès avec les offres par e-mail, tandis que les autres membres rejoignent le chemin d’accès avec le rappel SMS.

Suivez la réussite de votre parcours avec le rapport de Parcours. [En savoir plus](../reports/journey-global-report-cja.md#targeting)

### Cas d’utilisation des règles de ciblage {#uc-targeting}

Les exemples suivants montrent comment utiliser l&#39;activité **[!UICONTROL Optimize]** avec la méthode **[!UICONTROL Règle de ciblage]** afin de personnaliser les chemins d&#39;accès pour différentes sous-audiences.

+++Canaux spécifiques au segment

Les membres Gold peuvent recevoir des offres personnalisées par e-mail, tandis que les autres membres sont redirigés vers des rappels par SMS.

<!--➡️ Use the revenue per profile or conversion rate as the optimization metric.-->

![](assets/journey-optimize-targeting-uc-segment.png)

+++

+++Ciblage basé sur le comportement

Les clientes et clients qui ont ouvert un e-mail mais qui n’ont pas cliqué peuvent recevoir une notification push, tandis que ceux et celles qui ne l’ont pas ouvert du tout reçoivent un SMS.

<!--➡️ Use the click-through rate or downstream conversions as the optimization metric.-->

![](assets/journey-optimize-targeting-uc-behavior.png)

+++

+++Ciblage de l’historique des achats

Les clientes et clients qui ont récemment acheté des produits peuvent choisir un chemin court « Merci + vente croisée », tandis que ceux et celles qui n’ont pas d’historique d’achat rejoignent un parcours d’accompagnement plus long.

<!--➡️ Use the repeat purchase rate or engagement rate as the optimization metric.-->

![](assets/journey-optimize-targeting-uc-purchase.png)

+++

### Ajouter une condition {#conditions}

Les conditions sont un type de règles [de ciblage](#targeting) qui permet de définir la progression d’un individu dans un parcours en créant plusieurs chemins d’accès selon des critères spécifiques.

![](assets/journey-condition.png)

Découvrez comment définir une condition dans [cette section](conditions.md).

Les types de condition disponibles sont les suivants :

* [Condition de source de données](condition-activity.md#data_source_condition)
* [Condition de temps](condition-activity.md#time_condition)
* [Partage en pourcentage](condition-activity.md#percentage_split)
* [Condition de date](condition-activity.md#date_condition)
* [Limite de profils](condition-activity.md#profile_cap)
