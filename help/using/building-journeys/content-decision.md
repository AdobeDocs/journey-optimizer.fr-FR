---
solution: Journey Optimizer
product: journey optimizer
title: Activité de décision de contenu
description: En savoir plus sur l’activité de décision de contenu
feature: Journeys, Activities
topic: Content Management
role: User
level: Intermediate
badge: label="Disponibilité limitée" type="Informative"
keywords: activité, prise de décision, décision de contenu, politique de décision, zone de travail, parcours
exl-id: 6188644a-6a3b-4926-9ae9-0c6b42c96bae
source-git-commit: 701b2caeac704149c820ce3bf6338107ab4bc9f8
workflow-type: tm+mt
source-wordcount: '1030'
ht-degree: 7%

---

# Activité de décision de contenu {#content-decision}

>[!AVAILABILITY]
>
>Cette fonctionnalité n’est disponible que pour un ensemble d’organisations (disponibilité limitée) et sera proposée à tous les utilisateurs et utilisatrices dans une prochaine version.

[!DNL Journey Optimizer] vous permet d’inclure des offres dans vos parcours par le biais de l’activité dédiée **décision de contenu** dans la zone de travail du parcours. Vous pouvez ensuite ajouter d’autres activités (telles que des [actions personnalisées](../action/about-custom-action-configuration.md)) à vos parcours pour cibler vos audiences avec ces offres personnalisées.

>[!NOTE]
>
>La sortie d’une activité de décision de contenu ne peut pas être utilisée dans les activités de canal natives.

