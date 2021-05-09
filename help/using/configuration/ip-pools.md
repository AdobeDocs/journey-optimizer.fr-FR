---
title: Création de pools IP
description: Découvrez comment xxxx
page-status-flag: never-activated
uuid: null
contentOwner: null
products: null
audience: administrators
content-type: reference
topic-tags: null
discoiquuid: null
internal: n
snippet: y
translation-type: tm+mt
source-git-commit: a65cefd0bbd15ffa389bac910eaceb40181cb38d
workflow-type: tm+mt
source-wordcount: '270'
ht-degree: 0%

---


# Création de pools IP

## A propos des pools IP

Journey Optimizer vous permet de créer des pools d’adresses IP pour regrouper les adresses IP de vos sous-domaines.

La création de pools d’adresses IP est vivement recommandée pour la remise des courriers électroniques. Ce faisant, vous pouvez empêcher la réputation d’un sous-domaine d’avoir un impact sur vos autres sous-domaines.

Par exemple, il est recommandé d’avoir un pool d’adresses IP pour vos messages marketing et un autre pour vos messages transactionnels. Ainsi, si l’un de vos messages marketing se comporte mal et est déclaré indésirable par un client, cela n’affectera pas les messages transactionnels envoyés à ce même client, qui recevra toujours des messages transactionnels (confirmations d’achat, messages de récupération de mot de passe, etc.).

## Création d’un pool d’adresses IP

Pour créer un pool d’adresses IP, procédez comme suit :

1. Accédez au menu **[Configuration du message]** / **[!UICONTROL Pool IP]**, puis cliquez sur **[!UICONTROL Créer un pool IP]**.

   ![](../assets/ip-pool-create.png)

1. Indiquez un nom et une description (facultatif) pour le pool IP.

1. Sélectionnez les adresses IP à inclure dans le pool dans la liste déroulante, puis cliquez sur **[!UICONTROL Envoyer]**.

   >[!NOTE]
   >
   >Toutes les adresses IP configurées avec votre instance sont disponibles dans la liste.

   ![](../assets/ip-pool-config.png)

   ! Bouton Envoyer grisé sur l’instance d’affichage

Le pool IP est maintenant créé et s’affiche dans la liste. Vous pouvez la sélectionner pour accéder à ses propriétés et afficher les paramètres prédéfinis de message associés (voir [Création d’un paramètre prédéfini de message](message-presets.md)).

    -SCREENSHOT-
    
     ! !aucun pool ip créé sur la scène 

Pour modifier un pool d’adresses IP, ouvrez-le, puis modifiez ses propriétés selon vos besoins.

>[!NOTE]
>
>Si un paramètre prédéfini de message a été associé, vous devez d’abord le supprimer pour modifier le pool d’adresses IP. Une fois le pool d’adresses IP modifié, vous pouvez associer à nouveau le paramètre prédéfini de message.
