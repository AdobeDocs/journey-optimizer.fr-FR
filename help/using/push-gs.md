---
title: Prise en main de la configuration de notifications push
description: Présentation du flux de données et des composants des notifications push
feature: Paramétrage de l’application
topic: Push
role: Administrator
level: Intermediate
source-git-commit: e51be6bf18f2e3dfec11e80d34bf63a8ce8b1012
workflow-type: tm+mt
source-wordcount: '793'
ht-degree: 89%

---

# Prise en main de la configuration de notifications push {#get-started-push}

Les notifications push vous permettent d&#39;atteindre les utilisateurs de votre application mobile à tout moment, en particulier lorsqu&#39;ils ne l&#39;utilisent pas activement. Elles peuvent vous aider à réaliser divers cas d&#39;utilisation, tels que fournir des mises à jour sur votre service, demander à un utilisateur de prendre des mesures, avertir l&#39;utilisateur d&#39;une nouvelle transaction, etc. Les plateformes d&#39;appareil nécessitent un accord préalable avant que les utilisateurs finaux puissent recevoir ou afficher vos notifications. L&#39;accord préalable de l&#39;utilisateur peut être reçu dès le premier lancement de l&#39;application après l&#39;installation ou au cours d&#39;une session ou d&#39;un workflow ultérieur, selon le cas. [!DNL Journey Optimizer] prend en charge les notifications push et vous permet d&#39;envoyer des notifications extrêmement pertinentes à des taux de débit de pointe. Les notifications push peuvent inclure une personnalisation et un contexte basé sur les parcours afin d&#39;exploiter les données de votre marque avec Adobe Experience Cloud.

Cette page vous aidera à configurer et à comprendre les services et les workflows clés impliqués dans les notifications push dans [!DNL Journey Optimizer].

Les étapes de configuration du canal push dans [!DNL Adobe Journey Optimizer] sont présentées dans [cette page](push-configuration.md).

## Notifications push et [!DNL Adobe Journey Optimizer]

Le graphique suivant montre les systèmes et services impliqués dans les flux de données associés et décrit comment les notifications push sont diffusées sous la forme d&#39;un service de bout en bout.

![](assets/push-flow.png)

1. Enregistrement de votre application mobile de marque (Android ou iOS) auprès d&#39;APNs d&#39;Apple et des services de messagerie push Google FCM
1. Les services de messagerie génèrent un jeton push, qui est un identifiant que [!DNL Adobe Journey Optimizer] utilisera pour cibler l’appareil spécifique avec une notification push.
1. Le jeton push généré précédemment est transmis à Adobe Experience Platform et synchronisé avec le profil client en temps réel. Cette opération est effectuée en standard avec un SDK client facile à intégrer.
1. Les messages push sont créés dans [!DNL Adobe Journey Optimizer], les messages push sont créés par rapport à un paramètre prédéfini de message.
1. Les messages push peuvent être inclus dans la zone de travail d&#39;orchestration des parcours.
1. Lors de la publication des parcours, les profils client basés sur les conditions des parcours sont qualifiés pour recevoir des notifications push. Les payloads de messagerie push sont personnalisées à cette étape.
1. Les payloads push personnalisées sont transférées vers un service de diffusion de messagerie push interne.
1. Ce service interne valide ensuite les informations d&#39;identification de l&#39;application associée au message, et
1. envoie le message aux services de messagerie Apple et Google pour une diffusion finale.
1. Les retours des services de messagerie sont notés, les erreurs et les succès sont consignés pour le reporting dans les rapports dynamiques et globaux sur les parcours.
1. Les notifications push sont diffusées sur les appareils de l&#39;utilisateur final.
1. Les interactions de notification push de l&#39;utilisateur final sont envoyées en tant qu&#39;événements d&#39;expérience depuis le client de l&#39;utilisateur final via l&#39;intégration du SDK.

## Rôles des services clés dans les notifications push

* Les **fournisseurs de services de notification push** sont les services web des composants principaux qui diffusent des notifications de serveurs distants vers des applications mobiles.

   [!DNL Adobe Journey Optimizer] prend en charge les plateformes Android et iOS et s&#39;intègre ainsi aux fonctionnalités suivantes :
   * [Firebase Cloud Messaging (FCM)](https://firebase.google.com/docs/cloud-messaging) - pour envoyer des notifications à l&#39;application mobile Android
   * [Apple Push Notification Service (APNs)](https://developer.apple.com/library/archive/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/APNSOverview.html) - pour envoyer des notifications à l&#39;application mobile iOS

* **SDK mobile Adobe Experience Platform** qui fournit des API d&#39;intégration côté client pour vos mobiles via des SDK compatibles Android et iOS. Le SDK fournit une extension [!DNL Adobe Journey Optimizer] exposant diverses API spécifiques à la messagerie push et permettant le flux de données comme l’enregistrement du jeton push ou l’envoi d’événements de suivi push ou de tout autre événement d’expérience personnalisé à Adobe Experience Platform. Le SDK fournit également de nombreuses autres extensions qui activent d&#39;autres fonctionnalités Adobe Experience Cloud ainsi que des fonctionnalités de partenaires tiers.

   L&#39;intégration du SDK nécessite également la configuration des services de [collecte de données](https://experienceleague.adobe.com/docs/launch/using/home.html?lang=fr) Adobe Experience Platform, notamment :

   * Création d&#39;un flux de données pour configurer les jeux de données de profil et d&#39;événement d&#39;expérience par rapport auxquels les données sont transmises à Adobe Experience Platform
   * Création de propriétés mobiles côté client et ajout d&#39;extensions. Le SDK s&#39;intègre étroitement avec ces extensions pour offrir une expérience de collecte de données transparente.
   * Enregistrement de l&#39;identifiant d&#39;offre groupée d&#39;applications mobiles et des informations d&#39;identification de l&#39;application

* Le **Profil client en temps réel Adobe Experience Platform** offre une vue holistique de chaque client en combinant des données issues de plusieurs canaux, notamment le web, les appareils mobiles, le CRM et des tiers. Le Profil vous permet de consolider vos données client en une vue unifiée offrant un compte horodaté et exploitable de chaque interaction client. Le jeton push d&#39;un utilisateur de l&#39;application donné est stocké par rapport au profil de l&#39;utilisateur en tant que données d&#39;enregistrement, tandis que les interactions de l&#39;utilisateur avec les notifications push sont suivies en tant que données d&#39;événements de série temporelle. [En savoir plus sur le Profil client en temps réel Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html?lang=fr)

* **[!DNL Adobe Journey Optimizer]**[!DNL Adobe Journey Optimizer] : une fois que vos intégrations d&#39;applications mobiles avec les composants mentionnés ci-dessus sont en place, ainsi que vos profils client dans Adobe Experience Platform, vous pouvez créer et orchestrer des notifications push dans pour interagir avec vos utilisateurs.

## Configuration technique des notifications push et workflows pratiques

Le graphique suivant présente l&#39;ensemble des différentes étapes de la configuration des composants qui forment l&#39;ossature du flux de données push. Les éléments d&#39;action ont été classés en fonction du rôle exécutant la configuration et du composant en cours de configuration.

![](assets/user-flow.png)
