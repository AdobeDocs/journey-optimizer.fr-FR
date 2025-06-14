---
solution: Journey Optimizer
product: journey optimizer
title: Test à blanc du parcours
description: Découvrez comment publier un parcours en mode Exécution d’essai
feature: Journeys
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Disponibilité limitée" type="Informative"
keywords: publication, parcours, actif, validité, vérifier
exl-id: 58bcc8b8-5828-4ceb-9d34-8add9802b19d
source-git-commit: f308668ba1b7b20f6144e9200328e54986f66103
workflow-type: tm+mt
source-wordcount: '930'
ht-degree: 11%

---

# Test à blanc du parcours {#journey-dry-run}

>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run"
>title="Mode d’exécution d’essai"
>abstract="Ce parcours est en cours d’exécution d’essai. L’essai de parcours est un mode de publication de parcours spécial dans Adobe Journey Optimizer qui permet aux praticiens du parcours de tester un parcours à l’aide de données de production réelles sans contacter de vrais clients ou mettre à jour les informations de profil.  Cette fonctionnalité permet aux utilisateurs et utilisatrices du parcours d’avoir confiance dans leur conception de parcours et leur ciblage d’audience avant de le publier en direct."


>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run_start"
>title="Publication d’un parcours en mode d’exécution d’essai"
>abstract="L’essai de parcours est un mode de publication de parcours spécial dans Adobe Journey Optimizer qui permet aux praticiens du parcours de tester un parcours à l’aide de données de production réelles. Une fois que vous avez conçu votre parcours, effectuez un test à blanc pour confirmer qu’il est fonctionnel et vous assurer que les étapes sont correctes. Ce mode de publication vous permet de tester un parcours sans envoyer de communication à un profil."

L’essai de parcours est un mode de publication de parcours spécial dans Adobe Journey Optimizer qui permet aux praticiens du parcours de tester un parcours à l’aide de données de production réelles sans contacter de vrais clients ou mettre à jour les informations de profil.  Cette fonctionnalité permet aux utilisateurs et utilisatrices du parcours d’avoir confiance dans leur conception de parcours et leur ciblage d’audience avant de le publier en direct.


>[!AVAILABILITY]
>
>Cette fonctionnalité n’est disponible que pour un ensemble d’organisations (disponibilité limitée) et sera déployée à l’échelle mondiale dans une prochaine version.


## Avantages clés {#journey-dry-run-benefits}

Le parcours Dry Run améliore la confiance des professionnels et la réussite du parcours en permettant des tests sûrs et pilotés par les données des parcours clients à l’aide de données de production réelles, sans risque de contacter les clients ou de modifier les informations de profil. Cette fonctionnalité permet aux spécialistes du parcours de valider la portée de l’audience et la logique des branches avant la mise en ligne, en s’assurant que les parcours s’alignent sur les objectifs commerciaux prévus.

Grâce au Parcours Dry Run, vous avez la possibilité d’identifier les problèmes dès le début, d’optimiser les stratégies de ciblage et d’améliorer la conception du parcours en fonction des données réelles, et non des hypothèses. Directement intégré à la zone de travail de parcours, Dry Run offre des rapports intuitifs et une visibilité sur les indicateurs de performances clés, ce qui permet aux équipes d’effectuer une itération en toute confiance et de rationaliser les workflows d’approbation. Cela améliore l’efficacité opérationnelle, réduit les risques de lancement et génère de meilleurs résultats d’engagement client.

Cette fonctionnalité améliore le temps nécessaire à la valorisation et réduit les défaillances du parcours.

L’essai de parcours apporte :

1. **Environnement de test sécurisé** : les profils en mode d’exécution d’essai ne sont pas contactés, ce qui élimine tout risque d’envoi de communications ou d’impact sur les données actives.
1. **Informations sur l’audience** : les praticiens du Parcours peuvent prédire l’accessibilité de l’audience à divers nœuds du parcours, y compris les désinscriptions, les exclusions et d’autres conditions.
1. **Commentaires en temps réel** : les mesures s’affichent directement dans la zone de travail du parcours, comme les rapports en direct, ce qui permet aux spécialistes du parcours d’affiner leur conception de parcours.


