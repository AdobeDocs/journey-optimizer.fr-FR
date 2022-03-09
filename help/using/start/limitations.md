---
title: Limitations de Journey Optimizer
description: En savoir plus sur les limitations de Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 80de53e62da5fc3b0543ee09327e11edd277b234
workflow-type: tm+mt
source-wordcount: '615'
ht-degree: 94%

---

# Limitations {#limitations}

Les droits, les limitations de produit et la sécurisation des performance sont répertoriés dans la [page de description du produit Adobe Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html){target=&quot;_blank&quot;}.

Vous trouverez ci-dessous des limitations supplémentaires lors de l’utilisation de [!DNL Adobe Journey Optimizer].

## Limitations des messages {#limitations-messages}

* Vous ne pouvez pas ajouter de pièces jointes à un e-mail avec [!DNL Journey Optimizer].
* La fonctionnalité E-mail Cci n’est pas prise en charge dans [!DNL Journey Optimizer].
* Vous ne pouvez pas utiliser le même domaine d’envoi pour envoyer des messages depuis [!DNL Adobe Journey Optimizer] et depuis un autre produit, tel que [!DNL Adobe Campaign] ou [!DNL Adobe Marketo Engage] par exemple.

## Limites des landing pages {#limitations-lp}

* Un seul **Formulaire** peut être utilisé dans une seule Principale page.
* Le **Formulaire** ne peut pas être utilisé dans les sous-pages.
* Vous ne pouvez pas ajouter de pré-titre à une landing page.

<!--You cannot select the **Code your own** option when designing a landing primary page.-->

## Limitations dans les parcours {#limitations-journeys}

### Actions générales {#general-actions}

* Il n’y a pas de limite d’envoi.
* En cas d&#39;erreur, trois reprises sont systématiquement effectuées. Vous ne pouvez pas adapter le nombre de reprises en fonction du message d&#39;erreur renvoyé.
* L’événement **Réaction** intégré vous permet de réagir aux actions d’usine. En savoir plus sur [cette page](../building-journeys/reaction-events.md). Si vous souhaitez réagir à un message envoyé par le biais d’une action personnalisée, vous devez configurer un événement dédié.
* Vous ne pouvez pas placer deux actions en parallèle ; vous devez les ajouter l’une après l’autre.

### Action Message {#message-action}

* Lorsque vous ajoutez un message multicanal, deux messages sont envoyés.

### Versions de parcours {#journey-versions-limitations}

* Un parcours commençant par une activité d&#39;événement dans la version_v1 ne peut pas débuter avec un autre élément qu&#39;un événement dans d&#39;autres versions. Vous ne pouvez pas débuter un parcours avec un événement de **qualification de segment**.
* Un parcours commençant par une activité **Qualification de segment** dans la version_v1 doit toujours débuter avec une **qualification de segment** dans d&#39;autres versions.
* Le segment et l&#39;espace de noms sélectionnés dans **Qualification de segment** (premier nœud) ne peuvent pas être modifiés dans les nouvelles versions.
* La règle de nouvelle entrée doit être la même dans toutes les versions de parcours.
* Un parcours commençant par un événement **Lire le segment** ne peut pas commencer par un autre événement dans les versions suivantes.

### Actions personnalisées {#custom-actions}

* L’URL de l’action personnalisée ne prend pas en charge les paramètres dynamiques.
* Seules les méthodes d’appel POST et PUT sont prises en charge.
* Le nom du paramètre de la requête ou de l’en-tête ne doit pas commencer par « . » ou « $ »
* Les adresses IP ne sont pas autorisées.
* Les adresses Adobe internes (.adobe.) ne sont pas autorisées.

### Événements {#events}

* En ce qui concerne les événements générés par le système, les données de diffusion en continu utilisées pour initier un parcours client doivent d’abord être configurées dans Journey Optimizer pour obtenir un identifiant d’orchestration unique. Cet identifiant d’orchestration doit être ajouté à la payload de diffusion en continu entrant dans Adobe Experience Platform. Cette limitation ne s’applique pas aux événements basés sur une règle.

### Sources de données  {#data-sources}

* Les sources de données externes peuvent être exploitées au cours d’un parcours client pour consulter des données externes en temps réel. Ces sources doivent être utilisables via l’API REST, prendre en charge JSON et être en mesure de gérer le volume de requêtes.

### Parcours commençant en même temps qu&#39;une création de profil {#journeys-limitation-profile-creation}

Un délai est associé à la création/la mise à jour de profils basés sur l’API dans Adobe Experience Platform. La cible de niveau de service (TSL) en termes de latence est d’atteindre moins de 1 minute entre l&#39;ingestion et le profil unifié pour 95 % des demandes, avec un volume de 20K demandes par seconde (DPS).

Si un parcours est déclenché simultanément à la création d’un profil et qu’il vérifie/récupère immédiatement des informations auprès du service de profil, il est possible qu&#39;il ne fonctionne pas correctement.

Vous pouvez choisir l’une des deux solutions suivantes :

* Ajouter une activité d’attente après le premier événement pour donner à Adobe Experience Platform le temps nécessaire pour exécuter l’ingestion sur le service de profil.

* Configurer un parcours qui n’utilise pas immédiatement le profil. Par exemple, si le parcours est conçu pour confirmer la création d’un compte, l’événement d’expérience peut contenir les informations nécessaires à l’envoi du premier message de confirmation (prénom, nom, adresse électronique, etc.).

### Lecture de segment {#read-segment}

* Les segments diffusés en continu sont toujours à jour, mais les segments par lots ne sont pas calculés au moment de la récupération. Ils ne sont évalués que tous les jours au moment de l’évaluation quotidienne des lots.
