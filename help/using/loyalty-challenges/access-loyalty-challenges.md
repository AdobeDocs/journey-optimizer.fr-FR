---
solution: Journey Optimizer
product: journey optimizer
title: Accéder aux défis et aux tâches et les gérer
description: Découvrez comment accéder aux défis et aux tâches de fidélité, les gérer et les organiser dans Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
badge: label="Private Beta" type="Informative"
mini-toc-levels: 1
source-git-commit: 5e11a0817ef6d1c7ef2e363cde48cddf932cd2c1
workflow-type: tm+mt
source-wordcount: '469'
ht-degree: 3%

---


# Accéder aux défis et aux tâches et les gérer {#access-loyalty-challenges}

>[!AVAILABILITY]
>
>Cette fonctionnalité est actuellement en version **Private Beta** et peut ne pas être disponible dans votre environnement. Pour demander l’accès, contactez votre représentant Adobe. En savoir plus sur les [libellés de disponibilité](../rn/releases.md#availability-labels).

>[!BEGINSHADEBOX]

**Documentation sur les défis de fidélité :**

* [Prise en main des défis de fidélité](get-started.md)
* **Accéder aux défis et aux tâches et les gérer** ◀︎ **Vous êtes ici**
* [Créer des défis](create-challenges.md)
* [Création de tâches](create-tasks.md)

>[!ENDSHADEBOX]

## Accéder aux défis et aux tâches et les gérer

Pour accéder aux Défis de fidélité, accédez à Journey Optimizer et sélectionnez **[!UICONTROL Défi de fidélité (Beta)]** sous la section **[!UICONTROL Gestion des Parcours]**. L’interface des Défis de fidélité fournit un emplacement centralisé pour afficher, gérer et organiser tous vos défis et tâches.

L’interface donne accès à deux inventaires principaux :

* **Défis** : affichez et gérez tous les défis de fidélité, surveillez leur statut et effectuez des actions rapides telles que l’affichage, la modification, la duplication ou la suppression de défis
* **Tâches** : parcourez les tâches réutilisables pouvant être utilisées pour plusieurs défis et gérez les définitions de tâche indépendamment


## Inventaire des défis {#challenges-tab}

L’onglet **[!UICONTROL Défis]** affiche tous les défis triés par date de dernière modification, les défis modifiés le plus récemment apparaissant en premier.

![](assets/challenges-inventory.png)

Informations clés affichées :

* **[!UICONTROL État]** : État actuel du défi (version préliminaire ou publiée)
* **[!UICONTROL Tâches]** : nombre de tâches configurées dans le défi
* **[!UICONTROL Parcours]** : lien vers le parcours généré automatiquement associé au défi
* **[!UICONTROL Statut]** : statut actuel du parcours associé (brouillon, actif, arrêté, etc.)
* **[!UICONTROL Date de début/fin (UTC)]** : le moment où le défi devient actif et expire

Dans l’onglet Défis , vous pouvez effectuer des actions sur les défis :

* **Afficher le défi** : sélectionnez le nom du défi pour ouvrir sa page de détails
* **Dupliquer un défi** : sélectionnez l’icône ![](assets/do-not-localize/Smock_More_18_N.svg) et choisissez **[!UICONTROL Dupliquer]**. Une copie est créée avec toutes les tâches, le contenu et les messages intacts.
* **Supprimer un défi** : sélectionnez l’icône ![](assets/do-not-localize/Smock_More_18_N.svg) et choisissez **[!UICONTROL Supprimer]**
* **Modifier un défi** : sélectionnez le nom du défi pour ouvrir sa page de détails et le modifier.

  Lorsque vous ouvrez un défi publié pour le modifier, vous devez d’abord le rétablir à l’état « Brouillon ». Toutes les personnalisations apportées directement au parcours généré automatiquement seront perdues. Après avoir apporté vos modifications, enregistrez et publiez à nouveau le défi, puis republiez le parcours associé.

  >[!IMPORTANT]
  >
  >La restauration d’un défi publié en version préliminaire ne peut pas être annulée. Tenez compte de l’impact sur votre parcours actif avant de continuer.

## Inventaire des tâches {#tasks-tab}

L’onglet **[!UICONTROL Tâches]** affiche toutes les tâches réutilisables qui peuvent être utilisées pour plusieurs défis. Les tâches créées ici peuvent être sélectionnées lors de la création ou de la modification d’un défi.

![](assets/tasks-inventory.png)

Informations clés affichées :

* **[!UICONTROL Description]** : brève description de ce que la tâche requiert
* **[!UICONTROL Activité de tâche]** : Type d&#39;activité (Achat, Dépenses)
* **[!UICONTROL SKU]** : éléments éligibles et/ou exclus
* **[!UICONTROL Utilisé dans les défis]** : nombre de défis utilisant actuellement cette tâche

Dans l’onglet Tâches , vous pouvez effectuer des actions sur les tâches :

* **Afficher/Modifier une tâche** : sélectionnez le nom de la tâche pour afficher la configuration complète et modifier la tâche
* **Dupliquer une tâche** : sélectionnez l&#39;icône ![](assets/do-not-localize/Smock_More_18_N.svg) et choisissez **[!UICONTROL Dupliquer]**
* **Supprimer une tâche** : sélectionnez l&#39;icône ![](assets/do-not-localize/Smock_More_18_N.svg) et choisissez **[!UICONTROL Supprimer]**
