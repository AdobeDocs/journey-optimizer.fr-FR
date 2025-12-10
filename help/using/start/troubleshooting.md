---
solution: Journey Optimizer
product: journey optimizer
title: Articles sur la résolution des problèmes dans Journey Optimizer
description: Articles sur la résolution des problèmes dans Journey Optimizer
feature: Get Started, Monitoring
role: User
level: Intermediate
exl-id: f8acb987-5c6e-4545-93b9-fdfc0d74db57
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '2942'
ht-degree: 100%

---

# Articles sur la résolution des problèmes {#ajo-troubleshooting}

Voici une liste d’articles de résolution des problèmes pour Adobe Journey Optimizer. Chaque section de résolution des problèmes fournit des réponses aux questions fréquentes ainsi que des solutions aux problèmes.

Voir aussi les [Questions fréquentes sur Adobe Experience Platform et la documentation sur la résolution des problèmes](https://experienceleague.adobe.com/fr/docs/experience-platform/landing/troubleshooting){target="_blank"}.

## Canal e-mail {#ajo-troubleshooting-email}

+++ Comment éviter les problèmes de mise en forme des e-mails dans Adobe Journey Optimizer à l’aide des thèmes ?

Dans Adobe Journey Optimizer (AJO), la modification des blocs CSS par défaut dans l’en-tête de l’e-mail peut entraîner des problèmes de mise en forme inattendus, en particulier après la suppression de fragments de contenu. Ces problèmes sont plus visibles sur les appareils mobiles et peuvent entraîner des déformations de mise en page ou des incohérences de style. Pour éviter cela, utilisez la fonctionnalité Thèmes pour appliquer la feuille CSS personnalisée en toute sécurité sans modifier les styles CSS générés par le système.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-27252){target="_blank"} pour apprendre comment résoudre ce problème.

Pour en savoir plus sur la mise en forme des e-mails, consultez [cette page](../email/get-started-email-design.md).

+++


+++ Pourquoi les fragments contenant des champs modifiables ne fonctionnent-ils pas ?

Dans Adobe Journey Optimizer, les fragments contenant des champs modifiables peuvent ne pas se charger correctement ou se dupliquer de manière inattendue lorsque vous les ajoutez aux modèles. Le problème affecte généralement des fragments spécifiques dans différents environnements.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26908){target="_blank"} pour apprendre comment résoudre ce problème.

Pour en savoir plus sur les fragments personnalisables, consultez [cette page](../content-management/customizable-fragments.md).

+++

+++ Pourquoi les fragments HTML ne s’affichent-ils pas correctement dans les e-mails ?

Les fragments HTML peuvent ne pas s’afficher correctement dans les e-mails, apparaissant souvent sous la forme d’**ID de fragment** plutôt que de contenu réel. Contrairement aux fragments visuels, les fragments HTML nécessitent une configuration précise. Pour résoudre ce problème, suivez les bonnes pratiques relatives à l’utilisation des **fragments d’expression visuels et HTML** dans les campagnes par e-mail.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-25441){target="_blank"} pour apprendre comment résoudre ce problème.

Pour en savoir plus sur les fragments HTML, consultez [cette page](../content-management/fragments.md).

+++

+++ Pourquoi les modèles d’e-mail et le contenu disparaissent-ils des parcours dépubliés ?

Lors de la modification de modèles d’e-mail dans un parcours dépublié, le contenu et les modèles de certains e-mails peuvent disparaître de manière inattendue. Cela peut demander un travail supplémentaire et entraîner des retards. Pour réduire le risque de ce problème, évitez les modifications simultanées, limitez le nombre d’onglets ouverts et enregistrez fréquemment les modifications.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"} pour apprendre comment résoudre ce problème.

Pour en savoir plus sur les modèles, consultez [cette page](../email/use-email-templates.md).

+++

+++ Pourquoi le champ Pré-en-tête de l’e-mail ne s’affiche-t-il pas en mode « Coder votre propre contenu » ? 

