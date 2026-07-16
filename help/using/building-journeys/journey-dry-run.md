---
solution: Journey Optimizer
product: journey optimizer
title: Test à blanc des parcours
description: Découvrez comment publier un parcours en mode Test à blanc.
feature: Journeys
role: User
level: Intermediate
keywords: publication, parcours, actif, validité, vérification
exl-id: 58bcc8b8-5828-4ceb-9d34-8add9802b19d
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/a7qFw84obtkCRDmiqMxQNgvqhI4b6t5suROeF7ZPh1I
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: b3538224-471e-4c63-a444-9b19d89ae29cid: d998adac-2f81-400b-a669-d07bb196e4ebid: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2: id: b15c7c2e-788c-4eb7-86a8-390565b0d2c9id: b32bb433-f8c6-4931-8e52-e657230a3bf2id: cfba2953-2ce9-4b00-a00c-71cd338ae63fid: d8353d85-5da7-453d-bd68-40ad33fa0ab7id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5520579-b31f-4df7-9281-f0d9f91e2edcid: d00e9f03-e50b-4162-b143-0c0817c937c2id: e1e0219c-f879-479f-8427-888ed2a6e9c2
source-git-commit: 41e34973cb3213e08442bead6d1f1bb00af00921
workflow-type: tm+mt
source-wordcount: 2330
ht-degree: 46%

---

# Test à blanc des parcours {#journey-dry-run}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez comment publier un parcours en mode d’exécution d’essai pour le tester avec des données de production réelles sans contacter de vrais clients ou mettre à jour des profils, afin de pouvoir valider votre conception avant sa mise en ligne.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run"
>title="Mode Test à blanc"
>abstract="Ce parcours est en mode Test à blanc. Le test à blanc de parcours est un mode de publication de parcours spécial dans [!DNL Adobe Journey Optimizer] qui permet aux utilisateurs et utilisatrices du parcours de tester un parcours à l’aide de données de production réelles sans contacter de véritables clientes et clients ou mettre à jour les informations de profil.  Cette fonctionnalité permet aux concepteurs et conceptrices du parcours de valider leur conception et leur ciblage d’audience avant de publier le parcours."


>[!CONTEXTUALHELP]
>id="ajo_journey_dry_run_start"
>title="Publier un parcours en mode Test à blanc"
>abstract="Le test à blanc de parcours est un mode de publication de parcours spécial dans [!DNL Adobe Journey Optimizer] qui permet aux utilisateurs et utilisatrices du parcours de tester un parcours à l’aide de données de production réelles. Une fois qu’un parcours est conçu, un test à blanc confirme qu’il est fonctionnel et s’assure que les étapes sont correctes. Ce mode de publication vous permet de tester un parcours sans envoyer de communication à un profil."

Le test à blanc de parcours est un mode de publication de parcours spécial dans [!DNL Adobe Journey Optimizer] qui permet aux utilisateurs et utilisatrices du parcours de tester un parcours à l’aide de données de production réelles sans contacter de véritables clientes et clients ou mettre à jour les informations de profil.  Cette fonctionnalité permet aux concepteurs et conceptrices du parcours de valider leur conception et leur ciblage d’audience avant de publier le parcours.

