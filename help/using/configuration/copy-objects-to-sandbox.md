---
solution: Journey Optimizer
product: journey optimizer
title: Copier des objets Journey Optimizer entre des sandbox
description: Découvrez comment copier des parcours, des campagnes, des modèles de contenu et des fragments entre des sandbox.
feature: Journeys, Sandboxes
topic: Content Management
role: User, Developer
level: Experienced
keywords: sandbox, parcours, copier, environnement
exl-id: 356d56a5-9a90-4eba-9875-c7ba96967da9
TQID: https://experienceleague.adobe.com/FfasSBtxSzc20knTVljqAJi4MVyoK9-RApQcTfDAa3Q
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: bb359667-ec7d-4d4b-8663-5850fc219d32
  - id: d556b755-390a-43f0-be32-a08cf6236126
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: b3a93754-a8b8-46eb-9421-7eccaeeb3dff
  - id: c6e980f5-2d4f-494f-beef-186b9ecf1513
  - id: cf64c7f6-7428-4ae5-b158-8df9771f38f4
  - id: d2e8a157-b3b0-4143-9ff3-809bf400be56
  - id: d595a60b-bcf5-4a63-a189-66a0be755cc7
  - id: e23d48b5-7858-4d45-9c56-9e2b4be8500e
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: a004cc84-67b9-4a33-a3a7-8ec7273ef4dc
  - id: bcc5edb5-84c3-4940-9f84-ed88b6c16274
  - id: d095671a-1355-40aa-8b5f-06c33c68080b
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
  - id: eddd9b14-83bd-4ff4-9072-54a4a484abb7
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 2371
ht-degree: 68%

---

# Exporter des objets vers un autre sandbox {#copy-to-sandbox}

Vous pouvez copier des objets tels que des parcours, des campagnes, des actions personnalisées, des modèles de contenu ou des fragments sur plusieurs sandbox à l’aide des fonctionnalités d’exportation et d’importation de packages. Un package peut se composer d’un ou de plusieurs objets. Tous les objets inclus dans un package doivent provenir du même sandbox.

