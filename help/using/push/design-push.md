---
solution: Journey Optimizer
product: journey optimizer
title: Concevoir une notification push
description: Découvrez comment concevoir une notification push dans Journey Optimizer
feature: Overview
topic: Content Management
role: User
level: Beginner
exl-id: 6f6d693d-11f2-48b7-82a8-171829bf8045
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '1181'
ht-degree: 0%

---

# Concevoir une notification push {#design-push-notification}

## Titre et corps {#push-title-body}

Pour composer votre message, cliquez sur le bouton **[!UICONTROL Title]** et **[!UICONTROL Body]** champs. Utilisez l&#39;éditeur d&#39;expression pour définir le contenu, personnaliser les données et ajouter du contenu dynamique. En savoir plus sur [personnalisation](../personalization/personalize.md) et [contenu dynamique](../personalization/get-started-dynamic-content.md) dans l&#39;éditeur d&#39;expression.

Utilisez la section d’aperçu de l’appareil pour visualiser l’affichage de la notification push sur les appareils iOS et Android.

## Comportement en cas de clic {#on-click-behavior}

>[!CONTEXTUALHELP]
>id="ajo-message-push-onclick"
>title="À propos du comportement en cas de clic"
>abstract="Sélectionnez le comportement lorsqu&#39;un destinataire clique sur le corps de la notification push."

Vous pouvez sélectionner le comportement lorsqu’un utilisateur clique sur le corps de la notification push.

![](assets/title-body-push.png)

* Pour ouvrir l’application, sélectionnez la **[!UICONTROL Open app]** . L’application associée à la notification est définie dans la variable [surface du canal](../configuration/channel-surfaces.md) (c’est-à-dire le paramètre prédéfini du message).
* Pour rediriger l’utilisateur vers un élément de contenu spécifique dans une application, sélectionnez la variable **[!UICONTROL Deeplink]** .  Le contenu spécifique peut être une vue spécifique, une section spécifique d’une page ou un certain onglet. Une fois l&#39;option sélectionnée, saisissez le lien profond dans le champ associé.
* Pour rediriger l’utilisateur vers une URL externe, utilisez la méthode **[!UICONTROL Web URL]** . Une fois l&#39;option sélectionnée, saisissez l&#39;URL dans le champ associé.

## Ajouter un média {#add-media-push}

Dans la version iOS de votre notification push, vous pouvez ajouter une image, une vidéo ou un fichier GIF qui s&#39;affichera dans votre notification.

Dans la version Android, vous pouvez uniquement ajouter une icône d’image et une image pour les notifications étendues.

![](assets/push-config-add-media.png)

Deux options sont disponibles. Vous pouvez :

* Utilisez la variable **[!UICONTROL Add media]** pour sélectionner une ressource dans **[!DNL Adobe Experience Manager Assets Essentials]**.

   Découvrez comment utiliser **[!DNL Adobe Experience Manager Assets Essentials]** in [cette page](../email/assets-essentials.md).

* Ou saisissez l’URL du média dans la variable **[!UICONTROL Add media]** champ . Dans ce cas, vous pouvez ajouter une personnalisation à l’URL.

Une fois ajouté, le support s&#39;affiche à droite du corps de la notification.

## Ajouter des boutons {#add-buttons-push}

Créez une notification exploitable en ajoutant des boutons à votre contenu push.

Si l’écran du périphérique est verrouillé, les boutons suivants ne s’affichent pas : uniquement le **Titre** et le **Message** de la notification sont visibles. Si leur appareil est déverrouillé, les destinataires verront les boutons.

Dans la version iOS, vous pouvez ajouter jusqu’à quatre boutons. Dans la version Android, vous pouvez ajouter jusqu’à trois boutons.

>[!NOTE]
>
>Pour iOS, utilisez le **[!UICONTROL iOS category]** pour associer des actions à une catégorie de notification.

1. Utilisez la variable **[!UICONTROL Add button]** pour définir les paramètres : le libellé et l&#39;action associée. Les actions possibles sont les mêmes que pour [comportement en cas de clic](#on-click-behavior).

1. Utilisez la variable **[!UICONTROL Expand view]** sous l’image d’aperçu centrale pour prévisualiser vos boutons personnalisés.

![](assets/push_buttons.png)

## Envoyer une notification silencieuse {#silent-notification}

>[!CONTEXTUALHELP]
>id="ajo_message_push_silent_notification"
>title="A propos de la notification silencieuse"
>abstract="Envoyez des notifications sans déranger l’utilisateur. Les notifications ne sont pas affichées dans le centre de notifications ou dans la barre de notifications."

Une notification push silencieuse (ou notification en arrière-plan) est une instruction masquée diffusée à l’application. Il est utilisé, par exemple, pour informer votre application de la disponibilité du nouveau contenu ou lancer un téléchargement en arrière-plan.

Sélectionnez la **[!UICONTROL Silent Notification]** pour notifier silencieusement l’application : dans ce cas, la notification est directement transmise à l&#39;application. Aucune alerte n’est affichée à l’écran du périphérique.

Utilisez la variable **[!UICONTROL Custom data]** pour ajouter des paires clé-valeur.

## Données personnalisées

Dans le **[!UICONTROL Custom data]** , vous pouvez ajouter des variables personnalisées à la payload, en fonction de la configuration de votre application mobile. Pour plus d&#39;informations sur la configuration des notifications push dans Adobe Experience Platform et Adobe Launch, reportez-vous à la section [cette section](push-gs.md)

