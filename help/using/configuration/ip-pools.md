---
title: Création de groupes d’adresses IP
description: Découvrez comment gérer les pools d’adresses IP
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: 0e978d0eab570a28c187f3e7779c450437f16cfb
workflow-type: tm+mt
source-wordcount: '546'
ht-degree: 70%

---

# Création de groupes d’adresses IP {#create-ip-pools}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool"
>title="Configuration d’un groupe d’adresses IP"
>abstract="Vous pouvez créer des groupes d’adresses IP pour regrouper les adresses IP de vos sous-domaines afin d’améliorer la délivrabilité des e-mails."

## À propos des groupes d’adresses IP {#about-ip-pools}

Avec [!DNL Journey Optimizer], vous pouvez créer des groupes d’adresses IP pour regrouper les adresses IP de vos sous-domaines.

La création de pools d&#39;adresses IP est vivement recommandée pour la délivrabilité des e-mails. Ce faisant, vous pouvez empêcher la réputation d&#39;un sous-domaine d&#39;avoir un impact sur vos autres sous-domaines.

Par exemple, il est recommandé d&#39;avoir un pool d&#39;adresses IP pour vos messages marketing, et un autre pour vos messages transactionnels. De cette manière, si les performances de l&#39;un de vos messages marketing sont mauvaises et s&#39;il est déclaré comme indésirable par un client, cela n&#39;affecte pas les messages transactionnels envoyés à ce même client, qui recevra toujours des messages transactionnels (confirmations d’achat, messages de récupération de mot de passe, etc.).

## Création d&#39;un pool d&#39;adresses IP {#create-ip-pool}

Pour créer un pool d&#39;adresses IP, procédez comme suit :

1. Accédez au **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Groupes IP]** , puis cliquez sur **[!UICONTROL Créer un pool d’adresses IP]**.

   ![](assets/ip-pool-create.png)

1. Attribuez un nom et une description (facultatif) au pool d&#39;adresses IP.

   >[!NOTE]
   >
   >Le nom doit commencer par une lettre (A-Z) et contenir uniquement des caractères alphanumériques ou des caractères spéciaux ( _, ., - ).

1. Sélectionnez les adresses IP à inclure dans le pool dans la liste déroulante, puis cliquez sur **[!UICONTROL Envoyer]**.

   ![](assets/ip-pool-config.png)

   >[!NOTE]
   >
   >Toutes les adresses IP configurées avec votre instance sont disponibles dans la liste.

Le pool d&#39;adresses IP est maintenant créé et s&#39;affiche dans la liste. Vous pouvez la sélectionner pour accéder à ses propriétés et afficher la surface du canal associé (c’est-à-dire le paramètre prédéfini du message). Pour plus d’informations sur l’association d’une surface de canal à un pool d’adresses IP, reportez-vous à la section [cette section](message-presets.md).

![](assets/ip-pool-created.png)

## Modification d&#39;un pool d&#39;adresses IP {#edit-ip-pool}

Pour modifier un pool d’adresses IP :

1. Dans la liste, cliquez sur le nom du pool d’adresses IP pour l’ouvrir.

   ![](assets/ip-pool-list.png)

1. Modifiez ses propriétés selon vos besoins. Vous pouvez modifier la description et ajouter ou supprimer des adresses IP.

   >[!NOTE]
   >
   >Le nom du pool d’adresses IP n’est pas modifiable. Si vous souhaitez le modifier, vous devez supprimer le pool d’adresses IP et en créer un autre avec le nom de votre choix.

   ![](assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >Procédez avec attention lorsque vous envisagez de supprimer une adresse IP, car cela entraîne une charge supplémentaire pour les autres adresses IP, ce qui peut avoir de graves répercussions sur votre délivrabilité. En cas de doute, contactez un expert en délivrabilité.

1. Enregistrez vos modifications.

La mise à jour est effective immédiatement ou de manière asynchrone, selon le pool d’adresses IP associé à un [surface du canal](message-presets.md) ou non :

* Si le pool d’adresses IP est **not** associée à n’importe quelle surface de canal, la mise à jour est instantanée (**[!UICONTROL Succès]** status).
* Si le pool d’adresses IP **is** associée à la surface d’un canal, la mise à jour peut prendre jusqu’à 3 heures (**[!UICONTROL Traitement]** status).

>[!NOTE]
>
>When [création d’une surface de canal](message-presets.md#create-message-preset), si vous sélectionnez un pool d’adresses IP en cours d’édition (**[!UICONTROL Traitement]** ) et n’a jamais été associé au sous-domaine sélectionné pour cette surface, vous ne pouvez pas poursuivre la création de surface. [En savoir plus](message-presets.md#subdomains-and-ip-pools)

Pour vérifier l’état de mise à jour du pool d’adresses IP, cliquez sur le bouton **[!UICONTROL Autres actions]** et sélectionnez **[!UICONTROL Mises à jour récentes]**.

![](assets/ip-pool-recent-update.png)

>[!NOTE]
>
>Une fois qu’un pool d’adresses IP a été mis à jour, vous devrez peut-être attendre :
>* quelques minutes avant qu&#39;il soit consommé par les messages unitaires ;
>* jusqu’au lot suivant pour que le pool d’adresses IP soit effectif dans les messages par lots ;


Vous pouvez également utiliser le bouton **[!UICONTROL Supprimer]** pour supprimer un pool d’adresses IP. Notez que vous ne pouvez pas supprimer un pool d’adresses IP qui a été associé à une surface de canal.

