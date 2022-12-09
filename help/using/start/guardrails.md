---
solution: Journey Optimizer
product: journey optimizer
title: Barrières de sécurité et limites de Journey Optimizer
description: En savoir plus sur les protections Journey Optimizer
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: 9b4ab81a362c38dce5ff4b10fb301c81ed117688
workflow-type: tm+mt
source-wordcount: '854'
ht-degree: 0%

---

# Barrières de sécurité et limites {#limitations}

Les droits, les limites de produit et les barrières aux performances sont répertoriés dans la section [Page de description du produit Adobe Journey Optimizer](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target=&quot;_blank&quot;}.

Vous trouverez ci-dessous des barrières de sécurité et des limites supplémentaires lors de l’utilisation de [!DNL Adobe Journey Optimizer].

## Protections des messages {#message-guardrails}

* Vous ne pouvez pas ajouter de pièces jointes à un email avec [!DNL Journey Optimizer].
* Vous ne pouvez pas utiliser le même domaine d’envoi pour envoyer des messages depuis [!DNL Adobe Journey Optimizer] et provenant d’un autre produit, tel que [!DNL Adobe Campaign] ou [!DNL Adobe Marketo Engage] par exemple.


## Barrières de sécurité de la gestion des décisions {#offer-guardrails}

Les barrières de performance et les limites statiques pour la prise de décision sont répertoriées dans la section [Page de description du produit Adobe Offer Decisioning App Service](https://helpx.adobe.com/legal/product-descriptions/offer-decisioning-app-service.html){target=&quot;_blank&quot;}.


## Barrières de sécurité des landing pages {#lp-guardrails}

* Un seul **Formulaire** peut être utilisé dans une seule page principale.
* Le **Formulaire** ne peut pas être utilisé dans les sous-pages.
* Vous ne pouvez pas ajouter de pré-titre à une landing page.
* Vous ne pouvez pas sélectionner la variable **Codez vos propres** lors de la conception d&#39;une landing page principale.

## Barrières de sécurité du parcours {#journeys-guardrails}

### Actions générales {#general-actions-g}

* Il n’y a pas de ralentissement de l’envoi.
* Trois reprises sont systématiquement effectuées en cas d&#39;erreur. Vous ne pouvez pas ajuster le nombre de reprises en fonction du message d’erreur reçu.
* La version intégrée **Réaction** vous permet de réagir aux actions d’usine. En savoir plus dans [cette page](../building-journeys/reaction-events.md). Si vous souhaitez réagir à un message envoyé via une action personnalisée, vous devez configurer un événement dédié.
* Vous ne pouvez pas placer deux actions en parallèle, vous devez les ajouter l’une après l’autre.
* En règle générale, un profil ne peut pas être présent plusieurs fois au même moment dans le même parcours. Si la rentrée est activée, un profil peut revenir dans un parcours, mais ne peut pas le faire tant qu’il n’a pas complètement quitté cette instance précédente du parcours. [En savoir plus](../building-journeys/end-journey.md)

### Versions de parcours {#journey-versions-g}

* Un parcours commençant par une activité d’événement dans v1 ne peut pas commencer par autre chose qu’un événement dans d’autres versions. Vous ne pouvez pas commencer un parcours avec un **Qualification de segment** .
* Un parcours commençant par un **Qualification de segment** l’activité dans v1 doit toujours commencer par une **Qualification de segment** dans d’autres versions.
* Le segment et l’espace de noms choisis dans **Qualification de segment** (premier noeud) ne peut pas être modifié dans les nouvelles versions.
* La règle de rentrée doit être la même dans toutes les versions de parcours.
* Un parcours commençant par un **Lecture de segment** ne peut pas commencer avec un autre événement dans les versions suivantes.

### Actions personnalisées {#custom-actions-g}

* L’URL d’action personnalisée ne prend pas en charge les paramètres dynamiques.
* Seules les méthodes d’appel POST et PUT sont prises en charge
* Le nom du paramètre de requête ou de l’en-tête ne doit pas commencer par &quot;.&quot; ou &quot;$&quot;
* Les adresses IP ne sont pas autorisées
* Adresses Adobe internes (.adobe.) ne sont pas autorisées.

### Événements {#events-g}

* Pour les événements générés par le système, les données de diffusion en continu utilisées pour lancer un parcours client doivent d’abord être configurées dans Journey Optimizer pour obtenir un identifiant d’orchestration unique. Cet identifiant d’orchestration doit être ajouté à la charge utile de diffusion en continu entrant dans Adobe Experience Platform. Cette limitation ne s’applique pas aux événements basés sur des règles.
* Les événements professionnels ne peuvent pas être utilisés conjointement avec des événements unitaires ou des activités de qualification de segment.
* Les parcours unitaires (commençant par un événement ou une qualification de segment) incluent une barrière de sécurité qui empêche les parcours d’être déclenchés par erreur plusieurs fois pour le même événement. La rentrée du profil est temporairement bloquée par défaut pendant 5 minutes. Par exemple, si un événement déclenche un parcours à 12h01 pour un profil spécifique et qu’un autre arrive à 12h03 (s’il s’agit du même événement ou d’un autre déclenchant le même parcours), ce parcours ne redémarre pas pour ce profil.

### Sources de données {#data-sources-g}

* Les sources de données externes peuvent être exploitées au cours d’un parcours client pour rechercher des données externes en temps réel. Ces sources doivent être utilisables via l’API REST, prendre en charge JSON et être en mesure de gérer le volume de requêtes.

### Parcours et création de profil {#journeys-limitation-profile-creation}

Un délai est associé à la création/mise à jour de profils basés sur l’API dans Adobe Experience Platform. La cible de niveau de service (TSL) en termes de latence est de &lt; 1 minute entre l’ingestion et le profil unifié pour le 95e percentile de requêtes, à un volume de 20K requêtes par seconde (RPS).

Si un parcours est déclenché simultanément à la création d’un profil et qu’il vérifie/récupère immédiatement des informations à partir du service de profil, il se peut qu’il ne fonctionne pas correctement.

Vous pouvez choisir l’une des deux solutions suivantes :

* Ajoutez une activité d’attente après le premier événement pour donner à Adobe Experience Platform le temps nécessaire pour effectuer l’ingestion vers le service de profil.

* Configurez un parcours qui n’exploite pas immédiatement le profil. Si, par exemple, le parcours est conçu pour confirmer la création d’un compte, l’événement d’expérience peut contenir les informations nécessaires à l’envoi du premier message de confirmation (prénom, nom, adresse électronique, etc.).

### Lecture de segment {#read-segment-g}

* Les segments en flux continu sont toujours à jour, mais les segments par lot ne sont pas calculés au moment de la récupération. Elles ne sont évaluées que tous les jours au moment de l’évaluation quotidienne du lot.
* Pour les parcours qui utilisent une activité Lecture de segment , un nombre maximum de parcours peuvent démarrer exactement en même temps. Les reprises seront effectuées par le système, mais évitez d’avoir plus de cinq parcours (avec Lecture de segment, planifiés ou démarrés &quot;dès que possible&quot;) commençant exactement au même moment en les répartissant dans le temps, par exemple entre 5 et 10 minutes d’intervalle.

### Editeur d&#39;expression {#expression-editor}

* Les groupes de champs d’événement d’expérience ne peuvent pas être utilisés dans les parcours commençant par un segment de lecture, une qualification de segment ou une activité d’événement commercial.

