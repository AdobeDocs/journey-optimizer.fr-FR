---
solution: Journey Optimizer
product: journey optimizer
title: Limitations de parcours
description: En savoir plus sur les limitations de parcours
feature: Journeys, Best Practices, Guardrails
topic: Content Management
role: User
level: Intermediate
keywords: parcours, limitation
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
version: Journey Orchestration
source-git-commit: de71f603b98c44d09ede5cc6bafc945f124ceb09
workflow-type: tm+mt
source-wordcount: '564'
ht-degree: 91%

---

# Limitations {#journey-limitations}

Voici les limitations liées à l&#39;utilisation des parcours.

## Limitations des actions générales {#action-limitations}

* Il n’y a pas de limite d’envoi.
* En cas d&#39;erreur, trois reprises sont systématiquement effectuées. Vous ne pouvez pas adapter le nombre de reprises en fonction du message d&#39;erreur renvoyé.
* L’événement **Réaction** intégré vous permet de réagir aux actions d’usine (voir cette [page](../building-journeys/reaction-events.md)). Si vous souhaitez réagir à un message envoyé par le biais d’une action personnalisée, vous devez configurer un événement dédié.
* Vous ne pouvez pas placer deux actions en parallèle ; vous devez les ajouter l’une après l’autre.


## Limitations des versions de parcours {#journey-versions-limitations}

* Un parcours commençant par une activité d&#39;événement dans la version_v1 ne peut pas débuter avec un autre élément qu&#39;un événement dans d&#39;autres versions. Vous ne pouvez pas débuter un parcours avec un événement **Qualification d’audience**.
* Un parcours commençant par une activité **Qualification d’audience** dans la version v1 doit toujours débuter avec une **qualification d’audience** dans d’autres versions.
* L’audience et l’espace de noms sélectionnés dans **Qualification d’audience** (premier nœud) ne peuvent pas être modifiés dans les nouvelles versions.
* La règle de rentrée doit être la même dans toutes les versions du parcours.
* Un parcours commençant par une **lecture d’audience** ne peut pas commencer par un autre événement dans les versions suivantes.

## Limites des actions personnalisées {#custom-actions-limitations}

* L’URL de l’action personnalisée ne prend pas en charge les paramètres dynamiques. 
* Seules les méthodes d’appel POST et PUT sont prises en charge. 
* Le nom du paramètre de la requête ou de l’en-tête ne doit pas commencer par « . » ou « $ ». 
* Les adresses IP ne sont pas autorisées. 
* Les adresses Adobe internes (.adobe.) ne sont pas autorisées.

## Limitations des événements {#events-limitations}

* En ce qui concerne les événements générés par le système, les données de diffusion en continu utilisées pour initier un parcours client doivent d’abord être configurées dans Journey Optimizer pour obtenir un identifiant d’orchestration unique. Cet identifiant d’orchestration doit être ajouté à la payload de diffusion en continu entrant dans Adobe Experience Platform. Cette limitation ne s’applique pas aux événements basés sur une règle.

## Limites des événements de réaction {#reaction-limitations}

* Les activités **[!UICONTROL Réaction]** doivent être placées immédiatement après une activité [action de canal](../building-journeys/journeys-message.md) dans la zone de travail du parcours. Le placement d’une activité **[!UICONTROL Attente]** ou de toute autre activité entre l’action de canal et l’activité **[!UICONTROL Réaction]** n’est pas pris en charge et peut entraîner un dysfonctionnement de la réaction comme prévu. En savoir plus dans [cette section](../building-journeys/reaction-events.md).

## Limites des sources de données {#data-sources-limitations}

* Les sources de données externes peuvent être exploitées au cours d’un parcours client pour consulter des données externes en temps réel.Ces sources doivent être utilisables via l’API REST, prendre en charge JSON et être en mesure de gérer le volume de requêtes.

## Parcours commençant en même temps qu&#39;une création de profil {#journeys-limitation-profile-creation}

Un délai est associé à la création/la mise à jour de profils basés sur l’API dans Adobe Experience Platform. La cible de niveau de service (TSL) en termes de latence est d’atteindre moins de 1 minute entre l’ingestion et le profil unifié pour le 95e percentile des demandes, avec un volume de 20K demandes par seconde (DPS).

Si un parcours est déclenché simultanément à la création d’un profil et qu’il vérifie/récupère immédiatement des informations auprès du service de profil, il est possible qu&#39;il ne fonctionne pas correctement.

Vous pouvez choisir l’une des deux solutions suivantes :

* Ajouter une activité d’attente après le premier événement pour donner à Adobe Experience Platform le temps nécessaire pour exécuter l’ingestion sur le service de profil.

* Configurer un parcours qui n’utilise pas immédiatement le profil. Par exemple, si le parcours est conçu pour confirmer la création d’un compte, l’événement d’expérience peut contenir les informations nécessaires à l’envoi du premier message de confirmation (prénom, nom, adresse e-mail, etc).

## Limitations de lecture d’audience {#read-audiences-limitations}

* Les audiences en flux continu sont toujours à jour, mais les audiences par lots ne sont pas calculées au moment de la récupération. Elles ne sont évaluées que tous les jours au moment de l’évaluation quotidienne des lots.
