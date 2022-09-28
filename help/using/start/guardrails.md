---
title: Sécurité et limitations de Journey Optimizer
description: En savoir plus sur les limitations de Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: c530905eacbdf6161f6449d7a0b39c8afaf3a321
workflow-type: tm+mt
source-wordcount: '806'
ht-degree: 100%

---

# Sécurité et limitations {#limitations}

Les droits, les limitations de produit et la sécurisation des performances sont répertoriés dans la [page de description du produit Adobe Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html){target=&quot;_blank&quot;}.

Vous trouverez ci-dessous des éléments de sécurité et des limitations supplémentaires lors de l’utilisation de [!DNL Adobe Journey Optimizer].

## Sécurisation des messages {#message-guardrails}

* Vous ne pouvez pas ajouter de pièces jointes à un e-mail avec [!DNL Journey Optimizer].
* Vous ne pouvez pas utiliser le même domaine d’envoi pour envoyer des messages depuis [!DNL Adobe Journey Optimizer] et depuis un autre produit, tel que [!DNL Adobe Campaign] ou [!DNL Adobe Marketo Engage] par exemple.


## Sécurisation de la gestion des décisions {#offer-guardrails}

Les protections des performances et les limites statiques pour la prise des décisions sont répertoriées dans la [page de description du produit de service d’application d’Adobe Offer Decisioning](https://helpx.adobe.com/legal/product-descriptions/offer-decisioning-app-service.html){target=&quot;_blank&quot;}.


## Sécurisation des pages de destination {#lp-guardrails}

* Un seul composant de **Formulaire** peut être utilisé dans une page principale unique.
* Le composant de **Formulaire** ne peut pas être utilisé dans les sous-pages.
* Vous ne pouvez pas ajouter de pré-titre à une page de destination.
* Vous ne pouvez pas sélectionner l’option **Coder le vôtre** lors de la conception d’une page de destination principale.

## Sécurisation des parcours {#journeys-guardrails}

### Actions générales {#general-actions-g}

* Il n’y a pas de limite d’envoi.
* En cas d&#39;erreur, trois reprises sont systématiquement effectuées. Vous ne pouvez pas adapter le nombre de reprises en fonction du message d&#39;erreur renvoyé.
* L’événement **Réaction** intégré vous permet de réagir aux actions d’usine. En savoir plus sur [cette page](../building-journeys/reaction-events.md). Si vous souhaitez réagir à un message envoyé par le biais d’une action personnalisée, vous devez configurer un événement dédié.
* Vous ne pouvez pas placer deux actions en parallèle ; vous devez les ajouter l’une après l’autre.
* Il existe aujourd’hui une limitation technique dans les parcours qui empêche qu’un profil soit présent plusieurs fois dans le même parcours, en même temps. Un profil peut toujours rejoindre à nouveau un parcours (en fonction d’un paramètre), mais il ne peut pas le faire tant qu’il n’a pas complètement quitté cette instance précédente du parcours.
* Dans la plupart des cas, un profil ne peut pas être présent plusieurs fois dans le même parcours, en même temps. Si la reprise est activée, un profil peut rejoindre à nouveau un parcours, mais ne peut pas le faire tant qu’il n’a pas complètement quitté cette instance précédente du parcours. [En savoir plus](../building-journeys/journey-end.md)

### Versions de parcours {#journey-versions-g}

* Un parcours commençant par une activité d&#39;événement dans la version_v1 ne peut pas débuter avec un autre élément qu&#39;un événement dans d&#39;autres versions. Vous ne pouvez pas débuter un parcours avec un événement de **qualification de segment**.
* Un parcours commençant par une activité **Qualification de segment** dans la version_v1 doit toujours débuter avec une **qualification de segment** dans d&#39;autres versions.
* Le segment et l’espace de noms sélectionnés dans **Qualification de segment** (premier nœud) ne peuvent pas être modifiés dans les nouvelles versions.
* La règle de rentrée doit être la même dans toutes les versions du parcours.
* Un parcours commençant par un événement **Lire le segment** ne peut pas commencer par un autre événement dans les versions suivantes.

### Actions personnalisées {#custom-actions-g}

* L’URL de l’action personnalisée ne prend pas en charge les paramètres dynamiques.
* Seules les méthodes d’appel POST et PUT sont prises en charge.
* Le nom du paramètre de la requête ou de l’en-tête ne doit pas commencer par « . » ou « $ »
* Les adresses IP ne sont pas autorisées.
* Les adresses Adobe internes (.adobe.) ne sont pas autorisées.

### Événements {#events-g}

* En ce qui concerne les événements générés par le système, les données de diffusion en continu utilisées pour initier un parcours client doivent d’abord être configurées dans Journey Optimizer pour obtenir un identifiant d’orchestration unique. Cet identifiant d’orchestration doit être ajouté à la payload de diffusion en continu entrant dans Adobe Experience Platform. Cette limitation ne s’applique pas aux événements basés sur une règle.
* Les événements métier ne peuvent pas être utilisés conjointement avec des événements unitaires ou des activités de qualification de segment.

### Sources de données {#data-sources-g}

* Les sources de données externes peuvent être exploitées au cours d’un parcours client pour consulter des données externes en temps réel. Ces sources doivent être utilisables via l’API REST, prendre en charge JSON et être en mesure de gérer le volume de requêtes.

### Création de parcours et de profil {#journeys-limitation-profile-creation}

Un délai est associé à la création/la mise à jour de profils basés sur l’API dans Adobe Experience Platform. La cible de niveau de service (TSL) en termes de latence est d’atteindre moins de 1 minute entre l&#39;ingestion et le profil unifié pour 95 % des demandes, avec un volume de 20K demandes par seconde (DPS).

Si un parcours est déclenché simultanément à la création d’un profil et qu’il vérifie/récupère immédiatement des informations auprès du service de profil, il est possible qu&#39;il ne fonctionne pas correctement.

Vous pouvez choisir l’une des deux solutions suivantes :

* Ajouter une activité d’attente après le premier événement pour donner à Adobe Experience Platform le temps nécessaire pour exécuter l’ingestion sur le service de profil.

* Configurer un parcours qui n’utilise pas immédiatement le profil. Par exemple, si le parcours est conçu pour confirmer la création d’un compte, l’événement d’expérience peut contenir les informations nécessaires à l’envoi du premier message de confirmation (prénom, nom, adresse e-mail, etc.).

### Lecture de segment {#read-segment-g}

* Les segments diffusés en continu sont toujours à jour, mais les segments par lots ne sont pas calculés au moment de la récupération. Ils ne sont évalués que tous les jours au moment de l’évaluation quotidienne des lots.
* Pour les parcours qui utilisent une activité Lecture de segment, un nombre maximal de parcours peut commencer exactement au même moment. Les reprises seront effectuées par le système, mais évitez d’avoir plus de cinq parcours (avec Lecture de segment, planifié ou commençant « le plus tôt possible ») commençant exactement au même moment en les répartissant dans le temps, par exemple à 5 ou 10 minutes d’intervalle.
