---
solution: Journey Optimizer
product: journey optimizer
title: Limites du parcours
description: En savoir plus sur les limites du parcours
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '510'
ht-degree: 0%

---

# Limites {#journey-limitations}

Voici les limites liées à l’utilisation des parcours.

## Limites des actions générales

* Il n’y a pas de ralentissement de l’envoi. 
* Trois reprises sont systématiquement effectuées en cas d&#39;erreur. Vous ne pouvez pas ajuster le nombre de reprises en fonction du message d’erreur reçu. 
* La version intégrée **Réaction** vous permet de réagir aux actions d’usine (voir [page](../building-journeys/reaction-events.md)). Si vous souhaitez réagir à un message envoyé via une action personnalisée, vous devez configurer un événement dédié. 
* Vous ne pouvez pas placer deux actions en parallèle, vous devez les ajouter l’une après l’autre.

## Limites des versions de parcours {#journey-versions-limitations}

* Un parcours commençant par une activité d’événement dans v1 ne peut pas commencer par autre chose qu’un événement dans d’autres versions. Vous ne pouvez pas commencer un parcours avec un **Qualification de segment** .
* Un parcours commençant par un **Qualification de segment** l’activité dans v1 doit toujours commencer par une **Qualification de segment** dans d’autres versions.
* Le segment et l’espace de noms choisis dans **Qualification de segment** (premier noeud) ne peut pas être modifié dans les nouvelles versions.
* La règle de rentrée doit être la même dans toutes les versions de parcours.
* Un parcours commençant par un **Lecture de segment** ne peut pas commencer avec un autre événement dans les versions suivantes.
 

## Limites des actions personnalisées

* L’URL d’action personnalisée ne prend pas en charge les paramètres dynamiques. 
* Seules les méthodes d’appel POST et PUT sont prises en charge. 
* Le nom du paramètre de requête ou de l’en-tête ne doit pas commencer par &quot;.&quot; ou &quot;$&quot;. 
* Les adresses IP ne sont pas autorisées. 
* Adresses Adobe internes (.adobe.) ne sont pas autorisées.
 

## Limites des événements

* Pour les événements générés par le système, les données de diffusion en continu utilisées pour lancer un parcours client doivent d’abord être configurées dans Journey Optimizer pour obtenir un identifiant d’orchestration unique. Cet identifiant d’orchestration doit être ajouté à la charge utile de diffusion en continu entrant dans Adobe Experience Platform. Cette limitation ne s’applique pas aux événements basés sur des règles.
 

## Limites des sources de données

* Les sources de données externes peuvent être exploitées au cours d’un parcours client pour rechercher des données externes en temps réel. Ces sources doivent être utilisables via l’API REST, prendre en charge JSON et être en mesure de gérer le volume de requêtes.

## Parcours commençant en même temps qu’une création de profil {#journeys-limitation-profile-creation}

Un délai est associé à la création/mise à jour de profils basés sur l’API dans Adobe Experience Platform. La cible de niveau de service (TSL) en termes de latence est de &lt; 1 minute entre l’ingestion et le profil unifié pour le 95e percentile de requêtes, à un volume de 20K requêtes par seconde (RPS).

Si un parcours est déclenché simultanément à la création d’un profil et qu’il vérifie/récupère immédiatement des informations à partir du service de profil, il se peut qu’il ne fonctionne pas correctement.

Vous pouvez choisir l’une des deux solutions suivantes :

* Ajoutez une activité d’attente après le premier événement pour donner à Adobe Experience Platform le temps nécessaire pour effectuer l’ingestion vers le service de profil.

* Configurez un parcours qui n’exploite pas immédiatement le profil. Si, par exemple, le parcours est conçu pour confirmer la création d’un compte, l’événement d’expérience peut contenir les informations nécessaires à l’envoi du premier message de confirmation (prénom, nom, adresse électronique, etc.).

## Limites des segments de lecture

* Les segments en flux continu sont toujours à jour, mais les segments par lot ne sont pas calculés au moment de la récupération. Elles ne sont évaluées que tous les jours au moment de l’évaluation quotidienne du lot.
