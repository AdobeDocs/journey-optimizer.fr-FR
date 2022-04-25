---
title: API de prise de décision et de prise de décision Edge
description: 'La gestion des décisions est un ensemble de services et d''interfaces utilisateur qui permet aux spécialistes marketing de créer et de proposer des expériences d''offres personnalisées aux utilisateurs finaux par le biais de canaux et d''applications en s''appuyant sur une logique métier et des règles de décision. '
feature: Offers
topic: Integrations
role: Data Engineer
level: Experienced
source-git-commit: d3a22f223353dfa5d43acab400cea3d5c314662f
workflow-type: tm+mt
source-wordcount: '413'
ht-degree: 8%

---

# API de prise de décision et de prise de décision Edge {#about-decisioning-apis}

Vous pouvez diffuser des offres à l’aide de l’une des méthodes suivantes : **Prise de décision** ou le **Prise de décision Edge** API.

Cette page contient des informations sur les fonctionnalités spécifiques disponibles avec chaque API. Bien que les deux vous permettent de diffuser des offres à vos clients, nous vous recommandons d’utiliser la variable **Prise de décision Edge** API lorsque cela est possible pour les cas d’utilisation entrants et pour garantir une meilleure latence et un meilleur débit sur votre plateforme.

|  | Demandes/s | Latence |
|---|---|---|
| API de prise de décision | 2000 | &lt;500ms |
| API de prise de décision Edge | 5 000 | &lt;250ms |

Pour plus d’informations sur l’utilisation des API, reportez-vous aux sections suivantes :
* [API de prise de décision](decisioning-api.md)
* [API de prise de décision Edge](edge-decisioning-api.md)

## Fonctionnalités de l’API Edge Decisioning {#edge}

**Requête unique pour les événements d’expérience et les requêtes de prise de décision**

Avec l’API Edge Decisioning, vous pouvez envoyer une seule requête à l’événement d’expérience lui-même avec la requête de prise de décision, plutôt que d’avoir deux requêtes différentes.

Si, par exemple, un client visite votre site web, la demande inclut l’événement d’expérience (la visite du client sur la page) et reçoit une offre pour renseigner la page visitée.

**Stockage des données contextuelles dans Adobe Experience Platform**

Les données contextuelles font référence à des données que vous ne connaissez qu’au moment où vous souhaitez qu’une offre soit renvoyée. Par exemple, la couleur de l’article acheté, la météo au moment de l’achat, etc.

Lors de la transmission de données contextuelles avec une requête d’API Edge Decisioning, les données sont stockées dans le profil Adobe Experience Platform, ce qui permet une réutilisation ultérieure.

>[!NOTE]
>
>Pour que les données contextuelles soient stockées, un schéma XDM dédié doit être configuré. ( lien+ vers le document XDM)

## Fonctionnalités de l’API de prise de décision {#decisioning}

Les fonctionnalités répertoriées ci-dessous ne sont disponibles qu’avec l’API de prise de décision. Si vous devez utiliser l’un d’eux pour répondre à vos besoins, utilisez l’API de prise de décision. Dans le cas contraire, nous vous recommandons d’utiliser les API Edge Decisioning.

* **Événements d’expérience**: tirer parti des événements d’expérience pour créer vos règles de prise de décision.
* **Contenu et caractéristiques des offres**: vous pouvez choisir de ne pas renvoyer le contenu et les caractéristiques d&#39;une offre à l&#39;aide d&#39;une option dédiée.
* **Métadonnées d’offre**: Activez une option pour renvoyer les métadonnées d’une offre.
* **Stratégie de fusion**: utilisez dans votre requête une stratégie de fusion différente de celle associée à votre environnement de test.
* **Événements de prise de décision et limitation de fréquence**: bloquer les événements de prise de décision d’être comptabilisés par le plafonnement de la fréquence qui survient.
* **Propositions en double**: activer une option pour ne pas dédupliquer les propositions ;
