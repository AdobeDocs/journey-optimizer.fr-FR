---
solution: Journey Optimizer
product: journey optimizer
title: Créer votre premier workflow de composition
description: Découvrez comment créer des workflows de composition pour combiner et organiser des audiences existantes.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
source-git-commit: f924af0e1baadabb97167f42457b1b419256fa8c
workflow-type: tm+mt
source-wordcount: '409'
ht-degree: 89%

---

# Créer votre premier workflow de composition {#create-compositions}

>[!BEGINSHADEBOX]

Cette documentation fournit des informations détaillées sur l’utilisation de la composition d’audiences dans Adobe Journey Optimizer. Si vous n’utilisez pas Adobe Journey Optimizer, [cliquez ici](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html)

>[!ENDSHADEBOX]

## Créer un workflow de composition {#create}

Pour créer un workflow de composition, procédez comme suit :

1. Accédez au **[!UICONTROL Audiences]** et sélectionnez **[!UICONTROL Création d’une audience]**.

1. Sélectionnez **[!UICONTROL Composer l’audience]**.

   ![](assets/audiences-create.png)

   >[!NOTE]
   >
   >La méthode de création **[!UICONTROL Créer une règle]** vous permet de créer une définition de nouveau segment à l’aide de la méthode [Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=fr).

1. La zone de travail de composition s’affiche avec deux activités par défaut :

   * **[!UICONTROL Audience]** : le point de départ de votre composition. Cette activité permet de sélectionner une ou plusieurs audiences comme base de votre workflow,

   * **[!UICONTROL Enregistrer]** : la dernière étape de votre composition. Cette activité permet d&#39;enregistrer le résultat de votre workflow dans une nouvelle audience.

   Pour plus d’informations sur la configuration des activités dans la zone de travail du workflow de composition, reportez-vous à la section [Utiliser la zone de travail de composition](composition-canvas.md).

1. Ouvrez les propriétés de composition pour spécifier un titre et une description.

   Si aucun titre n’est défini dans les propriétés, le libellé de la composition comporte le terme « Composition », suivi de sa date et de son heure de création.

   ![](assets/audiences-properties.png)

1. Configurez votre composition en ajoutant autant d’activités que nécessaire entre les activités **[!UICONTROL Audience]** et **[!UICONTROL Enregistrer]**. [Découvrez comment utiliser la zone de travail de composition](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. Une fois votre composition prête, cliquez sur le bouton **[!UICONTROL Publier]** pour publier la composition et enregistrez les audiences obtenues dans Adobe Experience Platform.

   >[!IMPORTANT]
   >
   >Vous pouvez publier jusqu’à 10 compositions dans une sandbox donnée. Si vous avez atteint ce seuil, vous devez supprimer une composition pour libérer de l’espace et en publier une nouvelle.

   Si une erreur se produit lors de la publication, des alertes s’affichent avec des informations sur la façon de résoudre le problème.

   ![](assets/audiences-alerts.png)

1. La composition est publiée. Les audiences qui en résultent sont enregistrées dans Adobe Experience Platform et sont prêtes à être ciblées dans les campagnes Journey Optimizer. [Découvrez comment utiliser les campagnes](../campaigns/get-started-with-campaigns.md)

## Accéder aux compositions {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Publier votre audience"
>abstract="Publiez votre composition pour enregistrer les audiences obtenues dans Adobe Experience Platform."

Toutes les compositions créées sont accessibles à partir de l’onglet **[!UICONTROL Compositions]** . Elles peuvent avoir plusieurs statuts :

* **[!UICONTROL Brouillon]** : la composition est en cours et n’a pas été publiée.
* **[!UICONTROL Publié]** : la composition a été publiée, les audiences qui en résultent ont été enregistrées et peuvent être utilisées.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>Vous pouvez dupliquer ou supprimer une composition existante à tout moment à l’aide du bouton représentant des points de suspension dans la liste.
