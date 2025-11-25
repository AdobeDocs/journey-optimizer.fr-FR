---
solution: Journey Optimizer
product: journey optimizer
title: Activité de condition
description: En savoir plus sur l’activité de condition
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
keywords: activité, condition, zone de travail, parcours
hidefromtoc: true
hide: true
exl-id: 496c7666-a133-4aeb-be8e-c37b3b9bf5f9
version: Journey Orchestration
source-git-commit: 7822e9662d03e6c6b2d5bc5ecb9ca85dc32f0942
workflow-type: ht
source-wordcount: '1696'
ht-degree: 100%

---

# Conditions {#conditions}

>[!CONTEXTUALHELP]
>id="ajo_journey_conditions"
>title="Conditions"
>abstract="L’activité Condition permet de définir la progression des personnes dans votre parcours en créant plusieurs chemins basés sur des critères spécifiques. Vous pouvez également configurer un autre chemin pour gérer les temporisations ou les erreurs, assurant ainsi une expérience fluide."

Les **conditions** vous permettent de définir la progression des individus dans votre parcours en créant plusieurs chemins basés sur des critères spécifiques. Vous pouvez également configurer un autre chemin pour gérer les temporisations ou les erreurs, assurant ainsi une expérience fluide.

>[!AVAILABILITY]
>
>Ces conditions sont disponibles par le biais de l’activité **Optimiser**, accessible à la demande en disponibilité limitée. Contactez votre représentant ou représentante Adobe pour en obtenir l’accès.
>
>Si vous n’avez pas accès à cette fonctionnalité, vous pouvez tout de même utiliser l’ancienne [activité Condition](condition-activity.md).

## Ajouter une condition {#add-condition-activity}

Pour ajouter une condition à votre parcours, procédez comme suit :

1. Déposez l’activité **[!UICONTROL Optimiser]** dans la zone de travail du parcours. [En savoir plus](optimize.md)

1. Ajoutez un libellé facultatif pour identifier l’activité dans les journaux de mode de test et les rapports.

