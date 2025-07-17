---
solution: Journey Optimizer
product: journey optimizer
title: Ajouter une activité de canal dans une campagne à plusieurs étapes
description: Découvrez comment ajouter une activité de canal dans une campagne à plusieurs étapes
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: 1aa4f3e24a4cb7594232c0b25da8c9fd2e62c1de
workflow-type: tm+mt
source-wordcount: '992'
ht-degree: 36%

---

# Activités de canal {#channel}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="Activité e-mail"
>abstract="L’activité E-mail permet d’envoyer des e-mails dans votre campagne orchestrée, pour des messages ponctuels et récurrents. Elle permet d’automatiser le processus d’envoi d’e-mails à une cible calculée dans la même campagne orchestrée. Vous pouvez combiner des activités de canal dans une zone de travail de campagne à plusieurs étapes, afin de créer des campagnes cross-canal pouvant déclencher des actions en fonction du comportement de la clientèle et des données."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="Activité SMS"
>abstract="L’activité SMS permet d’envoyer des SMS dans votre campagne orchestrée, pour les messages ponctuels et récurrents. Elle permet d’automatiser le processus d’envoi de SMS à une cible calculée dans la même campagne orchestrée. Vous pouvez combiner des activités de canal dans la zone de travail de campagne à plusieurs étapes, afin de créer des campagnes cross-canal pouvant déclencher des actions en fonction du comportement de la clientèle et des données."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push"
>title="Activité Notification push"
>abstract="L’activité Notification push permet d’envoyer des notifications push dans le cadre de votre campagne orchestrée. Elle permet la diffusion de campagnes orchestrées ponctuelles et récurrentes, en automatisant l’envoi de notifications push à une cible prédéfinie dans la même campagne orchestrée. Vous pouvez combiner des activités de canal dans la zone de travail de campagne, afin de créer des campagnes cross-canal pouvant déclencher des actions en fonction du comportement de la clientèle et des données."

<!--
UNUSED IDs in BJ

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="Push iOS activity"
>abstract="The Push iOS activity let you send iOS Push notifications as part of your orchestrated campaign. It enables the delivery of both one-time and recurring orchestrated campaigns, automating the sending iOS Push notifications to a predefined target within the same workflow. You can combine channel activities into the campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="Push Android activity"
>abstract="The Push Android activity ket you send Android Push notifications as part of your orchestrated campaign. It enables the delivery of both one-time and recurring messages, automating the sending Android Push notifications to a predefined target within the same orchestrated campaign. You can combine channel activities into the orchestrated campaign canvas to create cross-channel campaigns that can trigger actions based on customer behavior and data."

-->

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="Activité Courrier"
>abstract="L’activité Courrier facilite l’envoi de courrier depuis votre campagne orchestrée pour les messages ponctuels et récurrents. Elle permet d’automatiser le processus de génération du fichier d’extraction requis par les fournisseurs de services postaux. Vous pouvez combiner des activités de canal dans la zone de travail de campagne orchestrée, afin de créer des campagnes cross-canal pouvant déclencher des actions en fonction du comportement de la clientèle et des données."


