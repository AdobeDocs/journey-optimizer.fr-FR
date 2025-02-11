---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main de la composition des audiences
description: En savoir plus sur la composition de l’audience
feature: Audiences, Profiles
topic: Content Management
role: User
level: Beginner
exl-id: af71d24d-77eb-44df-8216-b0aeaf4c4fa4
source-git-commit: 435898d7e806e93ee0154c3da22f6a011fc78175
workflow-type: tm+mt
source-wordcount: '681'
ht-degree: 89%

---

# Prise en main de la composition des audiences {#get-start-audience-composition}

>[!CONTEXTUALHELP]
>id="ajo_ao_create_composition"
>title="Créer une composition"
>abstract="Créez un workflow de composition afin de combiner les audiences d’Adobe Experience Platform existantes dans une zone de travail visuelle et d’exploiter diverses activités (telles que le partage, l’exclusion…) pour créer de nouvelles audiences."

>[!BEGINSHADEBOX]

Cette documentation fournit des informations détaillées sur l’utilisation de la composition d’audiences dans Adobe Journey Optimizer. Si vous êtes un client ou une cliente Profil client en temps réel uniquement et que vous n’utilisez pas Adobe Journey Optimizer, [cliquez ici](https://experienceleague.adobe.com/docs/experience-platform/segmentation/ui/audience-composition.html?lang=fr){target="_blank"}.

>[!ENDSHADEBOX]

La composition d’audiences vous permet de créer des **workflows de composition**, où vous pouvez combiner des audiences d’Adobe Experience Platform existantes en une zone de travail visuelle et exploiter diverses activités (telles que le partage, l’exclusion...) pour créer de nouvelles audiences.

Une fois cette opération terminée, les **audiences obtenues** sont enregistrées dans Adobe Experience Platform avec les audiences existantes et sont prêtes à être utilisées dans des campagnes Journey Optimizer pour cibler les clientes et les clients. Découvrez comment cibler des audiences dans Journey Optimizer
![](assets/audiences-process.png)

>[!IMPORTANT]
>
>L’utilisation des audiences et des attributs de la composition d’audiences est actuellement indisponible avec Healthcare Shield ou Privacy and Security Shield.
>
>Les attributs d’enrichissement ne sont pas encore intégrés au service d’application des politiques. Par conséquent, les libellés d’utilisation des données que vous appliquez à vos attributs d’enrichissement ne sont pas implémentés dans les campagnes et les parcours Journey Optimizer.

La composition de l’audience est accessible à partir du menu **[!UICONTROL Audiences]** d’Adobe Journey Optimizer :

![](assets/audiences-browse.png)

* L’onglet **[!UICONTROL Vue d’ensemble]** se compose d’un tableau de bord dédié avec des mesures clés liées aux données d’audience de votre organisation. Pour en savoir plus, consultez le [guide des tableaux de bord d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/dashboards/guides/segments.html?lang=fr).

* L’onglet **[!UICONTROL Parcourir]** répertorie toutes les audiences existantes stockées dans Adobe Experience Platform.

* L’onglet **[!UICONTROL Compositions]** vous permet de créer des workflows de composition dans lesquels vous pouvez combiner et organiser des audiences pour en créer de nouvelles.

## Créer un workflow de composition {#create}

Pour créer un workflow de composition, procédez comme suit :

1. Accédez au menu **[!UICONTROL Audiences]** et sélectionnez **[!UICONTROL Créer une audience]**.

1. Sélectionnez **[!UICONTROL Composer l’audience]**.

   ![](assets/audiences-create.png)

1. La zone de travail de composition s’affiche avec deux activités par défaut :

   * **[!UICONTROL Audience]** : le point de départ de votre composition. Cette activité permet de sélectionner une ou plusieurs audiences comme base de votre workflow,

   * **[!UICONTROL Enregistrer]** : la dernière étape de votre composition. Cette activité permet d&#39;enregistrer le résultat de votre workflow dans une nouvelle audience.

1. Ouvrez les propriétés de composition pour spécifier un titre et une description.

   Si aucun titre n’est défini dans les propriétés, le libellé de la composition comporte le terme « Composition », suivi de sa date et de son heure de création.

   ![](assets/audiences-properties.png)

1. Configurez votre composition en ajoutant autant d’activités que nécessaire entre les activités **[!UICONTROL Audience]** et **[!UICONTROL Enregistrer]**. Pour plus d’informations sur la création d’une composition, consultez la [documentation sur la composition d’audience](https://experienceleague.adobe.com/en/docs/experience-platform/segmentation/ui/audience-composition).

   ![](assets/audiences-publish.png)

1. Une fois votre composition prête, cliquez sur le bouton **[!UICONTROL Publier]** pour publier la composition et enregistrez les audiences obtenues dans Adobe Experience Platform.

   >[!IMPORTANT]
   >
   >Vous pouvez publier jusqu’à 10 compositions dans une sandbox donnée. Si vous avez atteint ce seuil, vous devez supprimer une composition pour libérer de l’espace et en publier une nouvelle.

   Si une erreur se produit lors de la publication, des alertes s’affichent avec des informations sur la façon de résoudre le problème.

   ![](assets/audiences-alerts.png)

1. La composition est publiée. Les audiences qui en résultent sont enregistrées dans Adobe Experience Platform et sont prêtes à être ciblées dans Journey Optimizer. [Découvrir comment cibler des audiences dans Journey Optimizer](../audience/about-audiences.md#segments-in-journey-optimizer)

>[!NOTE]
>
>Les audiences de **composition d’audience** sont exécutées quotidiennement. Vous devrez peut-être donc attendre jusqu’à 24 heures pour les utiliser dans Journey Optimizer. Les attributs enrichis des audiences de composition d’audience sont aussi récents que la dernière exécution de composition, qui peut durer jusqu’à 24 heures.

## Accéder aux compositions {#access}

>[!CONTEXTUALHELP]
>id="ajo_ao_publish"
>title="Publier votre audience"
>abstract="Publiez votre composition pour enregistrer les audiences obtenues dans Adobe Experience Platform."

Toutes les compositions créées sont accessibles à partir de l’onglet **[!UICONTROL Compositions]** . Vous pouvez dupliquer ou supprimer une composition existante à tout moment à l’aide du bouton représentant des points de suspension dans la liste.

Les compositions peuvent avoir plusieurs statuts :

* **[!UICONTROL Brouillon]** : la composition est en cours et n’a pas été publiée.
* **[!UICONTROL Publié]** : la composition a été publiée, les audiences qui en résultent ont été enregistrées et peuvent être utilisées.

![](assets/audiences-compositions.png)

>[!NOTE]
>
>La composition de l’audience n’est actuellement pas intégrée à la fonctionnalité de réinitialisation des sandbox. Avant de réinitialiser un sandbox, vous devez supprimer vos compositions manuellement pour vous assurer que les données d’audience associées sont correctement nettoyées. Des informations détaillées sont disponibles dans la [documentation sur les sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=fr#delete-audience-compositions) d’Adobe Experience Platform.
