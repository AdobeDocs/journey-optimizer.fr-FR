---
solution: Journey Optimizer
product: journey optimizer
title: Données et jeux de données de fidélité
description: Découvrez les données de profil Adobe Experience Platform et les jeux de données requis par les défis de fidélité, ainsi que l’impact de la durée de vie (TTL) des jeux de données sur la rétention.
feature: Journeys
topic: Content Management
role: Admin, Developer
level: Intermediate
hide: true
badge: label="Private Beta" type="Informative"
mini-toc-levels: 1
exl-id: a7c4e1b2-8f3d-4a6c-9e0b-1d2e3f4a5b6c
feature_v2: []
subfeature_v2: []
source-git-commit: 2e01cd1880b8527911376d94188d0204f7649541
workflow-type: tm+mt
source-wordcount: 538
ht-degree: 5%

---

# Données et jeux de données de fidélité {#loyalty-data-and-datasets}

>[!BEGINSHADEBOX]

**Table des matières**

[Prise en main des défis de fidélité](get-started.md)

<table style="table-layout:fixed">
<tr style="border: 0;">
<td style="vertical-align:top;">

**Créer et gérer des défis**

* [Accéder aux défis et aux tâches et les gérer](access-loyalty-challenges.md)
* [Créer des défis](create-challenges.md)
* [Création de tâches](create-tasks.md)
* [Surveillance des performances des défis de fidélité](loyalty-reporting.md)

</td>
<td style="vertical-align:top;">

**Configuration et intégration**

* [Configuration des défis de fidélité](loyalty-admin.md)
* **Données et jeux de données de fidélité** ◀︎ **Vous êtes ici**
* [Référence de l’API pour les défis de fidélité](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}

</td>
</tr>
</table>

>[!ENDSHADEBOX]

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version bêta **privée**. Pour plus d’informations sur le cycle de publication et les phases de disponibilité, consultez le [cycle de publication de Journey Optimizer](../rn/releases.md).

## Vue d’ensemble {#overview}

Les défis de fidélité reposent sur Adobe Experience Platform pour l’identité, les attributs de profil, les événements d’expérience et les audiences. Utilisez cette page pour savoir quelles données préparer, quels jeux de données sont impliqués et comment la **durée de vie (TTL)** affecte la rétention avant que vous ne créiez des défis ou n’utilisiez les API de défis de fidélité.

Contactez votre administrateur Adobe pour la configuration du programme Journey Optimizer ou configurez l’exécution des récompenses et le mappage des événements dans le menu **[!UICONTROL Administrateur de fidélité]**. [Découvrez comment configurer les défis de fidélité](loyalty-admin.md). Pour les points d’entrée REST et l’authentification, consultez la [référence de l’API Loyalty Challenges](https://developer.adobe.com/journey-optimizer-apis/references/loyalty-challenges){target="_blank"}.

## Données Adobe Experience Platform {#aep-data}

### Attributs de profil {#profile-attributes}

Mettez les audiences, la personnalisation et les profils d’utilisation de rapports au défi dans la classe **[!DNL XDM Individual Profile]**. Alignez l’identité [espace de noms](https://experienceleague.adobe.com/fr/docs/experience-platform/identity/features/namespaces){target="_blank"} que vous utilisez pour les défis de fidélité sur la manière dont les membres sont identifiés dans vos données de profil et sur l’espace de noms sélectionné dans **[!UICONTROL paramètres globaux]** dans le menu **[!UICONTROL Administration du programme de fidélité]**.

Pour les attributs de fidélité standard sur le profil (points, niveau, programme, statut et champs associés), utilisez le groupe de champs de schéma Experience Platform **[Détails de fidélité](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/profile/loyalty-details){target="_blank"}**. Ce groupe de champs définit l’objet `loyalty` et ses propriétés (par exemple `points`, `tier`, `program` et `status`).

➡️ [Groupe de champs de schéma Détails de fidélité](https://experienceleague.adobe.com/en/docs/experience-platform/xdm/field-groups/profile/loyalty-details){target="_blank"}

### Événements d’expérience {#experience-events}

Les tâches **[!UICONTROL Achat]**, **[!UICONTROL Dépenses]** et **[!UICONTROL Événement personnalisé]** dépendent des événements d’expérience ingérés dans Adobe Experience Platform. Pour les tâches **[!UICONTROL Événement personnalisé]**, les définitions d’événement correspondantes (chemin d’accès de l’identifiant, identifiant de schéma XDM facultatif, schéma et transformateur) doivent être configurées dans le menu **[!UICONTROL Administration du programme de fidélité]** avant que les marketeurs puissent saisir des valeurs d’événement personnalisé dans le créateur de tâches. [Découvrez comment configurer des définitions d’événement](loyalty-admin.md#event-definitions)

Assurez-vous que les payloads d’événement utilisent le même espace de noms d’identité que votre configuration des défis de fidélité afin que la progression puisse être attribuée au profil correct.

### Audiences et création de rapports {#audiences-reporting}

Les spécialistes marketing sélectionnent Plateforme [audiences](../audience/about-audiences.md) lors de la configuration de l’éligibilité des défis. Les tableaux de bord de rapports de fidélité utilisent Adobe Customer Journey Analytics. [Découvrez comment surveiller les performances du défi de fidélité](loyalty-reporting.md)

## Durée de vie (TTL) du jeu de données {#dataset-ttl}

Les défis de fidélité stockent les données opérationnelles et de création de rapports dans les jeux de données Adobe Experience Platform (y compris les jeux de données liés aux événements et à la personnalisation créés pour votre programme). Le jeu de données **durée de vie (TTL)** contrôle la durée de conservation des données dans le lac de données et, le cas échéant, dans la banque de profils.

Journey Optimizer applique des mécanismes de sécurisation de durée de vie à de nombreux jeux de données générés par le système. Les jeux de données liés à la fidélité suivent le même modèle de conservation Platform pour votre sandbox.

➡️ [Mécanismes de sécurisation de la durée de vie (TTL) des jeux de données dans Journey Optimizer](../data/datasets-ttl.md)

>[!NOTE]
>
>La configuration de la fidélité au niveau de l’organisation peut inclure des paramètres d’archivage et de conservation (par exemple, la durée de l’archivage) gérés par le service de métadonnées de fidélité. Contactez votre administrateur ou administratrice Adobe si vous devez ajuster la rétention pour votre environnement bêta privé.
