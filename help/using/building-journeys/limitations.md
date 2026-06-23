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
feature_v2: []
subfeature_v2: []
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 1276
ht-degree: 39%

---

# Limites {#journey-limitations}

>[!BEGINSHADEBOX]

**Sur cette page :** passez en revue les limitations et les mécanismes de sécurisation qui s’appliquent aux parcours, y compris les actions, les versions, les actions personnalisées, les événements et les sources de données.

>[!ENDSHADEBOX]

Voici les limitations liées à l&#39;utilisation des parcours.

## Limitations des actions générales {#action-limitations}

* Il n’y a pas de limite d’envoi.
* En cas d’erreur, trois reprises sont systématiquement effectuées. Vous ne pouvez pas adapter le nombre de reprises en fonction du message d&#39;erreur renvoyé.
* L’événement **Réaction** intégré vous permet de réagir aux actions prêtes à l’emploi (voir cette [page](../building-journeys/reaction-events.md)). Si vous souhaitez réagir à un message envoyé par le biais d’une action personnalisée, vous devez configurer un événement dédié.
* Vous ne pouvez pas placer deux actions en parallèle ; vous devez les ajouter l’une après l’autre.


## Limitations des versions de parcours {#journey-versions-limitations}

* Un parcours commençant par une activité d’événement dans la version_v1 ne peut pas débuter avec un autre élément qu’un événement dans d’autres versions. Vous ne pouvez pas débuter un parcours avec un événement **Qualification d’audience**.
* Un parcours commençant par une activité **Qualification d’audience** dans la version v1 doit toujours débuter avec une **qualification d’audience** dans d’autres versions.
* L’audience et l’espace de noms sélectionnés dans **Qualification d’audience** (premier nœud) ne peuvent pas être modifiés dans les nouvelles versions.
* La règle de rentrée doit être la même dans toutes les versions du parcours.
* Un parcours commençant par une **lecture d’audience** ne peut pas commencer par un autre événement dans les versions suivantes.

## Limites des actions personnalisées {#custom-actions-limitations}

* L’URL de l’action personnalisée ne prend pas en charge les paramètres dynamiques. 
* Seules les méthodes d’appel POST et PUT sont prises en charge. 
* Le nom du paramètre de requête ou de l’en-tête ne doit pas commencer par « . » ou « $ ». 
* Les adresses IP ne sont pas autorisées. 
* Les adresses Adobe internes (.adobe.) ne sont pas autorisées.

## Limitations des événements {#events-limitations}

* En ce qui concerne les événements générés par le système, les données de diffusion en continu utilisées pour initier un parcours client doivent d’abord être configurées dans Journey Optimizer pour obtenir un identifiant d’orchestration unique. Cet identifiant d’orchestration doit être ajouté à la payload de diffusion en continu entrant dans [!DNL Adobe Experience Platform]. Cette limitation ne s’applique pas aux événements basés sur une règle.

## Limites des événements de réaction {#reaction-limitations}

* Les activités **[!UICONTROL Réaction]** doivent être placées immédiatement après une activité [action de canal](../building-journeys/journey-action.md) dans la zone de travail du parcours. Le placement d’une activité **[!UICONTROL Attente]** ou de toute autre activité entre l’action de canal et l’activité **[!UICONTROL Réaction]** n’est pas pris en charge et peut entraîner un dysfonctionnement de la réaction. En savoir plus dans [cette section](../building-journeys/reaction-events.md).

## Limites des sources de données {#data-sources-limitations}

* Les sources de données externes peuvent être exploitées au cours d’un parcours client pour consulter des données externes en temps réel. Ces sources doivent être utilisables via l’API REST, prendre en charge JSON et être en mesure de gérer le volume de requêtes.

## Parcours commençant en même temps qu&#39;une création de profil {#journeys-limitation-profile-creation}

Un délai est associé à la création/mise à jour de profil basé sur l’API dans [!DNL Adobe Experience Platform]. La cible de niveau de service (TSL) en termes de latence est d’atteindre moins de 1 minute entre l’ingestion et le profil unifié pour le 95e percentile des demandes, avec un volume de 20K demandes par seconde (DPS).

Si un parcours est déclenché simultanément à la création d’un profil et qu’il vérifie/récupère immédiatement des informations auprès du service de profil, il est possible qu&#39;il ne fonctionne pas correctement.

Vous pouvez choisir l’une des deux solutions suivantes :

* Ajoutez une activité d’attente après le premier événement pour [!DNL Adobe Experience Platform] donner le temps nécessaire pour effectuer l’ingestion sur le service de profil.

* Configurer un parcours qui n’utilise pas immédiatement le profil. Par exemple, si le parcours est conçu pour confirmer la création d’un compte, l’événement d’expérience peut contenir les informations nécessaires à l’envoi du premier message de confirmation (prénom, nom, adresse e-mail, etc).

## Limitations de lecture d’audience {#read-audiences-limitations}

* Les audiences en flux continu sont toujours à jour, mais les audiences par lots ne sont pas calculées au moment de la récupération. Elles ne sont évaluées que tous les jours au moment de l’évaluation quotidienne des lots.

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page répertorie les limitations techniques strictes qui s’appliquent aux actions de parcours, aux versions de parcours, aux actions personnalisées, aux événements, aux événements de réaction, aux sources de données et à la lecture d’audience dans Adobe Journey Optimizer.

