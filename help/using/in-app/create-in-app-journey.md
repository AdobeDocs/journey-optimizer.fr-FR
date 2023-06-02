---
title: Créer une notification in-app dans un parcours
description: Découvrez comment créer un message in-app dans Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
keywords: in-app, message, création, commencer
hide: true
hidefromtoc: true
exl-id: b774e34f-8225-41a0-a2ec-b91d3a86cf2b
badge: label="Beta" type="Informative"
source-git-commit: 8ca779efd237174c3ac9b7694b1cb81fc8b3ea3e
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 82%

---

# Créer un message in-app dans un parcours. {#create-in-app-journey}

1. Ouvrez votre parcours, puis effectuez un glisser-déposer d’une activité **[!UICONTROL In-app]** depuis la section **[!UICONTROL Actions]** de la palette.

   Lorsqu’un profil atteint la fin de son parcours, tous les messages in-app qui lui sont affichés expirent automatiquement. Pour cette raison, une activité d’attente est automatiquement ajoutée après votre activité in-app afin d’assurer un timing correct.

   ![](assets/in_app_journey_1.png)

1. Saisissez un **[!UICONTROL libellé]** et une **[!UICONTROL description]** pour votre message.

1. Choisissez la [surface in-app](inapp-configuration.md) à utiliser.

   ![](assets/in_app_journey_2.png)

1. Vous pouvez maintenant commencer à concevoir votre contenu à l’aide du bouton **[!UICONTROL Modifier le contenu]**. [En savoir plus](design-in-app.md).

1. Cliquez sur **[!UICONTROL Modifier le trigger]** pour configurer votre trigger.

   ![](assets/in_app_journey_4.png)

1. Dans la **[!UICONTROL Déclencheur de message in-app]** , sélectionnez le ou les événements et critères qui déclencheront votre message :

   1. Cliquez sur **[!UICONTROL Ajouter une condition]** si vous souhaitez que le déclencheur prenne en compte plusieurs événements ou critères.
   1. Dans la **[!UICONTROL Sélection d’un événement]** , sélectionnez le type d’événement de votre déclencheur.
   1. Sélectionnez le mode de liaison de vos événements, par exemple choisissez **[!UICONTROL And]** si vous voulez que les déclencheurs soient **tous les deux** vérifiés pour que le message s’affiche ou choisissez **[!UICONTROL Or]** si vous souhaitez que le message ne s’affiche que si **l’un ou l’autre** des déclencheurs est vérifié.
   1. Cliquez sur **[!UICONTROL Créer un groupe]** pour regrouper les déclencheurs.

   ![](assets/in_app_journey_3.png)

1. Sélectionnez la fréquence de déclenchement lorsque votre message in-app est principal :

   * **[!UICONTROL Afficher à chaque fois]** : toujours afficher le message lorsque les événements sélectionnés dans le menu déroulant **[!UICONTROL Déclencheur d’application mobile]** se produisent.
   * **[!UICONTROL Afficher une fois]** : n’afficher ce message que la première fois que les événements sélectionnés dans le menu déroulant **[!UICONTROL Déclencheur d’application mobile]** se produisent.
   * **[!UICONTROL Afficher jusqu’au clic]** : afficher ce message lorsque les événements sélectionnés dans le menu déroulant **[!UICONTROL Déclencheur d’application mobile]** se produisent jusqu’à ce qu’un événement d’interaction soit envoyé par le SDK avec une action « faisant l’objet d’un clic ».

1. Sélectionnez le jour de la semaine et l’heure spécifique à laquelle votre message in-app doit être déclenché, puis cliquez sur **[!UICONTROL Enregistrer]**.

1. Si nécessaire, complétez votre flux de parcours en faisant glisser et en déposant des actions ou des événements supplémentaires. [En savoir plus](../building-journeys/about-journey-activities.md).

1. Une fois votre message in-app prêt, finalisez la configuration et publiez votre parcours pour l’activer.

Pour plus d’informations sur la configuration de votre parcours, consultez cette [page](../building-journeys/journey-gs.md).

## Limites des activités in-app {#in-app-activity-limitations}

* Cette fonctionnalité n’est actuellement pas disponible pour les clientes et clients du secteur de la santé.

* La personnalisation ne peut contenir que des attributs de profil.

* L’affichage in-app est lié à la durée de parcours, ce qui signifie que lorsque le parcours se termine pour un profil, tous les messages in-app de ce parcours ne s’affichent plus pour ce profil.  Par conséquent, il n’est pas possible d’arrêter un message in-app directement à partir d’une activité de parcours. Vous devez plutôt terminer le parcours entier pour que les messages in-app ne s’affichent pas sur le profil.

* En mode test, l’affichage in-app dépend de la durée de vie du parcours. Pour éviter que le parcours ne se termine trop tôt au cours du test, ajustez la valeur **[!UICONTROL Temps d’attente]** de vos activités **[!UICONTROL Attente]**.

* Les activités **[!UICONTROL Réaction]** ne peuvent pas être utilisées pour réagir à une ouverture ou un clic in-app.

* Un délai d’activation peut survenir entre le moment où un profil utilisateur atteint une activité In-App dans la zone de travail et le moment où il commence à voir ce message in-app.

**Rubriques connexes :**

* [Concevoir un message in-app](design-in-app.md)
* [Tester et envoyer le message in-app](send-in-app.md)
* [Rapport in-app](../reports/campaign-global-report.md#inapp-report)
* [Configuration in-app](inapp-configuration.md)
