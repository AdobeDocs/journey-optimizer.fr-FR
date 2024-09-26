---
solution: Journey Optimizer
product: journey optimizer
title: Copie d’objets Journey Optimizer entre des environnements de test
description: Découvrez comment copier des parcours, des modèles de contenu et des fragments entre des environnements de test.
feature: Journeys, Sandboxes
topic: Content Management
role: User, Developer, Data Engineer
level: Experienced
keywords: sandbox, parcours, copie, environnement
source-git-commit: 62b5cfd480414c898ab6f123de8c6b9f99667b7d
workflow-type: tm+mt
source-wordcount: '1074'
ht-degree: 26%

---


# Copie d’objets Journey Optimizer dans un autre environnement de test {#copy-to-sandbox}

Les outils Sandbox vous permettent de copier des objets tels que des parcours, des modèles de contenu ou des fragments, sur plusieurs environnements de test en exploitant l’exportation et l’importation de modules. Un package peut se composer d’un ou de plusieurs objets. Tous les objets inclus dans un package doivent provenir du même sandbox.

Cette page décrit le cas d’utilisation de l’outil Sandbox dans le contexte de Journey Optimizer. Pour plus d’informations sur la fonctionnalité elle-même, consultez la [documentation Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html?lang=fr).

>[!NOTE]
>
>Cette fonctionnalité nécessite les autorisations suivantes de la part de la fonctionnalité **Administration des sandbox** : gérer (ou afficher) les sandbox et gérer les packages. [En savoir plus](../administration/ootb-permissions.md)

Le processus de copie est réalisé via un export de package et un import entre les sandbox source et cible. Les étapes générales pour copier un parcours d’un sandbox vers un autre sont les suivantes :

1. Ajoutez l’objet à exporter sous la forme d’un package dans l’environnement de test source.
1. Exportez le package vers le sandbox cible.

