---
solution: Journey Optimizer
product: journey optimizer
title: Résoudre les problèmes d’exécution de votre parcours actif
description: Découvrez comment résoudre les erreurs d’exécution des parcours actifs.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: dépannage, résolution des problèmes, parcours, vérification, erreurs
exl-id: fd670b00-4ebb-4a3b-892f-d4e6f158d29e
version: Journey Orchestration
source-git-commit: acf73fbce4a8ebfc6f228c92480a5e597e0bfe53
workflow-type: ht
source-wordcount: '1260'
ht-degree: 100%

---

# Résoudre les problèmes d’exécution de votre parcours actif {#troubleshooting-execution}

Dans cette section, découvrez comment résoudre les problèmes liés aux événements de parcours, vérifier si des profils ont rejoint le parcours ainsi que leur progression, et si des messages sont envoyés.

Vous pouvez également résoudre les erreurs avant de tester ou de publier un parcours. Découvrez comment procéder [sur cette page](troubleshooting.md).

Si vous utilisez des actions entrantes, découvrez comment résoudre les problèmes liés à ces dernières [sur cette page](troubleshooting-inbound.md).

## Vérifier l’envoi correct des événements {#checking-that-events-are-properly-sent}

Le point de départ d&#39;un parcours est toujours un événement. Il est possible d&#39;effectuer des tests à l&#39;aide d&#39;outils tels que Postman.

Vous pouvez ainsi vérifier si l&#39;appel d&#39;API émis via ces outils est correctement envoyé ou non. Si vous obtenez une erreur en retour, cela signifie que votre appel a rencontré un problème. Vérifiez à nouveau la payload, l&#39;en-tête (et en particulier l&#39;identifiant d&#39;organisation) et l&#39;URL de destination. Vous pouvez demander à votre administrateur l&#39;URL appropriée pour l&#39;accès.

Les événements ne sont pas directement transmis de la source aux parcours. En effet, les parcours s’appuient sur les API d’ingestion en flux continu d’Adobe Experience Platform. En cas de problèmes relatifs aux événements, vous pouvez consulter la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=fr){target="_blank"} pour la résolution des problèmes liés aux API d’ingestion en flux continu.

Si votre parcours ne parvient pas à activer le mode test avec l’erreur `ERR_MODEL_RULES_16`, assurez-vous que l’événement utilisé inclut un [espace de noms d’identité](../audience/get-started-identity.md) lors de l’utilisation d’une action de canal.

L’espace de noms d’identité est utilisé pour identifier de manière unique les profils de test. Par exemple, si l&#39;e-mail est utilisé pour identifier les profils de test, l’espace de noms d’identité **E-mail** doit être sélectionné. Si l’identifiant unique est le numéro de téléphone, l’espace de noms d’identité **Téléphone** doit être sélectionné.

## Vérifier si les personnes rejoignent le parcours {#checking-if-people-enter-the-journey}

Les rapports produits par Journey donnent des mesures en temps réel des entrées des visiteurs dans un parcours.

Si l’événement a été envoyé avec succès, mais que vous ne voyez aucune entrée dans le parcours, cela signifie qu’une erreur s’est produite entre l’envoi de l’événement et la réception de l’événement dans le parcours.

Pour résoudre votre problème, commencez par répondre aux questions suivantes :

* Êtes-vous certain que le parcours où vous attendez l&#39;événement entrant est en mode test ou actif ?
* Avez-vous enregistré l&#39;événement avant de copier la payload depuis l&#39;aperçu de la payload ?
* La payload d&#39;événement contient-elle un identifiant d&#39;événement ?
* Avez-vous atteint la bonne URL ?
* Avez-vous appliqué la structure de payload des API d&#39;ingestion en flux continu en utilisant l&#39;aperçu de la structure de payload dans le volet de configuration des événements ? Voir [cette page](../event/about-creating.md#preview-the-payload).
* Avez-vous utilisé les paires clé-valeur appropriées dans l’en-tête de l’événement ?

  ```
  X-gw-ims-org-id - your organization's ID
  Content-type - application/json
  ```

