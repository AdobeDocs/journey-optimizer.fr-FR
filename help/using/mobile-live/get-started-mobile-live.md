---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec les activités en direct
description: Découvrez comment créer des activités en direct dans Journey Optimizer.
topic: Content Management
role: User
level: Beginner
exl-id: c9766603-df19-4efd-8319-27e9764254b4
source-git-commit: 1a5a69b9c2907e18a4649543ac0ddf6fdd486491
workflow-type: tm+mt
source-wordcount: '388'
ht-degree: 20%

---

# Commencer avec les activités en direct {#get-started-mobile-live}


Les activités en direct sont des éléments d’interface utilisateur persistants et modifiables affichés sur l’écran de verrouillage de l’appareil. Ils permettent à votre application de présenter des informations à jour en temps réel, en informant les utilisateurs tout au long d&#39;un événement en cours, sans qu&#39;ils aient à ouvrir l&#39;application ou à recevoir des notifications push répétées.

>[!AVAILABILITY]
>
>Les activités en direct dans Adobe Journey Optimizer ne sont compatibles qu’avec Apple iOS.

Contrairement aux notifications push traditionnelles, les activités en direct représentent l’engagement basé sur l’état **state-based engagement** : au lieu de diffuser des alertes ponctuelles, elles conservent une présence contextuelle continue, qui se met à jour dynamiquement au fur et à mesure de l’évolution des événements.


<table style="table-layout:fixed"><tr style="border: 0;">
<td>
<img alt="Activités iOS Live sur l’écran de verrouillage et Dynamic Island" src="assets/do-not-localize/live-activity.jpeg">
</td>
<td>
<p>Avec Adobe Journey Optimizer, vous pouvez <strong>démarrer</strong>, <strong>mettre à jour</strong> et <strong>terminer</strong> des activités en direct à distance par programmation via des campagnes déclenchées par API, en prenant en charge des cas d’utilisation individuels et basés sur une audience à grande échelle.</p>
<p>Les activités en direct peuvent <strong>uniquement</strong> être lancées par le biais de campagnes <strong>déclenchées par une API</strong>, ce qui vous permet de fournir des payloads personnalisés et d’effectuer toute la personnalisation par le biais de votre propre payload. Le type de campagne approprié doit être sélectionné en fonction du cas d’utilisation prévu de l’activité Live :</p>
<ul>
<li><strong>Marketing déclenché par API</strong> : cas d’utilisation de diffusion, mises à jour basées sur l’audience envoyées à grande échelle : scores sportifs et comptes à rebours des événements en direct, mises à jour du statut des vols, expériences partagées sur un segment d’utilisateurs.</li>
<li><strong>Transactionnel déclenché par API</strong> : cas d’utilisation individuels, mises à jour en temps réel 1:1 par utilisateur : suivi des commandes et progression de la diffusion, mises à jour de l’état du trajet ou du service, réservations en temps réel et confirmations de rendez-vous.</li>
</ul>
</td>
</tr>
</table>

## Avantages clés

Les activités en direct font passer l’engagement mobile de basé sur les notifications à basé sur les états, ce qui permet aux marques de :

* Maintenir une **présence continue** sur l’écran de verrouillage tout au long des événements à forte valeur ajoutée
* **Mettre à jour les informations de manière dynamique** sans surcharger les utilisateurs avec des notifications répétées
* Proposer des moments mobiles **plus riches, plus contextuels** liés à des événements réels
* **Augmenter l’engagement et la rétention** lors des transactions actives ou des expériences en direct

## Guide de démarrage rapide

Suivez les étapes ci-dessous pour configurer et implémenter des activités en direct dans votre application :

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

>[!VIDEO](https://video.tv.adobe.com/v/3479866/?captions=fre_fr&learn=on)
