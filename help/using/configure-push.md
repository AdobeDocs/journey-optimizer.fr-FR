---
title: Configurer une notification push
description: Découvrez comment créer une notification push dans Journey Optimizer
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: ht
source-wordcount: '976'
ht-degree: 100%

---

# Configurer une notification push {#create-push-notification}

![](assets/do-not-localize/badge.png)

Les notifications push sont configurées lors de la création d’un message, dans l’onglet **[!UICONTROL Notification push]** (voir [Création d’un message](create-message.md)).

Vous pouvez configurer le contenu des notifications push pour les systèmes d’exploitation iOS ou Android à l’aide des onglets dédiés.

![](assets/create-content-push.png)

## Titre et contenu

Pour composer votre message, cliquez sur les champs **[!UICONTROL Titre]** et **[!UICONTROL Corps]**. Utilisez l’éditeur d’expression pour définir le contenu et les données de personnalisation.

En savoir plus sur la personnalisation dans [cette section](personalization/personalize.md)

Utilisez la section centrale pour visualiser la façon dont s’affiche la notification push sur les terminaux iOS et Android.

>[!NOTE]
>
>La section **[!UICONTROL Composer le message]** est commune aux onglets **[!UICONTROL iOS]** et **[!UICONTROL Android]**. Toute modification apportée à cette section s&#39;appliquera aux deux systèmes d&#39;exploitation.

## Comportement en cas de clic {#on-click-behavior}

Sélectionnez le comportement lorsqu’un destinataire clique sur le corps de la notification push :

* Utilisez l&#39;option **[!UICONTROL Ouvrir l&#39;application]** pour ouvrir l&#39;application associée au **[!UICONTROL Préréglage]** du message.
* Utilisez l&#39;option **[!UICONTROL Lien profond]** pour rediriger le destinataire vers un contenu spécifique situé dans l&#39;application. Saisissez le lien profond dans le champ associé.
* Utilisez l&#39;option **[!UICONTROL URL Web]** pour rediriger le destinataire vers une URL externe. Saisissez l&#39;URL dans le champ associé.

## Envoyer une notification silencieuse

Une notification push silencieuse (ou notification en arrière-plan) est une instruction masquée qui est transmise à l’application. Elle est par exemple utilisée pour informer votre application de la disponibilité d&#39;un nouveau contenu ou pour lancer un téléchargement en arrière-plan.

Sélectionnez l&#39;option **[!UICONTROL Notification silencieuse]** pour avertir l&#39;application en silence : dans ce cas, la notification est transférée directement à l&#39;application. Aucune alerte ne s&#39;affiche sur l&#39;écran de l&#39;appareil.

Utilisez la section **[!UICONTROL Données personnalisées]** pour ajouter des paires clé/valeur.

## Options avancées

Configurez les **[!UICONTROL options avancées]**. Les paramètres disponibles sont les suivants :