En outre, vous pouvez tirer parti de l’**API REST du service de copie d’objet** Journey Optimizer pour gérer les objets des sandbox. [Découvrez comment utiliser l’API REST du service de copie d’objet.](https://developer.adobe.com/journey-optimizer-apis/references/sandbox/)

## Objets exportés et bonnes pratiques {#objects}

Journey Optimizer permet d’exporter des parcours, des modèles de contenu et des fragments vers un autre environnement de test. Les sections suivantes fournissent des informations et des bonnes pratiques pour chaque type d’objet.

### Bonnes pratiques générales {#global}

* Lors de la copie d’un objet, toutes les dépendances (telles que les fragments imbriqués, les audiences de parcours ou les actions) sont correctement mises à jour dans l’objet parent, assurant ainsi un mappage correct dans l’environnement de test cible.

* Si un objet exporté contient une personnalisation de profil, assurez-vous que le schéma approprié existe dans l’environnement de test cible afin d’éviter tout problème de personnalisation.

### Parcours {#journeys}

* Lors de l&#39;export d&#39;un parcours, en plus du parcours lui-même, Journey Optimizer copie également la plupart des objets dont le parcours dépend : audiences, schémas, événements et actions. Pour plus d’informations sur les objets copiés, reportez-vous à cette [section](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html?lang=fr#abobe-journey-optimizer-objects).

* Nous ne garantissons pas que tous les éléments liés sont copiés dans l’environnement de test de destination. Nous vous recommandons vivement d’effectuer une vérification approfondie, par exemple avant de publier un parcours. Vous pouvez ainsi identifier tout objet manquant potentiel.

* Les objets copiés dans le sandbox cible sont uniques et il n’y a aucun risque de remplacer des éléments existants. Le parcours et tous les messages qu’il contient sont transférés en mode brouillon. Cela vous permet d’effectuer une validation approfondie avant la publication sur l’environnement de test cible.

* Le processus de copie ne copie que les métadonnées et les objets de ce parcours. Aucune donnée de profil ou de jeu de données n’est copiée dans le cadre de ce processus.

### Modèles de contenu {#content-templates}

* Lors de l’exportation d’un modèle de contenu, tous les fragments imbriqués sont également copiés avec celui-ci.

* L’exportation de modèles de contenu peut parfois entraîner une duplication de fragments. Par exemple, si deux modèles partagent le même fragment et sont copiés dans des modules distincts, les deux modèles devront réutiliser le même fragment dans l’environnement de test cible. Pour éviter la duplication, sélectionnez l&#39;option &quot;Utiliser existant&quot; lors du processus d&#39;import. [Découvrez comment importer un package](#import)

* Pour éviter toute duplication, il est recommandé d&#39;exporter les modèles de contenu dans un seul package. Cela permet au système de gérer efficacement la déduplication.

### Fragments {#fragments}

* Les fragments peuvent avoir plusieurs états tels que En direct, Version préliminaire et En direct avec le brouillon en cours. Lors de l’exportation d’un fragment, son dernier état Brouillon est copié dans l’environnement de test cible.

* Lors de l’exportation d’un fragment, tous les fragments imbriqués sont également copiés avec celui-ci.

## Ajouter des objets en tant que package{#export}

Pour copier des objets dans un autre environnement de test, vous devez d’abord les ajouter sous la forme d’un package dans l’environnement de test source. Procédez de la façon suivante :

1. Accédez à l’inventaire où est stocké le premier objet que vous souhaitez copier, comme la liste parcours. Cliquez sur l’icône **Autres actions** (les trois points en regard du nom de l’objet) et cliquez sur **Ajouter au package**.

   ![](assets/journey-sandbox1.png)

1. Dans la fenêtre **Ajouter au package** , choisissez si vous souhaitez ajouter l’objet à un package existant ou créer un package :

   ![](assets/journey-sandbox2.png)

   * **Package existant** : sélectionnez le package dans le menu déroulant.
   * **Créer un nouveau package** : saisissez le nom du package. Vous pouvez également ajouter une description.

1. Répétez ces étapes pour ajouter tous les objets que vous souhaitez exporter avec votre package.

>[!NOTE]
>
>Pour l&#39;export de parcours, en plus du parcours lui-même, Journey Optimizer copie également la plupart des objets dont le parcours dépend : audiences, schémas, événements et actions. Pour plus d&#39;informations sur l&#39;export de parcours, consultez [cette section](../building-journeys/copy-to-sandbox.md).

## Publish du package à exporter {#publish}

Une fois votre package prêt à être exporté, procédez comme suit pour le publier :

1. Accédez au menu **[!UICONTROL Administration]** > **[!UICONTROL Sandbox]** , sélectionnez l’onglet **Packages** .

1. Ouvrez le package à exporter, sélectionnez les objets à exporter et cliquez sur **Publish**.

   Dans cet exemple, nous allons exporter un parcours, un modèle de contenu et un fragment.

   ![](assets/journey-sandbox4.png)

1. Pour suivre l’état de publication du package depuis l’onglet **[!UICONTROL Tâches]** . Pour plus d’informations sur une tâche, sélectionnez-la dans la liste et cliquez sur le bouton **[!UICONTROL Afficher les détails de l’importation]** .

   ![](assets/journey-sandbox9.png)

## Importez le package dans l’environnement de test cible {#import}

Une fois le package publié, vous devez l’importer dans l’environnement de test cible. Procédez de la façon suivante :

1. Accédez au menu **[!UICONTROL Sandbox]** et sélectionnez l’onglet **[!UICONTROL Parcourir]** .

1. Recherchez l’environnement de test dans lequel vous souhaitez importer le package, puis cliquez sur l’icône + en regard de son nom.

   ![](assets/journey-sandbox5.png)

   >[!NOTE]
   >
   >Seules les sandbox de votre organisation sont disponibles.

1. Dans le champ **Environnement de test Target** , vérifiez que les environnements de test cible appropriés sont sélectionnés et sélectionnez le package à importer dans la liste déroulante **[!UICONTROL Nom du package]** . Cliquez sur **Suivant**.

   ![](assets/journey-sandbox6.png)

1. Examinez les objets et les dépendances du package. Il s’agit de la liste des objets qui ont été ajoutés au package, ainsi que d’autres objets dont les parcours dépendent, tels que les audiences, les schémas, les événements ou les actions.

   Pour chaque objet, vous pouvez choisir d’en créer un nouveau ou d’en utiliser un existant dans l’environnement de test cible. Cela vous permet, par exemple, d’éviter la duplication de fragments qui peut se produire lors de l’importation de modèles de contenu à l’aide de fragments communs.

   ![](assets/journey-sandbox7.png)

1. Cliquez sur le bouton **Terminer** dans le coin supérieur droit pour commencer à copier le package dans l’environnement de test cible. Le processus de copie varie en fonction de la complexité des objets et du nombre d’objets à copier.

1. Cliquez sur le traitement d’import pour vérifier le résultat de la copie :

   * Cliquez sur le bouton **Afficher les objets importés** pour afficher chaque objet copié.
   * Cliquez sur le bouton **Afficher les détails de l’importation** pour vérifier les résultats de l’importation pour chaque objet.

   ![](assets/journey-sandbox8.png)

1. Accédez à votre sandbox cible et vérifiez minutieusement que tous les objets sont copiés.
