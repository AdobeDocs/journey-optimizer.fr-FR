---
solution: Journey Optimizer
product: journey optimizer
title: Dépannage de Journey Optimizer
description: Résolution des problèmes liés à Journey Optimizer
feature: Get Started
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 598be5d2c5aca0262063c61e80e6b36020983131
workflow-type: tm+mt
source-wordcount: '2674'
ht-degree: 2%

---

# Résolution des problèmes {#ajo-troubleshooting}

Voici une liste d’articles de dépannage pour Adobe Journey Optimizer. Chaque section de dépannage fournit des réponses aux questions les plus fréquemment posées ainsi que des solutions aux problèmes.

Voir aussi la [FAQ Adobe Experience Platform et la documentation de dépannage](https://experienceleague.adobe.com/en/docs/experience-platform/landing/troubleshooting#service-troubleshooting-directory){target="_blank"}.

## Canal e-mail {#ajo-troubleshooting-email}

+++ Comment éviter les problèmes de formatage des e-mails dans Adobe Journey Optimizer à l’aide des thèmes ?

Dans Adobe Journey Optimizer (AJO), la modification des blocs CSS par défaut dans l’en-tête de l’e-mail peut entraîner des problèmes de mise en forme inattendus, en particulier après la suppression de fragments de contenu. Ces problèmes sont plus visibles sur les appareils mobiles et peuvent entraîner des changements de disposition ou des incohérences de style. Pour éviter cela, utilisez la fonctionnalité Thèmes pour appliquer le CSS personnalisé en toute sécurité sans modifier les styles CSS générés par le système.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-27252){target="_blank"} pour savoir comment résoudre ce problème.

En savoir plus sur le formatage des e-mails [sur cette page](../email/get-started-email-design.md).

+++


+++ Pourquoi les fragments contenant des champs modifiables ne fonctionnent-ils pas ?

Dans Adobe Journey Optimizer, les fragments contenant des champs modifiables peuvent ne pas se charger correctement ou se dupliquer de manière inattendue lorsqu’ils sont ajoutés aux modèles. Le problème affecte généralement des fragments spécifiques dans les environnements.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26908){target="_blank"} pour savoir comment résoudre ce problème.

En savoir plus sur les fragments personnalisables [sur cette page](../content-management/customizable-fragments.md).

+++

+++ Pourquoi les fragments HTML ne s’affichent-ils pas correctement dans les e-mails ?

Les fragments HTML peuvent ne pas s’afficher correctement dans les e-mails, apparaissant souvent sous la forme **identifiants de fragment** plutôt que de contenu réel. Contrairement aux fragments visuels, les fragments HTML nécessitent une configuration soigneuse. Pour résoudre ce problème, suivez les bonnes pratiques relatives à l’utilisation des fragments d’expression **visuels et HTML** dans vos campagnes par e-mail.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-25441){target="_blank"} pour savoir comment résoudre ce problème.

Pour en savoir plus sur les fragments d’HTML [consultez cette page](../content-management/fragments.md).

+++

+++ Pourquoi les modèles d’e-mail et le contenu disparaissent-ils des parcours dépubliés ?

Lors de la modification de modèles d’e-mail dans un parcours dépublié, le contenu et les modèles de certains e-mails peuvent disparaître de manière inattendue. Cela peut entraîner des reprises et des retards. Pour réduire le risque de ce problème, évitez les modifications simultanées, limitez le nombre d’onglets ouverts et enregistrez fréquemment les modifications.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"} pour savoir comment résoudre ce problème.

En savoir plus sur les modèles [sur cette page](../email/use-email-templates.md).

+++

+++ Pourquoi le champ Pré-titre de l’e-mail ne s’affiche-t-il pas en mode « Coder le vôtre » ? 

En mode **&#39;Coder le vôtre&#39;** sous la fonction **Modifier le corps de l&#39;e-mail**, le champ de saisie Pré-titre n&#39;apparaît pas. Pour inclure le texte du pré-titre, les utilisateurs doivent **coder manuellement le pré-titre** dans leur contenu HTML personnalisé.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26174){target="_blank"} pour savoir comment résoudre ce problème.

