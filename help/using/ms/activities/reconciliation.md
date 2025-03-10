---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Réconciliation
description: Découvrez comment utiliser l’activité Réconciliation dans une campagne à plusieurs étapes
hide: true
hidefromtoc: true
source-git-commit: dfa6c6e11db10f3e843035d32e322b212361548c
workflow-type: tm+mt
source-wordcount: '692'
ht-degree: 68%

---

# Réconciliation {#reconciliation}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation"
>title="Activité Réconciliation"
>abstract="L&#39;activité **Réconciliation** est une activité **Ciblage** qui permet de définir le lien entre Adobe Journey Optimizer et les données d&#39;une table de travail."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_field"
>title="Champ de sélection de la réconciliation"
>abstract="Champ de sélection de la réconciliation"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_condition"
>title="Condition de création de réconciliation"
>abstract="Condition de création de réconciliation"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_complement"
>title="Complément de génération de réconciliation"
>abstract="Complément de génération de réconciliation"

L&#39;activité **Réconciliation** est une activité de **Ciblage** qui permet de définir le lien entre les données de Adobe Journey Optimizer et les données d&#39;une table de travail, par exemple les données chargées depuis un fichier externe.

## Bonnes pratiques {#reconciliation-best-practices}

Si vous utilisez l’activité **Enrichissement** pour définir des données supplémentaires à traiter dans votre campagne à plusieurs étapes (vous pouvez utiliser une activité **Enrichissement** pour combiner des données provenant de plusieurs jeux ou pour créer des liens vers une ressource temporaire), l’activité **Réconciliation** vous permet de lier des données non identifiées à des ressources existantes.

>[!NOTE]
>L’opération de réconciliation suppose que les données des dimensions liées sont déjà présentes dans la base de données.  Par exemple, si vous importez un fichier d’achats indiquant quel produit a été acheté, à quelle heure, par quel client, etc., le produit ainsi que le client doivent déjà exister dans la base de données.

## Configurer l’activité Réconciliation {#reconciliation-configuration}

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting"
>title="Dimension de ciblage"
>abstract="Sélectionnez la nouvelle dimension de ciblage. Une dimension vous permet de définir la population ciblée : destinataires, personnes abonnées à l’application, opérateurs et opératrices, personnes eabonnés, etc. Par défaut, la dimension de ciblage actuelle est sélectionnée."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_rules"
>title="Règles de réconciliation"
>abstract="Sélectionnez les règles de réconciliation à utiliser pour la déduplication. Pour utiliser des attributs, sélectionnez l’option **Attributs simples** et choisissez les champs source et de destination. Pour créer votre propre condition de réconciliation à l’aide du concepteur de requête, sélectionnez l’option **Conditions de réconciliation avancées**."
>additional-url="https://experienceleague.adobe.com/fr/docs/campaign-web/v8/query-database/query-modeler-overview" text="Utiliser le concepteur de requête"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_targeting_selection"
>title="Sélectionner la dimension de ciblage"
>abstract="Sélectionnez la dimension de ciblage de vos données entrantes avec lesquelles vous souhaitez effectuer la réconciliation."
>additional-url="https://experienceleague.adobe.com/docs/campaign-web/v8/audiences/gs-audiences-recipients.html?lang=fr#targeting-dimensions" text="Dimensions de ciblage"

>[!CONTEXTUALHELP]
>id="ajo_orchestration_keep_unreconciled_data"
>title="Conserver les données non réconciliées"
>abstract="Par défaut, les données non réconciliées sont conservées dans la transition sortante et disponibles dans la table de travail pour une utilisation ultérieure. Pour supprimer les données non réconciliées, désactivez l’option **Conserver les données non réconciliées**."

>[!CONTEXTUALHELP]
>id="ajo_orchestration_reconciliation_attribute"
>title="Attribut de réconciliation"
>abstract="Sélectionnez l’attribut à utiliser pour réconcilier les données, puis cliquez sur Confirmer."

Pour configurer l’activité **Réconciliation**, procédez comme suit :

1. Ajoutez une activité **Réconciliation** dans votre campagne à plusieurs étapes.

1. Sélectionnez la nouvelle dimension de ciblage. Une dimension vous permet de définir la population ciblée : destinataires, abonnés de l’application, opérateurs, abonnés, etc.

1. Sélectionnez le ou les champs à utiliser pour la réconciliation. Vous pouvez utiliser un ou plusieurs critères de réconciliation.

   1. Pour utiliser des attributs afin de réconcilier des données, sélectionnez l’option **Attributs simples**. Le champ **Source** répertorie les champs disponibles dans la transition d’entrée, qui doivent être réconciliés. Le champ **Destination** correspond aux champs de la dimension de ciblage sélectionnée. Les données sont réconciliées lorsque la source et la destination sont égales. Par exemple, sélectionnez les champs **E-mail** pour dédupliquer des profils en fonction de leur adresse e-mail.

      Pour ajouter un autre critère de réconciliation, cliquez sur le bouton **Ajouter une règle**. Si plusieurs conditions de jointure sont indiquées, elles doivent TOUTES être vérifiées pour que le lien entre les données puisse se faire.

      ![](../assets/workflow-reconciliation-criteria.png)

   1. Pour utiliser d’autres attributs afin de réconcilier des données, sélectionnez l’option **Conditions avancées de réconciliation**. Vous pouvez ensuite créer votre propre condition de réconciliation à l&#39;aide du modéliseur de requêtes.

1. Vous pouvez filtrer les données à réconcilier à l’aide du bouton **Créer un filtre**. Vous pouvez ainsi créer une condition personnalisée à l’aide du concepteur de requête.

Par défaut, les données non réconciliées sont conservées dans la transition sortante et disponibles dans la table de travail pour une utilisation ultérieure. Pour supprimer les données non réconciliées, désactivez l’option **Conserver les données non réconciliées**.

## Exemple {#reconciliation-example}

L’exemple suivant illustre une campagne en plusieurs étapes qui crée une audience de profils directement à partir d’un fichier importé contenant de nouveaux clients. Il se compose des activités suivantes :

La campagne à plusieurs étapes est conçue comme suit :

![](../assets/workflow-reconciliation-sample-1.0.png)


Il est créé avec les activités suivantes :

* Une activité [Chargement de fichier](load-file.md) charge un fichier contenant les données de profil extraites d’un outil externe.

  Par exemple :

  ```
  lastname;firstname;email;birthdate;
  JACKMAN;Megan;megan.jackman@testmail.com;07/08/1975;
  PHILLIPS;Edward;phillips@testmail.com;09/03/1986;
  WEAVER;Justin;justin_w@testmail.com;11/15/1990;
  MARTIN;Babe;babeth_martin@testmail.net;11/25/1964;
  REESE;Richard;rreese@testmail.com;02/08/1987;
  ```

* Une activité **Réconciliation** qui identifie les données entrantes sous forme de profils, en utilisant les champs **E-mail** et **Date de naissance** comme critères de réconciliation.

  ![](../assets/workflow-reconciliation-sample-1.1.png)

* Une activité [Sauvegarde d’audience](save-audience.md) pour créer une audience à partir de ces mises à jour. Vous pouvez également remplacer l’activité **Sauvegarde d’audience** par une activité **Fin** si aucune audience spécifique ne doit être créée ou mise à jour. Les profils des destinataires sont mis à jour dans tous les cas lorsque vous exécutez la campagne à plusieurs étapes.

