---
solution: Journey Optimizer
product: journey optimizer
title: Test à blanc du parcours
description: Découvrez comment publier un parcours en mode Test à blanc.
feature: Journeys
role: User
level: Intermediate
badge: label="Disponibilité limitée" type="Informative"
keywords: publication, parcours, actif, validité, vérification
exl-id: 58bcc8b8-5828-4ceb-9d34-8add9802b19d
source-git-commit: fa46397b87ae3a81cd016d95afd3e09bb002cfaa
workflow-type: tm+mt
source-wordcount: '995'
ht-degree: 84%

---

# Test à blanc du parcours {#journey-dry-run}

>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run"
>title="Mode Test à blanc"
>abstract="Ce parcours est en mode Test à blanc. Le test à blanc de parcours est un mode de publication de parcours spécial dans Adobe Journey Optimizer qui permet aux responsables des parcours de tester un parcours à l’aide de données de production réelles sans contacter de véritables clientes et clients ou sans mettre à jour les informations de profil.  Cette fonctionnalité permet aux responsables des parcours d’avoir confiance dans leur conception du parcours et leur ciblage d’audience avant de publier un parcours en ligne."


>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run_start"
>title="Publier un parcours en mode Test à blanc"
>abstract="Le test à blanc de parcours est un mode de publication de parcours spécial dans Adobe Journey Optimizer qui permet aux responsables des parcours de tester un parcours à l’aide de données de production réelles. Une fois que vous avez conçu votre parcours, effectuez un test à blanc pour confirmer qu’il est fonctionnel et vous assurer que les étapes sont correctes. Ce mode de publication vous permet de tester un parcours sans envoyer de communication à un profil."

Le test à blanc de parcours est un mode de publication de parcours spécial dans Adobe Journey Optimizer qui permet aux responsables des parcours de tester un parcours à l’aide de données de production réelles sans contacter de véritables clientes et clients ou sans mettre à jour les informations de profil.  Cette fonctionnalité permet aux responsables des parcours d’avoir confiance dans leur conception du parcours et leur ciblage d’audience avant de publier un parcours en ligne.


>[!AVAILABILITY]
>
>Cette fonctionnalité n’est disponible que pour un certain nombre d’organisations (disponibilité limitée) et sera proposée à tous les utilisateurs et toutes les utilisatrices dans une prochaine version.


## Avantages clés {#journey-dry-run-benefits}

Le test à blanc de parcours améliore la confiance des responsables des parcours et la réussite des parcours en offrant des tests sûrs et pilotés par les données des parcours clients à l’aide de données de production réelles, sans risque de contacter les clientes et clients ou de modifier les informations de profil. Cette fonctionnalité permet aux responsables des parcours de valider la portée de l’audience et la logique des branches avant l’activation, en s’assurant que les parcours s’alignent sur les objectifs commerciaux prévus.

Grâce au test à blanc de parcours, vous avez la possibilité d’identifier les problèmes dès le début, d’optimiser les stratégies de ciblage et d’améliorer la conception du parcours en fonction des données réelles, et non d’hypothèses. Directement intégré à la zone de travail du parcours, le test à blanc offre des rapports intuitifs et une visibilité sur les indicateurs de performances clés, ce qui permet aux équipes de réaliser des ajustements en toute confiance et d’optimiser les workflows d’approbation. Cela améliore l’efficacité opérationnelle, réduit les risques liés au lancement et favorise un meilleur engagement des clientes et clients.

Enfin, cette fonctionnalité améliore le délai de rentabilisation et réduit les défaillances du parcours.

Le test à blanc de parcours apporte :

1. **Environnement de test sécurisé** : les profils en mode Test à blanc ne sont pas contactés, ce qui élimine tout risque d’envoi de communications ou d’impact sur les données actives.
1. **Informations sur l’audience** : les responsables des parcours peuvent prédire l’accessibilité de l’audience à divers nœuds du parcours, y compris les désinscriptions, les exclusions et d’autres conditions.
1. **Commentaires en temps réel** : les mesures s’affichent directement dans la zone de travail du parcours, comme les rapports en temps réel, ce qui permet aux responsables des parcours d’affiner leur conception du parcours.

Lors du test à blanc, le parcours est exécuté avec les spécificités suivantes :

* Les nœuds **Action de canal** notamment les e-mails, SMS ou notifications push ne sont pas exécutés
* Les **actions personnalisées** sont désactivées pendant l’exécution d’essai et leurs réponses sont définies sur null.
* Les **nœuds d’attente** sont ignorés lors du test à blanc.
  <!--You can override the wait block timeouts, then if you have wait blocks duration longer than allowed dry run journey duration, then that branch will not execute completely.-->
* **Les sources de données** y compris les sources de données externes, sont exécutées par défaut

