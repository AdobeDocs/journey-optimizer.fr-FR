---
title: Limites du parcours
description: En savoir plus sur les restrictions de Parcours
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '592'
ht-degree: 70%

---

# Limites {#journey-limitations}

![](../assets/do-not-localize/badge.png)

Voici les limites liées à l&#39;utilisation des parcours.

## Limites des listes de parcours

* Dans la liste parcours, les filtres, les recherches et la sélection de colonnes sont réinitialisés lors de l’actualisation de la page.

## Limites des actions générales

* Il n’y a pas de limite d’envoi. 
* En cas d’erreur, deux reprises sont systématiquement effectuées. Vous ne pouvez pas adapter le nombre de reprises en fonction du message d’erreur renvoyé. 
* L’événement **Réaction** intégré vous permet de réagir aux actions d’usine (voir cette [page](../building-journeys/reaction-events.md)). Si vous souhaitez réagir à un message envoyé par le biais d’une action personnalisée, vous devez configurer un événement dédié. 
* Il n’y a pas d’intégration de produit avec Adobe Campaign Classic.
* Vous ne pouvez pas placer deux actions en parallèle, vous devez les ajouter l’une après l’autre.

## Limitations des actions de message

* L&#39;activité **Message** ne vous permet pas d&#39;utiliser des données contextuelles provenant du parcours. La personnalisation des messages est effectuée directement lors de la conception du message dans Journey Optimizer.

* Lorsque vous ajoutez un message multicanal, deux messages sont envoyés.

## Limites des versions de parcours {#journey-versions-limitations}

* Un parcours commençant par une activité d’événement dans la version_v1 ne peut pas débuter avec un autre élément qu’un événement dans d’autres versions. Vous ne pouvez pas débuter un parcours avec un événement de **qualification de segment**.
* Un parcours commençant par une activité **Qualification de segment** dans la version_v1 doit toujours débuter avec une **qualification de segment** dans d’autres versions.

* Le segment et l’espace de noms sélectionnés dans **Qualification de segment** (premier nœud) ne peuvent pas être modifiés dans les nouvelles versions.
* La règle de nouvelle entrée doit être la même dans toutes les versions de parcours.
* Un parcours commençant par un **segment de lecture** ne peut pas se début avec un autre événement dans les versions suivantes.
 

## Limites des actions personnalisées

* L’URL de l’action personnalisée ne prend pas en charge les paramètres dynamiques. 
* Seules les méthodes d’appel POST et PUT sont prises en charge. 
* Le nom du paramètre de requête ou de l’en-tête ne doit pas commencer par « . » or &quot;$&quot;. 
* Les adresses IP ne sont pas autorisées. 
* Les adresses Adobe internes (.adobe.) ne sont pas autorisées.
 

## Limites des événements

* Pour les événements générés par le système, les données en flux continu utilisées pour lancer un parcours client doivent être configurées dans Journey Optimizer en premier pour obtenir un identifiant d’orchestration unique.Cet identifiant d’orchestration doit être ajouté à la payload de diffusion en continu entrant dans Adobe Experience Platform. Cette limitation ne s’applique pas aux événements basés sur une règle.
 

## Limites des sources de données

* Les sources de données externes peuvent être exploitées au cours d’un parcours client pour rechercher des données externes en temps réel. Ces sources doivent être utilisables via l’API REST, prendre en charge JSON et être en mesure de gérer le volume de requêtes.

## Parcours commençant en même temps qu’une création de profil {#journeys-limitation-profile-creation}

Un délai est associé à la création/la mise à jour de profils basés sur l’API dans Adobe Experience Platform. La cible de niveau de service (TSL) en termes de latence est d’atteindre moins de 1 minute entre l&#39;ingestion et le profil unifié pour 95 % des demandes, avec un volume de 20K demandes par seconde (DPS).

Si un parcours est déclenché simultanément à la création d’un profil et qu’il vérifie/récupère immédiatement des informations auprès du service de profil, il est possible qu&#39;il ne fonctionne pas correctement.

Vous pouvez choisir l’une des deux solutions suivantes :

* Ajouter une activité d’attente après le premier événement pour donner à Adobe Experience Platform le temps nécessaire pour exécuter l’ingestion sur le service de profil.

* Configurer un parcours qui n’utilise pas immédiatement le profil. Par exemple, si le parcours est conçu pour confirmer la création d’un compte, l’événement d’expérience peut contenir les informations nécessaires à l’envoi du premier message de confirmation (prénom, nom, adresse électronique, etc.).

## Limitations des segments de lecture

* Il n’est pas possible de déclencher un parcours basé sur un segment dans une période plus courte que 1 heure.
* Les segments en flux continu sont toujours à jour, mais les segments par lot ne sont pas calculés au moment de la récupération. Ils ne sont évalués que tous les jours au moment de l&#39;évaluation quotidienne des lots.
