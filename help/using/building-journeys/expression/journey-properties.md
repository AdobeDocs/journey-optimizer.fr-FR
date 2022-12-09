---
solution: Journey Optimizer
product: journey optimizer
title: Propriétés du parcours
description: En savoir plus sur les propriétés d’un parcours
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: eb1ab0ed-90bd-4613-b63d-b28693947db2
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '586'
ht-degree: 0%

---

# Attributs de propriétés du parcours {#journey-properties}

Dans l’éditeur d’expression avancé, vous trouverez la variable **Propriétés du parcours** catégorie , sous les catégories d’événement et de source de données. Cette catégorie contient des champs techniques liés au parcours pour un profil donné. Il s’agit des informations récupérées par le système à partir des parcours actifs, telles que l’identifiant du parcours ou les erreurs spécifiques rencontrées.

>[!NOTE]
>
>Les attributs de propriétés du parcours sont également disponibles dans l’éditeur d’expression simple. Voir [section](../condition-activity.md#about_condition)

![](../assets/journey-properties.png)

Vous trouverez, par exemple, des informations sur :

* version du parcours : uid de parcours, uid de version de parcours, uid d’instance, etc.
* errors: récupération des données, exécution d’actions, etc.
* étape en cours, dernière étape en cours, etc.
* profils ignorés

Vous pouvez utiliser ces champs pour créer des expressions. Pendant l’exécution du parcours, les valeurs seront récupérées directement à partir de celui-ci.

Voici quelques exemples d’utilisation :

* **Enregistrer les profils ignorés**: vous pouvez envoyer tous les profils exclus d’un message par une règle de limitation à un système tiers à des fins de journalisation. Pour ce faire, vous configurez un chemin en cas de dépassement de délai et d’erreur et ajoutez une condition pour filtrer selon un type d’erreur spécifique, par exemple : &quot;Ignorer les gens par règle de limitation&quot;. Vous pouvez ensuite transmettre les profils ignorés à un système tiers via une action personnalisée.

* **Envoyer des alertes en cas d’erreur**: vous pouvez envoyer une notification à un système tiers chaque fois qu’une erreur se produit sur un message. Pour ce faire, vous configurez un chemin en cas d’erreur, ajoutez une condition et une action personnalisée. Vous pouvez envoyer une notification sur un canal Slack, par exemple, avec la description de l’erreur rencontrée.

* **Affiner les erreurs dans les rapports** : au lieu d’avoir un seul chemin pour les messages en erreur, vous pouvez définir une condition par type d’erreur. Vous pourrez ainsi affiner le reporting et afficher toutes les données de types d’erreur.

## Liste des champs {#journey-properties-fields}

| Catégorie | Nom du champ | Libellé | Description |
|---|---|---|------------|
| Version du parcours | journeyUID | Identifiant de parcours |  |
|  | journeyVersionUID | Identifiant de version du parcours |  |
|  | journeyVersionName | Nom de la version du parcours |  |
|  | journeyVersionDescription | Description de la version du parcours |  |
|  | journeyVersion | Version du parcours |  |
| Instance de parcours | instanceUID | Identifiant d’instance de parcours | ID de l’instance |
|  | externalKey | Clé externe | Identifiant individuel déclenchant le parcours |
|  | organizationId | Identifiant de l’organisation | Organisation de la marque |
|  | sandboxName | Nom de l’environnement de test | Nom de l’environnement de test |
| Identité | profileId | Identifiant d’identité du profil | Identifiant du profil dans le parcours |
|  | namespace | Espace de noms d’identité du profil | Espace de noms du profil dans le parcours (exemple : ECID) |
| Noeud actuel | currentNodeId | Identifiant de noeud actuel | Identifiant de l’activité actuelle (noeud) |
|  | currentNodeName | Nom du noeud actuel | Nom de l’activité actuelle (noeud) |
| Noeud précédent | previousNodeId | Identifiant de noeud précédent | Identifiant de l&#39;activité précédente (noeud) |
|  | previousNodeName | Nom du noeud précédent | Nom de l’activité précédente (noeud) |
| Erreurs | lastNodeUIDInError | Dernier identifiant de noeud en erreur | Identifiant de la dernière activité (noeud) en erreur |
|  | lastNodeNameInError | Nom du dernier noeud en erreur | Nom de la dernière activité (noeud) en erreur |
|  | lastNodeTypeInError | Dernier type de noeud en erreur | Type d’erreur de la dernière activité (noeud) en erreur. Types possibles :<ul><li>Événements : Événements, Réactions, QS (exemple : Qualification de segment)</li><li>Contrôle de flux : Fin, condition, attente</li><li>Actions : Actions ACS, saut, action personnalisée</li></ul> |
|  | lastErrorCode | Dernier code d’erreur | Code d’erreur de la dernière activité (noeud) en erreur. Erreurs possibles : <ul><li>Codes d’erreur HTTP</li><li>limité</li><li>timedOut</li><li>error (exemple : par défaut en cas d’erreur inattendue. Ne devrait pas/extrêmement rarement se produire)</li></ul> |
|  | lastExecutedActionErrorCode | Code d’erreur de la dernière action exécutée | Code d’erreur de la dernière action en erreur |
|  | lastDataFetchErrorCode | Code d’erreur de dernière récupération de données | Code d’erreur de la dernière récupération de données à partir de sources de données |
| Heure | lastActionExecutionElapsedTime | Temps écoulé avant l’exécution de la dernière action | Durée d’exécution de la dernière action |
|  | lastDataFetchElapsedTime | Temps écoulé avant la dernière récupération des données | Durée d’exécution de la dernière récupération de données à partir des sources de données |
