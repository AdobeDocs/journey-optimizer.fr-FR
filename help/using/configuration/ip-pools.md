---
title: Création de pools d'adresses IP
description: '"Découvrir comment gérer les pools d''adresses IP"'
feature: Application Settings
topic: Administration
role: Admin
level: Intermediate
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: a485c58366f0690fb2515139658224d59468a24f
workflow-type: tm+mt
source-wordcount: '542'
ht-degree: 87%

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

1. Accédez au menu **[!UICONTROL Canaux]**/**[!UICONTROL Pools d&#39;adresses IP]**, puis cliquez sur **[!UICONTROL Créer un pool d&#39;adresses IP]**.

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

Le pool d&#39;adresses IP est maintenant créé et s&#39;affiche dans la liste. Vous pouvez le sélectionner pour accéder à ses propriétés et afficher le préréglage de message associé. Pour plus d&#39;informations sur l&#39;association d&#39;un paramètre prédéfini de message à un pool d&#39;adresses IP, reportez-vous à la section [cette section](message-presets.md).

![](assets/ip-pool-created.png)

## Modification d&#39;un pool d&#39;adresses IP {#edit-ip-pool}

Pour modifier un pool d’adresses IP :

1. Dans la liste, cliquez sur le nom du pool d’adresses IP pour l’ouvrir.

   ![](assets/ip-pool-list.png)

1. Modifiez ses propriétés selon vos besoins. Vous pouvez modifier la description et ajouter ou supprimer des adresses IP.

   ![](assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >Procédez avec attention lorsque vous envisagez de supprimer une adresse IP, car cela entraîne une charge supplémentaire pour les autres adresses IP, ce qui peut avoir de graves répercussions sur votre délivrabilité. En cas de doute, contactez un expert en délivrabilité.

1. Enregistrez vos modifications.

>[!NOTE]
>
>Le nom du pool d’adresses IP n’est pas modifiable. Si vous souhaitez le modifier, vous devez supprimer le pool d’adresses IP et en créer un autre avec le nom de votre choix.

La mise à jour est effective immédiatement ou de manière asynchrone, selon que le pool d’adresses IP est associé ou non à un [préréglage de message](message-presets.md) :

* Si le pool d’adresses IP n’est **pas** sélectionné dans un préréglage de message, la mise à jour est instantanée (statut **[!UICONTROL Succès]**).
* Si le pool d’adresses IP **est** sélectionné dans un préréglage de messages, la mise à jour peut prendre jusqu’à 7 à 10 jours ouvrables (statut **[!UICONTROL En cours de traitement]**).

>[!NOTE]
>
>When [création d’un paramètre prédéfini de message](message-presets.md#create-message-preset), si vous sélectionnez un pool d’adresses IP en cours d’édition (**[!UICONTROL Traitement]** (état) et n’a jamais été associé au sous-domaine sélectionné pour ce paramètre prédéfini, vous ne pouvez pas poursuivre la création du paramètre prédéfini. [En savoir plus](message-presets.md#subdomains-and-ip-pools)

Pour vérifier l’état de mise à jour du pool d’adresses IP, cliquez sur le bouton **[!UICONTROL Autres actions]** et sélectionnez **[!UICONTROL Mises à jour récentes]**.

![](assets/ip-pool-recent-update.png)

>[!NOTE]
>
>Une fois qu’un pool d’adresses IP a été mis à jour, vous devrez peut-être attendre :
>* quelques minutes avant qu&#39;il soit consommé par les messages unitaires ;
>* jusqu’au lot suivant pour que le pool d’adresses IP soit effectif dans les messages par lots ;


Vous pouvez également utiliser le bouton **[!UICONTROL Supprimer]** pour supprimer un pool d’adresses IP. Notez que vous ne pouvez pas supprimer un pool d’adresses IP associé à un préréglage de message.