## Options avancées {#advanced-options-push}

Vous pouvez configurer **[!UICONTROL Advanced options]** pour votre notification push. Les paramètres disponibles sont répertoriés ci-dessous :

| Paramètre | Description |
|---------|---------|
| **[!UICONTROL Collapsible]** (iOS / Android) | Un message réductible est un message qui peut être remplacé par un nouveau message s’il est obsolète. Les messages utilisés pour indiquer à une application mobile de synchroniser les données du serveur constituent des cas d’utilisation courants de messages réductibles. Par exemple, une application sportive qui met à jour les utilisateurs avec le dernier score. Seul le message le plus récent est pertinent. D’un autre côté, avec un message non réductible, chaque message est important pour l’application cliente et doit être diffusé. |
| **[!UICONTROL Custom sound]** (iOS / Android) | Son que doit émettre le terminal mobile à la réception de la notification. Le son doit être regroupé dans l’application. |
| **[!UICONTROL Badges]** (iOS / Android) | Un badge est utilisé pour afficher directement sur l&#39;icône de l&#39;application le nombre de nouvelles informations non lues. <br/>La valeur du badge disparaît dès que l’utilisateur ouvre ou lit le nouveau contenu de l’application. Lorsqu’une notification est reçue sur un appareil, elle peut actualiser ou ajouter une valeur de badge pour l’application associée.<br/>Par exemple, si vous stockez le nombre d’articles non lus de vos clients, vous pouvez tirer parti de la personnalisation pour envoyer la valeur unique de badge d’articles non lus pour chaque client. Pour plus de personnalisation, voir [cette section](../personalization/personalize.md). |
| **[!UICONTROL Notification group]**  (iOS uniquement) | Associez un groupe de notifications à la notification push.<br/>Depuis iOS 12, les groupes de notifications permettent de consolider les threads de messages et les rubriques de notification dans les ID de threads. Par exemple, une marque peut envoyer des notifications marketing sous un identifiant de groupe, tout en conservant plus de notifications de type opérationnel sous un ou plusieurs identifiants différents.<br/>Pour illustrer cela, vous pouvez utiliser groupID : 123 &quot;Consultez la nouvelle collection printemps de pulls&quot; et groupID : 456 Groupes de notifications &quot;votre package a été livré&quot;. Dans cet exemple, toutes les notifications de diffusion seraient regroupées sous l’ID de groupe : 456. |
| **[!UICONTROL Notification channel]** (Android uniquement) | Associez un canal de notification à la notification push.<br/>À partir d’Android 8.0 (niveau API 26), toutes les notifications doivent être affectées à un canal pour s’afficher. Voir à ce sujet la section [Documentation pour les développeurs Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#ManageChannels). |
| **[!UICONTROL Add content-availability flag]** (iOS uniquement) | Envoie l’indicateur de contenu disponible dans la payload push pour s’assurer que l’application se réveille dès réception de la notification push, ce qui signifie que l’application pourra accéder aux données de la payload.<br/> Cela fonctionne même si l’application s’exécute en arrière-plan et sans avoir besoin d’une interaction de l’utilisateur (par exemple, en appuyant sur la notification push). Toutefois, cela ne s’applique pas si l’application n’est pas en cours d’exécution. Voir à ce sujet la section [Documentation destinée aux développeurs Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/CreatingtheNotificationPayload.html). |
| **[!UICONTROL Add mutable-content flag]** (iOS uniquement) | Envoie l’indicateur de contenu mutable dans la payload push et permettra de modifier le contenu de la notification push par une extension de l’application du service de notification fournie dans le SDK iOS. Voir à ce sujet la section [Documentation destinée aux développeurs Apple](https://developer.apple.com/library/content/documentation/NetworkingInternet/Conceptual/RemoteNotificationsPG/ModifyingNotifications.html).<br/>Vous pouvez ensuite tirer parti des extensions de votre application mobile pour modifier davantage le contenu ou la présentation des notifications push envoyées depuis [!DNL Journey Optimizer]. Par exemple, les utilisateurs peuvent utiliser cette option pour décrypter des données, modifier le corps ou le texte du titre d’une notification, ajouter un identifiant de thread à une notification, etc. |
| **[!UICONTROL Notification visibility]** (Android uniquement) | Définit la visibilité de la notification push. <br/><b>Privé</b> affiche la notification sur tous les écrans de verrouillage, mais masque les informations sensibles ou privées sur les écrans de verrouillage sécurisés. <br/><b>Public</b> affiche la notification dans son intégralité sur tous les écrans de fermeture. <br/><b>Secret</b> ne révèle aucune partie de la notification sur un écran de verrouillage sécurisé. <br/>Voir à ce propos la section [Documentation pour les développeurs Android](https://developer.android.com/reference/android/app/Notification). |
| **[!UICONTROL Notification priority]** (Android uniquement) | Définit l’importance de la notification push de bas en haut. Cela détermine l’&quot;intrusion&quot; de la notification push lors de sa diffusion. Voir à ce sujet la section [Documentation pour les développeurs Android](https://developer.android.com/guide/topics/ui/notifiers/notifications#importance) |
| **[!UICONTROL Delivery priority]** (Android uniquement) | Définit une priorité élevée ou normale pour vos notifications push. Pour plus d’informations sur la priorité des messages, reportez-vous à la section [Documentation destinée aux développeurs Google](https://firebase.google.com/docs/cloud-messaging/concept-options#setting-the-priority-of-a-message). |
