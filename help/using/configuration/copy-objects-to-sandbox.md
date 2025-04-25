---
solution: Journey Optimizer
product: journey optimizer
title: Copier des objets Journey Optimizer entre des sandbox
description: Découvrez comment copier des parcours, des modèles de contenu et des fragments entre des sandbox.
feature: Journeys, Sandboxes
topic: Content Management
role: User, Developer, Data Engineer
level: Experienced
keywords: sandbox, parcours, copier, environnement
exl-id: 356d56a5-9a90-4eba-9875-c7ba96967da9
source-git-commit: ead10229b82aa8cb2e638ac9c26539de766f3497
workflow-type: ht
source-wordcount: '1100'
ht-degree: 100%

---

# Exporter des objets vers un autre sandbox {#copy-to-sandbox}

Vous pouvez copier des objets tels que des parcours, des modèles de contenu ou des fragments, sur plusieurs sandbox grâce aux fonctionnalités d’export et d’import de packages. Un package peut se composer d’un ou de plusieurs objets. Tous les objets inclus dans un package doivent provenir du même sandbox.

Cette page décrit le cas d’utilisation de l’outil Sandbox dans le contexte de Journey Optimizer. Pour plus d’informations sur la fonctionnalité elle-même, consultez la [documentation Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html?lang=fr).

>[!NOTE]
>
>Cette fonctionnalité nécessite les autorisations suivantes de la part de la fonctionnalité **Administration des sandbox** : gérer (ou afficher) les sandbox et gérer les packages. [En savoir plus](../administration/ootb-permissions.md)

Le processus de copie est réalisé via un export de package et un import entre les sandbox source et cible. Les étapes générales pour copier un parcours d’un sandbox vers un autre sont les suivantes :

1. Ajoutez l’objet à exporter en tant que package dans le sandbox source.
1. Exportez le package vers le sandbox cible.

## Objets exportés et bonnes pratiques {#objects}

Journey Optimizer permet d’exporter des parcours, des modèles de contenu et des fragments vers un autre sandbox. Les sections suivantes fournissent des informations et des bonnes pratiques pour chaque type d’objet.

### Bonnes pratiques générales {#global}

* Lors de la copie d’un objet, toutes les dépendances (telles que les fragments imbriqués, les audiences de parcours ou les actions) sont correctement mises à jour dans l’objet parent, assurant ainsi un mappage correct dans le sandbox cible.

* Si un objet exporté contient une personnalisation de profil, assurez-vous que le schéma approprié existe dans le sandbox cible afin d’éviter tout problème de personnalisation.

### Parcours {#journeys}

