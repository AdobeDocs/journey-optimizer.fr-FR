---
title: Concevez votre parcours
description: Découvrez comment concevoir votre parcours
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '1437'
ht-degree: 0%

---

# Concevez votre parcours

![](../assets/do-not-localize/badge.png)

L’interface de parcours vous permet de faire glisser et déposer facilement des activités de la palette dans la zone de travail. Vous pouvez également cliquer sur une activité en doublon pour l’ajouter dans la trame à l’étape suivante disponible. Chaque activité a un rôle et une place spécifiques dans le processus. Les activités sont séquencées. Lorsqu’une activité est terminée, le flux se poursuit et traite l’activité suivante, etc.

## Commencer avec la conception de parcours

La **palette** se trouve sur le côté gauche de l’écran. Toutes les activités disponibles sont triées en plusieurs catégories : **[!UICONTROL Événements]**, **[!UICONTROL Orchestration]** et **[!UICONTROL Actions]**. Vous pouvez développer/réduire les différentes catégories en cliquant sur leur nom. Pour utiliser une activité dans votre parcours, faites-la glisser de la palette vers votre canevas.

Lors du démarrage d’un nouveau parcours, les éléments qui ne peuvent pas être déposés dans la trame comme première étape sont masqués. Cela concerne toutes les actions, l&#39;activité de la condition, l&#39;attente et la réaction.

![](../assets/journey38.png)

L&#39;icône **[!UICONTROL Filtrer les éléments]** dans le coin supérieur gauche vous permet d&#39;afficher les filtres suivants :

* **Afficher uniquement les éléments** disponibles : masquez ou affichez les éléments indisponibles dans la palette, par exemple les événements qui utilisent un espace de nommage différent de celui utilisé dans votre parcours. Par défaut, les éléments non disponibles sont masqués. Si vous choisissez de les afficher, elles apparaîtront grisées.

* **Afficher uniquement les éléments** récents : ce filtre vous permet d&#39;afficher uniquement les cinq derniers événements et actions utilisés, en plus de ceux prêts à l&#39;emploi. Il est spécifique à chaque utilisateur. Par défaut, tous les éléments sont affichés.

Vous pouvez également utiliser le champ **[!UICONTROL Rechercher]**.

La zone de travail **canvas** est la zone centrale du concepteur de parcours. C&#39;est dans cette zone que vous pouvez déposer vos activités et les configurer. Cliquez sur une activité dans la trame pour la configurer. Le volet de configuration de l&#39;activité s&#39;ouvre alors sur le côté droit.

![](../assets/journey39.png)

Le **volet de configuration de l&#39;activité** s&#39;affiche lorsque vous cliquez sur une activité de la palette. Renseignez les champs obligatoires. Cliquez sur l&#39;icône **[!UICONTROL Supprimer]** pour supprimer l&#39;activité. Cliquez sur **[!UICONTROL Annuler]** pour annuler les modifications ou **[!UICONTROL Ok]** pour confirmer. Pour supprimer des activités, vous pouvez également sélectionner une ou plusieurs activités et appuyer sur la touche Retour arrière. Appuyez sur la touche d&#39;échappement pour fermer le volet de configuration de l&#39;activité.

Par défaut, les champs en lecture seule sont masqués. Pour les afficher, cliquez sur l&#39;icône **Afficher les champs en lecture seule** en haut à gauche du volet de configuration de l&#39;activité.

![](../assets/journey59bis.png)

Selon l’état du parcours, vous pouvez exécuter différentes actions sur votre parcours à l’aide des boutons disponibles dans le coin supérieur droit : **[!UICONTROL Publier]**, **[!UICONTROL Duplicata]**, **[!UICONTROL Supprimer]**, **[!UICONTROL propriétés du Parcours]**, **[!UICONTROL Test]**. Ces boutons s’affichent lorsqu’aucune activité n’est sélectionnée. Certains boutons s’affichent dans le contexte. Le bouton journal du mode test s&#39;affiche lorsque le mode test est activé.

