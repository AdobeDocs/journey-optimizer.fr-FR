---
title: Publication et modification d’un message
description: Découvrez comment publier et mettre à jour vos messages
snippet: y
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '219'
ht-degree: 0%

---

# Publier vos messages {#publish-manage-messages}

![](assets/do-not-localize/badge.png)

## Publier un message {#publish-message}

Une fois votre message créé, vous pouvez le publier pour le rendre disponible pour exécution.

>[!CAUTION]
>
>Avant de publier, vérifiez et résolvez les alertes. [En savoir plus](alerts.md).

![](assets/publish-message.png)

Une fois votre message publié, il est ajouté à la liste de messages avec l’état **[!UICONTROL Publié]**.

Il est maintenant prêt à être déclenché par un ou plusieurs [parcours](building-journeys/journey.md).

## Mettre à jour un message en lecture seule {#modify-message}

Après la publication, un message est en lecture seule. Vous pouvez toujours le mettre à jour en créant un nouveau brouillon de ce message.

Cela vous permet de mettre à jour le contenu ou de corriger un problème, par exemple, sans republier l’ensemble du parcours d’utilisation de votre message.

>[!NOTE]
>
>La version préliminaire peut être modifiée alors que la version publiée est toujours publiée et principale.

Pour mettre à jour un message publié :

1. Dans la liste de messages, sélectionnez votre message pour l’ouvrir.

1. Cliquez sur **[!UICONTROL Modifier]**.

   ![](assets/message-modify.png)

1. Confirmez votre choix. Une version préliminaire du message est créée.

   ![](assets/message-modify-v2.png)

1. Modifiez le contenu ou les paramètres selon vos besoins.
1. Cliquez sur **[!UICONTROL Publier]**. Cette action publiera la nouvelle version du message qui sera utilisée pour les prochaines exécutions.

Dès que la nouvelle version est publiée, lors du prochain appel d’API, un nouveau message d’exécution est généré. Le prochain profil entrant recevra la nouvelle version.

<!--For batch messages, the audience/segment being processed in the previous execution will not be affected by the new version. Only the next incoming API call with an audience/segment will generate a new message execution with the new version.-->
