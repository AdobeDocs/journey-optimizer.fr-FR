---
title: Configuration d’un événement unitaire
description: Découvrez comment configurer un événement unitaire
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '1675'
ht-degree: 0%

---

# Configurer un événement unitaire {#configure-an-event}

![](../assets/do-not-localize/badge.png)

Les événements unitaires sont liés à un profil spécifique. Ils peuvent être basés sur des règles ou générés par le système.  En savoir plus sur le événement unitaire [cette section](../event/about-events.md).

Voici les premières étapes de la configuration d’un nouveau événement :

1. Dans le menu de gauche, cliquez sur l&#39;icône **[!UICONTROL Admin]**, puis sur **[!UICONTROL Événements]**. La liste des événements s’affiche.

   ![](../assets/jo-event1.png)

1. Cliquez sur **[!UICONTROL Ajouter]** pour créer un événement. Le volet de configuration du événement s&#39;ouvre sur le côté droit de l&#39;écran.

   ![](../assets/jo-event2.png)

1. Entrez le nom de votre événement. Vous pouvez également ajouter une description.

   ![](../assets/jo-event3.png)

   >[!NOTE]
   >
   >N’utilisez pas d’espaces ni de caractères spéciaux. N’utilisez pas plus de 30 caractères.

1. Dans le champ **[!UICONTROL Type]**, choisissez **événements unitaires**.

   ![](../assets/jo-event3bis.png)

1. Dans le champ **[!UICONTROL Événement ID type]**, sélectionnez le type d’ID de événement à utiliser : **Règle basée sur** ou **Généré par le système**. Pour en savoir plus sur les types d&#39;ID de événement, consultez [cette section](../event/about-events.md#event-id-type).

   ![](../assets/jo-event4.png)

1. Le nombre de parcours qui utilisent ce événement s’affiche dans le champ **[!UICONTROL Utilisé dans]**. Vous pouvez cliquer sur l&#39;icône **[!UICONTROL parcours de Vue]** pour afficher la liste des parcours utilisant ce événement.

