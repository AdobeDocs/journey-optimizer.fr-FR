---
title: Concevoir le parcours
description: Découvrez comment concevoir votre parcours
feature: Journeys
topic: Content Management
role: User
level: Intermediate
exl-id: 1998f6fc-60fd-4038-8669-39cd55bc02d1
source-git-commit: 5596c851b70cc38cd117793d492a15fd4ce175ef
workflow-type: tm+mt
source-wordcount: '1487'
ht-degree: 98%

---

# Concevoir le parcours {#design-your-journey}

>[!CONTEXTUALHELP]
>id="ajo_journey_canvas"
>title="Concevoir le parcours"
>abstract="L&#39;interface de parcours vous permet de faire glisser facilement des activités de la palette vers la zone de travail. Vous pouvez également double-cliquer sur une activité pour l&#39;ajouter dans la zone de travail à la prochaine étape disponible."

L&#39;interface de parcours vous permet de faire glisser facilement des activités de la palette vers la zone de travail. Vous pouvez également double-cliquer sur une activité pour l&#39;ajouter dans la zone de travail à la prochaine étape disponible. Chaque activité possède un rôle et un emplacement précis dans le processus. Les activités sont séquencées. Cela signifie que lorsqu&#39;une activité est terminée, le flux se poursuit et traite l&#39;activité suivante, et ainsi de suite.

## Prise en main de la conception de parcours

La **palette** se situe sur la partie gauche de l&#39;écran. Toutes les activités disponibles sont classées dans plusieurs catégories : **[!UICONTROL Événements]**, **[!UICONTROL Orchestration]** et **[!UICONTROL Actions]**. Vous pouvez développer/réduire les différentes catégories en cliquant sur leur nom. Pour utiliser une activité dans votre parcours, faites-la glisser de la palette vers la zone de travail.

Lors du démarrage d&#39;un nouveau parcours, les éléments qui ne peuvent pas être déposés dans la zone de travail comme première étape sont masqués. Cela concerne toutes les actions, l&#39;activité de la condition, l&#39;attente et la réaction.

![](assets/journey38.png)

L&#39;icône **[!UICONTROL Filtrer les éléments]** dans le coin supérieur gauche vous permet d&#39;afficher les filtres suivants :

* **Afficher uniquement les éléments disponibles** : masquez ou affichez les éléments indisponibles dans la palette, par exemple les événements qui utilisent un espace de noms différent de ceux utilisés dans votre parcours. Par défaut, les éléments non disponibles sont masqués. Si vous choisissez de les afficher, ils apparaîtront grisés.

* **Afficher uniquement les éléments récents** : ce filtre vous permet d&#39;afficher uniquement les cinq derniers événements et actions utilisés, en plus de ceux d&#39;usine. Il est spécifique à chaque utilisateur. Par défaut, tous les éléments s&#39;affichent.

Vous pouvez également utiliser le champ **[!UICONTROL Rechercher]**. Seuls les événements et les actions sont filtrés.

La **zone de travail** est la zone centrale du concepteur de parcours. C&#39;est là que vous pouvez déposer vos activités et les configurer. Cliquez sur une activité de la zone de travail pour la configurer. Le volet de configuration de l&#39;activité s&#39;ouvre alors sur le côté droit.

![](assets/journey39.png)

Le **volet de configuration des activités** s&#39;affiche lorsque vous cliquez sur une activité dans la palette. Renseignez les champs obligatoires. Cliquez sur l&#39;icône **[!UICONTROL Supprimer]** pour supprimer l&#39;activité. Cliquez sur **[!UICONTROL Annuler]** pour annuler les modifications ou sur **[!UICONTROL OK]** pour les confirmer. Vous pouvez également supprimer des activités en les sélectionnant, puis en appuyant sur la touche Retour arrière. Appuyez sur la touche d&#39;échappement pour fermer le volet de configuration des activités.

Par défaut, les champs en lecture seule sont masqués. Pour afficher les champs en lecture seule, cliquez sur l&#39;icône **Afficher les champs en lecture seule** en haut à gauche du volet de configuration de l&#39;activité. Ce paramètre s&#39;applique à toutes les activités de tous les parcours.

![](assets/journey59bis.png)

