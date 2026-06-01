---
solution: Journey Optimizer
product: journey optimizer
title: Questions fréquentes sur les campagnes orchestrées
description: Questions fréquentes sur les campagnes orchestrées Journey Optimizer
version: Campaign Orchestration
exl-id: 6a660605-5f75-4c0c-af84-9c19d82d30a0
TQID: https://experienceleague.adobe.com/25WjNcE8jmkqH2TvJnyST510xamIV-seDXTmHj0QEYs
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: ad78185d-8f79-40ad-9bad-cbde74af74eeid: b3538224-471e-4c63-a444-9b19d89ae29c
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: b5e335a9-0e5f-4dda-8845-c4ac5dca2be4
topic_v2: id: bcc5edb5-84c3-4940-9f84-ed88b6c16274id: bce87dde-a4ab-44c9-8a18-ad66e4ddb377id: c4147b6e-073b-4d3c-9ab1-d60f2f4434efid: c7d04a2c-412a-4c9d-9d7a-4456eaa5adebid: e0eb8757-182f-49f3-94a4-1587d16f5094id: fd2e3797-f2ea-4b36-a9af-52acf5e90513
source-git-commit: 18f6b23dbbe53e486e5af76ef7cc61fa1784475d
workflow-type: tm+mt
source-wordcount: 2765
ht-degree: 63%

---

# Questions fréquentes {#faq-oc}

Vous trouverez ci-dessous les questions fréquentes sur les campagnes orchestrées Adobe Journey Optimizer.

Vous avez besoin de plus d’informations ? Utilisez les options de commentaires au bas de cette page pour poser votre question ou contacter la [communauté Adobe Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/adobe-journey-optimizer/ct-p/journey-optimizer?profile.language=fr){target="_blank"}.

+++ Qu’est-ce que l’orchestration de campagne ?

L’orchestration de campagne est une fonctionnalité de Journey Optimizer qui prend en charge les workflows en une ou plusieurs étapes qui utilisent le magasin de données relationnelles pour créer et segmenter les audiences à des fins d’engagement par lots.

Journey Optimizer intègre un nouveau type de campagnes : les **campagnes orchestrées**. Les campagnes orchestrées permettent aux marques d’exécuter des campagnes marketing complexes de type « un-à-plusieurs » à grande échelle. Elles sont conçues pour l’engagement initié par la marque, tel que les promotions, les campagnes saisonnières ou les communications basées sur un compte.

Par rapport aux campagnes à action/envoi unique, elles apportent l’**orchestration et le séquencement** au marketing sortant : les audiences suivent ensemble un workflow en plusieurs étapes, plutôt que de recevoir un message unique.

**En savoir plus**

* [Commencer avec les campagnes orchestrées](gs-orchestrated-campaigns.md)
* [Créer votre première campagne orchestrée](gs-campaign-creation.md)

+++

+++ Que puis-je faire avec une campagne orchestrée ?

Les fonctionnalités principales sont les suivantes :

* **Audiences à la demande** : créez et affinez instantanément des groupes cibles à l’aide de requêtes relationnelles.
* **Segmentation d’entités multiples** : créez des audiences précises en connectant les données client à des entités associées (par exemple, comptes, achats, réservations).
* **Visibilité avant l’envoi** : obtenez une évaluation précise de la taille des audiences avant le lancement pour optimiser le ciblage.
* **Workflows à plusieurs étapes** : exécutez des campagnes séquencées telles que des promotions saisonnières, des lancements de produits ou des offres de fidélité.

**Bonnes pratiques**

* Définissez un **objectif de campagne clair** avant de concevoir des workflows.
* Commencez avec une **audience pilote** pour valider les nombres et la logique avant la mise à l’échelle.
* Conservez des règles de segmentation **aussi simples que possible** pour optimiser les performances et la transparence.
* Utilisez des **conventions de nommage cohérentes** pour les audiences et les campagnes afin de faciliter la gestion.

**En savoir plus**

* [Créer une campagne orchestrée](create-orchestrated-campaign.md)
* [Utiliser les activités de campagnes](activities/about-activities.md)
* [Créer votre règle à l’aide du concepteur de requête](build-query.md)

