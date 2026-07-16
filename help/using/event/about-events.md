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
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: baecb07f-ce89-4ebb-9cd9-0f7c053f944f
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: d08afb72-92f6-4856-88e3-11ec34313c2f
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: c66ffd68-0f65-42bb-aa23-b4020f12e0bd
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: d3cdead0-685a-4489-9250-4bb709942f66
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 6657a77a27455643fa0fb3d94a4d7e3ab83e6843
workflow-type: tm+mt
source-wordcount: 2407
ht-degree: 29%

---

# Utiliser des événements de parcours {#about-events}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez les trois types d’événements, les exigences en matière de schéma, les contraintes clés et comment choisir celui qui convient à votre cas d’utilisation.

>[!ENDSHADEBOX]

>[!CONTEXTUALHELP]
>id="ajo_journey_event_list"
>title="Événements de parcours"
>abstract="Journey Optimizer prend en charge trois types d’événements dans les parcours : les événements unitaires, liés au comportement d’une personne spécifique (comme un achat ou un jalon de fidélité), les événements métier, déclenchés par un événement global (comme une annulation de vol ou une mise à jour d’inventaire) et les événements de qualification d’audience, déclenchés lorsqu’un profil entre ou quitte une audience. Utilisez des événements pour déclencher des parcours et orchestrer les actions appropriées pour vos profils."

Utilisez des événements pour déclencher les parcours individuellement, en envoyant des messages en temps réel à chaque utilisateur ou utilisatrice dès son entrée dans le parcours. Dans la configuration des événements, vous configurez les événements attendus dans les parcours. Vous pouvez utiliser plusieurs événements (à différentes étapes d’un parcours) et plusieurs parcours peuvent utiliser un même événement.

La configuration de l’événement est **obligatoire** et doit être effectuée par un ingénieur ou une ingénieure de données.

