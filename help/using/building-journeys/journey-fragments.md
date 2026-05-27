---
solution: Journey Optimizer
product: journey optimizer
title: Fragments de parcours
description: Découvrez comment créer et utiliser des fragments de parcours pour enregistrer et réutiliser des ensembles de nœuds de parcours sur plusieurs parcours dans Adobe Journey Optimizer.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
keywords: fragments, parcours, réutilisation, nœuds, zone de travail, inventaire, réutilisable
badge: label="Disponibilité limitée" type="Informative"
version: Journey Orchestration
source-git-commit: 5e806bf6931a5c067adde232f61ff446bee18cca
workflow-type: tm+mt
source-wordcount: '1484'
ht-degree: 10%

---


# Fragments de parcours {#journey-fragments}

>[!AVAILABILITY]
>Cette fonctionnalité est actuellement en disponibilité limitée. Pour obtenir l’accès, contactez votre représentant ou représentante Adobe.

Les fragments de parcours sont des ensembles réutilisables de nœuds de parcours que vous pouvez créer une fois et déposer dans n’importe quel parcours de votre sandbox. Qu’il s’agisse d’une vérification d’éligibilité, d’une logique de routage de canal préférée ou d’une séquence de bienvenue, les fragments aident les équipes à se déplacer plus rapidement et à rester cohérentes, sans avoir à reconstruire la même logique à chaque fois. [Voir les exemples de cas d’utilisation.](#examples)

Une fois créés, les fragments sont stockés dans un **[!UICONTROL inventaire des fragments]** dédié et peuvent être insérés dans n’importe quel parcours à l’aide de l’activité **[!UICONTROL Fragments de Parcours]**.

>[!NOTE]
>Les fragments de parcours utilisent un comportement de **copie** : l’insertion d’un fragment dans un parcours crée une copie statique des nœuds d’origine. Les mises à jour apportées au fragment d’origine ne sont pas répercutées dans les parcours qui l’ont déjà utilisé.

## Autorisations {#journey-fragments-permissions}

Pour utiliser les fragments de parcours, vous avez besoin des [autorisations](../administration/permissions.md) suivantes :

* **Gérer les Parcours** : permet de créer, modifier et supprimer des fragments.
* **Publier les Parcours** — requis pour activer un fragment.

## Accès à l’inventaire des fragments {#journey-fragments-inventory}

Les fragments de parcours sont accessibles à partir de la section **[!UICONTROL Parcours]**. Ouvrez l’onglet **[!UICONTROL Fragments]** pour parcourir tous les fragments disponibles dans votre sandbox.

Vous pouvez filtrer la liste par nom de fragment, statut, date de création, créateur, date de dernière modification ou balise.

## Créer un fragment de parcours {#create-journey-fragment}

>[!CONTEXTUALHELP]
>id="ajo_journey_fragment_create_canvas"
>title="Enregistrer en tant que fragment de parcours"
>abstract="Saisissez un nom unique pour votre fragment et cliquez sur Enregistrer. Les nœuds sélectionnés seront enregistrés en tant que fragment réutilisable disponible dans l’inventaire des fragments."

Vous pouvez créer un fragment de parcours de deux manières : directement à partir de la zone de travail de parcours (recommandé) ou à partir de l’inventaire des fragments.

>[!BEGINTABS]

>[!TAB Dans la zone de travail du parcours ]

Pour enregistrer les nœuds de parcours en tant que fragment directement à partir de la zone de travail de parcours :

1. Ouvrez un parcours et sélectionnez un ou plusieurs nœuds connectés sur la zone de travail.
1. Cliquez sur l’icône **[!UICONTROL Enregistrer en tant que fragment]** dans la barre d’outils.

   ![Icône permettant d’insérer un fragment de parcours &#x200B;](assets/journey-fragment-icon.png)

1. Saisissez un nom unique pour le fragment dans votre sandbox.

   ![Enregistrez les nœuds en tant que fragment à partir de la zone de travail du parcours &#x200B;](assets/journey_fragment_create_canvas.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**. Le fragment est enregistré en tant que brouillon.

>[!TIP]
>
>Si vous créez un fragment à partir d’un parcours, [testez ou simulez votre parcours &#x200B;](testing-the-journey.md) **avant** d’enregistrer le fragment pour vous assurer que les nœuds sélectionnés se comportent comme prévu.

>[!TAB Dans l’inventaire des fragments]

Pour créer un fragment directement à partir de l’inventaire :

1. Accédez à l’onglet **[!UICONTROL Parcours]** > **[!UICONTROL Fragments de Parcours]**.
1. Cliquez sur **[!UICONTROL Créer un fragment de parcours]**.
1. Dans la zone de travail de création de fragments, ajoutez et configurez des activités de parcours.
1. Lorsque vous avez terminé, cliquez sur **[!UICONTROL Enregistrer]** pour enregistrer le fragment en tant que brouillon.

>[!CAUTION]
>
>Le mode Test et la simulation ne sont pas disponibles dans l’éditeur de fragments. Cela signifie que vous ne pouvez pas valider le comportement des activités configurées avant que le fragment ne soit activé et inséré dans un parcours. Pour les fragments dont la précision logique est essentielle, pensez à [créer et tester ou simuler les nœuds dans un parcours complet](testing-the-journey.md) tout d’abord, puis à les enregistrer en tant que fragment dans l’onglet Zone de travail ci-dessus.

>[!ENDTABS]

## Modifier un fragment {#edit-journey-fragment}

>[!CONTEXTUALHELP]
>id="ajo_journey_fragment_properties"
>title="Propriétés du fragment de parcours"
>abstract="Ouvrez un fragment à partir de l’inventaire pour modifier ses nœuds, propriétés, balises ou libellés. Les fragments actifs doivent être désactivés avant de pouvoir être modifiés."

Pour modifier un fragment, ouvrez-le dans l’**[!UICONTROL inventaire des fragments]** en cliquant sur son nom. Dans l’interface utilisateur de création de fragments, vous pouvez :

* Ajouter, supprimer ou modifier des activités.
* Définissez ou mettez à jour les propriétés du fragment : nom, balises et libellés.

>[!NOTE]
>
>* Seuls les fragments **[!UICONTROL Brouillon]** peuvent être modifiés. Pour modifier un fragment **[!UICONTROL actif]**, commencez par le désactiver.
>
>* Le mode Test et la simulation ne sont pas disponibles dans l’éditeur de fragments. Testez ou simulez une logique au niveau du parcours dans le parcours complet avant d’enregistrer les nœuds en tant que fragment.
>
>* Les activités [Saut](jump.md) ne sont pas autorisées dans un fragment.

## Gérer vos fragments {#manage-journey-fragments}

### Statuts des fragments {#fragment-statuses}

Les fragments de parcours suivent un cycle de vie avec les statuts suivants :

| État | Description |
|---|---|
| **[!UICONTROL Brouillon]** | Le fragment est en cours de création et ne peut pas encore être utilisé dans les parcours. |
| **[!UICONTROL Actif]** | Le fragment est prêt à être utilisé dans les parcours. |
| **[!UICONTROL Archivé]** | Le fragment a été archivé et ne peut plus être utilisé dans les parcours. |

Les règles suivantes s’appliquent aux transitions de statut de fragment :

* Seuls les fragments **[!UICONTROL Brouillon]** peuvent être activés. Ouvrez un brouillon de fragment et utilisez l’icône **[!UICONTROL Activer]**.
* Seuls les fragments **[!UICONTROL actifs]** peuvent être désactivés ou archivés.
* Seuls les fragments **[!UICONTROL archivés]** peuvent être désarchivés. Le désarchivage d’un fragment le renvoie au statut **[!UICONTROL Brouillon]**.
* Seuls les fragments **[!UICONTROL Brouillon]** peuvent être supprimés.

>[!NOTE]
>Lors de l’activation d’un fragment, la plupart des vérifications de validation exécutées lors de la publication du parcours sont appliquées. Toutefois, **les attributs contextuels ne sont pas validés** et **les politiques de gouvernance ne sont pas appliquées** au moment de l’activation ; les deux sont évaluées lorsque le fragment est inséré et utilisé dans un parcours.

### Actions sur le fragment {#fragment-actions}

Dans l’inventaire des fragments, vous pouvez effectuer les actions suivantes sur un fragment :

* **[!UICONTROL Ouvrir]** : modifiez le fragment en cliquant sur son nom.
* **[!UICONTROL Dupliquer]** : créez une copie du fragment, à partir des **[!UICONTROL Autres actions]** (...) icône.
* **[!UICONTROL Archiver]** : archivez un fragment (disponible uniquement pour les fragments **[!UICONTROL Actifs]**) à partir des **[!UICONTROL Autres actions]** (...). icône. Les fragments archivés ne sont plus disponibles dans le sélecteur de fragments.
* **[!UICONTROL Désarchiver]** : restaurez un fragment archivé (disponible uniquement pour les fragments **[!UICONTROL Archivés]**) à partir des **[!UICONTROL Autres actions]** (...). icône. Le fragment revient au statut **[!UICONTROL Brouillon]**.
* **[!UICONTROL Supprimer]** : supprimez définitivement un fragment (disponible uniquement pour les fragments **[!UICONTROL Brouillon]**) parmi les actions **[!UICONTROL Plus]** (...). icône.
* **[!UICONTROL Modifier les balises]** : ajoutez ou supprimez les balises d’un fragment, parmi les **[!UICONTROL Autres actions]** (...) icône.

## Utiliser un fragment dans un parcours {#use-journey-fragment}

>[!CONTEXTUALHELP]
>id="ajo_journey_fragment_add"
>title="Ajouter un fragment de parcours"
>abstract="Seuls les fragments **[!UICONTROL actifs]** sont disponibles dans le sélecteur. L’insertion d’un fragment crée une **copie statique** de ses nœuds. Les mises à jour apportées au fragment d’origine ne sont pas répercutées dans le parcours."

Pour insérer un fragment dans un parcours :

1. Ouvrez votre parcours et faites glisser l’activité **[!UICONTROL Fragments de Parcours]** depuis le rail de gauche.
1. Déposez-la dans une branche existante ou sur une zone de travail vide. Un sélecteur de fragment s’affiche.
1. Recherchez ou recherchez le fragment que vous souhaitez utiliser. Vous pouvez prévisualiser un fragment ou l’ouvrir dans un autre onglet avant de l’insérer.
1. Sélectionnez le fragment. Ses nœuds sont copiés dans la zone de travail au niveau du point de dépôt.

>[!NOTE]
>Seuls les fragments **[!UICONTROL actifs]** sont disponibles dans le sélecteur. L’insertion d’un fragment crée une **copie statique** de ses nœuds. Les mises à jour ultérieures apportées au fragment d’origine ne sont pas répercutées dans le parcours.
>
>Lorsqu’un fragment est déposé sur une zone de travail vide, il doit commencer par un nœud **[!UICONTROL Lecture d’audience]**, **[!UICONTROL Qualification d’audience]** ou **[!UICONTROL Événement]** (même règle que lors du démarrage d’un parcours).

## Mécanismes de sécurisation et limitations {#guardrails}

Les mécanismes de sécurisation suivants s’appliquent aux fragments de parcours :

**Création de fragment**

* Les noms de fragment doivent être **uniques par sandbox**.
* Un fragment ne peut avoir qu’**un seul chemin d’entrée**. Les sélections comportant plusieurs points d’entrée ne peuvent pas être enregistrées en tant que fragment.
* Seuls les **nœuds connectés** peuvent être enregistrés ensemble en tant que fragment.
* Un fragment **ne peut pas contenir d’activité [Saut](jump.md)**.
* Un fragment peut contenir **maximum 20 nœuds**.
* Un sandbox peut contenir un **maximum de 200 fragments actifs**.

**Utilisation des fragments**

* Seuls les fragments **[!UICONTROL actifs]** peuvent être insérés dans un parcours.
* L’insertion d’un fragment crée une **copie statique** de ses nœuds. Les mises à jour du fragment d’origine ne sont pas propagées aux parcours où il a été utilisé.
* Un fragment peut être déposé dans une branche existante ou sur une zone de travail vide. Lorsqu’il est déposé sur une zone de travail vide, le fragment doit commencer par un nœud **[!UICONTROL Lecture d’audience]**, **[!UICONTROL Qualification d’audience]** ou **[!UICONTROL Événement]**.

**Général**

* Les fragments se trouvent à l’aide de la barre [Recherche unifiée](../start/search-filter-categorize.md) sous la catégorie **[!UICONTROL Fragments de Parcours]**.
* [Balises](tags.md) et **Libellés** sont pris en charge sur les fragments.
* Les [&#x200B; Journaux d’audit &#x200B;](../privacy/audit-logs.md) sont pris en charge.
* Les parcours s’exécutant sur l’ancienne pile (à l’aide de campagnes intégrées) ne prennent pas en charge les fragments de parcours. Dupliquez un tel parcours pour le déplacer vers la nouvelle pile avant d’utiliser cette fonctionnalité.

## Exemples de cas d’utilisation {#examples}

Les exemples suivants illustrent des modèles de parcours courants qui peuvent être enregistrés et réutilisés en tant que fragments de parcours.

**Contrôles d’éligibilité**

Un modèle d’entrée standard, tel qu’un nœud [Lecture d’audience](read-audience.md) suivi de filtres d’éligibilité, peut être encapsulé dans un fragment. Cela permet aux équipes de maintenir une cohérence dans la manière dont les profils rejoignent les parcours tout en réduisant le temps de configuration. Le fragment peut être l’activité [Optimiser](optimize.md) uniquement ou l’activité Lecture d’audience et Optimiser ensemble.

![&#x200B; Exemple de fragment de vérification d’éligibilité &#x200B;](assets/journey-fragments-uc-eligibility-check.png)

**Canal préféré**

Un fragment peut évaluer le canal de communication préféré d’un profil (e-mail, notification push ou SMS) et acheminer le profil en conséquence. Cette logique peut être réutilisée dans n’importe quel parcours impliquant des messages sortants, ce qui permet d’assurer une gestion cohérente des préférences de canal. Le fragment peut inclure l’activité [Optimiser](optimize.md) et les trois branches de canal.

![&#x200B; Exemple de fragment de canal préféré &#x200B;](assets/journey-fragments-uc-preferred-channel.png)

**Séquence d’accueil de l’intégration**

Une séquence de bienvenue programmée, telle qu’une série de trois messages présentant un produit ou un service, peut être enregistrée en tant que fragment. Cela s’avère utile pour l’intégration de nouveaux utilisateurs dans différents segments d’audience ou lignes de produits. Le fragment peut inclure les activités [Attente](wait-activity.md) et les nœuds de message.

![Exemple de fragment de séquence d’accueil d’intégration](assets/journey-fragments-uc-welcome-sequence.png)

**Attente et rappel basés sur une réaction**

Un fragment peut encapsuler une activité E-mail suivie d’une [Réaction](reaction-events.md), en attendant que le profil ouvre l’e-mail dans un nombre de jours défini et en envoyant un rappel si ce n’est pas le cas. Cette logique est généralement réutilisée pour alimenter les parcours et tester les flux de conversion. Le fragment peut inclure les activités E-mail et Réaction .

![Exemple de fragment de rappel basé sur une réaction](assets/journey-fragments-uc-reminder.png)
