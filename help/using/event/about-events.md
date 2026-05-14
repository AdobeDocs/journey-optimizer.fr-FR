---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser des événements de parcours
description: Découvrir comment utiliser des événements dans vos parcours
feature: Journeys, Events
topic: Administration
role: Developer, Admin
level: Intermediate, Experienced
keywords: événements, événement, parcours, définition, commencer
exl-id: fb3e51b5-4cbb-4949-8992-1075959da67d
TQID: https://experienceleague.adobe.com/xvLSBd-rwKKNqwQNDa4D8GfFzc-ND1FkC3EdstufkIY
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: bb359667-ec7d-4d4b-8663-5850fc219d32id: d556b755-390a-43f0-be32-a08cf6236126id: d998adac-2f81-400b-a669-d07bb196e4ebid: df64005d-8f9a-422e-ba4d-c6f6dc3454b4id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2: id: b3a93754-a8b8-46eb-9421-7eccaeeb3dffid: d08afb72-92f6-4856-88e3-11ec34313c2fid: d2e8a157-b3b0-4143-9ff3-809bf400be56id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2: id: c66ffd68-0f65-42bb-aa23-b4020f12e0bdid: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2: id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2: id: d3cdead0-685a-4489-9250-4bb709942f66id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 2152
ht-degree: 65%

---

# Utiliser des événements de parcours {#about-events}

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Événements de parcours"
>abstract="Journey Optimizer prend en charge trois types d’événements dans les parcours : les événements unitaires, liés au comportement d’une personne spécifique (comme un achat ou un jalon de fidélité) ; les événements métier, déclenchés par un événement global (comme une annulation de vol ou une mise à jour d’inventaire) ; et les événements de qualification d’audience, déclenchés lorsqu’un profil entre ou quitte une audience. Utilisez des événements pour déclencher des parcours et orchestrer les actions appropriées pour vos profils."

Utilisez des événements pour déclencher les parcours individuellement, en envoyant des messages en temps réel à chaque utilisateur ou utilisatrice dès son entrée dans le parcours.

