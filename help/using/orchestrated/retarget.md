---
solution: Journey Optimizer
product: journey optimizer
title: Démarrer et surveiller les campagnes orchestrées avec Adobe Journey Optimizer
description: Découvrez comment démarrer et surveiller des campagnes orchestrées avec Adobe Journey Optimizer.
hide: true
hidefromtoc: true
exl-id: 3c1cad30-3ed7-4df1-a46a-60394a834e79
source-git-commit: 0ae8372c179707a87a6b512a5420753a4aaef754
workflow-type: tm+mt
source-wordcount: '591'
ht-degree: 2%

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

Le reciblage vous permet d’effectuer le suivi auprès des destinataires en fonction de leur réponse à une campagne orchestrée précédente. Par exemple, vous pouvez envoyer un second e-mail aux profils qui ont reçu le premier, mais n’ont pas cliqué dessus.

Pour ce faire, une campagne orchestrée fournit deux sources de données principales :

- **Commentaires sur le message** : capture les événements liés à la diffusion, par exemple le message envoyé, ouvert, rebond, etc.

- **Suivi des e-mails** : capture les actions de l’utilisateur, par exemple les clics et les ouvertures.

## Création d’une règle de reciblage basée sur les commentaires

La règle de reciblage basé sur les retours permet de recibler les destinataires en fonction des événements de diffusion de message capturés dans le jeu de données **Commentaires de message**. Ces événements incluent les résultats tels que les messages envoyés, ouverts, rejetés ou marqués comme spam.

Grâce à ces données, vous pouvez définir des règles pour identifier les destinataires qui ont reçu un message précédent, mais qui ne l’ont pas utilisé, ce qui permet une communication de suivi basée sur des statuts de diffusion spécifiques.

1. Créez une **Campagne orchestrée**.

2. Ajoutez une activité **Créer une audience** et définissez la dimension de ciblage sur **Destinataire (caas)**.

3. Dans le **Créateur de règles**, cliquez sur **Ajouter une condition** et sélectionnez **Retour d’informations du message** dans le sélecteur d’attributs. Cliquez sur **Confirmer**.

4. Ajoutez une condition pour **Statut des commentaires** et définissez la valeur sur **Message envoyé**.

5. Pour cibler une campagne orchestrée spécifique :

   - Ajoutez une autre condition, recherchez `entity` et accédez à :\
     `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`.

   - Sélectionnez **Nom de la campagne orchestrée** et indiquez le nom de la campagne.

6. Pour cibler un message ou une activité spécifique dans cette campagne orchestrée :

   - Ajoutez une autre condition, recherchez `entity` et accédez à :\
     `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`.

   - Sélectionnez **Nom de l’action de campagne orchestrée** et indiquez le nom de l’action de campagne.

     Pour trouver les noms des actions, cliquez sur l’icône ![Informations](assets/do-not-localize/info-icon.svg) en regard d’une activité dans la zone de travail.

   >[!TIP]
   >
   >Au lieu d’utiliser des noms, vous pouvez également filtrer selon l’**Identifiant de campagne** (UUID), qui se trouve dans vos propriétés Campaign.

## Création d’une règle de reciblage basé sur le tracking

La règle de reciblage basé sur le tracking cible les destinataires en fonction de leurs interactions avec un message, à l&#39;aide des données du jeu de données **Suivi des e-mails**. Il capture les actions des utilisateurs telles que les ouvertures d’e-mail et les clics sur les liens.

Pour recibler les destinataires en fonction des interactions des messages (ouverture ou clic, par exemple), utilisez l&#39;entité **Tracking des emails** comme suit :

1. Créez une **Campagne orchestrée**, puis ajoutez une activité **Créer une audience** avec **Destinataire (caas)** comme dimension de ciblage pour vous concentrer sur les destinataires précédents de la campagne orchestrée.

1. Ajoutez une nouvelle condition pour **Suivi des e-mails**. Cliquez sur **Confirmer** pour créer une condition « Le suivi des e-mails existe, par exemple ».

1. Dans cette condition, ajoutez une condition et recherchez l’attribut **Type d’interaction**.

1. Dans les options de condition personnalisée, utilisez **Inclus dans** comme opérateur et sélectionnez une ou plusieurs valeurs en fonction de votre cas d’utilisation. Par exemple :
   - **Message ouvert**
   - **Lien du message sur lequel l’utilisateur a cliqué**

1. Pour associer les données de tracking à une campagne spécifique :

   - Ajoutez une condition dans le bloc Tracking e-mail .

   - Accédez à `_experience > CustomerJourneyManagement > Entities > AJO Orchestrated Campaign`.

   - Ajoutez des conditions pour **Nom de campagne orchestré** et, si nécessaire, **Nom d’action de campagne orchestré**.

     Pour trouver les noms des actions, cliquez sur l’icône ![Informations](assets/do-not-localize/info-icon.svg) en regard d’une activité dans la zone de travail.

   >[!TIP]
   >
   >Au lieu d’utiliser des noms, vous pouvez également filtrer selon l’**Identifiant de campagne** (UUID), qui se trouve dans vos propriétés Campaign.