>[!CAUTION]
>
>* Les autorisations de démarrage de l’exécution d’essai sont limitées aux utilisateurs disposant de l’autorisation de haut niveau **[!DNL Publish journeys]**. Les autorisations d’arrêt de l’exécution d’essai sont limitées aux utilisateurs disposant de l’autorisation de haut niveau **[!DNL Manage journeys]**. Pour en savoir plus sur la gestion des droits d’accès des utilisateurs et des utilisatrices [!DNL Journey Optimizer], consultez [cette section](../administration/permissions-overview.md).
>
>* Avant de commencer à utiliser la fonctionnalité Exécution d’essai, [lisez les mécanismes de sécurisation et limites](#journey-dry-run-limitations).


## Démarrer une exécution d’essai {#journey-dry-run-start}

Vous pouvez utiliser la fonctionnalité Exécution d’essai dans n’importe quel parcours Brouillon sans erreur.

Pour activer l’exécution d’essai, procédez comme suit :

1. Ouvrez le parcours que vous souhaitez tester.
1. Cliquez sur le bouton **Exécution d’essai**.

   ![Démarrer la simulation du parcours ](assets/dry-run-button.png)

1. Confirmez la publication.

   Un message de statut, **Activation de l’exécution d’essai**, s’affiche pendant que la transition est en cours.

1. Une fois activé, le parcours passe en mode **Exécution d’essai**.

## Surveillance d’une exécution d’essai {#journey-dry-monitor}

Une fois la publication en mode sec lancée, vous pouvez visualiser l’exécution du parcours et la progression des profils dans les branches et les nœuds de parcours.

Les mesures s’affichent directement dans la zone de travail du parcours.

![Surveiller l’exécution de l’essai de parcours ](assets/dry-run-metrics.png)

Pour chaque activité, vous pouvez vérifier les éléments suivants :

* **[!UICONTROL Entrées]** : nombre total de personnes ayant rejoint cette activité.
* **[!UICONTROL Sorties (critères de sortie remplis)]** : nombre total de personnes ayant quitté le parcours de cette activité en raison d’un critère de sortie.
* **[!UICONTROL Sorti (sortie forcée)]** : nombre total de personnes ayant quitté le parcours alors qu’il était en pause en raison d’une configuration de praticien de parcours. Cette mesure est toujours égale à zéro pour les parcours en mode d’exécution d’essai.
* **[!UICONTROL Erreur]** : nombre total de personnes ayant rencontré une erreur pour cette activité.


Au niveau du parcours, vous pouvez vérifier les éléments suivants :

* Nombre total de **profils entrés**
* Nombre total de **profils sortis**
* Nombre total de **profils en erreur**
* Nombre total de **profils ignorés** dans le parcours

Vous pouvez également accéder aux **Rapports des dernières 24 heures** et **Rapports à tout moment** pour l’exécution d’essai. Pour accéder à ces rapports, cliquez sur le bouton **Afficher le rapport** dans le coin supérieur droit de la zone de travail du parcours.

![Accédez aux rapports pour l’exécution de l’essai du parcours ](assets/dry-run-report.png)

>[!CAUTION]
>
> Les données de rapport sont disponibles uniquement lorsque l’Exécution d’essai est **active**.  Une fois cette opération arrêtée, les données de rapport ne seront plus accessibles. Utilisez le bouton **Exporter** situé au-dessus des rapports pour les télécharger si nécessaire.


## Arrêt d’une exécution d’essai {#journey-dry-run-stop}

Les parcours d’essai **doivent** doivent être arrêtés manuellement.

Cliquez sur le bouton **Fermer** pour terminer le test, puis sur **Retour au brouillon** pour confirmer.

<!-- After 14 days, Dry run journeys automatically transition to the **Draft** status.-->

## Mécanismes de sécurisation et limitations {#journey-dry-run-limitations}

* Le mode Exécution d’essai n’est pas disponible pour les parcours contenant des événements de réaction.
* Les profils en mode Exécution d’essai sont comptabilisés dans les profils engageables.
* Les parcours d’exécution d’essai n’ont aucune incidence sur les règles métier.
* Lors de la création d’une version de parcours, si une version de parcours précédente est **en ligne**, l’activation de l’exécution d’essai n’est pas autorisée sur la nouvelle version.
* L’exécution d’essai de parcours génère des événements stepEvents. Ces événements stepEvents disposent d’un indicateur et d’un identifiant d’exécution d’essai spécifiques :
   * `_experience.journeyOrchestration.stepEvents.inDryRun` renvoie `true` si l’Exécution d’essai est activée et `false` dans le cas contraire
   * `_experience.journeyOrchestration.stepEvents.dryRunID` renvoie l’identifiant d’une instance d’essai
* Lors de l’exécution de l’essai, le parcours est exécuté avec les spécificités suivantes :

   * Les nœuds **Action de canal** notamment les e-mails, SMS ou notifications push ne sont pas exécutés.
   * Les **actions personnalisées** sont désactivées pendant l’exécution d’essai et leurs réponses sont définies sur null.
   * Les **nœuds d’attente** sont ignorés lors de l’exécution de l’essai.
     <!--You can override the wait block timeouts, then if you have wait blocks duration longer than allowed dry run journey duration, then that branch will not execute completely.-->
   * **Les sources de données** y compris les sources de données externes, sont exécutées par défaut.