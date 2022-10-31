---
solution: Journey Optimizer
product: journey optimizer
title: Créer des workflows de composition
description: Découvrez comment créer des workflows de composition pour combiner et organiser des audiences existantes.
feature: Journeys
topic: Content Management
role: User
level: Intermediate
hide: true
hidefromtoc: true
source-git-commit: 2160d52f24af50417cdcf8c6ec553b746a544c2f
workflow-type: tm+mt
source-wordcount: '352'
ht-degree: 93%

---

# Créer des workflows de composition {#create-compositions}

Les workflows de composition vous permettent de combiner et d’organiser des audiences existantes pour créer de nouvelles audiences.

## Créer un workflow de composition {#create}

1. Accédez au menu **[!UICONTROL Segments]** et sélectionnez **[!UICONTROL Créer une audience]**.

1. Sélectionnez **[!UICONTROL Composer l’audience]**.

   >[!NOTE]
   >
   >La méthode de création **[!UICONTROL Créer une règle]** vous permet de créer une définition de nouveau segment à l’aide de la méthode [Segmentation Service](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/overview.html?lang=fr).

   ![](assets/audiences-create.png)

1. La zone de travail de composition s’affiche avec deux activités par défaut :

   * **[!UICONTROL Audience]** : le point de départ de votre composition. Cette activité permet de sélectionner une ou plusieurs audiences comme base de votre workflow,

   * **[!UICONTROL Enregistrer]** : la dernière étape de votre composition. Cette activité permet d&#39;enregistrer le résultat de votre workflow dans une nouvelle audience.
   Pour plus d’informations sur la configuration des activités dans la zone de travail du workflow de composition, reportez-vous à la section [Utiliser la zone de travail de composition](composition-canvas.md).

1. Sélectionnez l’activité **[!UICONTROL Audience]** puis spécifiez un libellé pour votre composition.

   >[!IMPORTANT]
   >
   >Le libellé de l’activité **[!UICONTROL Audience]** est le libellé de votre composition. Veillez à fournir un nom significatif pour récupérer plus facilement la composition dans la liste.

   ![](assets/audiences-new-composition.png)

1. Configurez votre composition en ajoutant autant d’activités que nécessaire entre les activités **[!UICONTROL Audience]** et **[!UICONTROL Enregistrer]**. [Découvrez comment utiliser la zone de travail de composition](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. Une fois votre composition prête, cliquez sur le bouton **[!UICONTROL Publier]** pour publier la composition et enregistrer les audiences obtenues dans Adobe Experience Platform.

   Si une erreur se produit lors de la publication, des alertes s’affichent avec des informations sur la façon de résoudre le problème.

   ![](assets/audiences-alerts.png)

1. La composition est publiée. Les audiences obtenues sont enregistrées dans Adobe Experience Platform. <!-- and are ready to be targeted in Journey Optimizer campaigns. [Get started with campaigns](../campaigns/get-started-with-campaigns.md)-->

## Accéder aux compositions {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Publier votre audience"
>abstract="Publiez votre composition pour enregistrer les audiences obtenues dans Adobe Experience Platform."

Toutes les compositions créées sont accessibles à partir de l’onglet **[!UICONTROL Compositions]** . Elles peuvent avoir plusieurs statuts :

* **[!UICONTROL Brouillon]** : la composition est en cours et n’a pas été publiée.
* **[!UICONTROL Publiée]** : la composition a été publiée, les audiences obtenues ont été enregistrées. <!-- and are available for use.-->
* **[!UICONTROL Archivée]** : la composition a été archivée.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>Vous pouvez dupliquer ou supprimer une composition existante à tout moment à l’aide du bouton des points de suspension dans la liste.

En savoir plus :

* [Prise en main de la composition des audiences](get-started-audience-orchestration.md)
* [Utiliser la zone de travail de composition](composition-canvas.md)
* [Accéder aux audiences et les gérer](access-audiences.md)
