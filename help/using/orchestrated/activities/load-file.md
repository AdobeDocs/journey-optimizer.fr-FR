---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l'activité Chargement de fichier
description: Découvrez comment utiliser l’activité Chargement de fichier pour cibler une audience de campagne orchestrée à partir d’un fichier CSV ou TXT sans ingérer le fichier dans Adobe Experience Platform
hide: true
exl-id: a7c3e891-4f2d-4b8e-9c1a-6e8f0d3b2a41
version: Campaign Orchestration
product_v2: id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2: id: b3538224-471e-4c63-a444-9b19d89ae29cid: d556b755-390a-43f0-be32-a08cf6236126
topic_v2: id: b5ce8718-c3af-4fdb-a1a9-fca32f83a87c
source-git-commit: abac7d8c49e2dc7af9fde91b0e8305ce10a406ce
workflow-type: tm+mt
source-wordcount: 1511
ht-degree: 2%

---

# Chargement de fichier {#load-file}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_load_file"
>title="Activité Chargement de fichier"
>abstract="L’activité **Chargement de fichier** est une activité **Gestion des données**. Utilisez-la pour travailler avec des profils et des données stockés dans un fichier externe sur la zone de travail de campagne orchestrée et définir l’audience de la campagne. Les données de fichier sont utilisées au moment de l’exécution et ne sont pas conservées en tant que jeu de données Adobe Experience Platform. Les lignes sont réconciliées avec les destinataires existants à l’aide d’une colonne d’identité et d’une dimension de ciblage. Contactez votre représentant Adobe pour demander l’accès."

L’activité **[!UICONTROL Chargement de fichier]** est une activité **[!UICONTROL Gestion des données]**. Utilisez-la pour travailler avec des profils et des données stockés dans un fichier externe. Il prend en charge le **ciblage basé sur des fichiers** dans les campagnes orchestrées lorsque votre liste de destinataires provient d’un système externe (par exemple, une exportation CRM ou un fichier de partenaire) et que vous souhaitez exécuter une campagne sans créer d’abord un pipeline d’ingestion Adobe Experience Platform complet.

>[!AVAILABILITY]
>
>L’activité **Chargement de fichier** est disponible dans **Disponibilité limitée** pour un ensemble d’organisations. Pour obtenir l’accès, contactez votre représentant ou représentante Adobe. Pour connaître les phases de disponibilité, consultez le cycle de publication de [](../../rn/releases.md).
>
>L’activité n’est actuellement pas disponible pour une utilisation avec **Healthcare Shield** ou **Privacy and Security Shield**.

## Mécanismes de sécurisation et limitations {#limitations}

Les restrictions suivantes s&#39;appliquent à l&#39;activité Chargement de fichier :

* Vous pouvez charger jusqu’à 50 Mo par fichier.
* Seuls les fichiers CSV et TXT à structure plate sont pris en charge.
* Les données chargées sont utilisées lors de l’exécution de la campagne et ne sont pas stockées sous la forme d’un jeu de données Adobe Experience Platform.
* Chaque ligne doit correspondre à un destinataire existant pour la dimension de ciblage que vous sélectionnez. L’activité Chargement de fichier ne crée pas de profils à partir du fichier.

