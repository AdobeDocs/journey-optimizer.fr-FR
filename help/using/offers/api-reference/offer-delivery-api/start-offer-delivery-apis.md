---
title: Prise en main des API de diffusion d’offres
description: En savoir plus sur les API disponibles pour diffuser des offres personnalisées.
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
exl-id: 7bc1a4ec-113c-4af7-b549-ee17b843b818
source-git-commit: bf738ebac09d5c852872a8ea85f6532ad9d4222d
workflow-type: tm+mt
source-wordcount: '442'
ht-degree: 88%

---

# Prise en main des API de diffusion d’offres {#about-decisioning-apis}

Vous pouvez diffuser des offres à l’aide de l’une des API suivantes : API **Decisioning** ou **Edge Decisioning.** En outre, la variable **Prise de décision par lots** L’API vous permet de diffuser des offres à tous les profils d’un segment donné en un seul appel. Le contenu de l&#39;offre pour chaque profil du segment est placé dans un jeu de données Adobe Experience Platform où il est disponible pour les workflows par lots personnalisés.

Cette page contient des informations sur les fonctionnalités spécifiques disponibles avec la fonction **Prise de décision** et **Prise de décision Edge** API. Même si toutes deux vous permettent de diffuser des offres à vos clients, il est recommandé d’utiliser l’API **Edge Decisioning** chaque fois que possible pour les cas d’utilisation entrants. Cette dernière assure une latence plus faible et un débit plus élevé sur votre plateforme.

|  | Demandes/seconde | Latence |
|---|---|---|
| API Decisioning | 2 000 | &lt; 500 ms |
| API Edge Decisioning | 5 000 | &lt; 250 ms |

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

## Fonctionnalités de l’API Decisioning {#decisioning}

Les fonctionnalités répertoriées ci-dessous ne sont disponibles qu’avec l’API Decisioning. Si vous avez besoin de l’une d’entre elles pour répondre à vos besoins, utilisez l’API Decisioning. Dans le cas contraire, il est recommandé d’utiliser les API Edge Decisioning.

* **Événements d’expérience** : permet de tirer parti des événements d’expérience pour créer vos règles de prise de décision.
* **Contenu et caractéristiques de l’offre** : vous pouvez choisir de ne pas renvoyer le contenu et les caractéristiques d’une offre à l’aide d’une option dédiée.
* **Métadonnées de l’offre** : permet d’activer une option pour renvoyer les métadonnées d’une offre.
* **Stratégie de fusion** : permet d’utiliser dans votre demande une stratégie de fusion différente de celle associée à votre sandbox.
* **Événements de prise de décision et capping de la fréquence** : permet de bloquer les événements de prise de décision pour qu’ils ne soient pas comptabilisés par toute limitation de fréquence qui se produit.
* **Propositions en double** : permet d’activer une option pour ne pas dédupliquer les propositions.