+++

+++ Comment accéder à l’orchestration de campagne ?

Pour accéder à l’orchestration de campagne, votre licence doit inclure le package **Journey Optimizer - Campagnes et parcours** ou **Journey Optimizer - Campagnes**. Contactez votre représentant ou représentante Adobe pour confirmer votre licence et effectuer une mise à jour si nécessaire.

**En savoir plus**

* [Commencer avec les campagnes orchestrées](gs-orchestrated-campaigns.md)
* [Description du produit Adobe Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}

+++

+++ En quoi les campagnes orchestrées sont-elles différentes des parcours ?

* **Campagnes orchestrées** : idéales pour les campagnes **par lots, de type « un-à-plusieurs »**. Les audiences progressent en bloc, selon un planning.
* **Parcours** : parfaits pour l’engagement **en temps réel, de type « un-à-plusieurs »**. Chaque client ou cliente suit le parcours à son propre rythme, déclenché par un comportement ou des événements.

**Bonne pratique** : utilisez-les ensemble : Parcours pour les expériences déclenchées et réactives, et campagnes orchestrées pour les initiatives planifiées basées sur un calendrier.

**En savoir plus**

* [Commencer avec les campagnes orchestrées](gs-orchestrated-campaigns.md)
* [Créer votre premier parcours](../building-journeys/journey-gs.md)
* [Commencer avec les campagnes](../campaigns/get-started-with-campaigns.md)

+++

+++ Qu’est-ce que la segmentation multi-entités ?

L’orchestration de campagnes dans Adobe Journey Optimizer utilise une base de données relationnelle. Ce type de modèle de données comporte des schémas de données distincts, reliés par des relations 1:1 ou 1:many. Cela permet aux utilisateurs et aux utilisatrices de lancer une requête sur n’importe quel schéma, pas seulement au niveau du ou de la destinataire, puis de passer d’un schéma associé à un autre, comme les achats, les produits, les réservations ou les détails du ou de la destinataire, ce qui offre une grande flexibilité dans la création et l’affinement des segments et des audiences.

**Exemple** : cibler toutes les personnes destinataires dont les abonnements expirent dans les 30 prochains jours. Dans l’orchestration de campagne, la requête peut commencer par le schéma des abonnements, rechercher uniquement la colonne de date d’expiration de ce schéma et renvoyer tous les abonnements arrivant à expiration, puis remonter jusqu’aux données des destinataire associées à ces ID d’abonnement spécifiques, ce qui permet d’obtenir des résultats plus rapidement et efficacement que les modèles de données qui initient chaque requête au niveau des destinataires.

**En savoir plus**

* [Commencer à utiliser des schémas et des jeux de données](gs-schemas.md)
* [Configurer une dimension de ciblage](target-dimension.md)
* [Créer votre règle à l’aide du concepteur de requête](build-query.md)

+++

+++ Comment fonctionne le modèle de données ?

Les campagnes utilisent une **base de données relationnelle**. Vous pouvez ainsi interroger différents jeux de données (par exemple, clientes et clients, produits, abonnements) et les associer de manière flexible pour une segmentation plus avancée.

**Bonnes pratiques**

* Organisez les jeux de données de sorte que les **relations (jointures)** reflètent la logique commerciale.
* Évitez les jointures inutiles pour maintenir les performances des requêtes.
* Validez les exemples de résultats avant d’exécuter des extractions à grande échelle.

**En savoir plus**

* [Commencer à utiliser des schémas et des jeux de données](gs-schemas.md)
* [Créer un schéma manuellement](manual-schema.md)
* [Ingérer des données](ingest-data.md)

+++

+++ Puis-je personnaliser les messages avec des données relationnelles ?

Oui. Dans l’orchestration de campagne, un profil de destinataire appelé « Entité de personnes » peut être mis à jour et ces données sont utilisées pour la personnalisation. En outre, les données enrichies des entités liées dans la base de données relationnelle peuvent également être utilisées pour la personnalisation. Vous pouvez utiliser les profils clients ainsi que les données liées (comme les achats ou les abonnements) pour personnaliser le contenu sur tous les canaux pris en charge.

**Recommandations**

