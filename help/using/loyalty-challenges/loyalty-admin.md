---
solution: Journey Optimizer
product: journey optimizer
title: Configuration du programme de fidélité
description: Découvrez comment configurer les fournisseurs de récompenses, les définitions d’événement et les paramètres d’organisation pour votre programme de fidélité dans Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: Admin
level: Intermediate
hide: true
badge: label="Private Beta" type="Informative"
mini-toc-levels: 1
exl-id: f8a3b2c1-4d5e-6f7a-8b9c-0d1e2f3a4b5c
source-git-commit: aea783bd8f2351d4a5d8aa6b84c24a713a6c0306
workflow-type: tm+mt
source-wordcount: '1221'
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

La section **[!UICONTROL Administration du programme de fidélité]** vous permet de configurer la manière dont Journey Optimizer se connecte au serveur principal de votre programme de fidélité. Les marketeurs utilisent **[!UICONTROL Loyalty Challenges (Beta)]** pour concevoir des défis, des tâches, du contenu et des messages. Loyalty Admin est une configuration distincte et unique pour l&#39;exécution de récompenses et le mappage d&#39;événements.

Lorsqu’un client termine un défi (ou atteint un jalon de récompense), Journey Optimizer appelle le fournisseur de récompense que vous configurez ici pour lui envoyer des points ou d’autres récompenses. Les paramètres Défi **[!UICONTROL Contenu]**, **[!UICONTROL Messagerie]** et **[!UICONTROL Audience]** ne sont pas affectés par la configuration de l’administrateur de fidélité.

## Accéder à Loyalty Admin {#access-loyalty-admin}

Pour ouvrir Loyalty Admin, connectez-vous à Journey Optimizer et sélectionnez **[!UICONTROL Loyalty Admin]** dans le volet de navigation de gauche.

<!-- SCREENSHOT: Loyalty Admin entry in the left navigation -->

L’interface d’administration est organisée en onglets. Selon votre organisation, vous pouvez voir **[!UICONTROL Paramètres globaux]**, **[!UICONTROL Fournisseurs de récompenses]**, **[!UICONTROL Définitions d’événement]** et **[!UICONTROL Inventaire des produits]**.

## Paramètres globaux {#global-settings}

>[!CONTEXTUALHELP]
>id="ajo_loyalty_admin_global_settings"
>title="Paramètres globaux"
>abstract="Sélectionnez l’espace de noms d’identité Adobe Experience Platform de votre programme de fidélité et copiez votre identifiant de configuration. Ces paramètres au niveau de l’organisation sont requis pour que les fournisseurs de récompenses puissent gérer correctement les récompenses."

Utilisez **[!UICONTROL Paramètres globaux]** pour configurer les options à l’échelle de l’organisation pour les défis de fidélité.

1. Ouvrez l’onglet **[!UICONTROL Paramètres globaux]**.