En mode « **Coder votre propre contenu** » sous la fonction **Modifier le corps de l’e-mail**, le champ de saisie Pré-en-tête n’apparaît pas. Pour inclure le texte du pré-en-tête, les utilisateurs et les utilisatrices doivent **coder manuellement le pré-en-tête** dans leur contenu HTML personnalisé.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26174){target="_blank"} pour apprendre comment résoudre ce problème.

Pour en savoir plus sur la configuration du pré-en-tête des e-mails, consultez [cette page](../email/header-parameters.md).

+++

+++ Pourquoi y a-t-il une incohérence dans le comportement des liens lors de l’utilisation d’un composant HTML dans les modèles d’e-mail ?  

Lors de l’ajout d’un **composant HTML** à un modèle d’e-mail, les liens peuvent se comporter différemment selon le **client de messagerie**, le **mode d’affichage** ou l’**appareil/navigateur**. Par exemple, les liens d&#39;ancrage peuvent fonctionner différemment dans la **vue côte à côte d’Outlook** par rapport à la vue plein écran. Tenez compte de ces variations lors de la conception de modèles d’e-mail et testez-les sur plusieurs clients et appareils.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26221){target="_blank"} pour apprendre comment résoudre ce problème.

Consultez également la section relatives aux bonnes pratiques en matière de conception d’email [sur cette page](../email/get-started-email-design.md).

+++


+++ Comment éviter les liens de suivi des e-mails manquants dans les rapports ?

L’absence de suivi des liens dans Adobe Journey Optimizer se produit lorsque les URL des e-mails utilisent des variables dynamiques et ne commencent pas par http, ou lorsque des instructions logiques sont placées dans le champ de l’URL. Pour résoudre ce problème, assurez-vous que toutes les URL commencent par http, évitez d’utiliser une logique dans le champ de l’URL et déplacez la logique de personnalisation complexe vers le contenu HTML ou les attributs prétraités.


Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26932){target="_blank"} pour apprendre comment résoudre ce problème.

Pour en savoir plus sur le suivi des e-mails, consultez [cette page](../email/message-tracking.md).

+++

+++ Comment résoudre une erreur de serveur de messagerie lors de la configuration de campagnes par e-mail transactionnelles déclenchées par une API ? 

Une erreur de serveur de messagerie lors de la création d’une configuration de canal pour une campagne d’e-mail transactionnel déclenchée par une API dans Adobe Journey Optimizer peut être due à des **erreurs de configuration DNS** ou à des **limitations de la politique DMARC**. Pour résoudre ce problème, vérifiez que votre DNS est correctement configuré et que votre domaine est conforme aux exigences **DMARC (Domain-based Message Authentication, Reporting, and Conformance)**.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26200){target="_blank"} pour apprendre comment résoudre ce problème.

Pour en savoir pus sur les politiques DMARC, consultez [cette page](../configuration/dmarc-record-update.md).

Consultez également la [documentation sur les campagnes déclenchées par une API](../campaigns/api-triggered-campaigns.md).
+++

## Canal de notification push {#ajo-troubleshooting-push}

+++ Un profil peut-il avoir plusieurs jetons push dans Adobe Journey Optimizer ?

Lors de l’implémentation de notifications push dans Journey Optimizer, un seul profil peut en effet avoir plusieurs jetons push associés à différents appareils. Lors d’une campagne par notifications push, Journey Optimizer est conçu pour gérer ces jetons et s’assurer que le profil ciblé peut être atteint sur tous les appareils associés.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26738){target="_blank"} pour en savoir plus sur la gestion des jetons push.

Pour en savoir plus sur la configuration de notifications push, consultez [cette page](../push/push-configuration.md).

+++

+++ Pourquoi le fait de cliquer sur un message push ne me redirige-t-il pas vers l’URL web configurée ?  

Si les messages push ne redirigent pas vers l’URL web configurée, cela peut être dû à une erreur de configuration de l’action de clic ou à la désactivation des paramètres de notification push. Assurez-vous que l’**action de clic** du message push est correctement définie et que l’**affichage automatique et le suivi** des notifications push sont activés pour résoudre ce problème.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26226){target="_blank"} pour en savoir plus sur ce problème.

