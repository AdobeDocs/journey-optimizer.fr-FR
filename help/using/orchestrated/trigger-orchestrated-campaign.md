---
solution: Journey Optimizer
product: journey optimizer
title: Déclencher une campagne orchestrée à l’aide d’un signal
description: Découvrez comment déclencher une campagne orchestrée avec un signal de l’API REST ou de l’activité Fin d’une autre campagne, et comment transmettre des paramètres à la campagne.
feature: Campaigns
topic: Content Management
role: Developer
level: Intermediate
version: Campaign Orchestration
exl-id: d1fd072d-b143-4752-822f-23f98684ba80
feature_v2: 
subfeature_v2:
  - id: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
source-git-commit: 18f6b23dbbe53e486e5af76ef7cc61fa1784475d
workflow-type: tm+mt
source-wordcount: 1429
ht-degree: 1%

---

# Déclencher des campagnes orchestrées à l’aide d’un signal {#trigger-signal}

Vous pouvez démarrer une campagne orchestrée avec un signal au lieu d’un planning fixe. Lorsque la campagne reçoit le signal, elle s’exécute et vous pouvez transmettre des paramètres dans la payload. Ils deviennent disponibles en tant que variables pour le ciblage, les conditions ou les expressions.

Le signal peut provenir de l’une des sources suivantes :

