---
title: Configurer une notification push
description: Découvrez comment créer une notification push dans Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 2ebbcd7d-dcfc-4528-974d-6230fc0dca3d
source-git-commit: 7138e1f031bd26caf9379c3ff19d79ac29442bc6
workflow-type: tm+mt
source-wordcount: '1244'
ht-degree: 100%

---

# Créez une notification push {#create-push-notification}

Une fois que vous avez [créé un message](create-message.md), cliquez sur l&#39;onglet **[!UICONTROL Notification push]** pour définir les paramètres et le contenu de la notification push.

![](assets/create-content-push.png)

Utilisez les onglets dédiés pour définir les paramètres de notification push pour les systèmes d&#39;exploitation **iOS** et **Android**.

>[!NOTE]
>
>La section **[!UICONTROL Composer le message]** est commune aux onglets **[!UICONTROL iOS]** et **[!UICONTROL Android]**. Toute modification apportée à cette section s&#39;appliquera aux deux onglets.

## Titre et contenu

Pour composer votre message, cliquez sur les champs **[!UICONTROL Titre]** et **[!UICONTROL Corps]**. Utilisez l&#39;éditeur d&#39;expression pour définir le contenu et les données de personnalisation. Consultez [cette section](personalization/personalize.md) pour en savoir plus sur la personnalisation dans l&#39;éditeur d&#39;expression.

Utilisez la section de prévisualisation des appareils pour visualiser la façon dont s&#39;affiche la notification push sur les appareils iOS et Android.

## Comportement en cas de clic {#on-click-behavior}

Sélectionnez le comportement lorsqu&#39;un destinataire clique sur le corps de la notification push.

![](assets/title-body-push.png)

* Utilisez l&#39;option **[!UICONTROL Ouvrir l&#39;application]** pour ouvrir l&#39;application associée au **[!UICONTROL Préréglage]** du message.
* Utilisez l&#39;option **[!UICONTROL Lien profond]** pour rediriger le destinataire vers un contenu spécifique situé dans l&#39;application. Saisissez le lien profond dans le champ associé.
* Utilisez l&#39;option **[!UICONTROL URL Web]** pour rediriger le destinataire vers une URL externe. Saisissez l&#39;URL dans le champ associé.

## Ajouter un média

Dans la version iOS de votre notification push, vous pouvez ajouter une image, une vidéo ou un fichier GIF qui s&#39;affichera dans votre notification.

Dans la version Android, vous pouvez uniquement ajouter une icône d&#39;image et une image pour les notifications étendues.

![](assets/push-config-add-media.png)

Deux options sont disponibles. Vous pouvez :

* Cliquer sur le bouton **[!UICONTROL Ajouter un média]** pour sélectionner une ressource dans **[!DNL Adobe Experience Manager Assets Essentials]**.

   Découvrez comment utiliser **[!DNL Adobe Experience Manager Assets Essentials]** dans [cette page](assets-essentials.md).

* Ou saisir l&#39;URL du média en cliquant sur le champ **[!UICONTROL Ajouter un média]**. Dans ce cas, vous pouvez ajouter une personnalisation.

Une fois ajouté, le média s&#39;affiche à droite du corps de la notification.

## Ajouter des boutons

Vous pouvez créer une notification exploitable en ajoutant des boutons à votre contenu push.

Si l&#39;écran de l&#39;appareil est verrouillé, les boutons suivants ne s&#39;affichent pas : seuls le **Titre** et le **Message** de la notification sont visibles. Si leur appareil est déverrouillé, les destinataires verront les boutons.

Dans la version iOS, vous pouvez ajouter jusqu&#39;à 4 boutons. Dans la version Android, vous pouvez ajouter jusqu&#39;à 3 boutons.

>[!NOTE]
>
>Pour iOS, utilisez le champ **[!UICONTROL catégorie iOS]** pour associer les actions à une catégorie de notification.

Cliquez sur **[!UICONTROL Ajouter un bouton]** pour définir les paramètres : le libellé et l&#39;action associée. Les actions possibles sont les mêmes que pour le [comportement en cas de clic](#on-click-behavior).

Cliquez sur **[!UICONTROL Développer la vue]** pour prévisualiser vos boutons personnalisés.

![](assets/push_buttons.png)

## Envoyer une notification silencieuse

Une notification push silencieuse (ou notification en arrière-plan) est une instruction masquée qui est transmise à l&#39;application. Elle est par exemple utilisée pour informer votre application de la disponibilité d&#39;un nouveau contenu ou pour lancer un téléchargement en arrière-plan.

Sélectionnez l&#39;option **[!UICONTROL Notification silencieuse]** pour avertir l&#39;application en silence : dans ce cas, la notification est transférée directement à l&#39;application. Aucune alerte ne s&#39;affiche sur l&#39;écran de l&#39;appareil.

Utilisez la section **[!UICONTROL Données personnalisées]** pour ajouter des paires clé-valeur.

## Données personnalisées

Dans la section **[!UICONTROL Données personnalisées]**, vous pouvez ajouter des variables personnalisées à la payload, en fonction de la configuration de votre application mobile. Pour plus d&#39;informations sur la configuration des notifications push dans Adobe Experience Platform et Adobe Launch, voir [cette section](push-gs.md).

## Options avancées

Vous pouvez configurer les **[!UICONTROL options avancées]** pour votre notification push. Les paramètres disponibles sont répertoriés ci-dessous :

