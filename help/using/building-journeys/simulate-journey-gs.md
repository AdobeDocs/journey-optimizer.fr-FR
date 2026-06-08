---
solution: Journey Optimizer
product: journey optimizer
title: Simuler votre parcours
description: Découvrez comment simuler votre parcours
feature: Journeys, Test Profiles
topic: Content Management
role: User
level: Intermediate
keywords: test, parcours, vérification, erreur, dépannage
version: Journey Orchestration
hide: true
feature_v2: []
subfeature_v2: []
source-git-commit: 951343a6695b12aa44ecfc5df3771da2b61b6471
workflow-type: tm+mt
source-wordcount: 1491
ht-degree: 3%

---

# Prise en main de la simulation de Parcours {#simulate-journey-gs}

>[!IMPORTANT]
>
>Vous avez besoin d’au moins de l’une des autorisations suivantes pour accéder à la fonction **[!UICONTROL Simulation]** : **Simuler des parcours**, **Publier des parcours** ou **Approuver et publier des parcours**. [En savoir plus](../administration/permissions.md)

Vous pouvez définir le parcours sur **[!UICONTROL Simulation]** en plus de **Brouillon**, **Mode test** et **En direct**. Dans la simulation, vous testez avec des **utilisateurs simulés** : entités temporaires de type profil que vous ajoutez, sans utiliser de profils de test persistants dans Adobe Experience Platform.

Adobe Journey Optimizer propose deux méthodes pour tester et valider votre parcours :

