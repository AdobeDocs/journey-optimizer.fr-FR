---
solution: Journey Optimizer
product: journey optimizer
title: Commencer avec les activités en direct
description: Découvrez comment envoyer une activité en direct dans Journey Optimizer
topic: Content Management
role: User
level: Beginner
hide: true
hidefromtoc: true
exl-id: c9766603-df19-4efd-8319-27e9764254b4
source-git-commit: 2fc4b1ee34b44fb6c5bcddb13f1b2b02f7094ff1
workflow-type: tm+mt
source-wordcount: '250'
ht-degree: 60%

---

# Commencer avec les activités en direct {#get-started-mobile-live}

>[!AVAILABILITY]
>
>L’activité en direct dans Journey Optimizer est uniquement compatible avec iOS.

L’activité en direct fournit des mises à jour en temps réel et des expériences interactives dans les applications mobiles, ce qui permet aux utilisateurs de rester informés des événements ou tâches en cours directement sur l’écran de leur appareil.

Cette fonctionnalité améliore l’engagement en fournissant des informations en direct, telles que le suivi de la progression, les mises à jour d’événement ou le contenu interactif, sans que les utilisateurs et utilisatrices ouvrent l’application.

L’activité en direct peut **uniquement** être lancée par le biais de campagnes **déclenchées par une API**, ce qui vous permet de fournir des payloads personnalisés et d’effectuer toute la personnalisation par le biais de votre propre payload.
Le type de campagne **déclenchée par API** approprié doit être sélectionné en fonction du cas d’utilisation prévu de l’activité en direct :

* Sélectionnez **Marketing déclenché par API** pour les campagnes basées sur les audiences.

  Conçu pour les audiences ou la communication basée sur les segments où la même mise à jour est envoyée à plusieurs utilisateurs et utilisatrices, par exemple les scores de sport, les mises à jour d’événements, les expériences partagées.

* Sélectionnez **Transactionnelle déclenché par API** pour des campagnes individuelles

  Utilisateurs et utilisatrices individuels ciblés identifiés par leur profil, par exemple le statut de la commande, le suivi de la diffusion.

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