![](../assets/journey41.png)

## Démarrage de votre parcours

Lorsque vous concevez votre parcours, la première question que vous voulez poser est comment les profils vont entrer dans le parcours. Il existe deux possibilités :

**Début avec événement** : lorsqu&#39;un parcours est prêt à écouter les événements, les individus entrent dans l&#39; **** unité du parcours en temps réel. Les messages inclus dans votre parcours sont envoyés à la personne qui arrive actuellement dans le parcours. [En savoir plus sur les événements](../event/about-events.md)

**Début avec un segment** Lu : vous pouvez définir votre parcours pour écouter les segments Adobe Experience Platform. Dans ce cas, toutes les personnes appartenant au segment spécifié entrent dans le parcours. Les messages inclus dans votre parcours sont envoyés aux personnes appartenant au segment. [En savoir plus sur la lecture de segments](read-segment.md).

## Définir les étapes suivantes

Après votre premier événement ou segment de lecture, vous pouvez combiner les différentes activités afin de créer vos scénarios de canaux croisés en plusieurs étapes. Choisissez, dans la palette, les étapes dont vous avez besoin.

**Événements**

Lorsque vous début votre parcours avec un événement, le parcours est déclenché à la réception du événement. La personne suivra ensuite, individuellement, les étapes suivantes définies dans votre parcours.