* **[Simulation](simulate-journey.md#test-users)** : utilisez la fonctionnalité de parcours **[!UICONTROL Simulation]** et les utilisateurs simulés sans profils précréés dans Adobe Experience Platform, pour prendre en charge les utilisateurs optimisés par l’IA et les utilisateurs créés manuellement.

* **[Mode test](testing-the-journey.md)** : utilisez des profils persistants marqués comme profils de test dans Adobe Experience Platform, réutilisables entre les sessions. Choisissez cette approche lorsque vous avez besoin de données cohérentes et prédéfinies. [Découvrez comment créer des profils de test](../audience/creating-test-profiles.md).

## Simulation par type de parcours {#by-journey-type}

Le panneau **[!UICONTROL Simulation]** affiche uniquement les étapes dont votre parcours a besoin. Cela dépend de la manière dont les profils entrent dans le parcours. À partir de ces facteurs, Adobe Journey Optimizer fait apparaître différentes expériences de simulation. Développez chaque type ci-dessous pour voir en quoi l’exécution diffère et quels panneaux vous utilisez.

Pour plus d’informations, voir [ Simuler votre parcours ](simulate-journey.md).

+++ Parcours par lots avec une audience de lecture


Le parcours est déclenché par une **[!UICONTROL Lecture d’audience]** et la zone de travail ne comporte aucune activité d’événement unitaire. Lors de la simulation, la population d’audience n’est pas déclenchée. Seuls les utilisateurs simulés accèdent au parcours.
Les utilisateurs simulés sélectionnés pour la simulation apparaissent dans la section **Tester les utilisateurs** :

![Panneau Simulation pour un parcours par lots avec audience en lecture seule](assets/simulate-batch.png)

Pour les parcours avec une **[!UICONTROL Lecture d&#39;audience]**, vous pouvez accéder à **[!UICONTROL Simulation rapide]** ou **[!UICONTROL Simulation manuelle]**.

![Panneau Simulation pour un parcours par lots avec audience en lecture seule](assets/simulate-14.png)

+++

+++ Parcours par lots avec audience lue et événements unitaires

Parcours de déclenchement de segment qui comprend un ou plusieurs événements unitaires le long du chemin d’accès. Vous devez d’abord déclencher les utilisateurs simulés pour qu’ils rejoignent la simulation, puis déclencher des événements pour les utilisateurs qui attendent au niveau d’un nœud d’événement.
Les utilisateurs simulés sélectionnés pour les événements de simulation et configurés sont visibles respectivement dans les sections Utilisateurs tests et Événements de test . La section Événements de test n’est pas visible tant qu’un utilisateur simulé n’a pas accédé au parcours.

![Panneau Simulation pour un parcours par lots avec audience en lecture seule](assets/simulate-batch-2.png)

Avec parcours batch avec une audience lue et des événements unitaires **, vous pouvez accéder à**[!UICONTROL  Simulation rapide ]**ou**[!UICONTROL  Simulation manuelle ]**.**

![Bouton Mode test dans l’interface de parcours](assets/simulate-12.png)

+++

+++ Parcours unitaire

Le parcours commence par un événement unitaire, et non par une audience lue. Un utilisateur simulé ne saisit pas le parcours tant que cet événement de début n’a pas été déclenché pour lui.
Les utilisateurs simulés sélectionnés pour la simulation et les événements configurés sont visibles respectivement dans les sections **Tester les utilisateurs** et **Tester les événements**. La section **Tester les utilisateurs** n’inclut pas d’action permettant de déclencher un utilisateur simulé dans le parcours. Vous déclenchez l’entrée à partir de **Événements de test**.

![Panneau Simulation pour un parcours par lots avec audience en lecture seule](assets/simulate-batch-3.png)

Avec parcours unitaire **, vous accédez directement au menu Simulation manuelle .**

![Panneau de simulation pour un parcours unitaire](assets/simulate-13.png)

+++

## Lancer la simulation {#launch}

Passez le parcours à **[!UICONTROL Simulation]** pour le tester avec des utilisateurs et utilisatrices simulés. Les tâches détaillées sont présentées dans la section [ Simuler votre parcours ](simulate-journey-2.md).

1. Dans le parcours, cliquez sur **[!UICONTROL Simuler]** et choisissez **[!UICONTROL Simuler]**.

   ![Bouton Mode test dans l’interface de parcours](assets/test-mode-simulated.png)

1. Attendez la fin de l’activation. Lorsque le parcours passe à **[!UICONTROL Simulation]**, les commandes du panneau sont désactivées et réactivées automatiquement une fois l’activation terminée.

## Limites {#limitations}

Dans cette version, la **[!UICONTROL Simulation]** peut ne pas prendre en charge toutes les activités, tous les canaux ou toutes les intégrations pris en charge par le **[!UICONTROL mode Test]** ou un parcours en direct. En outre, le comportement peut changer à mesure que la fonctionnalité se développe. Utilisez cet article pour les workflows pris en charge.

Pour en savoir plus sur les limites de la simulation, consultez les listes déroulantes ci-dessous.

+++ Restrictions au niveau du nœud

Certains nœuds empêchent le démarrage de la **[!UICONTROL Simulation]**. D’autres s’exécutent en simulation avec le comportement décrit ci-dessous. Lorsqu’un nœud doit être supprimé ou modifié avant de procéder à la simulation, mettez d’abord à jour le parcours.

| Nœud restreint | Notes |
| --- | --- |
| Événements métier | Vous ne pouvez pas exécuter des parcours commençant par un événement métier dans **[!UICONTROL Simulation]**. |
| ID supplémentaire (plusieurs reprises) | La **[!UICONTROL simulation]** ne démarre pas lorsque plusieurs reprises sont activées et qu’un même utilisateur simulé peut avoir plusieurs instances actives à la fois. |
| Nœud de décision de contenu | Supprimez ou modifiez cette activité avant de simuler le parcours. |
| Recherche de jeu de données | **[!UICONTROL Simulation]** ne prend pas en charge les recherches de jeux de données client par clé. Supprimez ou modifiez cette activité avant d&#39;exécuter une simulation. |
| Activité **[!UICONTROL Optimiser]** | **[!UICONTROL Expérience]** et **[!UICONTROL Règle de ciblage]** ne sont pas pris en charge. Supprimez ou modifiez le nœud avant de procéder à la simulation.<br><br>Les autres méthodes **[!UICONTROL Optimize]** se comportent comme suit :<br><br>**[!UICONTROL Partage en pourcentage ]**: le Journey Agent crée un utilisateur simulé par branche, et non en fonction des pourcentages de branche. Au moment de l’exécution, l’évaluation en direct sélectionne la branche qui peut différer du chemin généré. Vous ne pouvez pas simuler un choix de branche. Pour diriger les utilisateurs, utilisez l’ordre des branches sur la zone de travail. La branche supérieure est toujours choisie.<br><br>**[!UICONTROL Condition de temps]** : les conditions s’appliquent au moment de l’exécution comme dans un parcours dynamique. Par exemple, une fenêtre de 8 :00 à 20 :00 permet uniquement aux utilisateurs de passer pendant que la simulation s’exécute à l’intérieur de cette fenêtre. Vous ne pouvez pas simuler l’heure d’exécution. Définissez la condition pour qu’elle corresponde à l’heure actuelle lors du test.<br><br>**[!UICONTROL Condition de date ]**: les conditions s’appliquent au moment de l’exécution comme dans un parcours dynamique. Par exemple, la date du 8 juin 2026 permet uniquement aux utilisateurs de passer lorsque la simulation s’exécute à cette date. Vous ne pouvez pas simuler la date d’exécution. Définissez la condition sur la date actuelle lors du test.<br><br>**[!UICONTROL Limite de profil]** : les limites ne sont pas appliquées pendant la simulation. Le Journey Agent crée un utilisateur simulé par branche. Vous ne pouvez pas simuler un choix de branche. Pour diriger les utilisateurs, utilisez l’ordre des branches sur la zone de travail. La branche supérieure est toujours choisie. |
| Branchements Temporisation et Erreur | Le Journey Agent ne génère pas d’utilisateurs pour les branches temporisation ou erreur de l’activité. Les utilisateurs ne saisissent ces chemins que si une temporisation ou une erreur réelle se produit lors de la simulation. |
| Branche Temporisation (activités d’événement) | Les utilisateurs simulés sont créés, mais dans la **[!UICONTROL simulation manuelle]** le Journey Agent ne décide pas qui accède à une branche de temporisation d’événement. Contrôlez le chemin en envoyant ou non l’événement . Par exemple, pour tester une branche de temporisation, attendez la temporisation configurée et n’envoyez pas l’événement. La **[!UICONTROL simulation rapide]** peut envoyer ou différer automatiquement des événements pour couvrir les branches de temporisation. |
| Événements de réaction | Les événements de réaction s’exécutent en simulation, mais l’action doit se produire dans la vie réelle. Par exemple, une réaction **ouverture** d’e-mail nécessite l’ouverture du message de l’épreuve. Vous ne pouvez pas simuler des réactions dans l’interface utilisateur de la simulation. |
| Sources de données externes | Les appels s’exécutent pendant la simulation de la même manière que dans un parcours en direct. Les activités en aval peuvent utiliser la réponse, mais vous ne pouvez pas la simuler. Lorsqu’une valeur de réponse alimente une activité **[!UICONTROL Optimiser]**, le Journey Agent ne peut pas inventer cette sortie. Il génère uniquement des entrées pour l’appel . Par exemple, si un appel prend une ville de profil et renvoie la météo, l’agent définit une ville sur l’utilisateur simulé et l’appel en direct renvoie la météo. |
| Actions personnalisées | Le comportement correspond aux sources de données externes. Les appels sortants s’exécutent en vrai. Le Journey Agent remplit les entrées. Les sorties proviennent de la réponse active. Vous ne pouvez pas simuler des réponses. |
| Enrichissement des attributs d’audience externe | Les parcours qui utilisent des attributs personnalisés provenant de sources d’audience externes ne commencent pas dans **[!UICONTROL Simulation]** lorsque cette validation s’applique. |

+++

</br>

+++ Limites fonctionnelles

Les fonctionnalités suivantes ne sont pas prises en charge dans **[!UICONTROL Simulation]**.

| Fonctionnalité | Notes |
| --- | --- |
| Critères de sortie | Les critères de sortie ne sont pas appliqués lorsque vous exécutez **[!UICONTROL Simulation]**. |
| [!DNL Adobe Journey Optimizer] la prise de décision au sein d’une action ; par exemple, le contenu d’un e-mail avec la prise de décision Adobe Journey Optimizer | Les épreuves d’action pour le contenu qui utilise [!DNL Adobe Journey Optimizer] decisioning ne sont pas générées. |
| Simuler une réponse d’action personnalisée | [!UICONTROL Actions personnalisées] effectuez par défaut un véritable appel sortant. La simulation de la réponse afin qu’aucun appel externe ne s’exécute n’est pas prise en charge. |
| Évaluation des politiques de consentement | Le consentement ne peut pas être simulé au niveau de l’utilisateur simulé et les politiques de consentement ne sont pas évaluées lors de la simulation. |
| plafonnement et arbitrage des parcours | Non évalué ni appliqué lors de la simulation. |
| Capping de la fréquence (par canal ou type de communication) | Non évalué ni appliqué lors de la simulation. |
| Gestion, suppression et listes autorisées du processus d’opt-out | Non évalué ni appliqué lors de la simulation. |
| Sous-domaine dynamique et attributs dynamiques dans les configurations de canal | Non pris en charge. |
| Optimisation de l’heure d’envoi (STO) | Non évalué ni appliqué lors de la simulation. |
| Outil Sandbox (copie d’utilisateurs simulés dans des sandbox) | Non pris en charge. |
| Envoi de vagues dans les parcours | Non pris en charge. |
| Heures creuses | Non évalué ni appliqué lors de la simulation. |
| Privacy Service | Les utilisateurs simulés ne sont pas des profils persistants conformes au RGPD. N’incluez pas de données client réelles dans les utilisateurs simulés. |

+++

</br>

+++ Mécanismes de sécurisation quantitatifs 

Ces mécanismes de sécurisation s’appliquent à **[!UICONTROL Simulation]**. Les limites numériques sont appliquées dans l’interface du parcours et au moment de l’exécution. Les limites peuvent changer dans une version ultérieure. Si vous approchez d’un plafond, vérifiez le comportement dans votre sandbox.

| Mécanisme de sécurisation | Limite | Notes |
| --- | --- | --- |
| Nombre maximal d’utilisateurs simulés pouvant être sélectionnés et déclenchés dans un lot (parcours par lots, flux déclenchés par un événement et flux de qualification d’audience) | 20 | Comptabilisé pour chaque **[!UICONTROL Envoyer tout]** ou **[!UICONTROL Déclencher les événements sélectionnés]**, et non une limite cumulée pour l’ensemble du parcours. |
| Nombre maximal d’utilisateurs simulés par requête de génération | 50 | Nombre maximal d’utilisateurs simulés généré par Journey Agent en une seule demande par le biais de **[!UICONTROL Simulation rapide]** ou **[!UICONTROL Générer avec l’IA]** en **[!UICONTROL Simulation manuelle]**. Si le parcours comporte plus de 50 chemins d’accès **50**, le Journey Agent sélectionne de manière aléatoire les chemins d’accès pour générer ces utilisateurs simulés de 50 ****. |
| Nombre maximal d’utilisateurs simulés uniques testés au cours d’une seule exécution de simulation | 100 | Atteindre **100** utilisateurs uniques en un seul bloc d’exécution **[!UICONTROL Sélectionner des utilisateurs simulés]** pour les nouveaux utilisateurs simulés. Si vous êtes à **90**, vous pouvez ajouter au plus 10 **** avant le même bloc. |
| Nombre maximal de parcours pouvant être exécutés en même temps dans un sandbox **[!UICONTROL Simulation]** | 20 | La limite est partagée par chaque parcours **[!UICONTROL Simulation]** à la fois dans ce sandbox. |
| Nombre maximal d’utilisateurs actifs simulés dans un sandbox | 2,000 | Nombre maximal d’utilisateurs simulés pouvant exister simultanément dans le sandbox. Adobe peut ajuster cette limite en fonction des commentaires des clients. |
| Préremplissage De L’Événement (Navigateur Uniquement) | — | Vous pouvez préremplir les champs de payload d’événement uniquement dans l’interface utilisateur de la simulation basée sur un navigateur. Les valeurs préremplies restent dans ce navigateur et ne sont pas synchronisées avec d’autres navigateurs, appareils ou sessions, de sorte que vous pouvez voir différentes données de préremplissage à chaque emplacement que vous testez. |

+++
