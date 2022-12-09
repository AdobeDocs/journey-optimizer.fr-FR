---
solution: Journey Optimizer
product: journey optimizer
title: À propos des événements
description: En savoir plus sur les événements
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: 63c52f04da9fd1a5fafc36ffb5079380229f885e
workflow-type: tm+mt
source-wordcount: '904'
ht-degree: 0%

---

# À propos des événements{#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="À propos des événements"
>abstract="Un événement est lié à une personne. Il se rapporte au comportement d’une personne (par exemple, une personne a acheté un produit, a visité un magasin, est sortie d’un site web, etc.) ou un événement lié à une personne (par exemple, une personne a atteint 10 000 points de fidélité). C’est ce que Journey Optimizer écoute dans les parcours pour orchestrer les meilleures actions suivantes."

La configuration de l’événement vous permet de définir les informations. [!DNL Journey Optimizer] recevra en tant qu’événements. Vous pouvez utiliser plusieurs événements (à différentes étapes d’un parcours) et plusieurs parcours peuvent utiliser le même événement.

>[!CAUTION]
>
>La configuration de l’événement est **mandatory** et doit être effectué par une **ingénieur en données**.

Vous pouvez configurer deux types d’événements :

* **Unitaire** events : ces événements sont liés à une personne. Elles se rapportent au comportement d’une personne (par exemple, une personne a acheté un produit, a visité un magasin, a quitté un site web, etc.) ou un événement lié à une personne (par exemple, une personne a atteint 10 000 points de fidélité). C&#39;est ce qui [!DNL Journey Optimizer] écoute dans les parcours pour orchestrer les meilleures actions suivantes. Les événements unitaires peuvent être générés par des règles ou par le système. Pour savoir comment créer un événement unitaire, reportez-vous à cette section [page](../event/about-creating.md).

* **Entreprises** events : un événement commercial est un événement qui, contrairement à un événement unitaire, n’est pas lié à un profil spécifique. Par exemple, il peut s’agir d’une alerte d’actualité, d’une mise à jour sportive, d’un changement ou d’une annulation d’un vol, d’une mise à jour de l’inventaire, d’événements météorologiques, etc. Bien que ces événements ne soient pas spécifiques à un profil, ils peuvent intéresser un certain nombre de profils : des personnes inscrites à des sujets d&#39;actualité particuliers, des passagers en vol, des acheteurs intéressés par un produit en rupture de stock, etc. Les événements professionnels sont toujours basés sur des règles. Lorsque vous déposez un événement d’entreprise dans un parcours, il ajoute automatiquement une **Lecture de segment** activité juste après. Pour savoir comment créer un événement professionnel, reportez-vous à cette section [page](../event/about-creating-business.md).


>[!NOTE]
>
>Si vous modifiez un événement utilisé dans un parcours actif ou dans un état de brouillon, vous pouvez uniquement modifier le nom, la description ou ajouter des champs de payload. Nous limitons strictement l’édition des parcours actifs ou dans un état de brouillon afin d’éviter toute interruption de parcours.

Les parcours unitaires (commençant par un événement ou une qualification de segment) incluent une barrière de sécurité qui empêche les parcours d’être déclenchés par erreur plusieurs fois pour le même événement. La rentrée du profil est temporairement bloquée par défaut pendant 5 minutes. Par exemple, si un événement déclenche un parcours à 12h01 pour un profil spécifique et qu’un autre arrive à 12h03 (s’il s’agit du même événement ou d’un autre déclenchant le même parcours), ce parcours ne redémarre pas pour ce profil.

➡️ [Découvrez cette fonctionnalité en vidéo](#video)

## Type d’identifiant d’événement{#event-id-type}

Pour les événements professionnels, le type d’ID d’événement est toujours basé sur des règles.

Pour les événements unitaires, il existe deux types d’ID d’événement :

* **Basé sur des règles** events : ce type d’événement ne génère pas d’eventID. À l’aide de l’éditeur d’expression simple, vous définissez simplement une règle qui sera utilisée par le système pour identifier les événements pertinents qui déclencheront vos parcours. Cette règle peut être basée sur n’importe quel champ disponible dans la payload de l’événement, par exemple l’emplacement du profil ou le nombre d’éléments ajoutés au panier du profil.

   >[!CAUTION]
   >
   >Une règle de limitation est définie pour les événements basés sur des règles. Elle limite à 5 000 le nombre d’événements qualifiés qu’un parcours peut traiter par seconde pour une organisation donnée. Il correspond aux contrats de niveau de service Journey Optimizer. Reportez-vous à votre licence Journey Optimizer et [Description du produit Journey Optimizer](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html).

* **Généré par le système** events : ces événements nécessitent un eventID. Ce champ eventID est généré automatiquement lors de la création de l’événement. Le système qui appuie sur l’événement ne doit pas générer d’identifiant, mais transmettre celui disponible dans l’aperçu de la payload.

Journey Optimizer nécessite que les événements soient diffusés en continu ou par lots dans Adobe Experience Platform. Ces données n’ont pas nécessairement besoin d’accéder au profil en temps réel. Si vous souhaitez utiliser les événements pour la segmentation ou la recherche dans un parcours distinct, nous vous recommandons d’activer le jeu de données pour profile.

## Cycle des données {#data-cycle}

Les événements sont des appels d’API POST. Les événements sont envoyés à Adobe Experience Platform par le biais des API d’ingestion en flux continu. La destination URL des événements envoyés par le biais des API de messagerie transactionnelle est appelée &quot;inlet&quot;. La payload des événements suit la mise en forme XDM.

La payload contient les informations requises par les API d’ingestion en flux continu pour fonctionner (dans l’en-tête) et les informations requises par [!DNL Journey Optimizer] pour travailler et les informations à utiliser dans les parcours (dans le corps, par exemple, le montant d’un panier abandonné). Il existe deux modes d’ingestion par flux : authentifié et non authentifié. Pour plus d’informations sur les API d’ingestion en flux continu, reportez-vous à la section [ce lien](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html).

Après avoir transité par les API d’ingestion en flux continu, les événements se propagent dans un service interne appelé Pipeline, puis dans Adobe Experience Platform. Si l’indicateur du service de profil client en temps réel est activé pour le schéma d’événement et qu’un identifiant de jeu de données est également associé à l’indicateur de profil client en temps réel, il est transmis au service de profil client en temps réel.

Pour les événements générés par le système, le pipeline filtre les événements dont la charge utile contient [!DNL Journey Optimizer] eventID (voir le processus de création d’événement ci-dessous) fournis par [!DNL Journey Optimizer] et contenus dans la payload d’événement. Pour les événements basés sur des règles, le système identifie l’événement à l’aide de la condition eventID. Ces événements sont écoutés par [!DNL Journey Optimizer] et le parcours correspondant est déclenché.

## Vidéos pratiques {#video}

Découvrez comment configurer un événement, spécifier le point de terminaison de diffusion en continu et la charge utile d’un événement.

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Comprendre les cas d’utilisation applicables pour les événements professionnels. Découvrez comment créer un parcours à l’aide d’un événement professionnel et les bonnes pratiques à appliquer.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
