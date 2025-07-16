---
solution: Journey Optimizer
product: journey optimizer
title: Démarrer et surveiller les campagnes orchestrées avec Adobe Journey Optimizer
description: Découvrez comment démarrer et surveiller des campagnes orchestrées avec Adobe Journey Optimizer.
hide: true
hidefromtoc: true
exl-id: 3c1cad30-3ed7-4df1-a46a-60394a834e79
source-git-commit: 5c23b4e41dcf426ca458f75057b3653175b2ade8
workflow-type: tm+mt
source-wordcount: '743'
ht-degree: 1%

---

# Création de requêtes de reciblage {#retarget}

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>[Étapes de configuration](configuration-steps.md)<br/><br/>[Accédez aux campagnes orchestrées et gérez-les](access-manage-orchestrated-campaigns.md)<br/><br/>[Étapes clés pour créer une campagne orchestrée](gs-campaign-creation.md) | [Créer et planifier la campagne](create-orchestrated-campaign.md)<br/><br/>[Orchestrer les activités](orchestrate-activities.md)<br/><br/>[Démarrer et surveiller la campagne](start-monitor-campaigns.md)<br/><br/>[le reporting](reporting-campaigns.md) | [Utiliser le créateur de règles](orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier les expressions](edit-expressions.md)<br/><br/><b>[Reciblage](retarget.md)</b> | [Prise en main des activités](activities/about-activities.md)<br/><br/>Activités:<br/>[Et-joindre](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Modifier la dimension](activities/change-dimension.md) - [Activités de canal](activities/channels.md) - [Combine](activities/combine.md) - [Deduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Fork](activities/fork.md) - [Reconciliation](activities/reconciliation.md) - [Enregistrer l’audience](activities/save-audience.md) - [Split](activities/split.md) - [Wait](activities/wait.md) |

{style="table-layout:fixed"}

+++

</br>

>[!BEGINSHADEBOX]

Documentation en cours

>[!ENDSHADEBOX]

Le reciblage vous permet d’effectuer le suivi auprès des destinataires en fonction de leur réponse à une campagne orchestrée précédente. Par exemple, vous pouvez envoyer un second e-mail aux destinataires qui ont reçu le premier message, mais n’ont pas cliqué dessus.

**[!UICONTROL Campagne orchestrée]** fournit deux attributs principaux à cet effet :

* **[!UICONTROL Commentaires sur le message]** : capture les événements liés à la diffusion, par exemple le message envoyé, ouvert, rebond, etc.
* **[!UICONTROL Suivi des e-mails]** : capture les actions de l’utilisateur, par exemple les clics et les ouvertures.

![](assets/do-not-localize/retarget-schema.png){zoomable="yes"}


## Création d’une règle de reciblage basée sur les retours d’informations {#feedback-retarget}

La règle de reciblage basée sur les retours permet de recibler les destinataires en fonction des événements de diffusion de message capturés dans l’attribut **[!UICONTROL Commentaires de message]**. Ces événements incluent les résultats tels que les messages envoyés, ouverts, rejetés ou marqués comme spam.

Grâce à ces données, vous pouvez définir des règles pour identifier les destinataires ayant reçu un message précédent, ce qui permet d’établir une communication de suivi en fonction de statuts de diffusion spécifiques.

1. Créez une **[!UICONTROL Campagne orchestrée]**.

1. Ajoutez une activité **[!UICONTROL Créer une audience]** et définissez la dimension de ciblage sur **[!UICONTROL Destinataire (caas)]**.

1. Dans le **[!UICONTROL Créateur de règles]**, cliquez sur **[!UICONTROL Ajouter une condition]** et sélectionnez **[!UICONTROL Commentaires de message]** dans le **[!UICONTROL Sélecteur d’attributs]**. Cliquez sur **[!UICONTROL Confirmer]** pour créer une condition **Le retour d’informations sur le message existe, telle que**.

   ![](assets/retarget_1.png){zoomable="yes"}

1. Choisissez l’attribut **[!UICONTROL Statut des commentaires]** pour cibler les événements de diffusion des messages.

+++ Détaillé pas à pas

   1. Ajoutez une autre condition liée à l&#39;attribut **[!UICONTROL Message feedback]**.

   1. Recherchez l’attribut **[!UICONTROL Statut du retour d’informations]** et cliquez sur **[!UICONTROL Confirmer]**.

      ![](assets/retarget_3.png){zoomable="yes"}

   1. Dans le menu **[!UICONTROL Condition personnalisée]**, choisissez l&#39;état de la diffusion à suivre dans le menu déroulant **[!UICONTROL Valeur]**.

      ![](assets/retarget_4.png){zoomable="yes"}

+++

1. Choisissez l’attribut **[!UICONTROL Nom de la campagne orchestrée]** pour cibler une campagne orchestrée spécifique.