>[!CAUTION]
>
>* Les autorisations de démarrage du test à blanc sont limitées aux utilisateurs et aux utilisatrices disposant de l’autorisation de haut niveau **[!DNL Publish journeys]**. Les autorisations d’arrêt du test à blanc sont limitées aux utilisateurs et utilisatrices disposant de l’autorisation de haut niveau **[!DNL Manage journeys]**. Pour en savoir plus sur la gestion des droits d’accès des utilisateurs et des utilisatrices [!DNL Journey Optimizer], consultez [cette section](../administration/permissions-overview.md).
>
>* Avant de commencer à utiliser la fonctionnalité de test à blanc, [lisez la section sur les Mécanismes de sécurisation et les limitations](#journey-dry-run-limitations).


## Démarrer un test à blanc {#journey-dry-run-start}

Vous pouvez utiliser la fonctionnalité Test à blanc dans n’importe quel brouillon de parcours sans erreur.

Pour activer le test à blanc, procédez comme suit :

1. Ouvrez le parcours que vous souhaitez tester.
1. Sélectionnez le bouton **Exécution d’essai**.

   ![Démarrer le test à blanc du parcours](assets/dry-run-button.png)

1. Confirmez la publication.

   Un message de statut, **Activation du test à blanc**, s’affiche pendant que la transition est en cours.

1. Une fois activé, le parcours passe en mode **Test à blanc**.

## Surveiller un test à blanc {#journey-dry-monitor}

Une fois la publication en mode Test à blanc lancée, vous pouvez visualiser l’exécution du parcours et la progression des profils dans les branches et les nœuds du parcours.

Les mesures s’affichent directement dans la zone de travail du parcours.

![Surveiller l’exécution du test à blanc du parcours](assets/dry-run-metrics.png)

Pour chaque activité, dans leur boîte d&#39;activité, vous pouvez cocher :

* **[!UICONTROL Entrées]** : nombre total de personnes ayant participé à cette activité. Pour les activités **Action**, étant donné qu’elles ne sont pas exécutées en mode d’exécution d’essai, cette mesure indique le passage des profils.
* **[!UICONTROL Sorties (critères de sortie remplis)]** : nombre total de personnes ayant quitté le parcours de cette activité en raison d’un critère de sortie.
* **[!UICONTROL Sorties (sorties forcées)]** : nombre total de personnes ayant quitté le parcours alors qu’il était en pause en raison d’une configuration opérée par la personne responsable du parcours. Cette mesure est toujours égale à zéro pour les parcours en mode Test à blanc.
* **[!UICONTROL Erreur]** : nombre total de personnes ayant rencontré une erreur pour cette activité.


En parcours, dans la section supérieure gauche de la zone de travail, vous pouvez vérifier les éléments suivants :

* Le nombre total de **profils d’entrée**.
* Le nombre total de **profils de sortie**.
* Le nombre total de **profils qui présentent une erreur**.
* Le nombre total de **profils supprimés** dans le parcours.

Vous pouvez également accéder aux **Rapports sur les dernières 24 heures** et aux **Rapports sur la durée entière** pour le test à blanc. Pour accéder à ces rapports, cliquez sur le bouton **Afficher le rapport** dans le coin supérieur droit de la zone de travail du parcours.

![Accéder aux rapports d’exécution du test à blanc du parcours](assets/dry-run-report.png)

>[!CAUTION]
>
> Les données de rapport sont disponibles uniquement lorsque le test à blanc est **actif**.  Dès que celui-ci s’arrête, les données de rapport ne sont plus accessibles. Utilisez le bouton **Exporter** situé au-dessus des rapports pour les télécharger si nécessaire.


## Arrêter un test à blanc {#journey-dry-run-stop}

Les tests à blanc des parcours **doivent obligatoirement** être arrêtés manuellement.

Cliquez sur le bouton **Fermer** pour terminer le test, puis sur **Retour au brouillon** pour confirmer.

<!-- After 14 days, Dry run journeys automatically transition to the **Draft** status.-->

## Mécanismes de sécurisation et limitations {#journey-dry-run-limitations}

* Le mode Exécution d’essai n’est pas disponible pour les parcours contenant des événements de réaction
* Les profils en mode Exécution d’essai sont comptabilisés dans les profils engageables
* Les parcours en mode Exécution d’essai sont comptabilisés dans le quota de parcours en direct
* Les parcours d’essai n’ont aucune incidence sur les règles métier.
* Lors de la création d’une version de parcours, si une version de parcours précédente est **active**, l’activation du test à blanc n’est pas autorisée sur la nouvelle version.
* Un test à blanc de parcours génère des événements stepEvents. Ces événements stepEvents disposent d’un indicateur et d’un identifiant de test à blanc spécifiques :
   * `_experience.journeyOrchestration.stepEvents.inDryRun` renvoie `true` si le test à blanc est activé et `false` dans le cas contraire.
   * `_experience.journeyOrchestration.stepEvents.dryRunID` renvoie l’identifiant d’une instance de test à blanc.

* Lors de l’analyse des mesures de rapports de parcours à l’aide de Adobe Experience Platform Query Service, les événements d’étape générés par l’exécution d’essai doivent être exclus. Pour ce faire, définissez l’indicateur de `inDryRun` sur `false`.