---
title: Utilisation d’un segment dans un parcours
description: Découvrez comment utiliser un segment dans un parcours
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '968'
ht-degree: 0%

---

# Utiliser un segment dans un parcours {#segment-trigger-activity}

![](../assets/do-not-localize/badge.png)

## À propos de l&#39;activité de segment de lecture {#about-segment-trigger-actvitiy}

L’activité Lire le segment vous permet de faire entrer un parcours à toutes les personnes appartenant à un segment Adobe Experience Platform. L&#39;entrée dans un parcours peut être effectuée une seule fois ou régulièrement.

Prenons l’exemple du segment &quot;Ouverture et passage en caisse de l’application Luma&quot; créé dans le cas d’utilisation de [Créer des segments](../segment/about-segments.md). Avec l’activité Lire le segment, vous pouvez faire entrer toutes les personnes appartenant à ce segment dans un parcours et les faire s’enchaîner dans des parcours personnalisés qui exploiteront toutes les fonctionnalités de parcours : conditions, minuteries, événements, actions.

>[!NOTE]
>
>Il n’est pas possible de déclencher un parcours basé sur un segment dans une période plus courte que 1 heure.

### Configuration de l’activité {#configuring-segment-trigger-activity}

Les étapes de configuration de l’activité de segment Lu sont les suivantes :

1. Dépliez la catégorie **[!UICONTROL Orchestration]** et déposez une activité **[!UICONTROL Lire le segment]** dans votre canevas.

   L&#39;activité doit être positionnée comme la première étape d&#39;un parcours.

1. Ajoutez une **[!UICONTROL étiquette]** à l&#39;activité (facultatif).

