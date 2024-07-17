---
solution: Journey Optimizer
product: journey optimizer
title: Dépannage de parcours
description: Découvrez comment résoudre les erreurs dans les parcours
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: dépannage, résolution des problèmes, parcours, vérification, erreurs
exl-id: 03fbc4f4-b0a8-46d5-91f9-620685b11493
source-git-commit: 135dd7528e87a6fde7e148745ef2f49104809bc1
workflow-type: tm+mt
source-wordcount: '1019'
ht-degree: 100%

---

# Résoudre les problèmes de votre parcours {#troubleshooting}

Cette section décrit comment résoudre les problèmes liés aux parcours avant de les tester ou de les publier. Il est possible d&#39;effectuer les vérifications répertoriées ci-dessous lorsque le parcours est en mode test ou actif. Il est recommandé de les réaliser en mode test, puis d&#39;effectuer la publication. Voir [cette page](../building-journeys/testing-the-journey.md).

## Rechercher des erreurs avant le test {#checking-for-errors-before-testing}

Avant de tester et de publier votre parcours, vérifiez que toutes les activités sont correctement configurées. Vous ne pouvez pas effectuer de tests ou de publications si des erreurs sont détectées par le système.

Les erreurs sont représentées par un symbole d&#39;avertissement, affiché sur l&#39;activité elle-même, dans la zone de travail. Placez le curseur sur le point d&#39;exclamation pour afficher le message d&#39;erreur. Si vous cliquez sur l&#39;activité, vous devez voir la ligne contenant l&#39;erreur associée à un avertissement. Par exemple, si un champ obligatoire est vide, une erreur s&#39;affiche.

![](assets/journey63.png)

Par exemple, dans la zone de travail, lorsque deux activités sont déconnectées, un avertissement s&#39;affiche.

![](assets/canvas-disconnected.png)

En regard du bouton bascule **[!UICONTROL Test]** et du bouton **[!UICONTROL Publier]**, un signe d&#39;avertissement peut s&#39;afficher. Il indique les erreurs détectées par le système et empêche l&#39;activation du mode test ou la publication du parcours. La plupart du temps, les erreurs détectées par le système sont liées à des dysfonctionnements visibles relatifs aux activités. Cependant, elles sont parfois associées à d&#39;autres problèmes. Dans ce cas, vous pouvez les afficher en essayant d&#39;identifier le problème à l&#39;aide de la description de l&#39;erreur. Si vous ne parvenez pas à identifier le problème, vous pouvez copier les détails et les envoyer à l’administrateur ou à l’administratrice ou à l’assistance technique. Notez que les erreurs qui bloquent le test et celles qui bloquent la publication sont similaires.

Le système détecte deux types de problèmes : les erreurs et les avertissements. Les erreurs bloquent la publication et l&#39;activation des tests. Les avertissements indiquent des problèmes potentiels qui ne bloquent pas l&#39;activation ou la publication des tests. Vous verrez une description du problème et un identifiant de journal des problèmes du type ERR_XXX_XXX. Ce format facilite l&#39;identification du problème par l&#39;assistance technique.

Le signe en regard du bouton bascule **[!UICONTROL Test]** et du bouton **[!UICONTROL Publier]** peut apparaître dans deux couleurs différentes. Il est rouge en cas d&#39;erreur, et orange pour un avertissement.

![](assets/journey75.png)

Les erreurs et les avertissements globaux du parcours apparaissent en tête de liste. Ceux liés à des activités spécifiques sont répertoriés ensuite, par ordre d&#39;activité ou d&#39;apparition dans le parcours, de gauche à droite. Le bouton **[!UICONTROL Copier les détails]** copie les informations techniques relatives au parcours qui seront utiles à l&#39;équipe d&#39;assistance technique pour résoudre les problèmes.

Lorsqu&#39;une erreur se produit dans une action ou une condition, le parcours d&#39;un individu s&#39;arrête. La seule façon de le faire continuer est de cocher la case **[!UICONTROL Ajouter un chemin alternatif en cas de temporisation ou d’erreur]**. Consultez [cette section](../building-journeys/using-the-journey-designer.md#paths).

## Vérifier l’envoi correct des événements {#checking-that-events-are-properly-sent}

Le point de départ d&#39;un parcours est toujours un événement. Il est possible d&#39;effectuer des tests à l&#39;aide d&#39;outils tels que Postman.

Vous pouvez ainsi vérifier si l&#39;appel d&#39;API émis via ces outils est correctement envoyé ou non. Si vous obtenez une erreur en retour, cela signifie que votre appel a rencontré un problème. Vérifiez à nouveau la payload, l&#39;en-tête (et en particulier l&#39;identifiant d&#39;organisation) et l&#39;URL de destination. Vous pouvez demander à votre administrateur l&#39;URL appropriée pour l&#39;accès.

Les événements ne sont pas directement transmis de la source aux parcours. En effet, les parcours s’appuient sur les API d’ingestion en flux continu d’Adobe Experience Platform. En cas de problèmes relatifs aux événements, vous pouvez donc consulter la [documentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/ingestion/streaming/troubleshooting.html?lang=fr){target="_blank"} pour la résolution des problèmes concernant les API d’ingestion en flux continu.

## Vérifier si les personnes rejoignent le parcours {#checking-if-people-enter-the-journey}

Les rapports produits par Journey donnent des mesures en temps réel des entrées des visiteurs dans un parcours.

Si l&#39;événement a été envoyé avec succès, mais que vous ne voyez pas d&#39;entrée dans le parcours, cela signifie qu&#39;une erreur s&#39;est produite entre l&#39;envoi de l&#39;événement et la réception de l&#39;événement dans le parcours.

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

Si des personnes suivent le bon chemin dans le parcours sans recevoir les messages qu’elles devraient recevoir, vous pouvez vérifier si :

* [!DNL Journey Optimizer] a correctement pris en compte la demande d&#39;envoi. Les utilisateurs professionnels peuvent accéder au message censé être envoyé et vérifier si l’heure de la dernière exécution correspond à l’heure d’exécution de votre parcours. Ils peuvent également vérifier les derniers appels/événements d’API reçus.
* [!DNL Journey Optimizer] a envoyé le message avec succès. Vérifiez les rapports sur les parcours pour vous assurer qu’il n’y a aucune erreur.

Dans le cas d’un message envoyé par le biais d’une action personnalisée, le seul élément vérifiable pendant le test du parcours est l’apparition ou non d’une erreur suite à l’appel du système à l’aide d’une action personnalisée. Si l’appel au système externe associé à l’action personnalisée n’entraîne pas d’erreur, mais ne déclenche pas l’envoi d’un message, certaines vérifications doivent être effectuées du côté du système externe.