Selon le statut du parcours, vous pouvez effectuer différentes actions à l&#39;aide des boutons disponibles dans le coin supérieur droit : **[!UICONTROL Publier]**, **[!UICONTROL Dupliquer]**, **[!UICONTROL Supprimer]**, afficher les **[!UICONTROL Propriétés du parcours]** et effectuer un **[!UICONTROL Test]**. Ces boutons s&#39;affichent lorsqu&#39;aucune activité n&#39;est sélectionnée. Certains boutons s&#39;affichent en fonction du contexte. Le bouton de journal du mode test s&#39;affiche lorsque le mode test est activé.

![](assets/journey41.png)

## Démarrage de votre parcours

Lorsque vous concevez votre parcours, la première question que vous devez vous poser est la suivante : comment les profils vont-ils rejoindre le parcours ? Il existe deux possibilités :

**Débuter avec un événement** : lorsqu&#39;un parcours est prêt à écouter les événements, les individus rejoignent le parcours **de façon unitaire** en temps réel. Les messages inclus dans votre parcours sont envoyés à la personne qui arrive actuellement dans le parcours. [En savoir plus sur les événements](../event/about-events.md)

**Débuter avec une Lecture de segment** : vous pouvez définir votre parcours pour écouter les segments Adobe Experience Platform. Dans ce cas, tous les individus appartenant au segment spécifié rejoignent le parcours. Les messages inclus dans votre parcours sont envoyés aux individus appartenant au segment. [En savoir plus sur la lecture de segments](read-segment.md).

## Définir les étapes suivantes

Après votre premier événement ou votre première lecture de segment, vous pouvez combiner les différentes activités afin de créer vos scénarios cross-canal en plusieurs étapes. Choisissez, dans la palette, les étapes dont vous avez besoin.

**Événements**

Lorsque vous débutez votre parcours avec un événement, le parcours est déclenché à la réception de l&#39;événement. La personne suivra ensuite, individuellement, les étapes suivantes définies dans votre parcours.

Vous pouvez ajouter **plusieurs événements** dans votre parcours, à condition qu&#39;ils utilisent le même espace de noms. Les événements sont configurés au préalable. [En savoir plus sur les événements](about-journey-activities.md#event-activities)

Vous pouvez également ajouter un événement de **réaction** après un message pour réagir aux données de suivi liées au message. Cela vous permet, par exemple, d&#39;envoyer un autre message si l&#39;individu a ouvert le message précédent ou cliqué dessus. En savoir plus dans cette [section](reaction-events.md).

L&#39;activité d&#39;événement **Qualification du segment** vous permet de faire en sorte que des individus rejoignent un parcours ou y progressent en fonction des entrées et des sorties de segments Adobe Experience Platform. Vous pouvez faire en sorte que tous les nouveaux clients Silver rejoignent un parcours et envoyer des messages personnalisés. En savoir plus dans cette [section](segment-qualification-events.md).

**Orchestration**

Dans les activités d&#39;orchestration, vous trouverez l&#39;activité **Lecture de segment** qui vous permet de définir votre parcours pour écouter un segment Adobe Experience Platform. [En savoir plus sur l&#39;activité Lecture de segment](read-segment.md).

Les autres activités vous permettent d&#39;ajouter des conditions à votre parcours afin de définir plusieurs chemins, de définir un délai d&#39;attente avant l&#39;exécution de l&#39;activité suivante, ou de terminer votre parcours. En savoir plus dans cette [section](about-journey-activities.md#orchestration-activities).

**Actions**

Vous trouverez ici l&#39;activité **Message** qui vous permet d&#39;inclure un message conçu dans [!DNL Journey Optimizer]. [En savoir plus sur l&#39;activité Message](journeys-message.md)

