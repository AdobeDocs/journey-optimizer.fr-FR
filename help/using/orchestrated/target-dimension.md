---
solution: Journey Optimizer
product: journey optimizer
title: Création de votre dimension de ciblage
description: Découvrez comment mapper un schéma relationnel au profil client
badge: label="Alpha"
hide: true
hidefromtoc: true
source-git-commit: 70d397614dc0e5b5ce94cc4221a28d47dc9b476d
workflow-type: tm+mt
source-wordcount: '642'
ht-degree: 11%

---


# Configuration d’une dimension de ciblage {#configuration}

+++ Table des matières

| Bienvenue dans les campagnes orchestrées | Lancer votre première campagne orchestrée | Interroger la base de données | Activités de campagnes orchestrées |
|---|---|---|---|
| [Prise en main des campagnes orchestrées](gs-orchestrated-campaigns.md)<br/><br/>Création et gestion de schémas et de jeux de données relationnels :</br> <ul><li>[Prise en main des schémas et des jeux de données](gs-schemas.md)</li><li>[Schéma manuel](manual-schema.md)</li><li>[Schéma de chargement de fichier](file-upload-schema.md)</li><li>[ Ingérer des données ](ingest-data.md)</li></ul>[Accéder aux campagnes orchestrées et les gérer](access-manage-orchestrated-campaigns.md)<br/><br/>[Étapes clés pour créer une campagne orchestrée](gs-campaign-creation.md)<br/><br/>[Configurer une dimension Target](target-dimension.md) | <b>[Créer et planifier la campagne](create-orchestrated-campaign.md)</b><br/><br/>[Orchestrer les activités](orchestrate-activities.md)<br/><br/>[Démarrer et surveiller la campagne](start-monitor-campaigns.md)<br/><br/>[Reporting](reporting-campaigns.md) | [Utiliser le créateur de règles](orchestrated-rule-builder.md)<br/><br/>[Créer votre première requête](build-query.md)<br/><br/>[Modifier les expressions](edit-expressions.md)<br/><br/>[Reciblage](retarget.md) | [Commencer avec les activités](activities/about-activities.md)<br/><br/>Activités :<br/>[Rendez-vous](activities/and-join.md) - [Créer une audience](activities/build-audience.md) - [Changement de dimension](activities/change-dimension.md) - [Activités de canal](activities/channels.md) - [Combiner](activities/combine.md) - [Déduplication](activities/deduplication.md) - [Enrichissement](activities/enrichment.md) - [Branchement](activities/fork.md) - [Réconciliation](activities/reconciliation.md) - [Enregistrer l’audience](activities/save-audience.md) - [Partage](activities/split.md) - [Attente](activities/wait.md) |

{style="table-layout:fixed"}

+++

<br/>

>[!BEGINSHADEBOX]

</br>

Le contenu de cette page n’est pas définitif et peut être modifié.

>[!ENDSHADEBOX]

Dans de nombreux cas, un seul profil client peut être lié à plusieurs entités associées, telles que des abonnements, des contrats de service ou des appareils, ayant chacun leur propre identifiant et leurs propres besoins en matière de communication.

Grâce aux **Campagnes orchestrées**, vous pouvez désormais concevoir et diffuser des communications ciblées au niveau de l’entité, à l’aide des fonctionnalités de schéma relationnel de **Adobe Experience Platform**. Vous pouvez ainsi segmenter, personnaliser et générer des rapports par entité plutôt que par destinataire.

## Création de votre dimension de ciblage {#targeting-dimension}

Un profil client unique peut être associé à plusieurs entités associées, telles que des contrats, des appareils ou des abonnements, chacune ayant son propre identifiant unique. Cette configuration vous permet de cibler, de segmenter et de générer des rapports sur chaque entité individuellement.

Commencez par configurer l&#39;orchestration des campagnes en mappant un schéma relationnel au profil client.

1. Dans **[!UICONTROL Administration]**, accédez au menu **[!UICONTROL Configurations]** et sélectionnez **[!UICONTROL Dimension Campaign Target]**.

   ![](assets/target-dimension-1.png)

