---
title: Cas d’utilisation des parcours
description: Cas d’utilisation des parcours
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '842'
ht-degree: 7%

---

# Cas d&#39;utilisation du parcours

![](../assets/do-not-localize/badge.png)

Cette section présente un cas d’utilisation qui combine un segment Lu, un événement, des événements de réaction et des messages électroniques/push.

![](../assets/jo-uc1.png)

## Description du cas d’utilisation

Dans ce cas d’utilisation, nous souhaitons envoyer un premier message (courrier électronique et push) à tous les clients appartenant à un segment spécifique.

Sur la base de leur réaction au premier message, nous voulons envoyer des messages spécifiques.

Après le premier message, nous attendons un jour que les clients ouvrent le message push ou e-mail. S&#39;il n&#39;y a pas de réaction, nous leur envoyons un courriel de suivi.

Ensuite, nous attendons un achat et envoyons un message push pour remercier le client.

## Conditions préalables  

Pour que cette utilisation fonctionne, vous devez configurer les éléments suivants :

* un segment pour tous les clients qui habitent à Atlanta, San Francisco ou Seattle et qui sont nés après 1980.
* un événement d&#39;achat
* trois messages

### Création du segment

Dans notre parcours, nous voulons exploiter un segment spécifique de clients. Toutes les personnes appartenant au segment entrent dans le parcours et suivent les différentes étapes. Dans notre exemple, nous avons besoin d&#39;un segment qui cible tous les clients qui vivent à Atlanta, San Francisco ou Seattle et qui sont nés après 1980.

Pour plus d&#39;informations sur les segments, consultez cette [page](../segment/about-segments.md).

1. Dans le menu **[!UICONTROL Segments]**, cliquez sur **[!UICONTROL Créer un segment]**.

1. Dans le volet **[!UICONTROL Propriétés de segment]**, saisissez le nom du segment.

1. Faites glisser et déposez les champs de votre choix depuis le volet de gauche vers l’espace de travail central, puis configurez-les en fonction de vos besoins. Dans cet exemple, nous utilisons les champs d’attributs **Ville** et **Année de naissance**.

1. Cliquez sur **[!UICONTROL Enregistrer]**.

   ![](../assets/add-attributes.png)

Le segment est maintenant créé et prêt à être utilisé dans votre parcours. En utilisant une activité **Lire le segment**, vous pouvez faire entrer dans le parcours toutes les personnes appartenant au segment.

### Configuration du événement

Vous devez configurer un événement qui est envoyé à votre parcours lorsqu’un client effectue un achat. Lorsque le parcours reçoit le événement, il déclenche le message de remerciement.

Pour cela, nous utilisons un événement fondé sur des règles. Pour plus d&#39;informations sur les événements, consultez cette [page](../event/about-events.md).

1. Dans le menu de gauche, cliquez sur l’icône **[!UICONTROL Administration]**, puis sur **[!UICONTROL Événements]**. Cliquez sur **[!UICONTROL Ajouter]** pour créer un événement.

1. Saisissez le nom de votre événement.

1. Dans le champ **[!UICONTROL Événement ID type]**, sélectionnez **[!UICONTROL Règle basée sur]**.

1. Définissez les champs **[!UICONTROL Schéma]** et **[!UICONTROL Payload]**. Vous pouvez utiliser plusieurs champs, par exemple, le produit acheté, la date d’achat et l’identifiant d’achat.

1. Dans le champ **[!UICONTROL Événement ID condition]**, définissez la condition utilisée par le système pour identifier les événements qui déclenchent votre parcours. Par exemple, vous pouvez ajouter un champ `purchaseMessage` et définir la règle suivante : `purchaseMessage="thank you"`

1. Définissez l’**[!UICONTROL espace de noms]** et la **[!UICONTROL clé]**.

1. Cliquez sur **[!UICONTROL Enregistrer]**.

   ![](../assets/jo-uc2.png)

Le événement est maintenant configuré et prêt à être utilisé dans votre parcours. A l’aide de l’activité de événement correspondante, vous pouvez déclencher une action chaque fois qu’un client effectue un achat.

### Créer les messages

Pour ce cas d’utilisation, nous devons créer trois messages :

* un premier message push et email
* un message de remerciement Push
* un message de suivi par courrier électronique ;

![](../assets/jo-uc3.png)

Reportez-vous à cette [section](../segment/about-segments.md) pour savoir comment concevoir et publier ces messages.

## Conception du parcours

1. Début le parcours avec une activité **Lire le segment**. Sélectionnez le segment créé précédemment. Toutes les personnes appartenant au segment entrent dans le parcours.

   ![](../assets/jo-uc4.png)

1. Déposez une activité **Message** et sélectionnez le premier message push et email. Ce message est envoyé à toutes les personnes du parcours.

   ![](../assets/jo-uc5.png)

1. Placez votre curseur sur l&#39;activité du message et cliquez sur le symbole &quot;+&quot; pour créer un nouveau chemin.

1. Dans le premier chemin, ajoutez un événement **Réaction** et sélectionnez **Pousser ouverte**. Le événement est déclenché lorsqu’une personne appartenant au segment ouvre la version Push du premier message.

1. Dans le second chemin, ajoutez un événement **Réaction** et sélectionnez **E-mail ouvert**. Le événement est déclenché lorsque l’utilisateur ouvre le courrier électronique.

1. Dans l&#39;une des activités de la réaction, cochez la case **Définir le délai d&#39;expiration du événement**, définissez une durée (1 jour dans notre exemple) et **Définissez un délai d&#39;expiration**. Cela crée un autre chemin pour les personnes qui n’ouvrent pas le premier message push ou email.

   >[!NOTE]
   >
   >Lors de la configuration d’un délai d’attente sur plusieurs événements (les deux réactions dans ce cas), il vous suffit de configurer le délai d’attente sur l’un de ces événements.

1. Dans le chemin du délai d’expiration, déposez une activité **Message** et sélectionnez le message de suivi du courrier électronique. Ce message est envoyé aux personnes qui n’ouvrent pas le courriel ou ne font pas passer le premier message le lendemain.

1. Connectez les trois chemins au événement d’achat créé précédemment. Le événement est déclenché lorsqu’une personne effectue un achat.

1. Après le événement, déposez une activité **Message** et sélectionnez le message de remerciement.

1. Ajoutez une activité **Fin**.

## Tester et publier le parcours

1. Avant de tester votre parcours, vérifiez qu’il est valide et qu’il ne comporte aucune erreur,

1. Cliquez sur la bascule **Test** située dans le coin supérieur droit pour activer le mode test. Définissez comment vous souhaitez que les profils de test entrent dans le test : un seul profil, ou jusqu&#39;à 100 à la fois. Reportez-vous à cette [section](testing-the-journey.md) pour savoir comment utiliser le mode test.

1. Lorsque le parcours est prêt, publiez-le à l’aide du bouton **Publier** situé dans le coin supérieur droit.
