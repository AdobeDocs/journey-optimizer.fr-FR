---
title: Cas d’utilisation de parcours
description: Cas d’utilisation de parcours
feature: Parcours
topic: Gestion de contenu
role: User
level: Intermediate
source-git-commit: 62d83f69ebf50f36688e3db956bb3860a468c2d6
workflow-type: tm+mt
source-wordcount: '862'
ht-degree: 89%

---

# Envoi de messages à plusieurs canaux

Cette section présente un cas pratique qui combine un segment de lecture, un événement, des événements de réaction et des messages électroniques/push.

![](../assets/jo-uc1.png)

## Description du cas d’utilisation

Dans ce cas d’utilisation, nous souhaitons envoyer un premier message (email et push) à tous les clients appartenant à un segment spécifique.

Sur la base de leur réaction au premier message, nous voulons envoyer des messages spécifiques.

Après le premier message, nous attendons un jour que les clients ouvrent le message push ou l&#39;email. S&#39;il n&#39;y a pas de réaction, nous leur envoyons un email de relance.

Ensuite, nous attendons un achat et envoyons un message push pour remercier le client.

## Prérequis

Pour que ce cas d&#39;utilisation fonctionne, vous devez configurer les éléments suivants :

* un segment pour tous les clients qui habitent à Atlanta, San Francisco ou Seattle et qui sont nés après 1980.
* un événement d&#39;achat
* trois messages

### Création du segment

Dans notre parcours, nous voulons utiliser un segment spécifique de clients. Tous les individus appartenant au segment rejoignent le parcours et suivent les différentes étapes. Dans notre exemple, nous avons besoin d&#39;un segment qui cible tous les clients qui vivent à Atlanta, San Francisco ou Seattle et qui sont nés après 1980.

Pour plus d’informations sur les segments, consultez cette [page](../segment/about-segments.md).

1. Dans la section du menu CLIENT , sélectionnez **[!UICONTROL Segments]**.

1. Cliquez sur le bouton **[!UICONTROL Créer un segment]** situé en haut à droite de la liste de segments.

1. Dans le volet **[!UICONTROL Propriétés de segment]**, saisissez le nom du segment.

1. Réalisez un glisser-déposer dans les champs de votre choix depuis le volet de gauche vers l’espace de travail central, puis configurez-les en fonction de vos besoins. Dans cet exemple, nous utilisons les champs d’attributs **Ville** et **Année de naissance**.

1. Cliquez sur **[!UICONTROL Enregistrer]**.

   ![](../assets/add-attributes.png)

Le segment est maintenant configuré et prêt à être utilisé dans votre parcours. À l’aide d’une activité **Lecture de segment** , vous pouvez faire entrer dans le parcours toutes les personnes appartenant au segment.

### Configurer l’événement

Vous devez configurer un événement qui est envoyé à votre parcours lorsqu’un client effectue un achat. Lorsque le parcours reçoit l&#39;événement, il déclenche le message de remerciement.

Pour cela, nous utilisons un événement basé sur des règles. Pour plus d’informations sur les événements, consultez cette [page](../event/about-events.md).

1. Dans la section du menu ADMINISTRATION, sélectionnez **[!UICONTROL Configurations]**, puis cliquez sur **[!UICONTROL Événements]**. Cliquez sur **[!UICONTROL Créer un événement]** pour créer un événement.

1. Saisissez le nom de votre événement.

1. Dans le champ **[!UICONTROL Type d’identifiant d’événement]**, sélectionnez **[!UICONTROL Basé sur des règles]**.

1. Définissez les champs **[!UICONTROL Schéma]** et **[!UICONTROL Payload]**. Vous pouvez utiliser plusieurs champs, par exemple, le produit acheté, la date d’achat et l’identifiant d’achat.

1. Dans le champ **[!UICONTROL Condition d’identifiant d’événement]**, définissez la condition utilisée par le système pour identifier les événements qui déclenchent votre parcours. Par exemple, vous pouvez ajouter un champ `purchaseMessage` et définir la règle suivante : `purchaseMessage="thank you"`

1. Définissez l’ **[!UICONTROL espace de noms]** et l’**[!UICONTROL identifiant de profil]**.

1. Cliquez sur **[!UICONTROL Enregistrer]**.

   ![](../assets/jo-uc2.png)

L&#39;événement maintenant configuré et prêt à être utilisé dans votre parcours. À l’aide de l’activité d&#39;événement correspondante, vous pouvez déclencher une action chaque fois qu’un client effectue un achat.

### Créer les messages

Pour ce cas d’utilisation, nous devons créer trois messages :

* un premier message push et email
* un message de remerciement push
* un email de relance

![](../assets/jo-uc3.png)

Consultez cette [section](../segment/about-segments.md) pour savoir comment concevoir et publier ces messages.

## Concevoir le parcours

1. Commencez le parcours par une activité **Lecture de segment** . Sélectionnez le segment créé précédemment. Tous les individus appartenant au segment rejoignent le parcours.

   ![](../assets/jo-uc4.png)

1. Déposez une activité **Message** et sélectionnez le premier message push et email. Ce message est envoyé à tous individus dans le parcours.

   ![](../assets/jo-uc5.png)

1. Placez votre curseur sur l&#39;activité du message et cliquez sur le symbole « + » pour créer un nouveau chemin.

1. Dans le premier chemin, ajoutez un événement **Réaction** et sélectionnez **Notification push ouverte**. L&#39;événement est déclenché lorsqu’un individu appartenant au segment ouvre la version push du premier message.

1. Dans le second chemin, ajoutez un événement **Réaction** et sélectionnez **Email ouvert**. L&#39;événement est déclenché lorsque l’individu ouvre l’email.

1. Dans l&#39;une des activités de la réaction, cochez la case **Définir la temporisation de l&#39;événement**, définissez une durée (1 jour dans notre exemple) et cochez **Ajouter un itinéraire de temporisation**. Cela crée un autre itinéraire pour les individus qui n’ouvrent pas le premier message push ou l’email.

   >[!NOTE]
   >
   >Lors de la configuration d’une temporisation sur plusieurs événements (les deux réactions dans ce cas), il vous suffit de configurer la temporisation sur l’un de ces événements.

1. Dans l’itinéraire de temporisation, déposez une activité **Message** et sélectionnez l’email de relance. Ce message est envoyé aux individus qui n’ouvrent pas le premier email ou la première notification push le lendemain.

1. Connectez les trois chemins à l&#39;événement d’achat créé précédemment. L&#39;événement est déclenché lorsqu’un individu effectue un achat.

1. Après l&#39;événement, déposez une activité **Message** et sélectionnez le message de remerciement.

1. Ajoutez une activité **Fin**.

## Tester et publier le parcours

1. Avant de tester votre parcours, vérifiez qu’il est valide et qu’il ne comporte aucune erreur,

1. Cliquez sur la bascule **Test** située dans le coin supérieur droit pour activer le mode test. Définissez comment vous souhaitez que les profils de test rejoignent le test : un seul profil, ou jusqu&#39;à 100 à la fois. Reportez-vous à cette [section](testing-the-journey.md) pour savoir comment utiliser le mode test.

1. Lorsque le parcours est prêt, publiez-le à l’aide du bouton **Publier** situé dans le coin supérieur droit.
