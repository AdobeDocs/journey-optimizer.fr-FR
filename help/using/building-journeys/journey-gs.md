---
solution: Journey Optimizer
product: journey optimizer
title: Créer votre premier parcours
description: Étapes clés de création de votre premier parcours avec Adobe Journey Optimizer
feature: Journeys, Get Started
topic: Content Management
role: User
level: Intermediate
keywords: parcours, premier, commencer, démarrage rapide, audience, événement, action
exl-id: d940191e-8f37-4956-8482-d2df0c4274aa
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: tm+mt
source-wordcount: '1803'
ht-degree: 98%

---

# Créer votre premier parcours{#jo-quick-start}

>[!CONTEXTUALHELP]
>id="ajo_homepage_card2"
>title="Créer des parcours"
>abstract="Utilisez **Adobe Journey Optimizer** pour créer des cas d’utilisation d’orchestration en temps réel à l’aide de données contextuelles stockées dans des événements ou des sources de données."

## Conditions préalables{#start-prerequisites}

Pour envoyer des messages avec des parcours, les configurations suivantes sont requises :

1. **Configurer un événement** : si vous souhaitez déclencher vos parcours une fois qu&#39;un événement est reçu, vous devez configurer un événement. Vous devez définir les informations attendues et comment les traiter. Cette étape est effectuée par un **utilisateur technique**. [En savoir plus](../event/about-events.md).

   ![](assets/jo-event7bis.png)

1. **Créer une audience** : votre parcours peut également écouter les audiences Adobe Experience Platform afin d’envoyer des messages par lots à un ensemble de profils spécifié. Pour cela, vous devez créer des audiences. [En savoir plus](../audience/about-audiences.md).

   ![](assets/segment2.png)

1. **Configurer la source de données** : vous devez définir une connexion à un système pour récupérer des informations supplémentaires qui seront utilisées pour vos parcours, par exemple dans vos conditions. Une source de données Adobe Experience Platform intégrée est également définie au moment de l&#39;approvisionnement. Cette étape n&#39;est pas obligatoire si vous n&#39;exploitez que les données des événements de votre parcours. Cette étape est effectuée par un **utilisateur technique**. [En savoir plus](../datasource/about-data-sources.md)

   ![](assets/jo-datasource.png)

1. **Configurer une action** : si vous utilisez un système tiers pour envoyer vos messages, vous pouvez créer une action personnalisée. En savoir plus dans cette [section](../action/action.md). Cette étape est effectuée par un **utilisateur technique**. Si vous utilisez les fonctionnalités de message intégrées à Journey Optimizer, vous devez simplement ajouter une action de canal à votre parcours et concevoir votre contenu.

   ![](assets/custom2.png)

## Accéder aux parcours {#journey-access}

>[!CONTEXTUALHELP]
>id="ajo_journey_create"
>title="Parcours"
>abstract="Concevoir des parcours clients pour offrir des expériences contextuelles personnalisées. Journey Optimizer vous permet de créer des cas d’utilisation d’orchestration en temps réel avec des données contextuelles stockées dans des événements ou des sources de données. L’onglet **Vue d’ensemble** affiche un tableau de bord avec les mesures clés liées à vos parcours : L’onglet **Parcourir** affiche la liste des parcours existants."

### Mesures clés et liste des parcours {#access-metrics}

Dans la section du menu GESTION DES PARCOURS, cliquez sur **[!UICONTROL Parcours]**. Deux onglets sont disponibles :

**Vue d’ensemble** : cet onglet affiche un tableau de bord avec les mesures clés liées à vos parcours :

* **Profils traités** : nombre total de profils traités au cours des dernières 24 heures
* **Parcours dynamiques** : nombre total de parcours dynamiques avec trafic au cours des dernières 24 heures. Les parcours dynamiques incluent les **parcours unitaires** (basés sur un événement) et les **parcours par lots** (lecture d’audience).
* **Taux d’erreur** : ratio de tous les profils en erreur par rapport au nombre total de profils entrés au cours des dernières 24 heures.
* **Taux de rejet** : ratio de tous les profils rejetés par rapport au nombre total de profils entrés au cours des dernières 24 heures. Un profil rejeté représente une personne qui ne répond pas aux conditions d’entrée du parcours, par exemple en raison d’un espace de noms incorrect ou des règles de reprise.