1. Définissez les champs schéma et charge utile : c’est là que vous sélectionnez les informations de événement (généralement appelées données utiles) que les parcours attendent de recevoir. Vous pourrez alors utiliser ces informations dans votre parcours. Voir [cette section](../event/about-creating.md#define-the-payload-fields).

   ![](../assets/jo-event5.png)

   >[!NOTE]
   >
   >Lorsque vous sélectionnez le type **[!UICONTROL System Generated]**, seuls les schémas dont le mixin de type eventID est disponible. Lorsque vous sélectionnez le type **[!UICONTROL Règle basée sur]**, tous les schémas de Événement d’expérience sont disponibles.

1. Pour les événements basés sur des règles, cliquez dans le champ **[!UICONTROL condition d’ID de Événement]**. A l’aide de l’éditeur d’expressions simple, définissez la condition qui sera utilisée par le système pour identifier les événements qui déclencheront votre parcours.
   ![](../assets/jo-event6.png)

   Dans notre exemple, nous avons écrit une condition basée sur la ville du profil. Cela signifie que chaque fois que le système reçoit un événement correspondant à cette condition (**[!UICONTROL champ Ville]** et **[!UICONTROL valeur Paris]**), il le transmet aux parcours.

1. Ajoutez un espace de nommage. Cette étape est facultative, mais recommandée car l’ajout d’un espace de nommage vous permet d’exploiter les informations stockées dans le service de Profil client en temps réel. Il définit le type de clé dont dispose le événement. Voir [cette section](../event/about-creating.md#select-the-namespace).
1. Définissez la clé : choisissez un champ dans vos champs de charge utile ou définissez une formule pour identifier la personne associée au événement. Cette clé est automatiquement configurée (mais peut toujours être modifiée) si vous sélectionnez un espace de nommage. En effet, les parcours sélectionnent la clé qui doit correspondre à l’espace de nommage (par exemple, si vous sélectionnez un espace de nommage de courriel, la clé de courriel est sélectionnée). Voir [cette section](../event/about-creating.md#define-the-event-key).

   ![](../assets/jo-event7.png)

1. Pour les événements générés par le système, vous pouvez ajouter une condition. Cette étape est facultative. Cela permet au système de traiter uniquement les événements qui répondent à la condition. La condition ne peut être basée que sur les informations contenues dans le événement. Voir [cette section](../event/about-creating.md#add-a-condition).
1. Cliquez sur **[!UICONTROL Enregistrer]**.

   ![](../assets/journey7.png)

   Le événement est maintenant configuré et prêt à être déposé dans un parcours. Des étapes de configuration supplémentaires sont requises pour recevoir des événements. Voir [cette page](../event/additional-steps-to-send-events-to-journey-orchestration.md).

## Définition des champs de charge utile {#define-the-payload-fields}

La définition de charge utile vous permet de choisir les informations que le système attend de recevoir du événement dans votre parcours et la clé pour identifier la personne associée au événement. La charge utile est basée sur la définition de champ XDM Experience Cloud. Pour plus d&#39;informations sur XDM, consultez [cette page](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html).

1. Sélectionnez un schéma XDM dans la liste et cliquez sur le champ **[!UICONTROL Charge utile]** ou sur l&#39;icône **[!UICONTROL Modifier]**.

   ![](../assets/journey8.png)

   Tous les champs définis dans le schéma s’affichent. La liste des champs varie d’un schéma à l’autre. Vous pouvez rechercher un champ spécifique ou utiliser les filtres pour afficher tous les noeuds et champs ou uniquement les champs sélectionnés. Selon la définition du schéma, certains champs peuvent être obligatoires et présélectionnés. Vous ne pouvez pas les désélectionner. Tous les champs obligatoires pour que le événement soit correctement reçu par les parcours sont sélectionnés par défaut.

   >[!NOTE]
   >
   >Assurez-vous d’avoir ajouté le mixin &quot;orchestration&quot; au schéma XDM. Ainsi, votre schéma contient toutes les informations requises pour fonctionner avec [!DNL Journey Optimizer].

   ![](../assets/journey9.png)

1. Sélectionnez les champs que vous prévoyez de recevoir du événement. Il s&#39;agit des champs que l&#39;utilisateur utilisera dans le parcours. Ils doivent également inclure la clé qui sera utilisée pour identifier la personne associée au événement (voir [cette section](../event/about-creating.md#define-the-event-key)).

   ![](../assets/journey10.png)

   >[!NOTE]
   >
   >Pour les événements générés par le système, le champ **[!UICONTROL eventID]** est automatiquement ajouté à la liste des champs sélectionnés afin que [!DNL Journey Optimizer] puisse identifier le événement. Le système qui pousse le événement ne doit pas générer d’identifiant, il doit utiliser celui disponible dans la prévisualisation de charge utile. Voir [cette section](../event/about-creating.md#preview-the-payload).

1. Lorsque vous avez terminé de sélectionner les champs nécessaires, cliquez sur **[!UICONTROL Enregistrer]** ou appuyez sur **[!UICONTROL Entrée]**.

   ![](../assets/journey11.png)

   Le nombre de champs sélectionnés apparaît dans le champ **[!UICONTROL Charge utile]**.

   ![](../assets/journey12.png)

## Sélectionnez l’espace de nommage {#select-the-namespace}

L’espace de nommage vous permet de définir le type de clé utilisé pour identifier la personne associée au événement. Sa configuration est facultative. Elle est requise si vous souhaitez récupérer, dans vos parcours, des informations supplémentaires provenant du [Profil client en temps réel](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html). La définition d’espace de nommage n’est pas nécessaire si vous utilisez uniquement des données provenant d’un système tiers via une source de données personnalisée.

Vous pouvez soit utiliser l&#39;un des prédéfinis, soit en créer un nouveau à l&#39;aide du service d&#39;Espace de nommage d&#39;identité. Reportez-vous à cette [page](https://experienceleague.adobe.com/docs/experience-platform/identity/home.html).

Si vous sélectionnez un schéma doté d&#39;une identité Principale, les champs **[!UICONTROL Clé]** et **[!UICONTROL Espace de nommage]** sont préremplis. Si aucune identité n&#39;est définie, nous sélectionnons _identityMap > id_ comme clé Principale. Ensuite, vous devez sélectionner un espace de nommage et la clé sera préremplie (sous le champ **[!UICONTROL Espace de nommage]**) en utilisant _IdentityMap > id_.

Lors de la sélection de champs, les champs d&#39;identité Principaux sont balisés.

![](../assets/primary-identity.png)


Sélectionnez un espace de nommage dans la liste déroulante.

![](../assets/journey17.png)

Un seul espace de nommage est autorisé par parcours. Si vous utilisez plusieurs événements dans le même parcours, ils doivent utiliser le même espace de nommage. Voir [cette page](../building-journeys/journey.md).

## Définir la clé de événement {#define-the-event-key}

La clé est que le champ ou la combinaison de champs fait partie des données de charge utile du événement et permet au système d&#39;identifier la personne associée au événement. La clé peut être, par exemple, l’ID d’Experience Cloud, un ID de gestion de la relation client ou une adresse électronique.

Si vous prévoyez d’exploiter les données stockées dans la base de données du Profil client en temps réel, vous devez sélectionner, en tant que clé de événement, les informations que vous avez définies comme identité de profil dans le [service de Profil client en temps réel](https://experienceleague.adobe.com/docs/experience-platform/profile/home.html).

Il permettra au système d&#39;effectuer le rapprochement entre le événement et le profil de l&#39;individu. Si vous sélectionnez un schéma doté d&#39;une identité Principale, les champs **[!UICONTROL Clé]** et **[!UICONTROL Espace de nommage]** sont préremplis. Si aucune identité n&#39;est définie, nous sélectionnons _identityMap > id_ comme clé Principale. Ensuite, vous devez sélectionner un espace de nommage et la clé sera préremplie (sous le champ **[!UICONTROL Espace de nommage]**) en utilisant _IdentityMap > id_.

Lors de la sélection de champs, les champs d&#39;identité Principaux sont balisés.

![](../assets/primary-identity.png)

Si vous devez utiliser une autre clé, telle qu’un identifiant de gestion de la relation client ou une adresse électronique, vous devez l’ajouter manuellement :

1. Cliquez dans le champ **[!UICONTROL Clé]** ou sur l&#39;icône représentant un crayon.

   ![](../assets/journey16.png)

1. Sélectionnez le champ choisi comme clé dans la liste des champs de charge utile. Vous pouvez également passer à l’éditeur d’expressions avancé pour créer des clés plus complexes (par exemple, une concaténation de deux champs des événements). Voir ci-dessous, dans cette section.

   ![](../assets/journey20.png)

Lorsque le événement est reçu, la valeur de la clé permet au système d&#39;identifier la personne associée au événement. Associée à un espace de nommage (voir [cette section](../event/about-creating.md#select-the-namespace)), la clé peut être utilisée pour exécuter des requêtes sur Adobe Experience Platform. Voir [cette page](../building-journeys/about-journey-activities.md#orchestration-activities).
La clé est également utilisée pour vérifier qu&#39;une personne est dans un parcours. En effet, une personne ne peut se trouver à deux endroits différents dans le même parcours. Par conséquent, le système ne permet pas que la même clé, par exemple la clé CRMID=3224, se trouve à des endroits différents dans le même parcours.

Vous avez également accès aux fonctions avancées d&#39;expression (**[!UICONTROL Mode avancé]**) si vous souhaitez effectuer des manipulations supplémentaires. Ces fonctions vous permettent de manipuler les valeurs utilisées pour exécuter des requêtes spécifiques telles que des formats de modification, des concaténations de champs, en ne prenant en compte qu’une partie d’un champ (par exemple, les 10 premiers caractères). Voir [cette page](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html).

## Ajouter une condition {#add-a-condition}

La condition n’est disponible que pour les événements générés par le système. Vous pouvez définir une condition de événement qui permet au système de filtrer le traitement des événements. Si la condition est vraie, le événement est traité. Si la condition n’est pas vraie, le événement est ignoré.

La condition sur les événements ne peut être basée que sur les données transmises dans la charge utile du événement. La condition définie au niveau du événement ne peut pas être modifiée dans la trame par un spécialiste du marketing. Le but est de durcir cette condition lorsque ce événement est utilisé. Par exemple, si vous ne souhaitez jamais que les spécialistes du marketing utilisent des événements d’abandon de panier si la valeur du panier est trop faible, vous pouvez créer une condition sur le champ événement &quot;valeur du panier&quot; et imposer une valeur supérieure à 100 dollars.

Vous pouvez utiliser l’éditeur d’expressions simple ou l’éditeur d’expressions avancé pour configurer les conditions sur les événements. Voir [cette page](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/expressionadvanced.html).

Par exemple, vous pouvez définir une condition pour traiter uniquement les événements d’un type d&#39;événement spécifique et ignorer les autres types. Ou si votre événement est un abandon de panier et que la charge utile inclut le champ de valeur de panier, vous pouvez définir une condition de événement pour traiter les événements uniquement si la valeur de panier est supérieure à 100 dollars.

![](../assets/journey78.png)

## Prévisualisation de la charge utile {#preview-the-payload}

La prévisualisation de charge utile vous permet de valider la définition de charge utile.

>[!NOTE]
>
>Pour les événements générés par le système, lorsque vous créez un événement, avant d’afficher la prévisualisation de charge utile, enregistrez votre événement et rouvrez-le. Cette étape est nécessaire pour générer un ID de événement dans la charge utile.

1. Cliquez sur l&#39;icône **[!UICONTROL Vue Payload]** pour prévisualisation de la charge utile attendue par le système.

   ![](../assets/journey13.png)

   Vous pouvez constater que les champs sélectionnés sont affichés.

   ![](../assets/journey14.png)

1. Vérifiez la prévisualisation pour valider la définition de charge utile.

1. Ensuite, vous pouvez partager la prévisualisation de charge utile avec la personne responsable de l’envoi du événement. Cette charge peut l&#39;aider à concevoir la configuration d&#39;un événement poussant vers [!DNL Journey Optimizer]. Voir [cette page](../event/additional-steps-to-send-events-to-journey-orchestration.md).