Cette page décrit le cas d’utilisation de l’outil Sandbox dans le contexte de Journey Optimizer. Pour plus d’informations sur la fonctionnalité elle-même, reportez-vous au [guide des outils Sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html?lang=fr#abobe-journey-optimizer-objects){target="_blank"} d’Adobe Experience Platform.

>[!NOTE]
>
>Cette fonctionnalité nécessite les autorisations suivantes de la part de la fonctionnalité **Administration des sandbox** : gérer (ou afficher) les sandbox et gérer les packages. [En savoir plus](../administration/ootb-permissions.md)

Le processus de copie est réalisé via un export de package et un import entre les sandbox source et cible. Les étapes générales pour copier un parcours d’un sandbox vers un autre sont les suivantes :

1. [Ajouter l’objet à exporter en tant que package dans le sandbox source](#export)
1. [Publier le package](#publish)
1. [Importer le package dans le sandbox cible](#import)

>[!NOTE]
>
>Pour migrer les objets de gestion des décisions vers Decisioning, utilisez l’API dédiée [Migration Decisioning](../experience-decisioning/decisioning-migration-api.md) qui fournit des fonctionnalités automatisées de résolution des dépendances et de restauration spécialement conçues pour la migration des entités de prise de décision.

## Objets exportés et bonnes pratiques {#objects}

Journey Optimizer permet d’exporter des parcours, des campagnes (actions, déclenchées par API et orchestrées), des actions personnalisées, des modèles de contenu, des fragments et d’autres objets vers un autre sandbox. Les sections suivantes fournissent des informations et des bonnes pratiques pour chaque type d’objet.

### Bonnes pratiques générales {#global}

* Lors de la copie d’un objet, toutes les dépendances (telles que les fragments imbriqués, les audiences de parcours ou les actions) sont correctement mises à jour dans l’objet parent, assurant ainsi un mappage correct dans le sandbox cible.

* Si un objet exporté contient une personnalisation de profil, assurez-vous que le schéma approprié existe dans le sandbox cible afin d’éviter tout problème de personnalisation.

* La migration de pages de destination entre des sandbox n’est actuellement pas prise en charge. Lorsque vous copiez un parcours dans un autre sandbox, toutes les références aux pages de destination dans votre parcours ou dans le contenu des e-mails dirigeront toujours vers les identifiants de page de destination d’origine (source) du sandbox. Après la migration, vous devez mettre à jour manuellement toutes les références de page de destination dans votre parcours et vos contenus d’e-mails afin d’utiliser les identifiants de page de destination corrects du sandbox cible (de destination). Voir [Créer et publier des pages de destination](../landing-pages/create-lp.md).

+++ Parcours

* **Dépendances copiées** : lors de l’export d’un parcours, en plus du parcours lui-même, Journey Optimizer copie également la plupart des objets dont dépend le parcours : audiences, actions personnalisées, schémas, événements et actions. Pour plus d’informations sur les objets copiés, reportez-vous au [guide des outils Sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/sandbox-tooling.html?lang=fr#abobe-journey-optimizer-objects){target="_blank"} d’Adobe Experience Platform.

* **Validation manuelle recommandée** : certains éléments associés peuvent ne pas être copiés dans le sandbox de destination. Nous vous recommandons vivement de vérifier la viabilité du parcours, avant sa publication par exemple. Vous pourrez ainsi identifier tout objet potentiellement manquant.

* **Mode brouillon et unicité** : les objets copiés dans le sandbox cible sont uniques et il n’y a aucun risque de remplacer des éléments existants. Le parcours et tous les messages qu’il contient sont transférés en mode brouillon. Vous pouvez ainsi effectuer une validation approfondie du parcours avant sa publication sur le sandbox cible.

* **Métadonnées** : le processus de copie ne copie que les métadonnées et les objets de ce parcours. Aucune donnée de profil ou de jeu de données n’est copiée dans le cadre de ce processus.

* **Actions personnalisées**

   * Lors de l’export d’actions personnalisées, les paramètres de payload et de configuration d’URL sont copiés. Toutefois, pour des raisons de sécurité, les paramètres d’authentification ne sont pas copiés et sont remplacés par « INSÉRER LE SECRET ICI ». Les valeurs constantes d’en-tête de requête et de paramètre de requête sont également remplacées par « INSÉRER LE SECRET ICI ».

     Cela inclut les actions personnalisées à des fins spéciales ([!DNL Adobe Campaign Standard], [!DNL Campaign Classic], [!DNL Marketo Engage]).

   * Lors de la copie d’un parcours dans un autre sandbox, si vous sélectionnez « Utiliser existant » pour une action personnalisée au cours du processus d’import, l’action personnalisée existante que vous sélectionnez doit être identique à l’action personnalisée source (c’est-à-dire la même configuration, les mêmes paramètres, etc.). Dans le cas contraire, la nouvelle copie de parcours contiendra des erreurs qui ne pourront pas être résolues dans la zone de travail.

* **Sources de données, groupes de champs et événements** : lors de la copie d’un parcours qui utilise des événements, des sources de données ou des groupes de champs, le processus d’import vérifie automatiquement si des composants portant le même nom et du même type existent déjà dans le sandbox cible. Par exemple, un événement unitaire sera remplacé par un événement unitaire dans le sandbox cible portant le même nom. Il en va de même pour les événements métier, les sources de données personnalisées et les groupes de champs basés sur des API et des schémas utilisés dans les parcours. Si un événement unitaire provenant du sandbox source porte le même nom qu’un sandbox de destination d’événement métier, il n’est ni copié ni créé. Cela s’applique également à tous les autres composants.

+++

+++ Campagnes déclenchées par action et API

Vous pouvez copier des campagnes **Action**, **déclenchées par l’API** entre des sandbox à l’aide de l’exportation et de l’importation de packages.

Ces types de campagnes sont copiés avec tous les éléments liés au profil, à l’audience, au schéma, aux messages intégrés et aux objets dépendants.

Toutefois, les éléments suivants ne sont pas copiés :

* Variantes multilingues et paramètres de langue
* Règles métier
* Balises
* Libellés DULE (application et libellé d’utilisation des données)

Lors de la copie de campagnes **Action** ou **déclenchées par l’API**, assurez-vous que l’objet répertorié ci-dessous est validé dans le sandbox cible afin d’éviter les configurations incorrectes :

* **Configurations de canal** : les configurations de canal sont copiées avec les campagnes. Une fois les campagnes copiées, les configurations de canal doivent être sélectionnées manuellement dans le sandbox cible.
* **Variantes et paramètres d’expérience** : les variantes et paramètres d’expérience sont inclus dans le processus de copie de la campagne. Validez ces paramètres dans le sandbox cible après l’import.
* **Prise de décisions unifiée** : les politiques de décision et les éléments de décision sont pris en charge pour l’export et l’import. Assurez-vous que les dépendances liées aux décisions sont correctement mappées dans le sandbox cible.

+++

+++Campagnes orchestrées

Vous pouvez copier des campagnes orchestrées entre des sandbox à l’aide de l’exportation et de l’importation de packages. Les campagnes orchestrées suivent le même modèle global que les autres objets, mais ce qui est inclus dans le package et ce que vous devez préparer dans le sandbox cible diffère des campagnes déclenchées par une action ou une API.

Pour exporter une campagne orchestrée, [ajoutez-la à un package sandbox](#add-objects-as-a-package-export) dans le sandbox source (quel que soit son statut), [publiez le package](#publish), puis [importez le package](#import) dans le sandbox cible.

Avant d’importer en production, gardez à l’esprit les comportements et limites suivants :

* **Version préliminaire** - La campagne orchestrée importée est toujours créée en version préliminaire dans le sandbox cible, quel que soit le statut de la campagne orchestrée source.

* **Nouvel objet à chaque import** - L’import d’un package crée à nouveau une campagne orchestrée. Il ne remplace ni ne met à jour une campagne que vous avez importée précédemment.

* **La réexportation du même package n’est pas prise en charge** - La deuxième publication du même package après son exportation entraîne le statut d’erreur des activités de la campagne importée. Si cela se produit, vous devez supprimer les activités affectées et les recréer manuellement. Cette limitation sera corrigée dans une version ultérieure.

* **Les dépendances ne sont pas toutes copiées automatiquement** - L’ajout d’une seule campagne orchestrée à un package n’inclut pas une chaîne de dépendance complète en elle-même. Les configurations de canal, les schémas de magasin relationnel, les jeux de données et les règles métier ne sont pas inclus, sauf si vous les abordez explicitement (voir la puce suivante pour plus de détails).

  Lors de l’[import de package](#import), Journey Optimizer répertorie les objets à résoudre dans le sandbox cible. Les règles suivantes s’appliquent aux objets les plus courants :

   * **Campagne** — Sélectionnez toujours **Créer**.
   * **Audiences** — Pour les audiences Adobe Experience Platform, vous pouvez sélectionner **Créer** ou **Utiliser existant**. Pour les audiences de campagne orchestrées, vous devez sélectionner **Utiliser existant** et mapper à l’audience correspondante dans le sandbox cible.
   * **Politiques de fusion** — Sélectionnez **Utiliser existante** et mappez-la à la politique de fusion appropriée ou utilisez la politique par défaut dans le sandbox cible.

  Après l’importation, utilisez des alertes dans la campagne orchestrée pour trouver les écarts restants (par exemple, une ressource de profil ou de ciblage qui n’existe pas encore dans le sandbox cible peut laisser une activité avec une cible vide jusqu’à ce que vous la corrigiez).

* **Éléments à ajouter ou à aligner séparément** - Les éléments suivants ne sont pas inclus dans l’exportation de la campagne orchestrée :

   * **Configurations de canal** — Elles ne sont ni exportées ni importées avec le package. Pour que les activités de canal et d’e-mail fonctionnent sans correctifs manuels, le sandbox cible doit déjà disposer d’une configuration de canal dont le nom correspond exactement à la source (sensible à la casse) et qui utilise le même canal. Sinon, des alertes s’afficheront sur les activités après l’importation. Ouvrez chaque activité affectée et sélectionnez ou créez la configuration de canal appropriée.

   * **Schémas de magasin relationnel et jeux de données** — Si votre campagne dépend d&#39;un modèle de données donné, planifiez le schéma et l&#39;ordre d&#39;exportation/d&#39;importation des jeux de données afin que des dépendances existent lorsque vous en avez besoin (l&#39;exportation d&#39;un jeu de données extrait généralement les besoins des schémas associés, l&#39;exportation d&#39;un schéma seul n&#39;inclut pas son jeu de données). Notez que les jeux de données importés ne sont pas automatiquement activés pour les campagnes orchestrées. Vous devez les activer manuellement dans le sandbox cible après l’importation.

   * **Règles métier et objets de politique similaires** — Ils ne sont pas inclus dans l&#39;exportation de la campagne orchestrée. Si votre campagne en dépend, vérifiez qu’ils existent dans le sandbox cible ou recréez-les à cet endroit.

   * **Dimension cible du profil** — La dimension cible du profil n&#39;est pas incluse dans l&#39;exportation. S’il n’existe pas dans le sandbox cible, les activités correspondantes dans la campagne orchestrée importée seront vides jusqu’à ce que vous le configuriez manuellement.

+++

+++ Prise de décision

* Les objets ci-dessous doivent être présents dans le sandbox de destination avant de copier les objets de prise de décisions :

   * les attributs de profil utilisés dans les objets de prise de décisions,
   * le groupe de champs des attributs d’offre personnalisés,
   * les schémas des trains de données utilisés pour les attributs de contexte dans les règles, le classement ou la limitation.

* La copie de sandbox pour les formules de classement avec des modèles d’IA n’est actuellement pas prise en charge.

* Lors de la copie d’une campagne, les éléments de décision (éléments d’offre) ne sont pas automatiquement copiés. Veillez à les copier individuellement à l&#39;aide de l&#39;option « Ajouter au package ».

* Si une politique de décision comporte une stratégie de sélection, les éléments de décision doivent être ajoutés séparément. Si elle comporte des éléments de décision manuels/de secours, ils sont automatiquement ajoutés en tant que dépendances directes.

* Lors de la copie d’entités de prise de décisions, veillez à copier les éléments de décision **avant** tout autre objet. Par exemple, si vous copiez une collection en premier et qu’il n’existe aucune offre dans le nouveau sandbox, cette nouvelle collection reste vide.

* Lors de la copie d’entités avec des dépendances (un schéma, des segments, par exemple), cliquez sur « Créer » en regard de l’entité pour la désélectionner et afficher l’option « Utiliser celui existant » pour les artefacts dépendants. D’autres dépendances peuvent nécessiter de répéter cette étape plus bas dans la hiérarchie.

  Exemple : lors de l’import d’une campagne, pour réutiliser un schéma de train de données dans une règle, cliquez sur « Créer » pour DECISIONING_STRATEGY, puis de nouveau sur DECISIONING_RULES, afin d’afficher l’option « Utiliser celui existant » pour le schéma de train de données.

* Pour les entités qui dépendent d’un schéma contextuel de train de données, vérifiez que le train de données est créé au préalable et sélectionnez un schéma existant pour celui-ci.

* Si vous cliquez directement sur « Terminer » lors de l’import, toutes les dépendances sont recréées.

+++

+++ Modèles de contenu

* Lors de l’export d’un modèle de contenu, tous les fragments imbriqués sont également copiés avec celui-ci.

* L’export de modèles de contenu peut parfois entraîner une duplication de fragments. Par exemple, si deux modèles partagent le même fragment et sont copiés dans des packages distincts, les deux modèles devront réutiliser le même fragment dans le sandbox cible. Pour éviter la duplication, sélectionnez l’option « Utiliser le fragment existant » lors du processus d’import. [Découvrir comment importer un package](#import)

* Pour éviter toute duplication, il est recommandé d’exporter les modèles de contenu dans un seul package. Cela permet au système de gérer efficacement la déduplication.

+++

+++ Fragments

* Les fragments peuvent avoir plusieurs statuts comme Actif, Brouillon et Actif avec brouillon en cours. Lors de l’export d’un fragment, son dernier état Brouillon est copié dans le sandbox cible.

* Lors de l’export d’un fragment, tous les fragments imbriqués sont également copiés avec celui-ci.

+++

## Ajouter des objets en tant que package {#export}

Pour copier des objets dans un autre sandbox, vous devez d’abord les ajouter en tant que package dans le sandbox source. Procédez comme suit :

1. Accédez à l’inventaire où est stocké le premier objet que vous souhaitez copier, comme la liste des parcours. Cliquez sur l’icône **Autres actions** (points de suspension en regard du nom de l’objet) et cliquez sur **Ajouter au package**.

   ![](assets/journey-sandbox1.png)

1. Dans la fenêtre **Ajouter au package**, choisissez si vous souhaitez ajouter l’objet à un package existant ou créer un package :

   ![](assets/journey-sandbox2.png)

   * **Package existant** : sélectionnez le package dans le menu déroulant.
   * **Créer un nouveau package** : saisissez le nom du package. Vous pouvez également ajouter une description.

1. Répétez ces étapes pour ajouter tous les objets que vous souhaitez exporter avec votre package.

## Publier le package à exporter {#publish}

Une fois votre package prêt à être exporté, procédez comme suit pour le publier :

1. Accédez au menu **[!UICONTROL Administration]** > **[!UICONTROL Sandbox]** et sélectionnez l’onglet **Packages**.

1. Ouvrez le package à exporter, sélectionnez les objets à exporter et cliquez sur **Publier**.

   Dans cet exemple, nous allons exporter un parcours, un modèle de contenu et un fragment.

   ![](assets/journey-sandbox4.png)

1. Pour suivre le statut de publication du package depuis l’onglet **[!UICONTROL Traitements]**. Pour plus d’informations sur un traitement, sélectionnez-le dans la liste et cliquez sur le bouton **[!UICONTROL Afficher les détails de l’import]**.

   ![](assets/journey-sandbox9.png)

## Importer le package dans le sandbox cible {#import}

Une fois le package publié, vous devez l’importer vers le sandbox cible. Procédez comme suit :

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