* Lors de l’export d’un parcours, en plus du parcours lui-même, Journey Optimizer copie également la plupart des objets dont dépend le parcours : audiences, schémas, événements et actions. Pour plus d’informations sur les objets copiés, reportez-vous à cette [section](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html?lang=fr#abobe-journey-optimizer-objects).

* Certains éléments associés peuvent échapper à la copie dans le sandbox de destination. Nous vous recommandons vivement de vérifier la viabilité du parcours, avant sa publication par exemple. Vous pourrez ainsi identifier tout objet potentiellement manquant.

* Les objets copiés dans le sandbox cible sont uniques et il n’y a aucun risque de remplacer des éléments existants. Le parcours et tous les messages qu’il contient sont transférés en mode brouillon. Vous pouvez ainsi effectuer une validation approfondie du parcours avant sa publication sur le sandbox cible.

* Le processus de copie ne copie que les métadonnées et les objets de ce parcours. Aucune donnée de profil ou de jeu de données n’est copiée dans le cadre de ce processus.

### Campagnes {#campaigns}

Les campagnes sont copiées avec tous les éléments liés au profil, à l’audience, au schéma, aux messages en ligne et aux objets dépendants.

Toutefois, les éléments suivants **ne sont pas** copiés :

* Variantes multilingues et paramètres de langue
* Variantes d’expérience
* Politiques de décision et éléments de décision
* Règles métier
* Balises
* Libellés DULE (application et libellé d’utilisation des données)

Une fois les campagnes copiées, les configurations de canal doivent être sélectionnées manuellement.

### Modèles de contenu {#content-templates}

* Lors de l’export d’un modèle de contenu, tous les fragments imbriqués sont également copiés avec celui-ci.

* L’export de modèles de contenu peut parfois entraîner une duplication de fragments. Par exemple, si deux modèles partagent le même fragment et sont copiés dans des packages distincts, les deux modèles devront réutiliser le même fragment dans le sandbox cible. Pour éviter la duplication, sélectionnez l’option « Utiliser le fragment existant » lors du processus d’import. [Découvrir comment importer un package](#import)

* Pour éviter toute duplication, il est recommandé d’exporter les modèles de contenu dans un seul package. Cela permet au système de gérer efficacement la déduplication.

### Fragments {#fragments}

* Les fragments peuvent avoir plusieurs statuts comme Actif, Brouillon et Actif avec brouillon en cours. Lors de l’export d’un fragment, son dernier état Brouillon est copié dans le sandbox cible.

* Lors de l’export d’un fragment, tous les fragments imbriqués sont également copiés avec celui-ci.

## Ajouter des objets en tant que package{#export}

Pour copier des objets dans un autre sandbox, vous devez d’abord les ajouter en tant que package dans le sandbox source. Procédez de la façon suivante :

1. Accédez à l’inventaire où est stocké le premier objet que vous souhaitez copier, comme la liste des parcours. Cliquez sur l’icône **Autres actions** (points de suspension en regard du nom de l’objet) et cliquez sur **Ajouter au package**.

   ![](assets/journey-sandbox1.png)

1. Dans la fenêtre **Ajouter au package**, choisissez si vous souhaitez ajouter l’objet à un package existant ou créer un package :

   ![](assets/journey-sandbox2.png)

   * **Package existant** : sélectionnez le package dans le menu déroulant.
   * **Créer un nouveau package** : saisissez le nom du package. Vous pouvez également ajouter une description.

1. Répétez ces étapes pour ajouter tous les objets que vous souhaitez exporter avec votre package.

>[!NOTE]
>
>Pour l’export du parcours, en plus du parcours lui-même, Journey Optimizer copie également la plupart des objets dont dépend le parcours : audiences, schémas, événements et actions. Pour plus d’informations sur l’export des parcours, consultez [cette section](../building-journeys/copy-to-sandbox.md).

## Publier le package à exporter {#publish}

Une fois votre package prêt à être exporté, procédez comme suit pour le publier :

1. Accédez au menu **[!UICONTROL Administration]** > **[!UICONTROL Sandbox]** et sélectionnez l’onglet **Packages**.

1. Ouvrez le package à exporter, sélectionnez les objets à exporter et cliquez sur **Publier**.

   Dans cet exemple, nous allons exporter un parcours, un modèle de contenu et un fragment.

   ![](assets/journey-sandbox4.png)

1. Pour suivre le statut de publication du package depuis l’onglet **[!UICONTROL Traitements]**. Pour plus d’informations sur un traitement, sélectionnez-le dans la liste et cliquez sur le bouton **[!UICONTROL Afficher les détails de l’import]**.

   ![](assets/journey-sandbox9.png)

## Importer le package vers le sandbox cible {#import}

Une fois le package publié, vous devez l’importer vers le sandbox cible. Procédez de la façon suivante :

1. Accédez au menu **[!UICONTROL Sandbox]** et sélectionnez l’onglet **[!UICONTROL Parcourir]**.

1. Recherchez le sandbox dans lequel vous souhaitez importer le package, puis cliquez sur l’icône + en regard de son nom.

   ![](assets/journey-sandbox5.png)

   >[!NOTE]
   >
   >Seuls les sandbox de votre organisation sont disponibles.

1. Dans le champ **Sandbox cible**, vérifiez que les sandbox cibles appropriés sont sélectionnés et sélectionnez le package à importer dans la liste déroulante **[!UICONTROL Nom du package]**. Cliquez sur **Suivant**.

   ![](assets/journey-sandbox6.png)

1. Examinez les objets et les dépendances du package. Il s’agit de la liste des objets qui ont été ajoutés au package, ainsi que d’autres objets dont les parcours dépendent, tels que les audiences, les schémas, les événements ou les actions.

   Pour chaque objet, vous pouvez choisir d’en créer un nouveau ou d’en utiliser un existant dans le sandbox cible. Cela vous permet, par exemple, d’éviter la duplication de fragments qui peut se produire lors de l’import de modèles de contenu à l’aide de fragments communs.

   ![](assets/journey-sandbox7.png)

1. Cliquez sur le bouton **Terminer** situé dans le coin supérieur droit pour commencer à copier le package dans le sandbox cible. La durée du processus de copie dépend de la complexité des objets et du nombre d’objets à copier.

1. Cliquez sur le traitement d’import pour vérifier le résultat de la copie :

   * Cliquez sur le bouton **Afficher les objets importés** pour afficher chaque objet copié.
   * Cliquez sur **Afficher les détails de l’import** pour vérifier les résultats de l’import de chaque objet.

   ![](assets/journey-sandbox8.png)

1. Accédez à votre sandbox cible et vérifiez minutieusement que tous les objets sont copiés.