+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>Création et gestion de schémas et de jeux de données relationnels :</br> <ul><li>[Schéma manuel](manual-schema.md)</li><li>[Schéma de chargement de fichier](file-upload-schema.md)</li><li>[ Ingérer des données ](ingest-data.md)</li></ul><br/><br/>[Accéder aux campagnes orchestrées et les gérer](../access-manage-orchestrated-campaigns.md) | [Étapes clés de création d’une campagne orchestrée](../gs-campaign-creation.md)<br/><br/>[Créez et planifiez la campagne](../create-orchestrated-campaign.md)<br/><br/>[Orchestrez les activités](../orchestrate-activities.md)<br/><br/>[Lancez et surveillez la campagne](../start-monitor-campaigns.md)<br/><br/>[Reporting](../reporting-campaigns.md) | [Utiliser le créateur de règles](../orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](../build-query.md)<br/><br/>[Modifier les expressions](../edit-expressions.md)<br/><br/>[Reciblage](../retarget.md) | [Prise en main des activités](about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](and-join.md) - [Créer une audience](build-audience.md) - [Modifier la dimension](change-dimension.md) - <b>[Activités de canal](channels.md)</b> - [Combine](combine.md) - [Deduplication](deduplication.md) - [Enrichissement](enrichment.md) - [Fork](fork.md) - [Reconciliation](reconciliation.md) - [Enregistrer l’audience](save-audience.md) - [Split](split.md) - [Wait](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

Le contenu de cette page n’est pas définitif et peut être modifié.

>[!ENDSHADEBOX]

[!DNL Adobe Journey Optimizer] vous permet d’automatiser et d’exécuter des campagnes marketing sur plusieurs canaux (e-mail, SMS et notifications push). Vous pouvez combiner ces activités de canal dans la zone de travail de campagne afin de créer des campagnes orchestrées cross-canal pouvant déclencher des actions en fonction du comportement du client et des données.

Par exemple :
* Envoyez une série de bienvenue par e-mail, SMS et notification push.
* Envoyez un e-mail de relance après l’achat.
* Envoyez des salutations d’anniversaire personnalisées par SMS.

Grâce aux activités de canal, vous pouvez créer des campagnes personnalisées et complètes qui impliquent la clientèle sur plusieurs touchpoints et génèrent des conversions.

>[!PREREQUISITES]
>
>Avant d’ajouter une activité de canal, définissez l’audience cible à l’aide d’une [ Activité Créer une audience ](build-audience.md).

## Ajoutez une activité de canal et définissez ses propriétés {#add}

1. Ajoutez une activité de canal dans la zone de travail. Les activités de canal disponibles sont **[!UICONTROL E-mail]**, **[!UICONTROL SMS]** et **[!UICONTROL Push]**.

   ![image montrant la zone de travail avec les activités disponibles](../assets/channel-add.png)

1. Sélectionnez l’activité et cliquez sur **[!UICONTROL Modifier l’e-mail]**, **[!UICONTROL Modifier le SMS]** ou **[!UICONTROL Modifier la notification push]** selon le canal choisi.

   ![image illustrant la zone de travail avec une activité E-mail ](../assets/channel-edit.png)

1. Dans l’onglet **[!UICONTROL Propriétés]** , saisissez une description, puis passez à l’onglet **[!UICONTROL Actions]** pour configurer l’activité.

## Configurer la configuration et les paramètres du canal {#configuration}

Utilisez l’onglet **[!UICONTROL Actions]** pour sélectionner une configuration de canal pour votre message et configurer des paramètres supplémentaires tels que le suivi, l’expérience de contenu ou le contenu multilingue.

1. Sélectionnez une configuration de canal.

   Celle-ci est définie par une [équipe d’administration système](../../start/path/administrator.md). Elle contient tous les paramètres techniques relatifs à l’envoi du message, tels que les paramètres d’en-tête, le sous-domaine, les applications mobiles, etc. [Découvrez comment configurer des configurations de canal](../../configuration/channel-surfaces.md).

   ![image illustrant la section Actions](../assets/channel-actions.png)

1. Suivre l’engagement (pour les e-mails et les SMS).

   Utilisez la section **[!UICONTROL Tracking des actions]** pour suivre la réaction des destinataires à vos diffusions e-mail ou SMS. Les résultats du suivi sont accessibles dans le rapport de la campagne, une fois celle-ci exécutée. [En savoir plus sur les rapports de campagne](../../reports/campaign-global-report-cja.md)

1. Activez le mode de diffusion rapide (pour les notifications push).

   Le mode de diffusion rapide est un module complémentaire [!DNL Journey Optimizer] qui permet d’envoyer très rapidement des messages push en grande quantité dans le cadre d’une campagne. La diffusion rapide est utilisée lorsque le retard de diffusion des messages est critique pour l’entreprise, lorsque vous souhaitez envoyer une alerte push urgente sur les téléphones mobiles, par exemple des nouvelles importantes aux utilisateurs qui ont installé votre application de canal d’actualités. Pour plus d’informations sur les performances lors de l’utilisation du mode de diffusion rapide, reportez-vous à la section [Description du produit Adobe Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html).

1. Créez une expérience de contenu.

   Utilisez la section **[!UICONTROL Expérience de contenu]** pour définir plusieurs traitements de diffusion afin de mesurer celui qui fonctionne le mieux pour votre audience cible. Cliquez sur le bouton **[!UICONTROL Créer une expérience]** puis suivez les étapes détaillées dans cette section : [Créer une expérience de contenu](../../content-management/content-experiment.md).

1. Ajoutez du contenu multilingue.

   Utilisez la section **[!UICONTROL Langues]** pour créer du contenu dans plusieurs langues au sein de votre campagne. Pour ce faire, cliquez sur le bouton **[!UICONTROL Ajouter des langues]** et sélectionnez l’option **[!UICONTROL Paramètres de langue]** souhaitée. Vous trouverez des informations détaillées sur la configuration et l’utilisation des fonctionnalités multilingues dans cette section : [Prise en main du contenu multilingue](../../content-management/multilingual-gs.md)

   ![image illustrant la section Expérience de contenu](../assets/channel-experiment.png)

Une fois votre activité de canal configurée, sélectionnez l’onglet **[!UICONTROL Contenu]** pour définir son contenu.

## Définir le contenu {#content}

Passez à l’onglet **[!UICONTROL Contenu]** pour créer votre message. Les étapes du processus varient en fonction du canal sélectionné. Découvrez les étapes détaillées pour créer le contenu de votre message dans les pages suivantes.

<table style="table-layout:fixed"><tr style="border: 0; text-align: center;" >
<td><a href="../../email/create-email.md"><img alt="E-mail" src="../../channels/assets/do-not-localize/email.png"></a><br/><a href="../../email/create-email.md"><strong>Création d’un e-mail</strong></a></td>
<td><a href="../../sms/create-sms.md"><img alt="SMS" src="../../channels/assets/do-not-localize/sms.png"></a><br/><a href="../../sms/create-sms.md"><strong>Créer un SMS</strong></a></td>
<td><a href="../../push/create-push.md"><img alt="Notification push" src="../../channels/assets/do-not-localize/push.png"></a><a href="../../push/create-push.md"><strong>Créer une notification push</strong></a></td>
</tr></table>

Une fois le contenu créé, cliquez sur le bouton **[!UICONTROL Simuler du contenu]** pour prévisualiser et tester votre contenu avec des profils de test ou des exemples de données d’entrée chargés à partir d’un fichier CSV/JSON, ou ajoutés manuellement. [En savoir plus](../../content-management/preview-test.md)

![image illustrant le bouton Simuler du contenu](../assets/channel-simulate.png)

## Étapes suivantes {#next}

Lorsque le contenu du message est prêt, revenez à votre campagne orchestrée à l’aide de la flèche **[!UICONTROL Précédent]**. Vous pouvez ensuite terminer l’orchestration des activités dans la zone de travail et publier la campagne pour commencer l’envoi des messages. [Découvrez comment démarrer et surveiller des campagnes orchestrées](../start-monitor-campaigns.md)

![image illustrant le bouton Précédent](../assets/channel-back.png)

<!--
## Examples {#cross-channel-workflow-sample}

Here is a cross-channel orchestrated campaign example with a segmentation and two deliveries. The orchestrated campaign targets all customers who live in Paris and who are interested in coffee machines. Among this population, an email is sent to the regular customers and an SMS is sent to the VIP clients.

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

<!--You can also create a recurring orchestrated campaign to send a personalized SMS every first day of the month at 8 PM to all customers living in Paris.

![](../assets/workflow-channel-example2.png)-->

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
