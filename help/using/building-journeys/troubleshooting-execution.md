---
solution: Journey Optimizer
product: journey optimizer
title: Résolution des problèmes liés à l’exécution du parcours en direct
description: Découvrez comment résoudre les erreurs dans l’exécution des parcours en direct
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: dépannage, résolution des problèmes, parcours, vérification, erreurs
source-git-commit: 61498b61f7f05e0553fe575c980fd1bee08500a3
workflow-type: tm+mt
source-wordcount: '702'
ht-degree: 78%

---

# Résolution des problèmes liés à l’exécution du parcours en direct {#troubleshooting-execution}

Dans cette section, découvrez comment résoudre les problèmes liés aux événements de parcours, vérifier si les profils ont accédé à votre parcours, comment ils le parcourent et si des messages sont envoyés.

Vous pouvez également résoudre les erreurs avant de tester ou de publier un parcours. Découvrez comment [sur cette page](troubleshooting.md).

Si vous utilisez des actions entrantes, découvrez comment les résoudre [sur cette page](troubleshooting-inbound.md).

## Vérifier l’envoi correct des événements {#checking-that-events-are-properly-sent}

Le point de départ d&#39;un parcours est toujours un événement. Il est possible d&#39;effectuer des tests à l&#39;aide d&#39;outils tels que Postman.

Vous pouvez ainsi vérifier si l&#39;appel d&#39;API émis via ces outils est correctement envoyé ou non. Si vous obtenez une erreur en retour, cela signifie que votre appel a rencontré un problème. Vérifiez à nouveau la payload, l&#39;en-tête (et en particulier l&#39;identifiant d&#39;organisation) et l&#39;URL de destination. Vous pouvez demander à votre administrateur l&#39;URL appropriée pour l&#39;accès.

Les événements ne sont pas directement transmis de la source aux parcours. En effet, les parcours s’appuient sur les API d’ingestion en flux continu d’Adobe Experience Platform. En cas de problèmes relatifs aux événements, vous pouvez donc consulter la documentation de [Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=fr){target="_blank"} pour la résolution des problèmes concernant les API d&#39;ingestion en flux continu.

Si votre parcours ne parvient pas à activer le mode test avec l’erreur `ERR_MODEL_RULES_16`, assurez-vous que l’événement utilisé inclut un [espace de noms d’identité](../audience/get-started-identity.md) lors de l’utilisation d’une action de canal.

L’espace de noms d’identité est utilisé pour identifier de manière unique les profils de test. Par exemple, si l&#39;e-mail est utilisé pour identifier les profils de test, l’espace de noms d’identité **E-mail** doit être sélectionné. Si l’identifiant unique est le numéro de téléphone, l’espace de noms d’identité **Téléphone** doit être sélectionné.

## Vérifier si les personnes rejoignent le parcours {#checking-if-people-enter-the-journey}

Les rapports produits par Journey donnent des mesures en temps réel des entrées des visiteurs dans un parcours.

Si l’événement est envoyé avec succès, mais que vous ne voyez pas d’entrée dans le parcours, cela signifie qu’une erreur s’est produite entre l’envoi de l’événement et la réception de l’événement dans le parcours.

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

## Vérifier comment les gens naviguent dans le parcours {#checking-how-people-navigate-through-the-journey}

Les rapports produits par Journey mesurent la progression des individus dans un parcours. Il est très facile d&#39;identifier où et pourquoi une personne s&#39;est arrêtée.

Les éléments à vérifier sont les suivants :

* La situation est-elle due à une condition excluant la personne concernée ? Par exemple, la condition est « genre = masculin » et la personne est une femme. Si la condition n&#39;est pas trop complexe, un utilisateur chargé de la conception de parcours peut effectuer cette vérification.
* La situation est-elle due à une source de données qui ne répond pas ? Lorsque le parcours est en test, ces informations apparaissent dans les journaux du mode test. Lorsque le parcours est actif, un administrateur peut tester les appels directs à la source de données et vérifier la réponse reçue. Il peut également dupliquer le parcours et le tester.

## Vérifier que les messages sont bien envoyés {#checking-that-messages-are-sent-successfully}

Si les individus suivent le bon chemin dans le parcours sans recevoir les messages qu’ils devraient recevoir, vous pouvez vérifier si :

* [!DNL Journey Optimizer] a correctement pris en compte la demande d&#39;envoi. Les utilisateurs professionnels peuvent accéder au message censé être envoyé et vérifier si l’heure de la dernière exécution correspond à l’heure d’exécution de votre parcours. Ils peuvent également vérifier les derniers appels/événements d’API reçus.
* [!DNL Journey Optimizer] a envoyé le message avec succès. Vérifiez les rapports sur les parcours pour vous assurer qu’il n’y a aucune erreur.

Dans le cas d’un message envoyé par le biais d’une action personnalisée, le seul élément vérifiable pendant le test du parcours est l’apparition ou non d’une erreur suite à l’appel du système à l’aide d’une action personnalisée. Si l’appel au système externe associé à l’action personnalisée n’entraîne pas d’erreur, mais ne déclenche pas l’envoi d’un message, certaines vérifications doivent être effectuées du côté du système externe.