+++ Détaillé pas à pas

   1. Ajoutez une autre condition liée à l’attribut **[!UICONTROL Commentaires de message]**, recherchez **[!UICONTROL entité]** et accédez à :

      `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign entity`.

   1. Sélectionnez **[!UICONTROL Nom orchestré de la campagne]**.

      ![](assets/retarget_5.png){zoomable="yes"}

   1. Dans le menu **[!UICONTROL Condition personnalisée]**, indiquez le nom de la campagne dans le champ **[!UICONTROL Valeur]**.

+++

1. Sélectionnez l’attribut **[!UICONTROL Nom de l’action de campagne orchestrée]** pour cibler un message ou une activité spécifique dans une campagne orchestrée.

+++ Détaillé pas à pas

   1. Ajoutez une autre condition liée à l’attribut **[!UICONTROL Commentaires de message]**, recherchez **[!UICONTROL entité]** et accédez à :

      `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign entity`.

   1. Sélectionnez **[!UICONTROL Nom de l’action de campagne orchestrée]**.

      ![](assets/retarget_6.png){zoomable="yes"}

   1. Dans le menu **[!UICONTROL Condition personnalisée]**, indiquez le nom de l’action de campagne dans le champ **[!UICONTROL Valeur]**.

      Pour trouver les noms des actions, cliquez sur l’icône ![Informations](assets/do-not-localize/info-icon.svg) en regard du champ Libellé de votre activité.

+++

1. Vous pouvez également filtrer selon l’**[!UICONTROL identifiant de campagne]** (UUID) qui se trouve dans vos propriétés Campaign.

Vous avez maintenant configuré une règle de reciblage basée sur les commentaires pour identifier les destinataires en fonction du statut de diffusion d&#39;un message précédent, tel que envoyé, ouvert, retourné ou marqué comme spam. Une fois cette audience définie, vous pouvez ajouter un e-mail de relance ou affiner davantage votre ciblage en [configurant une règle de reciblage basé sur le tracking](#tracking-based), qui utilise les données d’interaction utilisateur.

![](assets/retarget_9.png){zoomable="yes"}


## Création d’une règle de reciblage basé sur le tracking {#tracking-based}

La règle de reciblage basé sur le tracking cible les destinataires en fonction de leurs interactions avec un message, à l&#39;aide des données de l&#39;attribut **[!UICONTROL Suivi des emails]**. Il capture les actions des utilisateurs telles que les ouvertures d’e-mail et les clics sur les liens.

Pour recibler les destinataires en fonction des interactions des messages (ouverture ou clic, par exemple), utilisez l&#39;entité **[!UICONTROL Tracking des emails]** comme suit :

1. Créez une **[!UICONTROL Campagne orchestrée]**.

1. Ajoutez une activité **[!UICONTROL Créer une audience]** et définissez la dimension de ciblage sur **[!UICONTROL Destinataire (caas)]** pour vous concentrer sur les destinataires précédents de la campagne orchestrée.

1. Dans le **[!UICONTROL Créateur de règles]**, cliquez sur **[!UICONTROL Ajouter une condition]** et sélectionnez **[!UICONTROL Suivi des e-mails]** dans le **[!UICONTROL Sélecteur d’attributs]**.

   Cliquez sur **[!UICONTROL Confirmer]** pour créer une condition **Le suivi des e-mails existe, telle que**.

   ![](assets/retarget_2.png){zoomable="yes"}

1. Pour cibler les interactions des destinataires avec un message, ajoutez une autre condition liée à l&#39;attribut **[!UICONTROL Tracking des emails]** et recherchez l&#39;attribut **[!UICONTROL Type d&#39;interaction]**.

   ![](assets/retarget_7.png){zoomable="yes"}

1. Dans les options de condition personnalisée, utilisez **[!UICONTROL Inclus dans]** comme opérateur et sélectionnez une ou plusieurs valeurs en fonction de votre cas d’utilisation, par exemple **[!UICONTROL Message ouvert]** ou **[!UICONTROL Lien du message sur lequel l’utilisateur a cliqué]**.

   ![](assets/retarget_8.png){zoomable="yes"}

Vous avez maintenant configuré une règle de reciblage basée sur le tracking pour cibler les destinataires en fonction de leurs interactions avec un message précédent, telles que les ouvertures d’e-mail ou les clics sur des liens, à l’aide des données de l’attribut **[!UICONTROL Suivi des e-mails]**. Une fois cette audience définie, vous pouvez ajouter une action de suivi ou affiner davantage votre ciblage en la combinant avec une [règle de reciblage basé sur les commentaires](#feedback-retarget) pour inclure les résultats des messages tels que l’envoi, le rebond ou le marquage comme spam.


![](assets/retarget_10.png){zoomable="yes"}
