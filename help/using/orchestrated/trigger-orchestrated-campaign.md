---
solution: Journey Optimizer
product: journey optimizer
title: Déclencher une campagne orchestrée à l’aide d’un signal
description: Découvrez comment déclencher une campagne orchestrée à l’aide d’un signal dans  [!DNL Adobe Journey Optimizer].
feature: Campaigns
topic: Content Management
role: Developer
level: Intermediate
version: Campaign Orchestration
exl-id: d1fd072d-b143-4752-822f-23f98684ba80
source-git-commit: 6bae2fd7d52dd779d272a9a39ba4dfb7e852d4a8
workflow-type: tm+mt
source-wordcount: '880'
ht-degree: 1%

---

# Déclencher des campagnes orchestrées à l’aide d’un signal {#trigger-signal}

Vous pouvez déclencher une campagne orchestrée en lui envoyant un signal au lieu de l’exécuter selon un planning. Le signal est envoyé via un appel API à partir d’un système ou d’une application externe. Lors de l’utilisation d’un signal , vous pouvez transmettre des paramètres. Elles sont ensuite mises à disposition dans la campagne orchestrée sous la forme de variables d’événement dans le contexte d’exécution, à utiliser dans le ciblage, les conditions ou les expressions.

Pour obtenir la spécification REST complète du point d’entrée du déclencheur (chemins, en-têtes, corps, réponses et erreurs), consultez [API Trigger Orchestrated Campagnes](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} dans la documentation de l’API Adobe Journey Optimizer.

Processus de bout en bout pour déclencher une campagne orchestrée à l&#39;aide d&#39;un signal :

1. [Planifier la campagne à déclencher par un signal](#set-an-orchestrated-campaign-to-wait-for-a-signal-configure-signal)
1. [Ajouter des paramètres pour la payload du signal](#add-parameters-for-the-signal-payload-optional-parameters) (facultatif)
1. [Créer et tester la campagne](#build-and-test-the-campaign-build-and-test)
1. [Publier et déclencher la campagne](#publish-and-trigger-the-campaign-publish)

>[!NOTE]
>
>Pour déclencher une campagne orchestrée à l’aide d’un signal, vous devez disposer de l’autorisation **[!DNL Publish orchestrated campaigns]** (`orchestrated-campaign.publish`). Voir [ Autorisations intégrées ](../administration/ootb-permissions.md).

## Planifier la campagne à déclencher par un signal {#configure-signal}

Pour définir une campagne orchestrée pour démarrer sur un signal au lieu d’un planning, procédez comme suit :

1. Ouvrez la campagne orchestrée à déclencher à l’aide d’un signal.

1. Ouvrez la configuration du planning. [Découvrez comment planifier une campagne orchestrée](create-orchestrated-campaign.md#schedule).

1. Sélectionnez **[!UICONTROL Déclenché par un signal]** afin que la campagne attende un signal au lieu de s’exécuter selon un planning.

   ![Menu Horaire avec l’option Déclenché par un signal sélectionnée](assets/triggered-oc-scheduler.png){zoomable="yes"}

## Ajout de paramètres pour la payload du signal (facultatif) {#parameters}

Vous pouvez transmettre des paramètres dans le signal de déclenchement et les utiliser dans votre campagne dans le contexte d’exécution, par exemple dans le ciblage, les conditions ou les expressions. Définissez d’abord chaque paramètre dans les paramètres de planification, puis transmettez sa valeur lorsque vous appelez l’API de déclenchement.

1. Ouvrez le planificateur de campagne et sélectionnez **[!UICONTROL Ajouter un paramètre]**.

1. Définissez le nom et le type de données de chaque paramètre à envoyer dans la payload du signal. Vous pouvez également fournir des **Valeurs de test** qui seront utilisées lorsque vous déclencherez la campagne en mode test. [Découvrez comment tester une campagne déclenchée](#build-and-test).

   ![Ajoutez un paramètre pour définir les paramètres de payload du signal](assets/triggered-oc-parameter.png){zoomable="yes"}

>[!NOTE]
>
>Si vous transmettez un paramètre dans l’appel API qui n’a pas été défini dans le planificateur, l’appel API réussit toujours et le paramètre est propagé, et vous pouvez l’utiliser dans les expressions. Cependant, l’interface de campagne orchestrée ne vous aidera pas à l’utiliser ; par exemple, l’activité Test ne répertorie ni n’affiche les paramètres qui n’ont pas été définis dans le planificateur.

## Créer et tester la campagne {#build-and-test}

Créez votre campagne sur la zone de travail, puis testez-la éventuellement dans le brouillon en déclenchant le signal via l’API avant de la publier.

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

Une fois que vous avez [créé et testé la campagne](#build-and-test), publiez la campagne afin qu’elle puisse être déclenchée à partir de votre application.

1. Cliquez sur **[!UICONTROL Publier]** dans la zone de travail de la campagne. La campagne doit être publiée avant de pouvoir être déclenchée à partir d’un système externe. [En savoir plus sur le démarrage et le suivi de la campagne](start-monitor-campaigns.md#publish).

1. Ouvrez le planificateur de campagne, sélectionnez **[!UICONTROL Copier la requête d’API]** et choisissez le format (cURL ou requête HTTP).

   Les informations copiées incluent l’identifiant de campagne orchestré, le nom du sandbox, l’identifiant d’organisation et les paramètres si vous en avez ajouté.

   ![Copier la requête d’API dans la configuration du planning](assets/triggered-oc-copy.png)

1. Appelez l’API de déclenchement depuis votre système. Consultez [Déclencher l’API de campagnes orchestrées](https://developer.adobe.com/journey-optimizer-apis/references/oc-trigger){target="_blank"} pour la spécification des points d’entrée dynamiques.

   >[!IMPORTANT]
   >
   >Pour une campagne orchestrée en direct, un mécanisme de sécurisation de ralentissement applique un **intervalle minimum d’une heure** entre deux exécutions de déclencheur d’API. Si vous appelez à nouveau l’API avant l’expiration de cet intervalle, l’API renvoie une erreur **HTTP 429** (Trop de requêtes). Ce mécanisme de sécurisation n’est pas appliqué lorsque vous déclenchez un brouillon pour le tester.

   Si vous avez ajouté des paramètres à la payload du signal, les valeurs que vous transmettez dans l’appel API sont exposées en tant que variables d’événement de campagne lors de l’exécution de la campagne. Pour les examiner, ouvrez les journaux de campagne dans la barre d’outils de la zone de travail de campagne. Dans l’onglet **[!UICONTROL Tâches]**, identifiez la tâche correspondant au signal et cliquez sur l’icône en forme de crayon pour accéder aux variables d’événement associées. [Découvrez comment accéder aux journaux et aux tâches](start-monitor-campaigns.md#logs-tasks).

   ![Écran Logs et tâches où les variables d’événement de campagne sont disponibles](assets/trigger-events-variables.png){zoomable="yes"}