* API REST — Votre application ou intégration appelle le point d’entrée de déclenchement (voir [Publication et déclenchement de la campagne](#publish) et la [référence de l’API](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"}).
* Une autre campagne orchestrée : l’activité **[!UICONTROL Fin]** d’une campagne en amont envoie le même type de signal lorsqu’une branche se termine. [Découvrez comment configurer l’activité Fin](#signal-end).

Cette page explique comment configurer la campagne qui reçoit le signal (planning, paramètres, test, publication), puis comment le déclencher à partir de l’API ou d’une activité **[!UICONTROL Fin]**. Une fois les variables disponibles, pour plus d’informations sur leur utilisation dans les règles et les conditions **[!UICONTROL Test]**, consultez la section [Utiliser des variables dans des campagnes orchestrées](variables-orchestrated-campaigns.md).

Pour obtenir la spécification REST complète du point d’entrée du déclencheur (chemins, en-têtes, corps, réponses et erreurs), consultez [API Trigger Orchestrated Campagnes](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} dans la documentation de l’API Adobe Journey Optimizer.

Processus de bout en bout pour déclencher une campagne orchestrée à l&#39;aide d&#39;un signal :

1. [Planifier la campagne à déclencher par un signal](#configure-signal)
1. [Ajouter des paramètres pour la payload du signal](#parameters) (facultatif)
1. [Créer et tester la campagne](#build-and-test)
1. [Publier et déclencher la campagne](#publish)

>[!NOTE]
>
>Pour déclencher une campagne orchestrée à l’aide d’un signal, vous devez disposer de l’autorisation **[!DNL Publish orchestrated campaigns]** (`orchestrated-campaign.publish`). Voir [&#x200B; Autorisations intégrées &#x200B;](../administration/ootb-permissions.md).

## Planifier la campagne à déclencher par un signal {#configure-signal}

Pour définir une campagne orchestrée pour démarrer sur un signal au lieu d’un planning, procédez comme suit :

1. Ouvrez la campagne orchestrée à déclencher à l’aide d’un signal.

1. Ouvrez la configuration du planning. [Découvrez comment planifier une campagne orchestrée](create-orchestrated-campaign.md#schedule).

1. Sélectionnez **[!UICONTROL Déclenché par un signal]** afin que la campagne attende un signal au lieu de s’exécuter selon un planning.

   ![Menu Horaire avec l’option Déclenché par un signal sélectionnée](assets/triggered-oc-scheduler.png){zoomable="yes"}

## Ajout de paramètres pour la payload du signal (facultatif) {#parameters}

Vous pouvez transmettre des paramètres dans le signal de déclenchement et les utiliser dans votre campagne dans le contexte d’exécution, par exemple dans le ciblage, les conditions ou les expressions. Définissez d’abord chaque paramètre dans les paramètres de planning, puis transmettez sa valeur lorsque vous appelez l’API de déclenchement ou lorsque vous mappez des paramètres à partir de l’activité **[!UICONTROL Fin]** d’une campagne en amont ([voir ci-dessous](#signal-end)).

1. Ouvrez le planificateur de campagne et sélectionnez **[!UICONTROL Ajouter un paramètre]**.

1. Définissez le nom et le type de données de chaque paramètre à envoyer dans la payload du signal. Vous pouvez également fournir des **Valeurs de test** qui seront utilisées lorsque vous déclencherez la campagne en mode test. [Découvrez comment tester une campagne déclenchée](#build-and-test).

   ![Ajoutez un paramètre pour définir les paramètres de payload du signal](assets/triggered-oc-parameter.png){zoomable="yes"}

>[!NOTE]
>
>Pour les campagnes orchestrées déclenchées par l’API REST, si vous transmettez un paramètre dans l’appel API qui n’a pas été défini dans le planificateur, l’appel API réussit toujours et le paramètre est propagé, et vous pouvez l’utiliser dans les expressions. Toutefois, l’interface de campagne orchestrée ne vous aidera pas à l’utiliser ; par exemple, l’activité Test ne répertorie ni n’affiche les paramètres qui n’ont pas été définis dans le planificateur.

## Tester la campagne {#build-and-test}

Créez votre campagne sur la zone de travail, puis testez-la dans **[!UICONTROL Version préliminaire]** avant de la publier en envoyant le signal via l’API REST.

* **Campagnes orchestrées déclenchées par l’API REST** — Suivez les étapes ci-dessous pour exécuter la campagne en tant que brouillon et valider le ciblage, les paramètres et la logique de diffusion avant la publication.

* **Campagnes orchestrées déclenchées par une activité Fin** — Vous ne pouvez pas exécuter la chaîne complète de bout en bout dans le brouillon : une fois la campagne en amont publiée, son activité **[!UICONTROL Fin]** ne fait que lancer une campagne en aval publiée. Pour tester le côté en aval avant la publication des deux campagnes, conservez cette campagne dans **[!UICONTROL Brouillon]**, définissez **[!UICONTROL Tester les valeurs]** pour vos paramètres de signal dans le planificateur ([Ajouter des paramètres pour la payload du signal](#parameters)), puis suivez les étapes d’API ci-dessous. L’appel d’API de déclenchement utilise la même payload qu’une activité **[!UICONTROL Fin]** à l’exécution. Vous pouvez ainsi valider le routage des paramètres et la logique de zone de travail avant de publier la campagne en aval et de configurer l’activité **[!UICONTROL Fin]** en amont ([Déclencheur à partir de l’activité Fin d’une autre campagne](#signal-end)).

1. Ajoutez et connectez les activités (audience, ciblage, diffusions) sur la zone de travail. [Découvrez comment orchestrer des activités de campagne](orchestrate-activities.md).

1. Si vous avez défini des paramètres dans le signal, vous pouvez les connecter à votre logique de zone de travail (par exemple, dans des conditions ou un ciblage). Dans cet exemple, le paramètre « channel » est utilisé comme condition dans une activité **[!UICONTROL Test]**.

   ![Paramètre de canal utilisé comme condition dans l’activité Test](assets/triggered-oc-use-parameters.png)

   Pour utiliser un paramètre de signal dans l’éditeur d’expression (par exemple, pour créer une requête dans une activité **[!UICONTROL Créer une audience]**), saisissez `$(vars/@<parameterName>)` dans le champ d’expression. Remplacez `<parameterName>` par le nom du paramètre défini dans le planificateur, par exemple `$(vars/@channel)`. [Découvrez comment utiliser l’éditeur d’expression](edit-expressions.md).

1. Ouvrez le planificateur de campagne, sélectionnez **[!UICONTROL Copier la requête d’API]** et choisissez le format (cURL ou requête HTTP).

   Les informations copiées incluent l’identifiant de campagne orchestré, le nom du sandbox, l’identifiant d’organisation et les valeurs de test pour vos paramètres si vous en avez ajouté.

   ![Option Copier la requête API dans la configuration du planning](assets/triggered-oc-copy.png)

   +++Exemple de requête cURL avec un paramètre et une valeur de test

   ```bash
   POST https://platform.adobe.io/ajo/campaign-orchestration/orchestratedCampaigns/1c7529c7-7a8c-491a-a2c6-3d8131d2e17d/trigger
   
   Headers:
   Authorization: Bearer ## Access token ##
   Content-Type: application/json
   x-api-key: ## Provide API Key here ##
   x-api-version: 1
   x-gw-ims-org-id: 123456ABCDEFG@LumaOrg
   x-sandbox-name: prod
   
   Body:
   {
   "variables": {
      "channel": "sms"
   }
   }
   ```

   +++

1. Cliquez sur **[!UICONTROL Démarrer]** pour démarrer la campagne.

1. Envoyez l’appel API déclencheur à l’aide de l’exemple de requête que vous avez copié à partir du planificateur. Voir [Déclencher l’API de campagnes orchestrées](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} pour les détails de la requête et de la réponse.

Lorsque les résultats des tests vous conviennent, [publiez la campagne](#publish).

## Publier et déclencher la campagne {#publish}

Une fois que vous avez [testé la campagne](#build-and-test), publiez-la afin qu’elle puisse recevoir un signal de votre application ou de l’activité **[!UICONTROL Fin]** d’une autre campagne. [En savoir plus sur le démarrage et le suivi de la campagne](start-monitor-campaigns.md#publish).

Vous pouvez ensuite le déclencher à partir de l’API REST ou de l’activité **[!UICONTROL Fin]** d’une autre campagne. Voir les sections ci-dessous.

### Envoyer le signal avec l’API REST {#publish-api}

Après la publication, procédez comme suit chaque fois que vous déclenchez la campagne à partir de votre propre application :

1. Ouvrez le planificateur de campagne, sélectionnez **[!UICONTROL Copier la requête d’API]** et choisissez le format (cURL ou requête HTTP).

   Les informations copiées incluent l’identifiant de campagne orchestré, le nom du sandbox, l’identifiant d’organisation et les paramètres si vous en avez ajouté.

   ![Copier la requête d’API dans la configuration du planning](assets/triggered-oc-copy.png)

1. Appelez l’API de déclenchement depuis votre système. Consultez [Déclencher l’API de campagnes orchestrées](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} pour la spécification des points d’entrée dynamiques.

   >[!IMPORTANT]
   >
   >Pour une campagne orchestrée en direct, un mécanisme de sécurisation de ralentissement applique un intervalle minimum d’une heure entre deux exécutions de déclencheur d’API. Si vous appelez à nouveau l’API avant l’expiration de cet intervalle, l’API renvoie un HTTP 429 (Too many requests). Ce mécanisme de sécurisation n’est pas appliqué lorsque vous déclenchez un brouillon pour le tester.

   Si vous avez ajouté des paramètres à la payload du signal, les valeurs que vous transmettez dans l’appel API sont exposées en tant que variables d’événement de campagne lors de l’exécution de la campagne. Pour les examiner, ouvrez les journaux de campagne dans la barre d’outils de la zone de travail de campagne. Dans l’onglet **[!UICONTROL Tâches]**, identifiez la tâche correspondant au signal et cliquez sur l’icône en forme de crayon pour accéder aux variables d’événement associées. [Découvrez comment accéder aux journaux et aux tâches](start-monitor-campaigns.md#logs-tasks).

   ![Écran Logs et tâches où les variables d’événement de campagne sont disponibles](assets/trigger-events-variables.png){zoomable="yes"}

### Envoyer le signal à partir de l’activité Fin d’une autre campagne {#signal-end}

Utilisez ce chemin d’accès pour chaîner les campagnes orchestrées : lorsque la campagne en amont termine une branche, l’activité **[!UICONTROL Fin]** envoie un signal à une campagne en aval qui est déjà définie sur **[!UICONTROL Déclenchée par un signal]**. Vous pouvez ainsi réutiliser des campagnes plus petites et transmettre une payload différente de chaque appelant.

>[!NOTE]
>
>* Vous pouvez utiliser plusieurs activités **[!UICONTROL de fin]** sur la même zone de travail et configurer chacune d’elles pour déclencher une campagne en aval différente.
>* Plusieurs campagnes peuvent déclencher la même campagne en aval. Chaque appel peut envoyer une payload différente.

Procédez comme suit sur la campagne qui doit s’exécuter en premier :

1. Ouvrez la campagne orchestrée qui doit envoyer le signal et sélectionnez une activité **[!UICONTROL Fin]** à l’extrémité de la branche qui doit se terminer avant le début de la campagne en aval.
1. Dans la section **[!UICONTROL Signal externe]**, sélectionnez la campagne en aval à déclencher.

1. Vous pouvez éventuellement ajouter des paramètres : utilisez les mêmes noms que dans le planning de la campagne en aval et définissez chaque valeur.

   ![](assets/end-signal.png)

1. Pour tester la campagne en aval en mode brouillon avant de la publier, suivez les étapes de la section [tester la campagne](#build-and-test) pour la déclencher en mode brouillon avec l’API REST.

La campagne en aval doit être publiée avant que la campagne en amont ne s’exécute suffisamment pour atteindre l’activité **[!UICONTROL Fin]** qui la déclenche. Si le signal est envoyé alors que la campagne cible n’est pas publiée, l’exécution échoue. Publiez la campagne en aval, puis reprenez ou redémarrez-la si nécessaire.