En savoir plus sur la configuration du pré-titre des e-mails [sur cette page](../email/header-parameters.md).

+++

+++ Pourquoi y a-t-il une incohérence dans le comportement des liens lors de l’utilisation d’un composant HTML dans les modèles d’e-mail ?  

Lors de l’ajout d’un composant **HTML** à un modèle d’e-mail, les liens peuvent se comporter différemment selon le **client de messagerie**, **mode d’affichage** ou **appareil/navigateur**. Par exemple, les liens d&#39;ancrage peuvent fonctionner différemment dans la vue côte à côte d&#39;**Outlook** par rapport à la vue plein écran. Tenez compte de ces variations lors de la conception de modèles d’e-mail et testez-les sur plusieurs clients et appareils.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26221){target="_blank"} pour savoir comment résoudre ce problème.

Consultez également la section Bonnes pratiques en matière de conception d&#39;email [sur cette page](../email/get-started-email-design.md).

+++


+++ Comment éviter les liens de tracking e-mail manquants dans les rapports ?

Le suivi des liens manquants dans Adobe Journey Optimizer se produit lorsque les URL d’e-mail utilisent des variables dynamiques et ne commencent pas par http, ou lorsque des instructions logiques sont placées dans le champ URL. Pour résoudre ce problème, assurez-vous que toutes les URL commencent par http, évitez d’utiliser la logique dans le champ URL et déplacez la logique de personnalisation complexe vers le contenu HTML ou les attributs prétraités.


Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26932){target="_blank"} pour savoir comment résoudre ce problème.

En savoir plus sur le tracking e-mail [sur cette page](../email/message-tracking.md).

+++

+++ Comment résoudre une erreur d’échangeur de messagerie lors de la configuration de campagnes par e-mail transactionnelles déclenchées par l’API ? 

Si vous rencontrez une erreur Mail Exchanger (MX) lors de la création d’une configuration de canal pour une campagne d’e-mail transactionnel déclenchée par l’API dans Adobe Journey Optimizer, elle peut être due à des **erreurs de configuration DNS** ou à des **limitations de la politique DMARC**. Pour résoudre ce problème, vérifiez que votre DNS est correctement configuré et que votre domaine est conforme aux exigences **Domain-based Message Authentication, Reporting, and Conformance (DMARC)**.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26200){target="_blank"} pour savoir comment résoudre ce problème.

En savoir plus sur les politiques de DMARC des e-mails [sur cette page](../configuration/dmarc-record-update.md).

Voir aussi [documentation des campagnes déclenchées par API](../campaigns/api-triggered-campaigns.md).
+++

## Canal de notification push {#ajo-troubleshooting-push}

+++ Un profil peut-il avoir plusieurs jetons push dans Adobe Journey Optimizer ?

Lors de l’implémentation de notifications push dans Journey Optimizer, un seul profil peut en effet avoir plusieurs jetons push associés à différents appareils. Lors d’une campagne de notification push, Journey Optimizer est conçu pour gérer ces jetons et s’assurer que le profil ciblé peut être atteint sur tous les appareils associés.

