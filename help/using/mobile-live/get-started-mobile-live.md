---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec les activités en direct
description: Découvrez comment envoyer une activité en direct dans Journey Optimizer
topic: Content Management
role: User
level: Beginner
exl-id: c9766603-df19-4efd-8319-27e9764254b4
source-git-commit: 4f599e46c35bc328057247b84193a4db670fee83
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 21%

---

# Commencer avec les activités en direct {#get-started-mobile-live}


Les activités en direct sont des éléments d’interface utilisateur persistants et modifiables affichés sur l’écran de verrouillage de l’appareil. Ils permettent à votre application de présenter des informations à jour en temps réel, en informant les utilisateurs tout au long d&#39;un événement en cours, sans qu&#39;ils aient à ouvrir l&#39;application ou à recevoir des notifications push répétées.

>[!AVAILABILITY]
>
>L’activité en direct dans Adobe Journey Optimizer n’est compatible qu’avec Apple iOS.

Contrairement aux notifications push traditionnelles, les activités en direct représentent l’engagement basé sur l’état **state-based engagement** : au lieu de diffuser des alertes ponctuelles, elles conservent une présence contextuelle continue, qui se met à jour dynamiquement au fur et à mesure de l’évolution des événements.


![](assets/do-not-localize/live-activity.jpeg){width="50%" align="left"}

Avec Adobe Journey Optimizer, vous pouvez **démarrer**, **mettre à jour** et **terminer** des activités en direct à distance et par programmation, par le biais de campagnes déclenchées par API. Cela permet de prendre en charge des cas d’utilisation individuels et basés sur une audience à grande échelle.

L’activité en direct peut **uniquement** être lancée par le biais de campagnes **déclenchées par une API**, ce qui vous permet de fournir des payloads personnalisés et d’effectuer toute la personnalisation par le biais de votre propre payload.
Le type de campagne **déclenché par API** approprié doit être sélectionné en fonction du cas d’utilisation prévu de l’activité Live :

* Sélectionnez **Marketing déclenché par API** pour les cas d’utilisation de diffusion : mises à jour basées sur l’audience envoyées à grande échelle :

   * Scores sportifs et comptes à rebours des événements en direct
   * Mises à jour de l’état des vols pour tous les passagers sur une route
   * Expériences partagées sur un segment d’utilisateurs

* Sélectionnez **Transactionnel déclenché par API** pour les cas d’utilisation individuels — 1 :1 mises à jour en temps réel par utilisateur :

   * Suivi des commandes et progression de la diffusion
   * Mises à jour de l’état du pilote ou du service
   * Confirmation de réservation et de rendez-vous en temps réel

## Avantages clés

Les activités en direct font passer l’engagement mobile de basé sur les notifications à basé sur les états, ce qui permet aux marques de :

* Maintenir une **présence continue** sur l’écran de verrouillage tout au long des événements à forte valeur ajoutée
* **Mettre à jour les informations de manière dynamique** sans surcharger les utilisateurs avec des notifications répétées
* Proposer des moments mobiles **plus riches, plus contextuels** liés à des événements réels
* **Augmenter l’engagement et la rétention** lors des transactions actives ou des expériences en direct

## Guide de démarrage rapide

Suivez les étapes ci-dessous pour configurer et implémenter l’activité dynamique dans votre application :

1. **[Configurer Adobe Journey Optimizer](mobile-live-configuration.md)**

   Configurez votre environnement en créant une configuration mobile.

1. **[Intégrer le SDK mobile d’Adobe Experience Platform](mobile-live-configuration-sdk.md)**

   Intégrez le SDK mobile Adobe Experience Platform pour activer les mises à jour dynamiques en temps réel sur l’écran de verrouillage et Dynamic Island.

1. **[Créer une activité Live dans Journey Optimizer](create-mobile-live.md)**

   Utilisez des campagnes déclenchées par API dans Journey Optimizer pour démarrer votre activité Live .

1. **[Surveiller vos campagnes](../reports/campaign-global-report-cja-activity.md)**

   Commencez à mesurer l’impact de votre Activité dynamique à l’aide de rapports intégrés.

## Vidéo pratique

Découvrez comment configurer les activités iOS Live avec Adobe Journey Optimizer pour diffuser des mises à jour enrichies en temps réel sur l’écran de verrouillage d’iPhone et l’île dynamique.

>[!VIDEO](https://video.tv.adobe.com/v/3479864/?learn=on)
