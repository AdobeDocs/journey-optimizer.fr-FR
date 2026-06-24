---
solution: Journey Optimizer
product: journey optimizer
title: Migrer des audiences par lots à partir des parcours de qualification d’audience
description: Découvrez comment migrer les parcours qui utilisent des audiences par lots dans un nœud de qualification d’audience avant la date d’application d’août 2026.
feature: Journeys, Activities, Audiences
topic: Content Management
role: User
level: Intermediate
keywords: qualification d’audience, audience par lots, obsolescence, migration, lecture d’audience, diffusion en continu d’audience
exl-id: f3c2a7d1-b58e-4a92-c3d5-0e871f2a9b4c
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: ad78185d-8f79-40ad-9bad-cbde74af74ee
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
source-git-commit: cea41add5b86adb3b447ce606e73248adce0f731
workflow-type: tm+mt
source-wordcount: 869
ht-degree: 0%

---


# Migrer des audiences par lots à partir des parcours de qualification d’audience {#aq-batch-migration}

À compter d’août 2026, Journey Optimizer bloquera la publication pour les parcours qui utilisent une audience par lots dans un nœud de qualification d’audience. Identifiez votre cas d’utilisation ci-dessous et suivez le chemin de migration recommandé.

>[!CAUTION]
>
>**Date d’application : août 2026.** Les nouveaux parcours, les brouillons et les doublons utilisant une audience par lots dans un nœud Qualification de l’audience ne peuvent pas être publiés après cette date. Un avertissement de validation est déjà affiché dans la zone de travail de parcours depuis la version de juin 2026.

## Pourquoi ce changement ? {#why}

Le nœud **[Qualification d’audience](audience-qualification-events.md)** est conçu pour réagir en temps quasi réel lorsque des profils individuels entrent ou sortent d’une audience. Les événements de qualification arrivent en continu, un par un. Il est destiné aux **[audiences en flux continu](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer)**.

Lorsqu’une audience par lots est utilisée à la place avec un nœud Qualification de l’audience , tous les événements de qualification arrivent simultanément pendant la fenêtre d’ingestion. Cela peut entraîner des dizaines de milliers, voire des millions d’entrées de parcours en même temps, ce qui entraîne une forte pression sur le système et un comportement imprévisible des systèmes en aval. Il ne s’agit pas de la conception prévue du nœud Qualification de l’audience .

L’activité **[Lecture d’audience](read-audience.md)** est l’outil approprié pour les cas d’utilisation par lots : elle est conçue pour gérer le traitement en bloc planifié d’une manière contrôlée et prévisible.

## Comment vos parcours sont affectés {#impact}

Un parcours en direct qui utilise une audience par lots dans un nœud Qualification de l’audience continue de s’exécuter après août 2026. Cependant, si vous arrêtez, dupliquez ou republiez le parcours, il sera bloqué jusqu’à ce que la configuration soit mise à jour.


| Statut du parcours | Impact après août 2026 |
| --- | --- |
| parcours en direct **&#x200B;**&#x200B;| Pas impacté. Les parcours dynamiques existants continuent de s’exécuter. Pas d&#39;arrêt automatique. |
| **Nouveaux parcours** | Bloqué de la publication jusqu’au remplacement de l’audience par lots. |
| **Projets de parcours** | Bloqué de la publication jusqu’au remplacement de l’audience par lots. |
| **parcours dupliqués** | Bloqué de la publication jusqu’au remplacement de l’audience par lots. |


## Guide de migration {#migration-paths}

Si vous utilisez une audience par lots dans un nœud Qualification de l’audience , identifiez votre cas d’utilisation ci-dessous et suivez le chemin de migration recommandé.

### Cas d’utilisation 1 : audience basée sur les événements de suivi des messages AJO {#use-case-1}

