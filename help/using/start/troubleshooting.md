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
source-git-commit: 3ab8957d0aec6f30853de5537e03f0e7bec2017c
workflow-type: tm+mt
source-wordcount: '1663'
ht-degree: 2%

---

# Résolution des problèmes {#ajo-troubleshooting}


Voici une liste d’articles de dépannage pour Adobe Journey Optimizer. Chaque section de dépannage fournit des réponses aux questions les plus fréquemment posées ainsi que des solutions aux problèmes.

Voir aussi la [FAQ Adobe Experience Platform et la documentation de dépannage](https://experienceleague.adobe.com/en/docs/experience-platform/landing/troubleshooting#service-troubleshooting-directory){target="_blank"}.

## Canal e-mail {#ajo-troubleshooting-email}

### Conception d’e-mail {#ajo-troubleshooting-design}

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

+++ Pourquoi les modèles d’e-mail et le contenu disparaissent-ils des parcours dépubliés ?

Lors de la modification de modèles d’e-mail dans un parcours dépublié, le contenu et les modèles de certains e-mails peuvent disparaître de manière inattendue. Cela peut entraîner des reprises et des retards. Pour réduire le risque de ce problème, évitez les modifications simultanées, limitez le nombre d’onglets ouverts et enregistrez fréquemment les modifications.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"} pour savoir comment résoudre ce problème.

En savoir plus sur les modèles [sur cette page](../email/use-email-templates.md).

+++

+++ Un profil peut-il avoir plusieurs jetons push dans Adobe Journey Optimizer ?

Lors de l’implémentation de notifications push dans Journey Optimizer, un seul profil peut en effet avoir plusieurs jetons push associés à différents appareils. Lors d’une campagne de notification push, Journey Optimizer est conçu pour gérer ces jetons et s’assurer que le profil ciblé peut être atteint sur tous les appareils associés.

Consultez [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"} pour en savoir plus sur la gestion des jetons push.

En savoir plus sur la configuration des notifications push [sur cette page](../push/push-configuration.md).

+++

### Tracking et reporting des e-mails {#ajo-troubleshooting-tracking}

+++ Comment éviter les liens de tracking e-mail manquants dans les rapports ?

Le suivi des liens manquants dans Adobe Journey Optimizer se produit lorsque les URL d’e-mail utilisent des variables dynamiques et ne commencent pas par http, ou lorsque des instructions logiques sont placées dans le champ URL. Pour résoudre ce problème, assurez-vous que toutes les URL commencent par http, évitez d’utiliser la logique dans le champ URL et déplacez la logique de personnalisation complexe vers le contenu HTML ou les attributs prétraités.


Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26932){target="_blank"} pour savoir comment résoudre ce problème.

En savoir plus sur le tracking e-mail [sur cette page](../email/message-tracking.md).

+++

### Envoi d&#39;email {#ajo-troubleshooting-sending}

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

+++ Comment résoudre les problèmes de déclencheur de parcours après les modifications d’audience dans Adobe Journey Optimizer ? 

Si un parcours cesse de se déclencher après des modifications apportées à son audience associée, telles que des modifications apportées à la politique de fusion , vous pouvez rencontrer des flux de campagne interrompus. Pour résoudre ce problème, **dupliquez et republiez le parcours** avec les paramètres d’audience mis à jour afin de vous assurer que les déclencheurs fonctionnent correctement.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26224){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

Découvrez comment dupliquer un parcours [sur cette page](../building-journeys/journey-ui.md#duplicate-a-journey).

+++


## Parcours

### Événements

+++ Pourquoi mon événement ne déclenche-t-il pas le parcours prévu ?  

Les événements peuvent ne pas déclencher de parcours même si tous les critères sont satisfaits lorsqu’ils sont **créés par le biais de query services** plutôt que d’être diffusés en continu vers le **Data Collection Core Service (DCCS)**. Pour résoudre ce problème, passez en revue la configuration de l’événement, assurez-vous que les événements sont **diffusés directement sur DCCS** et vérifiez les fonctionnalités à l’aide du **mode test**.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26031){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

En savoir plus sur les événements [sur cette page](../event/about-events.md).

Consultez également la section Mécanismes de sécurisation des événements de Parcours [&#128279;](../start/guardrails.md#events).

+++

## Prise de décision {#ajo-troubleshooting-decisioning}

+++ Comment résoudre des problèmes lors de la création de collections d’offres ?

Les difficultés de création des collections d’offres se produisent souvent lorsque **catalogues n’ont pas été configurés** pour votre organisation. Pour résoudre ce problème, vérifiez que tous les catalogues requis sont correctement configurés avant de tenter de créer des collections d’offres.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26265){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

En savoir plus sur les collections d’offres [sur cette page](../offers/offer-library/creating-collections.md).

+++


## Multilingue {#ajo-troubleshooting-multilingual}

+++ Comment résoudre ce problème `Message validation error (CJMMAS - 1069-500)` ?

Dans Adobe Journey Optimizer, une erreur de validation du message (CJMMAS - 1069-500) liée à la fonctionnalité multilingue empêche le passage des parcours en mode Test ou Publication.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26168){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

En savoir plus sur le contenu multilingue [sur cette page](../content-management/multilingual-gs.md).

++


## Configuration {#ajo-troubleshooting-config}

### Sécurité {#ajo-troubleshooting-security}

+++ Comment activer TLS v1.3 pour les actions personnalisées ?  

Pour maintenir l’**intégrité et la sécurité des données** lors de la connexion à des systèmes tiers, assurez-vous que Transport Layer Security (**TLS**) v1.3 est activé pour vos actions personnalisées. Cela permet de protéger les communications et d’éviter les vulnérabilités de sécurité potentielles.


Consultez [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26223){target="_blank"} pour en savoir plus.

En savoir plus sur le contenu multilingue [sur cette page](../action/about-custom-action-configuration.md).

+++

### Tableaux de bord {#ajo-troubleshooting-dashboards}

+++ Pourquoi ne puis-je pas créer un tableau de bord directement à partir d’une requête dans Adobe Journey Optimizer ? 

Dans Adobe Journey Optimizer, les tableaux de bord ne peuvent pas être créés directement à partir de requêtes. Pour créer des tableaux de bord, utilisez les fonctionnalités **création de tableaux de bord** disponibles dans Adobe Experience Platform, qui vous permettent de visualiser et d’analyser efficacement les données des requêtes.

Consultez [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26201){target="_blank"} pour en savoir plus.

++