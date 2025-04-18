---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’activité Mettre à jour les données dans vos campagnes orchestrées
description: Découvrez comment utiliser l’activité Mettre à jour les données .
badge: label="Alpha"
hide: true
hidefromtoc: true
exl-id: 68e7c929-5f07-4d5a-9831-690e071947f8
source-git-commit: bdc584c1aae0c735d81dfc95e11f96f755bea26a
workflow-type: tm+mt
source-wordcount: '504'
ht-degree: 74%

---

# Mettre à jour les données {#update-data}

L’activité **Mise à jour de données** est une activité de **Gestion des données**. L’activité Mise à jour de données permet de mettre à jour en masse les champs de la base de données. Plusieurs options vous permettent de personnaliser la mise à jour des données.

<!--
The **Operation type** field lets you choose the process to be carried out on the data in the database. Select the first option to add data or update (it if it has already been added). You can also only add data, only update data, or delete data. Select the **Update and merge collections** to select a primary record to link duplicates to, and delete those duplicates safely

Specify how to identify the records in the database: if data relate to an existing targeting dimension, select the **Using the targeting dimension** option and select the targeting dimension and fields to update. Otherwise, specify one or more custom links to identify the data in the database, or direct use of reconciliation keys.

Select the fields to update and reconciliation settings. You can use the **Auto-mapping** option to automatically identify the fields to be updated.

The **Advanced options** section let you specify additional settings to manage data and duplicates.

Toggle the **Generate an outbound transition** option to add an outbound transition that will be activated at the end of the execution of the **Update data** activity. The update generally marks the end of a targeting workflow and therefore the option is not activated by default.

Toggle the **Generate an outbound transition for rejects** option to add an outbound transition containing records that have not been correctly processed after the update (for example if there is a duplicate). The update generally marks the end of a targeting workflow and therefore the option is not activated by default.
-->

## Configurer l’activité Mise à jour de données{#update-data-configuration}

Pour configurer l’activité **Mise à jour de données**, commencez par ajouter l’activité à votre campagne orchestrée et définissez un libellé.

![](../assets/workflow-update-data.png)

### Type d&#39;opération

Le champ **Type d&#39;opération** permet de choisir le traitement à réaliser sur les données de la base de données :

* **Insérer ou mettre à jour** : insérez des données ou mettez-les à jour si des enregistrements existent déjà dans la base de données.
* **Insérer** : insérez des données uniquement. Les enregistrements qui existent déjà ne sont pas mis à jour. Si des critères de réconciliation sont définis, seuls les enregistrements non rapprochés seront ajoutés.
* **Mettre à jour** : mettre à jour des données des enregistrements déjà présents en base uniquement.
* **Supprimer** : supprimer des données.

Le champ **Taille des mises à jours** permet de sélectionner le nombre d&#39;éléments de la transition entrante qui seront mis à jour. Par exemple, si vous indiquez 500, les 500 premiers enregistrements traités seront mis à jour.

### Identification des enregistrements

Cette section vous permet de définir comment identifier les enregistrements dans la base de données :

* Si les données saisies correspondent à une dimension de ciblage existante, sélectionnez l’option **Utiliser la dimension de ciblage** et sélectionnez-la dans le champ **Dimension de ciblage à mettre à jour**.
* Vous pouvez également sélectionner **Utiliser des liens personnalisés** et spécifier un ou plusieurs liens qui permettront d’identifier les données de la base de données.
* Si le type d’opération sélectionné implique une mise à jour, vous devez obligatoirement utiliser l’option **Utiliser des règles de réconciliation**.

### Champs à mettre à jour

Dans l’onglet **Champs à mettre à jour**, ajoutez les champs sur lesquels appliquer la mise à jour et, au besoin, ajoutez des conditions pour que cette mise à jour soit réalisée. Pour cela, utilisez le champ **Pris en compte si** Les conditions sont appliquées l’une après l’autre dans l’ordre des listes. Utilisez les flèches situées à droite pour modifier l’ordre des mises à jour. Vous pouvez utiliser le même champ de destination plusieurs fois.

Vous pouvez associer automatiquement les champs à l’aide du bouton **Mappage automatique**. L’association automatique détecte les champs portant le même nom.

Dans le cadre d’une opération de type **Insérer ou mettre à jour**, vous pouvez sélectionner individuellement, pour chaque champ, l’opération à appliquer. Pour cela, sélectionnez la valeur souhaitée dans le champ **Type d’opération**.

### Options avancées

Les **options avancées** permettent de spécifier des options supplémentaires pour le traitement des données mises à jour ainsi que pour la gestion des doublons.

<!--
* **Disable automatic key management**
* **Disable audit**
* **Empty the destination value if the source value is empty**
* **Update all columns with matching names**
* **Ignore records which concern the same target**: only the first in the list of expressions will be considered
-->

Les deux dernières options permettent d’effectuer des actions spécifiques :

* **Générer une transition sortante** : crée une transition sortante qui sera activée à la fin de l’exécution. La mise à jour marque généralement la fin d’une campagne orchestrée de ciblage. Par conséquent, l’option n’est pas activée par défaut.

* **Générer une transition sortante pour les rejets** : créé une transition sortante qui contient les enregistrements qui n’ont pas été correctement traités après la mise à jour (par exemple en cas de doublon). La mise à jour marque généralement la fin d’une campagne de ciblage orchestrée. Par conséquent, l’option n’est pas activée par défaut.