>[!NOTE]
>
>**Pour les parcours de qualification d’audience avec audiences en streaming** : si vous utilisez une activité de qualification d’audience comme point d’entrée d’un parcours, gardez à l’esprit que tous les profils correspondant aux critères de cette audience ne rejoindront pas nécessairement le parcours, en raison de facteurs de délai, de sorties rapides de l’audience ou du fait qu’ils se trouvaient déjà dans l’audience avant la publication. En savoir plus sur les [considérations relatives au délai de qualification des audiences en streaming](audience-qualification-events.md#streaming-entry-caveats).

## Vérifier comment les gens naviguent dans le parcours {#checking-how-people-navigate-through-the-journey}

Les rapports produits par Journey mesurent la progression des individus dans un parcours. Il est très facile d&#39;identifier où et pourquoi une personne s&#39;est arrêtée.

Les éléments à vérifier sont les suivants :

* La situation est-elle due à une condition excluant la personne concernée ? Par exemple, la condition est « genre = masculin » et la personne est une femme. Si la condition n&#39;est pas trop complexe, un utilisateur chargé de la conception de parcours peut effectuer cette vérification.
* La situation est-elle due à une source de données qui ne répond pas ? Lorsque le parcours est en test, ces informations apparaissent dans les journaux du mode test. Lorsque le parcours est actif, un administrateur peut tester les appels directs à la source de données et vérifier la réponse reçue. Il peut également dupliquer le parcours et le tester.

## Vérifier que les messages sont bien envoyés {#checking-that-messages-are-sent-successfully}

Si les personnes progressent correctement dans le parcours sans recevoir les messages qu’ils devraient recevoir, vous pouvez vérifier les points suivants :

* [!DNL Journey Optimizer] a correctement pris en compte la demande d&#39;envoi. Les utilisateurs professionnels peuvent accéder au message censé être envoyé et vérifier si l’heure de la dernière exécution correspond à l’heure d’exécution de votre parcours. Ils peuvent également vérifier les derniers appels/événements d’API reçus.
* [!DNL Journey Optimizer] a envoyé le message avec succès. Vérifiez les rapports sur les parcours pour vous assurer qu’il n’y a aucune erreur.

Dans le cas d’un message envoyé par le biais d’une action personnalisée, le seul élément vérifiable pendant le test du parcours est l’apparition ou non d’une erreur suite à l’appel du système à l’aide d’une action personnalisée. Si l’appel au système externe associé à l’action personnalisée n’entraîne pas d’erreur, mais ne déclenche pas l’envoi d’un message, certaines vérifications doivent être effectuées du côté du système externe.

## Explication des entrées en double dans les événements d’étape de parcours {#duplicate-step-events}

### Pourquoi est-ce que je vois plusieurs entrées avec les mêmes ID d’instance de parcours, de profil, de nœud et de requête ?

Lors de l’interrogation des données d’événements d’étape de parcours, vous pouvez parfois détecter des entrées de journal en double pour la même exécution de parcours. Ces entrées partagent des valeurs identiques pour les éléments suivants :

* `profileID` - Identité du profil
* `instanceID` - Identifiant de l’instance de parcours
* `nodeID` - Nœud de parcours spécifique
* `requestID` - Identifiant de la requête

Cependant, ces entrées ont des **valeurs `_id` différentes**, ce qui indique qu’il ne s’agit pas d’une duplication réelle des données.

### Qu’est-ce qui provoque ce comportement ?

Cela se produit en raison des opérations de mise à l’échelle automatique du système back-end (également appelées « rééquilibrage ») dans l’architecture des microservices d’Adobe Journey Optimizer. Pendant les périodes de forte charge ou d’optimisation du système :

1. un événement d’étape de parcours commence à être traité et est enregistré dans le jeu de données Événements d’étape de parcours ;
2. une opération de mise à l’échelle automatique redistribue la charge de travail entre les instances de service ;
3. le même événement peut être retraité par une autre instance de service, créant ainsi une seconde entrée de journal avec une valeur `_id` différente.

Il s’agit d’un comportement système attendu qui **fonctionne comme prévu**.

### Y a-t-il un impact sur l’exécution du parcours ou la diffusion des messages ?

**Non.** L’impact ne concerne que la journalisation. Adobe Journey Optimizer dispose de mécanismes de déduplication intégrés au niveau de la couche d’exécution des messages qui garantissent ce qui suit :

* Un seul message (e-mail, SMS, notification push, etc.) est envoyé à chaque profil.
* Les actions sont exécutées une seule fois.
* L’exécution du parcours se déroule correctement.

Vous pouvez vérifier en interrogeant le `ajo_message_feedback_event_dataset` ou en consultant les journaux d’exécution d’action. Vous verrez qu’un seul message a été réellement envoyé, malgré les entrées d’événement d’étape de parcours en double.

### Comment puis-je identifier ces cas dans mes requêtes ?

Lors de l’analyse des données d’événements d’étape de parcours :

1. **Vérifier le champ `_id`** : les vrais doublons au niveau du système auraient la même valeur `_id`. Des valeurs `_id` différentes indiquent qu’il s’agit d’entrées de journal distinctes du scénario de rééquilibrage décrit ci-dessus.

2. **Vérifier la diffusion du message** : comparez avec les données de feedback sur les messages pour confirmer qu’un seul message a été envoyé :

   ```sql
   SELECT
     timestamp,
     _experience.customerJourneyManagement.messageExecution.messageExecutionID,
     _experience.customerJourneyManagement.messageDeliveryfeedback.feedbackStatus
   FROM ajo_message_feedback_event_dataset
   WHERE
     _experience.customerJourneyManagement.messageExecution.journeyVersionID = '<journeyVersionID>'
     AND TO_JSON(identityMap) like '%<profileID>%'
   ORDER BY timestamp DESC;
   ```

3. **Regrouper par identifiants uniques** : lors du comptage des exécutions, utilisez `_id` pour obtenir des décomptes précis :

   ```sql
   SELECT
     COUNT(DISTINCT _id) as unique_executions
   FROM journey_step_events
   WHERE
     _experience.journeyOrchestration.stepEvents.journeyVersionID = '<journeyVersionID>'
     AND _experience.journeyOrchestration.stepEvents.profileID = '<profileID>'
   ```

### Que dois-je faire si cela se produit ?

Il s’agit d’un comportement normal du système et **aucune action n’est requise**. La journalisation en double n’indique aucun problème au niveau de la configuration du parcours ou de la diffusion des messages.

Si vous créez des rapports ou des analyses en fonction d’événements d’étape de parcours :

* Utilisez `_id` comme clé primaire pour compter les événements uniques.
* Comparez avec les jeux de données de feedback sur les messages lors de l’analyse de la diffusion des messages.
* Gardez à l’esprit que l’analyse temporelle peut afficher des entrées regroupées sur quelques secondes d’intervalle.

Pour plus d’informations sur l’interrogation des événements d’étape de parcours, voir [Exemples de requêtes](../reports/query-examples.md).

## Résolution des problèmes liés aux incohérences des mesures du tableau de bord {#dashboard-metrics}

Si les mesures affichées dans le tableau de bord **Vue d’ensemble** ne correspondent pas au nombre réel de parcours dans l’onglet **Parcourir**, vérifiez les points suivants :

* Assurez-vous que les parcours en question ont eu du trafic au cours des dernières 24 heures, car les parcours sans activité récente sont exclus du tableau de bord.
* Vérifiez que vous disposez des autorisations d’accès appropriées pour afficher tous les parcours de votre organisation.
* Patientez jusqu’à 30 minutes pour que les mesures s’actualisent après avoir apporté des modifications à vos parcours.

Si les incohérences persistent, contactez l’assistance Adobe avec des copies d’écran des onglets Vue d’ensemble et Parcourir pour en savoir plus.
