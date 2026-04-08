---
solution: Journey Optimizer
product: journey optimizer
title: Expérimentation du chemin
description: Découvrez comment utiliser l’expérimentation de chemin dans les parcours
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: expérimentation, expérience, parcours, chemin, optimisation, test A/B, bandit manchot, mettre le gagnant à l’échelle
exl-id: 7241ade3-577c-4bb3-b0c3-017133871ca5
source-git-commit: 9cf7479bcdb12e5d2ebadfcf977b17738a97536d
workflow-type: tm+mt
source-wordcount: '1107'
ht-degree: 77%

---

# Utiliser l’expérimentation de chemin {#experimentation}

>[!CONTEXTUALHELP]
>id="ajo_path_experiment_success_metric"
>title="Mesure de succès"
>abstract="La mesure de succès permet de suivre et d’évaluer le traitement le plus performant dans une expérience."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/orchestrate-journeys/create-journey/success-metrics" text="Configurer et suivre les mesures de votre parcours"

L’expérimentation permet de tester plusieurs chemins selon un partage aléatoire afin de déterminer celui qui offre les meilleures performances en fonction de mesures de succès prédéfinies.

Pour configurer l’expérimentation des chemins dans un parcours, suivez les étapes ci-après.

Supposons que vous souhaitiez comparer trois chemins :

* Un chemin avec un e-mail
* Un deuxième chemin avec un nœud d’**[!UICONTROL attente]** de deux jours et un e-mail
* Un troisième chemin avec un e-mail, puis un SMS

1. Dans la section **[!UICONTROL Orchestration]**, faites glisser l’activité **[!UICONTROL Optimiser]** et déposez-la dans la zone de travail du parcours.

1. Ajoutez un libellé facultatif qui peut servir à identifier l’activité dans les journaux en mode de test et les rapports.

1. Sélectionnez **[!UICONTROL Expérience]** dans la liste déroulante **[!UICONTROL Méthode]**.

   ![Panneau de configuration de l’expérience Path](assets/journey-optimize-experiment.png){width=65%}

1. Cliquez sur **[!UICONTROL Créer une expérience]**.

1. Sélectionnez les **[!UICONTROL mesures de succès]** que vous souhaitez définir pour votre expérience. En savoir plus sur les mesures disponibles et sur la configuration de la liste dans [cette section](success-metrics.md).

   ![Sélection de métriques principales et supplémentaires pour l’expérience](assets/journey-optimize-experiment-metrics.png){width=80%}

1. Sélectionnez le **[!UICONTROL Type d’expérience]** pour votre expérience de chemin d’accès :

   * **[!UICONTROL Expérience A/B]** — Définissez la répartition du trafic entre les traitements au début du test. Les performances sont évaluées en fonction de la mesure principale que vous avez choisie. Les rapports montrent l’effet élévateur observé entre les traitements.

   * **[!UICONTROL Bandit manchot]** — La répartition du trafic entre les traitements est gérée automatiquement. Tous les 7 jours, les performances de la mesure principale sont examinées et les pondérations sont ajustées en conséquence. La création de rapports continue d’afficher une courbe d’élévation, comme pour les tests A/B.

   ![Liste déroulante Type d’expérience dans l’expérience de chemin](assets/journey-path-experiment-type.png){width=80%}

   ➡️ [En savoir plus sur la différence entre les expériences A/B et le bandit manchot](../content-management/mab-vs-ab.md)

1. Vous pouvez ajouter un groupe d’**[!UICONTROL exclusion]** à votre diffusion. Ce groupe ne rejoindra aucun chemin de cette expérience.

   >[!NOTE]
   >
   >Le fait d’activer le bouton (bascule) retirera automatiquement 10 % de votre population. Vous pouvez ajuster ce pourcentage si nécessaire.

   <!--
    DOES THIS APPLY TO PATH EXPERIMENT?
    IMPORTANT: When a holdout group is used in an action for path experimentation, the holdout assignment only applies to that specific action. After the action is completed, profiles in the holdout group will continue down the journey path and can receive messages from other actions. Therefore, ensure that any subsequent messages do not rely on the receipt of a message by a profile that might be in a holdout group. If they do, you may need to remove the holdout assignment.-->

