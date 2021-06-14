---
title: Limites de parcours
description: En savoir plus sur les limites de parcours
feature: Parcours
topic: Gestion de contenu
role: User
level: Intermediate
source-git-commit: b58c5b527e594c03f3b415549e6b7cd15b050139
workflow-type: tm+mt
source-wordcount: '595'
ht-degree: 100%

---

# Limites {#journey-limitations}

![](../assets/do-not-localize/badge.png)

Voici les limites liées à l’utilisation des parcours.

## Limites des listes de parcours

* Dans la liste de parcours, les filtres, les recherches et la sélection de colonnes sont réinitialisés lors de l’actualisation de la page.

## Limites des actions générales

* Il n’y a pas de limite d’envoi. 
* En cas d’erreur, deux reprises sont systématiquement effectuées. Vous ne pouvez pas adapter le nombre de reprises en fonction du message d’erreur renvoyé. 
* L’événement **Réaction** intégré vous permet de réagir aux actions d’usine (voir cette [page](../building-journeys/reaction-events.md)). Si vous souhaitez réagir à un message envoyé par le biais d’une action personnalisée, vous devez configurer un événement dédié. 
* Il n’y a pas d’intégration de produit avec Adobe Campaign Classic.
* Vous ne pouvez pas placer deux actions en parallèle ; vous devez les ajouter l’une après l’autre.

## Limites des actions de message

* L’activité **Message** ne vous permet pas d’utiliser des données contextuelles provenant du parcours. La personnalisation des messages est effectuée directement lors de la conception du message dans Journey Optimizer.

* Lorsque vous ajoutez un message multicanal, deux messages sont envoyés.

## Limites des versions de parcours {#journey-versions-limitations}

* Un parcours commençant par une activité d’événement dans la version_v1 ne peut pas débuter avec un autre élément qu’un événement dans d’autres versions. Vous ne pouvez pas débuter un parcours avec un événement de **qualification de segment**.
* Un parcours commençant par une activité **Qualification de segment** dans la version_v1 doit toujours débuter avec une **qualification de segment** dans d’autres versions.

* Le segment et l’espace de noms sélectionnés dans **Qualification de segment** (premier nœud) ne peuvent pas être modifiés dans les nouvelles versions.
* La règle de nouvelle entrée doit être la même dans toutes les versions de parcours.
* Un parcours commençant par une **lecture de segment** ne peut pas commencer par un autre événement dans les versions suivantes.
 

## Limites des actions personnalisées

* L’URL de l’action personnalisée ne prend pas en charge les paramètres dynamiques. 
* Seules les méthodes d’appel POST et PUT sont prises en charge. 
* Le nom du paramètre de requête ou de l’en-tête ne doit pas commencer par « . » ou « $ ». 
* Les adresses IP ne sont pas autorisées. 
* Les adresses Adobe internes (.adobe.) ne sont pas autorisées.
 

## Limites des événements

* En ce qui concerne les événements générés par le système, les données de diffusion en continu utilisées pour initier un parcours client doivent d’abord être configurées dans Journey Optimizer pour obtenir un identifiant d’orchestration unique. Cet identifiant d’orchestration doit être ajouté à la payload de diffusion en continu entrant dans Adobe Experience Platform. Cette limitation ne s’applique pas aux événements basés sur une règle.
 

## Limites des sources de données

* Les sources de données externes peuvent être exploitées au cours d’un parcours client pour rechercher des données externes en temps réel. Ces sources doivent être utilisables via l’API REST, prendre en charge JSON et être en mesure de gérer le volume de requêtes.

## Parcours commençant en même temps qu’une création de profil {#journeys-limitation-profile-creation}

Un délai est associé à la création/la mise à jour de profils basés sur l’API dans Adobe Experience Platform. La cible de niveau de service (TSL) en termes de latence est d’atteindre moins de 1 minute entre l&#39;ingestion et le profil unifié pour 95 % des demandes, avec un volume de 20K demandes par seconde (DPS).

Si un parcours est déclenché simultanément à la création d’un profil et qu’il vérifie/récupère immédiatement des informations auprès du service de profil, il est possible qu&#39;il ne fonctionne pas correctement.

Vous pouvez choisir l’une des deux solutions suivantes :

* Ajouter une activité d’attente après le premier événement pour donner à Adobe Experience Platform le temps nécessaire pour exécuter l’ingestion sur le service de profil.

* Configurer un parcours qui n’utilise pas immédiatement le profil. Par exemple, si le parcours est conçu pour confirmer la création d’un compte, l’événement d’expérience peut contenir les informations nécessaires à l’envoi du premier message de confirmation (prénom, nom, adresse électronique, etc.).

## Limites de lecture de segment

* Il n’est pas possible de déclencher un parcours basé sur les segments dans un délai inférieur à 1 heure.
* Les segments diffusés en continu sont toujours à jour, mais les segments par lots ne sont pas calculés au moment de la récupération. Ils ne sont évalués que tous les jours au moment de l’évaluation quotidienne des lots.
