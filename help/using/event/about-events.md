---
title: A propos des événements
description: En savoir plus sur les événements
translation-type: tm+mt
source-git-commit: 5c3f1e4d916c7259f25208785788d2566b316934
workflow-type: tm+mt
source-wordcount: '724'
ht-degree: 0%

---

# A propos des événements{#concept_gfj_fqt_52b}

![](../assets/do-not-localize/badge.png)

>[!CONTEXTUALHELP]
>id="jo_events"
>title="A propos des événements"
>abstract="Un événement est lié à une personne. Il se rapporte au comportement d&#39;une personne (par exemple, une personne a acheté un produit, a visité un magasin, est sortie d&#39;un site Web, etc.) ou quelque chose qui se passe lié à une personne (par exemple, une personne a atteint 10 000 points de fidélité). C&#39;est ce que [!DNL Journey Optimizer] va écouter dans les parcours pour orchestrer les meilleures actions suivantes."

La configuration du événement vous permet de définir les informations que [!DNL Journey Optimizer] recevra en tant que événements. Vous pouvez utiliser plusieurs événements (à différentes étapes d’un parcours) et plusieurs parcours peuvent utiliser le même événement.

>[!CAUTION]
>
>La configuration du événement est **obligatoire** et doit être effectuée par un **utilisateur technique**.

Vous pouvez configurer deux types de événements :

* **** Unitaryevents : ces événements sont liés à une personne. Ils se rapportent au comportement d&#39;une personne (par exemple, une personne a acheté un produit, a visité un magasin, est sortie d&#39;un site Web, etc.) ou quelque chose qui se passe lié à une personne (par exemple, une personne a atteint 10 000 points de fidélité). C&#39;est ce que [!DNL Journey Optimizer] va écouter dans les parcours pour orchestrer les meilleures actions suivantes. Les événements uniques peuvent être générés selon des règles ou par un système. Pour savoir comment créer un événement unitaire, consultez cette [page](../event/about-creating.md).

* **** Entreprises : un événement d&#39;entreprise est un événement qui, contrairement à un événement unitaire, n&#39;est pas lié à un profil spécifique. Par exemple, il peut s’agir d’une alerte de l’actualité, d’une mise à jour du sport, d’un changement ou d’une annulation de vol, d’une mise à jour de l’inventaire, de événements météorologiques, etc. Bien que ces événements ne soient pas spécifiques à un profil, ils peuvent intéresser un certain nombre de profils : les particuliers s&#39;abonnaient à des sujets d&#39;actualité particuliers, les passagers en vol, les acheteurs intéressés par un produit en rupture de stock, etc. Les événements d&#39;entreprise sont toujours basés sur des règles. Lorsque vous déposez un événement métier dans un parcours, il ajoute automatiquement une activité **Lire le segment** juste après. Pour savoir comment créer un événement d&#39;entreprise, consultez cette [page](../event/about-creating-business.md).


>[!NOTE]
>
>Si vous modifiez un événement utilisé dans un brouillon ou un parcours actif, vous pouvez uniquement modifier le nom, la description ou ajouter des champs de charge utile. Nous limitons strictement l&#39;édition des ébauches ou des parcours en direct pour éviter de briser les parcours.

## Type d’ID de événement{#event-id-type}

Pour les événements professionnels, le type d’ID de événement est toujours basé sur des règles.

Pour les événements unitaires, il existe deux types d’ID de événement :

* **Événements** fondés sur des règles : ce type de événement ne génère pas d’eventID. En utilisant l&#39;éditeur d&#39;expressions simple, vous définissez simplement une règle qui sera utilisée par le système pour identifier les événements pertinents qui déclencheront vos parcours. Cette règle peut être basée sur n’importe quel champ disponible dans la charge de événement, par exemple l’emplacement du profil ou le nombre d’éléments ajoutés au panier du profil.

   >[!CAUTION]
   >
   >Une règle de plafonnement est définie pour les événements basés sur des règles. Il limite à 5 000 le nombre de événements qualifiés qu’un parcours peut traiter par seconde pour une organisation donnée (ORG). Il correspond aux ALS Journey Optimizer. Voir cette [page](https://helpx.adobe.com/legal/product-descriptions/journey-orchestration.html).

* **Équipements** générés par le système : ces événements nécessitent un eventID. Ce champ eventID est généré automatiquement lors de la création du événement. Le système qui pousse le événement ne doit pas générer d’identifiant, il doit transmettre celui disponible dans la prévisualisation de charge utile.

## Cycle de données {#section_r1f_xqt_pgb}

Les événements sont des appels d’API POST. Les événements sont envoyés à Adobe Experience Platform par le biais des API d&#39;importation en flux continu. La destination URL des événements envoyés par le biais des API de messagerie transactionnelle est appelée &quot;entrée&quot;. La charge utile des événements suit le formatage XDM.

La charge utile contient les informations requises par les API d&#39;importation en flux continu pour fonctionner (dans l&#39;en-tête) et les informations requises par [!DNL Journey Optimizer] pour fonctionner et les informations à utiliser dans les parcours (dans le corps, par exemple, la quantité d&#39;un panier abandonné). Il existe deux modes pour l’assimilation en flux continu, authentifié et non authentifié. Pour plus d&#39;informations sur les API d&#39;importation en flux continu, consultez [ce lien](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html).

Une fois les API d&#39;importation en flux continu arrivées, les événements s&#39;enchaînent dans un service interne appelé Pipeline, puis dans Adobe Experience Platform. Si l’indicateur Service de Profil client en temps réel est activé sur le schéma de événement et qu’un ID de jeu de données est également associé à l’indicateur Profil client en temps réel, il est transmis au service de Profil client en temps réel.

Pour les événements générés par le système, le pipeline filtres les événements dont la charge utile contient [!DNL Journey Optimizer] eventID (voir le processus de création de événement ci-dessous) fournis par [!DNL Journey Optimizer] et contenus dans la charge utile du événement. Pour les événements basés sur des règles, le système identifie le événement à l’aide de la condition eventID. Ces événements sont écoutés par [!DNL Journey Optimizer] et le parcours correspondant est déclenché.