**À quoi cela ressemble :** votre audience de qualification d’audience utilise des conditions basées sur les envois d’e-mails, les ouvertures ou les clics provenant de jeux de données de suivi interne de Journey Optimizer (par exemple, *« le profil a reçu un e-mail »* ou *« le profil a ouvert un e-mail »*.

>[!NOTE]
>
>Depuis novembre 2024, la segmentation en flux continu ne prend plus en charge les événements d’envoi et d’ouverture provenant de jeux de données de suivi Journey Optimizer. Les audiences basées sur ces événements sont désormais évaluées en mode batch. [En savoir plus sur les méthodes d’évaluation des audiences](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer)

**Alternatives recommandées :**

* **Réagir aux ouvertures ou aux clics dans le même parcours** — Utilisez le nœud **[Événement de réaction](reaction-events.md)**. Il est conçu pour répondre aux ouvertures et aux clics d’un message envoyé dans le même parcours, sans nécessiter d’audience distincte. [Consultez un exemple complet à l’aide d’événements de réaction](journeys-uc.md#send-multi-channel-messages)

* **Ciblage des clics sur plusieurs parcours** — Créez une [audience de diffusion en continu](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer) à partir des événements de clic et utilisez plutôt le nœud Qualification d’audience avec cette audience de diffusion en continu.

* **Suppression basée sur les rebonds** — Utilisez le Journey Optimizer natif [liste de suppression](../configuration/manage-suppression-list.md) plutôt que de modéliser le comportement des rebonds comme condition d&#39;audience.

* **Toute logique d’envoi/d’ouverture restante** — Passez à un parcours **[Lecture d’audience](read-audience.md)** lors d’une exécution planifiée pour traiter l’audience par lots en toute sécurité.


### Cas d’utilisation 2 : Parcours en attente de nouvelles données de segmentation par lots {#use-case-2}

**À quoi cela ressemble :** planifiez l’exécution d’un parcours après une tâche de segmentation quotidienne, et utilisez un nœud Qualification de l’audience pour vous assurer que le parcours ne se déclenche qu’une fois que les dernières données d’audience sont disponibles.

**Alternative recommandée :**

Utilisez un parcours **[Lecture d’audience](read-audience.md)** avec l’option **[!UICONTROL Déclencheur après l’évaluation de l’audience par lots]** activée. Cette fonctionnalité intégrée permet d’exécuter le parcours jusqu’à ce que la tâche de segmentation soit terminée, puis démarre immédiatement lorsque de nouvelles données sont disponibles, sans nécessiter de nœud Qualification de l’audience. [Découvrez comment configurer cette option](read-audience.md#schedule)


### Cas d’utilisation 3 : activation d’audiences par lots périodiques volumineuses {#use-case-3}

**À quoi cela ressemble** activez ou actualisez une audience volumineuse (potentiellement des millions de profils) de manière périodique, et le parcours de qualification d’audience se déclenche pour tous les profils nouvellement qualifiés en même temps.

**Alternative recommandée :**

Utilisez un parcours **[Lecture d’audience](read-audience.md)**. Il est conçu pour traiter des audiences volumineuses en bloc, gérer les profils par lots contrôlés et offrir une exécution de parcours plus prévisible et plus fiable à grande échelle. [Voir un exemple complet](message-to-subscribers-uc.md)

## Que faire si aucune des alternatives ne fonctionne pour votre cas d’utilisation ? {#exceptions}

Si votre cas d’utilisation ne peut pas être résolu à l’aide de l’un des chemins de migration ci-dessus, contactez votre représentant Adobe. Les cas qui ne peuvent être traités avec les solutions de rechange existantes seront examinés individuellement.

## Ressources connexes {#related}

* [Événements de qualification d’audience](audience-qualification-events.md) — guide de configuration complet et mécanismes de sécurisation
* [Activité Lecture d’audience](read-audience.md) - Comment configurer une entrée d’audience par lots planifiée
* [Événements de réaction](reaction-events.md) — Comment réagir aux ouvertures et aux clics dans le même parcours
* [Méthodes d’évaluation d’audience](../audience/creating-a-segment-definition.md#evaluation-method-in-journey-optimizer) — explication de la segmentation par lots, en flux continu et Edge
* [À propos des audiences](../audience/about-audiences.md) — types d’audiences et leur création dans Journey Optimizer
* [Gérer la liste de suppression](../configuration/manage-suppression-list.md) — Comment accéder à la suppression des rebonds et la configurer
* [Mécanismes de sécurisation et limitations du parcours](limitations.md)
* [Critères d&#39;entrée et de sortie de Parcours &#x200B;](entry-exit-criteria-guide.md) — comprendre les modèles d&#39;entrée en temps réel ou par lots à l&#39;aide d&#39;exemples concrets
* [Envoyer des messages multicanaux](journeys-uc.md#send-multi-channel-messages) : cas d&#39;utilisation complet combinant la lecture d&#39;audience, les événements de réaction, les e-mails et les notifications push
* [Envoyer un message aux abonnés](message-to-subscribers-uc.md) — cas d’utilisation de bout en bout pour l’activation d’audiences en masse avec Lecture d’audience