| Paramètre | Description |
|---------|---------|
| **[!UICONTROL Réductible]** (iOS/Android) | Un message réductible est un message qui peut être remplacé par un nouveau message s&#39;il est obsolète. Les messages utilisés pour indiquer à une application mobile de synchroniser les données du serveur constituent des cas d&#39;utilisation courants de messages réductibles. Par exemple, une application sportive qui informe les utilisateurs du dernier score. Seul le message le plus récent est pertinent. D&#39;un autre côté, avec des messages non réductibles, chaque message est important pour l&#39;application cliente et doit être diffusé. |
| **[!UICONTROL Son personnalisé]**     (iOS / Android) | Son à émettre par le terminal mobile lors de la réception de la notification. Le son doit être assemblé dans l&#39;application. |
| **[!UICONTROL Badges]**     (iOS / Android) | Un badge est utilisé pour afficher directement sur l&#39;icône de l&#39;application le nombre de nouvelles informations non lues. <br/>La valeur du badge disparaît dès que l&#39;utilisateur ouvre ou lit le nouveau contenu de l&#39;application. Lorsqu&#39;une notification est reçue sur un appareil, elle peut actualiser ou ajouter une valeur de badge pour l&#39;application associée.<br/>Par exemple, si vous stockez le nombre d&#39;articles non lus de vos clients, vous pouvez tirer parti de la personnalisation pour envoyer la valeur unique de badge d&#39;articles non lus pour chaque client. Pour plus d&#39;informations sur la personnalisation, consultez [cette section](personalization/personalize.md). |
| **[!UICONTROL Groupe de notifications]** (iOS uniquement) | Associez un groupe de notification à la notification push.<br/>À partir d&#39;iOS 12, les groupes de notifications vous permettent de consolider les threads de message et les rubriques de notification en identifiants de threads. Par exemple, une marque peut envoyer des notifications marketing sous un identifiant de groupe, tout en conservant d&#39;autres notifications de type opérationnel sous un ou plusieurs identifiants différents.<br/>Pour illustrer cela, vous pouvez avoir les groupes de notification groupID : 123 « Consultez la nouvelle collection printanière de pulls » et groupID : 456 « Votre colis a été livré ». Dans cet exemple, toutes les notifications de diffusion sont regroupées sous l&#39;identifiant de groupe : 456. |
| **[!UICONTROL Canal de notification]**     (Android uniquement) | Associez un canal de notification à la notification push.<br/>À partir d&#39;Android 8.0 (niveau API 26), toutes les notifications doivent être affectées à un canal pour s&#39;afficher. Consultez à ce sujet la [documentation pour développeur Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Ajouter un indicateur de disponibilité de contenu]**     (iOS uniquement) | Envoie l&#39;indicateur de disponibilité de contenu dans la payload push pour veiller à ce que l&#39;application sorte de veille à la réception de la notification push et puisse accéder ainsi aux données de la payload.<br/> Ce mécanisme fonctionne même si l&#39;application est en cours d&#39;exécution à l&#39;arrière-plan et qu&#39;elle ne nécessite pas l&#39;intervention de l&#39;utilisateur (comme appuyer sur la notification push, par exemple). Toutefois, il ne s&#39;applique pas si l&#39;application n&#39;est pas en cours d&#39;exécution. Consultez à ce sujet la [documentation pour développeur Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| **[!UICONTROL Ajouter un indicateur de contenu modifiable]**     (iOS uniquement) | Envoie l&#39;indicateur de contenu modifiable dans la payload push et permet de modifier le contenu de la notification push en utilisant l&#39;extension d&#39;application du service de notification fournie dans le SDK iOS. Consultez à ce sujet la [documentation pour développeur Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>Vous pouvez ensuite exploiter vos extensions d&#39;applications mobiles pour modifier davantage le contenu ou la présentation des notifications push envoyées depuis [!DNL Journey Optimizer]. Par exemple, les utilisateurs peuvent utiliser cette option pour déchiffrer des données, modifier le corps ou le titre d&#39;une notification, ajouter un identifiant de thread à une notification, etc. |
| **[!UICONTROL Visibilité de la notification]**     (Android uniquement) | Définit la visibilité de la notification push. <br/><b>Private</b> affichera la notification sur tous les écrans verrouillés, mais dissimulera les informations sensibles ou privées sur les écrans verrouillés sécurisés. <br/><b>public</b> affichera la notification dans son intégralité sur tous les écrans verrouillés. <br/><b>secret</b> ne divulguera aucune partie de la notification sur un écran verrouillé sécurisé. <br/>Consultez à ce sujet la [documentation pour développeur Android](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Priorité des notifications]** (Android uniquement) | Définit l&#39;importance de la notification push de Faible à Max. Cette opération détermine l&#39;intrusion de la notification push lors de sa diffusion. Consultez à ce sujet la [documentation pour développeur Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Priorité de diffusion]**     (Android uniquement) | Définit une priorité élevée ou normale pour vos notifications push. Pour plus d&#39;informations sur la priorité des messages, consultez la [documentation destinée aux développeurs Google](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message). |

**Rubriques connexes**

<!--
* [Understand push notification flow](push-gs.md)
-->

* [Configuration du canal push](push-gs.md)
* [Création d&#39;un nouveau message](create-message.md)
* [Ajout d&#39;un message dans un parcours](building-journeys/journeys-message.md)
