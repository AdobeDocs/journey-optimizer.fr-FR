---
title: Limites du parcours
description: En savoir plus sur les restrictions de Parcours
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 0%

---

# Limites {#journey-limitations}

![](../assets/do-not-localize/badge.png)

Voici les limites liées à l&#39;utilisation des parcours.

## Limites des listes de parcours

* Dans la liste parcours, les filtres, les recherches et la sélection de colonnes sont réinitialisés lors de l’actualisation de la page.

## Limitations des actions générales

* Il n&#39;y a pas de limitation d&#39;envoi. 
* Deux Reprises sont systématiquement effectuées en cas d&#39;erreur. Vous ne pouvez pas ajuster le nombre de Reprises en fonction du message d’erreur reçu. 
* Le événement intégré **Réaction** vous permet de réagir aux actions prêtes à l&#39;emploi (voir cette [page](../building-journeys/reaction-events.md)). Si vous souhaitez réagir à un message envoyé via une action personnalisée, vous devez configurer un événement dédié. 
* Il n&#39;y a pas d&#39;intégration productive à Adobe Campaign Classic.
* Vous ne pouvez pas placer deux actions en parallèle, vous devez les ajouter l’une après l’autre.

## Limitations des actions de message

* L&#39;activité **Message** ne vous permet pas d&#39;utiliser des données contextuelles provenant du parcours. La personnalisation des messages est effectuée directement lors de la conception du message dans Journey Optimizer.

* Lorsque vous ajoutez un message multicanal, deux messages sont envoyés.

## Limites des versions de parcours {#journey-versions-limitations}

* un parcours commençant par une activité de événement dans v1 ne peut pas début avec autre chose qu’un événement dans d’autres versions. Vous ne pouvez pas début un parcours avec un événement **Qualification de segment**.
* un parcours commençant par une activité **Qualification de segment** dans v1 doit toujours s&#39;début avec une **Qualification de segment** dans d&#39;autres versions.
* Le segment et l&#39;espace de nommage sélectionnés dans **Qualification de segment** (premier noeud) ne peuvent pas être modifiés dans les nouvelles versions.
* La règle de réadmission doit être la même dans toutes les versions de parcours.
* Un parcours commençant par un **segment de lecture** ne peut pas se début avec un autre événement dans les versions suivantes.
 

## Limitations des actions personnalisées

* L’URL d’action personnalisée ne prend pas en charge les paramètres dynamiques. 
* Seules les méthodes d’appel POST et PUT sont prises en charge. 
* Le nom du paramètre ou de l’en-tête de la requête ne doit pas être début de &quot;&quot;. ou &quot;$&quot;. 
* Les adresses IP ne sont pas autorisées. 
* Adresses d’Adobe internes (.adobe). ne sont pas autorisées.
 

## Limites des événements

* Pour les événements générés par le système, les données en flux continu utilisées pour lancer un parcours client doivent être configurées dans Journey Optimizer en premier pour obtenir un identifiant d’orchestration unique. Cet ID d’orchestration doit être ajouté à la charge utile de diffusion en flux continu entrant dans Adobe Experience Platform. Cette limitation ne s’applique pas aux événements basés sur des règles.
 

## Limitations des sources de données

* Les sources de données externes peuvent être exploitées dans un parcours client pour rechercher des données externes en temps réel. Ces sources doivent être utilisables via l’API REST, prendre en charge JSON et être en mesure de gérer le volume de requêtes.

## Parcours commençant en même temps qu’une création de profil {#journeys-limitation-profile-creation}

Un délai est associé à la création/mise à jour de profils basés sur l&#39;API dans Adobe Experience Platform. La Cible de niveau de service (TSL) en termes de latence est de &lt; 1 min entre l&#39;ingestion et le Profil unifié pour le 95e percentile de demandes, à un volume de 20K Demandes par seconde (SRP).

Si un Parcours est déclenché simultanément à la création d&#39;un profil et qu&#39;il vérifie/récupère immédiatement les informations de Profil Service, il peut ne pas fonctionner correctement.

Vous pouvez choisir l’une des deux solutions suivantes :

* Ajoutez une activité d&#39;attente après le premier événement pour donner à Adobe Experience Platform le temps nécessaire pour exécuter l&#39;assimilation à Profil Service.

* Configurez un parcours qui n’exploite pas immédiatement le profil. Par exemple, si le parcours est conçu pour confirmer la création d’un compte, le événement d’expérience peut contenir les informations nécessaires à l’envoi du premier message de confirmation (prénom, nom, adresse électronique, etc.).

## Limitations des segments de lecture

* Il n’est pas possible de déclencher un parcours basé sur un segment dans une période plus courte que 1 heure.
* Les segments en flux continu sont toujours à jour, mais les segments par lot ne sont pas calculés au moment de la récupération. Ils ne sont évalués que tous les jours au moment de l&#39;évaluation quotidienne des lots.
