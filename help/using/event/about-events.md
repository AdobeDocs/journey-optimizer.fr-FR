---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser des événements de parcours
description: Découvrir comment utiliser des événements dans vos parcours
feature: Journeys, Events
topic: Administration
role: Data Engineer, Data Architect, Admin
level: Intermediate, Experienced
keywords: événements, événement, parcours, définition, commencer
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
source-git-commit: 8701afe345f0eeed1503e4765d4715398823b102
workflow-type: tm+mt
source-wordcount: '1079'
ht-degree: 95%

---

# Utiliser des événements de parcours {#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Événements de parcours"
>abstract="Un événement est lié à une personne. Il s’agit du comportement d’une personne (par exemple, une personne a acheté un produit, a visité un magasin, est sortie d’un site web, etc.) ou d’un élément lié à une personne (par exemple, une personne a atteint 10 000 points de fidélité). Journey Optimizer écoute les événements unitaires dans les parcours pour orchestrer les meilleures actions suivantes."

Utilisez des événements pour déclencher les parcours individuellement, en envoyant des messages en temps réel à chaque utilisateur ou utilisatrice dès son entrée dans le parcours.

Dans la configuration des événements, vous configurez les événements attendus dans les parcours. Les données des événements entrants sont normalisées conformément au modèle de données d’expérience Adobe (XDM). Les événements authentifiés et non authentifiés proviennent des API d’ingestion en flux continu (notamment ceux issus du kit de développement Adobe Mobile SDK). Vous pouvez utiliser plusieurs événements (à différentes étapes d’un parcours) et plusieurs parcours peuvent utiliser un même événement.

La configuration de l’événement est **obligatoire** et doit être effectuée par un ingénieur ou une ingénieure de données.

Vous pouvez configurer deux types d’événements : des **événements unitaires** et des **événements métier**.