1. Vous pouvez ensuite choisir d’attribuer un pourcentage précis à chaque **[!UICONTROL Traitement]** ou simplement ou simplement activer le bouton (bascule) **[!UICONTROL Répartir proportionnellement]**.

   ![Curseur d’affectation de traitement avec distribution en pourcentage](assets/journey-optimize-experiment-treatments.png){width=80%}

1. Activez l’expérience avec mise à l’échelle automatique pour déployer automatiquement la variation gagnante de votre expérience. [Découvrir comment mettre à l’échelle le gagnant](#scale-winner)

1. Cliquez sur **[!UICONTROL Créer]**.

1. Définissez les éléments de chaque branche résultant de l’expérience, par exemple :

   * Effectuez un glisser-déposer d’une activité [E-mail](../email/create-email.md) sur la première branche (**Traitement A**).

   * Effectuez un glisser-déposer d’une activité [Attente](wait-activity.md) de deux jours sur la première branche, suivie d’une activité [E-mail](../email/create-email.md) (**Traitement B**).

   * Effectuez un glisser-déposer d’une activité [E-mail](../email/create-email.md) sur la troisième branche, suivie d’une activité [SMS](../sms/create-sms.md) (**Traitement C**).

   ![Exemple d’expérience de chemin avec trois chemins de traitement](assets/journey-optimize-experiment-ex.png){width=100%}

1. Vous pouvez éventuellement utiliser l’**[!UICONTROL Ajouter un itinéraire alternatif en cas de temporisation ou d’erreur]** pour définir une action de remplacement. [En savoir plus](using-the-journey-designer.md#paths)

1. [Publiez](publish-journey.md) votre parcours.

<!--

    Select a channel action and use the **[!UICONTROL Edit content]** button to access the design tools.

    ![Edit content button in channel action activity](assets/journey-optimize-experiment-edit-content.png){width=70%}

    From there, using the left pane you can navigate between the different contents for each action in your experiment. Select each content and design it as needed.

    ![Content selection panel showing treatments for experiment](assets/journey-optimize-experiment-content.png){width=100%}

-->

Une fois le parcours actif, les utilisateurs et utilisatrices sont affectés de manière aléatoire à différents chemins. [!DNL Journey Optimizer] suit le chemin le plus performant et fournit des informations exploitables.

Suivez le succès de votre parcours avec le rapport d’expérience de chemin de parcours. [En savoir plus](../reports/journey-global-report-cja-experimentation.md)

<!--REMOVED WITH GA

>[!CAUTION]
>
>Do not edit the metadata of a path experiment once it has been published. Editing the metadata will disrupt the calculation and reporting of experiment results.
-->

## Cas d’utilisation des expériences {#uc-experiment}

Les exemples suivants montrent comment utiliser l’activité **[!UICONTROL Optimiser]** avec la méthode **[!UICONTROL Expérience]** pour déterminer le chemin qui fonctionne le mieux globalement.

+++Efficacité des canaux

Testez si l’envoi du premier message par e-mail plutôt que par SMS génère un taux de conversion plus élevé.

➡️ Utilisez le taux de conversion comme mesure de succès (par exemple : achats, inscriptions).

![Expérience sur l’efficacité des canaux comparant les e-mails aux SMS](assets/journey-optimize-experiment-uc-channel.png)

+++

+++Fréquence des messages

Exécutez une expérience pour vérifier si l’envoi d’un e-mail plutôt que de trois e-mails sur une semaine entraîne plus d’achats.

➡️ Utilisez les achats ou le taux de désabonnement comme mesure de succès.

![Expérience de fréquence des messages testant un e-mail par rapport à trois e-mails](assets/journey-optimize-experiment-uc-frequency.png)

+++

+++Temps d’attente entre deux communications

Comparez une attente de 24 heures à une attente de 72 heures avant une relance afin de déterminer quel délai maximise l’engagement.

➡️ Utilisez le taux de clics ou le chiffre d’affaires comme mesure de succès.

![Expérience sur le temps d’attente comparant des retards de 24 heures à des retards de 72 heures](assets/journey-optimize-experiment-uc-wait.png)

+++

## Mettre à l’échelle le gagnant {#scale-winner}

>[!AVAILABILITY]
>
>Pour les expériences de parcours, la fonction Mettre à l’échelle le gagnant est disponible uniquement dans les parcours unitaires (qualifications déclenchées par un événement et audience).
>
>Elle n’est pas disponible pour les parcours Lecture d’audience .

Mettre à l’échelle le gagnant vous permet de déployer automatiquement ou manuellement la variation gagnante d’une expérience sur l’ensemble de votre audience. Cette fonctionnalité vous permet, une fois un gagnant déterminé, d’en amplifier la portée et l’efficacité sans avoir à surveiller continuellement l’expérience.

Vous pouvez choisir entre deux modes :

* **Mise à l’échelle automatique** : configurez les paramètres de mise à l’échelle automatique lors de la création de votre expérience, en définissant le moment et les conditions de mise à l’échelle du traitement gagnant ou d’une solution de secours si aucun gagnant n’émerge.

* **Mise à l’échelle manuelle** : examinez manuellement les résultats de l’expérience et déclenchez le déploiement du traitement gagnant en gardant un contrôle total sur le moment et les décisions.

### Mise à l’échelle automatique {#autoscaling}

La mise à l’échelle automatique vous permet de définir des règles prédéfinies pour déterminer quand déployer le traitement gagnant ou une solution de secours en fonction des résultats de l’expérience.

Remarque : une fois la mise à l’échelle automatique effectuée, la mise à l’échelle manuelle n’est plus disponible.

Pour activer la mise à l’échelle automatique dans vos expériences :

1. Configurez votre parcours et configurez votre expérience selon les besoins. [En savoir plus](#experimentation)

1. Activez l’option de mise à l’échelle automatique pendant la configuration de l’expérience.

   ![Option de mise à l’échelle automatique dans l’expérience de chemin](assets/journey-optimize-autoscale.png)

1. Définissez le moment où le gagnant doit être déployé :

   * Dès qu’un gagnant est identifié.
   * Après que l’expérience est active depuis une durée donnée.

   Le moment de la mise à l’échelle doit obligatoirement être planifié avant la date de fin de l’expérience. Si elle est définie pour une heure postérieure à la date de fin, un avertissement de validation s’affiche et le parcours n’est pas publié.

   ![Sélection automatique de l’échelle de temps dans l’expérience de chemin d’accès](assets/journey-optimize-autoscale-time.png)

1. Définissez le comportement de secours si aucun gagnant n’est identifié au moment de la mise à l’échelle :

   * Poursuivre l’expérience jusqu’à la fin prévue.
   * Mettre à l’échelle le traitement alternatif après un délai spécifié.

Une fois tous les paramètres remplis, le gagnant ou le traitement alternatif est envoyé à votre audience.

### Mise à l’échelle manuelle {#manual-scaling}

La mise à l’échelle manuelle vous permet d’examiner les résultats de l’expérience et de décider quand déployer le traitement gagnant selon votre propre planning.

Remarque : si vous effectuez manuellement la mise à l’échelle du gagnant avant le moment prévu pour la mise à l’échelle automatique, cette dernière est annulée.

Pour effectuer la mise à l’échelle manuelle du gagnant de vos expériences :

1. Configurez votre parcours et configurez votre expérience selon les besoins. [En savoir plus](#experimentation)

1. Laissez l’expérience se dérouler jusqu’à ce qu’un gagnant soit identifié ou qu’une signification statistique soit atteinte.

1. Ouvrez votre parcours et sélectionnez l’activité **[!UICONTROL Optimiser]** contenant l’expérience de chemin d’accès.

   Passez en revue les résultats dans la vue **[!UICONTROL Expérience de chemin]** pour identifier le traitement le plus performant.

   ![Gagnant d’échelle manuel dans l’expérience de parcours](assets/journey-optimize-manual-scale-winner.png)

1. Cliquez sur **[!UICONTROL Mettre à l’échelle le traitement]** pour envoyer le traitement gagnant au reste de votre audience.

   <!--![](assets/journey-optimize-scale-treatment.png)-->

1. Dans le menu déroulant, sélectionnez le traitement que vous souhaitez mettre à l’échelle, puis cliquez sur **[!UICONTROL Mettre à l’échelle]**.

   ![Sélection du traitement d’échelle dans l’expérience de chemin](assets/journey-optimize-scale-treatment.png){width=80%}

Remarque : la mise à l’échelle du traitement peut prendre jusqu’à une heure. Vous recevrez une notification une fois la mise à l’échelle manuelle terminée.