Vous trouverez également les actions personnalisées que vous avez configurées pour envoyer des messages avec des systèmes tiers. En savoir plus dans cette [section](about-journey-activities.md#action-activities).

## Utilisation des chemins dans la zone de travail {#paths}

Plusieurs activités (**[!UICONTROL Condition]**, **[!UICONTROL Action]**, etc.) vous permettent de définir une action de remplacement en cas d&#39;erreur ou de temporisation. Dans le volet de configuration des activités, cochez la case **[!UICONTROL Ajouter un itinéraire alternatif en cas de temporisation ou d&#39;erreur]**. Un autre chemin est alors ajouté après l&#39;activité. La temporisation est définie dans les propriétés du parcours (voir [cette page](../building-journeys/journey-gs.md#change-properties) par un utilisateur administrateur. Par exemple, si l&#39;envoi d&#39;un email prend trop de temps ou est en erreur, vous pouvez décider d&#39;envoyer une notification push.

![](assets/journey42.png)

Différentes activités (événement, action, attente) peuvent être suivies de plusieurs chemins. Pour ce faire, placez votre curseur sur l&#39;activité en question et cliquez ensuite sur le symbole « + ». Seules les activités d&#39;événement et d&#39;attente peuvent être définies en parallèle. Si plusieurs événements sont définis en parallèle, le chemin choisi est celui du premier événement qui se produit.

Lorsque vous écoutez un événement, nous vous recommandons de ne pas attendre indéfiniment qu&#39;il se produise. Notez qu&#39;il s&#39;agit d&#39;une bonne pratique et que cela n&#39;est, en aucun cas, obligatoire. Si vous souhaitez limiter l&#39;écoute d&#39;un ou de plusieurs événements à une période bien définie, vous devez placer en parallèle un ou plusieurs événements et une activité d&#39;attente. Consultez [cette section](../building-journeys/general-events.md#events-specific-time).

Pour supprimer le chemin d&#39;accès, placez votre curseur sur celui-ci et cliquez sur l&#39;icône **[!UICONTROL Supprimer le chemin]**.

![](assets/journey42ter.png)

Dans la zone de travail, un avertissement s&#39;affiche lorsque deux activités sont déconnectées. Placez le curseur sur l&#39;icône d&#39;avertissement pour afficher le message d&#39;erreur. Pour résoudre le problème, il suffit de déplacer l&#39;activité déconnectée et de la relier à l&#39;activité précédente.

![](assets/canvas-disconnected.png)

## Opérations de copier/coller d&#39;activités {#copy-paste}

Vous pouvez copier une ou plusieurs activités d&#39;un parcours et les coller soit dans le même parcours, soit dans un autre. C&#39;est un gain de temps si vous souhaitez réutiliser de nombreuses activités déjà configurées lors d&#39;un parcours précédent.

**Remarques importantes**

* Vous pouvez effectuer une opération copier/coller dans différents onglets et navigateurs. Vous ne pouvez copier/coller des activités que dans la même instance.
* Vous ne pouvez pas copier/coller un événement si le parcours de destination comporte un événement utilisant un autre espace de noms.
* Les activités collées peuvent référencer des données qui n&#39;existent pas dans le parcours de destination, par exemple si vous copiez/collez des données dans différents environnements Sandbox. Recherchez toujours des erreurs et effectuez les ajustements nécessaires.
* Notez que vous ne pouvez pas annuler une action. Pour supprimer des activités collées, vous devez les sélectionner et les supprimer. Vous devez donc veiller, avant de les copier, à ne sélectionner que les activités dont vous avez besoin.
* Vous pouvez copier des activités issues de n&#39;importe quel parcours, même celles qui sont en lecture seule.
* Vous pouvez sélectionner n&#39;importe quelle activité, même celles qui ne sont pas liées. Les activités liées resteront liées après avoir été collées.

Pour copier/coller des activités, procédez comme suit :

1. Ouvrez un parcours.
1. Sélectionnez les activités à copier en déplaçant la souris tout en cliquant dessus. Vous pouvez également cliquer sur chaque activité tout en appuyant sur la touche **Ctrl/Commande**. Utilisez **Ctrl/Commande + A** pour sélectionner toutes les activités.
   ![](assets/copy-paste1.png)
1. Appuyez sur **Ctrl/Commande + C**.
Si vous ne souhaitez copier qu&#39;une seule activité, vous pouvez cliquer dessus et utiliser l&#39;icône **Copier** en haut à gauche du volet de configuration de l&#39;activité.
   ![](assets/copy-paste2.png)
1. Dans un parcours quelconque, appuyez sur **Ctrl/Commande + V** pour coller les activités sans les lier à un nœud existant. Les activités collées sont placées dans le même ordre. Une fois collées, les activités restent sélectionnées pour que vous puissiez facilement les déplacer. Vous pouvez également placer le curseur sur un espace réservé vide et cliquer sur **Ctrl/Commande + V**. Les activités collées seront liées au nœud.
   ![](assets/copy-paste3.png)