Pour en savoir plus sur la configuration de notifications push, consultez [cette page](../push/push-configuration.md).

+++


## Canal SMS {#ajo-troubleshooting-sms}

+++ Pourquoi mes SMS transactionnels ne sont-ils pas diffusés alors que le consentement est défini sur `marketing.sms.value=y` ?

Si une personne destinataire répond **STOP** à un SMS, tous les futurs messages de ce numéro court sont bloqués, y compris les messages transactionnels. Pour garantir une diffusion ininterrompue des SMS transactionnels, configurez-les et envoyez-les par le biais d’un **numéro court distinct** duquel les destinataires ne se sont pas désinscrits.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26258){target="_blank"} pour en savoir plus sur ce problème.

Pour en savoir plus sur la configuration de l’opt-out des SMS, consultez [cette page](../sms/sms-opt-out.md).

+++

## Canal in-app

+++ Pourquoi ne puis-je pas créer de rapports sur le canal in-app dans Customer Journey Analytics ?

Les difficultés liées à la création de rapports sur le **canal in-app** dans Adobe Customer Journey Analytics proviennent souvent d’une erreur de configuration des **vues de données**, des **jeux de données** ou des **mises à jour de schéma**. Vérifiez que ces configurations sont correctement appliquées pour résoudre le problème.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26206){target="_blank"} pour en savoir plus sur ce problème.

Découvrez comment intégrer des données d’analyse Journey Optimizer dans Customer Journey Analytics [sur cette page](https://experienceleague.adobe.com/fr/docs/analytics-platform/using/integrations/ajo#automatically-configure-journey-optimizer-integration){target="_blank"}.

Consultez également la [documentation sur les rapports complets de Journey Optimizer](../reports/report-gs-cja.md).

+++


## Gestion des données {#ajo-troubleshooting-data-management}

+++ Comment les paramètres de durée de vie (TTL) s’appliquent-ils aux jeux de données de profil et de lac de données lorsque vous créez un sandbox ?

Les organisations qui configurent de nouveaux sandbox dans Adobe Journey Optimizer se sont interrogées sur la manière dont les paramètres de durée de vie (TTL) s’appliquent aux jeux de données de profil et de lac de données. Cet article précise que les paramètres de durée de vie n’affectent pas les sandbox existants et sont automatiquement appliqués aux nouveaux sandbox uniquement.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"} pour savoir comment gérer la durée de vie.

Pour en savoir plus sur la durée de vie des jeux de données, consultez [cette page](../data/datasets-ttl.md).

+++


## Gestion des profils et de l’audience {#ajo-troubleshooting-audiences}

+++ Comment résoudre les incohérences des tailles d’audiences ?

Le nombre d’entrées traitées dans la fonctionnalité **Lecture d’audience** d’Adobe Journey Optimizer peut être inférieur à la taille d’audience attendue. Ce problème se produit souvent en raison d’erreurs de configuration d’espace de noms, ce qui entraîne l’exclusion de profils des parcours. La résolution implique la vérification et la correction des configurations d’espace de noms, la lecture de la documentation pertinente et l’ajustement des priorités pour garantir des opérations plus fluides dans Adobe Journey Optimizer.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26135){target="_blank"} pour apprendre comment résoudre ce problème.

Consultez également [cet article sur les tailles d’audiences obsolètes](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26166){target="_blank"}.

Pour en savoir plus sur l’activité **Lecture d’audience** dans les parcours, consultez [cette page](../building-journeys/read-audience.md).

+++

+++ Pourquoi les mises à jour de profil échouent-elles ?

Dans Adobe Journey Optimizer, certaines valeurs de champ peuvent ne pas se mettre à jour correctement après avoir exécuté une activité **Mettre à jour le profil** dans un parcours. Dans certains cas, les champs mis à jour peuvent disparaître ou revenir à leur état précédent. Pour résoudre ce problème, recherchez les règles ou conditions en conflit, vérifiez les paramètres des autorisations, utilisez un jeu de données unique pour l’activité **Mettre à jour le profil** et assurez-vous qu’aucun autre processus d’ingestion n’écrit sur le même profil en même temps.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26352){target="_blank"} pour apprendre comment résoudre ce problème.