* Utilisez des **données transactionnelles et comportementales** pour rendre les offres pertinentes.
* Combinez des **attributs statiques** (par exemple, le niveau de fidélité) avec des **attributs dynamiques** (par exemple, la date de dernier achat).
* Gardez la personnalisation concise : surcharger les messages avec des données peut nuire à la lisibilité.

**En savoir plus**

* [Utiliser l’activité Enrichissement](activities/enrichment.md)
* [Ajouter une activité de canal dans une campagne orchestrée](activities/channels.md)

+++

<!--
## Do Orchestrated campaigns integrate with other Adobe solutions? {#integrations}

Yes. Campaign orchestration is natively integrated with:

* **Customer Journey Analytics**: Campaign orchestration reports are available.  
* **Real-Time CDP**: Audiences built in Campaigns can be read in Real-Time CDP.  
* **Federated Audience Composition (FAC)**: Available as an add-on.  
-->

+++ Comment tester une campagne orchestrée déclenchée par un signal avant sa publication ?

Lorsque la campagne est en version **brouillon**, vous pouvez la tester en définissant des **paramètres** dans le planning et en fournissant des **valeurs de test** pour chacune. Démarrez le workflow, puis appelez l’API de déclenchement (à l’aide de l’exemple de requête de la configuration de planning ou de votre propre requête avec le même point d’entrée) pour exécuter la campagne avec ces valeurs de test. [Découvrez comment terminer et tester une campagne déclenchée par un signal](trigger-orchestrated-campaign.md#build-and-test).

+++

+++ Puis-je rétablir le brouillon d’une campagne orchestrée active ?

Oui, dans des situations particulières. L’option **[!UICONTROL Retour au brouillon]** est conçue comme un mécanisme de récupération permettant de dépublier et de rétablir un statut de brouillon pour une campagne.

Cette option est disponible pour les campagnes planifiées en attente d’exécution ou pour les campagnes actives contenant des erreurs d’exécution. [Découvrez comment rétablir le brouillon d’une campagne active](start-monitor-campaigns.md#back-to-draft)

+++

+++ Que se passe-t-il en interne lorsque je publie une campagne orchestrée ?

Lorsque vous cliquez sur **[!UICONTROL Publier]**, la séquence suivante se produit :

1. **Activation du planificateur** — Si une planification est configurée, le planificateur se déclenche et déclenche l&#39;exécution à l&#39;heure définie.
1. **Les activités Sauvegarde d’audience s’exécutent en premier** — Toutes les activités Sauvegarde d’audience s’exécutent avant les activités de message. Le shell d’audience est créé dans Audience Portal et les profils qualifiés commencent l’ingestion.
1. **L&#39;exécution du message commence** — Les activités de canal commencent le traitement pour la première activité de message du workflow.
1. **Recherche d’instantané de profil** — Les données de profil sont résolues par rapport à un instantané pris au moment de la publication, et non par rapport au profil en temps réel, ce qui garantit la cohérence de l’ensemble de l’exécution.
1. **Évaluation du consentement** — Le consentement est directement respecté à partir de l’enregistrement du profil et n’est pas réévalué au moment de l’envoi.
1. **Réconciliation des profils** — Les destinataires sont réconciliés avec les profils Adobe Experience Platform au moment de l&#39;envoi.
1. **Création du log de diffusion** — Les événements de diffusion sont enregistrés dans le jeu de données `ajo_message_feedback_event`.

**En savoir plus**

* [Séquence d’exécution au moment de la publication](start-monitor-campaigns.md#publication-sequence)
* [Démarrer et surveiller vos campagnes orchestrées](start-monitor-campaigns.md)

+++

+++ Pourquoi mes messages ne sont-ils pas envoyés après la publication de la campagne ?

Plusieurs situations peuvent empêcher l&#39;envoi de messages après leur publication. Vérifiez les éléments suivants dans l’ordre :

1. **Confirmation d’envoi en attente (la plus courante)** — Pour les campagnes non récurrentes, la diffusion des messages est suspendue par défaut jusqu’à ce que vous confirmiez explicitement l’envoi à partir du volet des propriétés de l’activité de canal. La campagne s’affiche comme **en direct** mais aucun message n’est envoyé tant qu’elle n’est pas confirmée. [En savoir plus](start-monitor-campaigns.md#confirm-sending)

1. **La campagne est planifiée pour une heure ultérieure** — Si un planning est configuré, la campagne est Active mais l&#39;exécution n&#39;a pas encore commencé. Vérifiez les paramètres de planification et attendez l’heure de début configurée. [En savoir plus](create-orchestrated-campaign.md#schedule)

1. **Les activités Sauvegarde d’audience sont toujours en cours d’ingestion** — Les activités Sauvegarde d’audience s’exécutent avant les activités de message au moment de la publication. Si l’ingestion de l’audience est toujours en cours, l’exécution du message n’a pas encore commencé. Surveillez les indicateurs de statut d’activité dans la zone de travail. [En savoir plus](start-monitor-campaigns.md#activities)

1. **L’audience est vide** — La requête de ciblage n’a renvoyé aucun profil. Passez en revue vos règles de segmentation et validez le nombre de profils des audiences avant de le republier.

1. **Tous les profils ont été désinscrits** — Le consentement est évalué au moment de l’envoi par rapport à chaque profil. Si tous les profils ciblés se sont désinscrits sur le canal approprié, aucun message n’est envoyé. [En savoir plus](../action/consent.md)

1. **Activité du canal en état d’erreur** — Un indicateur de statut orange ou rouge sur l’activité du canal signale un problème de blocage. Ouvrez les **[!UICONTROL Journaux]** pour plus d’informations sur l’erreur et sur la manière de la résoudre. [En savoir plus](start-monitor-campaigns.md#logs-tasks)

1. **Limitation de la diffusion par contrôle de débit** — Si le contrôle de débit est activé sur l&#39;activité de canal, la diffusion peut être plus lente que prévu. Vérifiez les paramètres de contrôle du débit dans le volet des propriétés de l’activité du canal. [En savoir plus](activities/channels.md#rate-control)

**En savoir plus**

* [Démarrer et surveiller vos campagnes orchestrées](start-monitor-campaigns.md)
* [Ajouter une activité de canal dans une campagne orchestrée](activities/channels.md)

+++

+++ La publication utilise-t-elle le profil en temps réel ou un instantané ?

Au moment de la publication, les données de profil sont résolues par rapport à un **instantané pris au moment de la publication** et non par rapport au profil en temps réel. Cela garantit la cohérence sur l’ensemble de l’exécution de la campagne : toutes les activités traitent le même état de profil, quelle que soit la durée d’exécution de la campagne.

Toutefois, le consentement est toujours respecté à partir de l’enregistrement de profil actuel et n’est pas réévalué au moment de l’envoi.

Notez que la segmentation dans les campagnes orchestrées est effectuée sur les destinataires (magasin relationnel), tandis que l’envoi des messages et les vérifications de consentement sont résolus par rapport au profil Adobe Experience Platform.

**En savoir plus**

* [Séquence d’exécution au moment de la publication](start-monitor-campaigns.md#publication-sequence)
* [Quelle est la relation entre les entités Destinataire et Profil ?](#faq-oc)
* [Utiliser les politiques de consentement](../action/consent.md)

+++

+++ Quels canaux sont pris en charge ?

Vous pouvez créer des campagnes orchestrées pour envoyer des **e-mails**, **SMS**, **notifications push** et **courriers**.

**En savoir plus**

* [Ajouter une activité de canal dans une campagne orchestrée](activities/channels.md)
* [Utiliser les activités de campagnes](activities/about-activities.md)

+++

+++ Est-il possible de lancer plusieurs communications et différents canaux au sein d’une même campagne orchestrée ?

Oui, les campagnes orchestrées prennent en charge l’orchestration cross-canal. Vous pouvez combiner des activités de type e-mail, SMS, notification push et courrier dans une zone de travail de campagne à plusieurs étapes afin de créer des expériences client complètes.

**En savoir plus**

* [Ajouter une activité de canal dans une campagne orchestrée](activities/channels.md)
* [Utiliser les activités de campagnes](activities/about-activities.md)

+++

+++ Des modèles de campagne orchestrée sont-ils disponibles ?

Non, vous ne pouvez pas définir ni utiliser de modèles de campagne, mais vous pouvez utiliser des modèles de contenu pour vos communications.

**En savoir plus**

* [Ajouter une activité de canal dans une campagne orchestrée](activities/channels.md)
* [Créer une campagne orchestrée](create-orchestrated-campaign.md)

+++

+++ Le concepteur de contenu des messages est-il spécifique aux campagnes orchestrées ?

Non, le concepteur de contenu, y compris le Concepteur d’e-mail, est commun à toutes les fonctionnalités de Journey Optimizer.

**En savoir plus**

* [Ajouter une activité de canal dans une campagne orchestrée](activities/channels.md)
* [Utiliser l’activité Enrichissement](activities/enrichment.md)

+++

+++ Comment les différents canaux sont-ils connectés dans les campagnes orchestrées ?

Le composant de canal et l’exécution sont communs à toutes les campagnes Journey Optimizer, mais les canaux pris en charge diffèrent. Les campagnes orchestrées prennent en charge les e-mails, SMS, notifications push et le publipostage direct.

**En savoir plus**

* [Ajouter une activité de canal dans une campagne orchestrée](activities/channels.md)
* [Mécanismes de sécurisation et limitations](guardrails.md)

+++


+++ Les campagnes orchestrées peuvent-elles se connecter aux canaux sortants (web, inApp) ?

Non, les canaux entrants tels que web et in-app ne sont pas pris en charge dans les campagnes orchestrées. Seuls les canaux sortants (e-mail, SMS, notifications push et courrier) sont pris en charge.

**En savoir plus**

* [Mécanismes de sécurisation et limitations](guardrails.md)
* [Ajouter une activité de canal dans une campagne orchestrée](activities/channels.md)

+++

+++ Qu’en est-il des autorisations et du consentement ?

Les autorisations et le consentement pour les campagnes et les parcours orchestrés sont gérés de manière centralisée dans Adobe Experience Platform. Ces paramètres sont appliqués aux deux solutions pour chaque destinataire avant l’envoi.

**Bonnes pratiques**

* Appliquez une **gouvernance centralisée** : évitez de gérer le consentement séparément au niveau de la campagne.
* Contrôlez régulièrement les données de consentement pour détecter des incohérences.
* Respectez les **opt-out spécifiques à un canal** : ne supposez pas que le consentement global couvre tous les canaux.

**En savoir plus**

* [Commencer avec les campagnes orchestrées](gs-orchestrated-campaigns.md)
* [Mécanismes de sécurisation et limitations](guardrails.md)

+++


+++ Puis-je effectuer une segmentation ad hoc dans les campagnes orchestrées ?

Dans l’orchestration de campagne, nous appelons la segmentation ad hoc « segmentation en direct ». Elle vous permet d’accéder en temps réel à l’ensemble des données disponibles dans le stockage relationnel, de concevoir une requête complexe par-dessus et d’obtenir immédiatement un résultat prêt à être activé sur les canaux sortants (par exemple : e-mail et SMS).

**Conseils**

* Utilisez la segmentation ad hoc pour les **besoins urgents** (par exemple, les promotions Flash).
* Enregistrez et documentez les requêtes utiles afin qu’elles puissent être réutilisées dans les prochaines campagnes.
* Validez la taille d’audience avant l’activation pour éviter un envoi insuffisant ou excessif.

**En savoir plus**

* [Créer votre règle à l’aide du concepteur de requête](build-query.md)
* [Utiliser l’activité Créer une audience](activities/build-audience.md)
* [Configurer une dimension de ciblage](target-dimension.md)

+++


+++ L’orchestration de campagne accède-t-elle uniquement aux données chargées par lots ou interroge-t-elle aussi les tables mises à jour en temps réel (par exemple, les données Analytics) ?

L’orchestration de campagne dans Journey Optimizer peut d’abord créer des requêtes ad hoc sur les schémas relationnels. Les schémas relationnels prennent actuellement en charge uniquement les sources par lots. De plus, ils prennent en charge les activités de lecture d’audience de tout type d’audience d’Adobe Experience Platform.

**En savoir plus**

* [Commencer à utiliser des schémas et des jeux de données](gs-schemas.md)
* [Ingérer des données](ingest-data.md)
* [À propos de l’activité Lecture d’audience](activities/read-audience.md)

+++

+++ Les campagnes orchestrées prennent-elles en charge la prise de décision ?

Non, les campagnes orchestrées ne prennent pas en charge les fonctionnalités de prise de décision. Pour les fonctionnalités de prise de décision, utilisez plutôt des parcours Journey Optimizer ou des campagnes d’action standard.

**En savoir plus**

* [Commencer avec les décisions pour les expériences](../experience-decisioning/gs-experience-decisioning.md)
* [Créer votre premier parcours](../building-journeys/journey-gs.md)
* [Commencer avec les campagnes](../campaigns/get-started-with-campaigns.md)

+++


+++ Comment le déploiement fonctionne-t-il entre les différents environnements ?

Les objets créés dans des campagnes orchestrées (par exemple, des audiences et des workflows) appartiennent au sandbox dans lequel ils ont été créés. Pour réutiliser une campagne orchestrée dans un autre sandbox (par exemple, de développement, d’évaluation ou de production), copiez-la à l’aide de l’outil **Sandbox** : ajoutez la campagne à un package, publiez le package et importez-la dans le sandbox cible. La copie importée est créée dans **brouillon** et **réimporter le même package crée une nouvelle campagne** plutôt que de mettre à jour une campagne existante. Un déplacement complet nécessite souvent **plusieurs étapes** : vous pouvez avoir besoin d’aligner **configurations de canal** (les noms correspondants dans la cible), **schémas** et **jeux de données** par le biais du même package ou d’importations de package supplémentaires ; les configurations de canal ne sont pas copiées avec la campagne. Il n’existe pas de liste de contrôle complète avant exportation dans l’interface utilisateur ; utilisez le flux de mappage d’importation et les **alertes post-importation** pour terminer la configuration. Pour plus d’informations et connaître les limitations, voir [Copie d’objets Journey Optimizer entre des sandbox](../configuration/copy-objects-to-sandbox.md).

**Bonnes pratiques**

* Conservez des **sandbox distincts** pour l’expérimentation, l’assurance qualité et la production.
* Juste après l’importation, [dupliquez la campagne](../campaigns/manage-campaigns.md#duplicate-a-campaign) et travaillez à partir du doublon afin que les rapports affichent correctement les commentaires et les données de tracking.
* Après chaque importation, validez la campagne de bout en bout dans le sandbox cible avant de la publier.
* Documentez les configurations et alignez-vous sur les équipes de gouvernance pour réduire la dérive de configuration entre les environnements.

**En savoir plus**

* [Copier des objets Journey Optimizer entre des sandbox](../configuration/copy-objects-to-sandbox.md)
* [Commencer avec les campagnes orchestrées](gs-orchestrated-campaigns.md)
* [Mécanismes de sécurisation et limitations](guardrails.md)

+++

<!--
## Are there recommended practices for running campaigns at scale? {#scale}

Yes, follow the best practices below:  

* **Plan campaigns around business calendars** (product launches, seasonal peaks) to align volume and resources.  
* Use **audience pre-views** before sending to confirm the expected size and avoid surprises.  
* Where possible, **stagger send times** to avoid overwhelming downstream systems (e.g., call centers, websites).  
* Establish a **monitoring routine**—track delivery logs, error rates, and opt-outs after each send.  
* Run **post-campaign analysis** in Customer Journey Analytics to refine targeting and orchestration for the next cycle.  
-->

+++ Quelle est la relation entre les entités Destinataire et Profil ?

La segmentation est effectuée sur les destinataires lors de l’envoi par rapport au profil Adobe Experience Platform. La dimension cible Destinataire étend le Profil unifié avec des données supplémentaires utilisées pour la segmentation dans les campagnes orchestrées, tandis que le Destinataire est réconcilié avec le Profil lors de l’exécution pour envoyer des messages et vérifier la politique de consentement et les règles métier. Cette réconciliation permet d’unifier les règles métier et l’application du consentement au niveau du profil.

![](assets/recipients-and-profiles.png)

**En savoir plus**

* [Configurer une dimension de ciblage](target-dimension.md)
* [Commencer à utiliser des schémas et des jeux de données](gs-schemas.md)
* [Créer votre règle à l’aide du concepteur de requête](build-query.md)

+++

+++ Dans quels cas est-il recommandé d’utiliser les entités Destinataire plutôt que Profil ?

Répondre « Oui » suggère la meilleure banque de données. Cependant, confirmez toujours la meilleure approche en fonction de votre cas d’utilisation et des contraintes avec votre représentant ou représentante Adobe.

| Stockage relationnel | Real-time Customer Profile |
|---------|----------|
| La source des données est-elle déjà relationnelle ? | La source des données est-elle en streaming ? |
| Prévoyez-vous d’ingérer les données en l’état pour les cas d’utilisation marketing ? | La fraîcheur des données est-elle une exigence majeure ? |
| Existe-t-il un volume important de données historiques (`>` 2 mois) nécessaire pour des cas d’utilisation d’activation marketing ? | Existe-t-il des scénarios où une action ou une décision en temps réel nécessite des données ? |
| Existe-t-il des besoins ad hoc de création, d’évaluation et d’activation d’audiences ? | Les données comportementales peuvent-elles être limitées à `<` 90 jours à l’aide d’agrégats précalculés ? |
|  | Des données sont-elles nécessaires pour personnaliser les messages en temps réel ? |

**En savoir plus**

* [Configurer une dimension de ciblage](target-dimension.md)
* [Commencer à utiliser des schémas et des jeux de données](gs-schemas.md)
* [Créer votre règle à l’aide du concepteur de requête](build-query.md)

+++

+++ Quel est le nombre maximal d’activités par campagne orchestrée ?

Deux limites distinctes s’appliquent :

* **Activités de canal** — Un maximum de 10 activités de canal par campagne orchestrée (e-mail, SMS, notification push ou courrier). Les activités de ciblage et de contrôle de flux ne sont pas prises en compte. Le dépassement de cette limite lors de l’enregistrement ou de la publication entraîne l’échec de l’opération.

* **Taille de la zone de travail** — Jusqu’à 500 **d’activités** sur la zone de travail. Pour la maintenabilité, gardez les workflows de moins de 100 **en pratique**

**En savoir plus**

* [Mécanismes de sécurisation et limitations](guardrails.md)
* [Utiliser les activités de campagnes](activities/about-activities.md)

+++

+++ Est-il possible d’effectuer des enrichissements pour ajouter des données supplémentaires ?

Oui, il est possible d’enrichir les données à partir du stockage relationnel et des audiences d’Adobe Experience Platform. Utilisez l’activité Enrichissement pour améliorer les données de votre audience avec des attributs supplémentaires issus de schémas associés.

**En savoir plus**

* [Utiliser l’activité Enrichissement](activities/enrichment.md)
* [Utiliser l’activité Réconciliation](activities/reconciliation.md)

+++

+++ Tous les filtres doivent-ils être définis via des audiences ou est-il possible de configurer un autre type de filtre ?

Les campagnes orchestrées prennent en charge les filtres prédéfinis : vous pouvez définir et enregistrer une requête en tant que filtre, l’ajouter à vos favoris et la réutiliser dans d’autres tâches de segmentation. Les filtres prédéfinis peuvent inclure des paramètres afin que vous puissiez saisir des valeurs au moment de l’utilisation. [Découvrir comment utiliser des filtres prédéfinis](predefined-filters.md)

**En savoir plus**

* [Créer votre règle à l’aide du concepteur de requête](build-query.md)
* [Utiliser l’activité Créer une audience](activities/build-audience.md)
* [Utiliser des filtres prédéfinis](orchestrated-rule-builder.md)

+++


## Ressources supplémentaires

Pour des mises à jour et des formations supplémentaires, consultez les ressources suivantes :

* [Mécanismes de sécurisation et limitations des campagnes orchestrées](guardrails.md)
* [Commencer avec les schémas et les jeux de données dans les campagnes orchestrées](gs-schemas.md)
* [Créer votre première campagne orchestrée](gs-campaign-creation.md)
* [Description du produit Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}
