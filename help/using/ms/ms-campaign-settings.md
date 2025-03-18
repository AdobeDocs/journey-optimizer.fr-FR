---
solution: Journey Optimizer
product: journey optimizer
title: Configurer des paramètres de campagne à étapes multiples
description: Découvrez comment configurer les paramètres de campagne à plusieurs étapes avec Adobe Journey Optimizer
hide: true
hidefromtoc: true
exl-id: a9bb3782-a4d1-43fe-ae2a-aef3f17ba588
source-git-commit: 323472ef9d6203cbbadc44ceb17ddcc7f6207323
workflow-type: tm+mt
source-wordcount: '1082'
ht-degree: 41%

---

# Configurer des paramètres de campagne à étapes multiples {#workflow-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_creation_properties"
>title="Propriétés des campagnes à étapes multiples"
>abstract="Dans cet écran, choisissez le modèle à utiliser pour créer la campagne à étapes multiples et indiquez un libellé. Développez la section **Options supplémentaires** pour configurer d’autres paramètres, tels que le nom interne de la campagne à étapes multiples, son dossier, son fuseau horaire et le groupe de supervision. Il est vivement recommandé de sélectionner un groupe de supervision afin d’alerter les opérateurs et opératrices en cas d’erreur."

Lors de la création d’une campagne à plusieurs étapes ou de l’orchestration d’activités de campagne à plusieurs étapes dans la zone de travail, vous pouvez accéder aux paramètres avancés de la campagne à plusieurs étapes. Par exemple, vous pouvez définir un fuseau horaire spécifique pour la campagne à plusieurs étapes, gérer le comportement de la campagne à plusieurs étapes en cas d’erreur ou gérer le délai après lequel l’historique de la campagne à plusieurs étapes doit être purgé.

Ces paramètres sont préconfigurés dans le modèle sélectionné lors de la création de la campagne à plusieurs étapes, mais peuvent être modifiés selon les besoins pour cette campagne spécifique à plusieurs étapes.

![](assets/workflow-settings-button.png){zoomable="yes"}{width="70%" align="left"}

## Propriétés des campagnes à étapes multiples {#properties}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_properties"
>title="Propriétés des campagnes à étapes multiples"
>abstract="Cette section fournit des propriétés de campagnes à étapes multiples génériques, lesquelles sont également accessibles lors de la création de la campagne à étapes multiples. Vous pouvez choisir le modèle à utiliser pour créer la campagne à étapes multiples et indiquer un libellé. Développez la section Options supplémentaires pour configurer des paramètres spécifiques, tels que le dossier de stockage de la campagne à étapes multiples ou le fuseau horaire."

La section **[!UICONTROL Propriétés]** fournit des paramètres génériques qui peuvent être configurés lors de la création d’une campagne à plusieurs étapes. Pour accéder aux propriétés d’une campagne existante à plusieurs étapes, cliquez sur le bouton **[!UICONTROL Paramètres]** disponible dans la barre d’actions située au-dessus de la zone de travail de la campagne à plusieurs étapes.


![](assets/workflow-settings.png){zoomable="yes"}{width="70%" align="left"}


Ces propriétés sont les suivantes :

* Le **[!UICONTROL Libellé]** de la campagne à plusieurs étapes qui s’affiche dans la liste.
* Le **[!UICONTROL Nom interne]** de la campagne à plusieurs étapes.
* Le **[!UICONTROL Dossier]** dans lequel la campagne à plusieurs étapes doit être enregistrée.
* La valeur par défaut **[!UICONTROL Fuseau horaire]** à utiliser dans toutes les activités de la campagne à plusieurs étapes. Par défaut, le fuseau horaire de la campagne à plusieurs étapes est celui défini pour l’opérateur Campaign actuel.
Les valeurs possibles sont les suivantes :
   * **Fuseau horaire du serveur** pour utiliser le fuseau horaire de votre organisation Adobe Experience Platform
   * **Fuseau horaire de l’opérateur** pour utiliser le fuseau horaire de l’opérateur qui exécute la campagne à plusieurs étapes
   * **Fuseau horaire de la base de données** pour utiliser le fuseau horaire du serveur de base de données.
   * Un fuseau horaire spécifique.
* Lorsqu’une campagne à plusieurs étapes échoue, les opérateurs et opératrices appartenant au groupe d’opérateurs sélectionné dans le champ **[!UICONTROL Superviseur(s)]** sont avertis par e-mail.
* Vous pouvez également saisir une **[!UICONTROL Description]** de votre campagne à plusieurs étapes.

## Paramètres de segmentation  {#segmentation-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_segmentation"
>title="Paramètres de segmentation"
>abstract="Cette section vous permet de sélectionner la dimension de ciblage pour cibler les profils dans la campagne à étapes multiples et de conserver ou non les résultats du workflow entre deux exécutions. Cette option ne doit être utilisée qu’à des fins de test. Elle ne doit en aucun cas être activée dans une campagne de production à étapes multiples."

* **[!UICONTROL Dimension de ciblage]** : sélectionnez la dimension de ciblage à utiliser pour cibler les profils (destinataires, bénéficiaires d’un contrat, opérateur ou opératrice, abonnées et abonnés, etc.).

* **[!UICONTROL Conserver le résultat des populations intermédiaires entre deux exécutions]** : par défaut, seules les tables de travail de la dernière exécution de la campagne à plusieurs étapes sont conservées. Les tables de travail des exécutions précédentes sont purgées par une campagne technique à plusieurs étapes qui s’exécute quotidiennement.

  Si cette option est activée, les tables de travail sont conservées même après l’exécution de la campagne à plusieurs étapes. Vous pouvez l’utiliser à des fins de test. N’utilisez donc cette option **que** dans les environnements de développement ou d’évaluation. Elle ne doit jamais être cochée dans une campagne en production à plusieurs étapes.

