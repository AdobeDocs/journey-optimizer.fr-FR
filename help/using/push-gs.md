---
title: Prise en main de la configuration push
description: Présentation du flux de données et des composants des notifications push
hide: true
hidefromtoc: true
source-git-commit: a2eee802f82552e56ced00f93e5e4c8a7b3feb7a
workflow-type: tm+mt
source-wordcount: '1127'
ht-degree: 0%

---

# Prise en main de la configuration push {#get-started-push}

![](assets/do-not-localize/badge.png)

Les notifications push constituent un canal de communication rapide qui vous permet de transmettre des messages, des offres ou d’autres informations aux utilisateurs de vos applications mobiles. En règle générale, l’utilisateur final doit opt-in pour recevoir les notifications push ; l’opt-in a généralement lieu pendant le processus d’installation et les utilisateurs finaux disposent d’un moyen de gérer les notifications s’ils changent d’avis ultérieurement. Un avantage important des notifications push dans l’informatique mobile est que la technologie ne nécessite pas l’ouverture d’applications spécifiques sur un appareil mobile pour qu’un message soit reçu. Cela permet à un smartphone de recevoir et d’afficher des notifications même lorsque l’écran de l’appareil est verrouillé et que l’application mobile est en arrière-plan ou fermée.

**[!DNL Adobe Journey Optimizer]**  vous permet d’envoyer des messages push personnalisés, pertinents et sensibles au temps sur une grande échelle. Un segment de profils client peut être ciblé pour recevoir des notifications push enrichies sur leurs appareils mobiles iOS et Android. Ces segments peuvent être créés sur la base d’événements d’expérience utilisateur passés ou actifs, de données d’enregistrement utilisateur ou d’une combinaison d’interactions utilisateur et de données. Une fois qu’un parcours est en ligne, vous pouvez afficher des rapports détaillés sur le nombre de messages envoyés, les échecs pour quelle raison et des informations de suivi push, telles que le nombre d’utilisateurs qui ont cliqué dessus.

Ce document vous guide tout au long d’un flux de données de bout en bout de notifications push de base à l’aide de [!DNL Journey Optimizer] et d’un diagramme de flux utilisateur pour expliquer comment chaque rôle remplit ses responsabilités et collabore pour rassembler le flux de données push.


## Composants et services impliqués

* **Les** fournisseurs de messagerie Cloud sont des services tiers qui nous permettent de diffuser des notifications de serveurs distants vers des applications mobiles.

   [!DNL Adobe Journey Optimizer]  prend en charge les plateformes Android et iOS et traite deux Principaux services de messagerie cloud :
   * Firebase Cloud Messaging (FCM) - pour envoyer des notifications à l’application mobile Android
   * Apple Push Notification Service (APN) - pour envoyer des notifications à l’application mobile iOS

* **Application mobile intégrée avec le** SDK Mobile Adobe qui permet d’intégrer vos applications mobiles avec les solutions Adobe Experience Cloud. Le SDK Mobile comprend diverses extensions de solution Experience Cloud afin de fournir des fonctionnalités spécifiques au service qu’elles représentent. Ces extensions exposent diverses API pour activer le flux de données, comme l’enregistrement du jeton push ou l’envoi d’événements de suivi push ou de tout autre événement d’expérience personnalisé à Adobe Experience Platform.

* **Adobe Launch**  (ou collecte de données) est la nouvelle génération de fonctionnalités de gestion du SDK mobile qui permet le flux de données du SDK Mobile vers  [!DNL Adobe Experience Platform]. Il permet d’enregistrer des extensions, de créer des règles et des éléments de données pour envoyer des données de votre application mobile vers les solutions Adobe Experience Cloud. En ce qui concerne le flux de données des notifications push, les Principales configurations requises dans Adobe Launch sont les suivantes :

   * Création d’un flux de données pour configurer les jeux de données de profil et d’événement d’expérience sur lesquels les données sont transmises à Experience Platform.
   * Création d’une propriété mobile côté client et ajout d’extensions. Le SDK Mobile s’intègre étroitement à ces extensions pour offrir une expérience de collecte de données transparente.
   * Enregistrement de l’identifiant de lot d’applications mobiles et des informations d’identification de l’application qui aideraient à identifier et valider de manière unique l’intégrité de l’application au moment de la diffusion de la notification push.