| Paramètre | Disponibilité | Description |
|---------|----------|---------|
| **[!UICONTROL Réductible]** | iOS / Android | Un message réductible est un message qui peut être remplacé par un nouveau message. Par exemple, une application qui met à jour les utilisateurs avec les dernières informations sur une rubrique. Dans ce cas, seul le message le plus récent est pertinent. D’un autre côté, avec des messages non réductibles, chaque message est important pour l’application cliente et doit être diffusé. |
| **[!UICONTROL Son personnalisé]** | iOS / Android | Son à émettre par le terminal mobile lors de la réception de la notification. Le son doit être assemblé dans l’application. |
| **[!UICONTROL Badges]** | iOS / Android | Un badge est utilisé pour afficher directement sur l’icône de l’application le nombre de nouvelles informations non lues. <br/>La valeur du badge disparaît dès que l’utilisateur ouvre ou lit le nouveau contenu de l’application. Lorsqu’une notification est reçue sur un appareil, elle peut actualiser ou ajouter une valeur de badge pour l’application associée.<br/>Par exemple, si vous stockez le nombre d’articles non lus de vos clients, vous pouvez tirer parti de la personnalisation pour envoyer la valeur unique de badge d’articles non lus pour chaque client. Pour plus d&#39;informations sur la personnalisation, consultez [cette section](personalization/personalize.md). |
| **[!UICONTROL Groupe de notification]** / | iOS | Associez un groupe de notification à la notification push.<br/>À partir d’iOS 12, les groupes de notifications vous permettent de consolider les threads de message et les rubriques de notification en identifiants de threads. Par exemple, une marque peut envoyer des notifications marketing sous un identifiant de groupe, tout en conservant d’autres notifications de type opérationnel sous un ou plusieurs identifiants différents.<br/>Pour illustrer cela, vous pouvez avoir les groupes de notification groupID : 123 « Consultez la nouvelle collection printanière de pulls » et groupID : 456 « Votre colis a été livré ». Dans cet exemple, toutes les notifications de diffusion sont regroupées sous l&#39;identifiant de groupe : 456. |
| **[!UICONTROL Canal de notification]** | Android | Associez un canal de notification à la notification push.<br/>À partir d&#39;Android 8.0 (niveau API 26), toutes les notifications doivent être affectées à un canal pour s’afficher. Consultez à ce sujet la [documentation pour développeur Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Ajouter un indicateur de disponibilité de contenu]** | iOS | Envoie l&#39;indicateur de disponibilité de contenu dans la payload push pour veiller à ce que l&#39;application sorte de veille à la réception de la notification push et puisse accéder ainsi aux données de la payload.<br/> Ce mécanisme fonctionne même si l&#39;application est en cours d&#39;exécution à l&#39;arrière-plan et qu&#39;elle ne nécessite pas l&#39;intervention de l&#39;utilisateur (comme appuyer sur la notification push, par exemple). Toutefois, il ne s&#39;applique pas si l&#39;application n&#39;est pas en cours d&#39;exécution. Consultez à ce sujet la [documentation pour développeur Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| **[!UICONTROL Ajouter un indicateur de contenu modifiable]** | iOS | Envoie l’indicateur de contenu modifiable dans la payload push et permet de modifier le contenu de la notification push en utilisant l’extension d’application du service de notification fournie dans le SDK iOS. Consultez à ce sujet la [documentation pour développeur Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>Vous pouvez ensuite exploiter vos extensions d&#39;applications mobiles pour modifier davantage le contenu ou la présentation des notifications push envoyées depuis [!DNL Journey Optimizer] Par exemple, les utilisateurs peuvent utiliser cette option pour déchiffrer des données, modifier le corps ou le titre d&#39;une notification, ajouter un identifiant de thread à une notification, etc. |
| **[!UICONTROL Visibilité de la notification]** | Android | Définit la visibilité de la notification push. <b>private</b> affichera la notification sur tous les écrans verrouillés, mais dissimulera les informations sensibles ou privées sur les écrans verrouillés sécurisés. <b>public</b> affichera la notification dans son intégralité sur tous les écrans verrouillés. <b>secret</b> ne divulguera aucune partie de la notification sur un écran verrouillé sécurisé. Consultez à ce sujet la [documentation pour développeur Android](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Priorité de notification]** | Android | Définit l’importance de la notification push de Faible à Max. Cette opération détermine l’intrusion de la notification push lors de sa diffusion. Consultez à ce sujet la [documentation pour développeur Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Priorité de diffusion]** | Android | Définit une priorité élevée ou normale pour vos notifications push. Pour plus d&#39;informations sur la priorité des messages, consultez la [documentation destinée aux développeurs Google](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message). |

## Données personnalisées

Dans la section **[!UICONTROL Données personnalisées]**, vous pouvez ajouter des variables personnalisées à la payload, en fonction de la configuration de votre application mobile. Pour plus d’informations sur la configuration des notifications push dans Adobe Experience Platform et Adobe Launch, voir [cette section](push-configuration.md).

