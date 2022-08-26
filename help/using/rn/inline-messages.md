---
title: Migrer vers la création en ligne de parcours
description: Découvrez comment migrer vos messages
exl-id: accdebba-5322-401e-8a40-3e1539e65a7e
source-git-commit: b31eb2bcf52bb57aec8e145ad8e94790a1fb44bf
workflow-type: tm+mt
source-wordcount: '1732'
ht-degree: 100%

---


# Aperçu de la migration vers la création en ligne{#inline-authoring}

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_before"
>title="En savoir plus sur la nouvelle fonctionnalité de création en ligne"
>abstract="À compter du 25 juillet 2022, les messages seront créés directement à partir d’un parcours. Les messages existants sont automatiquement migrés vers le nouveau modèle. Des actions supplémentaires seront nécessaires après la migration, si vous utilisez actuellement des messages dans vos parcours."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-authoring/inline-messages-steps.html?lang=fr" text="Étapes de migration"

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_during"
>title="Découvrez ce qui se passe"
>abstract="À compter du 25 juillet 2022, les messages seront créés directement à partir d’un parcours. Votre environnement est en cours de migration. Des actions supplémentaires seront nécessaires après la migration, si vous utilisez actuellement des messages dans vos parcours."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-authoring/inline-messages-steps.html" text="Étapes de migration"

>[!CONTEXTUALHELP]
>id="ajo_messages_migration_after"
>title="Découvrez comment migrer vos messages"
>abstract="À compter du 25 juillet 2022, les messages seront créés directement à partir d’un parcours. Les messages existants ont été migrés vers le nouveau modèle. En tant que praticien des parcours, des actions supplémentaires sont désormais nécessaires pour les parcours qui utilisent des messages."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/whats-new/inline-authoring/inline-messages-steps.html" text="Étapes de migration"

>[!CONTEXTUALHELP]
>id="ajo_messages_depecrated_inventory"
>title="Découvrez comment migrer vos messages"
>abstract="À compter du 25 juillet 2022, le menu Messages disparaîtra et les messages seront créés directement à partir d’un parcours. Si vous souhaitez réutiliser vos messages hérités dans les parcours, vous devez les enregistrer en tant que modèles."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/design/email-templates.html?lang=fr#save-as-template" text="Enregistrer des messages en tant que modèles"

Adobe Journey Optimizer propose une nouvelle fonctionnalité qui améliore la façon dont vous créez du contenu pour les canaux Journey Optimizer (e-mail, notification push, SMS). En tant que praticien de Journey Optimizer, vous pouvez désormais créer vos messages directement à partir d’un parcours.

Cette fonctionnalité nécessite une migration des parcours existants qui utilisent des messages. Dans cette page, vous trouverez les informations nécessaires à cette modification ainsi que les étapes que vous devez suivre.

Pour plus d’informations sur vos rôles et responsabilités en tant que praticien de Journey Optimizer, reportez-vous à cette [page](../start/path/marketer.md).

<!--
Here are the main changes in the interface:

* Messages are created direcly from journeys.
* The **Messages** entry in the left navigation menu has been removed. 
* There is no separate library of messages, the journey now centralizes all components.


-->

