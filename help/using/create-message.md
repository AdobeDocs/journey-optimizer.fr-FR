---
title: Création d’un message
description: Découvrez comment créer un message
feature: Présentation
topic: Gestion de contenu
role: User
level: Beginner
source-git-commit: 9872df0ac91fff249a7b41ecd99b7c25c25463a9
workflow-type: tm+mt
source-wordcount: '495'
ht-degree: 93%

---

# Création d’un message {#create-message}

Les messages sont disponibles à partir du raccourci **[!UICONTROL Messages]** dans le volet de navigation de gauche. Tous les messages sont répertoriés, triés par date de publication (pour les messages publiés) ou par date de création (pour les messages en version préliminaire).

>[!NOTE]
>
>Les utilisateurs peuvent accéder aux messages, les créer, les modifier et/ou les publier en fonction de leur profil de produit. En savoir plus sur les autorisations utilisateur [dans cette section](../using/administration/permissions.md).

![](assets/messages-list.png)

Utilisez la bascule **[!UICONTROL Afficher récents]** pour ajouter des liens directs aux messages que vous avez consultés au cours des 5 derniers jours.

![](assets/show-recent-messages.png)

Utilisez l&#39;icône en forme de filtre pour afficher uniquement les messages rédigés, publiés ou en cours de publication. Vous pouvez également effectuer une recherche sur le libellé du message, comme suit :

![](assets/filter-messages.png)

## Création d’un nouveau message

Pour créer un nouveau message, procédez comme suit :

1. Accédez à la liste de messages, puis cliquez sur **[!UICONTROL Créer un message]**.

1. Définissez les propriétés du message.

   ![](assets/create-message-properties.png)

   * Saisissez un **[!UICONTROL Titre]** (obligatoire) et une **[!UICONTROL Description]**.

   * Sélectionnez le **[!UICONTROL Préréglage]** à utiliser pour le message.

      Les préréglages comprennent tous les paramètres requis pour qu’un email et/ou une notification push soit envoyés selon votre marque. [En savoir plus sur les paramètres prédéfinis](../using/configuration/message-presets.md).

   * Sélectionnez le ou les canaux à utiliser pour ce message : email et/ou notification push. Vous devez sélectionner au moins un canal pour pouvoir créer le message.
   Notez que vous pouvez à tout moment accéder au titre, à la description et au préréglage et les modifier à l’aide du bouton **[!UICONTROL Propriétés]** de l’interface de message.

   ![](assets/message-properties.png)


1. Cliquez sur **[!UICONTROL Créer]** pour confirmer la création du message. Votre message est ajouté dans la liste de messages, dans l’état **[!UICONTROL Version préliminaire]**.

   Un onglet est disponible pour chaque canal sélectionné. Utilisez ces onglets pour configurer le contenu pour chaque canal. Vous pouvez supprimer un onglet en le sélectionnant et en cliquant sur le bouton **[!UICONTROL Supprimer le canal]** à droite.

   ![](assets/create-messages-content.png)

   Vous pouvez désormais créer le contenu du message et adapter les paramètres. Des informations détaillées sur la configuration des emails et des notifications push sont disponibles dans les sections suivantes :

   * [Créer un email](create-email.md)
   * [Créer des notifications push](create-push.md)

   >[!NOTE]
   >   
   >Vous pouvez personnaliser vos messages à l’aide des données de profil, au moyen de l&#39;éditeur d’expression. Pour plus d&#39;informations sur la personnalisation, consultez [cette section](personalization/personalize.md).


1. Contrôlez le rendu de vos messages et vérifiez les paramètres de personnalisation avec les profils de test, à l&#39;aide de la section prévisualisation sur le côté gauche. Voir à ce propos [cette section](preview.md).

   ![](assets/messages-simple-preview.png)

1. Vérifiez les alertes dans la section supérieure de l’éditeur.  Certains d&#39;entre eux sont de simples avertissements, mais d&#39;autres peuvent vous empêcher de publier le message. En savoir plus dans [cette section](alerts.md).

1. Vous pouvez désormais publier votre message en cliquant sur le bouton **[!UICONTROL Publier]**, ou le conserver en tant que version préliminaire et le publier ultérieurement. Pour plus d&#39;informations sur la publication de messages, consultez [cette section](publish-manage-message.md).

## Dupliquer un message

Pour créer un message à partir d’un message existant, utilisez le bouton **[!UICONTROL Dupliquer]** de l’interface de message. Tous les paramètres et la configuration seront copiés dans le nouveau message.

![](assets/message-duplicate.png)

Vous pouvez renommer le message avant de confirmer la duplication.

![](assets/message-duplicate-confirm.png)

Un message de confirmation s’affiche au bas de la fenêtre une fois le nouveau message créé.

Vous pouvez également dupliquer un message à partir de la liste de messages à l’aide de l’icône dédiée.

![](assets/message-duplicate-from-list.png)

Le même processus de confirmation s&#39;applique.