## Paramètres d’exécution  {#exec-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_execution"
>title="Paramètres d’exécution"
>abstract="Dans cette section, vous pouvez définir les paramètres relatifs à l’exécution du workflow, comme le nombre de jours pendant lesquels l’historique de la campagne à étapes multiples est conservé."

* **[!UICONTROL Jours d’historique]** : indique le nombre de jours après lesquels l’historique doit être purgé. L’historique contient des éléments liés à la campagne à plusieurs étapes : logs, tâches, événements (objets techniques liés à l’opération de campagne à plusieurs étapes). La valeur par défaut est de 30 jours pour les modèles de campagne prêts à l’emploi à plusieurs étapes. La purge de l’historique est effectuée par la campagne technique à plusieurs étapes de nettoyage de la base de données, qui est exécutée par défaut tous les jours

  >[!IMPORTANT]
  >
  >Si le champ **[!UICONTROL Jours d’historique]** n’est pas renseigné, la valeur prise en compte est « 1 », ce qui signifie que l’historique sera purgé après 1 jour.

* **[!UICONTROL Affinité par défaut]** : si votre installation comprend plusieurs serveurs de campagne à plusieurs étapes, utilisez ce champ pour spécifier le serveur sur lequel la campagne à plusieurs étapes sera exécutée. Cela force l’exécution de cette campagne en plusieurs étapes sur un serveur particulier. Vous pouvez choisir n’importe quel nom d’affinité existant, mais veillez à ne pas utiliser d’espaces ni de signes de ponctuation. Si vous utilisez des serveurs différents, spécifiez aussi des noms différents, séparés par des virgules.

  >[!IMPORTANT]
  >
  >Si la valeur définie dans ce champ n’existe sur aucun serveur, la campagne à plusieurs étapes reste en attente.


* **[!UICONTROL Enregistrer les requêtes SQL dans le journal]** : cochez cette option pour enregistrer les requêtes SQL de la campagne à plusieurs étapes du workflow maintenant dans les journaux. Cette fonctionnalité est réservée aux utilisateurs et utilisatrices avancés. Elle s’applique aux campagnes à plusieurs étapes qui contiennent des activités de ciblage comme **[!UICONTROL Créer une audience]**. Lorsque cette option est activée, les requêtes SQL envoyées à la base de données lors de l’exécution de la campagne à plusieurs étapes sont affichées dans les journaux de la campagne à plusieurs étapes, ce qui vous permet de les analyser afin d’optimiser les requêtes ou de diagnostiquer les problèmes.

## Paramètres de gestion des erreurs  {#error-settings}

>[!CONTEXTUALHELP]
>id="ajo_workflow_settings_error"
>title="Paramètres de gestion des erreurs"
>abstract="Dans cette section, vous pouvez définir la façon dont la campagne à étapes multiples doit gérer les erreurs lors de son exécution. Vous pouvez choisir de suspendre le processus, d’ignorer un certain nombre d’erreurs ou d’arrêter l’exécution de la campagne à étapes multiples."

* **[!UICONTROL Gestion des erreurs]** : ce champ vous permet de définir les actions à effectuer si une tâche de campagne multi-étapes comporte des erreurs. Trois choix s’offrent à vous :

   * **[!UICONTROL Suspendre le processus]** : la campagne à plusieurs étapes est automatiquement mise en pause et adopte le statut **[!UICONTROL Échec]**. Une fois le problème résolu, reprenez la campagne à plusieurs étapes à l’aide des boutons **[!UICONTROL Reprendre]**.
   * **[!UICONTROL Ignorer]** : le statut de la tâche qui a déclenché l’erreur passe à **[!UICONTROL Échec]**, mais la campagne à plusieurs étapes conserve le statut **[!UICONTROL Démarré]**. <!-- TO ADD ONCE SCHEUDLER IS AVAILABLE This configuration is relevant for recurring tasks: if the branch includes a scheduler, it will start normally next time the workflow is executed.-->
   * **[!UICONTROL Abandonner le processus]** : la campagne à plusieurs étapes est automatiquement arrêtée et son statut passe à **[!UICONTROL En échec]**. Une fois le problème résolu, redémarrez la campagne à plusieurs étapes à l’aide des boutons **[!UICONTROL Démarrer]**.

* **[!UICONTROL Erreurs consécutives]** : ce champ est disponible lorsque la valeur **[!UICONTROL Ignorer]** est sélectionnée dans le champ **[!UICONTROL En cas d’erreur]**. Vous pouvez indiquer le nombre d’erreurs qui peuvent être ignorées avant l’arrêt du processus. Une fois ce nombre atteint, le statut de la campagne à plusieurs étapes devient **[!UICONTROL Échec]**. Si la valeur de ce champ est 0, la campagne à plusieurs étapes ne sera jamais arrêtée, quel que soit le nombre d’erreurs.

## Script d’initialisation {#initialization-script}

Ce **script d’initialisation** vous permet d’initialiser des variables ou de modifier des propriétés d’activité. Cliquez sur le bouton **Modifier le code** et saisissez l’extrait de code à exécuter. Le script est appelé lorsque la campagne à plusieurs étapes s’exécute. Consultez la section relative aux [variables d’événement](event-variables.md).
