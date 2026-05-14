---
solution: Journey Optimizer
product: journey optimizer
title: Articles sur la résolution des problèmes dans Journey Optimizer
description: Articles sur la résolution des problèmes dans Journey Optimizer
feature: Get Started, Monitoring
role: User
level: Intermediate
exl-id: f8acb987-5c6e-4545-93b9-fdfc0d74db57
TQID: https://experienceleague.adobe.com/-E1vLZQv8dDZqejyh944at7jHheePuzXybU4lCyMris
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: fe338112-e2ce-4876-8989-fc4d497613f1id: fe96aceb-8194-4a8a-a6b0-75302d02804d
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: c2beecbb-b93e-4ae3-baa9-72adcdc06781id: d08afb72-92f6-4856-88e3-11ec34313c2fid: d2e8a157-b3b0-4143-9ff3-809bf400be56id: ee5bb250-0884-4d71-86eb-d8489e8bcaddid: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: aa2f3246-cb95-4b30-8899-fdf7d73550ccid: b5ce8718-c3af-4fdb-a1a9-fca32f83a87cid: c1579802-ddd4-4214-8a91-97b2066abe11id: d095671a-1355-40aa-8b5f-06c33c68080bid: d3cdead0-685a-4489-9250-4bb709942f66id: e0eb8757-182f-49f3-94a4-1587d16f5094id: ebde5b41-29c9-4f5e-9ef6-1197e85409e3id: ff2b9b37-92e0-45fc-b853-379d44c08c89
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 4714
ht-degree: 48%

---

# Questions fréquentes sur la résolution des problèmes {#ajo-troubleshooting}

Voici une liste d’articles de résolution des problèmes pour Adobe Journey Optimizer. Chaque section de résolution des problèmes fournit des réponses aux questions fréquentes ainsi que des solutions aux problèmes.

