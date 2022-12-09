---
solution: Journey Optimizer
product: journey optimizer
title: Création de pools d’adresses IP
description: Découvrez comment gérer les pools d’adresses IP
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: 3a932747de33ced59d68835a96386b7ac560e4fe
workflow-type: tm+mt
source-wordcount: '598'
ht-degree: 0%

---

# Création de pools d’adresses IP {#create-ip-pools}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool_header"
>title="Configuration d’un pool d’adresses IP"
>abstract="Les pools d’adresses IP rassemblent les adresses IP de vos sous-domaines pour une meilleure délivrabilité des emails."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool"
>title="Configuration d’un pool d’adresses IP"
>abstract="Avec Journey Optimizer, vous pouvez créer des pools d’adresses IP pour regrouper les adresses IP de vos sous-domaines. Cela peut améliorer considérablement la délivrabilité de vos emails, car ce faisant, vous pouvez empêcher la réputation d’un sous-domaine d’avoir un impact sur vos autres sous-domaines."

## À propos des pools d’adresses IP {#about-ip-pools}

Avec [!DNL Journey Optimizer], vous pouvez créer des pools d’adresses IP pour regrouper les adresses IP de vos sous-domaines.

La création de pools d’adresses IP est vivement recommandée pour la délivrabilité des emails. Ce faisant, vous pouvez empêcher la réputation d’un sous-domaine d’avoir un impact sur vos autres sous-domaines.

Par exemple, il est recommandé d’avoir un pool d’adresses IP pour vos messages marketing, et un autre pour vos messages transactionnels. De cette manière, si l’un de vos messages marketing fonctionne mal et est déclaré comme indésirable par un client, cela n’affecte pas les messages transactionnels envoyés à ce même client, qui recevra toujours des messages transactionnels (confirmations d’achat, messages de récupération de mot de passe, etc.).

>[!CAUTION]
>
>La configuration du pool d’adresses IP est commune à tous les environnements. Par conséquent, toute création ou modification de pool d’adresses IP aura également un impact sur les environnements de test de production.

## Création d’un pool d’adresses IP {#create-ip-pool}

Pour créer un pool d’adresses IP, procédez comme suit :

1. Accédez au **[!UICONTROL Administration]** > **[!UICONTROL Channels]** > **[!UICONTROL IP pools]** , puis cliquez sur **[!UICONTROL Create IP Pool]**.

   ![](assets/ip-pool-create.png)

1. Attribuez un nom et une description (facultatif) au pool d’adresses IP.

   >[!NOTE]
   >
   >Le nom doit commencer par une lettre (A-Z) et contenir uniquement des caractères alphanumériques ou des caractères spéciaux ( _, ., - ).

1. Sélectionnez les adresses IP à inclure dans le pool dans la liste déroulante, puis cliquez sur **[!UICONTROL Submit]**.

   ![](assets/ip-pool-config.png)

   >[!NOTE]
   >
   >Toutes les adresses IP configurées avec votre instance sont disponibles dans la liste.

Le pool d’adresses IP est maintenant créé et s’affiche dans la liste. Vous pouvez la sélectionner pour accéder à ses propriétés et afficher la surface du canal associé (c’est-à-dire le paramètre prédéfini du message). Pour plus d’informations sur l’association d’une surface de canal à un pool d’adresses IP, reportez-vous à la section [cette section](channel-surfaces.md).

![](assets/ip-pool-created.png)

## Modification d’un pool d’adresses IP {#edit-ip-pool}

Pour modifier un pool d’adresses IP, procédez comme suit.

1. Dans la liste, cliquez sur le nom du pool d’adresses IP pour l’ouvrir.

   ![](assets/ip-pool-list.png)

1. Modifiez ses propriétés selon vos besoins. Vous pouvez modifier la description et ajouter ou supprimer des adresses IP.

   >[!NOTE]
   >
   >Le nom du pool d’adresses IP n’est pas modifiable. Si vous souhaitez le modifier, vous devez supprimer le pool d’adresses IP et en créer un autre avec le nom de votre choix.

   ![](assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >Procédez avec une attention particulière lorsque vous envisagez de supprimer une adresse IP, car cela imposera une charge supplémentaire aux autres adresses IP et peut avoir de graves répercussions sur votre délivrabilité. En cas de doute, contactez un expert en délivrabilité.

1. Enregistrez vos modifications.

La mise à jour est effective immédiatement ou de manière asynchrone, selon le pool d’adresses IP associé à un [surface du canal](channel-surfaces.md) ou non :

* Si le pool d’adresses IP est **not** associée à n’importe quelle surface de canal, la mise à jour est instantanée (**[!UICONTROL Success]** status).
* Si le pool d’adresses IP **is** associée à la surface d’un canal, la mise à jour peut prendre jusqu’à 3 heures (**[!UICONTROL Processing]** status).

>[!NOTE]
>
>When [création d’une surface de canal](channel-surfaces.md#create-channel-surface), si vous sélectionnez un pool d’adresses IP en cours d’édition (**[!UICONTROL Processing]** ) et n’a jamais été associé au sous-domaine sélectionné pour cette surface, vous ne pouvez pas poursuivre la création de surface. [En savoir plus](channel-surfaces.md#subdomains-and-ip-pools)

Pour vérifier l’état de mise à jour du pool d’adresses IP, cliquez sur le bouton **[!UICONTROL More actions]** et sélectionnez **[!UICONTROL Recent updates]**.

![](assets/ip-pool-recent-update.png)

>[!NOTE]
>
>Une fois qu’un pool d’adresses IP a été mis à jour, vous devrez peut-être attendre :
>* quelques minutes avant d&#39;être consommée par les messages unitaires,
>* jusqu’au lot suivant pour que le pool d’adresses IP soit efficace dans les messages par lots.


Vous pouvez également utiliser la variable **[!UICONTROL Delete]** pour supprimer un pool d’adresses IP. Notez que vous ne pouvez pas supprimer un pool d’adresses IP qui a été associé à une surface de canal.