1. Dans le champ **[!UICONTROL Segment]**, sélectionnez le segment Adobe Experience Platform qui va entrer dans le parcours, puis cliquez sur **[!UICONTROL Enregistrer]**.

   Notez que vous pouvez personnaliser les colonnes affichées dans la liste et les trier.

   >[!NOTE]
   >
   >Seuls les individus présentant les états de participation **Réalisés** et **Existants** entrent dans le parcours. Pour plus d’informations sur l’évaluation d’un segment, consultez la [documentation du service de segmentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=en#interpret-segment-results).

   ![](../assets/read-segment-selection.png)

   Une fois le segment ajouté, le bouton **[!UICONTROL Copier]** permet de copier son nom et son ID :

   `{"name":"Luma app opening and checkout",”id":"8597c5dc-70e3-4b05-8fb9-7e938f5c07a3"}`

   ![](../assets/read-segment-copy.png)

1. Dans le champ **[!UICONTROL Espace de nommage]**, choisissez l’espace de nommage à utiliser pour identifier les individus. [En savoir plus sur les espaces de nommage](../event/about-creating.md#select-the-namespace).

   >[!NOTE]
   >
   >Les personnes appartenant à un segment qui n&#39;a pas l&#39;identité sélectionnée (espace de nommage) parmi leurs différentes identités ne peuvent pas entrer dans le parcours.

1. L&#39;activité **[!UICONTROL Lire le segment]** vous permet de spécifier l&#39;heure à laquelle le segment va entrer dans le parcours. Pour ce faire, cliquez sur le lien **[!UICONTROL Modifier la planification du parcours]** pour accéder aux propriétés du parcours, puis configurez le champ **[!UICONTROL type de Planificateur]**.

   ![](../assets/read-segment-schedule.png)

   Par défaut, les segments entrent dans le parcours **[!UICONTROL Dès que possible]**, ce qui signifie 1 heure après la publication du parcours. Si vous souhaitez que le segment entre dans le parcours à une date/heure spécifique ou sur une base récurrente, sélectionnez la valeur souhaitée dans la liste.

   >[!NOTE]
   >
   >Notez que la section **[!UICONTROL Planification]** n&#39;est disponible que lorsqu&#39;une activité **[!UICONTROL Lire le segment]** a été supprimée dans le canevas.

   ![](../assets/read-segment-schedule-list.png)

### Tester et publier le parcours {#testing-publishing}

L&#39;activité **[!UICONTROL Lire le segment]** vous permet de tester le parcours soit sur un profil unitaire, soit sur 100 profils de test aléatoire sélectionnés parmi les profils qualifiés pour le segment.

Pour ce faire, activez le mode de test, puis sélectionnez l’option de votre choix dans le volet de gauche.

![](../assets/read-segment-test-mode.png)

Vous pouvez ensuite configurer et exécuter le mode de test comme vous le faites habituellement. [Apprenez à tester un parcours](testing-the-journey.md).

Une fois le test en cours d’exécution, le bouton **[!UICONTROL Afficher les journaux]** permet d’afficher les résultats du test en fonction de l’option de test sélectionnée :

* **[!UICONTROL Profil unique à la fois]** : les journaux de test affichent les mêmes informations que lors de l’utilisation du mode de test unitaire. Pour plus d&#39;informations à ce sujet, reportez-vous à [cette section](testing-the-journey.md#viewing_logs)

* **[!UICONTROL Jusqu&#39;à 100 profils à la fois]** : les journaux de test vous permettent de suivre la progression de l’exportation de segments à partir de Adobe Experience Platform, ainsi que la progression individuelle de toutes les personnes qui sont entrées sur le parcours.

   Notez que le test du parcours en utilisant jusqu’à 100 profils à la fois ne vous permet pas de suivre la progression des individus dans le parcours à l’aide du flux visuel.

   ![](../assets/read-segment-log.png)

Une fois les tests réussis, vous pouvez publier votre parcours (voir [Publication du parcours](publishing-the-journey.md)). Les personnes appartenant au segment entrent le parcours à la date et à l’heure spécifiées dans la section des propriétés du parcours **[!UICONTROL Planificateur]**.

>[!NOTE]
>
>Lorsqu’un parcours basé sur un segment qui n’est pas récurrent (&quot;en commençant dès que possible&quot; ou &quot;une fois&quot;) est exécuté, son état devient automatiquement &quot;fermé&quot;.
>
>Pour les parcours récurrents basés sur des segments, le parcours se ferme automatiquement une fois sa dernière occurrence exécutée. Si aucune date/heure de fin n&#39;a été spécifiée, vous devrez fermer manuellement le parcours à de nouvelles entrées pour le terminer.


## Ciblage des Audiences dans les parcours par segment

Les parcours basés sur les segments sont toujours débuts avec une activité **Lire le segment** pour récupérer les individus appartenant à un segment Adobe Experience Platform.

L’audience appartenant au segment est récupérée une fois ou régulièrement.

Une fois le parcours entré, vous pouvez créer des cas d’utilisation de l’orchestration des audiences, ce qui permet aux individus du segment initial de s’écouler dans différentes branches du parcours.

**Segmentation**

Vous pouvez utiliser des conditions pour effectuer la segmentation à l’aide de l’activité **Condition**. Vous pouvez, par exemple, faire en sorte que VIP personnes empruntent un chemin particulier et qu’elles ne suivent pas VIP flux dans un autre chemin.

La segmentation peut être basée sur :

* données de source de données
* le contexte des événements faisant partie des données du parcours, par exemple : est-ce qu&#39;une personne a cliqué sur le message qu&#39;elle a reçu il y a une heure ?
* une date, par exemple : sommes-nous en juin lorsqu&#39;une personne traverse le parcours?
* une heure, par exemple : est-ce le matin dans le fuseau horaire de la personne?
* un algorithme fractionnant l’audience circulant dans le parcours en fonction d’un pourcentage, par exemple : 90 à 10 % pour exclure une Population témoin

![](../assets/read-segment-audience1.png)

**Exclusion**

La même activité **Condition** utilisée pour la segmentation (voir ci-dessus) vous permet également d’exclure une partie de la population. Par exemple, vous pouvez exclure VIP personnes en les faisant glisser dans une branche avec une étape de fin juste après.

Cette exclusion peut se produire juste après la récupération des segments, à des fins de comptage de population ou le long d’un parcours à plusieurs étapes.

![](../assets/read-segment-audience2.png)

**Union**

Les parcours vous permettent de créer des branches N et de les associer après une segmentation.

Par conséquent, vous pouvez faire en sorte que deux audiences reviennent à une expérience commune.

Par exemple, après avoir suivi une expérience différente pendant dix jours dans un parcours, les clients VIP et non VIP peuvent revenir au même chemin.

Après une union, vous pouvez fractionner à nouveau l’audience en exécutant une segmentation ou une exclusion.

![](../assets/read-segment-audience3.png)
