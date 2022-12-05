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
exl-id: 8b978900-fcef-46f2-bc19-70776e4f3d43
source-git-commit: 8d56e3060e78422b028ced17f415497789908ff9
workflow-type: ht
source-wordcount: '367'
ht-degree: 100%

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

1. Ouvrez les propriétés de composition pour spécifier un titre et une description.

   Si aucun titre n’est défini dans les propriétés, le libellé de composition est celui de l’activité **[!UICONTROL Audience]** qui débute.

   ![](assets/audiences-properties.png)

1. Configurez votre composition en ajoutant autant d’activités que nécessaire entre les activités **[!UICONTROL Audience]** et **[!UICONTROL Enregistrer]**. [Découvrez comment utiliser la zone de travail de composition](composition-canvas.md)

   ![](assets/audiences-publish.png)

1. Une fois votre composition prête, cliquez sur le bouton **[!UICONTROL Publier]** pour publier la composition et enregistrez les audiences obtenues dans Adobe Experience Platform.

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
* **[!UICONTROL Archivée]** : la composition a été archivée.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>Vous pouvez dupliquer ou supprimer une composition existante à tout moment à l’aide du bouton des points de suspension dans la liste.

En savoir plus :

* [Prise en main de la composition des audiences](get-started-audience-orchestration.md)
* [Utiliser la zone de travail de composition](composition-canvas.md)
* [Accéder aux audiences et les gérer](access-audiences.md)