1. Dans la liste déroulante **[!UICONTROL Espace de noms]**, sélectionnez l’[espace de noms d’identité](https://experienceleague.adobe.com/fr/docs/experience-platform/identity/features/namespaces) de Adobe Experience Platform utilisé par votre programme de fidélité. Sélectionnez **[!UICONTROL Enregistrer]** pour mettre à jour l’espace de noms sur la configuration des défis de fidélité de votre organisation.

1. Copiez l’**[!UICONTROL ID de configuration]** si vous devez le partager avec votre équipe d’implémentation ou des systèmes externes.

<!-- SCREENSHOT: Global settings tab showing namespace drop-down, Save, and Configuration ID -->

## Fournisseurs de récompenses {#reward-providers}

Un **fournisseur de récompense** indique à Journey Optimizer où envoyer des appels d’exécution lorsqu’une progression du défi est enregistrée ou qu’un défi est terminé ; par exemple, une API qui attribue des points de fidélité ou des étoiles à un compte de membre.

Un fournisseur de récompense comprend :

* Détails de connexion de base (nom, description, URL d’API, en-têtes)
* **[!UICONTROL Définitions de récompense]** — types de récompense que ce fournisseur peut émettre (par exemple, étoiles ou miles)
* **[!UICONTROL Récompenser les proxys]** (facultatif) : acheminez les appels via un proxy plutôt que directement vers votre point d’entrée
* **[!UICONTROL Générateurs de jetons d’authentification]** : méthode de Journey Optimizer pour obtenir des jetons d’accès avant d’appeler votre API

### Créer un fournisseur de récompense {#create-reward-provider}

Pour enregistrer un nouveau fournisseur de récompense et ses ressources associées, procédez comme suit.

1. Ouvrez l’onglet **[!UICONTROL Fournisseurs de récompenses]** et commencez à créer un fournisseur.

1. Saisissez un **[!UICONTROL Nom]** et un **[!UICONTROL Description]**, puis l’**[!UICONTROL URL de l’API]** où les demandes d’exécution sont envoyées.

1. Ajoutez des **[!UICONTROL en-têtes]** selon les besoins de votre API (par exemple, des clés API ou des types de contenu). Vous pouvez ajouter ou supprimer des lignes d’en-tête dans l’interface utilisateur.

1. Configurez les **[!UICONTROL définitions de récompense]** :

   * Définissez chaque type de récompense pris en charge par votre fournisseur (par exemple, points de programme ou étoiles).
   * Vous pouvez éventuellement marquer une définition comme **par défaut** pour ce fournisseur.
   * Spécifiez la **payload** envoyée avec des appels d’exécution pour chaque définition.

1. Vous pouvez éventuellement configurer un **[!UICONTROL proxy Reward]** :

   * **[!UICONTROL Hôte]**, **[!UICONTROL Port]** et informations d’identification
   * **[!UICONTROL Nom]**, **[!UICONTROL Description]** et si le proxy est **activé**

1. Configurez un **[!UICONTROL générateur de jetons d’authentification]** si votre API requiert un jeton avant chaque appel :

   * URL du point d’entrée de jeton et méthode HTTP (par exemple, **POST** pour les flux de style OAuth)
   * **[!UICONTROL Clé du jeton]** dans la réponse (par exemple, `access_token`)
   * En-têtes requis par le point d’entrée du jeton

   Journey Optimizer demande un jeton à partir de cette configuration avant d’appeler votre API de récompense afin que les appels utilisent des informations d’identification actuelles.

1. Sélectionnez **[!UICONTROL Créer un fournisseur de récompense]**. Le fournisseur et ses ressources enfants (définitions, proxy et générateur de jetons) sont créés ensemble.

<!-- SCREENSHOT: Reward provider creation form with definitions, proxy, and auth token sections -->

Après sa création, le fournisseur apparaît dans la liste des fournisseurs de récompense. Les marketeurs sélectionnent ce fournisseur lors de la [configuration des récompenses du défi](create-challenges.md#rewards).

### Modifier un fournisseur de récompense {#edit-reward-provider}

1. Ouvrez l’onglet **[!UICONTROL Fournisseurs de récompenses]** et sélectionnez un fournisseur.

1. Mettez à jour le nom, la description, l’URL ou les en-têtes du fournisseur selon les besoins.

1. Pour modifier les **[!UICONTROL définitions de récompense]**, **[!UICONTROL proxys de récompense]** ou **[!UICONTROL générateurs de jetons d’authentification]**, ouvrez la section correspondante et modifiez les champs. Les modifications apportées à ces ressources enfants sont enregistrées lorsque vous les mettez à jour sur place.

<!-- SCREENSHOT: Reward provider detail view with child resource sections -->

>[!NOTE]
>
>Pour **[!UICONTROL Apportez vos propres données]** les défis pour lesquels les tâches et les récompenses proviennent entièrement de votre intégration de données, les fournisseurs de récompense configurés ici peuvent ne pas s’appliquer. [En savoir plus sur les défis liés aux données à relever](create-challenges.md#create-the-challenge).

## Définitions des événements {#event-definitions}

**[!UICONTROL Définitions des événements]** mappez les événements d’expérience entrants au format de votre marque aux activités que les défis de fidélité peuvent utiliser, en particulier les tâches **[!UICONTROL Événement personnalisé]**. Lorsque des données arrivent de vos canaux, Journey Optimizer utilise ces définitions pour décider si un événement est pertinent et comment l’interpréter. Les événements qui ne correspondent à aucune définition sont ignorés.

### Création d’une définition d’événement {#create-event-definition}

1. Ouvrez l’onglet **[!UICONTROL Définitions d’événement]** et créez une définition.

1. Saisissez un **[!UICONTROL Nom]** pour l’événement (par exemple, `Coffee purchase`). Ce nom est celui que les spécialistes marketing sélectionnent lorsqu’ils configurent une tâche **[!UICONTROL Événement personnalisé]**.

1. Indiquez comment identifier l’événement dans les payloads entrantes :

   * **[!UICONTROL Chemin d’accès de l’identifiant]** — Chemin JSON vers le champ qui identifie l’événement ou le membre (par exemple, `data.memberId`)
   * **[!UICONTROL Valeurs d&#39;identifiant]** — valeurs qui doivent être présentes pour que cette définition corresponde

1. Vous pouvez éventuellement spécifier un **[!UICONTROL ID de schéma XDM]** et/ou utiliser les champs **[!UICONTROL Schéma]** et **[!UICONTROL Transformateur]** pour coller les chaînes de schéma et de transformation utilisées par votre équipe pour analyser et valider le fichier JSON entrant avant traitement.

   Vous pouvez fournir un identifiant de schéma XDM, un chemin d’accès à l’identifiant, ou les deux, selon la structure de vos événements.

1. Enregistrez la définition de l’événement.

<!-- SCREENSHOT: Event definition form with identifier path, values, and schema fields -->

La plupart des entreprises créent plusieurs définitions d’événement, une par activité dont elles souhaitent effectuer le suivi (par exemple, achat, enregistrement ou visite du site). [Découvrez comment utiliser les tâches d’événement personnalisé dans les défis](create-tasks.md#choose-activity).

## Inventaire des produits {#product-inventory}

L’onglet **[!UICONTROL Inventaire des produits]** vous permet de télécharger un fichier CSV pour mapper les identifiants de produits ou d’articles (par exemple, les identifiants MPG) aux groupes de produits utilisés dans l’éligibilité de la tâche. Cela prend en charge les scénarios où les tâches font référence à des produits groupés plutôt qu’à des SKU individuels saisis manuellement.

1. Ouvrez l’onglet **[!UICONTROL Inventaire des produits]**.

1. Chargez votre fichier de mappage en le faisant glisser dans la zone de chargement ou en accédant à pour le sélectionner.

1. Passez en revue les mappages importés dans la liste d&#39;inventaire. Sélectionnez un groupe de produits pour afficher tous les éléments de ce groupe. Utilisez la fonction de recherche pour rechercher des éléments par nom ou ID.

1. Utilisez **[!UICONTROL Historique de chargement]** pour afficher les chargements précédents.

<!-- SCREENSHOT: Product inventory list after CSV upload -->

>[!NOTE]
>
>**[!UICONTROL Exclusions globales]** pour l’inventaire des produits est prévu pour une version ultérieure et n’est pas documenté ici.

## Relation entre l’administrateur de fidélité et les défis {#how-admin-relates-to-challenges}

| Zone | Configuré dans Loyalty Admin | Configuré dans les défis de fidélité |
|------|----------------------------|----------------------------------|
| API d’exécution de récompense | Oui — fournisseurs de récompenses | Non — sélectionner le fournisseur et les montants uniquement |
| Mappage des événements pour les activités personnalisées | Oui — Définitions d&#39;événement | Non — sélectionner le nom de l&#39;événement dans les tâches d&#39;événement personnalisées |
| Mappages de groupes de produits | Oui — inventaire des produits | Non — utiliser des groupes lors de la création de tâches Achat/Dépenses |
| Structure du défi, contenu, audience | Non | Oui |

Ordre de configuration standard :

1. Configurez **[!UICONTROL paramètres globaux]** et au moins un **[!UICONTROL fournisseur de récompense]** dans Loyalty Admin.
1. Vous pouvez éventuellement ajouter **[!UICONTROL Définitions d’événement]** et **[!UICONTROL Inventaire de produits]** si votre programme utilise des événements personnalisés ou des groupes de produits basés sur CSV.
1. Créez [tâches](create-tasks.md) et [défis](create-challenges.md) dans **[!UICONTROL Défis de fidélité (Beta)]** en sélectionnant le fournisseur de récompense et les définitions que vous avez configurés.

Adobe Journey Optimizer envoie des appels d’exécution à votre fournisseur lorsque les clients gagnent des récompenses ; votre plateforme de fidélité gère le crédit du compte du membre.

## Conditions préalables {#prerequisites}

Loyalty Admin est destiné à un petit groupe d’administrateurs dans votre organisation. Outre les autorisations requises pour les [Défis de fidélité](get-started.md#prerequisites), vous devez avoir accès à la configuration des paramètres de fidélité au niveau de l’organisation.

Contactez votre administrateur si **[!UICONTROL Loyalty Admin]** n’apparaît pas dans le volet de navigation de gauche ou si vous ne pouvez pas enregistrer les paramètres globaux ou les fournisseurs de récompenses.
