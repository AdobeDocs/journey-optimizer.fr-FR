---
title: Création de pools d'adresses IP
description: '"Découvrir comment gérer les pools d''adresses IP"'
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
feature: Paramétrage de l’application
topic: Administration
role: Admin
level: Intermediate
source-git-commit: 63de381ea3a87b9a77bc6f1643272597b50ed575
workflow-type: tm+mt
source-wordcount: '294'
ht-degree: 100%

---


# Création de pools d&#39;adresses IP

## À propos des pools d&#39;adresses IP

Avec Journey Optimizer, vous pouvez créer des pools d&#39;adresses IP pour regrouper les adresses IP de vos sous-domaines.

La création de pools d&#39;adresses IP est vivement recommandée pour la délivrabilité des e-mails. Ce faisant, vous pouvez empêcher la réputation d&#39;un sous-domaine d&#39;avoir un impact sur vos autres sous-domaines.

Par exemple, il est recommandé d&#39;avoir un pool d&#39;adresses IP pour vos messages marketing, et un autre pour vos messages transactionnels. De cette manière, si les performances de l&#39;un de vos messages marketing sont mauvaises et s&#39;il est déclaré comme indésirable par un client, cela n&#39;affecte pas les messages transactionnels envoyés à ce même client, qui recevra toujours des messages transactionnels (confirmations d’achat, messages de récupération de mot de passe, etc.).

## Création d&#39;un pool d&#39;adresses IP

Pour créer un pool d&#39;adresses IP, procédez comme suit :

1. Accédez au menu **[!UICONTROL Canaux]**/**[!UICONTROL Pools d&#39;adresses IP]**, puis cliquez sur **[!UICONTROL Créer un pool d&#39;adresses IP]**.

   ![](../assets/ip-pool-create.png)

1. Attribuez un nom et une description (facultatif) au pool d&#39;adresses IP.

   >[!NOTE]
   >
   >Le nom du sous-domaine doit commencer par une lettre (A-Z) et contenir uniquement des caractères alphanumériques ou des caractères spéciaux ( _, ., - ).

1. Sélectionnez les adresses IP à inclure dans le pool dans la liste déroulante, puis cliquez sur **[!UICONTROL Envoyer]**.

   ![](../assets/ip-pool-config.png)

   >[!NOTE]
   >
   >Toutes les adresses IP configurées avec votre instance sont disponibles dans la liste.

Le pool d&#39;adresses IP est maintenant créé et s&#39;affiche dans la liste. Vous pouvez le sélectionner pour accéder à ses propriétés et afficher le préréglage de message associé. Pour plus d&#39;informations sur l&#39;association d&#39;un préréglage de message à un pool d&#39;adresses IP, consultez [cette section](message-presets.md).

![](../assets/ip-pool-created.png)

Pour modifier un pool d&#39;adresses IP, ouvrez-le, puis modifiez ses propriétés selon vos besoins.

>[!NOTE]
>
>Si un préréglage de message a été associé au pool d&#39;adresses IP, vous devez d&#39;abord le supprimer avant de modifier le pool d&#39;adresses IP. Une fois vos modifications effectuées, vous pouvez associer à nouveau le préréglage de message.