**Intentions:**

* Comprendre les limites d’envoi et de reprise pour les actions de parcours
* Découvrez les transitions de version de parcours autorisées ou bloquées
* Identifier les restrictions sur la configuration de l’URL, de la méthode et de l’en-tête des actions personnalisées
* Comprendre les exigences en matière de sources de données pour l’intégration de systèmes externes
* Éviter les problèmes de minutage lors du démarrage d’un parcours au même moment que la création d’un profil

**Glossaire:**

* **Événement de réaction** : activité de parcours qui écoute l’interaction d’un profil avec une action de canal (par exemple, ouverture d’e-mail ou clic). Elle doit être placée immédiatement après l’activité d’action de canal. *(spécifique au produit)*
* **Événement basé sur des règles** : type d’événement où le déclencheur est défini par une condition logique plutôt que par un identifiant d’orchestration généré par le système. *(spécifique au produit)*
* **SLT (Service Level Target)** : référence de latence pour la création/mise à jour de profils basés sur les API dans Adobe Experience Platform, soit moins d’une minute entre l’ingestion et le profil unifié, au 95e centile pour 20K RPS.

**Mécanismes de sécurisation :**

* Aucune limitation d’envoi n’est appliquée ; trois reprises sont automatiquement effectuées en cas d’erreur et ne peuvent pas être ajustées
* Deux actions ne peuvent pas s’exécuter en parallèle. Elles doivent être ajoutées de manière séquentielle.
* Un parcours commençant par une activité d&#39;événement dans la version_v1 ne peut pas commencer par une activité autre qu&#39;un événement dans les versions ultérieures
* Un parcours commençant par une qualification d’audience dans la version_v1 doit toujours commencer par une qualification d’audience dans toutes les versions ultérieures ; l’audience et l’espace de noms ne peuvent pas être modifiés
* Un parcours commençant par Lecture d’audience ne peut pas commencer par un événement différent dans les versions suivantes
* L’URL d’action personnalisée ne prend pas en charge les paramètres dynamiques. Seules les méthodes d’appel POST et PUT sont prises en charge
* Le paramètre de requête d’action personnalisée et les noms des en-têtes ne doivent pas commencer par « . » ou « $ »; adresses IP et adresses Adobe internes (.adobe.) ne sont pas autorisées.
* Les activités Réaction doivent être placées immédiatement après une activité d’action de canal. L’insertion d’une activité Attente ou autre entre elles n’est pas prise en charge
* Les sources de données externes doivent être accessibles via l’API REST, prendre en charge JSON et gérer le volume des requêtes
* Les audiences par lots ne sont évaluées qu’une seule fois par jour au moment de l’évaluation quotidienne des lots. Elles ne sont pas recalculées au moment de la récupération
* Lorsqu’un parcours est déclenché simultanément à la création d’un profil, les données de profil peuvent ne pas encore être disponibles en raison de la latence d’ingestion de Platform

**Terminologie:**

* Nom canonique : limitations de Parcours — Acronyme : none — variantes : mécanismes de sécurisation de parcours, restrictions de parcours
* Ne confondez pas : « Limitation de l’événement de réaction » ≠ « Limitation de l’action générale » - L’événement de réaction doit être placé directement après une action de canal ; la limitation de l’action générale couvre les reprises, le parallélisme et le ralentissement

**FAQ:**

* **Q : Combien de fois Journey Optimizer tente-t-il de relancer une action ayant échoué ?** — Trois reprises sont effectuées automatiquement ; le nombre de reprises ne peut pas être configuré.
* **Q : Puis-je placer une activité Attente entre une action de canal et un événement Réaction ?** — Non ; l&#39;événement de réaction doit être placé immédiatement après l&#39;activité d&#39;action de canal. L’ajout d’une activité entre les deux n’est pas pris en charge et peut entraîner le dysfonctionnement attendu de l’événement de réaction.
* **Q : Puis-je modifier le premier type d’événement lors de la création d’une nouvelle version de parcours ?** — Non ; le mécanisme d&#39;entrée défini dans v1 doit être conservé dans toutes les versions ultérieures. Un parcours commençant par un événement doit continuer à commencer par un événement, et un parcours commençant par la qualification d’audience doit toujours commencer par la qualification d’audience.
* **Q : Pourquoi mon parcours ne fonctionne-t-il pas lorsqu’il est déclenché en même temps que la création d’un profil ?** — La création de profils via l’API présente une latence avant que les données ne soient disponibles dans le profil unifié (SLT &lt; 1 minute au 95e percentile). L’ajout d’une activité Attente après le premier événement donne à Platform le temps de terminer l’ingestion.
* **Q : Les audiences de diffusion en continu sont-elles toujours à jour dans les parcours ?** — Oui ; les audiences de streaming sont toujours à jour. Toutefois, les audiences par lots ne sont évaluées qu’une seule fois par jour au moment de l’évaluation quotidienne des lots, et non au moment de la récupération.

+++
