---
solution: Journey Optimizer
product: journey optimizer
title: Ajouter une activité de canal dans une campagne à plusieurs étapes
description: Découvrez comment ajouter une activité de canal dans une campagne à plusieurs étapes
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: cfb09467809a69516c34d52be3f41e7a1abdb7c3
workflow-type: tm+mt
source-wordcount: '985'
ht-degree: 30%

---

# Activités de canal {#channel}

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](../gs-orchestrated-campaigns.md)<br/><br/>[Étapes de configuration](../configuration-steps.md)<br/><br/>[Étapes clés de la création de campagnes orchestrées](../gs-campaign-creation.md) | [Créer une campagne orchestrée](../create-orchestrated-campaign.md)<br/><br/>[Orchestrer les activités](../orchestrate-activities.md)<br/><br/><br/>[Démarrer et surveiller la campagne](../start-monitor-campaigns.md)<br/><br/>[le reporting](../reporting-campaigns.md) | [Utiliser la requête Modeler](../orchestrated-rule-builder.md)<br/><br/>[créer votre première requête](../build-query.md)<br/><br/>[modifier des expressions](../edit-expressions.md) | [Prise en main des activités](about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](and-join.md) - [Créer une audience](build-audience.md) - [Modifier la dimension](change-dimension.md) - **[Activités de canal](channels.md)** - [Combine](combine.md) - [Deduplication](deduplication.md) - [Enrichissement](enrichment.md) - [Fork](fork.md) - [Reconciliation](reconciliation.md) - [Split](split.md) - [Wait](wait.md) |

{style="table-layout:fixed"}

+++

<br/>

[!DNL Adobe Journey Optimizer] vous permet d’automatiser et d’exécuter des campagnes marketing sur plusieurs canaux. Vous pouvez combiner des activités de canal dans la zone de travail de campagne orchestrée afin de créer des campagnes orchestrées cross-canal pouvant déclencher des actions en fonction du comportement du client et des données.

Vous pouvez par exemple créer une campagne par e-mail de bienvenue qui comprend une série de messages sur différents canaux, tels que les e-mails, les SMS et les notifications push. Vous pouvez également envoyer un e-mail de relance une fois qu’un client ou une cliente a effectué un achat, ou envoyer un message d’anniversaire personnalisé par SMS.

Grâce aux activités de canal, vous pouvez créer des campagnes personnalisées et complètes qui impliquent les clients et clientes sur plusieurs points de contact et génèrent des conversions. Les canaux pris en charge sont les e-mails, SMS et les notifications push.

## Conditions préalables {#channel-activity-prereq}

Commencez à créer votre campagne orchestrée avec les activités pertinentes :

* Avant d’insérer une activité de canal, vous devez définir l’audience. L’audience est la cible principale de votre diffusion : il s’agit des profils qui reçoivent les messages. [Découvrez comment utiliser l’activité Créer une audience](build-audience.md)