Pour tirer parti de cette fonctionnalité, créez un parcours dans lequel vous ajoutez une [activité de décision de contenu](#add-content-decision-activity) pour définir les offres que vous souhaitez présenter aux profils éligibles.

Vous pouvez ensuite utiliser la sortie de l’activité de décision de contenu dans :

* une [activité de condition](#add-condition-activity) permettant de déplacer les profils vers des chemins spécifiques en fonction des offres récupérées ;

* une [action personnalisée](#add-custom-action), dans laquelle vous pouvez envoyer ces offres à des systèmes externes.

## Configurer une activité de décision de contenu {#add-content-decision-activity}

À l’aide de l’activité de décision de contenu, vous pouvez définir une politique de décision qui vous permet de sélectionner les meilleurs éléments d’[!DNL Journey Optimizer] Decisioning et de les diffuser à la bonne audience.

<!--Their goal is to select the best offers for each profile, while the campaign/journey authoring allows you to indicate how the selected decision items should be presented, including which item attributes to be included in the message.-->

Pour configurer l’activité **[!UICONTROL Décision de contenu]**, procédez comme suit.

1. Développez la catégorie **[!UICONTROL Orchestration]** et déposez une activité **[!UICONTROL Décision de contenu]** dans la zone de travail.

   ![Ajouter une décision de contenu au parcours ](assets/journey-content-decision.png){width=100%}

1. Vous pouvez éventuellement ajouter un libellé et une description à l’activité.

1. Cliquez sur **[!UICONTROL Ajouter une politique de décision]**. [En savoir plus sur les politiques de décision](../experience-decisioning/create-decision.md)

   >[!NOTE]
   >
   >Les autorisations de prise de décision sont nécessaires pour créer une politique de décision. [En savoir plus](../experience-decisioning/gs-experience-decisioning.md#steps)

1. Sélectionnez le nombre d’éléments à renvoyer. Par exemple, si vous sélectionnez 2, les 2 meilleures offres éligibles seront présentées. Cliquez sur **[!UICONTROL Suivant]**.

1. Dans la section **[!UICONTROL Séquence de stratégie]**, sélectionnez les éléments de décision et/ou les stratégies de sélection à présenter avec la politique de décision. [En savoir plus](../experience-decisioning/create-decision.md#select)

1. Organisez l’ordre d’évaluation selon les besoins.

   Lors de l’ajout de plusieurs éléments de décision et/ou stratégies, ils sont évalués dans un ordre séquentiel, avec des nombres à gauche de chaque objet ou groupe d’objets. Pour modifier la séquence par défaut, vous pouvez faire glisser et déposer les objets et/ou les groupes afin de les réorganiser selon vos besoins. [En savoir plus](../experience-decisioning/create-decision.md#evaluation-order)

1. Vous pouvez éventuellement ajouter une offre de secours. [En savoir plus](../experience-decisioning/create-decision.md#fallback)

1. Examinez et enregistrez votre politique de décision.

   ![Résumé de la politique de décision](assets/journey-content-decision-policy.png){width=70%}<!--reshoot or change screen-->

Vous êtes maintenant prêt à exploiter la sortie de cette activité de décision de contenu dans votre parcours.

## Utiliser la sortie de l’activité de décision de contenu {#use-content-decision-output}

La sortie d’une décision de contenu peut être utilisée dans plusieurs activités de parcours. Par exemple, vous pouvez utiliser une [activité de condition](#add-condition-activity) pour déplacer des profils vers des branches spécifiques de votre parcours, en fonction du nombre d’offres récupérées pour ces dernières.

Vous pouvez également ajouter une [action personnalisée](#add-custom-action) à votre parcours afin de partager les offres de l&#39;activité de décision de contenu avec un système externe.

### Dans une activité de condition {#add-condition-activity}

Pour tirer parti de la sortie d’une activité de décision de contenu, vous pouvez ajouter une condition à votre parcours, où vous définissez des expressions pour déplacer des profils vers des chemins spécifiques à l’aide des données de ces offres. Suivez les étapes ci-dessous.

1. Dans la catégorie **[!UICONTROL Orchestration]**, déposez une activité **[!UICONTROL Condition]** dans la zone de travail. [En savoir plus](condition-activity.md#add-condition-activity)

1. Vous pouvez éventuellement renommer **[!UICONTROL Path1]**, qui correspond à la première expression que vous définissez, en un libellé plus pertinent.

1. Pour ce premier chemin, cliquez dans le champ **[!UICONTROL Expression]** ou utilisez l’icône Modifier pour ajouter une expression.

   ![Ajoutez une condition et modifiez l’expression](assets/journey-content-decision-condition.png){width=80%}

1. Dans la fenêtre pop-up qui s’ouvre, passez en **[!UICONTROL mode avancé]** pour utiliser l’[éditeur d’expression avancé](expression/expressionadvanced.md).

   >[!CAUTION]
   >
   >La sortie d’un nœud de décision de contenu est uniquement disponible en **[!UICONTROL mode avancé]**.

1. Développez le nœud **[!UICONTROL Context]** et accédez à votre politique de décision pour afficher tous les attributs disponibles dans le [schéma de catalogue des offres](../experience-decisioning/catalogs.md#access-catalog-schema).

   ![Ajoutez une condition et modifiez l’expression](assets/journey-content-decision-context.png)

   >[!NOTE]
   >
   >Toute étiquette restreinte définie sur un attribut, dans un événement d’expérience de parcours utilisé dans une règle de décision (comme données contextuelles) ou dans le [schéma d’offres](../experience-decisioning/catalogs.md#access-catalog-schema), n’entraîne pas de violation de la politique pour DULE ou le consentement. En savoir plus sur les politiques de gouvernance des données dans [cette section](../action/action-privacy.md)

1. Pour vérifier si une offre a été renvoyée pour les profils qui rejoignent le parcours, utilisez la fonction [listSize](functions/functionlistsize.md) avec la syntaxe suivante : `listSize(@decision{ContentdecisionName.items})>0`

   >[!NOTE]
   >
   >Dans cet exemple, `Name` est le libellé de la décision de contenu que vous avez ajoutée à votre parcours.

   ![Ajouter une condition avec la liste](assets/journey-content-decision-condition-list.png)

1. Cliquez sur **[!UICONTROL OK]**.

1. Ajoutez d’autres chemins d’accès pour définir d’autres conditions si nécessaire.

   Vous pouvez également créer un autre chemin pour les profils qui ne répondent pas à la première condition en cochant la case **[!UICONTROL Afficher le chemin pour d’autres cas que celui ou ceux ci-dessus]**. <!--These profiles will then exit the journey if no other activity is added in that path.-->

1. Enregistrez l’activité de condition.

### Dans une action personnalisée {#add-custom-action}

Pour tirer parti de la sortie d’une activité de décision de contenu, vous pouvez ajouter une action personnalisée à votre parcours, dans laquelle vous partagerez les offres que vous avez définies avec un système externe. Suivez les étapes ci-dessous.

1. Ajoutez une action personnalisée à votre parcours. [En savoir plus](../action/about-custom-action-configuration.md)

1. Saisissez un libellé pour votre action.

1. Dans la section **[!UICONTROL Paramètres de requête]**, sélectionnez le paramètre que vous souhaitez mapper aux attributs des offres qui ont été récupérées.

   Cliquez dans le champ de texte modifiable et sélectionnez tout paramètre que vous souhaitez mapper aux attributs des offres qui ont été récupérées.

   ![Modifier les paramètres de requête de l’action personnalisée](assets/journey-content-decision-custom-action-param.png)

1. Passez en **[!UICONTROL mode avancé]** dans la fenêtre pop-up qui s’ouvre. Dans l’[éditeur d’expression avancé](expression/expressionadvanced.md), développez le nœud **[!UICONTROL Context]** pour afficher tous les éléments de la politique de décision.

   >[!CAUTION]
   >
   >La sortie d’un nœud de décision de contenu est uniquement disponible en **[!UICONTROL mode avancé]**.

1. Parcourez le [schéma de catalogue d’offres](../experience-decisioning/catalogs.md#access-catalog-schema) à l’aide du tableau `items`. Par exemple, utilisez la `itemName` de la première offre récupérée et la `itemName` de la seconde offre récupérée.

   ![Paramètres de requête de l’action personnalisée, y compris la politique de décision](assets/journey-content-decision-custom-action-param-ex.png)

1. Cliquez sur **[!UICONTROL Ok]** pour enregistrer votre expression.

1. **[!UICONTROL Enregistrez]** votre configuration d’action personnalisée.

### Exemple complet {#use-case}

Vous trouverez ci-dessous l’exemple complet d’un parcours utilisant une activité de décision de contenu combinée à une activité de condition et à une action personnalisée, comme décrit ci-dessus.

![parcours complet](assets/journey-content-decision-full-journey.png)

<!--When all activities are properly configured and saved, [publish](publishing-the-journey.md) your journey.-->

Une fois le parcours [activé](publishing-the-journey.md) :

<!--* Profiles who enter the journey and are eligible for at least one offer are targeted by the custom action.

* If no offer is returned for a profile, they are excluded from the custom action.-->

1. Chaque fois qu’un profil se qualifie pour cette audience, il entre dans le parcours.

1. Par le biais de l’activité de décision de contenu , [!DNL Journey Optimizer] récupère les offres pertinentes pour chaque profil.

1. Seuls les profils pour lesquels au moins une offre est récupérée continuent le parcours (via le chemin « Profils éligibles »).

1. Si la condition est remplie, les offres correspondantes sont envoyées à un système externe via l’action personnalisée.
