---
solution: Journey Optimizer, Experience Platform
product: Journey Optimizer
title: Commencer avec les API de diffusion d’offres
description: Découvrez les API disponibles pour diffuser des offres personnalisées.
badge: label="Hérité" type="Informative"
feature: Decision Management, API
topic: Integrations
role: Developer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
version: Journey Orchestration
source-git-commit: 8732a73118b807eaa7f57cfdad60355b535282ff
workflow-type: tm+mt
source-wordcount: '487'
ht-degree: 100%

---

# Commencer avec les API de diffusion d’offres {#about-decisioning-apis}

>[!TIP]
>
>La prise de décision, la nouvelle fonctionnalité de prise de décision d’[!DNL Adobe Journey Optimizer], est désormais disponible via les canaux d’expérience basée sur du code et d’e-mail. [En savoir plus](../../../experience-decisioning/gs-experience-decisioning.md)

Vous pouvez diffuser des offres à l’aide de l’une des API suivantes : API **Decisioning** ou **Edge Decisioning.** En outre, l’API **Batch Decisioning** vous permet de diffuser des offres à tous les profils d’une audience donnée en un seul appel. Le contenu de l’offre pour chaque profil de l’audience est placé dans un jeu de données Adobe Experience Platform où il est disponible pour les workflows par lots personnalisés.

Cette page contient des informations sur les fonctionnalités spécifiques disponibles avec les API **Decisioning** et **Edge Decisioning**. Même si toutes deux vous permettent de diffuser des offres à vos clients, il est recommandé d’utiliser l’API **Edge Decisioning** chaque fois que possible pour les cas d’utilisation entrants. Cette dernière assure une latence plus faible et un débit plus élevé sur votre plateforme.

Pour plus d’informations sur l’utilisation des API, reportez-vous aux sections suivantes :

* [API Decisioning](decisioning-api.md)
* [API Edge Decisioning](edge-decisioning-api.md)
* [API Batch Decisioning](batch-decisioning-api.md)

## Fonctionnalités de l’API Edge Decisioning {#edge}

**Demande unique pour les événements d’expérience et les demandes de prise de décision**

Grâce à l’API Edge Decisioning, vous pouvez envoyer l’événement d’expérience lui-même ainsi que la demande de prise de décision, et ce en une seule demande au lieu de deux.

Par exemple, si un client visite votre site web, la demande comprendra l’événement d’expérience (la visite du client sur la page) et elle recevra une offre en retour pour remplir la page visitée.

**Stockage des données contextuelles dans Adobe Experience Platform**

Les données contextuelles font référence aux données dont vous ne prenez connaissance qu’au moment où vous voulez récupérer une offre. Par exemple, la couleur de l’article acheté, la météo au moment de l’achat, etc.

Lors de la transmission de données contextuelles avec une demande de l’API Edge Decisioning, les données sont stockées dans le profil Adobe Experience Platform, pour une réutilisation ultérieure.

>[!NOTE]
>
>Pour que les données contextuelles soient stockées, vous devez avoir configuré un schéma XDM dédié.

**Mise à jour du compteur de limitation de la fréquence**

Si la limitation de la fréquence a été activée pour certaines de vos offres afin de définir la fréquence à laquelle leur nombre de limitation est réinitialisé, le compteur est mis à jour et disponible dans une décision de l’API Edge Decisioning en moins de 3 secondes. [Découvrir comment ajouter des contraintes à une offre](../../offer-library/add-constraints.md)

## Fonctionnalités de l’API Decisioning {#decisioning}

Les fonctionnalités répertoriées ci-dessous ne sont disponibles qu’avec l’API Decisioning. Si vous avez besoin de l’une d’entre elles pour répondre à vos besoins, utilisez l’API Decisioning. Dans le cas contraire, il est recommandé d’utiliser les API Edge Decisioning.

* **Contenu et caractéristiques de l’offre** : vous pouvez choisir de ne pas renvoyer le contenu et les caractéristiques d’une offre à l’aide d’une option dédiée.
* **Métadonnées de l’offre** : permet d’activer une option pour renvoyer les métadonnées d’une offre.
* **Politique de fusion** : permet d’utiliser dans votre demande une politique de fusion différente de celle associée à votre sandbox.
* **Événements de prise de décision et capping de la fréquence** : permet de bloquer les événements de prise de décision pour qu’ils ne soient pas comptabilisés par toute limitation de fréquence qui se produit.
* **Propositions en double** : permet d’activer une option pour ne pas dédupliquer les propositions.
