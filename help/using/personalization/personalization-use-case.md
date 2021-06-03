---
title: Cas d’utilisation de la personnalisation
description: Cas d’utilisation de la personnalisation
source-git-commit: cd1b07bbb4b247d1d8c0cc87be9e4bdad22377ed
workflow-type: tm+mt
source-wordcount: '606'
ht-degree: 95%

---


# Cas d’utilisation de la personnalisation {#personalization-use-case}

![](../assets/do-not-localize/badge.png)

Dans ce cas d’utilisation, vous verrez comment utiliser plusieurs types de personnalisation dans un seul message de notification push. Trois types de personnalisation seront utilisés :

* **Profil** : personnalisation des messages à partir d&#39;un champ de profil
* **Décision** de l’offre : personnalisation basée sur les variables de décision d’offre
* **Contexte** : personnalisation basée sur les données contextuelles du parcours

L’objectif de cet exemple est de pousser (push) un événement vers Journey Optimizer chaque fois qu’une commande client est mise à jour. Une notification push est ensuite envoyée au client avec des informations sur la commande et une offre personnalisée.

Pour ce cas d’utilisation, les conditions préalables suivantes doivent être remplies 

* Créer et concevoir un message de notification push sans le publier. Reportez-vous à cette [section](../create-message.md).
* Configurer un événement de commande incluant le numéro de commande, le statut et le nom de l’élément. Reportez-vous à cette [section](../event/about-events.md).
* Créez une décision (auparavant « activité d’offre ») ; consultez cette [section](../offers/offer-activities/create-offer-activities.md).

## Étape 1 - Ajouter une personnalisation au profil

1. Cliquez sur le menu **[!UICONTROL Message]**, puis sélectionnez votre message.

   ![](assets/perso-uc.png)

1. Cliquez sur le champ **Titre**.

   ![](assets/perso-uc2.png)

1. Saisissez l’objet et ajoutez la personnalisation de profil. Utilisez la barre de recherche pour rechercher le champ de prénom du profil. Dans le champ de texte de l’objet, placez le curseur à l’endroit où vous souhaitez insérer le champ de personnalisation, puis cliquez sur l’icône **+**. Cliquez sur **Enregistrer**.

   ![](assets/perso-uc3.png)

   >[!NOTE]
   >
   >Laissez le message à l’état préliminaire. Ne le publiez pas encore.

## Étape 2 - Créer le parcours

1. Cliquez sur le menu **[!UICONTROL Parcours]** et créez un parcours.

   ![](assets/perso-uc4.png)

1. Ajoutez votre événement d’entrée, un **Message** et une activité **Fin**.

   ![](assets/perso-uc5.png)

1. Dans l’activité **Message**, sélectionnez le message précédemment créé. Cliquez sur **OK**.

   ![](assets/perso-uc6.png)

   Un message s’affiche pour vous informer que les données de l’événement d’entrée et les propriétés du parcours ont été transmises au message.

   ![](assets/perso-uc7.png)

   >[!NOTE]
   >
   >Le message s’affiche avec une icône d’avertissement. En effet, le message n’est pas encore publié.

## Étape 3 - Ajouter une personnalisation aux données contextuelles

1. Dans l’activité **Message**, cliquez sur l’icône **Ouvrir le message**. Le message s’ouvre dans un nouvel onglet.

   ![](assets/perso-uc8.png)

1. Cliquez sur le champ **Titre**.

   ![](assets/perso-uc9.png)

1. Sélectionnez la catégorie **Contexte**. Cet élément n’est disponible que si un parcours a transmis des données contextuelles au message. Cliquez sur **Journey Orchestration**. Les informations contextuelles suivantes s’affichent :

   * **Événements** : cette catégorie regroupe tous les champs du ou des événements placés avant l’activité **Message** dans le parcours.
   * **Propriétés du parcours** : champs techniques liés au parcours pour un profil donné ; par exemple, identifiant du parcours ou erreurs spécifiques rencontrées. Consultez la [documentation de Journey Orchestration](https://experienceleague.adobe.com/docs/journeys/using/building-advanced-conditions-journeys/syntax/journey-properties.html#building-advanced-conditions-journeys).

   ![](assets/perso-uc10.png)

1. Développez l’élément **Événements** et recherchez le champ du numéro de commande associé à votre événement. Vous pouvez également utiliser la zone de recherche. Cliquez sur l’icône **+** pour insérer le champ de personnalisation dans le texte de l’objet. Cliquez sur **Enregistrer**.

   ![](assets/perso-uc11.png)

1. Cliquez maintenant sur le champ **Corps**.

   ![](assets/perso-uc12.png)

1. Tapez le message et, à partir de la catégorie **Contexte**, insérez le nom de l’élément de commande et la progression de la commande.

   ![](assets/perso-uc13.png)

1. Dans la liste déroulante, sélectionnez **Décision d’offre** pour insérer une variable de prise de décision d’offre. Sélectionnez l’emplacement et cliquez sur l’icône **+** en regard de la décision (auparavant « activité d’offre ») pour l’ajouter au corps.

   ![](assets/perso-uc14.png)

1. Cliquez sur Valider pour vous assurer qu’il n’y a aucune erreur, puis sur **Enregistrer**.

   ![](assets/perso-uc15.png)

1. Publiez à présent le message.

   ![](assets/perso-uc16.png)

## Étape 4 - Tester et publier le parcours

1. Ouvrez de nouveau le parcours. Si le parcours est déjà ouvert, veillez à actualiser la page. Maintenant que le message est publié, vous pouvez constater qu’il n’y a aucune erreur dans le parcours. Cliquez sur le bouton **Test**, puis sur **Déclencher un événement**.

   ![](assets/perso-uc17.png)

1. Entrez les différentes valeurs à transmettre dans le test. Le mode test ne fonctionne qu’avec les profils de test. L’identifiant de profil doit correspondre à un profil de test. Cliquez sur **Envoyer**.

   ![](assets/perso-uc18.png)

   La notification push est envoyée et affichée sur le téléphone portable du profil de test.

   ![](assets/perso-uc19.png)

1. Vérifiez qu’il n’y a pas d’erreur et publiez le parcours.