Vous pouvez ajouter **plusieurs événements** dans votre parcours, à condition qu’ils utilisent le même espace de nommage. Les événements sont configurés au préalable. [En savoir plus sur les événements](about-journey-activities.md#event-activities)

Vous pouvez également ajouter un événement **Réaction** après un message pour réagir aux données de suivi liées au message. Cela vous permet, par exemple, d’envoyer un autre message si l’utilisateur a ouvert le message précédent ou cliqué dessus. Pour en savoir plus, consultez cette [section](reaction-events.md).

L&#39;activité d&#39;événement **Qualification de segment** vous permet de faire entrer ou avancer des individus dans un parcours en fonction des entrées et sorties de segments Adobe Experience Platform. Vous pouvez faire entrer tous les nouveaux clients argentés dans un parcours et envoyer des messages personnalisés. Pour en savoir plus, consultez cette [section](segment-qualification-events.md).

**Orchestration**

Dans les activités d&#39;orchestration, vous trouverez l&#39;activité **Lire segment** qui vous permet de définir votre parcours pour écouter un segment Adobe Experience Platform. [En savoir plus sur l’activité](read-segment.md) du segment Lu.

Les autres activités vous permettent d’ajouter des conditions à votre parcours afin de définir plusieurs chemins, de définir un délai d’attente avant l’exécution de l’activité suivante ou de terminer votre parcours. Pour en savoir plus, consultez cette [section](about-journey-activities.md#orchestration-activities).

**Actions**

Vous trouverez ici l&#39;activité **Message** qui vous permet d&#39;inclure un message conçu dans Journey Optimizer. [En savoir plus sur l&#39;activité de message](journeys-message.md)

Vous trouverez également les actions personnalisées que vous avez configurées pour envoyer des messages avec des systèmes tiers. Pour en savoir plus, consultez cette [section](about-journey-activities.md#action-activities).

## Utilisation des chemins dans la trame {#paths}

Plusieurs activités (**[!UICONTROL Condition]**, **[!UICONTROL Action]** activités) vous permettent de définir une action de secours en cas d&#39;erreur ou d&#39;expiration. Dans le volet de configuration de l&#39;activité, cochez la case : **[!UICONTROL Ajouter un autre chemin en cas de dépassement de délai ou d&#39;erreur]**. Un autre chemin est ajouté après l’activité. La durée du délai d’expiration est définie dans les propriétés du parcours (voir [cette page](../building-journeys/journey-gs.md#change-properties) par un utilisateur administrateur. Par exemple, si l&#39;envoi d&#39;un courriel prend trop de temps ou est erroné, vous pouvez décider d&#39;envoyer un SMS.

![](../assets/journey42.png)

Diverses activités (événement, action, attente) vous permettent d’ajouter plusieurs chemins. Pour ce faire, placez votre curseur sur l&#39;activité et cliquez sur le symbole &quot;+&quot;. Seules les activités de événement et d’attente peuvent être définies en parallèle. Si plusieurs événements sont définis en parallèle, le chemin choisi sera celui du premier événement.

Lorsque vous écoutez un événement, nous vous recommandons de ne pas attendre le événement indéfiniment. Ce n&#39;est pas obligatoire, juste une bonne pratique. Si vous souhaitez écouter un ou plusieurs événements seulement pendant une certaine période, vous placez un ou plusieurs événements et une activité d&#39;attente en parallèle. Voir [cette section](../building-journeys/general-events.md#events-specific-time).

Pour supprimer le chemin, placez le curseur dessus et cliquez sur l&#39;icône **[!UICONTROL Supprimer la flèche]**.

![](../assets/journey42ter.png)

Dans la trame, lorsque deux activités sont déconnectées, un avertissement s’affiche. Placez votre curseur sur l’icône d’avertissement pour afficher le message d’erreur. Pour résoudre le problème, il vous suffit de déplacer l’activité déconnectée et de la connecter à l’activité précédente.

![](../assets/canvas-disconnected.png)

## Copie et collage des activités {#copy-paste}

Vous pouvez copier une ou plusieurs activités d’un parcours et les coller dans le même parcours ou dans un autre. Cela vous permet de gagner du temps si vous souhaitez réutiliser de nombreuses activités qui ont déjà été configurées dans un parcours précédent.

**Remarques importantes**

* Vous pouvez copier/coller sur différents onglets et navigateurs. Vous pouvez uniquement copier/coller des activités dans la même instance.
* Vous ne pouvez pas copier/coller un événement si le parcours de destination comporte un événement qui utilise un autre espace de nommage.
* Les activités collées peuvent référencer des données qui n’existent pas dans le parcours de destination, par exemple si vous copiez/collez des données sur différents sandbox. Vérifiez toujours les erreurs et effectuez les ajustements nécessaires.
* Notez que vous ne pouvez pas annuler une action. Pour supprimer des activités collées, vous devez les sélectionner et les supprimer. Par conséquent, veillez à ne sélectionner que les activités dont vous avez besoin avant de les copier.
* Vous pouvez copier des activités de n’importe quel parcours, même celles qui sont en lecture seule.
* Vous pouvez sélectionner n’importe quelle activité, même celles qui ne sont pas liées. Les activités liées resteront liées après avoir été collées.

Pour copier/coller des activités, procédez comme suit :

1. Ouvrez un parcours.
1. Sélectionnez les activités à copier en déplaçant la souris tout en cliquant dessus. Vous pouvez également cliquer sur chaque activité tout en appuyant sur la touche **Ctrl/Commande**. Utilisez **Ctrl/Commande + A** si vous souhaitez sélectionner toutes les activités.
   ![](../assets/copy-paste1.png)
1. Appuyez sur **Ctrl/Commande + C**.
Si vous ne souhaitez copier qu&#39;une seule activité, vous pouvez cliquer dessus et utiliser l&#39;icône **Copier** en haut à gauche du volet de configuration de l&#39;activité.
   ![](../assets/copy-paste2.png)
1. Dans n’importe quel parcours, appuyez sur **Ctrl/Commande + V** pour coller les activités sans les lier à un noeud existant. Les activités collées sont placées dans le même ordre. Une fois collées, les activités restent sélectionnées afin que vous puissiez facilement les déplacer. Vous pouvez également placer le curseur sur un espace réservé vide et cliquer sur **Ctrl/Commande + V**. Les activités collées seront liées au noeud.
   ![](../assets/copy-paste3.png)
