---
solution: Journey Optimizer
product: journey optimizer
title: Configuration du programme de fidélité
description: Découvrez comment configurer des fournisseurs de récompenses, des définitions d’événement et des paramètres au niveau de l’organisation pour votre programme de fidélité dans Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Private Beta" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: a4ad533e54f3692eb0483138a8cfd1cee0e77ba1
workflow-type: tm+mt
source-wordcount: '1128'
ht-degree: 2%

---

# Configuration du programme de fidélité {#loyalty-admin}

>[!BEGINSHADEBOX]

**Documentation sur les défis de fidélité :**

* [Prise en main des défis de fidélité](get-started.md)
* [Accéder aux défis et aux tâches et les gérer](access-loyalty-challenges.md)
* [Créer des défis](create-challenges.md)
* [Création de tâches](create-tasks.md)
* [Surveillance des performances des défis de fidélité](loyalty-reporting.md)
* **Configurer le programme de fidélité** ◀︎ **Vous êtes ici**
* [Référence de l’API pour les défis de fidélité](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version bêta **privée**. Pour plus d’informations sur le cycle de publication et les phases de disponibilité, consultez le [cycle de publication de Journey Optimizer](../rn/releases.md).

La section **[!UICONTROL Loyalty Admin]** vous permet de configurer la manière dont Journey Optimizer se connecte à vos systèmes de fidélité externes. Les marketeurs utilisent **[!UICONTROL Loyalty Challenges (Beta)]** pour concevoir des défis, des tâches, du contenu et des messages. **[!UICONTROL Administration du programme de fidélité]** est une zone distincte réservée aux administrateurs pour l’exécution des récompenses, le mappage des événements et l’inventaire des produits.

Lorsqu’un client termine un défi ou atteint un jalon de récompense, Journey Optimizer appelle le fournisseur de récompense que vous avez configuré pour lui offrir des points ou d’autres récompenses. La configuration dans **[!UICONTROL Loyalty Admin]** n’affecte pas les paramètres de défi **[!UICONTROL Contenu]**, **[!UICONTROL Messagerie]** ou **[!UICONTROL Audience]**, qui restent sous le contrôle du marketeur.

## Ce que vous configurez ici par rapport à dans Loyalty Challenges {#scope}

| Zone | Configuré dans Loyalty Admin | Configuré dans les défis de fidélité |
|------|----------------------------|----------------------------------|
| API d’exécution de récompense | Oui — fournisseurs de récompenses | Non — sélectionner le fournisseur et les montants uniquement |
| Mappage des événements pour les activités personnalisées | Oui — Définitions d&#39;événement | Non — sélectionner le nom de l&#39;événement dans les tâches d&#39;événement personnalisées |
| Mappages de groupes de produits | Oui — inventaire des produits | Non — utiliser des groupes lors de la création de tâches Achat/Dépenses |
| Structure du défi, contenu, audience | Non | Oui |

Adobe Journey Optimizer envoie des appels d’exécution à votre fournisseur de récompense lorsque les clients gagnent des récompenses. Votre plateforme de fidélité est responsable du crédit du compte du membre.

## Conditions préalables {#prerequisites}

**[!UICONTROL Loyalty Admin]** est destiné à un petit nombre d’administrateurs par organisation. Outre les autorisations requises pour les [Défis de fidélité](get-started.md#prerequisites), vous avez besoin d’un accès de niveau administrateur à votre instance Journey Optimizer. Contactez votre administrateur Adobe pour demander l’accès.

## Accéder à Loyalty Admin {#access-loyalty-admin}

Pour ouvrir **[!UICONTROL Loyalty Admin]**, sélectionnez-le dans le volet de navigation de gauche de Journey Optimizer.

<!-- SCREENSHOT: Loyalty Admin entry in the left navigation -->

**[!UICONTROL Loyalty Admin]** est organisé en onglets : **[!UICONTROL Paramètres globaux]**, **[!UICONTROL Fournisseurs de récompenses]**, **[!UICONTROL Définitions d’événement]** et **[!UICONTROL Inventaire des produits]**. Les onglets disponibles dépendent des autorisations et de la configuration des fonctionnalités de votre entreprise.

## Paramètres globaux {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="Paramètres globaux"
>abstract="Sélectionnez l’espace de noms d’identité Adobe Experience Platform de votre programme de fidélité et copiez votre identifiant de configuration. Ces paramètres au niveau de l’organisation sont requis pour que les fournisseurs de récompenses puissent gérer correctement les récompenses."

Utilisez **[!UICONTROL Paramètres globaux]** pour configurer des options à l’échelle de l’organisation pour les défis de fidélité.

1. Ouvrez l’onglet **[!UICONTROL Paramètres globaux]**.

1. Dans la liste déroulante **[!UICONTROL Espace de noms]**, sélectionnez l’[espace de noms d’identité](https://experienceleague.adobe.com/fr/docs/experience-platform/identity/features/namespaces) utilisé par votre programme de fidélité.

1. Sélectionnez **[!UICONTROL Enregistrer]** pour appliquer l’espace de noms à votre configuration des défis de fidélité.

1. Copiez l’**[!UICONTROL ID de configuration]** lorsque vous devez le partager avec votre équipe d’implémentation ou des systèmes externes, par exemple lors de la configuration de la diffusion d’événements entrants.

<!-- SCREENSHOT: Global settings tab showing namespace drop-down, Save, and Configuration ID -->

## Fournisseurs de récompenses {#reward-providers}

Un **fournisseur de récompense** indique à Journey Optimizer où envoyer des appels d’exécution lorsqu’une progression du défi est enregistrée ou qu’un défi est terminé ; par exemple, une API qui attribue des points de fidélité ou des étoiles à un compte de membre.

Une configuration de fournisseur de récompense comprend :

* Détails de connexion de base (nom, description, URL d’API, en-têtes)
* **[!UICONTROL Définitions de récompense]** — types de récompense que ce fournisseur peut émettre (par exemple, étoiles ou miles)
* **[!UICONTROL Proxy de récompense]** (facultatif) : proxy intermédiaire par lequel les appels sont acheminés au lieu de votre point d’entrée directement
* **[!UICONTROL Générateurs de jetons d’authentification]** : mécanisme utilisé par Journey Optimizer pour obtenir des jetons d’accès avant d’appeler votre API

### Créer un fournisseur de récompense {#create-reward-provider}

1. Ouvrez l’onglet **[!UICONTROL Fournisseurs de récompenses]** et sélectionnez **[!UICONTROL Créer un fournisseur de récompense]**.

1. Saisissez un **[!UICONTROL Nom]**, **[!UICONTROL Description]** et l’**[!UICONTROL URL de l’API]** qui reçoit les demandes d’exécution.

1. Ajoutez des **[!UICONTROL en-têtes]** selon les besoins de votre API (par exemple, des clés API ou des types de contenu).

1. Configurez **[!UICONTROL Définitions de récompense]** — une entrée par type de récompense pris en charge par votre fournisseur (par exemple, points de programme ou étoiles). Pour chaque définition :

   * Spécifiez la **payload** envoyée avec des appels d’exécution.
   * Vous pouvez éventuellement marquer une définition comme **par défaut** pour ce fournisseur.

1. Vous pouvez éventuellement configurer un **[!UICONTROL proxy Reward]** pour acheminer les appels d’exécution via un serveur intermédiaire :

   * **[!UICONTROL Nom]**, **[!UICONTROL Description]** et si le proxy est **activé**
   * **[!UICONTROL Hôte]**, **[!UICONTROL Port]** et informations d’identification

1. Configurez un **[!UICONTROL générateur de jetons d’authentification]** si votre API requiert un jeton porteur pour l’authentification :

   * URL du point d’entrée de jeton et méthode HTTP (par exemple, **POST** pour les flux de style OAuth)
   * **[!UICONTROL Clé du jeton]** dans la réponse (par exemple, `access_token`)
   * En-têtes requis par le point d’entrée du jeton

   Journey Optimizer utilise cette configuration pour obtenir un nouveau jeton avant d’appeler votre API de récompense.

1. Sélectionnez **[!UICONTROL Créer un fournisseur de récompense]**. Le fournisseur et toutes les ressources enfants configurées sont enregistrés ensemble.

<!-- SCREENSHOT: Reward provider creation form with definitions, proxy, and auth token sections -->

Après l’enregistrement, le fournisseur apparaît dans la liste des fournisseurs de récompenses. Les marketeurs sélectionnent ce fournisseur lors de la [configuration des récompenses du défi](create-challenges.md#rewards).

Pour modifier un fournisseur de récompense existant, ouvrez l’onglet **[!UICONTROL Fournisseurs de récompense]**, sélectionnez le fournisseur et mettez à jour les champs en place. Les modifications apportées aux ressources enfants (définitions de récompense, proxys, générateurs de jetons d’authentification) sont enregistrées lorsque vous les mettez à jour.

<!-- SCREENSHOT: Reward provider detail view with child resource sections -->

>[!NOTE]
>
>**[!UICONTROL Apportez vos propres données]** les défis génèrent des récompenses grâce à votre propre intégration de données. Les fournisseurs de récompenses configurés ici ne s’appliquent pas à ces défis. [En savoir plus sur les défis liés aux données à relever](create-challenges.md#create-the-challenge).

## Définitions d’événement (facultatif) {#event-definitions}

**[!UICONTROL Définitions des événements]** mappez les événements d’expérience de vos systèmes (quel que soit le format JSON ou XDM utilisé par votre marque) aux activités sur lesquelles les défis de fidélité peuvent agir, notamment les tâches **[!UICONTROL Événement personnalisé]**. Lorsque des événements arrivent, Journey Optimizer utilise ces définitions pour décider de les traiter ou non. Les événements qui ne correspondent à aucune définition sont ignorés.

### Création d’une définition d’événement {#create-event-definition}

1. Ouvrez l’onglet **[!UICONTROL Définitions d’événement]** et créez une définition.

1. Saisissez un **[!UICONTROL Nom]** pour l’événement (par exemple, `Coffee purchase`) — il s’agit du nom que les spécialistes marketing voient lors de la configuration d’une tâche **[!UICONTROL Événement personnalisé]**.

1. Indiquez comment identifier l’événement dans les payloads entrantes :

   * **[!UICONTROL Chemin d’accès de l’identifiant]** — Chemin JSON vers le champ qui identifie l’événement ou le membre (par exemple, `data.memberId`)
   * **[!UICONTROL Valeurs d&#39;identifiant]** — valeurs qui doivent être présentes pour que cette définition corresponde

1. Vous pouvez éventuellement spécifier un **[!UICONTROL identifiant de schéma XDM]** si les payloads de l’événement sont conformes à un schéma Experience Platform.

1. Utilisez éventuellement les champs **[!UICONTROL Schéma]** et **[!UICONTROL Transformateur]** pour fournir un schéma personnalisé et des chaînes de transformation pour analyser et valider le fichier JSON entrant.

   Vous pouvez fournir un identifiant de schéma XDM, un chemin d’accès à l’identifiant, ou les deux, selon la structure de vos événements.

1. Enregistrez la définition de l’événement.

<!-- SCREENSHOT: Event definition form with identifier path, values, and schema fields -->

La plupart des entreprises créent plusieurs définitions d’événement, une par activité dont elles souhaitent effectuer le suivi (par exemple, achat, enregistrement ou visite du site). [Découvrez comment utiliser les tâches d’événement personnalisé dans les défis](create-tasks.md#choose-activity).

## Inventaire des produits (facultatif) {#product-inventory}

Utilisez l’onglet **[!UICONTROL Inventaire des produits]** pour charger un fichier CSV qui mappe les identifiants de produits ou d’articles (par exemple, les identifiants MPG) à des groupes de produits. Les marketeurs peuvent ensuite référencer ces groupes dans les règles d’éligibilité de tâche au lieu de saisir des SKU individuels.

1. Ouvrez l’onglet **[!UICONTROL Inventaire des produits]**.

1. Chargez votre fichier de mappage.

1. Passez en revue les mappages importés dans la liste d&#39;inventaire. Sélectionnez un groupe de produits pour afficher tous les éléments de ce groupe ou utilisez la fonction de recherche pour rechercher des éléments par nom ou ID.

1. Utilisez **[!UICONTROL Historique de chargement]** pour afficher les chargements précédents.

<!-- SCREENSHOT: Product inventory list after CSV upload -->

>[!NOTE]
>
>**[!UICONTROL Exclusions globales]** pour l’inventaire des produits est prévu pour une version ultérieure et n’est pas documenté ici.
