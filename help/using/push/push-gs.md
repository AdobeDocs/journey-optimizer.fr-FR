---
solution: Journey Optimizer
product: journey optimizer
title: Notifications push et Adobe Journey Optimizer
description: Présentation du flux de données et des composants des notifications push
topic: Mobile
feature: Push
role: Admin
level: Intermediate
exl-id: 9718c4b6-2558-4dfd-9d8f-f8845def19ba
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '658'
ht-degree: 0%

---

# Notifications push et Adobe Journey Optimizer {#get-started-push}

Cette page vous aidera à configurer et à comprendre les services clés et les workflows impliqués dans les notifications push dans [!DNL Journey Optimizer]. Découvrez comment créer des notifications push sur [cette page](create-push.md).

Étapes de configuration du canal push dans [!DNL Adobe Journey Optimizer] sont détaillées sur [cette page](push-configuration.md).

Le graphique suivant montre les systèmes et services impliqués dans les flux de données associés et montre comment les notifications push sont diffusées du point de vue du service de bout en bout.

![](assets/push-flow.png)

1. Enregistrement de votre application mobile de marque (Android ou iOS) avec les APNS d’Apple et les services de messagerie push Google FCM
1. Les services de messagerie génèrent un jeton push, qui est un identifiant qui [!DNL Adobe Journey Optimizer] utilisera pour cibler l’appareil spécifique avec une notification push.
1. Le jeton push généré précédemment est transmis à Adobe Experience Platform et synchronisé avec Real-time Customer Profile. cela est fait en standard avec un SDK client facile à intégrer
1. Les messages push sont créés dans [!DNL Adobe Journey Optimizer], les messages push sont créés sur une surface de canal (c’est-à-dire un paramètre prédéfini de message).
1. Les messages push peuvent être inclus dans la zone de travail d’orchestration dans les parcours.
1. Lors de la publication du parcours, les profils client basés sur les conditions du parcours sont qualifiés pour recevoir des notifications push, les payloads des messages push sont personnalisés à cette étape.
1. Les payloads push personnalisées sont transférées vers un service de diffusion de messagerie push interne.
1. Ce service interne valide ensuite les informations d’identification de l’application associée au message, et
1. Envoie le message à Apple et aux services de messagerie Google pour une diffusion finale
1. Les commentaires des services de messagerie sont signalés, les erreurs et les succès sont consignés pour la création de rapports dans les rapports Journey Live et Global.
1. Les notifications push sont diffusées sur les appareils de l’utilisateur final.
1. Les interactions de notification push de l’utilisateur final sont envoyées en tant qu’événements d’expérience du client de l’utilisateur final via l’intégration du SDK.

## Rôles des services clés dans les notifications push {#roles-of-key-services}

* **Prestataires de notification push** sont les services web des composants principaux qui diffusent des notifications de serveurs distants vers des applications mobiles.

   [!DNL Adobe Journey Optimizer]  prend en charge les plateformes Android et iOS et s’intègre ainsi aux fonctionnalités suivantes :
   * [Firebase Cloud Messaging (FCM)](https://firebase.google.com/docs/cloud-messaging) - pour envoyer des notifications à l’application mobile Android
   * [Service de notification push Apple (APNS)](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html) - pour envoyer des notifications à l’application mobile iOS

* **SDK Mobile Adobe Experience Platform** qui fournit des API d’intégration côté client pour vos mobiles via des SDK compatibles Android et iOS. Le SDK fournit une [!DNL Adobe Journey Optimizer] Exposant une variété d’API spécifiques à la messagerie push et permettant un flux de données comme l’enregistrement du jeton push ou l’envoi d’événements de suivi push ou de tout autre événement d’expérience personnalisé à Adobe Experience Platform. Le SDK fournit également diverses autres extensions qui activent d’autres fonctionnalités Adobe Experience Cloud ainsi que des fonctionnalités de partenaires tiers.

   L’intégration du SDK nécessite également la configuration d’Adobe Experience Platform. [Collecte de données](https://experienceleague.adobe.com/docs/experience-platform/tags/home.html){target=&quot;_blank&quot;} services tels que :

   * Création d’un flux de données pour configurer les jeux de données de profil et d’événement d’expérience sur lesquels les données s’enchaînent dans Adobe Experience Platform
   * Création de propriétés mobiles côté client et ajout d’extensions. Le SDK s’intègre étroitement à ces extensions pour offrir une expérience de collecte de données transparente.
   * Enregistrement de l’identifiant de lot d’applications mobiles et des informations d’identification de l’application

* **Profil client en temps réel d’Adobe Experience Platform**  offre une vue d’ensemble de chaque client en combinant des données issues de plusieurs canaux, notamment le web, les appareils mobiles, le CRM et des tiers. Profile vous permet de consolider vos données client en une vue unifiée offrant un compte horodaté et exploitable de chaque interaction client. Le jeton push d’un utilisateur de l’application donné est stocké par rapport au profil de l’utilisateur en tant que données d’enregistrement, tandis que les interactions de l’utilisateur avec les notifications push sont suivies en tant que données d’événements de série temporelle. [En savoir plus sur le profil client en temps réel d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html){target=&quot;_blank&quot;}.

* **[!DNL Adobe Journey Optimizer]** : une fois vos intégrations d’applications mobiles avec les composants mentionnés ci-dessus en place et vos profils client dans Adobe Experience Platform, vous pouvez créer et orchestrer des notifications push dans [!DNL Adobe Journey Optimizer] pour interagir avec vos utilisateurs.

## Configuration technique push et workflows pratiques {#push-technical-setup}

Le graphique suivant présente les différentes étapes, de bout en bout, de la configuration des composants qui forment l’ossature du flux de données push. Les éléments d’action ont été classés en fonction du rôle exécutant la configuration et du composant en cours de configuration.

![](assets/user-flow.png)