* Pour envoyer une diffusion récurrente, lancez votre campagne orchestrée avec une activité **[!UICONTROL Planificateur]**. Vous pouvez également utiliser une activité **[!UICONTROL Planificateur]** pour les diffusions ponctuelles afin de définir la date de contact de celles-ci. Cette date de contact peut également être définie dans les paramètres de la diffusion. [Découvrir comment planifier une campagne orchestrée](../create-orchestrated-campaign.md#schedule)

## Configurer une activité de canal {#create-a-delivery-in-a-workflow}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="Activité e-mail"
>abstract="L’activité E-mail permet d’envoyer des e-mails dans votre campagne orchestrée, pour des messages ponctuels et récurrents. Il permet d’automatiser le processus d’envoi d’e-mails à une cible calculée dans la même campagne orchestrée. Vous pouvez combiner des activités de canal dans une zone de travail de campagne à plusieurs étapes, afin de créer des campagnes cross-canal pouvant déclencher des actions en fonction du comportement de la clientèle et des données."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="Activité SMS"
>abstract="L’activité SMS permet d’envoyer des SMS au sein de votre campagne orchestrée, pour les messages ponctuels et récurrents. Il permet d’automatiser le processus d’envoi de SMS à une cible calculée dans la même campagne orchestrée. Vous pouvez combiner des activités de canal dans la zone de travail de campagne à plusieurs étapes, afin de créer des campagnes cross-canal pouvant déclencher des actions en fonction du comportement de la clientèle et des données."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push"
>title="Activité push"
>abstract="L’activité Push permet d’envoyer des notifications push dans le cadre de votre campagne orchestrée. Elle permet la diffusion de campagnes orchestrées ponctuelles et récurrentes, automatisant l’envoi de notifications push à une cible prédéfinie dans la même campagne orchestrée. Vous pouvez combiner des activités de canal dans la zone de travail de campagne afin de créer des campagnes cross-canal pouvant déclencher des actions en fonction du comportement du client et des données."

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
>abstract="L’activité Publipostage direct facilite l’envoi de publipostage direct dans votre campagne orchestrée, pour les messages ponctuels et récurrents. Elle permet d’automatiser le processus de génération du fichier d’extraction requis par les fournisseurs de services postaux. Vous pouvez combiner des activités de canal dans la zone de travail de campagne orchestrée afin de créer des campagnes cross-canal pouvant déclencher des actions en fonction du comportement du client et des données."

Pour configurer une diffusion dans le cadre d&#39;une campagne orchestrée, procédez comme suit.

### Ajoutez une activité de canal et définissez ses propriétés {#add}

1. Ajoutez une activité de canal dans la zone de travail. Les activités de canal disponibles sont **[!UICONTROL E-mail]**, **[!UICONTROL SMS]** et **[!UICONTROL Push]**.

   ![image montrant la zone de travail avec les activités disponibles](../assets/channel-add.png)

1. Sélectionnez l’activité ajoutée et cliquez sur le bouton **[!UICONTROL Modifier l’e-mail]**, **[!UICONTROL Modifier le SMS]** ou **[!UICONTROL Modifier la notification push]** selon le canal choisi.

   ![image illustrant la zone de travail avec une activité E-mail ](../assets/channel-edit.png)

1. Dans l’onglet **[!UICONTROL Propriétés]** , saisissez une description pour votre campagne.

### Configurer la configuration et les paramètres du canal {#configuration}

1. Sélectionnez l’onglet **[!UICONTROL Actions]** et choisissez la configuration de canal à utiliser pour votre message.

   Celle-ci est définie par une [équipe d’administration système](../../start/path/administrator.md). Elle contient tous les paramètres techniques relatifs à l’envoi du message, tels que les paramètres d’en-tête, le sous-domaine, les applications mobiles, etc. [Découvrez comment configurer des configurations de canal](../../configuration/channel-surfaces.md).

1. Pour les e-mails et les SMS, utilisez les options de suivi pour surveiller la réaction des destinataires à vos diffusions e-mail ou SMS.

   Les résultats du suivi sont accessibles dans le rapport de la campagne, une fois celle-ci exécutée. [En savoir plus sur les rapports de campagne](../../reports/campaign-global-report-cja.md)

1. Pour les notifications push, utilisez l’option **[!UICONTROL Mode de diffusion rapide]** pour envoyer des messages à grande vitesse sur le canal push pour une taille d’audience inférieure à 30 millions.

   Le mode de diffusion rapide est un module complémentaire **[!DNL Journey Optimizer]** qui permet d’envoyer très rapidement des messages push en grande quantité. [En savoir plus](../../push/create-push.md#rapid-delivery)

1. La section **[!UICONTROL Expérience de contenu]** vous permet de définir plusieurs traitements de diffusion afin de mesurer celui qui fonctionne le mieux pour votre audience cible.

   Pour ce faire, cliquez sur le bouton **[!UICONTROL Créer une expérience]** puis suivez les étapes détaillées dans cette section : [Créer des fonctionnalités d’expérimentation de contenu](../../content-management/content-experiment.md).

1. La section **[!UICONTROL Langues]** vous permet de créer du contenu dans plusieurs langues au sein de votre campagne.

   Pour ce faire, cliquez sur le bouton **[!UICONTROL Ajouter des langues]** et sélectionnez l’option **[!UICONTROL Paramètres de langue]** souhaitée. Vous trouverez des informations détaillées sur la configuration et l’utilisation des fonctionnalités multilingues dans cette section : [Prise en main du contenu multilingue](../../content-management/multilingual-gs.md)

### Définir le contenu {#content}

Sélectionnez l’onglet **[!UICONTROL Contenu]** pour définir le contenu du message. Le processus de création de contenu dépend du canal sélectionné.

Découvrez les étapes détaillées pour créer le contenu de votre message dans les pages suivantes :

<table style="table-layout:fixed"><tr style="border: 0;">
<td><a href="../../email/create-email.md"><img alt="E-mail" src="../../channels/assets/do-not-localize/email.png"></a>
<div align="center"><a href="../../email/create-email.md"><strong>E-mail</strong></a></div></td>
<td><a href="../../sms/create-sms.md"><img alt="SMS" src="../../channels/assets/do-not-localize/sms.png"></a>
<div align="center"><a href="../../sms/create-sms.md"><strong>SMS</strong></a></div></td>
<td><a href="../../push/create-push.md"><img alt="Notification push" src="../../channels/assets/do-not-localize/push.png"></a>
<div align="center"><a href="../../push/create-push.md"><strong>Notification push</strong></a></div></td>
</tr></table>

Une fois votre contenu défini, utilisez le bouton **[!UICONTROL Simuler le contenu]** pour prévisualiser et tester votre contenu avec des profils de test ou des exemples de données d’entrée chargés à partir d’un fichier CSV/JSON ou ajoutés manuellement. [En savoir plus](../../content-management/preview-test.md)

## Étapes suivantes {#next}

Revenez à votre campagne orchestrée à l’aide de la flèche **[!UICONTROL Précédent]**.

![image illustrant le bouton Précédent](../assets/channel-back.png)

Vous pouvez maintenant terminer l’orchestration des activités dans la zone de travail et publier la campagne pour commencer l’envoi des messages. [Découvrez comment démarrer et surveiller des campagnes orchestrées](../start-monitor-campaigns.md)

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