Consultez [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"} pour en savoir plus sur la gestion des jetons push.

En savoir plus sur la configuration des notifications push [sur cette page](../push/push-configuration.md).

+++

+++ Pourquoi le fait de cliquer sur un message push ne me redirige-t-il pas vers l’URL web configurée ?  

Si les messages push ne sont pas redirigés vers l&#39;URL web prévue, cela peut être dû à une configuration incorrecte de l&#39;action de clic ou à la désactivation des paramètres de notification push. Assurez-vous que l’**action de clic** du message push est correctement définie et que l’**affichage automatique et le suivi** des notifications push sont activés pour résoudre ce problème.

Consultez [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26226){target="_blank"} pour en savoir plus sur ce problème.

En savoir plus sur la configuration des notifications push [sur cette page](../push/push-configuration.md).

+++


## Canal SMS {#ajo-troubleshooting-sms}

+++ Pourquoi mes SMS transactionnels ne sont-ils pas diffusés même si le consentement est défini sur `marketing.sms.value=y` ?

Si un destinataire répond **STOP** à un SMS, tous les futurs messages de ce numéro court sont bloqués, y compris les messages transactionnels. Pour garantir la diffusion ininterrompue des SMS transactionnels, configurez-les et envoyez-les par le biais d’un **numéro court distinct** auquel les destinataires ne se sont pas précédemment désinscrits.

Consultez [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26258){target="_blank"} pour en savoir plus sur ce problème.

En savoir plus sur la configuration du processus d’opt-out des SMS [sur cette page](../sms/sms-opt-out.md).

+++

## Canal in-app

+++ Pourquoi ne puis-je pas créer de rapports sur le canal in-app dans Customer Journey Analytics ?

Les difficultés liées à la création de rapports sur le **canal in-app** dans Adobe Customer Journey Analytics proviennent souvent de **vues de données**, **jeux de données** ou **mises à jour de schéma** mal configurées. Assurez-vous que ces configurations sont correctement appliquées pour résoudre le problème.

Consultez [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26206){target="_blank"} pour en savoir plus sur ce problème.

Découvrez comment intégrer des données d’analyse Journey Optimizer dans Customer Journey Analytics [sur cette page](https://experienceleague.adobe.com/en/docs/analytics-platform/using/integrations/ajo?lang=en#automatically-configure-journey-optimizer-integration){target="_blank"}.

Consultez également la documentation sur les rapports à tout moment de [Journey Optimizer](../reports/report-gs-cja.md)

+++


## Gestion des données {#ajo-troubleshooting-data-management}

+++ Comment les paramètres de durée de vie (TTL) s’appliquent-ils aux jeux de données de profil et de lac de données lorsque vous créez un nouveau sandbox ?

Les organisations qui configurent de nouveaux sandbox dans Adobe Journey Optimizer se sont interrogées sur la manière dont les paramètres de durée de vie (TTL) s’appliquent aux jeux de données de profil et du lac de données. Cet article précise que les paramètres de durée de vie n’affectent pas les sandbox existants et sont automatiquement appliqués uniquement aux sandbox nouvellement configurés.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"} pour savoir comment gérer la durée de vie.

En savoir plus sur la durée de vie du jeu de données [sur cette page](../data/datasets-ttl.md).

+++


## Gestion des profils et des audiences {#ajo-troubleshooting-audiences}

+++ Comment résoudre les incohérences du nombre d’audiences ?

Le nombre d’entrées traitées dans la fonction **Lecture d’audience** de Adobe Journey Optimizer peut être inférieur au nombre d’audiences attendu. Ce problème survient souvent en raison de configurations d’espace de noms incorrectes, ce qui entraîne l’exclusion des profils des parcours. La résolution implique la vérification et la correction des configurations d’espace de noms, l’examen de la documentation pertinente et l’ajustement des priorités pour garantir des opérations plus fluides dans Adobe Journey Optimizer.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/en/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"} pour savoir comment résoudre ce problème.

Voir aussi [cet article sur le nombre d’audiences obsolètes](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26166){target="_blank"}.

Pour en savoir plus sur l’activité **Lecture d’audience** dans les parcours [consultez cette page](../building-journeys/read-audience.md).

+++

+++ Pourquoi les mises à jour de profil échouent-elles ?

Dans Adobe Journey Optimizer, certaines valeurs de champ peuvent ne pas se mettre à jour correctement après avoir exécuté une activité **Mettre à jour le profil** dans un parcours. Dans certains cas, les champs mis à jour peuvent disparaître ou revenir à leur état précédent. Pour résoudre ce problème, recherchez les règles ou conditions en conflit, vérifiez les paramètres d’autorisations, utilisez un jeu de données unique pour l’activité **Mettre à jour le profil** et assurez-vous qu’aucun autre processus d’ingestion n’écrit sur le même profil en même temps.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26352){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

En savoir plus sur l&#39;activité **Mettre à jour le profil** dans parcours [sur cette page](../building-journeys/update-profiles.md).

Consultez également la documentation de [Adobe Experience Platform sur l’ingestion de données](https://experienceleague.adobe.com/en/docs/experience-platform/ingestion/tutorials/ingest-batch-data?lang=en#dataset-activity){target="_blank"}.

+++

+++ Pourquoi le nombre de profils entrant dans un parcours diffère-t-il de celui de l’audience associée ?

Cette incohérence peut survenir lorsque le parcours utilise l’instantané de profil d’un jour précédent si l’instantané du jour en cours n’est pas disponible au moment de l’exécution du parcours.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26253){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

En savoir plus dans [cette publication de la communauté Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/real-time-customer-data-platform/profile-snapshot-and-segment-qualification-troubleshooting/ba-p/698998){target="_blank"}.

Consultez également la documentation de l’API [Adobe Experience Platform Schedules](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/api/schedules?lang=en){target="_blank"} pour savoir quand votre tâche quotidienne est planifiée.

+++


+++ Comment résoudre les problèmes de population d’audience ?

Des problèmes de population d’audiences peuvent se produire lorsque des composants ou des ressources sont manquants, souvent en raison de droits, d’approvisionnement ou de configurations d’autorisation incorrectes. Pour résoudre ces problèmes, commencez par vérifier les droits, en assurant un approvisionnement correct et en examinant les autorisations. Si le problème persiste, escaladez le dossier et contactez les équipes d’assistance pour obtenir une résolution complète.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26333){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

En savoir plus sur l&#39;activité **Mettre à jour le profil** dans parcours [sur cette page](../building-journeys/update-profiles.md).

Consultez également la [documentation du profil Adobe Real-Time CDP](https://experienceleague.adobe.com/en/docs/experience-platform/profile/ui/user-guide?lang=en#profile-detail){target="_blank"}.

+++

+++ Pourquoi le nombre de profils engageables a-t-il augmenté de manière significative en une courte période ? 

La mesure **Profils engageables** reflète le nombre de profils uniques engagés par des parcours ou des campagnes au cours des 12 derniers mois. Une augmentation soudaine peut résulter du ciblage d’audiences importantes ou de modifications dans les jeux de données. Pour gérer cela, révisez la **logique de comptage des profils**, explorez les parcours ciblant les audiences volumineuses, **filtrez les audiences** au niveau du parcours, réduisez la **taille d’audience adressable** et surveillez **les modifications apportées au jeu de données**.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26161){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

Surveillez l’utilisation de la licence et les profils engageables de votre entreprise à l’aide du [ Tableau de bord d’utilisation de la licence ](../audience/license-usage.md)

Consultez également la présentation de [Adobe Experience Platform Query Service](https://experienceleague.adobe.com/en/docs/experience-platform/query/home?lang=en){target="_blank"}.

+++

+++ Pourquoi les e-mails envoyés à des personnes en dehors de l’audience prévue sont-ils basés sur des fonctions de date ?

Les e-mails peuvent être envoyés aux destinataires qui **ne répondent pas aux critères d’audience spécifiés**. Par exemple, les membres dont la date de remboursement est **avant le 4 juillet 2025** peuvent recevoir des e-mails destinés uniquement à ceux postérieurs à cette date. Ce comportement peut résulter d’une **segmentation d’audience mal configurée** ou **de modifications inattendues de la logique de qualification du profil**.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26173){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

En savoir plus sur les fonctions de date [sur cette page](../../rp_landing_pages/date-landing-page.md).

+++

+++ Comment résoudre les problèmes de sélection d’audience et les erreurs Chrome lors de l’enregistrement de parcours ?

L’ajout d’audiences à des conditions de parcours peut parfois entraîner des **plantages de l’application** ou afficher une erreur **Aw Snap** dans Chrome, y compris des erreurs lors de l’enregistrement des parcours. Ces problèmes sont souvent liés aux **services Chromium**. Pour les résoudre, appliquez une **mise à jour du navigateur** ou utilisez une **solution de contournement** appropriée.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26145){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

+++

## Parcours {#ajo-troubleshooting-journeys}

Pour les Parcours, reportez-vous aux sections de dépannage suivantes :

* [Résolution des erreurs avant de tester votre parcours ](../building-journeys/troubleshooting.md)
* [Résolution des problèmes liés aux actions entrantes dans les parcours](../building-journeys/troubleshooting-inbound.md)
* [Résolution des problèmes liés à l’exécution de votre parcours dynamique](../building-journeys/troubleshooting-execution.md)
* [Résoudre les problèmes liés aux actions personnalisées](../action/troubleshoot-custom-action.md)



+++ Pourquoi les expressions sont-elles perdues lors de la création d’une version de parcours ?  

Lors de la création d’une nouvelle version d’un parcours, les expressions **expressions d’étapes spécifiques** peuvent être perdues, ce qui entraîne des erreurs et nécessite une rentrée manuelle. Pour résoudre ce problème, **dupliquez le parcours**, testez la reproductibilité, **évitez les rechargements du navigateur** et utilisez la zone de travail **mise à jour** pour les parcours plus anciens.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26152){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

Découvrez comment dupliquer un parcours [sur cette page](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ Pourquoi les profils quittent-ils les parcours prématurément ? 

Les profils peuvent quitter un parcours de manière inattendue sans passer par un nœud désigné lorsque le **statut de vérification des commentaires** des messages envoyés est mal configuré. Pour résoudre ce problème, consultez la **logique de condition**, implémentez **logique alternative** ou consultez votre **équipe d’implémentation**.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26127){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

Consultez également les [directives de conception de Parcours ](../building-journeys/using-the-journey-designer.md).

+++


+++ Pourquoi les profils quittent-ils les parcours de manière inattendue ?

Les profils peuvent quitter un parcours de manière inattendue lorsque la **limitation d’événement** se produit, ce qui entraîne l’abandon de certains profils si le nombre d’événements traités dépasse la capacité du système. Pour réduire les sorties de profil, comprenez les **limites du système**, surveillez les **pics d’événement** et optimisez le **flux de données** pour éviter de dépasser les seuils.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26018){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

Consultez également la section Mécanismes de sécurisation de Parcours [&#128279;](../start/guardrails.md#journey-guardrails).

+++


+++ Pourquoi mon événement ne déclenche-t-il pas le parcours prévu ?  

Les événements peuvent ne pas déclencher de parcours même si tous les critères sont satisfaits lorsqu’ils sont **créés par le biais de query services** plutôt que d’être diffusés en continu vers le **Data Collection Core Service (DCCS)**. Pour résoudre ce problème, passez en revue la configuration de l’événement, assurez-vous que les événements sont **diffusés directement sur DCCS** et vérifiez les fonctionnalités à l’aide du **mode test**.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26031){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

En savoir plus sur les événements [sur cette page](../event/about-events.md).

Consultez également la section Mécanismes de sécurisation des événements de Parcours [&#128279;](../start/guardrails.md#events).

+++


+++ Comment résoudre les problèmes de déclencheur de parcours après les modifications d’audience dans Adobe Journey Optimizer ? 

Si un parcours cesse de se déclencher après des modifications apportées à son audience associée, telles que des modifications de la politique de fusion , vous pouvez rencontrer des flux interrompus. Pour résoudre ce problème, **dupliquez et republiez le parcours** avec les paramètres d’audience mis à jour afin de vous assurer que les déclencheurs fonctionnent correctement.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26224){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

Découvrez comment dupliquer un parcours [sur cette page](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ Pourquoi une action personnalisée appelant un point d’entrée tiers externe expire-t-elle ?

Des erreurs de délai d’expiration peuvent se produire lorsqu’une **action personnalisée** appelle un point d’entrée tiers externe. Pour résoudre ce problème, vérifiez que le point d’entrée **est accessible**, vérifiez **journaux du serveur**, assurez-vous qu’il n’y a **aucun blocage de la part d’Adobe**, mettez à jour les configurations de point d’entrée si nécessaire et **testez après les mises à jour**. Gardez également à l’esprit les spécifications de délai d’appel de l’API **&#x200B;**.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26156){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

Pour en savoir plus sur l’API de limitation du Parcours [consultez cette page](../configuration/throttling.md).

Consultez également la [documentation sur l’intégration à des systèmes externes](../configuration/external-systems.md).

+++

## Règles {#ajo-troubleshooting-rules}

+++ Pourquoi la liste déroulante Règles de limitation ne fonctionne-t-elle pas ?

Des problèmes liés à la liste déroulante **Règles de limitation** se produisent souvent lorsque les ensembles de règles sont **mal configurés** ou **inaccessibles**. Assurez-vous que tous les ensembles de règles sont correctement configurés et disponibles pour résoudre le problème.

Consultez [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26204){target="_blank"} pour en savoir plus.

Découvrez comment appliquer des règles de limitation [dans cette section](../conflict-prioritization/rule-sets.md).

+++

## Prise de décision {#ajo-troubleshooting-decisioning}

+++ Comment résoudre des problèmes lors de la création de collections d’offres ?

Les difficultés de création des collections d’offres se produisent souvent lorsque **catalogues n’ont pas été configurés** pour votre organisation. Pour résoudre ce problème, vérifiez que tous les catalogues requis sont correctement configurés avant de tenter de créer des collections d’offres.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26265){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

En savoir plus sur les collections d’offres [sur cette page](../offers/offer-library/creating-collections.md).

+++

+++ Pourquoi ne puis-je pas accéder à Offer Decisioning ?  

Lors de l’intégration d’Adobe Target à une application à l’aide de Adobe Journey Optimizer, l’option **Offer Decisioning** peut être inaccessible dans la configuration du flux de données. Cela se produit généralement en raison de **paramètres d’autorisation** ou **contraintes d’approvisionnement**. Pour résoudre ce problème, vérifiez les autorisations utilisateur et assurez-vous que l’approvisionnement nécessaire est en place.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26175){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

Pour en savoir plus sur les autorisations requises pour Offer Decisioning [consultez cette page](../offers/get-started/starting-offer-decisioning.md#granting-acess-to-decision-management).

+++



## Multilingue {#ajo-troubleshooting-multilingual}

+++ Comment résoudre ce problème `Message validation error (CJMMAS - 1069-500)` ?

Dans Adobe Journey Optimizer, une erreur de validation du message (CJMMAS - 1069-500) liée à la fonctionnalité multilingue empêche le passage des parcours en mode Test ou Publication.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26168){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

En savoir plus sur le contenu multilingue [sur cette page](../content-management/multilingual-gs.md).

+++


## Configuration {#ajo-troubleshooting-config}

+++ Comment activer TLS v1.3 pour les actions personnalisées ?  

Pour maintenir l’**intégrité et la sécurité des données** lors de la connexion à des systèmes tiers, assurez-vous que Transport Layer Security (**TLS**) v1.3 est activé pour vos actions personnalisées. Cela permet de protéger les communications et d’éviter les vulnérabilités de sécurité potentielles.


Consultez [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26223){target="_blank"} pour en savoir plus.

En savoir plus sur le contenu multilingue [sur cette page](../action/about-custom-action-configuration.md).

+++

+++ Pourquoi ne puis-je pas créer un tableau de bord directement à partir d’une requête dans Adobe Journey Optimizer ? 

Dans Adobe Journey Optimizer, les tableaux de bord ne peuvent pas être créés directement à partir de requêtes. Pour créer des tableaux de bord, utilisez les fonctionnalités **création de tableaux de bord** disponibles dans Adobe Experience Platform, qui vous permettent de visualiser et d’analyser efficacement les données des requêtes.

Consultez [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26201){target="_blank"} pour en savoir plus.

+++

## API {#ajo-troubleshooting-apis}

+++ Comment résoudre les problèmes d’accès avec l’API Query Service ?  

Les erreurs d’accès lors de l’utilisation de l’**API Query Service** via Postman ou des outils similaires sont généralement dues à **des autorisations insuffisantes**. Pour résoudre ce problème, vérifiez les autorisations utilisateur, vérifiez les informations d’identification de l’API et fournissez des informations détaillées à la prise en charge d’si nécessaire.

Consultez [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26196){target="_blank"} pour en savoir plus.

Consultez également la [documentation sur la gestion des informations d’identification d’API](https://experienceleague.adobe.com/en/docs/experience-platform/access-control/abac/permissions-ui/permissions?lang=en#manage-api-credentials-for-role){target="_blank"}.

+++

