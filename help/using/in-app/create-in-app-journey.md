---
title: Créer une notification In-App dans un Parcours
description: Découvrez comment créer un message in-app dans Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: in-app, message, création, commencer
hide: true
hidefromtoc: true
exl-id: b774e34f-8225-41a0-a2ec-b91d3a86cf2b
source-git-commit: 252011710574122c1f321a388b65bdafb7c666df
workflow-type: tm+mt
source-wordcount: '553'
ht-degree: 46%

---

# Créer un message in-app dans un Parcours {#create-in-app-journey}

>[!AVAILABILITY]
>
>L’activité In-App est actuellement disponible en version bêta pour sélectionner uniquement les utilisateurs. Pour rejoindre le programme bêta, contactez l’assistance clientèle d’Adobe.

1. Ouvrez votre parcours, puis effectuez un glisser-déposer d’un **[!UICONTROL In-app]** de l’activité **[!UICONTROL Actions]** de la palette.

   Lorsqu’un profil atteint la fin de son parcours, tous les messages in-app qui lui sont affichés expirent automatiquement. Pour cette raison, une activité Attente est automatiquement ajoutée après votre activité In-App afin d’assurer un timing correct.

   ![](assets/in_app_journey_1.png)

1. Saisissez un **[!UICONTROL Libellé]** et **[!UICONTROL Description]** pour votre message.

1. Choisissez la [Surface in-app](inapp-configuration.md) à utiliser.

   ![](assets/in_app_journey_2.png)

1. Vous pouvez maintenant commencer à concevoir votre contenu à l’aide du bouton **[!UICONTROL Modifier le contenu]**. [En savoir plus](design-in-app.md).

1. Cliquez sur **[!UICONTROL Modifier le déclencheur]** pour configurer votre déclencheur.

   ![](assets/in_app_journey_4.png)

1. Sélectionnez la fréquence de votre déclencheur lorsque votre message in-app est actif :

   * **[!UICONTROL Afficher à chaque fois]** : toujours afficher le message lorsque les événements sélectionnés dans le menu déroulant **[!UICONTROL Déclencheur d’application mobile]** se produisent.
   * **[!UICONTROL Afficher une fois]** : n’afficher ce message que la première fois que les événements sélectionnés dans le menu déroulant **[!UICONTROL Déclencheur d’application mobile]** se produisent.
   * **[!UICONTROL Afficher jusqu’au clic]** : afficher ce message lorsque les événements sélectionnés dans le menu déroulant **[!UICONTROL Déclencheur d’application mobile]** se produisent jusqu’à ce qu’un événement d’interaction soit envoyé par le SDK avec une action « faisant l’objet d’un clic ».

1. Dans le ou les menus déroulants **[!UICONTROL Déclencheur d’application mobile]**, choisissez le ou les événements et les critères qui déclencheront votre message :

   1. Dans le menu déroulant de gauche, sélectionnez l’événement nécessaire pour déclencher le message.
   1. Dans le menu déroulant de droite, sélectionnez la validation requise pour l’événement sélectionné.
   1. Cliquez sur le bouton **[!UICONTROL Ajouter]** si vous souhaitez que le déclencheur prenne en compte plusieurs événements ou critères. Répétez ensuite les étapes ci-dessus.
   1. Sélectionnez le mode de liaison de vos événements, par exemple choisissez **[!UICONTROL And]** si vous voulez que les déclencheurs soient **tous les deux** vérifiés pour que le message s’affiche ou choisissez **[!UICONTROL Or]** si vous souhaitez que le message ne s’affiche que si **l’un ou l’autre** des déclencheurs est vérifié.
   1. Cliquez sur **[!UICONTROL Enregistrer]** une fois vos déclencheurs configurés.

   ![](assets/in_app_journey_3.png)

1. Si nécessaire, complétez votre flux de parcours en faisant glisser et en déposant des actions ou des événements supplémentaires. [En savoir plus](../building-journeys/about-journey-activities.md).

1. Une fois votre message in-app prêt, finalisez la configuration et publiez votre parcours pour l’activer.

Pour plus d’informations sur la configuration de votre parcours, consultez cette [page](../building-journeys/journey-gs.md).

## Limites des activités in-app {#in-app-activity-limitations}

* Cette fonctionnalité n’est actuellement pas disponible pour les clients du secteur de la santé.

* La personnalisation ne peut contenir que des attributs de profil.

* L’affichage in-app est lié à la durée de parcours, ce qui signifie que lorsque le parcours se termine pour un profil, tous les messages in-app de ce parcours ne s’affichent plus pour ce profil.  Par conséquent, il n’est pas possible d’arrêter un message In-App directement à partir d’une activité de parcours. Vous devrez plutôt terminer le parcours entier pour que les messages In-App ne s’affichent pas sur le profil.

* En mode test, l’affichage In-App dépend de la durée de vie du parcours. Pour éviter que le parcours ne se termine trop tôt au cours du test, ajustez la variable **[!UICONTROL Temps d’attente]** pour votre **[!UICONTROL Attente]** activités.

* **[!UICONTROL Réaction]** Les activités ne peuvent pas être utilisées pour réagir à une ouverture ou à un clic In-App.

* Un délai d’activation se produit entre le moment où un profil utilisateur atteint une activité In-App dans la zone de travail et le moment où il commence à voir ce message in-app. Ce délai peut aller de 15 minutes à 1 heure.

**Rubriques connexes :**

* [Concevoir un message in-app](design-in-app.md)
* [Tester et envoyer le message in-app](send-in-app.md)
* [Rapport in-app](../reports/campaign-global-report.md#inapp-report)
* [Configuration in-app](inapp-configuration.md)
