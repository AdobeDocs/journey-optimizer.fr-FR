---
title: Configurer une source de données
description: Découvrez comment configurer une source de données.
feature: Sources de données
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '705'
ht-degree: 100%

---

# Configuration d&#39;une source de données {#configure-data-source}

Les principales étapes de configuration d’une source de données sont les suivantes :

>[!NOTE]
>
>La configuration d’une source de données est toujours effectuée par un **utilisateur technique**.

1. Dans la section du menu ADMINISTRATION, sélectionnez **[!UICONTROL Configurations]**. Dans la section **[!UICONTROL Sources de données]**, cliquez sur **[!UICONTROL Gérer]**. La liste des sources de données s’affiche. Pour plus d&#39;informations sur l&#39;interface, voir [cette page](../user-interface.md)

   ![](../assets/journey18.png)

1. Ensuite, vous pouvez soit ajouter des groupes de champs à la source de données intégrée (voir [cette page](../datasource/adobe-experience-platform-data-source.md)), soit créer une source de données externe (voir [cette page](../datasource/external-data-sources.md)) et les groupes de champs associés (voir [cette page](../datasource/configure-data-sources.md#define-field-groups)).

   ![](../assets/journey23.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

   La source de données est maintenant configurée et prête à être utilisée dans vos parcours.

## Définir des groupes de champs {#define-field-groups}

Les groupes de champs sont des ensembles de champs que vous pouvez récupérer d’une source de données et utiliser dans un parcours.

Pour chaque source de données, vous pouvez définir plusieurs groupes de champs ayant chacun une durée de mise en cache spécifique.

Vous pouvez, par exemple, créer un groupe de champs avec le numéro de téléphone, l’adresse e-mail, le prénom et l’adresse du profil. Vous pourrez alors utiliser ces données dans votre parcours afin de créer des conditions. Par exemple, vous pouvez choisir de n’envoyer un SMS que si le numéro de téléphone du profil est renseigné. Si le champ est vide, vous pouvez envoyer un e-mail.

Bien qu’un nom par défaut soit automatiquement ajouté à votre groupe de champs, nous vous recommandons d’attribuer un nom personnalisé. En effet, ce nom sera visible par d’autres utilisateurs de [!DNL Journey Optimizer]. Il est conseillé d’attribuer au groupe un nom pertinent.

Lorsqu’un champ de source de données est utilisé dans un parcours, le système récupère tous ceux qui sont définis pour ce groupe. Par conséquent, il est recommandé de ne sélectionner que les champs dont vous avez besoin pour vos parcours. Cela permettra de réduire la latence des requêtes dans vos parcours et d’améliorer les performances. Notez que vous pourrez facilement ajouter d’autres champs dans les groupes ultérieurement.

La **[!UICONTROL durée de mise en cache]** est également un élément important, car elle contribue à l’optimisation des performances. Concrètement, cela signifie que dans le cadre d’un parcours, si des données d’un groupe de champs sont récupérées une fois, le système les met temporairement en cache. Si les mêmes données sont requises plus tard dans le même parcours, le système n’effectue aucune autre requête vers la source de données. La configuration de la durée de mise en cache doit être adaptée à chaque cas d’utilisation. Si vous devez récupérer des données en temps réel, telles que le statut d’une réservation d’hôtel, des informations météorologiques ou le nombre de points de fidélité, vous associerez le groupe contenant ces champs à une durée de mise en cache brève (1 seconde, par exemple). Pour les champs mis à jour moins souvent (nom, genre, etc.), vous créerez un deuxième groupe de champs avec une durée de mise en cache plus longue (5 jours, par exemple).

Le nombre de parcours qui font appel à un groupe de champs est affiché dans le champ **[!UICONTROL Utilisé(e) dans]**. Vous pouvez cliquer sur le bouton **[!UICONTROL Afficher les parcours]** pour faire apparaître la liste des parcours utilisant ce groupe de champs.

>[!NOTE]
>
>Notez que si un groupe ne contient aucun champ, il ne s’affiche pas dans l’éditeur d’expression.

![](../assets/journey3bis.png)

## Cycle de vie du groupe de champs {#field-group-lifecycle}

Vous pouvez ajouter des champs à un groupe qui n’est utilisé dans aucun parcours actif ou dans un état de brouillon, ou en supprimer.

Vous pouvez ajouter un champ à un groupe utilisé dans un ou plusieurs parcours actifs ou dans un état de brouillon, mais pas en supprimer. Cela permet d’éviter l’interruption des parcours.

Pour supprimer un champ d’un groupe utilisé dans un ou plusieurs parcours, procédez comme suit. Prenons l’exemple d’un groupe de champs appelé « Groupe de champs A ».

1. Dans la liste des groupes de champs, placez le curseur sur « Groupe de champs A » et cliquez ensuite sur l’icône **[!UICONTROL Dupliquer]** située à droite. Appelez le groupe de champs dupliqué « Groupe de champs B », par exemple.
1. Dans « Groupe de champs B », supprimez les champs dont vous n’avez plus besoin.
1. Dans « Groupe de champs A », vérifiez à quel emplacement ce groupe de champs est utilisé. Ces informations sont affichées dans le champ **[!UICONTROL Utilisé(e) dans]**.
1. Ouvrez tous les parcours qui utilisent « Groupe de champs A ».
1. Créez de nouvelles versions de chacun de ces parcours. Modifiez toutes les activités qui utilisent « Groupe de champs A » et sélectionnez « Groupe de champs B ».
1. Arrêtez les anciennes versions des parcours qui utilisent « Groupe de champs A ». Normalement, il ne devrait plus y avoir de parcours qui utilisent « Groupe de champs A ».
1. Supprimez « Groupe de champs A », car il n’est plus utilisé.
