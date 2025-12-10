---
solution: Journey Optimizer
product: journey optimizer
title: 'Cas d’utilisation de la personnalisation : notification du statut de la commande'
description: Découvrez comment personnaliser un message à l’aide des informations de profil, de décision d’offres et de contexte.
feature: Personalization, Use Cases
topic: Personalization
role: Developer
level: Intermediate
keywords: expression, éditeur, cas d’utilisation, personnalisation
exl-id: 7d9c3d31-af57-4f41-aa23-6efa5b785260
source-git-commit: 619db0a371b96fbe9480300a874839b7b919268d
workflow-type: tm+mt
source-wordcount: '531'
ht-degree: 100%

---

# Cas d’utilisation de la personnalisation : notification du statut de la commande {#personalization-use-case}

Dans ce cas d&#39;utilisation, vous verrez comment utiliser plusieurs types de personnalisations dans un seul message de notification push. Trois types de personnalisations seront utilisés :

* **Profil** : personnalisation des messages en fonction d&#39;un champ de profil
* **Décision d’offre** : personnalisation basée sur des variables de gestion des décisions
* **Contexte** : personnalisation basée sur les données contextuelles du parcours

L&#39;objectif de cet exemple est de pousser (push) un événement vers [!DNL Journey Optimizer] chaque fois qu&#39;une commande client est mise à jour. Une notification push est ensuite envoyée au client avec des informations sur la commande et une offre personnalisée.

Pour ce cas d&#39;utilisation, les conditions préalables suivantes doivent être remplies

* Configurer un événement de commande incluant le numéro de commande, le statut et le nom de l&#39;article. Reportez-vous à cette [section](../event/about-events.md).
* Créer une décision, voir à ce sujet cette [section](../offers/offer-activities/create-offer-activities.md).

➡️ [Découvrir un cas d’utilisation similaire en vidéo](#video)

## Étape 1 - Créer le parcours {#create-journey}

1. Cliquez sur le menu **[!UICONTROL Parcours]** et créez un parcours.

   ![](assets/perso-uc4.png)

1. Ajoutez votre événement d’entrée et une activité d’action **Push**.

   ![](assets/perso-uc5.png)

1. Configurez et concevez votre message de notification push. Reportez-vous à cette [section](../push/create-push.md).

## Étape 2 - Ajouter une personnalisation au profil {#add-perso}

1. Dans l’activité **Push**, cliquez sur **Modifier le contenu**.

1. Cliquez sur le champ **Titre**.

   ![](assets/perso-uc2.png)

1. Saisissez l’objet et ajoutez la personnalisation de profil. Utilisez la barre de recherche pour rechercher le champ de prénom du profil. Dans le texte de l&#39;objet, placez le curseur à l&#39;endroit où vous souhaitez insérer le champ de personnalisation, puis cliquez sur l&#39;icône **+**. Cliquez sur **Enregistrer**.

   ![](assets/perso-uc3.png)

## Étape 3 - Ajouter une personnalisation aux données contextuelles {#add-perso-contextual-data}

1. Dans l’activité **Push**, cliquez sur **Modifier le contenu** et cliquez sur le champ **Titre**.

   ![](assets/perso-uc9.png)

1. Sélectionnez le menu **Attributs contextuels**. Les attributs contextuels ne sont disponibles que si un parcours a transmis des données contextuelles au message. Cliquez sur **Journey Orchestration**. Les informations contextuelles suivantes s&#39;affichent :

   * **Événements** : cette catégorie regroupe tous les champs du ou des événements placés avant l&#39;activité d’action de canal dans le parcours.
   * **Propriétés du parcours** : champs techniques liés au parcours pour un profil donné ; par exemple, identifiant du parcours ou erreurs spécifiques rencontrées. Pour en savoir plus, consultez la [documentation de Journey Orchestration](../building-journeys/expression/journey-properties.md).

   ![](assets/perso-uc10.png)

1. Développez l&#39;élément **Événements** et recherchez le champ du numéro de commande associé à votre événement. Vous pouvez également utiliser la zone de recherche. Cliquez sur l&#39;icône **+** pour insérer le champ de personnalisation dans le texte de l&#39;objet. Cliquez sur **Enregistrer**.

   ![](assets/perso-uc11.png)

1. Cliquez maintenant sur le champ **Corps**.

   ![](assets/perso-uc12.png)

1. Tapez le message et, à partir du menu **[!UICONTROL Attributs contextuels]**, insérez le nom de l’élément de commande et la progression de la commande.

   ![](assets/perso-uc13.png)

1. Dans le menu de gauche, sélectionnez **Décisions d’offre** pour insérer une variable de prise de décision. Sélectionnez l&#39;emplacement et cliquez sur l&#39;icône **+** en regard de la décision pour l’ajouter au corps.

   ![](assets/perso-uc14.png)

1. Cliquez sur Valider pour vous assurer qu’il n&#39;y a aucune erreur, puis sur **Enregistrer**.

   ![](assets/perso-uc15.png)

## Étape 4 - Tester et publier le parcours {#test-publish}

1. Cliquez sur le bouton **Test**, puis sur **Déclencher un événement**.

   ![](assets/perso-uc17.png)

1. Entrez les différentes valeurs à transmettre dans le test. Le mode test ne fonctionne qu&#39;avec les profils de test. L&#39;identifiant du profil doit correspondre à un profil de test. Cliquez sur **Envoyer**.

   ![](assets/perso-uc18.png)

   La notification push est envoyée et affichée sur le téléphone portable du profil de test.

   ![](assets/perso-uc19.png)

1. Vérifiez qu&#39;il n&#39;y a pas d&#39;erreur et publiez le parcours.

## Vidéo pratique {#video}

La vidéo ci-dessous présente un cas d’utilisation similaire en exploitant les données contextuelles d’un parcours pour personnaliser un e-mail.

>[!VIDEO](https://video.tv.adobe.com/v/3428528?captions=fre_fr&quality=12)
