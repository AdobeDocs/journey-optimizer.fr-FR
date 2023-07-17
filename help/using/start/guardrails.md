---
solution: Journey Optimizer
product: journey optimizer
title: Mécanismes de sécurisation et limitations de Journey Optimizer
description: En savoir plus sur les mécanismes de sécurisation de Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 5d59f21c-f76e-45a9-a839-55816e39758a
source-git-commit: e0f2a96054886737861e261173f68933cab56e99
workflow-type: tm+mt
source-wordcount: '1119'
ht-degree: 75%

---

# Mécanismes de sécurisation et limitations {#limitations}

Les droits, les limitations de produit et la sécurisation des performances sont répertoriés dans la [page de description du produit Adobe Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

Vous devez également connaître les [mécanismes de sécurisation pour les données du profil client en temps réel avant de commencer](https://experienceleague.adobe.com/docs/experience-platform/profile/guardrails.html?lang=fr){target="_blank"}.

Vous trouverez ci-dessous des mécanismes de sécurisation et des limitations supplémentaires lors de l’utilisation d’[!DNL Adobe Journey Optimizer].

## Navigateurs pris en charge {#browsers}

L&#39;interface d&#39;Adobe [!DNL Journey Optimizer] est conçue pour fonctionner de manière optimale avec la dernière version de Google Chrome. Vous pouvez rencontrer des problèmes lors de l&#39;utilisation de certaines fonctions sur des versions plus anciennes ou d&#39;autres navigateurs.

## Mécanismes de sécurisation des messages {#message-guardrails}

* Vous ne pouvez pas ajouter de pièces jointes à un e-mail avec [!DNL Journey Optimizer].
* Vous ne pouvez pas utiliser le même domaine d’envoi pour envoyer des messages depuis [!DNL Adobe Journey Optimizer] et depuis un autre produit, tel que [!DNL Adobe Campaign] ou [!DNL Adobe Marketo Engage] par exemple.


## Mécanismes de sécurisation des pages de destination {#lp-guardrails}

* Un seul composant de **Formulaire** peut être utilisé dans une page principale unique.
* Le composant de **Formulaire** ne peut pas être utilisé dans les sous-pages.
* Vous ne pouvez pas ajouter de pré-titre à une page de destination.
* Vous ne pouvez pas sélectionner l’option **Coder le vôtre** lors de la conception d’une page de destination principale.

## Mécanismes de sécurisation des parcours {#journeys-guardrails}

### Mécanismes de sécurisation généraux des parcours {#journeys-guardrails-journeys}

* Le nombre d’activités d’un parcours est désormais limité à 50. Le nombre d’activités s’affiche dans la section supérieure gauche de la zone de travail du parcours. Cela permet de faciliter la lisibilité, l’assurance qualité et la résolution des problèmes.
* Lorsque vous publiez des parcours, nous les mettons automatiquement à l’échelle et les ajustons pour garantir une stabilité et un débit maximaux. Lorsque vous approchez du jalon de 100 parcours actifs à la fois, une notification s’affiche dans l’interface utilisateur pour cette réalisation. Si cette notification s’affiche et que vous devez étendre vos parcours au-delà de 100 parcours actifs à la fois, créez un ticket pour l’assistance clientèle et nous vous aiderons à atteindre vos objectifs.

### Actions générales {#general-actions-g}

* Il n’y a pas de limite d’envoi.
* En cas d&#39;erreur, trois reprises sont systématiquement effectuées. Vous ne pouvez pas adapter le nombre de reprises en fonction du message d&#39;erreur renvoyé.
* L’événement **Réaction** intégré vous permet de réagir aux actions d’usine. En savoir plus sur [cette page](../building-journeys/reaction-events.md). Si vous souhaitez réagir à un message envoyé par le biais d’une action personnalisée, vous devez configurer un événement dédié.
* Vous ne pouvez pas placer deux actions en parallèle ; vous devez les ajouter l’une après l’autre.
* Un profil ne peut pas être présent plusieurs fois dans le même parcours, en même temps. Si la reprise est activée, un profil peut rejoindre à nouveau un parcours, mais ne peut pas le faire tant qu’il n’a pas complètement quitté cette instance précédente du parcours. [En savoir plus](../building-journeys/end-journey.md)

### Versions de parcours {#journey-versions-g}

* Un parcours commençant par une activité d&#39;événement dans la version_v1 ne peut pas débuter avec un autre élément qu&#39;un événement dans d&#39;autres versions. Vous ne pouvez pas commencer un parcours avec un **Qualification de l’audience** .
* Un parcours commençant par un **Qualification de l’audience** l’activité dans v1 doit toujours commencer par une **Qualification de l’audience** dans d’autres versions.
* L’audience et l’espace de noms sélectionnés dans **Qualification de l’audience** (premier noeud) ne peut pas être modifié dans les nouvelles versions.
* La règle de rentrée doit être la même dans toutes les versions du parcours.
* Un parcours commençant par un **Lecture d’audience** ne peut pas commencer avec un autre événement dans les versions suivantes.
* Vous ne pouvez pas créer de version d’un parcours d’audience de lecture avec lecture incrémentielle. Vous devez dupliquer le parcours.

### Actions personnalisées {#custom-actions-g}

* L’URL de l’action personnalisée ne prend pas en charge les paramètres dynamiques.
* Seules les méthodes d’appel POST et PUT sont prises en charge.
* Le nom du paramètre de la requête ou de l’en-tête ne doit pas commencer par « . » ou « $ »
* Les adresses IP ne sont pas autorisées.
* Les adresses d’Adobe internes (`.adobe.*`) ne sont pas autorisées dans les URL et les API.
* Les actions personnalisées intégrées ne peuvent pas être supprimées.

### Événements {#events-g}

* En ce qui concerne les événements générés par le système, les données de diffusion en continu utilisées pour initier un parcours client doivent d’abord être configurées dans Journey Optimizer pour obtenir un identifiant d’orchestration unique. Cet identifiant d’orchestration doit être ajouté à la payload de diffusion en continu entrant dans Adobe Experience Platform. Cette limitation ne s’applique pas aux événements basés sur une règle.
* Les événements professionnels ne peuvent pas être utilisés conjointement avec des événements unitaires ou des activités de qualification d’audience.
* Les parcours unitaires (commençant par un événement ou une qualification d’audience) incluent une barrière de sécurité qui empêche les parcours d’être déclenchés par erreur plusieurs fois pour le même événement. La reprise du profil est temporairement bloquée par défaut pendant 5 minutes. Par exemple, si un événement déclenche un parcours à 12 h 01 pour un profil spécifique et qu’un autre arrive à 12 h 03 (qu’il s’agisse du même événement ou d’un autre déclenchant le même parcours), ce parcours ne reprendra pas pour ce profil.
* Journey Optimizer exige que les événements soient diffusés en continu vers Data Collection Core Service (DCCS) pour pouvoir déclencher un parcours. Les événements ingérés par lot ou les événements provenant de jeux de données Journey Optimizer internes (commentaires des messages, tracking e-mail, etc.) ne peuvent pas être utilisés pour déclencher un parcours. Pour les cas d’utilisation où vous ne pouvez pas obtenir d’événements diffusés en continu, créez une audience basée sur ces événements et utilisez la variable **Lecture d’audience** à la place. La qualification de l’audience peut être techniquement utilisée, mais peut entraîner des défis en aval en fonction des actions utilisées.

### Sources de données {#data-sources-g}

* Les sources de données externes peuvent être exploitées au cours d’un parcours client pour consulter des données externes en temps réel. Ces sources doivent être utilisables via l’API REST, prendre en charge JSON et être en mesure de gérer le volume de requêtes.
* Les adresses d’Adobe internes (`.adobe.*`) ne sont pas autorisées dans les URL et les API.

### Création de parcours et de profil {#journeys-limitation-profile-creation}

Un délai est associé à la création/la mise à jour de profils basés sur l’API dans Adobe Experience Platform. La cible de niveau de service (TSL) en termes de latence est d’atteindre moins de 1 minute entre l&#39;ingestion et le profil unifié pour 95 % des demandes, avec un volume de 20K demandes par seconde (DPS).

Si un parcours est déclenché simultanément à la création d’un profil et qu’il vérifie/récupère immédiatement des informations auprès du service de profil, il est possible qu&#39;il ne fonctionne pas correctement.

Vous pouvez choisir l’une des deux solutions suivantes :

* Ajouter une activité d’attente après le premier événement pour donner à Adobe Experience Platform le temps nécessaire pour exécuter l’ingestion sur le service de profil.

* Configurer un parcours qui n’utilise pas immédiatement le profil. Par exemple, si le parcours est conçu pour confirmer la création d’un compte, l’événement d’expérience peut contenir les informations nécessaires à l’envoi du premier message de confirmation (prénom, nom, adresse e-mail, etc.).

### Lecture d&#39;audience {#read-segment-g}

* Les audiences diffusées en continu sont toujours à jour, mais les audiences par lots ne sont pas calculées au moment de la récupération. Ils ne sont évalués que tous les jours au moment de l’évaluation quotidienne des lots.
* Pour les parcours qui utilisent une activité Lecture d’audience , un nombre maximum de parcours peut démarrer exactement en même temps. Les reprises seront effectuées par le système, mais évitez d’avoir plus de cinq parcours (avec Lecture d’audience, planifié ou commençant &quot;dès que possible&quot;) à partir exactement en même temps en les répartissant dans le temps, par exemple entre 5 et 10 minutes d’intervalle.

### Éditeur d’expression {#expression-editor}

* Les groupes de champs d’événement d’expérience ne peuvent pas être utilisés dans les parcours commençant par une audience de lecture, une qualification d’audience ou une activité d’événement commercial. Vous devez créer une audience et utiliser une condition d’inaudience dans le parcours.

