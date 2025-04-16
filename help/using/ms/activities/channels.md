---
solution: Journey Optimizer
product: journey optimizer
title: Ajouter une activité de canal dans une campagne à plusieurs étapes
description: Découvrez comment ajouter une activité de canal dans une campagne à plusieurs étapes
hide: true
hidefromtoc: true
exl-id: ffe1e77c-6c4f-4f23-9183-d715a4c7c402
source-git-commit: 3d380d2d02eb7043aebcffd00bb2092e7341b0d5
workflow-type: tm+mt
source-wordcount: '899'
ht-degree: 70%

---

# Activités de canal {#channel}

Adobe Journey Optimizer vous permet d’automatiser et d’exécuter des campagnes marketing sur les canaux entrants et sortants. Vous pouvez combiner des activités de canal dans la zone de travail de campagne orchestrée afin de créer des campagnes orchestrées cross-canal pouvant déclencher des actions en fonction du comportement du client et des données. Les canaux pris en charge sont répertoriés sur [cette page](../../channels/gs-channels.md).

Vous pouvez par exemple créer une campagne de bienvenue par e-mail qui inclut une série de messages sur différents canaux, tels que les canaux e-mails, SMS, notifications push et courrier. Vous pouvez également envoyer un e-mail de relance une fois qu’un client ou une cliente a effectué un achat, ou envoyer un message d’anniversaire personnalisé par SMS.

Grâce aux activités de canal, vous pouvez créer des campagnes personnalisées et complètes qui impliquent la clientèle sur plusieurs touchpoints et génèrent des conversions.

## Conditions préalables {#channel-activity-prereq}

Commencez à créer votre campagne orchestrée avec les activités pertinentes :

* Avant d’insérer une activité de canal, vous devez définir l’audience. L’audience est la cible principale de votre diffusion : les profils qui reçoivent les messages.

* Pour envoyer une diffusion récurrente, lancez votre campagne orchestrée avec une activité **Planificateur**. Vous pouvez également utiliser une activité **Planificateur** pour les diffusions ponctuelles afin de définir la date de contact de celles-ci. Cette date de contact peut également être définie dans les paramètres de la diffusion. Consultez [cette section](scheduler.md).

## Configurer une activité de canal {#create-a-delivery-in-a-workflow}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_email"
>title="Activité e-mail"
>abstract="L’activité E-mail permet d’envoyer des e-mails dans votre campagne à plusieurs étapes pour des messages ponctuels et récurrents. Elle permet d’automatiser le processus d’envoi d’e-mails à une cible calculée dans la même campagne à plusieurs étapes. Vous pouvez combiner des activités de canal dans une zone de travail de campagne à plusieurs étapes, afin de créer des campagnes cross-canal pouvant déclencher des actions en fonction du comportement de la clientèle et des données."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_sms"
>title="Activité SMS"
>abstract="L’activité SMS permet d’envoyer des SMS dans votre campagne à plusieurs étapes pour les messages ponctuels et récurrents. Elle permet d’automatiser le processus d’envoi de SMS à une cible calculée dans la même campagne à plusieurs étapes. Vous pouvez combiner des activités de canal dans la zone de travail de campagne à plusieurs étapes, afin de créer des campagnes cross-canal pouvant déclencher des actions en fonction du comportement de la clientèle et des données."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_ios"
>title="Activité Notification push iOS"
>abstract="L’activité Notification push iOS permet d’envoyer des notifications push iOS dans le cadre de votre campagne à plusieurs étapes. Elle permet la diffusion de campagnes à plusieurs étapes ponctuelles et récurrentes, en automatisant l’envoi de notifications push iOS à une cible prédéfinie dans le même workflow. Vous pouvez combiner des activités de canal dans la zone de travail du workflow afin de créer des workflows cross-canal pouvant déclencher des actions en fonction du comportement et des données de la clientèle."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_push_android"
>title="Activité notification push Android"
>abstract="L’activité Notification push Android permet d’envoyer des notifications push Android dans le cadre de votre campagne à plusieurs étapes. Elle permet la diffusion de messages ponctuels et récurrents, en automatisant l’envoi de notifications push Android à une cible prédéfinie dans la même campagne à plusieurs étapes. Vous pouvez combiner des activités de canal dans la zone de travail de campagne à plusieurs étapes, afin de créer des campagnes cross-canal pouvant déclencher des actions en fonction du comportement de la clientèle et des données."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_directmail"
>title="Activité Courrier"
>abstract="L’activité Courrier facilite l’envoi de courrier depuis votre campagne à plusieurs étapes pour les messages ponctuels et récurrents. Elle permet d’automatiser le processus de génération du fichier d’extraction requis par les fournisseurs de services postaux. Vous pouvez combiner des activités de canal dans la zone de travail de campagne à plusieurs étapes, afin de créer des campagnes cross-canal pouvant déclencher des actions en fonction du comportement de la clientèle et des données."

