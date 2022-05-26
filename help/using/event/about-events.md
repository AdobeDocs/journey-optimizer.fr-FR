---
title: À propos des événements
description: En savoir plus sur les événements
feature: Events
topic: Administration
role: Admin
level: Intermediate
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: 1fa91a841d4f941f2c5bd1efd4a06ac8a9938bc7
workflow-type: ht
source-wordcount: '829'
ht-degree: 100%

---

# À propos des événements{#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="À propos des événements"
>abstract="Un événement est lié à une personne. Il décrit son comportement (par exemple, cette personne a acheté un produit, a visité un magasin, a quitté un site web, etc.) ou un événement qui s’est produit en rapport avec cette personne (par exemple, elle a accumulé 10 000 points de fidélité). C’est ce type d’élément que Journey Optimizer écoute dans les parcours pour orchestrer les meilleures actions qu’il convient de prendre ensuite."

La configuration d’événement vous permet de définir les informations que [!DNL Journey Optimizer] recevra en tant qu’événements. Vous pouvez utiliser plusieurs événements (à différentes étapes d’un parcours) et plusieurs parcours peuvent utiliser un même événement.

>[!CAUTION]
>
>La configuration de l&#39;événement est **obligatoire** et doit être effectuée par un **utilisateur technique**.

Vous pouvez configurer deux types d’événements :

* Événements **unitaires** : ces événements sont liés à une personne. Ils décrivent son comportement (par exemple, cette personne a acheté un produit, a visité un magasin, a quitté un site web, etc.) ou un événement qui s’est produit en rapport avec cette personne (par exemple, elle a accumulé 10 000 points de fidélité). C’est ce type d’élément que [!DNL Journey Optimizer] écoute dans les parcours pour orchestrer les meilleures actions qu’il convient de prendre ensuite. Les événements unitaires peuvent être générés selon des règles ou par un système. Pour savoir comment créer un événement unitaire, consultez cette [page](../event/about-creating.md).

* Événements **métier** : un événement métier est un événement qui, contrairement à un événement unitaire, n&#39;est pas lié à un profil spécifique. Par exemple, il peut s’agir d’une alerte d’actualité, d’une mise à jour sportive, d’un changement ou d’une annulation de vol, d’une mise à jour d’inventaire, d&#39;événements météorologiques, etc. Bien que ces événements ne soient pas spécifiques à un profil, ils peuvent intéresser un certain nombre de profils : les particuliers abonnés à des sujets d&#39;actualité spécifiques, les passagers d&#39;un vol, les acheteurs intéressés par un produit en rupture de stock, etc. Les événements métier sont toujours basés sur des règles. Lorsque vous déposez un événement métier dans un parcours, il ajoute automatiquement une activité **Lecture de segment** juste après. Pour savoir comment créer un événement métier, consultez cette [page](../event/about-creating-business.md).


>[!NOTE]
>
>Si vous modifiez un événement utilisé dans un parcours actif ou dans un état de brouillon, vous pouvez uniquement en modifier le nom ou la description, ou ajouter des champs de payload. La modification des parcours actifs ou dans un état de brouillon est strictement limitée pour éviter de les interrompre.

➡️ [Découvrez cette fonctionnalité en vidéo](#video)

## Type d’identifiant d&#39;événement{#event-id-type}

Pour les événements métier, le type d’identifiant d&#39;événement est toujours basé sur des règles.

Pour les événements unitaires, il existe deux types d’identifiant d&#39;événement :

* **Événements** basés sur des règles : ce type d’événement ne génère pas d’eventID. En utilisant l’éditeur d’expression simple, vous définissez simplement une règle qui sera utilisée par le système pour identifier les événements pertinents qui déclencheront vos parcours. Cette règle peut être basée sur n’importe quel champ disponible dans la payload de l’événement, par exemple l’emplacement du profil ou le nombre d’éléments ajoutés au panier du profil.

   >[!CAUTION]
   >
   >Une règle de limitation est définie pour les événements basés sur des règles. Il limite à 5 000 le nombre d’événements qualifiés qu’un parcours peut traiter par seconde pour une organisation donnée. Il correspond à des contrats de niveau de service Journey Optimizer. Reportez-vous à votre licence Journey Optimizer et [Description du produit Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html).

* **Événements** générés par le système : ces événements nécessitent un eventID. Ce champ eventID est généré automatiquement lors de la création de l’événement. Le système à l’origine de l’envoi de l’événement ne doit pas générer d’identifiant, mais plutôt transmettre celui indiqué dans la prévisualisation de la payload.

Journey Optimizer nécessite que les événements soient diffusés en continu ou par lots dans Adobe Experience Platform. Ces données n&#39;ont pas nécessairement besoin d&#39;accéder au profil en temps réel. Si vous souhaitez utiliser les événements pour la segmentation ou la recherche dans un parcours distinct, nous vous recommandons d&#39;activer le jeu de données pour profile.

## Cycle des données {#data-cycle}

Les événements sont des appels d’API POST. Ils sont envoyés à Adobe Experience Platform par biais des API d’ingestion en flux continu. L’URL de destination des événements envoyés via les API de messagerie transactionnelle est appelée « inlet ». La payload des événements respecte la mise en forme XDM.

La payload contient les informations nécessaires au fonctionnement des API d’ingestion en flux continu (dans l’en-tête) et  les informations requises par [!DNL Journey Optimizer] pour travailler, ainsi que les informations à utiliser dans les parcours (dans le corps, par exemple, le montant d’un panier abandonné). Il existe deux modes d’ingestion en flux continu : authentifié et non authentifié. Pour plus d’informations sur les API d’ingestion en flux continu, cliquez sur [ce lien](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=fr).

Après avoir transité par les API d’ingestion en flux continu, les événements se propagent dans un service interne appelé Pipeline, puis dans Adobe Experience Platform. Si l’indicateur du service de profil client en temps réel est activé pour le schéma d’événement et que ce dernier comprend également un identifiant de jeu de données avec l’indicateur de profil client en temps réel, le schéma est propagé dans ce service.

Pour les événements générés par le système, le service Pipeline filtre les événements disposant d’une payload contenant des [!DNL Journey Optimizer] eventID (reportez-vous au processus de création d’événements ci-dessous) fournis par [!DNL Journey Optimizer] et contenus dans une payload d’événement. Pour les événements basés sur des règles, le système identifie l’événement à l’aide de la condition eventID. Ces événements sont écoutés par [!DNL Journey Optimizer] et le parcours correspondant est déclenché.

## Tutoriels vidéo {#video}

Découvrez comment configurer un événement, spécifier le point dʼentrée du flux en continu et la payload dʼun événement.

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Comprendre les cas d’utilisation applicables pour les événements métier. Découvrez comment créer un parcours à l’aide d’un événement métier et les bonnes pratiques à appliquer.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