1. Cliquez sur **[!UICONTROL Créer]** pour commencer à créer votre **[!UICONTROL dimension de ciblage]**.

1. Sélectionnez le [Schéma précédemment configuré](gs-schemas.md) &#x200B; dans la liste déroulante.

1. Sélectionnez la **[!UICONTROL valeur d’identité]** qui représente l’entité à cibler.

   Dans cet exemple, le profil client est lié à plusieurs abonnements, chacun étant représenté par un `crmID` unique dans le schéma `Recipient`. En définissant le **[!UICONTROL Dimension cible]** pour utiliser le schéma `Recipient` et son identité `crmID`, vous pouvez envoyer des messages au niveau de l’abonnement, plutôt qu’au niveau du profil client principal, en vous assurant que chaque contrat ou ligne reçoit son propre message personnalisé.

   [En savoir plus dans la documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/schema/composition#identity)

   ![](assets/target-dimension-2.png)

1. Cliquez sur **[!UICONTROL Enregistrer]** pour terminer la configuration.

Après avoir configuré le **[!UICONTROL Dimension cible]**, procédez à la création et à la configuration de votre **[!UICONTROL Configuration de canal]** et définissez les **[!UICONTROL Détails d’exécution]** correspondants.

## Configuration de votre configuration de canal {#channel-configuration}

Après avoir configuré votre **[!UICONTROL Dimension Target]**, vous devez configurer votre e-mail ou SMS **[!UICONTROL Configuration du canal]** et définir les **[!UICONTROL Détails d’exécution]** appropriés. Cela permet de s’assurer que les messages sont envoyés en utilisant la logique d’identité et de ciblage correcte.

1. Commencez par créer et configurer votre **[!UICONTROL configuration de canal]**.

   Vous pouvez également mettre à jour une **[!UICONTROL configuration de canal]** existante.

   ➡️ [Suivez les étapes présentées sur cette page](../email/surface-personalization.md)

1. Dans la section **[!UICONTROL Détails d’exécution]** de votre **[!UICONTROL Configuration du canal]**, accédez à l’onglet **[!UICONTROL Campagnes orchestrées]**.

   ![](assets/target-dimension-3.png)

1. Cliquez sur **[!UICONTROL Activé]** pour le rendre compatible avec les campagnes orchestrées.

1. Choisissez votre méthode de diffusion :

   * **[!UICONTROL Dimension cible]** : envoyez-le à l’entité principale, par exemple au destinataire.

   * **[!UICONTROL Target + Dimension Secondaire]** : envoi à l’aide des entités principales et secondaires, par exemple destinataire + contrat.

1. Dans la liste déroulante, sélectionnez votre [Dimension Target précédemment créé](#targeting-dimension).

   ![](assets/target-dimension-4.png)

1. Dans la section **[!UICONTROL Adresse d’exécution]**, choisissez le **[!UICONTROL Source]** à utiliser pour récupérer l’adresse de diffusion, telle que l’adresse e-mail ou le numéro de téléphone :

   * **[!UICONTROL Profil]** : sélectionnez cette option si l’adresse de diffusion, par exemple l’adresse e-mail, est stockée directement dans le profil principal du client.

     Utile lors de l’envoi de messages au client principal, et non à une entité associée spécifique.

   * **[!UICONTROL Dimension cible]** : choisissez cette option si l’adresse de diffusion est stockée dans l’entité associée, par exemple un destinataire ou un abonnement.

     Utile lorsque chaque destinataire possède sa propre adresse de diffusion, telle qu’un e-mail ou un numéro de téléphone différent.

1. Dans le champ **[!UICONTROL Adresse de diffusion]**, cliquez sur ![icône de modification](assets/do-not-localize/edit.svg) pour choisir le champ spécifique à utiliser pour votre diffusion de messages.

   ![](assets/target-dimension-4.png)

1. Une fois la configuration effectuée, cliquez sur **[!UICONTROL Envoyer]**.

Votre canal est maintenant prêt à être utilisé avec les campagnes orchestrées. Les messages seront diffusés en fonction de la dimension cible sélectionnée.