Pour configurer une diffusion dans le cadre d&#39;une campagne orchestrée, procédez comme suit :

1. Ajoutez une activité de canal : **[!UICONTROL E-mail]**, **[!UICONTROL SMS]**, **[!UICONTROL Notification push (Android)]**, **[!UICONTROL Notification push (iOS)]** ou **[!UICONTROL Courrier]**.

1. Sélectionnez le **Type de diffusion** : unique ou récurrent.

   * **Diffusion unique** : il s’agit d’une diffusion ponctuelle, envoyée une seule fois, par exemple un e-mail pour le Black Friday.
   * **Diffusion récurrente** : cette diffusion est envoyée plusieurs fois en fonction de sa fréquence d’exécution définie dans une [activité Planificateur](scheduler.md). Chaque fois que la campagne orchestrée s’exécute, l’audience est recalculée et la diffusion est envoyée à l’audience mise à jour, avec le contenu mis à jour. Il peut s’agir d’une newsletter hebdomadaire ou d’un e-mail d’anniversaire récurrent.

1. Choisissez un **modèle** de diffusion. Les modèles sont des paramètres de diffusion préconfigurés, spécifiques à un canal. Un modèle intégré est disponible pour chaque canal et prérempli par défaut.

   ![](../assets/delivery-activity-in-wf.png)

   Vous pouvez sélectionner le modèle dans le volet de gauche de la configuration de l’activité de canal. Si l’audience précédemment sélectionnée n’est pas compatible avec le canal, vous ne pouvez pas sélectionner de modèle. Pour résoudre ce problème, mettez à jour l’activité **Créer une audience** afin de sélectionner une audience ayant le mapping de ciblage approprié.

1. Cliquez sur **Créer une diffusion**. Vous pouvez définir les paramètres et le contenu de votre message de la même manière que vous créez une diffusion autonome. Vous pouvez également tester et simuler le contenu.

1. Revenez à votre workflow. Pour continuer votre workflow, activez l’option **Générer une transition sortante** pour ajouter une transition après l’activité de canal.

1. Cliquez sur **Démarrer** pour lancer votre campagne orchestrée.

   Par défaut, le démarrage d’une campagne orchestrée déclenche l’étape de préparation du message, sans envoyer immédiatement le message.

1. Ouvrez votre activité de canal pour confirmer l’envoi avec le bouton **Vérifier et envoyer**.

1. Dans le tableau de bord de la diffusion, cliquez sur **Envoyer**.

## Exemples {#cross-channel-workflow-sample}

Voici un exemple de campagne orchestrée cross-canal avec une segmentation et deux diffusions. La campagne orchestrée cible tous les clients qui vivent à Paris et qui sont intéressés par les machines à café. Parmi cette population, un e-mail est envoyé à la clientèle régulière, et un SMS est envoyé à la clientèle VIP.

![](../assets/workflow-channel-example.png)

<!--
description, which use case you can perform (common other activities that you can link before of after the activity)

how to add and configure the activity

example of a configured activity within a workflow
The Email delivery activity allows you to configure the sending an email in a workflow. 

-->

Vous pouvez également créer une campagne orchestrée récurrente afin d&#39;envoyer un SMS personnalisé tous les premiers jours du mois à 20h00 à l&#39;ensemble de la clientèle parisienne.

![](../assets/workflow-channel-example2.png)

<!-- Scheduled emails available?

This can be a single send email and sent just once, or it can be a recurring email.
* Single send emails are standard emails, sent once.
* Recurring emails allow you to send the same email multiple times to different targets over a defined period. You can aggregate the deliveries per period in order to get reports that correspond to your needs.

When linked to a scheduler, you can define recurring emails.
Email recipients are defined upstream of the activity in the same workflow, via an Audience targeting activity.

-->


<!--The message preparation is triggered according to the workflow execution parameters. From the message dashboard, you can select whether to request or not a manual confirmation to send the message (required by default). You can start the workflow manually or place a scheduler activity in the workflow to automate execution.-->