Pour en savoir plus sur l’activité **Mettre à jour le parcours**, consultez [cette page](../building-journeys/update-profiles.md).

Consultez également la [documentation d’Adobe Experience Platform sur l’ingestion de données](https://experienceleague.adobe.com/fr/docs/experience-platform/ingestion/tutorials/ingest-batch-data#dataset-activity){target="_blank"}.

+++

+++ Pourquoi le nombre de profils rejoignant un parcours est-il différent de celui de l’audience associée ?

Cette incohérence peut se produire lorsque le parcours utilise l’instantané de profil d’un jour passé si celui du jour en cours n’est pas disponible au moment de l’exécution du parcours.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26253){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

Pour en savoir plus, consultez [cette publication de la communauté Journey Optimizer](https://experienceleaguecommunities.adobe.com/t5/real-time-customer-data-platform/profile-snapshot-and-segment-qualification-troubleshooting/ba-p/698998?profile.language=fr){target="_blank"}.

Consultez également la [documentation de l’API Schedules d’Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/segmentation/api/schedules){target="_blank"} pour savoir quand votre tâche quotidienne est planifiée.

+++

+++ Pourquoi le sélecteur d’audience affiche-t-il un nombre de profils différent dans les campagnes et les parcours ?

Vous remarquerez peut-être qu’une même audience affiche un nombre de profils différent dans les campagnes et les parcours. Cela se produit, car chaque fonctionnalité utilise des API différentes pour récupérer les données d’audience, qui peuvent renvoyer des valeurs différentes.

Il s’agit d’un comportement attendu qui n’a aucune incidence sur l’exécution de votre campagne. Les profils corrects seront toujours ciblés. Pour vérifier la taille réelle de l’audience, accédez à **[!UICONTROL Client ou cliente]** > **[!UICONTROL Audiences]** et sélectionnez votre audience.

+++


+++ Comment résoudre les problèmes de population d’audience ?

Des problèmes de population d’audience peuvent survenir lorsqu’il manque des composants ou des ressources, souvent en raison d’erreur de droits, d’approvisionnement ou de configuration des autorisations. Pour résoudre ces problèmes, commencez par vérifier les droits, l’approvisionnement et les autorisations. Si le problème persiste, faites-le remonter et contactez les équipes d’assistance pour une résolution complète.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26333){target="_blank"} pour apprendre comment résoudre ce problème.

Pour en savoir plus sur l’activité **Mettre à jour le parcours**, consultez [cette page](../building-journeys/update-profiles.md).

Consultez également la [documentation du profil Adobe Real-Time CDP](https://experienceleague.adobe.com/fr/docs/experience-platform/profile/ui/user-guide#profile-detail){target="_blank"}.

+++

+++ Pourquoi le nombre de profils engageables a-t-il augmenté de manière significative en peu de temps ? 

La mesure **Profils engageables** reflète le nombre de profils uniques engagés par des parcours ou des campagnes au cours des 12 derniers mois. Une augmentation soudaine peut résulter du ciblage d’audiences importantes ou de modifications dans les jeux de données. Pour gérer ces hausses, vérifiez la **logique de comptage des profils**, explorez les parcours ciblant des audiences importantes, **filtrez les audiences** au niveau du parcours, réduisez la **taille d’audience adressable** et surveillez les **modifications apportées au jeu de données**.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26161){target="_blank"} pour apprendre comment résoudre ce problème.

Surveillez l’utilisation des licences et les profils engageables de votre organisation à l’aide du [tableau de bord d’utilisation des licences.](../audience/license-usage.md)

Consultez également la [présentation du service de requête Adobe Experience Platform](https://experienceleague.adobe.com/fr/docs/experience-platform/query/home){target="_blank"}.

+++

+++ Pourquoi les e-mails envoyés à des personnes en dehors de l’audience ciblée sont-ils basés sur des fonctions de date ?

Les e-mails peuvent être envoyés à des destinataires qui **ne répondent pas aux critères d’audience spécifiés**. Par exemple, les personnes membres dont la date de rachat est **antérieure au 4 juillet 2025** peuvent recevoir des e-mails destinés uniquement à celles dont la date est postérieure à cette date. Ce comportement peut résulter d’une **erreur de segmentation d’audience** ou de **modifications inattendues de la logique de qualification des profils**.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26173){target="_blank"} pour apprendre comment résoudre ce problème.

Pour en savoir plus sur les fonctions de date, consultez [cette page](../building-journeys/functions/date-functions.md).

+++

+++ Pourquoi la somme Exclusions + Diffusés dépasse-t-elle ma taille d’audience ciblée dans les rapports de campagne ?

Dans les rapports de campagne, vous remarquerez peut-être que la somme des **Diffusés** et **Exclusions** dépasse la taille de l’audience ciblée d’origine. Cela se produit, car la mesure **Exclusions** comptabilise tous les événements d’exclusion, y compris les événements d’exclusion en double pour un même profil. Si un profil est exclu plusieurs fois au cours d’une campagne, chaque événement est comptabilisé séparément.

**Exemple** : une campagne ciblant 94 000 profils affiche 69 000 diffusions et 37 000 exclusions, pour un total de 106 000, ce qui dépasse les 94 000 profils ciblés d’origine. C’est un comportement normal.

Pour comprendre la différence entre les événements d’exclusion totale et les exclusions de profil uniques, reportez-vous à l’[explication du comptage des exclusions](../reports/exclusion-list.md#exclusion-list).

En savoir plus sur les [rapports de campagne](../reports/campaign-global-report-cja.md) et les [mesures de rapport](../reports/global-report-components-cja.md).

+++

+++ Comment résoudre les problèmes de sélection d’audience et les erreurs Chrome lors de l’enregistrement des parcours ?

L’ajout d’audiences à des conditions de parcours peut parfois entraîner des **blocages de l’application** ou afficher une **erreur « Aw Snap! »** dans Chrome, y compris des erreurs lors de l’enregistrement des parcours. Ces problèmes sont souvent liés aux **services Chromium**. Pour les résoudre, effectuez une **mise à jour du navigateur** ou utilisez une **solution de contournement** appropriée.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26145){target="_blank"} pour apprendre comment résoudre ce problème.

+++

## Parcours {#ajo-troubleshooting-journeys}

Pour les parcours, reportez-vous aux sections de résolution des problèmes suivantes :

* [Résoudre les erreurs avant de tester votre parcours](../building-journeys/troubleshooting.md)
* [Résoudre les problèmes liés aux actions entrantes dans les parcours](../building-journeys/troubleshooting-inbound.md)
* [Résoudre les problèmes d’exécution de votre parcours actif](../building-journeys/troubleshooting-execution.md)
* [Résoudre les problèmes liés aux actions personnalisées](../action/troubleshoot-custom-action.md)


+++ Pourquoi les expressions disparaissent-elles lors de la création d’une version de parcours ?  

Lors de la création de la version d’un parcours, les **expressions d’étapes spécifiques** peuvent être perdues, ce qui entraîne des erreurs et nécessite une nouvelle saisie manuelle. Pour résoudre ce problème, **dupliquez le parcours**, testez la reproductibilité, **évitez les rechargements du navigateur** et utilisez la **zone de travail mise à jour** pour les parcours plus anciens.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26152){target="_blank"} pour apprendre comment résoudre ce problème.