>[!VIDEO](https://video.tv.adobe.com/v/344698)


## Principaux points à retenir{#keys}

* **Cela me concerne-t-il ?** : cela vous concerne si vous créez des messages à partir du menu **Messages** dans le volet de navigation de gauche et si vous les utilisez dans vos parcours. Si vous utilisez un système tiers (tel qu’Adobe Campaign), cette migration ne vous concerne pas.

* **Modifications du produit** : à la date de disponibilité générale (25 juillet), le contenu de votre canal est créé et géré dans chaque parcours. Le menu **Messages**, dans le volet de navigation de gauche n’est plus disponible ([en savoir plus](../rn/inline-messages.md#change)). Nous allons procéder à une migration de vos parcours existants.

* **Chronologie** : la migration se fait pendant la nuit pour chaque région, via plusieurs [itérations](../rn/inline-messages.md#iterations).

   ![](assets/inline-migration-timeline.png)

* **Actions requises** : une conversion automatique de parcours est effectuée pour vous. Cela dit, nous avons besoin de votre aide pour certaines étapes. Pour en savoir plus sur les étapes requises, consultez cette [page](../rn/inline-messages-steps.md).

* **Obsolescence** : après le 6 septembre, tous les parcours utilisant encore des messages hérités seront arrêtés et ultérieurement supprimés.

## Avantages et modifications du produit{#change}

La vision d’Adobe est de simplifier continuellement le produit afin de fournir des flux d’utilisateurs efficaces et optimisés. Cette nouvelle façon de créer les messages simplifie davantage le processus utilisateur.

Nous avons conçu ce nouveau workflow pour centraliser le contenu au même endroit, directement là où il est utilisé.

Désormais, la création de contenu s’effectue directement dans le parcours. Les **avantages** immédiats que vous obtenez sont :

* Création plus rapide de parcours à l’aide des canaux Journey Optimizer dans un seul flux.
* Visualisation rapide du contenu en basculant de manière transparente entre tous les contenus d’e-mail, de notification push et de SMS dans un parcours.
* Amélioration du flux pour les e-mails et les notifications push à l’aide de la personnalisation contextuelle à partir de la zone de travail.
* Les rapports de parcours centralisent les informations détaillées sur les rapports des canaux.

Voici les **modifications du produit** découlant de cette nouvelle fonctionnalité :

<table>
<tr>
<th>Avant la migration</th>
<th>Après la migration</th>
</tr>
<tr>
<td><img src="assets/inline-migration-before.png"><p>Avant, vous créiez votre message à partir du menu <strong>Messages</strong>. </p></td>
<td><img src="assets/inline-migration-after.png"><p>Désormais, le menu <strong>Messages</strong>, dans le volet de navigation de gauche, n’est plus disponible. </p></td>
</tr>
<tr>
<td><img src="assets/inline-migration-before2.png"><p>Ensuite, vous créiez un parcours, ajoutiez une activité <strong>Message</strong> et sélectionniez le message précédemment créé.</p></td>
<td><img src="assets/inline-migration-after2.png"><p>Désormais, Il vous suffit d’ajouter l’activité d’action du canal souhaité (e-mail, SMS, notification push) à votre parcours. Dans l’activité, vous configurez directement les paramètres du message et accédez à l’éditeur de contenu.</p></td>
</tr>
<tr>
<td><img src="assets/inline-migration-before3.png"><p>Auparavant, les rapports étaient accessibles au niveau des messages et des parcours. Vous deviez jongler entre l’onglet d’exécution du message et le rapport de parcours.</p></td>
<td><img src="assets/inline-migration-after3.png"><p>Désormais, tous les rapports sont centralisés au niveau des parcours. Cela offre une meilleure navigation et expérience utilisateur. Lorsque vous avez plusieurs e-mails dans un parcours, vous pouvez utiliser le menu déroulant <strong>Action</strong> pour afficher le rapport correspondant.
</p></td>
</tr>
</table>

Lors de la phase de disponibilité générale (25 juillet), ce nouveau flux utilisateur sera appliqué à tous les nouveaux parcours. Le menu **Messages**, dans le volet de navigation de gauche, n’est plus disponible.

## Calendrier de la migration{#iterations}

Une migration est nécessaire pour transformer vos parcours existants utilisant des **Messages** dans les parcours avec des actions créées en ligne. Une conversion automatique de parcours est effectuée pour vous. Cela dit, nous avons besoin de votre aide pour certaines étapes.

La migration se produit de nuit pour chaque région, à travers plusieurs itérations. Le calendrier de la migration est le suivant :

* 25 juillet 2022 : disponibilité générale - 1ère itération
* 1er août 2022 : 2e itération
* 5 septembre 2022 : 3e itération
* 6 septembre 2022 : abandon

Pourquoi plusieurs itérations sont-elles nécessaires ?

Au cours d’une itération, chaque parcours est analysé, puis migré lorsque cela est possible. Dans certains cas, la migration automatique n’est pas souhaitée : lorsque le parcours est actif (ce qui signifie qu’il peut encore contenir des profils). Dans ces situations, il vous sera demandé d’effectuer une action. Lors de la prochaine itération, les parcours qui n’ont pas pu être migrés lors de l’itération précédente seront migrés.

## FAQ {#faq}

### Comment ce changement me sera-t-il communiqué ?{#inform}

Avant la première itération, Adobe prendra contact avec vous.

Le changement est déployé de nuit, à travers plusieurs itérations. En savoir plus sur les [itérations](../rn/inline-messages.md#inline-authoring).

Des notifications internes au produit, affichées sur les fenêtres de parcours, vous sont également envoyées :

* Avant le déploiement de la modification

   ![](assets/inline-migration-banner1.png)

* Pendant une itération

   ![](assets/inline-migration-banner2.png)

* Après une itération

   ![](assets/inline-migration-banner3.png)

   Après une itération, le bouton **Vérifier le statut** s’affiche. Vous pouvez ainsi afficher tous vos parcours au format JSON et leurs statuts de migration respectifs. Consultez cette [section](../rn/inline-messages.md#status).

* Lorsque la bannière disparaît, tout est fin prêt. Aucune autre action de votre part n’est requise.

### Qu’est-ce que le processus de migration ?{#process}

La migration est entièrement automatique pour les parcours qui ne sont pas actifs ou fermés. Nous ne voulons pas modifier les parcours actifs ou fermés pour éviter tout impact sur la production. Nous vous demandons de publier la nouvelle version que nous avons créée pour vous.

Toutes les sandboxes d’une organisation cliente sont traitées simultanément. Lors du déploiement de la modification, les actions suivantes sont effectuées :

**TOUT parcours n’utilisant pas de messages**

Ceux-ci ne sont pas affectés par la modification. Seuls les parcours utilisant les messages sont visés par la migration. Cependant, vous pourrez toujours accéder aux messages qui ne sont pas utilisés dans un parcours via l’URL suivante : https://experience.adobe.com/#/@[ORG]/sname:[SANDBOX]/journey-optimizer/messages/

**BROUILLONS de parcours utilisant au moins un message**

Les brouillons des messages sont modifiés pendant la migration. Elles ne font plus référence à un message. Les activités de **Message** sont remplacées par les activités d’action de canal appropriées. Chacune d’entre elles inclut les paramètres et le contenu du canal.

Comme d’habitude, testez le brouillon de votre parcours avant de le publier.

**PARCOURS actifs utilisant au moins un message**

La version active d’un parcours continue à fonctionner pour éviter tout impact sur la production.

Un nouveau brouillon de ce parcours est créé lors de la migration. Ce nouveau brouillon est une copie de votre version active, mais les messages sont remplacés par des actions de canal créées en ligne. Chaque activité d’action de canal inclut les paramètres et le contenu du canal. Le contenu n’est pas perdu. Les rapports ne sont pas perdus.

Nous attendons que vous examiniez ce brouillon, que vous le testiez et que vous le publiiez afin qu’il devienne la version active.

**Parcours TERMINÉS ou ARRÊTÉS utilisant au moins un message**

Ces parcours sont également migrés.

Lors de l’examen du rapport de parcours, les rapports sont désormais plus étoffés et incluent le niveau d’information précédemment disponible dans le rapport des messages.

**Parcours FERMÉS utilisant au moins un message**

La version fermée d’un parcours continue à s’exécuter pour tout profil qu’il contient, afin d’éviter tout impact sur la production.

Les parcours fermés passent automatiquement au statut « Terminé » après 30 jours. Ils seront pris en compte lors de la prochaine itération, lorsqu’ils seront terminés.

**Parcours multicanaux**

Ils ne sont pas migrés. Vous devez les recréer.

### Quels sont mes éléments d’action en tant que client ?{#actions}

Une conversion automatique de parcours est effectuée pour vous, mais quelques étapes sont requises. Pour en savoir plus sur les étapes requises, consultez cette [page](../rn/inline-messages-steps.md).

<!--

The process timeline is indicated in a blue banner on the Journeys screen. See this [section](../rn/inline-messages.md#inform). 

**Before migration**

* Check the date indicated in the banner. 
* Stop non-critical journeys, on development, stage and production environments.
* If you have draft messages that you want to keep using, add them to a journey so they are migrated.

**During migration**

* Migration occurs at night-time
* Do not to create, edit or delete journeys.

**After migration**

* After each iteration, click the **Check status** button in the top banner. This page lists all journeys and their migration status. See this [section](../rn/inline-messages.md#status). 

* For each live journey, a new version is created. Review the new version, test it and publish it. 

* The **Messages** menu, in the left navigation is no longer available. You need to use the new in-line message feature. See this [section](../rn/inline-messages.md#change). 

* If you need to access a specific message which was not used in a journey, you can use this URL and save the content as a template: https://experience.adobe.com/#/@[ORG]/sname:[SANDBOX]/journey-optimizer/messages/

## How can I check the migration status?{#status}

Click the **Check status** button in the top banner. The following page is displayed.

![](assets/inline-migration-log.png)

The status report is at sandbox level. This report includes several useful sections:

**migrationStatus**

This section displays the migration information since the first iteration. Numbers are incremented after each iteration.

* MIGRATED: number of draft journeys migrated successfully.
* NEW_VERSION_CREATED: number of live journeys migrated. For each live journey, a new draft version is created: you must test and publish this version.
* ERROR: number of draft journeys not migrated because of a failure. You need to re-create them.
* ERROR_ON_NEW_VERSION_CREATION: number of live journeys not migrated because of a failure. new draft journey versions not migrated because of a failure. You need to re-create them.

**eligibilityStatus**

This section lists the remaining items after the last iteration:

* toMigrate: number of draft journeys that need to be migrated.
* createNewVersion: number of live journeys to migrate.
* noMigration_live: number of live journeys that do not need to be migrated
* noMigration: number of draft journeys that do not need to be migrated.

The **details** section gives, for each of the above indicators, the list of related journeys.

-->

### Comment puis-je vérifier le statut de la migration ?{#status}

Cliquez sur le bouton **Vérifier le statut** dans la bannière supérieure. La page suivante s’affiche.

![](assets/inline-migration-log.png)

Le rapport de statut est au niveau des sandboxes. Ce rapport comprend plusieurs sections utiles :

**migrationStatus**

Cette section affiche les informations de migration depuis la première itération. Les nombres sont incrémentés après chaque itération.

* MIGRATED : nombre de brouillons de parcours, terminés et arrêtés ayant été migrés avec succès.
* NEW_VERSION_CREATED : nombre de parcours actifs migrés. Pour chaque parcours actif, un nouveau brouillon est créé : c’est ce brouillon que vous devez tester et publier.
* ERROR : nombre de brouillons de parcours, terminés et arrêtés qui n’ont pas été migrés en raison d’un échec. Vous devez les recréer.
* ERROR_ON_NEW_VERSION_CREATION : nombre de parcours actifs non migrés en raison d’un échec. Nouveaux brouillons de parcours non migrés en raison d’un échec. De nouveaux brouillons n’ont pas été créés pour eux. Vous devez les recréer manuellement.

**eligibilityStatus**

Cette section répertorie les éléments restants après la dernière itération :

* toMigrate : nombre de brouillons en version préliminaire, terminés et arrêtés qui doivent être migrés.
* createNewVersion : nombre de parcours actifs à migrer.
* noMigration_live : nombre de parcours actifs n’ayant pas besoin d’être migrés. Les parcours fermés sont également répertoriés ici.
* noMigration : nombre de parcours n’ayant pas besoin d’être migrés.

La section **détails** fournit, pour chacune des sections ci-dessus, la liste des parcours associés.

### Cette modification entraînera-t-elle une interruption du service ?{#interruption}

Il n’y aura pas d’interruption du service.

* Sur les parcours actifs : aucun impact, leur exécution se poursuit.
* Sur les parcours créés : lors de la migration (de nuit), il est vivement recommandé de ne pas créer, modifier ni supprimer des parcours.

### Des données seront-elles perdues ? {#data}

Aucune donnée ne sera perdue et il n’y aura aucun impact sur les parcours actifs. Vous aurez le contrôle de la publication des versions de parcours mises à jour.

### Des fonctionnalités seront-elles abandonnées ?{#functionality}

La façon dont vous créez les messages va changer. Aucune fonctionnalité ne passe à la trappe.

### L’environnement est-il accessible pendant le processus de migration ?

La migration a lieu la nuit. Vous pourrez continuer à utiliser le produit. Mais ne créez pas de parcours, ne les modifiez pas non plus ou ne les supprimez pas.

### Les messages seront-ils toujours envoyés ?

Oui, les parcours actifs continuent de fonctionner.

### Comment savoir si la migration est terminée ?

La migration est terminée lorsque la bannière disparaît. Consultez cette [section](../rn/inline-messages.md#inform).

### Comment les autorisations liées aux messages seront-elles affectées ?

La fonctionnalité de création insérée aura un impact sur les autorisations. Chaque autorisation liée aux messages, telle que [!DNL View Messages] ou [!DNL Manage Messages], sera automatiquement incluse dans les autorisations liées à la fonctionnalité Parcours.

En savoir plus sur cette [page](../administration/ootb-product-profiles.md).

<!--
* Improved authoring flow and navigation
* Personalization: improved contextual personalization flow
* Reporting: the message execution screen will no longer exist. Reporting is centralized in journeys.
* You will still be able to update content in a live journey.
->>