>[!IMPORTANT]
>
>* Avant de configurer des événements, assurez-vous d’avoir : le rôle **Administrateur** ou **Ingénieur de données**, un schéma XDM avec **Profil client en temps réel** activé, un point d’entrée de diffusion en continu actif et l’accès au sandbox approprié.
>
>* Pour connaître les exigences et les limitations des événements (diffusion en continu, Query Service, ingestion par lots), consultez [Mécanismes de sécurisation de Parcours - Événements](../start/guardrails.md#events-g).

**Qui fait quoi**

| Tâche | Rôle |
| --- | --- |
| Conception et création du schéma XDM | Ingénieur de données |
| Configurer le point d’entrée de diffusion en continu | Ingénieur de données |
| Configuration des événements unitaires et métier (**Administration > Événements**) | Ingénieur ou administrateur de données |
| Utilisation d’événements dans un parcours | praticien de parcours |
| Configurer des événements de qualification d’audience (sélectionnés sur la zone de travail) | praticien de parcours |

Vous pouvez configurer trois types d’événements : **Événements unitaires**, **Événements métier** et **Événements de qualification d’audience**.

➡️ [Découvrez cette fonctionnalité en vidéo.](#video)

➡️ [Découvrez cette fonctionnalité en vidéo.](#video)

## Événements unitaires {#unitary-events}

Les événements **unitaires** sont liés à une personne. Elles sont liées au comportement d’une personne (par exemple, une personne a acheté un produit, a visité un magasin, a quitté un site web, etc.) ou un événement qui s’est produit en rapport avec cette personne (par exemple, elle a accumulé 10 000 points de fidélité). C’est ce type d’élément que [!DNL Journey Optimizer] écoute dans les parcours pour orchestrer les meilleures actions qu’il convient de prendre ensuite. Les événements unitaires peuvent être générés selon des règles ou par un système. [Découvrez comment créer un événement unitaire](../event/about-creating.md).

**Schéma requis :** schéma XDM ExperienceEvent avec une identité principale basée sur la personne et **profil client en temps réel** activé.

**Exemple :** un client ajoute des articles à son panier et ferme le navigateur. Un événement abandonné au panier se déclenche, le profil entre sur le parcours en temps réel et reçoit un e-mail de récupération une heure plus tard.

>[!NOTE]
>
>Les parcours unitaires incluent un mécanisme de sécurisation de reprise : la reprise de profil est bloquée par défaut pendant 5 minutes après le déclenchement du parcours. Par exemple, si un événement déclenche un parcours à 12:01 pour un profil et qu’un autre arrive à 12:03, le parcours ne redémarre pas pour ce profil.

## Événements métier {#business-events}

Les événements **métier** ne sont pas liés à un profil spécifique. Par exemple, il peut s’agir d’une alerte aux informations, d’une mise à jour sportive, d’un changement ou d’une annulation de vol, d’une mise à jour des stocks, d’événements météorologiques, etc. Bien que ces événements ne soient pas spécifiques à un profil, ils peuvent intéresser un certain nombre de profils : les individus abonnés à des sujets d&#39;actualité spécifiques, les passagers d&#39;un vol, les acheteurs intéressés par un produit en rupture de stock, etc. Les événements métier sont toujours basés sur des règles. Lorsque vous déposez un événement métier dans un parcours, cela ajoute automatiquement une activité **Lecture d’audience** juste après. [Découvrez comment créer un événement métier](../event/about-creating-business.md).

**Exigence de schéma :** schéma XDM de série temporelle avec une identité principale non-personne et les champs `_id` et `timestamp` renseignés. Planifiez un délai d’exportation d’audience de 15 minutes à jusqu’à une heure.

**Exemple :** Une compagnie aérienne annule un vol. Un événement métier se déclenche, [!DNL Journey Optimizer] lit l’audience des passagers concernés et envoie à chacun une notification de reréservation.

## Événements de qualification d’audience {#audience-qualification-events}

Un événement **qualification de l’audience** est déclenché lorsqu’un profil entre ou quitte une audience. Par exemple, un client qui dépasse un seuil de dépenses de fidélité entre dans l’audience de niveau Gold ; cette qualification déclenche le parcours de ce profil en temps réel (pour les audiences de streaming) ou lors de l’évaluation du lot suivant. Contrairement aux événements unitaires, la qualification d’audience vous permet de créer une logique de déclenchement complexe en utilisant toute la puissance des définitions d’audience, sans avoir à apporter de modifications à l’implémentation pour envoyer un nouvel événement. En savoir plus sur les [événements de qualification d’audience](../building-journeys/audience-qualification-events.md).

**Schéma requis :** aucun schéma supplémentaire requis — l’événement repose sur des définitions d’audience existantes déjà intégrées dans Adobe Experience Platform.

**Exemple :** les dépenses de fidélité d’un client dépassent le seuil du niveau Gold. Leur profil est qualifié pour l’audience Gold, le parcours se déclenche automatiquement et envoie une récompense de bienvenue.

>[!NOTE]
>
>Les événements de qualification d’audience ne sont pas configurés dans **Administration > Événements** — ils sont sélectionnés directement sur la zone de travail de parcours comme première étape d’un parcours.

## Types d’événements en un coup d’œil {#event-comparison}

| | Événement unitaire | Événement métier | Événement de qualification d’audience |
| --- | --- | --- | --- |
| **Lié à un profil ?** | Oui — déclenché par l&#39;action d&#39;une personne spécifique. | Non : déclenché par une occurrence externe qui n’est pas liée à une personne. | Oui : déclenché lorsqu’un profil entre ou sort d’une audience. |
| **Comportement d’entrée** | Un profil entre sur le parcours en temps réel. | Plusieurs profils rejoignent l’audience par le biais d’une étape Lecture d’audience automatique. | Un profil entre lorsque l’appartenance à l’audience change. |
| **Cas d’utilisation standard** | Récupération de l’abandon de panier, envoi de formulaire, connexion à l’application, jalon de fidélité. | Annulation du vol, alerte de réapprovisionnement des stocks, nouvelles de dernière minute, événement météorologique. | Réengagement des clients obsolètes, modifications du niveau de fidélité, flux d’intégration VIP. |
| **Comment commence le parcours** | Entrée basée sur un événement : aucune audience nécessaire. | Événement métier + lecture d’audience automatique (ajoutée par Journey Optimizer). | Le profil entre ou sort d’une audience définie. |
| **Plusieurs par parcours ?** | Oui — vous pouvez écouter plusieurs événements unitaires à travers des étapes parcours. | Non : un seul événement métier par parcours, placé au début. | Oui — peut être combiné avec d&#39;autres activités. |
| **Type d’identifiant d’événement** | Basé sur des règles ou généré par le système. | Toujours basé sur des règles. | Aucun identifiant d’événement — basé sur l’évaluation de l’appartenance à l’audience. |
| **Configuré dans Administration ?** | Oui | Oui | Non : sélectionné directement sur la zone de travail du parcours. |

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
>Seuls les événements diffusés en continu peuvent déclencher des parcours. L’élément **ne peut pas** suivant peut être utilisé pour déclencher un parcours :
>
>* Événements ingérés par lot
>* Événements insérés via **Query Service**
>* Événements des jeux de données de [!DNL Journey Optimizer] internes (commentaires des messages, suivi des e-mails, etc.)
>
>Si vous ne pouvez pas obtenir d’événements diffusés en continu, créez une audience basée sur ces événements et utilisez à la place une activité **Lecture d’audience**. Pour utiliser les événements uniquement pour la segmentation, activez le jeu de données pour **Profil client en temps réel**.

## Comment choisir {#choose-event-type}

Utilisez les critères suivants pour sélectionner le type d’événement approprié à votre parcours. La question essentielle est la suivante : **déclenchez-vous une action pour une personne spécifique ou diffusez-vous des événements vers plusieurs profils ?** [En savoir plus sur les types de parcours &#x200B;](../building-journeys/journey.md#journey-types).

Chaque type d’événement est mappé à un modèle de parcours spécifique :

| Type d’événement | modèle de parcours |
| --- | --- |
| Événement unitaire | Parcours en temps réel à profil unique : se déclenche immédiatement lorsqu’une personne agit |
| Événement métier | Parcours de diffusion : cible de nombreux profils par le biais d’une étape Lecture d’audience automatique |
| Événement de qualification d’audience | Parcours déclenché par un segment : se déclenche lorsqu’un profil entre ou sort d’une audience |

* **Choisissez un événement unitaire** lorsque le déclencheur est lié à une personne spécifique (par exemple, un achat, un envoi de formulaire ou un jalon de fidélité). Les événements unitaires nécessitent une identité principale basée sur une personne dans le schéma et lancent immédiatement le parcours pour ce profil. [Découvrez comment configurer un événement unitaire](../event/about-creating.md).

* **Choisissez un événement métier** lorsque le déclencheur est un événement global (par exemple, un réapprovisionnement de produit, une baisse de prix ou une annulation de vol) et que vous souhaitez diffuser vers un ensemble de profils liés à ce signal. Les événements métier doivent être la première étape du parcours et cibler automatiquement les profils par le biais d&#39;une activité **Lecture d&#39;audience**. Ils nécessitent un schéma de série temporelle avec une identité principale autre que des personnes et les champs `_id` et `timestamp`. Planifiez un délai d’exportation d’audience de 15 minutes à jusqu’à une heure. [Découvrez comment configurer un événement métier](../event/about-creating-business.md).

* **Choisissez un événement de qualification d’audience** lorsque le déclencheur est un profil qui entre ou sort d’une audience et que vous avez besoin d’une logique de segmentation plus complexe que celle qu’un seul événement peut fournir (par exemple, réengager des clients obsolètes qui viennent d’atteindre un seuil de dépenses ou déclencher un flux de délocalisation lorsqu’un membre de VIP abandonne le niveau de fidélité). [En savoir plus sur les événements de qualification d’audience](../building-journeys/audience-qualification-events.md).

>[!CAUTION]
>
>Les événements métier ne peuvent pas être utilisés dans le même parcours que les événements unitaires ou les activités de qualification d’audience.

## Contraintes clés {#key-constraints}

Utilisez ce résumé pour planifier votre implémentation avant de configurer des événements.

| Contrainte | Détails |
| --- | --- |
| Limite de débit | 5 000 événements par seconde par organisation, dans tous les sandbox (parcours unitaires et Lecture d’audience) |
| Bloc de rentrée | Reprise du profil bloquée pendant 5 minutes après le déclenchement d’un parcours unitaire |
| Événements métier par parcours | Maximum 1, doit être la première étape |
| Combiner entreprise et unité dans un seul parcours | Non pris en charge |
| Evénements batch | Impossible de déclencher les parcours : utilisez plutôt une activité **Lecture d’audience**. |
| Qualification de l’audience — Administration | Non configuré dans **Administration > Événements** — sélectionné directement sur la zone de travail du parcours |
| Modification d’un événement en direct | Modification du nom, de la description ou ajout de champs de payload uniquement |

## Comment les événements atteignent Journey Optimizer {#data-cycle}

Les événements doivent être envoyés à [!DNL Journey Optimizer] en tant qu’appels POST via les [API d’ingestion de diffusion Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/xdm/api/getting-started.html?lang=fr){target="_blank"}. La payload doit respecter la mise en forme XDM et le schéma d’événement doit avoir l’option **Real-Time Customer Profile** activée.

Les modes de streaming authentifié et non authentifié sont pris en charge. Les événements ingérés par lots et les événements provenant de jeux de données de [!DNL Journey Optimizer] interne (commentaires de messages, suivi des e-mails, etc.) ne peuvent pas être utilisés pour déclencher des parcours. Utilisez une activité **Lecture d’audience** à la place pour ces cas d’utilisation.


## Limites de débit des événements {#event-throughput}

Adobe Journey Optimizer applique des limites de débit distinctes par type d’événement, au niveau de l’organisation et sur tous les sandbox :

* **Événements unitaires** : 5 000 événements par seconde
* **Lecture d’événements de parcours basés sur l’audience** : 5 000 événements par seconde

Ces limites s’appliquent à tous les événements utilisés dans les parcours actifs, notamment les parcours **En ligne**, **Exécution d’essai**, **Fermé** et **En pause**. Lorsqu’une limite est atteinte, les nouveaux événements sont mis en file d’attente et traités à 5 000 par seconde jusqu’à ce que la file d’attente soit vidée.

Pour plus d’informations sur les taux de traitement des parcours et sur l’impact des différents types de parcours sur le débit, [en savoir plus sur les taux de traitement des parcours &#x200B;](../building-journeys/entry-management.md#journey-processing-rate).

Les types d&#39;événements suivants sont comptabilisés dans ces quotas :

* **Événements unitaires externes** : inclut les événements basés sur des règles et ceux générés par le système. Si un même événement brut est admissible pour plusieurs définitions de règle, chaque règle correspondante est comptabilisée comme un événement distinct dans le quota.

* **Événements de qualification d’audience** : si la même audience en streaming est utilisée dans plusieurs parcours, chaque utilisation est comptabilisée séparément. Par exemple, l’emploi d’une même audience dans une activité de qualification d’audience dans deux parcours génère deux événements comptabilisés.

* **Événements de réaction** : événements déclenchés par des réactions de profil (ouverture d’e-mail, clic sur l’e-mail, etc.) dans un parcours.

* **Événements métiers** : événements non liés à un profil spécifique, mais à un événement lié à l’activité professionnelle.

* **Événements Analytics** : si l’[intégration à Adobe Analytics a été activée en vue de déclencher des parcours](about-analytics.md), ces événements sont également inclus.

* **Événements de reprise** : événement technique déclenché lorsqu’un profil reprend à partir d’un parcours en pause. En savoir plus sur la [reprise des parcours mis en pause](../building-journeys/journey-pause.md#journey-resume-steps).

* **Événements d’achèvement de nœud d’attente** : lorsqu’un profil quitte un nœud d’attente, un événement technique est généré pour reprendre le parcours.

>[!NOTE]
>
>À l’exception des événements d’attente et de reprise, tous les autres types d’événements sont également comptabilisés dans le quota lorsqu’ils sont utilisés dans des parcours basés sur des audiences lues.

## Mise à jour et suppression d’un événement {#update-event}


Pour éviter d’interrompre les parcours existants, lorsque vous modifiez un événement utilisé dans un parcours **brouillon**, **actif** ou **fermé**, vous pouvez uniquement en modifier le nom ou la description, ou ajouter des champs de payload.

Les événements utilisés dans des parcours **actifs**, **brouillons** ou **fermés** ne peuvent pas être supprimés. Pour supprimer un événement utilisé, vous devez arrêter les parcours qui l’utilisent et/ou le supprimer des brouillons de parcours où il est utilisé. Vous pouvez cocher le champ **[!UICONTROL Utilisé dans]**. Il affiche le nombre de parcours qui utilisent cet événement particulier. Vous pouvez cliquer sur le bouton **[!UICONTROL Afficher les parcours]** pour faire apparaître la liste des parcours correspondants.

## Questions fréquentes {#faq}

**Puis-je utiliser le même événement dans plusieurs parcours ?**
Oui : plusieurs parcours peuvent écouter simultanément le même événement.

**Puis-je associer un événement métier et un événement unitaire dans le même parcours ?**
Non - les événements métier ne peuvent pas être utilisés dans le même parcours que les événements unitaires ou les activités de qualification d’audience.

**Dois-je configurer quoi que ce soit pour les événements de qualification d’audience ?**
Non — Les événements de qualification d’audience ne sont pas configurés dans **Administration > Événements**. Sélectionnez l’audience directement sur la zone de travail du parcours comme première étape.

**Puis-je utiliser des données ingérées par lots pour déclencher un parcours ?**
Non — seuls les événements diffusés en continu peuvent déclencher des parcours. Pour les données par lot, créez une audience et utilisez plutôt une activité **Lecture d’audience**.

**Mon parcours ne se déclenche pas. Que dois-je vérifier ?**

* Vérifiez que le **profil client en temps réel** est activé pour votre schéma d’événement.
* Confirmer que les événements sont diffusés en continu : les événements ingérés par lots ne peuvent pas déclencher de parcours.
* Pour les événements basés sur des règles, vérifiez que la condition de règle correspond aux champs de payload entrants.
* Vérifiez que le parcours a le statut **Actif** et que le profil remplit toutes les conditions d’entrée.

## Étapes suivantes {#next-steps}

* [Configurer un événement unitaire](../event/about-creating.md)
* [Configuration d’un événement métier](../event/about-creating-business.md)
* [En savoir plus sur les événements de qualification d’audience](../building-journeys/audience-qualification-events.md)
* [Gérer l’entrée et la reprise du parcours](../building-journeys/entry-management.md)

>[!TIP]
>
>Si votre parcours ne se déclenche pas, vérifiez que le **profil client en temps réel** est activé pour votre schéma d’événement et que les événements sont diffusés en continu. Les événements ingérés par lots ne peuvent pas déclencher de parcours.

## Vidéos pratiques {#video}

Découvrez comment configurer un événement, spécifier le point dʼentrée du flux en continu et la payload dʼun événement.

>[!VIDEO](https://video.tv.adobe.com/v/336253?quality=12)

Comprendre les cas d’utilisation applicables pour les événements métier. Découvrez comment créer un parcours à l’aide d’un événement métier et les bonnes pratiques à appliquer.

>[!VIDEO](https://video.tv.adobe.com/v/334234?quality=12)
