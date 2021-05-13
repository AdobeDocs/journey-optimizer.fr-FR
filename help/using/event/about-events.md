---
title: À propos des événements
description: En savoir plus sur les événements
translation-type: tm+mt
source-git-commit: 5c3f1e4d916c7259f25208785788d2566b316934
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 57%

---

# À propos des événements{#concept_gfj_fqt_52b}

![](../assets/do-not-localize/badge.png)

>[!CONTEXTUALHELP]
>id="jo_events"
>title="À propos des événements"
>abstract="Un événement est lié à une personne. Il décrit son comportement (par exemple, cette personne a acheté un produit, a visité un magasin, a quitté un site web, etc.) ou un événement qui s’est produit en rapport avec cette personne (par exemple, elle a accumulé 10 000 points de fidélité). C’est ce type d’élément que [!DNL Journey Optimizer] écoute dans les parcours pour orchestrer les meilleures actions qu’il convient de prendre ensuite."

La configuration d’événement vous permet de définir les informations que [!DNL Journey Optimizer] recevra en tant qu’événements. Vous pouvez utiliser plusieurs événements (à différentes étapes d’un parcours) et plusieurs parcours peuvent utiliser le même événement.

>[!CAUTION]
>
>La configuration du événement est **obligatoire** et doit être effectuée par un **utilisateur technique**.

Vous pouvez configurer deux types de événements :

* **** Unitaryevents : ces événements sont liés à une personne. Ils se rapportent au comportement d&#39;une personne (par exemple, une personne a acheté un produit, a visité un magasin, est sortie d&#39;un site Web, etc.) ou un événement qui s’est produit en rapport avec cette personne (par exemple, elle a accumulé 10 000 points de fidélité). C’est ce type d’élément que [!DNL Journey Optimizer] écoute dans les parcours pour orchestrer les meilleures actions qu’il convient de prendre ensuite. Les événements uniques peuvent être générés selon des règles ou par un système. Pour savoir comment créer un événement unitaire, consultez cette [page](../event/about-creating.md).

* **** Entreprises : un événement d&#39;entreprise est un événement qui, contrairement à un événement unitaire, n&#39;est pas lié à un profil spécifique. Par exemple, il peut s’agir d’une alerte de l’actualité, d’une mise à jour du sport, d’un changement ou d’une annulation de vol, d’une mise à jour de l’inventaire, de événements météorologiques, etc. Bien que ces événements ne soient pas spécifiques à un profil, ils peuvent intéresser un certain nombre de profils : les particuliers s&#39;abonnaient à des sujets d&#39;actualité particuliers, les passagers en vol, les acheteurs intéressés par un produit en rupture de stock, etc. Les événements d&#39;entreprise sont toujours basés sur des règles. Lorsque vous déposez un événement métier dans un parcours, il ajoute automatiquement une activité **Lire le segment** juste après. Pour savoir comment créer un événement d&#39;entreprise, consultez cette [page](../event/about-creating-business.md).


>[!NOTE]
>
>Si vous modifiez un événement utilisé dans un parcours actif ou dans un état de brouillon, vous pouvez uniquement en modifier le nom ou la description, ou ajouter des champs de payload. La modification des parcours actifs ou dans un état de brouillon est strictement limitée pour éviter de les interrompre.

## Type d’ID de événement{#event-id-type}

Pour les événements professionnels, le type d’ID de événement est toujours basé sur des règles.

Pour les événements unitaires, il existe deux types d’ID de événement :

* **Événements** basés sur des règles : ce type d’événement ne génère pas d’eventID. En utilisant l’éditeur d’expression simple, vous définissez simplement une règle qui sera utilisée par le système pour identifier les événements pertinents qui déclencheront vos parcours. Cette règle peut être basée sur n’importe quel champ disponible dans la payload de l’événement, par exemple l’emplacement du profil ou le nombre d’éléments ajoutés au panier du profil.

   >[!CAUTION]
   >
   >Une règle de limitation est définie pour les événements basés sur des règles. Il limite à 5 000 le nombre d’événements qualifiés qu’un parcours peut traiter par seconde pour une organisation donnée (ORG). Il correspond aux ALS Journey Optimizer. Voir cette [page](https://helpx.adobe.com/legal/product-descriptions/journey-orchestration.html).

* **Événements** générés par le système : ces événements nécessitent un eventID. Ce champ eventID est généré automatiquement lors de la création de l’événement. Le système à l’origine de l’envoi de l’événement ne doit pas générer d’identifiant, mais plutôt transmettre celui indiqué dans la prévisualisation de la payload.

## Cycle des données {#section_r1f_xqt_pgb}

Les événements sont des appels d’API POST. Les événements sont envoyés à Adobe Experience Platform par le biais des API d&#39;importation en flux continu. L’URL de destination des événements envoyés via les API de messagerie transactionnelle est appelée « inlet ». La payload des événements respecte la mise en forme XDM.

La charge utile contient les informations requises par les API d&#39;importation en flux continu pour fonctionner (dans l&#39;en-tête) et les informations requises par [!DNL Journey Optimizer] pour fonctionner et les informations à utiliser dans les parcours (dans le corps, par exemple, la quantité d&#39;un panier abandonné). Il existe deux modes d’ingestion en flux continu : authentifié et non authentifié. Pour plus d’informations sur les API d’ingestion en flux continu, cliquez sur [ce lien](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html).

Une fois les API d&#39;importation en flux continu arrivées, les événements s&#39;enchaînent dans un service interne appelé Pipeline, puis dans Adobe Experience Platform. Si l’indicateur du service de profil client en temps réel est activé pour le schéma d’événement et que ce dernier comprend également un identifiant de jeu de données avec l’indicateur de profil client en temps réel, le schéma est propagé dans ce service.

Pour les événements générés par le système, le service Pipeline filtre les événements disposant d’une payload contenant des [!DNL Journey Optimizer] eventID (reportez-vous au processus de création d’événements ci-dessous) fournis par [!DNL Journey Optimizer] et contenus dans une payload d’événement. Pour les événements basés sur des règles, le système identifie l’événement à l’aide de la condition eventID. Ces événements sont écoutés par [!DNL Journey Optimizer] et le parcours correspondant est déclenché.