Lorsque vous contactez l’assistance Adobe pour des problèmes non résolus, incluez les détails de l’environnement, le niveau d’impact, les étapes de réplication, les journaux ou captures d’écran et les identifiants pertinents. [Découvrez les éléments à inclure dans les tickets d’assistance](user-interface.md#support-ticket-guidelines).

## Canal E-mail {#ajo-troubleshooting-email}

+++ Comment éviter les problèmes de mise en forme des e-mails dans Adobe Journey Optimizer à l’aide des thèmes ?

Dans Adobe Journey Optimizer (AJO), la modification des blocs CSS par défaut dans l’en-tête de l’e-mail peut entraîner des problèmes de mise en forme inattendus, en particulier après la suppression de fragments de contenu. Ces problèmes sont plus visibles sur les appareils mobiles et peuvent entraîner des déformations de mise en page ou des incohérences de style. Pour éviter cela, utilisez la fonctionnalité Thèmes pour appliquer la feuille CSS personnalisée en toute sécurité sans modifier les styles CSS générés par le système.

Pour en savoir plus sur la mise en forme des e-mails, consultez [cette page](../email/get-started-email-design.md).

+++


+++ Pourquoi les fragments contenant des champs modifiables ne fonctionnent-ils pas ?

Dans Adobe Journey Optimizer, les fragments contenant des champs modifiables peuvent ne pas se charger correctement ou se dupliquer de manière inattendue lorsque vous les ajoutez aux modèles. Le problème affecte généralement des fragments spécifiques dans différents environnements. Pour résoudre ce problème, vérifiez la configuration du fragment, recherchez les définitions de champ modifiable en conflit et testez-les dans un sandbox de développement avant de republier.

Pour en savoir plus sur les fragments personnalisables, consultez [cette page](../content-management/customizable-fragments.md).

+++

+++ Pourquoi les fragments HTML ne s’affichent-ils pas correctement dans les e-mails ?

Les fragments HTML peuvent ne pas s’afficher correctement dans les e-mails, apparaissant souvent sous la forme d’**ID de fragment** plutôt que de contenu réel. Contrairement aux fragments visuels, les fragments HTML nécessitent une configuration précise. Pour résoudre ce problème, suivez les bonnes pratiques relatives à l’utilisation des **fragments d’expression visuels et HTML** dans les campagnes par e-mail.

Pour en savoir plus sur les fragments HTML, consultez [cette page](../content-management/fragments.md).

+++

+++ Pourquoi les modèles d’e-mail et le contenu disparaissent-ils des parcours dépubliés ?

Lors de la modification de modèles d’e-mail dans un parcours dépublié, le contenu et les modèles de certains e-mails peuvent disparaître de manière inattendue. Cela peut demander un travail supplémentaire et entraîner des retards. Pour réduire le risque de ce problème, évitez les modifications simultanées, limitez le nombre d’onglets ouverts et enregistrez fréquemment les modifications.

Pour en savoir plus sur les modèles, consultez [cette page](../email/use-email-templates.md).

+++

+++ Pourquoi le champ Pré-en-tête de l’e-mail ne s’affiche-t-il pas en mode « Coder votre propre contenu » ? 

En mode « **Coder votre propre contenu** » sous la fonction **Modifier le corps de l’e-mail**, le champ de saisie Pré-en-tête n’apparaît pas. Pour inclure le texte du pré-en-tête, les utilisateurs et les utilisatrices doivent **coder manuellement le pré-en-tête** dans leur contenu HTML personnalisé.

Pour en savoir plus sur la configuration du pré-en-tête des e-mails, consultez [cette page](../email/header-parameters.md).

+++

+++ Pourquoi y a-t-il une incohérence dans le comportement des liens lors de l’utilisation d’un composant HTML dans les modèles d’e-mail ?  

Lors de l’ajout d’un **composant HTML** à un modèle d’e-mail, les liens peuvent se comporter différemment selon le **client de messagerie**, le **mode d’affichage** ou l’**appareil/navigateur**. Par exemple, les liens d&#39;ancrage peuvent fonctionner différemment dans la **vue côte à côte d’Outlook** par rapport à la vue plein écran. Tenez compte de ces variations lors de la conception de modèles d’e-mail et testez-les sur plusieurs clients et appareils.

Consultez également la section relatives aux bonnes pratiques en matière de conception d’email [sur cette page](../email/get-started-email-design.md).

+++


+++ Comment éviter les liens de suivi des e-mails manquants dans les rapports ?

L’absence de suivi des liens dans Adobe Journey Optimizer se produit lorsque les URL des e-mails utilisent des variables dynamiques et ne commencent pas par http, ou lorsque des instructions logiques sont placées dans le champ de l’URL. Pour résoudre ce problème, assurez-vous que toutes les URL commencent par http, évitez d’utiliser une logique dans le champ de l’URL et déplacez la logique de personnalisation complexe vers le contenu HTML ou les attributs prétraités.

Pour en savoir plus sur le suivi des e-mails, consultez [cette page](../email/message-tracking.md).

+++

+++ Comment résoudre une erreur de serveur de messagerie lors de la configuration de campagnes par e-mail transactionnelles déclenchées par une API ? 

Une erreur de serveur de messagerie lors de la création d’une configuration de canal pour une campagne d’e-mail transactionnel déclenchée par une API dans Adobe Journey Optimizer peut être due à des **erreurs de configuration DNS** ou à des **limitations de la politique DMARC**. Pour résoudre ce problème, vérifiez que votre DNS est correctement configuré et que votre domaine est conforme aux exigences **DMARC (Domain-based Message Authentication, Reporting, and Conformance)**.

Pour en savoir pus sur les politiques DMARC, consultez [cette page](../configuration/dmarc-record-update.md).

Consultez également la [documentation sur les campagnes déclenchées par une API](../campaigns/api-triggered-campaigns.md).
+++

## Canal de notification push {#ajo-troubleshooting-push}

+++ Un profil peut-il avoir plusieurs jetons push dans Adobe Journey Optimizer ?

Lors de l’implémentation de notifications push dans Journey Optimizer, un seul profil peut en effet avoir plusieurs jetons push associés à différents appareils. Lors d’une campagne par notifications push, Journey Optimizer est conçu pour gérer ces jetons et s’assurer que le profil ciblé peut être atteint sur tous les appareils associés.

Pour en savoir plus sur la configuration de notifications push, consultez [cette page](../push/push-configuration.md).

Consultez également la section [flux de données des notifications push](../push/push-gs.md) pour comprendre comment les jetons sont enregistrés et gérés de bout en bout.

+++

+++ Pourquoi le fait de cliquer sur un message push ne me redirige-t-il pas vers l’URL web configurée ?  

Si les messages push ne redirigent pas vers l’URL web configurée, cela peut être dû à une erreur de configuration de l’action de clic ou à la désactivation des paramètres de notification push. Assurez-vous que l’**action de clic** du message push est correctement définie et que l’**affichage automatique et le suivi** des notifications push sont activés pour résoudre ce problème.

Pour en savoir plus sur la configuration de notifications push, consultez [cette page](../push/push-configuration.md).

+++

+++ Pourquoi les notifications push échouent-elles après la mise à jour des informations d’identification de l’application ?

Les informations d’identification push expirées ou mal configurées (un certificat APNs pour iOS ou une clé FCM pour Android, par exemple) entraînent des échecs de diffusion silencieux. Journey Optimizer ne peut pas envoyer de notifications si les informations d’identification stockées dans la configuration du canal push ne correspondent plus à celles enregistrées sur la plateforme de l’appareil. Mettez à jour les informations d’identification dans la configuration du canal push et vérifiez que la surface de l’application mobile associée est republiée.

Découvrez comment configurer les informations d’identification push [sur cette page](../push/push-gs.md).

Consultez également la [documentation sur la configuration du canal push](../push/push-configuration.md).

+++


## Canal SMS {#ajo-troubleshooting-sms}

+++ Pourquoi mes SMS transactionnels ne sont-ils pas diffusés alors que le consentement est défini sur `marketing.sms.value=y` ?

Si une personne destinataire répond **STOP** à un SMS, tous les futurs messages de ce numéro court sont bloqués, y compris les messages transactionnels. Pour garantir une diffusion ininterrompue des SMS transactionnels, configurez-les et envoyez-les par le biais d’un **numéro court distinct** duquel les destinataires ne se sont pas désinscrits.

Pour en savoir plus sur la configuration de l’opt-out des SMS, consultez [cette page](../sms/sms-opt-out.md).

+++

+++ Pourquoi la diffusion SMS échoue-t-elle même si le canal est configuré ?

Les échecs de diffusion SMS après la configuration du canal sont le plus souvent causés par des informations d’identification d’API de fournisseur incorrectes, une incohérence entre l’ID d’expéditeur et ce que le fournisseur a enregistré, ou des restrictions de routage au niveau du fournisseur. Vérifiez que la clé API, le mot de passe et les détails de l’expéditeur saisis dans Journey Optimizer correspondent exactement à ce que votre fournisseur SMS a configuré. Envoyez ensuite un message de test pour confirmer la connectivité avant de lancer une campagne.

Découvrez comment configurer votre fournisseur SMS [sur cette page](../sms/sms-configuration.md).

+++

+++ Comment puis-je vérifier qu’un profil s’est opposé aux communications SMS ?

Lorsqu’un profil envoie un SMS à STOP, Journey Optimizer met à jour l’attribut de consentement SMS du profil. Pour vérifier le statut de désinscription actuel, ouvrez le profil dans l’interface utilisateur d’Experience Platform et examinez les champs de consentement sous **Confidentialité** > **Consentements**. Pour la résolution des problèmes de campagne, vérifiez également les raisons d’exclusion dans le rapport de campagne - les profils désinscrits apparaissent sous le nombre **Exclus** avec le motif « Désinscrit ».

En savoir plus sur la gestion des désinscriptions aux SMS [sur cette page](../sms/sms-opt-out.md).

+++

## Canal in-app {#ajo-troubleshooting-inapp}

+++ Pourquoi ne puis-je pas créer de rapports sur le canal in-app dans Customer Journey Analytics ?

Les difficultés liées à la création de rapports sur le **canal in-app** dans Adobe Customer Journey Analytics proviennent souvent d’une erreur de configuration des **vues de données**, des **jeux de données** ou des **mises à jour de schéma**. Vérifiez que ces configurations sont correctement appliquées pour résoudre le problème.

Consultez également la documentation sur les rapports à tout moment de [](../reports/report-gs-cja.md).

+++

+++ Pourquoi mon message in-app ne s’affiche-t-il pas pour les utilisateurs et utilisatrices ?

Les messages in-app nécessitent que Adobe Experience Platform Mobile SDK soit correctement installé et que l’extension de messagerie soit enregistrée dans votre application. Si le message n’apparaît pas, vérifiez que le SDK est initialisé avant que l’application ne tente de récupérer les messages in-app, que la surface d’application correcte (identifiant de bundle) est configurée dans Journey Optimizer et que la campagne a le statut **En ligne**. Vérifiez également que le profil répond aux critères d’audience et n’a pas déjà été limité par une règle de fréquence.

Découvrez comment configurer le canal in-app [sur cette page](../in-app/inapp-configuration.md).

+++

+++ Pourquoi ma campagne in-app ne se déclenche-t-elle pas sur l’événement attendu ?

Les campagnes in-app se déclenchent en fonction des noms d’événement qui doivent correspondre exactement entre l’implémentation SDK de votre application et la condition de déclencheur définie dans Journey Optimizer. Une discordance dans la structure de la payload des majuscules, des orthographes ou des événements empêchera le déclenchement du déclencheur. Utilisez l’outil Adobe Experience Platform Assurance pour inspecter les événements SDK en direct et les comparer à la configuration de déclencheur de votre campagne.

Découvrez comment créer et configurer un message in-app [sur cette page](../in-app/create-in-app.md).

+++


## Cartes de contenu {#ajo-troubleshooting-content-cards}

+++ Pourquoi les cartes de contenu ne s’affichent-elles pas dans l’application ?

Les cartes de contenu nécessitent que le SDK mobile Adobe Experience Platform et le **SDK de messagerie** soient installés, enregistrés et configurés dans l’application. Contrairement aux messages push ou in-app, les cartes de contenu ne s’affichent pas automatiquement : votre application doit appeler explicitement les API Messaging SDK pour récupérer les cartes disponibles, puis les afficher dans votre interface utilisateur. Si les cartes n’apparaissent pas, utilisez **** pour vérifier que les demandes de décision sont envoyées lorsque l’événement cible se déclenche et que les réponses reviennent d’Edge Network.

Découvrez comment configurer la prise en charge des cartes de contenu dans Mobile SDK [sur cette page](../content-card/content-card-configuration-sdk.md).

+++

+++ Les cartes de contenu requièrent-elles que l’utilisateur accorde des autorisations de notification push ?

Non. Les cartes de contenu sont silencieuses et persistantes. Elles ne dépendent pas des autorisations push au niveau du système d’exploitation et ne sont pas affectées par le statut d’accord préalable à la notification d’un utilisateur. Cela en fait un canal de secours utile pour atteindre les utilisateurs et utilisatrices qui ont désactivé les notifications push. Les cartes sont récupérées à partir d’Edge Network lorsque l’utilisateur est en session et affichées dans l’interface utilisateur de votre application.

En savoir plus sur le canal des cartes de contenu [sur cette page](../content-card/get-started-content-card.md).

+++

+++ Pourquoi les impressions de carte de contenu n’apparaissent-elles pas dans les rapports de campagne ?

Les impressions et interactions de cartes de contenu (clics, suppressions) ne sont pas automatiquement suivies. Votre application doit explicitement renvoyer les événements de suivi à Adobe via le SDK de messagerie après le rendu d’une carte et après toute interaction de l’utilisateur avec celle-ci. Si ces appels de suivi sont absents de l’implémentation de , les rapports n’affichent aucune impression, même si les cartes sont correctement diffusées. Vérifiez que les appels de suivi se déclenchent dans **** avant d’examiner la configuration de la campagne.

Découvrez comment accéder aux rapports de carte de contenu [sur cette page](../content-card/content-card-report.md).

Consultez également la section [configuration du SDK de carte de contenu](../content-card/content-card-configuration-sdk.md) pour connaître les appels de suivi requis.

+++

## WhatsApp {#ajo-troubleshooting-whatsapp}

+++ Pourquoi mes messages WhatsApp ne sont-ils pas envoyés ?

La diffusion de messages WhatsApp requiert deux conditions : le destinataire doit avoir explicitement choisi de recevoir des communications WhatsApp de votre marque, et le message doit utiliser un **modèle de message pré-approuvé** enregistré auprès de l&#39;API commerciale WhatsApp. Si l&#39;une de ces conditions n&#39;est pas remplie, le message sera bloqué silencieusement par la plateforme WhatsApp avant d&#39;être diffusé. Vérifiez le statut d&#39;opt-in dans les attributs de consentement du profil du destinataire et confirmez que le modèle a le statut **Approuvé** dans votre compte professionnel WhatsApp.

Découvrez comment configurer le canal WhatsApp [sur cette page](../whatsapp/whatsapp-configuration.md).

+++

+++ Pourquoi mon message WhatsApp est-il rejeté avec une erreur de modèle ?

L&#39;API commerciale WhatsApp autorise uniquement les modèles de messages pré-approuvés pour les messages sortants initiés par l&#39;entreprise. Les messages de forme libre ne sont autorisés que dans un délai de 24 heures **intervalle du service client** c’est-à-dire dans les 24 heures suivant l’envoi d’un message à votre marque en premier. Si votre message est rejeté, vérifiez que le modèle a été envoyé à et approuvé par Meta, que les variables de modèle (espaces réservés) dans le message Journey Optimizer correspondent exactement à la structure de modèle approuvée et que le modèle correct est sélectionné dans la campagne ou l’action de parcours.

Découvrez comment créer des messages WhatsApp [sur cette page](../whatsapp/create-whatsapp.md).

+++

+++ Comment puis-je collecter et vérifier l’opt-in WhatsApp des utilisateurs ?

WhatsApp requiert un opt-in explicite avant de pouvoir envoyer des messages marketing. L’Opt-in peut être collecté via n’importe quel canal contrôlé par votre marque (formulaire web, double opt-in des SMS ou écran de consentement in-app, par exemple), à condition que le processus soit clair et documenté. Une fois collecté, mettez à jour l’attribut de consentement WhatsApp du profil dans Adobe Experience Platform. Pour vérifier le statut actuel du consentement pour un profil, ouvrez le profil dans l’interface utilisateur d’Experience Platform et examinez la section **Consentements**. Envoyer des messages à des profils sans consentement valide viole les politiques commerciales de WhatsApp et peut entraîner la suspension de votre compte.

Découvrez comment commencer à utiliser le canal WhatsApp [sur cette page](../whatsapp/get-started-whatsapp.md).

+++

## Gestion des données {#ajo-troubleshooting-data-management}

+++ Comment les paramètres de durée de vie (TTL) s’appliquent-ils aux jeux de données de profil et de lac de données lorsque vous créez un sandbox ?

Les organisations qui configurent de nouveaux sandbox dans Adobe Journey Optimizer se sont interrogées sur la manière dont les paramètres de durée de vie (TTL) s’appliquent aux jeux de données de profil et de lac de données. Les paramètres de durée de vie n’affectent pas les sandbox existants et sont automatiquement appliqués uniquement aux sandbox nouvellement configurés.

Pour en savoir plus sur la durée de vie des jeux de données, consultez [cette page](../data/datasets-ttl.md).

+++

+++ Pourquoi un jeu de données n’est-il pas activé pour le profil client en temps réel ?

Pour qu’un jeu de données alimente les conditions de parcours et de personnalisation basées sur les profils dans Journey Optimizer, deux conditions doivent être remplies : le schéma XDM sous-jacent doit avoir l’option **Profil** activée et le jeu de données lui-même doit être activé pour **Profil client en temps réel** dans l’interface utilisateur d’Experience Platform. Si l’un des deux est manquant, les données seront ingérées dans le lac de données, mais ne seront pas fusionnées en profils unifiés. Assurez-vous également que le jeu de données contient au moins un champ d’identité mappé à un espace de noms reconnu.

Découvrez comment configurer des jeux de données [sur cette page](../data/get-started-datasets.md).

Consultez également la [présentation de la gestion des données](../data/gs-data.md) pour obtenir la liste de contrôle de configuration complète.

+++

+++ Comment surveiller et résoudre les échecs d’ingestion de données ?

Les échecs d’ingestion apparaissent dans le tableau de bord **Surveillance** de Adobe Experience Platform sous **Sources** > **Flux de données**. Les causes courantes incluent les erreurs de validation du schéma (un champ des données sources ne correspond pas au schéma XDM), les champs d’identité obligatoires manquants ou les payloads JSON incorrects. Ouvrez l’enregistrement par lot en échec pour afficher le code d’erreur spécifique et les lignes concernées. Corrigez les données sources et réingérez-les, ou ajustez le mappage de schéma si le format source a changé.

En savoir plus sur les schémas et la configuration des données [sur cette page](../data/gs-data.md).

+++


## Gestion des profils et de l’audience {#ajo-troubleshooting-audiences}

+++ Comment résoudre les incohérences des tailles d’audiences ?

Le nombre d’entrées traitées dans la fonctionnalité **Lecture d’audience** d’Adobe Journey Optimizer peut être inférieur à la taille d’audience attendue. Ce problème se produit souvent en raison d’erreurs de configuration d’espace de noms, ce qui entraîne l’exclusion de profils des parcours. La résolution implique la vérification et la correction des configurations d’espace de noms, la lecture de la documentation pertinente et l’ajustement des priorités pour garantir des opérations plus fluides dans Adobe Journey Optimizer.

Pour en savoir plus sur l’activité **Lecture d’audience** dans les parcours, consultez [cette page](../building-journeys/read-audience.md).

+++

+++ Pourquoi les mises à jour de profil échouent-elles ?

Dans Adobe Journey Optimizer, certaines valeurs de champ peuvent ne pas se mettre à jour correctement après avoir exécuté une activité **Mettre à jour le profil** dans un parcours. Dans certains cas, les champs mis à jour peuvent disparaître ou revenir à leur état précédent. Pour résoudre ce problème, recherchez les règles ou conditions en conflit, vérifiez les paramètres des autorisations, utilisez un jeu de données unique pour l’activité **Mettre à jour le profil** et assurez-vous qu’aucun autre processus d’ingestion n’écrit sur le même profil en même temps.

Pour en savoir plus sur l’activité **Mettre à jour le parcours**, consultez [cette page](../building-journeys/update-profiles.md).

+++

+++ Pourquoi le nombre de profils rejoignant un parcours est-il différent de celui de l’audience associée ?

Cette incohérence peut se produire lorsque le parcours utilise l’instantané de profil d’un jour passé si celui du jour en cours n’est pas disponible au moment de l’exécution du parcours. Pour plus d’informations, vérifiez quand votre tâche de segmentation quotidienne s’est exécutée pour la dernière fois et si le parcours a été déclenché avant que l’instantané ne soit prêt.

Pour en savoir plus sur l’activité **Lecture d’audience** et le comportement de planification [consultez cette page](../building-journeys/read-audience.md).

+++

+++ Pourquoi le sélecteur d’audience affiche-t-il un nombre de profils différent dans les campagnes et les parcours ?

Vous remarquerez peut-être qu’une même audience affiche un nombre de profils différent dans les campagnes et les parcours. Cela se produit, car chaque fonctionnalité utilise des API différentes pour récupérer les données d’audience, qui peuvent renvoyer des valeurs différentes.

Il s’agit d’un comportement attendu qui n’a aucune incidence sur l’exécution de votre campagne. Les profils corrects seront toujours ciblés. Pour vérifier la taille réelle de l’audience, accédez à **[!UICONTROL Client ou cliente]** > **[!UICONTROL Audiences]** et sélectionnez votre audience.

+++


+++ Comment résoudre les problèmes de population d’audience ?

Des problèmes de population d’audience peuvent survenir lorsqu’il manque des composants ou des ressources, souvent en raison d’erreur de droits, d’approvisionnement ou de configuration des autorisations. Pour résoudre ces problèmes, commencez par vérifier les droits, l’approvisionnement et les autorisations. Si le problème persiste, faites-le remonter et contactez les équipes d’assistance pour une résolution complète.

En savoir plus sur la gestion des audiences [sur cette page](../audience/about-audiences.md).

+++

+++ Pourquoi le nombre de profils engageables a-t-il augmenté de manière significative en peu de temps ? 

La mesure **Profils engageables** reflète le nombre de profils uniques engagés par des parcours ou des campagnes au cours des 12 derniers mois. Une augmentation soudaine peut résulter de parcours ou de campagnes ciblant de grandes audiences qui n’ont pas été engagées récemment, ou de modifications de jeux de données activés pour le service de profil.

Pour étudier et résoudre ce problème, vous devez comprendre la logique du comptage des profils, étudier les parcours et les campagnes ciblant de grandes audiences, filtrer les audiences de manière appropriée, surveiller les modifications des jeux de données et potentiellement réduire la taille de votre audience adressable.

Découvrez comment dépanner et résoudre les augmentations des profils engageables et surveiller l’utilisation des licences de votre entreprise dans la [documentation du tableau de bord d’utilisation des licences](../audience/license-usage.md#troubleshooting-engageable-profiles).

+++

+++ Pourquoi les e-mails envoyés à des personnes en dehors de l’audience ciblée sont-ils basés sur des fonctions de date ?

Les e-mails peuvent être envoyés à des destinataires qui **ne répondent pas aux critères d’audience spécifiés**. Par exemple, les personnes membres dont la date de rachat est **antérieure au 4 juillet 2025** peuvent recevoir des e-mails destinés uniquement à celles dont la date est postérieure à cette date. Ce comportement peut résulter d’une **erreur de segmentation d’audience** ou de **modifications inattendues de la logique de qualification des profils**. Passez en revue la définition de l’audience et effectuez des tests avec des profils types pour vérifier que la logique de date est correctement appliquée.

Pour en savoir plus sur les fonctions de date, consultez [cette page](../building-journeys/functions/date-functions.md).

+++

+++ Pourquoi la somme Exclusions + Diffusés dépasse-t-elle ma taille d’audience ciblée dans les rapports de campagne ?

Dans les rapports de campagne, vous remarquerez peut-être que la somme des **Diffusés** et **Exclusions** dépasse la taille de l’audience ciblée d’origine. Cela se produit, car la mesure **Exclusions** comptabilise tous les événements d’exclusion, y compris les événements d’exclusion en double pour un même profil. Si un profil est exclu plusieurs fois au cours d’une campagne, chaque événement est comptabilisé séparément.

**Exemple** : une campagne ciblant 94 000 profils affiche 69 000 diffusions et 37 000 exclusions, pour un total de 106 000, ce qui dépasse les 94 000 profils ciblés d’origine. C’est un comportement normal.

Pour comprendre la différence entre les événements d’exclusion totale et les exclusions de profil uniques, reportez-vous à l’[explication du comptage des exclusions](../reports/exclusion-list.md#exclusion-list).

En savoir plus sur les [rapports de campagne](../reports/campaign-global-report-cja.md) et les [mesures de rapport](../reports/global-report-components-cja.md).

+++

+++ Comment résoudre les problèmes de sélection d’audience et les erreurs Chrome lors de l’enregistrement des parcours ?

L’ajout d’audiences à des conditions de parcours peut parfois entraîner des **blocages de l’application** ou afficher une **erreur « Aw Snap! »** dans Chrome, y compris des erreurs lors de l’enregistrement des parcours. Ces problèmes sont souvent liés aux **services Chromium**. Pour les résoudre, appliquez une **mise à jour du navigateur**, effacez la mémoire cache du navigateur ou essayez une autre session du navigateur.

En savoir plus sur la [navigation dans l’interface de Journey Optimizer](user-interface.md).

+++

## Parcours {#ajo-troubleshooting-journeys}

Pour les parcours, reportez-vous aux sections de résolution des problèmes suivantes :

* [Résoudre les erreurs avant de tester votre parcours](../building-journeys/troubleshooting.md)
* [Résoudre les problèmes liés aux actions entrantes dans les parcours](../building-journeys/troubleshooting-inbound.md)
* [Résoudre les problèmes d’exécution de votre parcours actif](../building-journeys/troubleshooting-execution.md)
* [Résoudre les problèmes liés aux actions personnalisées](../action/troubleshoot-custom-action.md)


+++ Pourquoi les expressions disparaissent-elles lors de la création d’une version de parcours ?  

Lors de la création de la version d’un parcours, les **expressions d’étapes spécifiques** peuvent être perdues, ce qui entraîne des erreurs et nécessite une nouvelle saisie manuelle. Pour résoudre ce problème, **dupliquez le parcours**, testez la reproductibilité, **évitez les rechargements du navigateur** et utilisez la **zone de travail mise à jour** pour les parcours plus anciens.

Découvrez comment dupliquer un parcours [sur cette page](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ Pourquoi les profils quittent-ils prématurément des parcours ? 

Les profils peuvent quitter un parcours de manière inattendue sans passer par un nœud désigné lorsque la **condition utilisée pour vérifier le statut du restours** des messages envoyés est mal configurée. Pour résoudre ce problème, examinez la **logique de condition**, implémentez une **autre logique** ou consultez votre **équipe d’implémentation**.

Consultez également les [directives de conception de parcours](../building-journeys/using-the-journey-designer.md).

+++


+++ Pourquoi les profils quittent-ils les parcours de manière inattendue ?

Les profils peuvent quitter un parcours de manière inattendue lorsque la **limitation d’événement** se produit, ce qui entraîne l’abandon de certains profils si le nombre d’événements traités dépasse la capacité du système. Pour réduire les sorties de profil, comprenez les **limites du système**, surveillez les **pics d’événement** et optimisez le **flux de données** pour éviter de dépasser les seuils.

Consultez également la section [Mécanismes de sécurisation de parcours](../start/guardrails.md#decisioning-guardrails).

+++


+++ Pourquoi mon événement ne déclenche-t-il pas le parcours prévu ?  

Les événements peuvent ne pas déclencher de parcours même si tous les critères sont remplis lorsqu’ils sont **créés par le biais des services de requête** plutôt que d’être diffusés en streaming vers **Data Collection Core Service (DCCS)**. Pour résoudre ce problème, vérifiez la configuration de l’événement, assurez-vous que les événements sont **envoyés directement à DCCS** et effectuez une vérification à l’aide du **mode test**.

Apprenez-en plus sur les événements [sur cette page](../event/about-events.md).

Consultez également la section [Mécanismes de sécurisation des événements de parcours](../start/guardrails.md#events-g).

+++


+++ Comment résoudre les problèmes de déclenchement de parcours après modification de l’audience dans Adobe Journey Optimizer ? 

Si un parcours cesse de se déclencher après des modifications apportées à l’audience associée, telles que la modification de la politique de fusion, vous pouvez rencontrer des flux interrompus. Pour résoudre ce problème, **dupliquez et republiez le parcours** avec les paramètres d’audience mis à jour afin de vous assurer que les déclencheurs fonctionnent correctement.

Découvrez comment dupliquer un parcours sur [cette page](../building-journeys/journey-ui.md#duplicate-a-journey).

+++

+++ Pourquoi une action personnalisée qui appelle un point d’entrée tiers externe expire-t-elle ?

Des erreurs de dépassement de délai d’expiration peuvent se produire lorsqu’une **action personnalisée** appelle un point d’entrée tiers externe. Pour résoudre ce problème, vérifiez que le **point d’entrée est accessible**, consultez les **journaux du serveur**, assurez-vous qu’il n’y a **aucun blocage de la part d’Adobe**, mettez à jour les configurations des points d’entrée si nécessaire et **exécutez un test une fois les mises à jour effectuées**. Notez également les **spécifications concernant les délais d’expiration pour les appels API**.

Pour en savoir plus sur l’API Journey Throttling, consultez [cette page](../configuration/throttling.md).

Consultez également la [documentation sur l’intégration à des systèmes externes](../configuration/external-systems.md).

+++

+++ Quelles mesures devez-vous prendre si vous rencontrez une erreur 403 avec le message **invalid_access** ou **No access to this dataId=XX granted** lors de la publication d’une audience à partir d’un parcours ?

Pour résoudre cette erreur, demandez à votre administrateur ou administratrice de vérifier que votre profil utilisateur a accès aux vues de données requises pour la publication d’audience, puis essayez de republier l’audience.

Reportez-vous à [la documentation sur les autorisations](../administration/permissions.md) pour savoir comment résoudre ce problème.

+++

## Règles {#ajo-troubleshooting-rules}

+++ Pourquoi la liste déroulante Règles de limitation ne fonctionne-t-elle pas ?

Les problèmes liés à la liste déroulante **Règles de limitation** se produisent souvent lorsque les jeux de règles sont **mal configurés** ou **inaccessibles**. Vérifiez que tous les jeux de règles sont correctement configurés et disponibles pour résoudre le problème.

Découvrez comment appliquer des règles de limitation dans [cette section](../conflict-prioritization/rule-sets.md).

+++

+++ Pourquoi une règle de limitation de la fréquence n’est-elle pas appliquée à ma campagne ou à mon parcours ?

Les règles de limitation de la fréquence ne prennent effet que lorsque le jeu de règles est explicitement associé à la campagne ou au parcours. Si la limitation ne fonctionne pas, vérifiez que l’ensemble de règles approprié est sélectionné dans les paramètres de la campagne ou du parcours, que le type de canal de la règle correspond au canal utilisé et que la règle a le statut **Actif**. Vérifiez également si le profil a déjà atteint la limite lors d’une exécution précédente, ce qui empêcherait la génération d’autres messages même si la règle semble correctement configurée.

Découvrez comment configurer les règles de limitation de canal [sur cette page](../conflict-prioritization/channel-capping.md).

+++

+++ Comment configurer les heures creuses pour empêcher l&#39;envoi de messages la nuit ?

Les heures creuses sont des règles d’exclusion temporelles configurées dans un **ensemble de règles de canal**. Définissez la fenêtre d’arrêt de la surveillance (par exemple, de 22 h à 8 h) et appliquez l’ensemble de règles aux campagnes ou parcours appropriés. Lorsque l’envoi d’un message est planifié pendant les heures calmes, Journey Optimizer retient le message jusqu’à la prochaine fenêtre autorisée ou le rejette, selon la configuration de la règle.

Découvrez comment configurer des heures calmes [sur cette page](../conflict-prioritization/quiet-hours.md).

+++

## Prise de décision {#ajo-troubleshooting-decisioning}

+++ Comment résoudre les problèmes qui se produisent lors de la création de collections d’offres ?

Lors de la création de collections d’offres, des problèmes se produisent souvent lorsque les **catalogues n’ont pas été approvisionnés** pour votre organisation. Pour résoudre ce problème, vérifiez que tous les catalogues requis sont correctement approvisionnés avant de tenter de créer des collections d’offres.

Pour en savoir plus sur les collections d’offres, consultez [cette page](../offers/offer-library/creating-collections.md).

+++

+++ Pourquoi ne puis-je pas accéder à Offer Decisioning ?  

Lors de l’intégration d’Adobe Target à une application à l’aide d’Adobe Journey Optimizer, l’option **Offer Decisioning** peut être inaccessible dans la configuration du train de données. Cela se produit généralement en raison des **paramètres des autorisations** ou de **contraintes d’approvisionnement**. Pour résoudre ce problème, vérifiez les autorisations utilisateur et assurez-vous que l’approvisionnement nécessaire est présent.

Pour en savoir plus sur les autorisations requises pour Offer Decisioning, consultez [cette page](../offers/get-started/starting-offer-decisioning.md#granting-acess-to-decision-management).

+++

+++ Pourquoi une offre n’est-elle pas renvoyée alors qu’elle répond aux critères d’éligibilité ?

Si une offre qualifiante n’apparaît pas dans une réponse de prise de décision, vérifiez les points suivants dans l’ordre : vérifiez que l’offre a le statut **Approuvé** (et non Brouillon); confirmez que l’identifiant d’emplacement dans la requête correspond à la surface de représentation de l’offre ; vérifiez si une limite de limitation (totale ou par profil) a été atteinte pour cette offre ; et assurez-vous que la portée de la collection et de la décision est correctement configurée. Utilisez l’outil **Simulation** dans Experience Decisioning pour tester les réponses des offres par rapport à un profil spécifique sans envoyer de trafic en direct.

Découvrez comment commencer à utiliser Experience Decisioning [sur cette page](../experience-decisioning/gs-experience-decisioning.md).

+++


## Multilingue {#ajo-troubleshooting-multilingual}

+++ Comment résoudre ce problème `Message validation error (CJMMAS - 1069-500)` ?

Dans Adobe Journey Optimizer, une erreur de validation de message (CJMMAS - 1069-500) liée à la fonctionnalité multilingue empêche les parcours d’être définis sur Mode de test ou Publié. Vérifiez que tout le contenu des paramètres régionaux est complet, que la langue principale est correctement définie et qu’aucun champ de traduction obligatoire n’est vide avant de tenter de publier.

Pour en savoir plus sur le contenu multilingue, consultez [cette page](../content-management/multilingual-gs.md).

+++

+++ Pourquoi le fournisseur de traduction ne se connecte-t-il pas dans Journey Optimizer ?

Les échecs de connexion du fournisseur de traduction sont généralement dus à des informations d’identification d’API incorrectes ou à une configuration de fournisseur manquante dans les paramètres multilingues. Vérifiez que la clé API, l’URL du point d’entrée et les jetons d’authentification requis saisis dans Journey Optimizer correspondent exactement à ce que votre fournisseur de traduction a configuré. Si les informations d’identification sont correctes, vérifiez si le compte du fournisseur dispose d’un quota suffisant ou d’un statut d’abonnement actif, puis enregistrez et testez à nouveau la connexion.

Découvrez comment configurer un fournisseur de traduction [sur cette page](../content-management/multilingual-provider.md).

+++

+++ Que se passe-t-il lorsqu’une traduction est manquante pour un paramètre régional ?

Si aucune traduction n’a été fournie pour des paramètres régionaux spécifiques, Journey Optimizer revient au contenu défini dans la **langue principale** (paramètres régionaux de secours) configurée dans vos paramètres linguistiques. Si aucune solution de secours n’est configurée, le message peut être rendu vide ou la validation peut échouer avant l’envoi. Pour éviter cela, définissez toujours un paramètre régional de secours dans les paramètres de votre projet multilingue et vérifiez que tous les paramètres régionaux contiennent des traductions approuvées avant d’activer la campagne ou le parcours.

En savoir plus sur la configuration du contenu multilingue [sur cette page](../content-management/multilingual-gs.md).

+++


## Configuration {#ajo-troubleshooting-config}

+++ Comment activer TLS v1.3 pour les actions personnalisées ?  

Pour maintenir l’**intégrité et la sécurité des données** lors de la connexion à des systèmes tiers, assurez-vous que le protocole TLS (**Transport Layer Security**) v1.3 est activé pour vos actions personnalisées. Cela permet de protéger les communications et d’éviter des vulnérabilités de sécurité potentielles.

En savoir plus sur la configuration d’une action personnalisée [sur cette page](../action/about-custom-action-configuration.md).

+++

+++ Pourquoi est-il impossible de créer un tableau de bord directement à partir d’une requête dans Adobe Journey Optimizer ? 

Dans Adobe Journey Optimizer, les tableaux de bord ne peuvent pas être créés directement à partir des requêtes. Pour créer des tableaux de bord, utilisez les fonctionnalités de **création de tableaux de bord** disponibles dans Adobe Experience Platform, qui vous permettent de visualiser et d’analyser efficacement les données des requêtes.

En savoir plus sur les requêtes dans Journey Optimizer [sur cette page](../data/get-started-queries.md).

+++

+++ Pourquoi mes messages sont-ils bloqués par la liste de suppression ?

Les adresses sont automatiquement ajoutées à la liste de suppression après les hard bounces, les plaintes contre le spam ou les ajouts manuels par un administrateur. Une fois supprimé, un profil ne recevra aucun message de ce canal, quel que soit le ciblage de la campagne ou du parcours. Pour plus d’informations, ouvrez **Administration** > **Canaux** > **Liste de suppression** et recherchez l’adresse. Si la suppression a été ajoutée par erreur, elle peut être supprimée directement de l’interface. Pour les suppressions de hard bounces, vérifiez également le problème de délivrabilité sous-jacent avant de supprimer l’adresse.

Découvrez comment gérer la liste de suppression [sur cette page](../configuration/manage-suppression-list.md).

+++

## API {#ajo-troubleshooting-apis}

+++ Comment résoudre les problèmes d’accès avec l’API Query Service ?  

Les erreurs d’accès lors de l’utilisation de l’**API Query Service** via Postman ou des outils similaires sont généralement dues à des **autorisations insuffisantes**. Pour résoudre ce problème, vérifiez les autorisations utilisateur, vérifiez les informations d’identification de l’API par rapport aux rôles configurés dans votre organisation et fournissez des informations détaillées à prendre en charge si nécessaire.

En savoir plus sur les autorisations dans Journey Optimizer [sur cette page](../administration/permissions.md).

+++

+++ Comment résoudre les erreurs 429 Too Many Requests lors de l’appel des API Journey Optimizer ?

Une réponse 429 signifie que votre intégration a dépassé la limite de taux d’API pour le point d’entrée . Chaque API Journey Optimizer a défini des seuils de débit. Pour résoudre ce problème, implémentez la logique **retour exponentiel** dans votre intégration : attendez la durée spécifiée dans l’en-tête de réponse `Retry-After` avant de réessayer. Pour les cas d’utilisation intenses et durables, passez en revue la configuration de limitation et de plafonnement de vos actions personnalisées et de vos sources de données afin d’aligner les taux d’appels API sur les limites du système.

Pour en savoir plus sur la limitation de Journey Optimizer [consultez cette page](../configuration/throttling.md).

Consultez également la [documentation sur l’intégration de systèmes externes](../configuration/external-systems.md).

+++

+++ Pourquoi ma campagne déclenchée par API ne s’exécute-t-elle pas après l’appel API ?

Si une campagne déclenchée par une API n’est pas en cours d’exécution, vérifiez les points suivants : la campagne est à l’état **Actif** (non à l’état de brouillon ou arrêtée) ; l’appel API inclut l’identifiant de campagne correct dans le chemin d’accès du point d’entrée ; la payload de la requête correspond au schéma d’identifiant de profil attendu par la campagne ; et les informations d’identification d’API utilisées disposent de l’autorisation **Gérer les campagnes**. Vérifiez les logs d&#39;exécution de la campagne dans le tableau de bord de reporting pour identifier si le profil a été reçu mais exclu, ou si l&#39;appel n&#39;a pas du tout atteint la campagne.

En savoir plus sur les campagnes déclenchées par API [sur cette page](../campaigns/api-triggered-campaigns.md).

+++