1. Sélectionnez une condition dans la liste déroulante **[!UICONTROL Méthode]**.

   ![Activité Optimiser avec la méthode Condition sélectionnée](assets/journey-optimize-condition.png){width=80%}

   Les types de condition disponibles sont les suivants :

   * [Condition de source de données](#data_source_condition)
   * [Condition de temps](#time_condition)
   * [Partage en pourcentage](#percentage_split)
   * [Condition de date](#date_condition)
   * [Limite de profils](#profile_cap)
   * Vous pouvez également utiliser une audience dans une condition de parcours. [En savoir plus](#using-a-segment)

## Gérer les chemins des conditions {#condition_paths}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_simple2"
>title="À propos de l&#39;éditeur d&#39;expression simple"
>abstract="Le mode Éditeur d&#39;expression simple vous permet d&#39;exécuter des requêtes simples en fonction d&#39;une combinaison de champs. Tous les champs disponibles s’affichent dans la partie gauche de l’écran. Faites glisser des champs dans la zone principale. Pour combiner les différents éléments, imbriquez-les afin de créer différents groupes et/ou niveaux de groupes. Vous pouvez alors sélectionner un opérateur logique afin de combiner les éléments de même niveau."

Lorsque vous utilisez plusieurs conditions dans un parcours, vous pouvez définir des libellés pour chacune d’elles afin de les identifier plus facilement.

Cliquez sur **[!UICONTROL Ajouter un chemin]** si vous souhaitez définir plusieurs conditions. Pour chaque condition, un nouveau chemin est ajouté dans la zone de travail après l’activité.

![Bouton Ajouter un chemin pour créer plusieurs chemins de condition](assets/journey-condition-add-path.png){width=80%}

Notez que la conception de parcours n’est pas sans conséquences sur le plan fonctionnel. Lorsque plusieurs chemins sont définis après une condition, seul le premier chemin éligible est exécuté. Cela signifie que vous pouvez modifier la priorité des chemins en les plaçant les uns au-dessus ou en dessous des autres.

Prenons l’exemple de la condition « La personne est un VIP » d’un premier chemin et la condition « La personne est un homme » d’un second chemin. Si une personne répondant aux deux conditions (à savoir, un VIP de sexe masculin) franchit cette étape, le premier chemin d’accès est choisi, même s’il est également éligible au second, compte tenu de sa position hiérarchique supérieure. Pour modifier cette priorité, déplacez vos activités verticalement.

![Exemple de hiérarchisation des chemins affichant la condition VIP au-dessus de la condition Homme](assets/journey48.png)

Vous pouvez créer un autre chemin pour les audiences qui ne sont pas éligibles aux conditions définies en cochant la case **[!UICONTROL Afficher le chemin pour d’autres cas que celui ou ceux ci-dessus]**.

>[!NOTE]
>
>Cette option n’est pas disponible dans les conditions de partage. [En savoir plus](#percentage_split)

Le mode simple vous permet d’exécuter des requêtes simples en fonction d’une combinaison de champs. Tous les champs disponibles s’affichent dans la partie gauche de l’écran. Faites glisser des champs dans la zone principale. Pour combiner les différents éléments, imbriquez-les afin de créer différents groupes et/ou niveaux de groupes. Vous pouvez alors sélectionner un opérateur logique afin de combiner les éléments de même niveau :

* **ET** : intersection de deux critères. Seuls les éléments répondant à tous les critères sont pris en compte.
* **OU** : union de deux critères. Les éléments répondant à au moins l’un des deux critères sont pris en compte.

![Éditeur d’expression simple avec des champs de type glisser-déposer et des opérateurs logiques](assets/journey64.png){width=80%}

Si vous utilisez le [service de segmentation d’Adobe Experience Platform](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=fr){target="_blank"} pour créer vos audiences, vous pouvez les utiliser dans vos conditions de parcours. Pour plus d’informations, consultez la section [Utilisation d’audiences dans des conditions](../building-journeys/condition-activity.md#using-a-segment).

>[!NOTE]
>
>Vous ne pouvez pas effectuer de requêtes sur des séries temporelles (une liste d’achats ou des clics précédents sur des messages, par exemple) à l’aide de l’éditeur simple. Pour cela, vous devez utiliser l’éditeur avancé. Voir [cette page](expression/expressionadvanced.md).

Lorsqu’une erreur se produit dans une action ou une condition, le parcours d’une personne s’arrête. La seule façon de le faire continuer est de cocher la case **[!UICONTROL Ajouter un chemin alternatif en cas de temporisation ou d’erreur]**. [En savoir plus](../building-journeys/using-the-journey-designer.md#paths)

Dans l’éditeur simple, vous trouverez la catégorie Propriétés du parcours, sous les catégories d’événement et de source de données. Cette catégorie contient des champs techniques liés au parcours d’un profil donné. Il s’agit des informations récupérées par le système à partir de parcours dynamiques, telles que l’identifiant du parcours ou les erreurs spécifiques rencontrées. [En savoir plus](expression/journey-properties.md)

## Condition de source de données {#data_source_condition}

Utilisez une **[!UICONTROL condition de source de données]** pour définir une condition en fonction de champs issus des sources de données ou des événements positionnés précédemment dans le parcours. Ce type de condition est défini à l’aide de l’éditeur d’expression. [En savoir plus sur l’utilisation de l’éditeur d’expression](expression/expressionadvanced.md)

Par exemple, si vous ciblez une audience avec des attributs d’enrichissement générés à l’aide d’un workflow de composition ou d’un chargement personnalisé (fichier CSV), vous pouvez utiliser ces attributs d’enrichissement pour créer votre condition.

L’éditeur d’expression avancé vous permet de configurer des conditions plus sophistiquées pour manipuler des collections ou utiliser des sources de données nécessitant la transmission de paramètres. [En savoir plus](../datasource/external-data-sources.md)

![Condition de source de données avec éditeur d’expression avancé](assets/journey50.png){width=80%}

## Condition de date {#date_condition}

Cette condition vous permet de définir un flux différent en fonction de la date. Par exemple, si la personne accède à l’étape pendant la période de soldes, vous lui enverrez un message spécifique. Le reste de l’année, vous lui enverrez un autre message.

>[!NOTE]
>
>Le fuseau horaire n’est plus spécifique à une condition et est maintenant défini au niveau du parcours dans les propriétés de celui-ci. [En savoir plus](../building-journeys/timezone-management.md)

![Configuration de la condition de date avec les champs de date de début et de fin](assets/journey53.png)

## Partage en pourcentage {#percentage_split}

Cette option vous permet de fractionner l’audience de manière aléatoire afin de définir une action différente pour chaque groupe. Définissez le nombre de divisions, ainsi que la répartition pour chaque chemin. La division est un calcul statistique, dans la mesure où le système ne peut pas prévoir le nombre de personnes qui suivront cette activité du parcours. Par conséquent, la marge d’erreur de la division est très faible. Cette fonction est basée sur un [mécanisme Java aléatoire](https://docs.oracle.com/javase/7/docs/api/java/util/Random.html){target="_blank"}.

En mode test, lorsqu&#39;un partage est atteint, la branche supérieure est toujours choisie. Vous pouvez réorganiser la position des branches partagées si vous souhaitez que le test choisisse un autre chemin. [En savoir plus](../building-journeys/testing-the-journey.md)

>[!NOTE]
>
>Notez qu’il n’existe aucun bouton permettant d’ajouter un chemin dans la condition de division en pourcentage. Le nombre de chemins dépend du nombre de divisions. Dans les conditions de division, vous ne pouvez pas ajouter de chemin pour d’autres cas, car cela ne peut pas se produire. Les utilisateurs se trouveront toujours dans l’un des chemins de division.

![Configuration Partage en pourcentage avec un curseur affichant la répartition du trafic](assets/journey52.png)

## Condition de temps {#time_condition}

Utilisez une **[!UICONTROL Condition de temps]** pour effectuer des actions différentes en fonction de l’heure du jour et/ou du jour de la semaine. Par exemple, les jours de semaine, vous pouvez choisir d’envoyer des notifications push pendant la journée et des e-mails le soir.

>[!NOTE]
>
>* Le fuseau horaire n’est plus spécifique à une condition et est désormais défini au niveau du parcours dans les propriétés de celui-ci. [En savoir plus](../building-journeys/timezone-management.md)
>
>* Par défaut, la **[!UICONTROL Condition de temps]** est définie par heure, de 00:00 à 12:00.

![Condition de temps avec les sélecteurs de plage horaire et de jour de la semaine](assets/journey51.png)

Trois options de filtrage temporel sont disponibles :

* **Heure** : vous permet de configurer une condition en fonction de l’heure de la journée. Vous définissez ensuite les heures de début et de fin. Les personnes ne saisissent le chemin d’accès que pendant la plage d’heures définie.
* **Jour de la semaine** : vous permet de configurer une condition en fonction du jour de la semaine. Vous sélectionnez ensuite les jours où vous souhaitez que les individus rejoignent le chemin.
* **Jour de la semaine et heure** : cette option regroupe les deux premières options.

## Limite de profils {#profile_cap}

Utilisez ce type de condition pour définir un nombre maximal de profils pour le chemin dʼun parcours. Lorsque cette limite est atteinte, les profils entrants prennent un autre chemin. De cette manière, vos parcours ne dépasseront jamais la limite définie.

>[!NOTE]
>
>Nous vous recommandons de définir une limite de profil à valeur élevée. La précision et la probabilité qu’une population atteigne le nombre exact de limites ne font qu’augmenter à mesure que la limite augmente. Pour les petits nombres (par exemple une limite de 50), les nombres ne correspondent pas toujours, car la limite peut ne pas être atteinte avant que les profils ne prennent un autre chemin.

<!--You can use this condition type to ramp up the volume of your deliveries. See this [use case](ramp-up-deliveries-uc.md).-->

La limite par défaut est fixée à 1 000.

Le compteur s’applique uniquement à la version du parcours sélectionnée. Le compteur se réinitialise à zéro lorsque le parcours est dupliqué ou qu’une nouvelle version est créée. Après une réinitialisation, les profils entrants reprennent le chemin nominal jusqu’à ce que la limite de compteur soit atteinte.

Lorsque la limite de profil est définie sur un parcours récurrent, le compteur ne se réinitialise pas après chaque périodicité.

Le chemin nominal a toujours la priorité sur le chemin alternatif, même si vous déplacez le chemin alternatif au-dessus du chemin nominal sur la zone de travail de parcours.

Pour les parcours actifs, voici les seuils à prendre en compte pour que la limite soit atteinte :

* Pour une limite supérieure à 10 000, le nombre de profils distincts à injecter doit être au moins égal à 1,3 fois la limite.
* Pour une limite inférieure à 10 000, le nombre de profils distincts à injecter doit être de 1 000 plus la limite.

La limite de profils n’est pas prise en compte en mode test.

![Condition de limite de profils avec champ d’entrée de la limite maximale de profils](assets/profile-cap-condition.png)

## Utiliser des audiences dans des conditions {#using-a-segment}

Cette section explique comment utiliser une audience dans une condition de parcours. Pour plus d’informations sur les audiences et sur la manière de les créer, consultez [cette section](../audience/about-audiences.md).

Pour utiliser une audience dans une condition de parcours, procédez comme suit :

1. Ouvrez un parcours, déposez une activité **[!UICONTROL Optimiser]** et choisissez la **[!UICONTROL condition de source de données]**.

   ![Méthode Condition de source de données sélectionnée dans le menu déroulant](assets/segment3.png)

1. Cliquez sur **[!UICONTROL Ajouter un chemin]** pour chaque chemin supplémentaire nécessaire. Pour chaque chemin, cliquez sur le champ **[!UICONTROL Expression]**.

1. Sur le côté gauche, développez le nœud **[!UICONTROL Audiences]**. Faites glisser et déposez l’audience à utiliser pour votre condition. Par défaut, la condition sur l’audience est « true ».

   ![Nœud Audiences de l’éditeur d’expression pour sélectionner les audiences Adobe Experience Platform](assets/segment4.png){width=80%}

   >[!NOTE]
   >
   >Notez que seules les personnes ayant le statut de participation d’audience **Réalisé** sont considérées comme membres de l’audience. Pour plus d’informations sur l’évaluation d’une audience, consultez la [documentation du service de segmentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/tutorials/evaluate-a-segment.html?lang=fr#interpret-segment-results){target="_blank"}.