➡️ [Découvrez cette fonctionnalité en vidéo.](#video)

## Événements unitaires {#unitary-events}

Les événements **unitaires** sont liés à une personne. Il s’agit du comportement d’une personne (par exemple, une personne a acheté un produit, a visité un magasin, a quitté un site web, etc.) ou d’une chose qui se produit et qui est liée à une personne (par exemple, une personne qui atteint 10 000 points de fidélité). C’est ce type d’élément que [!DNL Journey Optimizer] écoute dans les parcours pour orchestrer les meilleures actions qu’il convient de prendre ensuite. Les événements unitaires peuvent être générés selon des règles ou par un système. Pour savoir comment créer un événement unitaire, consultez cette [page](../event/about-creating.md).

Les parcours unitaires (qui commencent par un événement ou une qualification d’audience) incluent un mécanisme de sécurisation qui empêche les parcours d’être déclenchés par erreur plusieurs fois pour le même événement. La rentrée du profil est temporairement bloquée par défaut pendant 5 minutes. Par exemple, si un événement déclenche un parcours à 12:01 pour un profil spécifique et qu’un autre événement se produit à 12:03 (qu’il s’agisse du même événement ou d’un autre déclenchant le même parcours), ce parcours ne reprendra pas pour ce profil.

## Événements métier {#business-events}

Les événements **métier** ne sont pas liés à un profil spécifique. Par exemple, il peut s’agir d’une alerte d’actualité, d’une mise à jour sportive, d’un changement ou d’une annulation de vol, d’une mise à jour d’inventaire, d&#39;événements météorologiques, etc. Bien que ces événements ne soient pas spécifiques à un profil, ils peuvent intéresser un certain nombre de profils : les particuliers abonnés à des sujets d&#39;actualité spécifiques, les passagers d&#39;un vol, les acheteurs intéressés par un produit en rupture de stock, etc. Les événements métier sont toujours basés sur des règles. Lorsque vous ajoutez un événement métier dans un parcours, cela ajoute automatiquement une activité **Lecture d’audience** juste après. Découvrez comment créer un événement métier [sur cette page](../event/about-creating-business.md). 


## Type d’identifiant d’événement {#event-id-type}

Pour les événements **métier**, le type d’identifiant d’événement est toujours basé sur des règles.

Pour les événements **unitaires**, il existe deux types d’identifiant d’événement :

* Événements **basés sur des règles** : ce type d’événement ne génère pas d’eventID. En utilisant l’éditeur d’expression simple, vous définissez simplement une règle qui sera utilisée par le système pour identifier les événements pertinents qui déclencheront vos parcours. Cette règle peut être basée sur n’importe quel champ disponible dans le payload de l’événement, par exemple l’emplacement du profil ou le nombre d’éléments ajoutés au panier du profil.

  >[!CAUTION]
  >
  >Une règle de limitation est définie pour les événements basés sur des règles. Il limite à 5 000 le nombre d’événements qualifiés qu’un parcours peut traiter par seconde pour une organisation donnée. Il correspond à des contrats de niveau de service Journey Optimizer. Reportez-vous à votre licence Journey Optimizer et à la Description du produit [Journey Optimizer](https://helpx.adobe.com/fr/legal/product-descriptions/adobe-journey-optimizer.html).

* **Événements** générés par le système : ces événements nécessitent un eventID. Ce champ eventID est généré automatiquement lors de la création de l’événement. Le système à l’origine de l’envoi de l’événement ne doit pas générer d’identifiant, mais plutôt transmettre celui indiqué dans la prévisualisation de la payload.

>[!NOTE]
>
>Journey Optimizer exige que les événements soient diffusés en continu vers Data Collection Core Service (DCCS) pour pouvoir déclencher un parcours. Les événements ingérés par lot ou les événements provenant de jeux de données Journey Optimizer internes (commentaires des messages, tracking e-mail, etc.) ne peuvent pas être utilisés pour déclencher un parcours. Pour les cas d’utilisation où vous ne pouvez pas obtenir d’événements en flux continu, créez un segment basé sur ces événements et utilisez l’activité **Lecture d’audience** à la place. La qualification d’audience peut techniquement être utilisée, mais peut entraîner des difficultés en aval en fonction des actions utilisées. Ces données n’ont pas nécessairement besoin d’accéder au profil en temps réel. Si vous souhaitez utiliser les événements pour la segmentation, nous vous recommandons d’activer le jeu de données pour le profil.

## Cycle des données {#data-cycle}

Les événements sont des appels d’API POST. Ils sont envoyés à Adobe Experience Platform par biais des API d’ingestion en flux continu. L’URL de destination des événements envoyés via les API de messagerie transactionnelle est appelée « inlet ». La payload des événements respecte la mise en forme XDM.

La payload contient les informations nécessaires au fonctionnement des API d’ingestion en flux continu (dans l’en-tête) et  les informations requises par [!DNL Journey Optimizer] pour travailler, ainsi que les informations à utiliser dans les parcours (dans le corps, par exemple, le montant d’un panier abandonné). Il existe deux modes d’ingestion en flux continu : authentifié et non authentifié. Pour plus d’informations sur les API d’ingestion en flux continu, cliquez sur [ce lien](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=fr){target="_blank"}.

Après avoir transité par les API d’ingestion en flux continu, les événements se propagent dans un service interne appelé Pipeline, puis dans Adobe Experience Platform. Si l’indicateur du service de profil client en temps réel est activé pour le schéma d’événement et que ce dernier comprend également un identifiant de jeu de données avec l’indicateur de profil client en temps réel, le schéma est propagé dans ce service.

Pour les événements générés par le système, le service Pipeline filtre les événements disposant d’une payload contenant des [!DNL Journey Optimizer] eventID (reportez-vous au processus de création d’événements ci-dessous) fournis par [!DNL Journey Optimizer] et contenus dans une payload d’événement. Pour les événements basés sur des règles, le système identifie l’événement à l’aide de la condition eventID. Ces événements sont écoutés par [!DNL Journey Optimizer] et le parcours correspondant est déclenché.

## Mise à jour et suppression d’un événement {#update-event}


Pour éviter de rompre des parcours existants, lorsque vous modifiez un événement utilisé dans un parcours **Brouillon**, **En ligne** ou **Fermé**, vous pouvez uniquement modifier le nom, la description ou ajouter des champs de payload.

Les événements utilisés dans les parcours **En ligne**, **Brouillon** ou **Fermé** ne peuvent pas être supprimés. Pour supprimer un événement utilisé, vous devez arrêter les parcours qui l’utilisent et/ou le supprimer des brouillons de parcours. Vous pouvez cocher le champ **[!UICONTROL Utilisé dans]**. Il affiche le nombre de parcours qui utilisent cet événement particulier. Vous pouvez cliquer sur le bouton **[!UICONTROL Afficher les parcours]** pour faire apparaître la liste des parcours correspondants.

## Tutoriels vidéo {#video}

Découvrez comment configurer un événement, spécifier le point dʼentrée du flux en continu et la payload dʼun événement.

>[!VIDEO](https://video.tv.adobe.com/v/3431514?quality=12&captions=fre_fr)

Comprendre les cas d’utilisation applicables pour les événements métier. Découvrez comment créer un parcours à l’aide d’un événement métier et les bonnes pratiques à appliquer.

>[!VIDEO](https://video.tv.adobe.com/v/3416325?quality=12&captions=fre_fr)