* **Real-time Customer** Profile est le composant de Adobe Experience Platform qui vous permet d’obtenir une vue d’ensemble de chaque client en combinant des données provenant de plusieurs canaux, notamment le web, les appareils mobiles, le CRM et des tiers. Profile vous permet de consolider vos données client en une vue unifiée offrant un compte horodaté et exploitable de chaque interaction client. Les données statiques qui identifient l’utilisateur de l’application mobile, telles qu’un jeton push, sont stockées par rapport au profil de l’utilisateur en tant que données d’enregistrement, tandis que les interactions de l’utilisateur avec les notifications push sont suivies comme des données d’événements de série temporelle.

* **[!DNL Adobe Journey Optimizer]** : une fois vos intégrations d’applications mobiles avec les composants mentionnés ci-dessus en place et vos profils client disponibles en tant que profils client en temps réel, vous pouvez tirer parti des puissantes fonctionnalités de segmentation d’audience de  [!DNL Adobe Journey Optimizer]  afin d’assurer une expérience optimale pour chaque personne.


## Flux de données push

Ce diagramme présente un flux de données de messagerie push de base et donne un aperçu des différents produits et composants d’Adobe impliqués dans le flux.

![](assets/push-flow.png)


1. Le client développe une application mobile sur Android ou iOS qu’il mettra à disposition de ses utilisateurs. Pour utiliser la fonctionnalité push fournie par les fournisseurs de notifications push, c’est-à-dire APNS par Apple et FCM par Google, l’application mobile s’enregistre elle-même et active la fonctionnalité push.
1. Les fournisseurs de notifications push génèrent et envoient un jeton push à l’application mobile. Un jeton push est un identifiant que les expéditeurs utilisent pour cibler des appareils spécifiques avec une notification push.
1. L’application mobile est intégrée au SDK Mobile Adobe qui expose diverses extensions et API. L’extension de messagerie expose une API pour enregistrer le jeton push dans Adobe Experience Platform par rapport au profil du client.
1. Une fois l’application mobile prête, elle est configurée dans **[!DNL Journey Launch]** `>` **Configurations de l’application** avec les informations d’identification.
Le marketeur crée désormais une notification push dans **[!DNL Adone Journey Optimizer]** `>` **Messages** par rapport à l’application mobile enregistrée.
1. Le marketeur orchestre un parcours client définissant le flux des événements et actions. Pour envoyer une notification push à un stade du parcours, le marketeur ajoute une action de type &#39;Message&#39; et l&#39;associe au message créé à l&#39;étape précédente.
1. Chaque fois qu’un profil client est admissible pour recevoir la notification push pour une raison quelconque, par exemple lors du déclenchement d’un événement ou lors de la qualification d’un segment, le message est personnalisé par rapport au profil, le cas échéant.
1. Le message push personnalisé est envoyé pour traitement supplémentaire au service de diffusion push.
1. Le service de diffusion Push valide les informations d’identification de l’application associée au message.
1. Le message est envoyé aux fournisseurs de notifications push pour diffusion à l’application mobile par rapport au jeton push et aux informations d’identification spécifiques.
1. Les fournisseurs de notifications push envoient un commentaire suggérant si le message a bien été délivré au fournisseur ou non. Dans le cas contraire, le message d’erreur correspondant fait partie du commentaire. Ce commentaire est envoyé pour Adobe des rapports que le client peut afficher dans son Parcours [Live](reports/live-report.md) et [Rapports globaux](reports/global-report.md).
1. En attendant, les fournisseurs de notifications push diffusent de manière asynchrone la notification push réussie à l’application mobile.
1. Comme le client interagit avec la notification, les impressions telles que clic/ouverture peuvent ensuite être suivies en tant que **Événements d’expérience**. L’extension de messagerie expose les API pour envoyer des événements de suivi dans Adobe Experience Platform par rapport au profil du client.

## Flux d’utilisateur push

Ce diagramme présente les différentes étapes impliquées dans la configuration des composants qui forment l’ossature du flux de données push. Les éléments d’action ont été classés en fonction du rôle exécutant la configuration et du composant en cours de configuration. Comme vous pouvez le constater, avant de commencer à envoyer des notifications push avec **[!DNL Adobe Journey Optimizer]** , vous devez vous assurer que les configurations et les intégrations sont en place sur l’application mobile, **[!DNL Adobe Launch]** et **[!DNL Adobe Experience Platform]**.

![](assets/user-flow.png)

Les étapes détaillées pour configurer le canal push et activer les notifications push dans [!DNL Journey Optimizer] sont disponibles dans [cette page](push-configuration.md).