Découvrez comment dupliquer un parcours [sur cette page](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ Pourquoi les profils quittent-ils prématurément des parcours ? 

Les profils peuvent quitter un parcours de manière inattendue sans passer par un nœud désigné lorsque la **condition utilisée pour vérifier le statut du restours** des messages envoyés est mal configurée. Pour résoudre ce problème, examinez la **logique de condition**, implémentez une **autre logique** ou consultez votre **équipe d’implémentation**.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26127){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

Consultez également les [directives de conception de parcours](../building-journeys/using-the-journey-designer.md).

+++


+++ Pourquoi les profils quittent-ils les parcours de manière inattendue ?

Les profils peuvent quitter un parcours de manière inattendue lorsque la **limitation d’événement** se produit, ce qui entraîne l’abandon de certains profils si le nombre d’événements traités dépasse la capacité du système. Pour réduire les sorties de profil, comprenez les **limites du système**, surveillez les **pics d’événement** et optimisez le **flux de données** pour éviter de dépasser les seuils.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26018){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

Consultez également la section [Mécanismes de sécurisation de parcours](../start/guardrails.md#decisioning-guardrails).

+++


+++ Pourquoi mon événement ne déclenche-t-il pas le parcours prévu ?  

Les événements peuvent ne pas déclencher de parcours même si tous les critères sont remplis lorsqu’ils sont **créés par le biais des services de requête** plutôt que d’être diffusés en streaming vers **Data Collection Core Service (DCCS)**. Pour résoudre ce problème, vérifiez la configuration de l’événement, assurez-vous que les événements sont **envoyés directement à DCCS** et effectuez une vérification à l’aide du **mode test**.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26031){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

Apprenez-en plus sur les événements [sur cette page](../event/about-events.md).

Consultez également la section [Mécanismes de sécurisation des événements de parcours](../start/guardrails.md#events-g).

+++


+++ Comment résoudre les problèmes de déclenchement de parcours après modification de l’audience dans Adobe Journey Optimizer ? 

Si un parcours cesse de se déclencher après des modifications apportées à l’audience associée, telles que la modification de la politique de fusion, vous pouvez rencontrer des flux interrompus. Pour résoudre ce problème, **dupliquez et republiez le parcours** avec les paramètres d’audience mis à jour afin de vous assurer que les déclencheurs fonctionnent correctement.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26224){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

Découvrez comment dupliquer un parcours sur [cette page](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ Pourquoi une action personnalisée qui appelle un point d’entrée tiers externe expire-t-elle ?

Des erreurs de dépassement de délai d’expiration peuvent se produire lorsqu’une **action personnalisée** appelle un point d’entrée tiers externe. Pour résoudre ce problème, vérifiez que le **point d’entrée est accessible**, consultez les **journaux du serveur**, assurez-vous qu’il n’y a **aucun blocage de la part d’Adobe**, mettez à jour les configurations des points d’entrée si nécessaire et **exécutez un test une fois les mises à jour effectuées**. Notez également les **spécifications concernant les délais d’expiration pour les appels API**.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26156){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

Pour en savoir plus sur l’API Journey Throttling, consultez [cette page](../configuration/throttling.md).

Consultez également la [documentation sur l’intégration à des systèmes externes](../configuration/external-systems.md).

+++

+++ Que devez-vous faire si vous rencontrez une erreur 403 avec le message **accès_invalide** ou **Aucun accès à ce dataId=XX accordé** lors de la publication d’une audience à partir d’une flèche ?

Pour résoudre cette erreur, demandez à votre administrateur ou administratrice de vérifier que votre profil utilisateur a accès aux vues de données requises pour la publication d’audience, puis essayez de republier l’audience.

Reportez-vous à [la documentation sur les autorisations](../administration/permissions.md){target="_blank"} pour savoir comment résoudre ce problème.

+++

## Règles {#ajo-troubleshooting-rules}

+++ Pourquoi la liste déroulante Règles de limitation ne fonctionne-t-elle pas ?

Les problèmes liés à la liste déroulante **Règles de limitation** se produisent souvent lorsque les jeux de règles sont **mal configurés** ou **inaccessibles**. Vérifiez que tous les jeux de règles sont correctement configurés et disponibles pour résoudre le problème.

Consultez [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26204){target="_blank"} pour en savoir plus.

Découvrez comment appliquer des règles de limitation dans [cette section](../conflict-prioritization/rule-sets.md).

+++

## Prise de décision {#ajo-troubleshooting-decisioning}

+++ Comment résoudre les problèmes qui se produisent lors de la création de collections d’offres ?

Lors de la création de collections d’offres, des problèmes se produisent souvent lorsque les **catalogues n’ont pas été approvisionnés** pour votre organisation. Pour résoudre ce problème, vérifiez que tous les catalogues requis sont correctement approvisionnés avant de tenter de créer des collections d’offres.

Reportez-vous à [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26265){target="_blank"} pour apprendre comment résoudre ce problème.

Pour en savoir plus sur les collections d’offres, consultez [cette page](../offers/offer-library/creating-collections.md).

+++

+++ Pourquoi ne puis-je pas accéder à Offer Decisioning ?  

Lors de l’intégration d’Adobe Target à une application à l’aide d’Adobe Journey Optimizer, l’option **Offer Decisioning** peut être inaccessible dans la configuration du train de données. Cela se produit généralement en raison des **paramètres des autorisations** ou de **contraintes d’approvisionnement**. Pour résoudre ce problème, vérifiez les autorisations utilisateur et assurez-vous que l’approvisionnement nécessaire est présent.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26175){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

Pour en savoir plus sur les autorisations requises pour Offer Decisioning, consultez [cette page](../offers/get-started/starting-offer-decisioning.md#granting-acess-to-decision-management).

+++



## Multilingue {#ajo-troubleshooting-multilingual}

+++ Comment résoudre ce problème `Message validation error (CJMMAS - 1069-500)` ?

Dans Adobe Journey Optimizer, une erreur de validation de message (CJMMAS - 1069-500) liée à la fonctionnalité multilingue empêche les parcours d’être définis sur Mode de test ou Publié.

Reportez-vous à [cet article de dépannage](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26168){target="_blank"} pour découvrir les étapes à suivre pour résoudre ce problème.

Pour en savoir plus sur le contenu multilingue, consultez [cette page](../content-management/multilingual-gs.md).

+++


## Configuration {#ajo-troubleshooting-config}

+++ Comment activer TLS v1.3 pour les actions personnalisées ?  

Pour maintenir l’**intégrité et la sécurité des données** lors de la connexion à des systèmes tiers, assurez-vous que le protocole TLS (**Transport Layer Security**) v1.3 est activé pour vos actions personnalisées. Cela permet de protéger les communications et d’éviter des vulnérabilités de sécurité potentielles.


Consultez [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26223){target="_blank"} pour en savoir plus.

Pour en savoir plus sur le contenu multilingue, consultez [cette page](../action/about-custom-action-configuration.md).

+++

+++ Pourquoi est-il impossible de créer un tableau de bord directement à partir d’une requête dans Adobe Journey Optimizer ? 

Dans Adobe Journey Optimizer, les tableaux de bord ne peuvent pas être créés directement à partir des requêtes. Pour créer des tableaux de bord, utilisez les fonctionnalités de **création de tableaux de bord** disponibles dans Adobe Experience Platform, qui vous permettent de visualiser et d’analyser efficacement les données des requêtes.

Consultez [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26201){target="_blank"} pour en savoir plus.

+++

## API {#ajo-troubleshooting-apis}

+++ Comment résoudre les problèmes d’accès avec l’API Query Service ?  

Les erreurs d’accès lors de l’utilisation de l’**API Query Service** via Postman ou des outils similaires sont généralement dues à des **autorisations insuffisantes**. Pour résoudre ce problème, vérifiez les autorisations utilisateur et les informations d’identification de l’API et fournissez des informations détaillées au service d’assistance si nécessaire.

Consultez [cet article](https://experienceleague.adobe.com/fr/docs/experience-cloud-kcs/kbarticles/ka-26196){target="_blank"} pour en savoir plus.

Consultez également la [documentation sur la gestion des informations d’identification des API](https://experienceleague.adobe.com/fr/docs/experience-platform/access-control/abac/permissions-ui/permissions#manage-api-credentials-for-role){target="_blank"}.

+++