Pour connaître les limites des activités de canal et de zone de travail, voir [Mécanismes de sécurisation et limitations](../guardrails.md#activities-limitations).

## Conditions préalables {#prerequisites}

Avant de configurer une activité **[!UICONTROL Chargement de fichier]** :

1. Créez la **[!UICONTROL dimension de ciblage]** dont vous avez besoin pour la réconciliation (par exemple, Destinataires). [Découvrez comment créer une dimension de ciblage](../target-dimension.md)

1. Assurez-vous que les valeurs d’identité de votre fichier correspondent aux enregistrements existants pour cette dimension. Les lignes du fichier chargé sont réconciliées avec les destinataires existants. L’activité ne crée pas de nouveaux profils à partir du fichier.

## Configurer l’activité Chargement de fichier {#load-file-configuration}

Configurez l’activité en deux parties : définissez la structure de fichiers attendue avec un exemple de fichier, puis spécifiez le fichier à charger lors de l’exécution de la campagne et le mode de réconciliation des lignes avec votre dimension de ciblage.

Pour configurer l&#39;activité **[!UICONTROL Chargement de fichier]**, procédez comme suit :

1. Ajoutez une activité **[!UICONTROL Chargement de fichier]** à la zone de travail de votre campagne orchestrée.

   ![](../assets/load-file.png)

1. Saisissez un **[!UICONTROL Libellé]** pour l’activité.

1. Dans la section **[!UICONTROL Fichier d’exemple]**, sélectionnez le fichier local qui définit la structure attendue.

   >[!NOTE]
   >
   > L’exemple de fichier est utilisé pour configurer les colonnes et la mise en forme uniquement. Ses données ne sont pas importées en tant qu’audience de campagne. Le format doit correspondre aux fichiers que vous chargerez lors de l’exécution de la campagne.

1. Dans la liste déroulante **[!UICONTROL Type de fichier]**, indiquez si le fichier utilise des **colonnes délimitées** ou **colonnes à largeur fixe**.

   ![](../assets/load-file-sample.png)

1. Dans la section **[!UICONTROL Colonnes]**, développez chaque colonne et configurez ses propriétés.

   ![](../assets/load-file-sample-columns.png)

   Les propriétés suivantes sont disponibles pour chaque colonne. Après avoir sélectionné un **[!UICONTROL type de données]**, des options supplémentaires s’affichent pour ce type. Développez les sections ci-dessous pour obtenir la liste complète par type de données.

   * **[!UICONTROL Ignorer la colonne]** — Exclure la colonne de l&#39;importation lorsqu&#39;elle est sélectionnée.
   * **[!UICONTROL Libellé]** — Nom d&#39;affichage de la colonne (par exemple, `email`).
   * **[!UICONTROL Nom interne]** — Nom système de la colonne, dérivé de l&#39;en-tête du fichier (lecture seule).
   * **[!UICONTROL Type de données]** — Type de données dans la colonne.
   * **[!UICONTROL Allow NULLs]** — Indique comment gérer les valeurs vides dans la colonne :

      * **[!UICONTROL Adobe Campaign par défaut]** — Génère une erreur pour les champs numériques uniquement. Sinon insère une valeur NULL.
      * **[!UICONTROL Valeur vide autorisée]** — Autorise les valeurs vides. La valeur NULL est alors insérée.
      * **[!UICONTROL Toujours renseignée]** — Génère une erreur en cas de valeur vide.

   * **[!UICONTROL Traitement des erreurs]** — Définit le comportement en cas d&#39;erreur dans la colonne :

      * **[!UICONTROL Ignorer la valeur]** — La valeur est ignorée.
      * **[!UICONTROL Rejeter la ligne]** — La ligne entière n&#39;est pas traitée.
      * **[!UICONTROL Utiliser une valeur par défaut en cas d&#39;erreur]** — Remplace la valeur causant l&#39;erreur par une valeur par défaut, définie dans le champ **[!UICONTROL Valeur par défaut]**.
      * **[!UICONTROL Utiliser une valeur par défaut en cas d&#39;absence de recodification]** — Remplace la valeur causant l&#39;erreur par une valeur par défaut, définie dans le champ **[!UICONTROL Valeur par défaut]**, sauf si une correspondance a été définie pour la valeur en erreur.
      * **[!UICONTROL Rejeter la ligne en cas d&#39;absence de recodification]** — La ligne entière n&#39;est pas traitée sauf si une correspondance a été définie pour la valeur en erreur.

   * **[!UICONTROL Valeur par défaut]** — Valeur par défaut à utiliser lorsque **[!UICONTROL Traitement d&#39;erreur]** est défini pour utiliser une valeur par défaut.
   * **[!UICONTROL Remappage des valeurs]** — Mappez des valeurs spécifiques aux nouvelles. Cliquez sur **[!UICONTROL Ajouter un mappage]** pour définir chaque mappage (par exemple, remplacez `True`/`False` par `1`/`0`).

   +++Paramètres des colonnes de chaînes

   * **[!UICONTROL Largeur]** — Nombre maximal de caractères.
   * **[!UICONTROL Transformation des données]** — Transformation de la casse appliquée aux valeurs de chaîne (par exemple, aucune ou majuscule/minuscule).
   * **[!UICONTROL Gestion des espaces]** — Comment gérer les espaces de début et de fin dans les valeurs de chaîne.

   +++

   +++Paramètres des colonnes de nombres entiers et flottants

   * **[!UICONTROL Format]** — Définit la façon dont les valeurs numériques du fichier sont lues :

      * **[!UICONTROL Autre]** — Définissez le **[!UICONTROL séparateur des milliers]** et le **[!UICONTROL séparateur décimal]** dans la section **[!UICONTROL Séparateurs]**.
      * **[!UICONTROL 1,000.00]** — Virgule comme séparateur de milliers et point comme séparateur décimal.
      * **[!UICONTROL 1 000,00]** — Espace comme séparateur de milliers et virgule comme séparateur décimal.

   * **[!UICONTROL Séparateurs]** (lorsque **[!UICONTROL Format]** est **[!UICONTROL Autre]**) :

      * **[!UICONTROL Séparateur des milliers]** — Caractère qui regroupe des milliers en valeurs numériques (laisser vide si non utilisé).
      * **[!UICONTROL Séparateur décimal]** — Caractère utilisé pour la partie décimale des valeurs numériques (par exemple, `,` ou `.`).

   +++

   +++Paramètres des colonnes de dates

   * **[!UICONTROL Format de date]** — Modèle correspondant à la façon dont les dates apparaissent dans le fichier (par exemple, `yyyy/mm/dd`).
   * **[!UICONTROL Séparateurs]** :

      * **[!UICONTROL Année, mois, jour]** — Caractère entre les composants année, mois et jour (par exemple, `/`).

   +++

   +++Paramètres des colonnes de temps

   * **[!UICONTROL Format de l’heure]** — Modèle correspondant à la façon dont les heures apparaissent dans le fichier (par exemple, `13:30` pour les heures et minutes de 24 heures).
   * **[!UICONTROL Séparateurs]** :

      * **[!UICONTROL Heure, minute, seconde]** — Caractère entre les composants heure, minute et seconde (par exemple, `:`).

   +++

   +++Paramètres des colonnes Date et heure

   * **[!UICONTROL Format de date]** — Modèle correspondant à la façon dont la partie de date apparaît dans le fichier.
   * **[!UICONTROL Format de l’heure]** — Motif correspondant à l’affichage de la partie temporelle dans le fichier.
   * **[!UICONTROL Séparateurs]** — Caractères entre les composants de date et d’heure, comme indiqué dans l’interface utilisateur de votre colonne.

   +++

1. Dans la section **[!UICONTROL Formatage]**, spécifiez la structure du fichier pour que les lignes et les colonnes soient lues correctement lors de l’exécution de la campagne. Le fichier cible doit utiliser la même mise en forme que l’exemple de fichier.

   ![](../assets/load-file-sample-formatting.png)

   * **[!UICONTROL Utiliser la première ligne comme en-tête de colonne]** — Lorsqu&#39;elle est sélectionnée, la première ligne du fichier est traitée comme des noms de colonne. Cette option est généralement activée lorsque vous configurez l’exemple d’un fichier qui inclut une ligne d’en-tête.
   * **[!UICONTROL Utiliser un numéro de ligne comme identificateur]** — Lorsqu&#39;elle est sélectionnée, chaque ligne est identifiée par son numéro de ligne dans le fichier.
   * **[!UICONTROL Les enregistrements s&#39;étendent sur plusieurs lignes]** : si vous sélectionnez un seul enregistrement, il peut s&#39;étendre sur plusieurs lignes du fichier (par exemple, lorsque les champs contiennent des sauts de ligne).
   * **[!UICONTROL Lignes à ignorer]** — Nombre de lignes à ignorer au début du fichier avant la lecture des données (par exemple, lignes de commentaire ou de métadonnées).
   * **[!UICONTROL Fuseau horaire]** — Fuseau horaire appliqué lors de l&#39;importation des valeurs de date et d&#39;heure.
   * **[!UICONTROL Encodage]** — Encodage des caractères du fichier. Sélectionnez le codage correspondant à votre fichier source.
   * **[!UICONTROL Délimiteur de chaîne]** — Caractère utilisé pour entourer les valeurs de chaîne dans le fichier.
   * **[!UICONTROL Séparateur de colonnes]** — Caractère séparant les colonnes d&#39;un fichier délimité.

1. Dans la section **[!UICONTROL Fichier cible]**, choisissez comment le fichier est fourni (par exemple, **[!UICONTROL Charger un fichier à partir d’un ordinateur local]** pour un chargement manuel dans cette version).

1. Sélectionnez le fichier CSV ou TXT à charger.

   >[!CAUTION]
   >
   > Assurez-vous que le fichier cible suit le même format, la même structure de colonnes et le même nombre de colonnes que l’exemple de fichier. Les incohérences peuvent entraîner des erreurs lors de l’exécution.

1. Sélectionnez la colonne d’identité dans le fichier : champ utilisé pour faire correspondre chaque ligne à un destinataire existant (par exemple, adresse e-mail ou ID de client).

1. Sélectionnez la **[!UICONTROL Dimension de ciblage]** à réconcilier.

1. Une fois la configuration terminée, prévisualisez un exemple de lignes mappées si l’interface utilisateur le propose, puis confirmez.

1. Dans la section **[!UICONTROL Gestion des rejets]** , définissez le comportement de l’activité en cas d’erreur lors du traitement du fichier :

   * **[!UICONTROL Nombre d&#39;erreurs autorisées]** — Nombre maximal d&#39;erreurs autorisées avant l&#39;échec de l&#39;activité.
   * **[!UICONTROL Conserver les rejets dans un fichier]** — Lorsque cette option est activée, les lignes qui n&#39;ont pas pu être chargées sont écrites dans un fichier de rejets sur le serveur pour révision après exécution.

1. Connecter la transition sortante aux activités en aval.

Les lignes qui ne peuvent pas être réconciliées avec un destinataire existant sont exclues de l&#39;audience. Les lignes exclues sont enregistrées dans le journal d’exécution de la campagne ; la campagne n’échoue pas uniquement parce que certaines lignes ne correspondent pas.

## Utiliser l’audience de fichiers dans les diffusions {#downstream}

Une fois que **[!UICONTROL Charger le fichier]** a résolu l’audience, vous pouvez utiliser des activités de campagne orchestrées standard :

* **[Activités de canal](channels.md)** — E-mail, SMS, notification push ou courrier.

* **[Enrichissement](enrichment.md)** ou **[Réconciliation](reconciliation.md)** — Affinez ou liez davantage les données de la table de travail si nécessaire.

[Découvrez comment orchestrer des activités de campagne](../orchestrate-activities.md)

## Exécution et reporting {#execution}

Lorsque la campagne s’exécute :

* Le fichier est traité au **moment de l’exécution**.

* Lignes acceptées de l’audience transmise aux activités en aval.

* Les lignes rejetées ou non rapprochées sont exclues ; les nombres et les raisons apparaissent dans le **journal d’exécution** (par exemple, nombre total de lignes chargées, lignes acceptées, lignes rejetées).

La résolution de l’audience est conçue pour se terminer en environ **60 secondes** pour un fichier CSV de 100 000 lignes **** dans une infrastructure de campagne orchestrée standard.

## Contenu connexe {#related}

* [Créer une dimension de ciblage](../target-dimension.md)
* [Activité Créer une audience](build-audience.md)
* [Activité Lecture d’audience](read-audience.md)
* [Activité Réconciliation](reconciliation.md)
* [Mécanismes de sécurisation et limitations](../guardrails.md)
