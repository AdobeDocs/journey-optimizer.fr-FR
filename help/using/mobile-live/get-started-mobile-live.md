---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec les activités en direct
description: Découvrez comment créer des activités en direct dans Journey Optimizer.
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: c9766603-df19-4efd-8319-27e9764254b4
source-git-commit: 6b4e3a6c32d24861f1ea8df54fc2e4fbb19d0ce7
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 100%

---

# Commencer avec les activités en direct {#get-started-mobile-live}

>[!AVAILABILITY]
>
>L’activité en direct dans Journey Optimizer est uniquement compatible avec iOS.

Les activités en direct fournissent des mises à jour en temps réel et des expériences interactives dans les applications mobiles, ce qui permet aux utilisateurs et aux utilisatrices de rester informés des événements ou tâches en cours directement sur l’écran de leur appareil.

Cette fonctionnalité améliore l’engagement en fournissant des informations en direct, telles que le suivi de la progression, les mises à jour d’événement ou le contenu interactif, sans que les utilisateurs et utilisatrices ouvrent l’application.

Les activités en direct peuvent **uniquement** être lancées par le biais de campagnes **déclenchées par API**, ce qui vous permet de fournir des payloads personnalisées et d’effectuer toute la personnalisation par le biais de votre propre payload.
Le type de campagne **déclenchée par API** approprié doit être sélectionné en fonction du cas d’utilisation prévu de l’activité en direct :

* Sélectionnez **Marketing déclenché par API** pour les campagnes basées sur les audiences.

  Conçu pour les audiences ou la communication basée sur les segments où la même mise à jour est envoyée à plusieurs utilisateurs et utilisatrices, par exemple les scores de sport, les mises à jour d’événements, les expériences partagées.

* Sélectionnez **Transactionnelle déclenché par API** pour des campagnes individuelles

  Utilisateurs et utilisatrices individuels ciblés identifiés par leur profil, par exemple le statut de la commande, le suivi de la diffusion.

## Guide de démarrage rapide

Suivez les étapes ci-dessous pour configurer et implémenter des activités en direct dans votre application :

1. **[Configurer Adobe Journey Optimizer](mobile-live-configuration.md)**

   Configurez votre environnement en créant une configuration mobile.

1. **[Intégrer le SDK mobile d’Adobe Experience Platform](mobile-live-configuration-sdk.md)**

   Intégrez le SDK mobile Adobe Experience Platform pour activer les mises à jour dynamiques en temps réel sur l’écran de verrouillage et Dynamic Island.

1. **[Créer des activités en direct dans Journey Optimizer](create-mobile-live.md)**

   Utilisez des campagnes déclenchées par API dans Journey Optimizer pour démarrer vos activités en direct.

1. **[Surveiller vos campagnes](../reports/campaign-global-report-cja-activity.md)**

   Commencez à mesurer l’impact de vos activités en direct à l’aide de rapports intégrés.