➡️ [Pour en savoir plus sur le test à blanc des parcours, regardez cette vidéo.](#dry-run-video)

## Avantages clés {#journey-dry-run-benefits}

Le test à blanc de parcours améliore la confiance des responsables des parcours et la réussite des parcours en offrant des tests sûrs et pilotés par les données des parcours clients à l’aide de données de production réelles, sans risque de contacter les clientes et clients ou de modifier les informations de profil. Cette fonctionnalité permet aux responsables des parcours de valider la portée de l’audience et la logique des branches avant l’activation, en s’assurant que les parcours s’alignent sur les objectifs commerciaux prévus.

Grâce au test à blanc de parcours, vous avez la possibilité d’identifier les problèmes dès le début, d’optimiser les stratégies de ciblage et d’améliorer la conception du parcours en fonction des données réelles, et non d’hypothèses. Directement intégré à la zone de travail du parcours, le test à blanc offre des rapports intuitifs et une visibilité sur les indicateurs de performances clés, ce qui permet aux équipes de réaliser des ajustements en toute confiance et d’optimiser les workflows d’approbation. Cela améliore l’efficacité opérationnelle, réduit les risques liés au lancement et favorise un meilleur engagement des clientes et clients.

Enfin, cette fonctionnalité améliore le délai de rentabilisation et réduit les défaillances du parcours.

Le test à blanc de parcours apporte :

1. **Environnement de test sécurisé** : les profils en mode Test à blanc ne sont pas contactés, ce qui élimine tout risque d’envoi de communications ou d’impact sur les données actives.
1. **Informations sur l’audience** : les responsables des parcours peuvent prédire l’accessibilité de l’audience à divers nœuds du parcours, y compris les opt-out et les exclusions en fonction des conditions des parcours.
1. **Commentaires en temps réel** : les mesures s’affichent directement dans la zone de travail du parcours, comme les rapports en temps réel, ce qui permet aux responsables des parcours d’affiner leur conception du parcours.

## Logique d’exécution du test à blanc {#journey-dry-run-exec}

Lors du test à blanc, le parcours s’exécute en mode simulation, en appliquant les comportements spécifiques suivants à chaque activité de parcours sans déclencher d’actions réelles :

* Les nœuds **Action de canal** notamment les e-mails, SMS ou notifications push ne sont pas exécutés.
* Les **actions personnalisées** sont désactivées pendant le test à blanc et leurs réponses sont définies sur null.

  Pour améliorer la lisibilité, les actions personnalisées et les activités de canal apparaissent grisées lors de l’exécution d’un test à blanc.

  ![Activités d’action grisées dans un parcours de test à blanc](assets/dry-run-greyed-activities.png){width="80%"}

* Les **sources de données**, y compris les sources de données externes, et les activités **Attente** sont désactivées par défaut pendant le test à blanc. Vous pouvez toutefois modifier ce comportement [lors de l’activation du mode Test à blanc](#journey-dry-run-start).

* Les nœuds **Réaction** ne sont pas exécutés : tous les profils qui y accèdent les quittent. Toutefois, les règles de priorité suivantes s’appliquent :

   * Si un nœud **Réaction** est utilisé avec un ou plusieurs nœuds d’**événement unitaire** en parallèle, les profils passeront toujours par l’événement de réaction.
   * Si un nœud **Réaction** est utilisé avec un ou plusieurs nœuds d’**événement de réaction** en parallèle, les profils passeront toujours par le premier dans la zone de travail (celui en haut).

* Les activités **Lecture d’audience** dont l’heure d’exécution est planifiée (quotidienne, hebdomadaire ou mensuelle) ne suivent pas l’heure configurée dans le parcours. Le planning est ancré au moment où l’exécution d’essai a été activée. Par exemple, si votre parcours est configuré pour s’exécuter tous les jours à 10 heures du matin, mais que vous activez l’exécution d’essai à 8 heures du matin, toutes les lectures planifiées suivantes au cours de l’exécution d’essai s’exécutent à 8 heures du matin.

>[!CAUTION]
>
>* Les autorisations de démarrage d’un test à blanc sont limitées aux utilisateurs et aux utilisatrices disposant de l’autorisation de haut niveau **[!DNL Publish journeys]**. Les autorisations d’arrêt d’un test à blanc sont limitées aux utilisateurs et aux utilisatrices disposant de l’autorisation de haut niveau **[!DNL Manage journeys]**. Pour en savoir plus sur la gestion des droits d’accès des utilisateurs et des utilisatrices [!DNL Journey Optimizer], consultez [cette section](../administration/permissions-overview.md).
>
>* Avant de commencer à utiliser la fonctionnalité de test à blanc, [lisez la section sur les Mécanismes de sécurisation et les limitations](#journey-dry-run-limitations).

## Démarrer un test à blanc {#journey-dry-run-start}

Vous pouvez utiliser la fonctionnalité Test à blanc dans n’importe quel brouillon de parcours sans erreur.

Pour activer le test à blanc, procédez comme suit :

1. Ouvrez le parcours que vous souhaitez tester.
1. Cliquez sur le bouton **[!UICONTROL Test à blanc]**.

   ![Démarrer le test à blanc du parcours](assets/dry-run-button.png)

1. Indiquez si vous souhaitez activer ou désactiver les activités **Attente** et les appels **Sources de données externes**, puis confirmez la publication du test à blanc.

   ![Confirmer la publication du test à blanc du parcours](assets/dry-run-publish.png){width="50%"}

   Un message de statut, **[!UICONTROL Activation du test à blanc]**, s’affiche pendant que la transition est en cours.

1. Une fois activé, le parcours passe en mode **[!UICONTROL Test à blanc]**.


## Surveiller un test à blanc {#journey-dry-monitor}

Une fois la publication en mode Test à blanc lancée, vous pouvez visualiser l’exécution du parcours et la progression des profils dans les branches et les nœuds du parcours.

Les mesures s’affichent directement dans la zone de travail du parcours. Pour en savoir plus sur les rapports dynamiques et les mesures des parcours, consultez la section [Rapports dynamiques dans la zone de travail du parcours](report-journey.md).

![Surveiller l’exécution du test à blanc du parcours](assets/dry-run-metrics.png)

Vous pouvez également accéder aux **Rapports sur les dernières 24 heures** et aux **Rapports sur la durée entière** pour le test à blanc. Pour accéder à ces rapports, cliquez sur le bouton **Afficher le rapport** dans le coin supérieur droit de la zone de travail du parcours.

![Accéder aux rapports d’exécution du test à blanc du parcours](assets/dry-run-report.png)

>[!CAUTION]
>
> Les données de rapport sont disponibles uniquement lorsque le test à blanc est **actif**.  Dès que celui-ci s’arrête, les données de rapport ne sont plus accessibles. Utilisez le bouton **Exporter** situé au-dessus des rapports pour les télécharger si nécessaire.


## Arrêter un test à blanc {#journey-dry-run-stop}

Après 14 jours, les parcours de test à blanc passent automatiquement au statut **[!UICONTROL Brouillon]**.

Les parcours de test à blanc peuvent également être arrêtés manuellement. Pour désactiver le mode Test à blanc, procédez comme suit :

1. Ouvrez le parcours de test à blanc à arrêter.
1. Sélectionnez le bouton **[!UICONTROL Fermer]** pour terminer le test.
Les liens vers les rapports des 24 dernières heures ou de la durée entière sont disponibles dans l’écran de confirmation.

   ![Arrêter l’exécution du test à blanc du parcours](assets/dry-run-stop.png){width="50%"}

1. Cliquez sur **[!UICONTROL Retour au brouillon]** pour confirmer.


## Mécanismes de sécurisation et limitations {#journey-dry-run-limitations}

* Les profils en mode d’exécution d’essai sont comptabilisés dans les [profils engageables](../audience/license-usage.md)
* Les parcours en mode Test à blanc sont comptabilisés dans le quota des parcours actifs.
* Les parcours en mode Test à blanc n’ont aucune incidence sur les règles métier.
  <!--* When creating a new journey version, if a previous journey version is **Live**, then the Dry run activation is not allowed on the new version.-->
* Les actions **Saut** ne sont pas activées dans le test à blanc.
Lorsqu’un parcours source déclenche un événement de **saut** vers un parcours de destination, cet événement de saut ne s’applique pas à une version de parcours de test à blanc. Par exemple, si la dernière version d’un parcours est en test à blanc et que la version précédente est **active**, l’événement de saut ignorerait la version en test à blanc et ne s’appliquerait qu’à la version **active**.

## Événements d’étape de parcours et essai {#journey-step-events}

Le test à blanc de parcours génère des **événements d’étape**. Ces événements d’étape disposent d’un indicateur et d’un ID de test à blanc spécifiques : `inDryRun` et `dryRunID`.

![Attributs de schéma de test à blanc de parcours](assets/dry-run-attributes.png)

* `_experience.journeyOrchestration.stepEvents.inDryRun` renvoie `true` lorsque le parcours est en mode Exécution d’essai et `null` pour les parcours de test ou en direct (exécution d’essai).
* `_experience.journeyOrchestration.stepEvents.dryRunID` renvoie l’identifiant de l’instance d’exécution d’essai en mode Exécution d’essai ; pour les parcours de test ou en direct, il est `null`.


Si vous exportez des données d’événement d’étape vers des **systèmes externes**, vous pouvez filtrer les exécutions de test à blanc à l’aide de l’indicateur `inDryRun`.

Lors de l’analyse de **mesures de rapports de parcours** à l’aide de [!DNL Adobe Experience Platform] Query Service, les événements d’étape générés par l’exécution d’essai doivent être exclus. Pour ce faire, excluez les événements d’étape où `inDryRun` est `true` (c’est-à-dire incluez uniquement les événements où `inDryRun` est `null` ou `false`).

## Questions fréquentes {#faq}

**Une exécution d’essai envoie-t-elle des messages à des clients réels ?**

Non. L’exécution d’essai utilise des données de production réelles, mais ne contacte pas les profils ni ne met à jour les informations de profil. Les actions de canal (e-mail, SMS, notification push) ne sont pas exécutées et les actions personnalisées sont désactivées avec leurs réponses définies sur `null`.

**De quelles autorisations ai-je besoin pour démarrer ou arrêter une Exécution d’essai ?**

Le démarrage d’une exécution d’essai nécessite l’autorisation de haut niveau **[!DNL Publish journeys]**. L’arrêt d’une exécution d’essai nécessite l’autorisation de haut niveau **[!DNL Manage journeys]**. Pour en savoir plus, consultez la section [autorisations](../administration/permissions-overview.md).

**Sur quels parcours puis-je exécuter une Exécution d’essai ?**

Vous pouvez utiliser l’exécution d’essai sur n’importe quel parcours **[!UICONTROL Brouillon]** sans erreur.

**Combien de temps dure une exécution d’essai ?**

Après 14 jours, les parcours d’exécution d’essai repassent automatiquement au statut **[!UICONTROL Brouillon]**. Vous pouvez également arrêter manuellement une exécution d’essai à tout moment.

**Les activités d’attente et les sources de données externes sont-elles exécutées pendant une exécution d’essai ?**

Par défaut, les activités **Attente** et **Sources de données** (y compris les sources de données externes) sont désactivées lors d’une exécution d’essai. Vous pouvez modifier ce comportement lors de l’[activation du mode Exécution d’essai](#journey-dry-run-start).

**Les profils et parcours d’essai sont-ils pris en compte dans mes quotas ?**

Oui. Les profils en mode d’exécution d’essai sont comptabilisés dans le nombre de [Profils engageables](../audience/license-usage.md), et les parcours en mode d’exécution d’essai sont comptabilisés dans le quota de parcours en direct. Toutefois, les parcours d’exécution d’essai n’ont aucune incidence sur les règles métier.

**Puis-je toujours accéder aux rapports d’essai après l’arrêt du test ?**

Non. Les données de rapport ne sont disponibles que lorsque l’Exécution d’essai est **active**. Une fois arrêtés, les données ne sont plus accessibles : utilisez le bouton **Exporter** situé au-dessus des rapports pour les télécharger à l’avance, si nécessaire.

**Comment exclure les données d’essai de mes rapports ?**

L’exécution d’essai génère **stepEvents** marqué d’un `inDryRun` et d’un `dryRunID`. Lors de l’analyse des mesures de rapports de parcours avec [!DNL Adobe Experience Platform] Query Service, excluez les événements d’étape où `inDryRun` est `true` (incluez uniquement les événements où `inDryRun` est `null` ou `false`).

**L’heure d’exécution planifiée d’une activité Lecture d’audience change-t-elle dans l’exécution d’essai ?**

Oui. Pour les parcours utilisant une activité **Lecture d’audience** avec une heure planifiée (quotidienne, hebdomadaire ou mensuelle), l’exécution d’essai ancre la planification au moment où l’exécution d’essai a été activée, et non à l’heure configurée dans le parcours. Par exemple, si le parcours est configuré pour s’exécuter à 10 heures du matin mais que vous activez l’exécution d’essai à 8 heures du matin, toutes les lectures quotidiennes pendant l’exécution d’essai s’exécutent à 8 heures du matin.

## Vidéo pratique {#dry-run-video}

Découvrez comment exécuter un test à blanc de vos parcours dans cette vidéo.

>[!VIDEO](https://video.tv.adobe.com/v/3464681/?learn=on&enablevpops)

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page explique l’exécution d’essai de Parcours, un mode de publication spécial qui permet aux utilisateurs de tester un parcours à l’aide de données de production réelles sans contacter les clients ni modifier les profils. Elle explique également comment démarrer, surveiller, arrêter et filtrer les événements d’étape d’exécution d’essai.

**Intentions:**
* Activez le mode Exécution d’essai sur un parcours Brouillon pour valider la portée de l’audience et la logique des branches avec les données de production réelles
* Surveiller les mesures d’exécution de parcours dans la zone de travail lors d’une exécution d’essai
* Arrêtez manuellement une Exécution d’essai et revenez au statut Brouillon du parcours
* Filtrez les événements d’étape d’exécution d’essai sur les requêtes de création de rapports à l’aide de l’indicateur `inDryRun`
* Identifiez les activités désactivées ou simulées pendant une exécution d’essai

**Glossaire:**
* **Exécution d’essai** : mode de publication de parcours spécial qui exécute le parcours par rapport aux données de production réelles sans envoyer de communications ni mettre à jour les informations de profil *(spécifiques au produit)*
* **stepEvent** : enregistrement de jeu de données généré automatiquement capturant chaque étape d’un profil dans un parcours ; les événements d’étape d’exécution d’essai sont `inDryRun=true` et `dryRunID` *(spécifiques au produit)*
* **indicateur inDryRun** : champ booléen sur stepEvents `true` pour les exécutions d’exécution d’essai et `null` pour les parcours en direct ou de test *(spécifiques au produit)*

**Mécanismes de sécurisation :**
* Seuls les brouillons de parcours sans erreur peuvent être activés en mode Exécution d’essai
* Le démarrage d’une exécution d’essai nécessite l’autorisation **Publier des parcours** ; son arrêt nécessite l’autorisation **Gérer les parcours**
* Les parcours d’essai quittent automatiquement le mode Exécution d’essai et reviennent au statut Brouillon après 14 jours. Aucun contenu de parcours n’est perdu ; seule la session d’essai se termine.
* Les profils traités au cours d’une exécution d’essai sont comptabilisés dans les profils engageables et le quota de parcours en direct
* Les nœuds d’action de canal (e-mail, SMS, notification push) et les actions personnalisées ne sont pas exécutés lors de l’exécution d’essai
* Les actions de saut ne sont pas activées dans l’exécution d’essai.
* Les nœuds de réaction ne sont pas exécutés lors de l’exécution d’essai ; les profils se ferment correctement, avec des règles de priorité pour les branches unitaires et de réaction parallèles
* Les données de rapport ne sont disponibles que lorsque l’exécution d’essai est active ; une fois arrêtée, les données ne sont plus accessibles
* Les parcours en mode Test à blanc n’ont aucune incidence sur les règles métier.
* Pour les parcours utilisant une activité **Lecture d’audience** avec une heure planifiée (quotidienne, hebdomadaire ou mensuelle), l’exécution d’essai ne suit pas le planning de parcours configuré — le planning est ancré au moment où l’exécution d’essai a été activée (par exemple, parcours défini à 10 h, Exécution d’essai activée à 8 h → toutes les lectures pendant l’exécution d’essai s’exécutent à 8 h)

**Terminologie:**
* Nom canonique : Parcours Exécution d’essai — Acronyme : aucun — variantes : mode Exécution d’essai, mode de publication Exécution d’essai
* Synonymes : « Dry run » = « test de fumée » (officieusement)
* Ne les confondez pas : « Exécution d’essai » ≠ « Mode test » ≠ « Simulation » : l’exécution d’essai utilise des données de production réelles et comptabilise les profils engageables et le quota de parcours en direct ; le mode test utilise des profils de test AEP persistants dans un parcours brouillon ; la simulation utilise des utilisateurs simulés temporaires qui ne persistent pas dans AEP

**FAQ:**
* **Q : L’exécution d’essai envoie-t-elle réellement des e-mails ou des notifications push aux clients ?** — Non ; tous les nœuds d’action de canal et les actions personnalisées sont désactivés et ne sont pas exécutés pendant une exécution d’essai.
* **Q : Combien de temps dure une exécution d’essai avant qu’elle ne s’arrête automatiquement ?** — 14 jours, après quoi le parcours revient automatiquement au statut Brouillon.
* **Q : Comment exclure les données d’exécution d’essai de mes requêtes d’analyse de parcours ?** — Filtrez les événements d’étape où `inDryRun` est `true` ; incluez uniquement les événements où `inDryRun` est `null` ou `false`.
* **Q : Les profils sont-ils comptabilisés par rapport à des limites au cours d’une exécution d’essai ?** — Oui ; les profils sont comptabilisés dans les profils engageables et le parcours d’essai est comptabilisé dans le quota de parcours en direct.
* **Q : Puis-je activer les activités d’attente et les appels de source de données externe pendant une exécution d’essai ?** — Les deux sont désactivés par défaut, mais vous pouvez choisir de les activer ou de les désactiver lors de l’activation de l’Exécution d’essai.
* **Q : L’exécution d’essai respecte-t-elle le temps d’exécution planifié configuré dans un parcours Lecture d’audience ?** — Non. L’essai ancre le planning à l’heure d’activation, et non à l’heure de parcours configurée. Si le parcours est configuré pour s’exécuter à 10 heures du matin, mais que l’exécution d’essai est activée à 8 heures du matin, toutes les lectures planifiées pendant l’exécution d’essai s’exécutent à 8 heures du matin.

+++