>[!NOTE]
>
>Ce tableau de bord prend en compte les parcours avec trafic au cours des dernières 24 heures. Seuls les parcours auxquels vous avez accès s’affichent. Les mesures sont actualisées toutes les 30 minutes et uniquement lorsque de nouvelles données sont disponibles.

![](assets/journeys-dashboard.png)

**Parcourir** : cet onglet affiche la liste des parcours existants. Vous pouvez rechercher des parcours, utiliser des filtres et effectuer des actions de base sur chaque élément. Vous pouvez par exemple dupliquer ou supprimer un élément. Voir à ce sujet [cette section](../start/user-interface.md#filter-lists).

![](assets/journeys-browse.png)

### Filtrer les parcours {#filter}

Dans la liste des parcours, vous pouvez utiliser différents filtres pour affiner la liste des parcours afin d’en améliorer la lisibilité.

![](assets/filter-journeys.png)

Voici les différentes opérations de filtrage que vous pouvez effectuer :

* Filtrez les parcours en fonction de leur statut, type, version et balises attribuées depuis les **[!UICONTROL Filtres de statut et de version]**.

  Le type peut être : **[!UICONTROL Événement unitaire]**, **[!UICONTROL Qualification d’audience]**, **[!UICONTROL Lecture d’audience]**, **[!UICONTROL Événement métier]** ou **[!UICONTROL Rafale]**.

* Utilisez les **[!UICONTROL filtres de création]** pour filtrer les parcours en fonction de leur date de création ou de la personne qui les a créés.

* Affichez les parcours qui utilisent un événement, un groupe de champs ou une action spécifique à l’aide des **[!UICONTROL filtres d’activité]** et des **[!UICONTROL filtres de données]**.

* Utilisez les **[!UICONTROL filtres de publication]** pour sélectionner une date de publication ou une personne. Vous pouvez choisir, par exemple, d’afficher les dernières versions des parcours actifs publiées la veille.

  Pour filtrer les parcours selon une période spécifique, sélectionnez **[!UICONTROL Personnalisé]** de la **[!UICONTROL Publié]** liste déroulante.

Dans les volets de configuration des événements, des sources de données et des actions, le champ **[!UICONTROL Utilisé dans]** affiche également le nombre de parcours qui utilisent cet événement, ce groupe de champs ou cette action spécifique. Vous pouvez cliquer sur le bouton **[!UICONTROL Afficher les parcours]** pour faire apparaître la liste des parcours correspondants.

![](assets/journey3bis.png)

## Créer votre parcours{#jo-build}

Cette étape est effectuée par l&#39;**utilisateur chargé de la conception de parcours**. C&#39;est là que vous créez vos parcours. Combinez les différentes activités d&#39;événement, d&#39;orchestration et d&#39;action afin de créer des scénarios cross-canal à plusieurs étapes.

Voici les étapes principales pour envoyer des messages à travers des parcours :

1. Dans l’onglet **Parcourir**, cliquez sur **[!UICONTROL Créer un Parcours]** pour créer un parcours.

1. Modifiez les propriétés du parcours dans le volet de configuration qui s&#39;affiche dans la partie droite. En savoir plus dans cette [section](journey-gs.md#change-properties).

   ![](assets/jo-properties.png)

1. Commencez par effectuer un glisser-déposer d’un événement ou d’une activité **Lecture d’audience** de la palette vers la zone de travail. Pour en savoir plus sur la conception d&#39;un parcours, consultez [cette section](using-the-journey-designer.md).

   ![](assets/read-segment.png)

1. Faites glisser et déposez les étapes suivantes que l&#39;individu doit suivre. Par exemple, vous pouvez ajouter une condition suivie d’une action de canal. Pour en savoir plus sur les activités, consultez [cette section](using-the-journey-designer.md).

1. Testez votre parcours à l&#39;aide de profils de test. En savoir plus dans cette [section](testing-the-journey.md)

1. Publiez votre parcours pour l&#39;activer. En savoir plus dans cette [section](publishing-the-journey.md).

   ![](assets/jo-journeyuc2_32bis.png)

1. Surveillez votre parcours à l&#39;aide des outils de rapports dédiés afin de mesurer l&#39;efficacité de votre parcours. En savoir plus dans cette [section](../reports/live-report.md).

   ![](assets/jo-dynamic_report_journey_12.png)

## Définition des propriétés de votre parcours {#change-properties}

>[!CONTEXTUALHELP]
>id="ajo_journey_properties"
>title="Propriétés du parcours"
>abstract="Cette section présente les propriétés du parcours. Par défaut, les paramètres en lecture seule sont masqués. Les paramètres disponibles dépendent du statut du parcours, de vos autorisations et de la configuration de votre produit."

Cliquez sur l’icône en forme de crayon, en regard du nom du parcours, pour accéder à ses propriétés.

Vous pouvez modifier le nom du parcours, ajouter une description, autoriser une rentrée, choisir les dates de début et de fin, et, si vous être administrateur, définir une durée de **[!UICONTROL Temporisation et erreur]**. Vous pouvez également attribuer des balises unifiées Adobe Experience Platform à votre parcours. Vous pouvez ainsi facilement les classer et améliorer la recherche à partir de la liste des campagnes. [Découvrir comment utiliser les balises](../start/search-filter-categorize.md#tags)

Pour les parcours actifs, cet écran affiche la date de publication et le nom de l’utilisateur qui a publié le parcours.

La fonction **Copier les détails techniques** permet de copier les informations techniques relatives au parcours qui seront utiles à l&#39;équipe d&#39;assistance technique pour résoudre les problèmes. Les informations suivantes sont copiées : UID JourneyVersion, OrgID, orgName, sandboxName, lastDeployedBy, lastDeployedAt.

![](assets/journey32.png)

### Entrée et reprise {#entrance}

Par défaut, les nouveaux parcours autorisent la reprise. Vous pouvez désélectionner l’option **Autoriser la reprise** pour les parcours « uniques », par exemple, si vous souhaitez offrir un cadeau unique à un utilisateur ou une utilisatrice qui effectue sa première visite dans la boutique.

Lorsque l’option **Autoriser une reprise** est activée, le champ **Période d’attente de reprise** s’affiche. Ce champ vous permet de définir le temps d’attente avant d’autoriser un profil à entrer à nouveau dans un parcours pour les parcours unitaires (en commençant par un événement ou une qualification d’audience). Cela empêche les parcours d’être déclenchés plusieurs fois par erreur pour le même événement. Par défaut, le champ est défini sur 5 minutes. La durée maximale est de 29 jours.

En savoir plus sur la gestion des entrées et des reprises de profils dans [cette section](entry-management.md).

### Gérer l’accès {#manage-access}

Pour attribuer des libellés d’utilisation des données personnalisés ou de base au parcours, cliquez sur le bouton **[!UICONTROL Gérer l’accès]**. [En savoir plus sur le contrôle d’accès au niveau de l’objet (OLA)](../administration/object-based-access.md)

![](assets/journeys-manage-access.png)

### Fuseaux horaires des parcours et des profils {#timezone}

Le fuseau horaire est défini au niveau du parcours. Vous pouvez entrer un fuseau horaire fixe ou utiliser les profils Adobe Experience Platform pour définir le fuseau horaire du parcours. Si un fuseau horaire est défini dans le profil Adobe Experience Platform, il peut être récupéré dans le parcours.

Pour plus d&#39;informations sur la gestion des fuseaux horaires, voir [cette page](../building-journeys/timezone-management.md).

### Dates de début et de fin {#dates}

Vous pouvez définir une **date de début**. Si vous n’en avez pas spécifié une, elle sera automatiquement définie au moment de la publication.

Vous pouvez également ajouter une **date de fin**. Cela permet aux profils de se fermer automatiquement lorsque la date est atteinte. Si aucune date de fin n’est spécifiée, les profils peuvent rester jusqu’au [délai d’expiration du parcours global](#global_timeout) (30 jours en général ou 7 jours avec l’offre de module complémentaire Healthcare Shield). La seule exception concerne les parcours de lecture d’audience récurrents avec l’option **Forcer une reprise sur la périodicité** activée, qui se termine à la date de début de l’occurrence suivante.

### Temporisation et erreur dans les activités du parcours {#timeout_and_error}

Lorsque vous modifiez une action ou une activité de condition, vous pouvez définir un autre chemin en cas d&#39;erreur ou de temporisation. Si la durée de traitement de l’activité qui interroge un système tiers dépasse la durée de temporisation définie dans les propriétés du parcours (champ **[!UICONTROL Temporisation et erreur]**), le deuxième chemin d’accès est choisi pour effectuer une éventuelle action de remplacement.

Les valeurs autorisées sont comprises entre 1 et 30 secondes.

Nous vous recommandons de définir une valeur très basse pour **[!UICONTROL Temporisation et erreur]** si votre parcours est sensible au temps (c&#39;est le cas, par exemple, lorsqu&#39;il convient de réagir à la position en temps réel d&#39;une personne), car l&#39;action ne peut pas être différée de plus de quelques secondes. Si le facteur temps revêt une importance moindre, vous pouvez définir un délai plus long afin d’accorder davantage de temps au système appelé pour envoyer une réponse valide.

Les parcours utilisent également une temporisation globale. Pour plus d&#39;informations, consultez la [section suivante](#global_timeout).

### Temporisation de parcours globale {#global_timeout}

Outre la [temporisation](#timeout_and_error) utilisée dans les activités de parcours, il existe une temporisation globale qui n’est pas affichée dans l’interface et qui ne peut pas être modifiée.

Cette temporisation globale met fin à la progression des individus dans le parcours **30 jours** après leur entrée. Cette temporisation est réduite à **7 jours** avec l’offre de module complémentaire Healthcare Shield. En d’autres termes, la durée du parcours d’une personne ne peut pas excéder 30 jours (ou 7 jours). Après cette période de temporisation, les données de cette personne sont supprimées. Les personnes qui sont encore actives dans le parcours au terme de cette période de temporisation seront arrêtées et ne seront pas prises en compte dans le cadre du reporting. Vous pouvez donc voir plus de personnes rejoindre le parcours que le quitter.

>[!NOTE]
>
>Les parcours ne réagissent pas directement aux demandes d&#39;opt-out, de suppression ou d&#39;accès. Cependant, la temporisation globale limite à 30 jours la durée d&#39;activité d&#39;un individu au sein d&#39;un parcours.

Compte tenu de la temporisation de 30 jours, lorsque la rentrée n’est pas autorisée, nous sommes dans l’impossibilité de garantir que le blocage de rentrée fonctionnera plus de 30 jours. En effet, étant donné que nous supprimons toutes les informations sur les personnes qui ont rejoint le parcours 30 jours après leur entrée, rien ne nous permet de savoir qu&#39;une personne l&#39;a déjà rejoint il y a plus de 30 jours.

Un individu ne peut entrer dans une activité d’attente que s’il dispose de suffisamment de temps dans le parcours pour terminer la durée d’attente avant la temporisation de 30 jours du parcours. Consultez [cette page](../building-journeys/wait-activity.md).

## Dupliquer un parcours {#duplicate-a-journey}

Vous pouvez dupliquer un parcours existant à partir de l’onglet **Parcourir**. Tous les objets et paramètres sont dupliqués dans la copie de parcours.

Pour ce faire, suivez les étapes ci-après :

1. Accédez au parcours à copier, puis cliquez sur l’icône **Autres actions** (les points de suspension en regard du nom du parcours).
1. Sélectionnez **Dupliquer**.

   ![Duplication d’un parcours.](assets/duplicate-jo.png)

1. Saisissez le nom du parcours et confirmez. Vous pouvez également modifier le nom dans l’écran des propriétés du parcours. Par défaut, le nom est défini comme suit : `[JOURNEY-NAME]_copy`

   ![](assets/duplicate-jo2.png)

1. Le nouveau parcours est créé et disponible dans la liste des parcours.
