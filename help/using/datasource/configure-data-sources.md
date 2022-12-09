---
solution: Journey Optimizer
product: journey optimizer
title: Configuration d’une source de données
description: Découvrez comment configurer une source de données
feature: Data Sources
topic: Administration
role: Admin
level: Intermediate
exl-id: 9b0dcffb-f543-4066-850c-67ec33f74a31
source-git-commit: f6db4f7cbb1951c009fa7915f340da96eea74120
workflow-type: tm+mt
source-wordcount: '554'
ht-degree: 0%

---

# Configuration d’une source de données {#configure-data-source}


>[!NOTE]
>
>La configuration de la source de données est toujours effectuée par une **utilisateur technique**.

Pour configurer une source de données, procédez comme suit :

1. Dans la section du menu ADMINISTRATION, sélectionnez **[!UICONTROL Configurations]**. Dans le  **[!UICONTROL Data Sources]** , cliquez sur **[!UICONTROL Manage]**. La liste des sources de données s’affiche. Voir [cette page](../start/user-interface.md) pour plus d’informations sur l’interface.

   ![](assets/journey18.png)

1. Vous pouvez ensuite ajouter des groupes de champs à la source de données intégrée (voir [cette page](../datasource/adobe-experience-platform-data-source.md)) ou créer une source de données externe (voir [cette page](../datasource/external-data-sources.md)) et les groupes de champs associés (voir [cette page](../datasource/configure-data-sources.md#define-field-groups)).

   ![](assets/journey23.png)

1. Cliquez sur **[!UICONTROL Save]**.

   La source de données est maintenant configurée et prête à être utilisée dans vos parcours.

## Définition de groupes de champs {#define-field-groups}

Les groupes de champs sont des ensembles de champs que vous pouvez récupérer d’une source de données et utiliser dans un parcours.

Pour chaque source de données, vous pouvez définir plusieurs groupes de champs.

Vous pouvez par exemple créer un groupe de champs avec le numéro de téléphone, l&#39;email, le prénom et l&#39;adresse du profil. Vous pourrez ensuite utiliser ces données dans votre parcours pour créer des conditions. Par exemple, vous pouvez décider d’envoyer une notification push uniquement si le client a installé l’application mobile. S’il est vide, vous pouvez envoyer un email.

Même si un nom par défaut est automatiquement ajouté, il est recommandé de donner un nom à votre groupe de champs. En effet, le nom du groupe de champs sera visible par d’autres utilisateurs dans [!DNL Journey Optimizer]. Il est recommandé d’attribuer un nom pertinent aux groupes de champs.

Lorsqu’un champ de source de données est utilisé dans un parcours, le système récupère tous les champs définis pour ce groupe de champs. Par conséquent, il est recommandé de ne sélectionner que les champs dont vous avez besoin pour vos parcours. Cela réduira la latence des requêtes dans vos parcours, ce qui augmentera les performances. Notez que vous pourrez facilement ajouter d’autres champs dans les groupes de champs ultérieurement.

Le nombre de parcours qui utilisent un groupe de champs s’affiche dans la variable **[!UICONTROL Used in]** champ . Vous pouvez cliquer sur le bouton **[!UICONTROL View journeys]** pour afficher la liste des parcours utilisant ce groupe de champs.

>[!NOTE]
>
>Notez que si un groupe de champs ne comporte pas de champ, il ne s’affiche pas dans l’éditeur d’expression.

![](assets/journey3bis.png)

## Cycle de vie du groupe de champs {#field-group-lifecycle}

Vous pouvez ajouter ou supprimer des champs d’un groupe de champs qui n’est utilisé dans aucun parcours actif ou dans un état de brouillon.

Vous pouvez ajouter un champ à un groupe utilisé dans un ou plusieurs parcours actifs ou dans un état de brouillon, mais pas le supprimer. Cela permet d’éviter de rompre les parcours.

Pour supprimer un champ d’un groupe utilisé dans un ou plusieurs parcours, procédez comme suit. Prenons l’exemple d’un groupe de champs nommé &quot;Groupe de champs A&quot;.

1. Dans la liste des groupes de champs, placez le curseur sur &quot;Groupe de champs A&quot; et cliquez sur le bouton **[!UICONTROL Duplicate]** située à droite. Nommez le groupe de champs dupliqué &quot;Groupe de champs B&quot;, par exemple.
1. Dans &quot;Groupe de champs B&quot;, supprimez les champs dont vous ne souhaitez plus.
1. Dans &quot;Groupe de champs A&quot;, vérifiez où ce groupe de champs est utilisé. Ces informations s’affichent dans la **[!UICONTROL Used in]** champ .
1. Ouvrez tous les parcours qui utilisent &quot;Groupe de champs A&quot;.
1. Créez de nouvelles versions de chacun de ces parcours. Modifiez toutes les activités utilisant &quot;Groupe de champs A&quot; et sélectionnez &quot;Groupe de champs B&quot;.
1. Arrêtez les anciennes versions des parcours qui utilisent &quot;Groupe de champs A&quot;. Vous ne devriez alors pas avoir de parcours utilisant &quot;Groupe de champs A&quot;.
1. Supprimez &quot;Groupe de champs A&quot;, car il n’est plus utilisé.