>[!IMPORTANT]
>
>Pour connaître les exigences et les limitations des événements (diffusion en continu, Query Service, ingestion par lots), consultez [Mécanismes de sécurisation de Parcours - Événements](../start/guardrails.md#events-g).

Dans la configuration des événements, vous configurez les événements attendus dans les parcours. Les données des événements entrants sont normalisées conformément au modèle de données d’expérience Adobe (XDM). Les événements authentifiés et non authentifiés proviennent des API Streaming Ingestion (comme les événements du kit de développement Adobe Mobile SDK). Vous pouvez utiliser plusieurs événements (à différentes étapes d’un parcours) et plusieurs parcours peuvent utiliser un même événement.

La configuration de l’événement est **obligatoire** et doit être effectuée par un ingénieur ou une ingénieure de données.

Vous pouvez configurer trois types d’événements : **Événements unitaires**, **Événements métier** et **Événements de qualification d’audience**.

➡️ [Découvrez cette fonctionnalité en vidéo.](#video)

## Événements unitaires {#unitary-events}

Les événements **unitaires** sont liés à une personne. Elles sont liées au comportement d’une personne (par exemple, une personne a acheté un produit, a visité un magasin, a quitté un site web, etc.) ou un événement qui s’est produit en rapport avec cette personne (par exemple, elle a accumulé 10 000 points de fidélité). C’est ce type d’élément que [!DNL Journey Optimizer] écoute dans les parcours pour orchestrer les meilleures actions qu’il convient de prendre ensuite. Les événements unitaires peuvent être générés selon des règles ou par un système. Pour savoir comment créer un événement unitaire, consultez cette [page](../event/about-creating.md).

Les parcours unitaires (qui commencent par un événement ou une qualification d’audience) incluent un mécanisme de sécurisation qui empêche les parcours d’être déclenchés par erreur plusieurs fois pour le même événement. La rentrée du profil est temporairement bloquée par défaut pendant 5 minutes. Par exemple, si un événement déclenche un parcours à 12:01 pour un profil spécifique et qu’un autre événement se produit à 12:03 (qu’il s’agisse du même événement ou d’un autre déclenchant le même parcours), ce parcours ne reprendra pas pour ce profil.

## Événements métier {#business-events}

Les événements **métier** ne sont pas liés à un profil spécifique. Par exemple, il peut s’agir d’une alerte aux informations, d’une mise à jour sportive, d’un changement ou d’une annulation de vol, d’une mise à jour des stocks, d’événements météorologiques, etc. Bien que ces événements ne soient pas spécifiques à un profil, ils peuvent intéresser un certain nombre de profils : les individus abonnés à des sujets d&#39;actualité spécifiques, les passagers d&#39;un vol, les acheteurs intéressés par un produit en rupture de stock, etc. Les événements métier sont toujours basés sur des règles. Lorsque vous déposez un événement métier dans un parcours, cela ajoute automatiquement une activité **Lecture d’audience** juste après. Découvrez comment créer un événement métier [sur cette page](../event/about-creating-business.md).

## Événements de qualification d’audience {#audience-qualification-events}

Un événement **qualification de l’audience** est déclenché lorsqu’un profil entre ou quitte une audience. Par exemple, un client qui dépasse un seuil de dépenses de fidélité entre dans l’audience de niveau Gold ; cette qualification déclenche le parcours de ce profil en temps réel (pour les audiences de streaming) ou lors de l’évaluation du lot suivant. Contrairement aux événements unitaires, la qualification d’audience vous permet de créer une logique de déclenchement complexe en utilisant toute la puissance des définitions d’audience, sans avoir à apporter de modifications à l’implémentation pour envoyer un nouvel événement. En savoir plus sur les [événements de qualification d’audience](../building-journeys/audience-qualification-events.md).

>[!NOTE]
>
>Les événements de qualification d’audience ne sont pas configurés dans **Administration > Événements** — ils sont sélectionnés directement sur la zone de travail de parcours comme première étape d’un parcours.

## Événements unitaires ou métier en un coup d’œil {#event-comparison}

| | Événement unitaire | Événement métier |
|---|---|---|
| **Lié à un profil ?** | Oui — déclenché par l&#39;action d&#39;une personne spécifique. | Non : déclenché par une occurrence externe qui n’est pas liée à une personne. |
| **Comportement d’entrée** | Un profil entre sur le parcours en temps réel. | Plusieurs profils rejoignent l’audience par le biais d’une étape Lecture d’audience automatique. |
| **Cas d’utilisation standard** | Confirmation d’achat, envoi de formulaire, connexion à l’application, jalon de fidélité. | Annulation du vol, alerte de réapprovisionnement des stocks, nouvelles de dernière minute, événement météorologique. |
| **Comment commence le parcours** | Entrée basée sur un événement : aucune audience nécessaire. | Événement métier + lecture d’audience automatique (ajoutée par Journey Optimizer). |
| **Plusieurs par parcours ?** | Oui — vous pouvez écouter plusieurs événements unitaires à travers des étapes parcours. | Non : un seul événement métier par parcours, placé au début. |
| **Type d’identifiant d’événement** | Basé sur des règles ou généré par le système. | Toujours basé sur des règles. |

>[!NOTE]
>
>Un parcours ne peut contenir qu **un seul événement métier** qui doit être la première activité. Journey Optimizer ajoute automatiquement une activité **Lecture d’audience** à sa suite pour définir les profils qui recevront le parcours déclenché par cet événement.

## Type d’identifiant d’événement {#event-id-type}

Pour les événements **métier**, le type d’identifiant d’événement est toujours basé sur des règles.

Pour les événements **unitaires**, il existe deux types d’identifiant d’événement :

* Événements **basés sur des règles** : ce type d’événement ne génère pas d’eventID. En utilisant l’éditeur d’expression simple, vous définissez simplement une règle qui sera utilisée par le système pour identifier les événements pertinents qui déclencheront vos parcours. Cette règle peut être basée sur n’importe quel champ disponible dans le payload de l’événement, par exemple l’emplacement du profil ou le nombre d’éléments ajoutés au panier du profil.

  >[!CAUTION]
  >
  >Une règle de limitation est définie pour les événements basés sur des règles. Il limite à 5 000 le nombre d’événements qualifiés qu’un parcours peut traiter par seconde pour une organisation donnée. Il correspond à des contrats de niveau de service Journey Optimizer. Reportez-vous à votre licence Journey Optimizer et à la [description du produit Journey Optimizer](https://helpx.adobe.com/legal/product-descriptions/adobe-journey-optimizer.html){target="_blank"}.

* **Événements** générés par le système : ces événements nécessitent un eventID. Ce champ eventID est généré automatiquement lors de la création de l’événement. Le système à l’origine de l’envoi de l’événement ne doit pas générer d’identifiant, mais plutôt transmettre celui indiqué dans la prévisualisation de la payload.

>[!NOTE]
>
>Journey Optimizer exige que les événements soient diffusés en continu vers Data Collection Core Service (DCCS) pour pouvoir déclencher un parcours. Les événements ingérés par lot, les événements insérés via **Query Service**, ou les événements provenant de jeux de données Journey Optimizer internes (commentaires des messages, tracking e-mail, etc.) ne peuvent pas être utilisés pour déclencher un parcours. Pour les cas d’utilisation où vous ne pouvez pas obtenir d’événements en flux continu, créez un segment basé sur ces événements et utilisez l’activité **Lecture d’audience** à la place. La qualification d’audience peut techniquement être utilisée, mais peut entraîner des difficultés en aval en fonction des actions utilisées. Ces données n’ont pas nécessairement besoin d’accéder au profil en temps réel. Si vous souhaitez utiliser les événements pour la segmentation, nous vous recommandons d’activer le jeu de données pour le profil.

## Comment choisir {#choose-event-type}

Utilisez les critères suivants pour sélectionner le type d’événement approprié à votre parcours. La question essentielle est la suivante : **déclenchez-vous une action pour une personne spécifique ou diffusez-vous des événements vers plusieurs profils ?** [En savoir plus sur les types de parcours ](../building-journeys/journey.md#journey-types).

* **Choisissez un événement unitaire** lorsque le déclencheur est lié à une personne spécifique (par exemple, un achat, un envoi de formulaire ou un jalon de fidélité). Les événements unitaires nécessitent une identité principale basée sur une personne dans le schéma et lancent immédiatement le parcours pour ce profil. [Découvrez comment configurer un événement unitaire](../event/about-creating.md).

* **Choisissez un événement métier** lorsque le déclencheur est un événement global (par exemple, un réapprovisionnement de produit, une baisse de prix ou une annulation de vol) et que vous souhaitez diffuser vers un ensemble de profils liés à ce signal. Les événements métier doivent être la première étape du parcours et cibler automatiquement les profils par le biais d&#39;une activité **Lecture d&#39;audience**. Ils nécessitent un schéma de série temporelle avec une identité principale autre que des personnes et les champs `_id` et `timestamp`. Planifiez un délai d’exportation d’audience de 15 minutes à jusqu’à une heure. [Découvrez comment configurer un événement métier](../event/about-creating-business.md).

* **Choisissez un événement de qualification d’audience** lorsque le déclencheur est un profil qui entre ou sort d’une audience et que vous avez besoin d’une logique de segmentation plus complexe que celle qu’un seul événement peut fournir (par exemple, réengager des clients obsolètes qui viennent d’atteindre un seuil de dépenses ou déclencher un flux de délocalisation lorsqu’un membre de VIP abandonne le niveau de fidélité). [En savoir plus sur les événements de qualification d’audience](../building-journeys/audience-qualification-events.md).

>[!CAUTION]
>
>Les événements métier ne peuvent pas être utilisés dans le même parcours que les événements unitaires ou les activités de qualification d’audience.

## Cycle des données {#data-cycle}

Les événements sont des appels d’API POST. Ils sont envoyés à Adobe Experience Platform par biais des API d’ingestion en flux continu. L’URL de destination des événements envoyés via les API de messagerie transactionnelle est appelée « inlet ». La payload des événements respecte la mise en forme XDM.

La payload contient les informations nécessaires au fonctionnement des API d’ingestion en flux continu (dans l’en-tête) et  les informations requises par [!DNL Journey Optimizer] pour travailler, ainsi que les informations à utiliser dans les parcours (dans le corps, par exemple, le montant d’un panier abandonné). Il existe deux modes d’ingestion en flux continu : authentifié et non authentifié. Pour plus d’informations sur les API d’ingestion en flux continu, cliquez sur [ce lien](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=fr){target="_blank"}.

Après avoir transité par les API d’ingestion en flux continu, les événements se propagent dans un service interne appelé Pipeline, puis dans Adobe Experience Platform. Si l’indicateur du service de profil client en temps réel est activé pour le schéma d’événement et que ce dernier comprend également un identifiant de jeu de données avec l’indicateur de profil client en temps réel, le schéma est propagé dans ce service.

Pour les événements générés par le système, le service Pipeline filtre les événements disposant d’une payload contenant des [!DNL Journey Optimizer] eventID (reportez-vous au processus de création d’événements ci-dessous) fournis par [!DNL Journey Optimizer] et contenus dans une payload d’événement. Pour les événements basés sur des règles, le système identifie l’événement à l’aide de la condition eventID. Ces événements sont écoutés par [!DNL Journey Optimizer] et le parcours correspondant est déclenché.


## À propos du débit des événements de parcours {#event-thoughput}

Adobe Journey Optimizer prend en charge un volume maximal de 5 000 événements de parcours par seconde au niveau d’une organisation, sur tous les sandbox. Ce quota s’applique à tous les événements utilisés dans les parcours en cours, qui incluent les parcours **Actifs**, de **Test à blanc**, **Fermés** et **Mis en pause**. Lorsque ce quota est atteint, les nouveaux événements sont mis en file d’attente avec un taux de traitement de 5 000 éléments par seconde. La durée maximale qu’un événement peut passer dans la file d’attente est de **24 heures**.

Pour plus d’informations sur les taux de traitement des parcours et sur la façon dont les types de parcours affectent les débits, consultez [cette section](../building-journeys/entry-management.md#journey-processing-rate).

Les types d’événements suivants sont comptabilisés dans le quota des 5 000 TPS :

* **Événements unitaires externes** : inclut les événements basés sur des règles et ceux générés par le système. Si un même événement brut est admissible à plusieurs définitions de règle, chaque règle admise est comptabilisée comme un événement distinct. Vous trouverez plus de détails ci-dessous.

* **Événements de qualification d’audience** : si la même audience en streaming est utilisée dans plusieurs parcours, chaque utilisation est comptabilisée séparément. Par exemple, l’emploi d’une même audience dans une activité de qualification d’audience dans deux parcours génère deux événements comptabilisés.

* **Événements de réaction** : événements déclenchés par des réactions de profil (ouverture d’e-mail, clic sur l’e-mail, etc.) dans un parcours.

* **Événements métiers** : événements non liés à un profil spécifique, mais à un événement lié à l’activité professionnelle.

* **Événements Analytics** : si l’[intégration à Adobe Analytics a été activée en vue de déclencher des parcours](about-analytics.md), ces événements sont également inclus.

* **Événements de reprise** : événement technique déclenché lorsqu’un profil reprend à partir d’un parcours en pause. En savoir plus sur la [reprise des parcours mis en pause](../building-journeys/journey-pause.md#journey-resume-steps).

* **Événements d’achèvement de nœud d’attente** : lorsqu’un profil quitte un nœud d’attente, un événement technique est généré pour reprendre le parcours.

>[!NOTE]
>
>À l’exception des événements d’attente et de reprise, tous les autres types d’événements sont également comptabilisés dans le quota lorsqu’ils sont utilisés dans des parcours basés sur des audiences lues.

### À propos des événements bruts admissibles pour plusieurs définitions de règle

Un même événement brut peut être admissible pour plusieurs définitions de règle dans les parcours. Lorsqu’un événement est configuré dans la section **Administration**, pour le même schéma d’événement, plusieurs règles d’événement peuvent être définies. Supposons, par exemple, que nous ayons un événement d’achat qui comporte les champs city et purchaseValue. Examinons les scénarios suivants :

1. Un événement **E1** nommé `newYorkPurchases` est créé avec une définition de règle indiquant `city=='New York'`. Cet événement peut être utilisé dans 10 parcours, mais il sera toujours comptabilisé comme 1 seul événement lorsqu’il sera disponible.

1. Maintenant, supposons qu’un événement **E2** nommé `highValuePurchases` avec `purchaseValue > 1000` comme définition de règle soit également créé, sur le même schéma d’événement que **E1**. Dans ce cas, le même événement entrant est évalué par rapport à deux règles : `newYorkPurchases` et `highValuePurchases`. Maintenant, il se peut qu’un achat à New York soit également un achat de grande valeur.

   Dans ce cas, Journey Optimizer crée deux événements, **E1** et **E2**, à partir du même événement entrant, ce qui fait que cet événement entrant unique compte comme deux événements.

   Notez que ces événements commencent à être comptabilisés lorsqu’ils sont utilisés dans un parcours actif, y compris les parcours **actifs**, de **test à blanc**, **fermés** et **en pause**.

## Mise à jour et suppression d’un événement {#update-event}


Pour éviter d’interrompre les parcours existants, lorsque vous modifiez un événement utilisé dans un parcours **brouillon**, **actif** ou **fermé**, vous pouvez uniquement en modifier le nom ou la description, ou ajouter des champs de payload.

Les événements utilisés dans des parcours **actifs**, **brouillons** ou **fermés** ne peuvent pas être supprimés. Pour supprimer un événement utilisé, vous devez arrêter les parcours qui l’utilisent et/ou le supprimer des brouillons de parcours. Vous pouvez cocher le champ **[!UICONTROL Utilisé dans]**. Il affiche le nombre de parcours qui utilisent cet événement particulier. Vous pouvez cliquer sur le bouton **[!UICONTROL Afficher les parcours]** pour faire apparaître la liste des parcours correspondants.

## Vidéos pratiques {#video}

Découvrez comment configurer un événement, spécifier le point dʼentrée du flux en continu et la payload dʼun événement.

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Comprendre les cas d’utilisation applicables pour les événements métier. Découvrez comment créer un parcours à l’aide d’un événement métier et les bonnes pratiques à appliquer.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
