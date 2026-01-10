---
solution: Journey Optimizer
product: journey optimizer
title: Créer des groupes d’adresses IP
description: Découvrez comment gérer des groupes d’adresses IP
feature: Subdomains, Channel Configuration
topic: Administration
role: Admin
level: Experienced
keywords: adresses IP, groupes, groupe, sous-domaines, délivrabilité
exl-id: 606334c3-e3e6-41c1-a10e-63508a3ed747
source-git-commit: a44b68e99ec4c55b8ed27b244fcb9e76bdb97760
workflow-type: tm+mt
source-wordcount: '721'
ht-degree: 100%

---

# Créer des groupes d’adresses IP {#create-ip-pools}

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool_header"
>title="Configurer un groupe d’adresses IP"
>abstract="Les groupes d’adresses IP rassemblent les adresses IP de vos sous-domaines pour une délivrabilité des e-mails améliorée."

>[!CONTEXTUALHELP]
>id="ajo_admin_ip_pool"
>title="Configurer un groupe d’adresses IP"
>abstract="Journey Optimizer vous permet de créer des groupes d’adresses IP afin de regrouper les adresses IP de vos sous-domaines. Cela peut améliorer considérablement la délivrabilité de vos e-mails, car ce faisant, vous pouvez empêcher la réputation d’un sous-domaine d’avoir un impact sur vos autres sous-domaines."

## À propos des groupes d’adresses IP {#about-ip-pools}

Avec [!DNL Journey Optimizer], vous pouvez créer des groupes d’adresses IP pour regrouper les adresses IP de vos sous-domaines.

La création de pools d&#39;adresses IP est vivement recommandée pour la délivrabilité des e-mails. Ce faisant, vous pouvez empêcher la réputation d&#39;un sous-domaine d&#39;avoir un impact sur vos autres sous-domaines.

Par exemple, il est recommandé d&#39;avoir un pool d&#39;adresses IP pour vos messages marketing, et un autre pour vos messages transactionnels. De cette manière, si les performances de l&#39;un de vos messages marketing sont mauvaises et s&#39;il est déclaré comme indésirable par un client, cela n&#39;affecte pas les messages transactionnels envoyés à ce même client, qui recevra toujours des messages transactionnels (confirmations d’achat, messages de récupération de mot de passe, etc.).

>[!CAUTION]
>
>La configuration du groupe d’adresses IP est commune à tous les environnements. Par conséquent, toute création ou modification de groupe d’adresses IP aura également un impact sur les sandbox de production.

## Création d&#39;un pool d&#39;adresses IP {#create-ip-pool}

Pour créer un pool d&#39;adresses IP, procédez comme suit :

1. Accédez au menu **[!UICONTROL Administration]** > **[!UICONTROL Canaux]** > **[!UICONTROL Paramètres des e-mails]** > **[!UICONTROL Groupes d’adresses IP]**, puis cliquez sur **[!UICONTROL Créer un groupe d’adresses IP]**.

   ![](assets/ip-pool-create.png)

1. Attribuez un nom et une description (facultatif) au groupe d’adresses IP.

   >[!NOTE]
   >
   >Le nom doit commencer par une lettre (A-Z) et contenir uniquement des caractères alphanumériques ou des caractères spéciaux ( _, ., - ).

1. Sélectionnez les adresses IP à inclure dans le pool dans la liste déroulante, puis cliquez sur **[!UICONTROL Envoyer]**.

   ![](assets/ip-pool-config.png)

   >[!NOTE]
   >
   >Toutes les adresses IP configurées avec votre instance sont disponibles dans la liste.

Lors de la sélection des adresses IP, vous pouvez voir dans la liste les enregistrements PTR associés aux adresses IP. Vous pouvez ainsi vérifier les informations de branding de chaque adresse IP lors de la création d’un groupe d’adresses IP et sélectionner les adresses IP avec les mêmes informations de branding, par exemple. [En savoir plus sur les enregistrements PTR.](ptr-records.md)

![](assets/ip-pool-ptr-record.png)

>[!NOTE]
>
>Si aucun enregistrement PTR n’est configuré pour une adresse IP, vous ne pouvez pas la sélectionner. Pour configurer l’enregistrement PTR de cette adresse IP, contactez votre représentant ou représentante Adobe.<!--Now this only happens when first subdomain delegated to Adobe is with CNAME method.-->

Une fois un groupe d’adresses IP créé, les informations PTR sont visibles lorsque vous pointez sur les adresses IP affichées sous la liste déroulante du groupe d’adresses IP.

![](assets/ip-pool-ptr-record-tooltip.png)

Le groupe d&#39;adresses IP est maintenant créé et s&#39;affiche dans la liste. Vous pouvez le sélectionner pour accéder à ses propriétés et afficher la configuration de canal associée (c’est-à-dire le paramètres prédéfini de message). Pour plus d’informations sur l’association d’une configuration de canal à un groupe d’adresses IP, consultez [cette section](channel-surfaces.md).

## Modifier un groupe d’adresses IP {#edit-ip-pool}

Pour modifier un groupe dʼadresses IP, suivez les étapes ci-dessous.

1. Dans la liste, cliquez sur le nom du pool d’adresses IP pour l’ouvrir.

1. Modifiez ses propriétés selon vos besoins. Vous pouvez modifier la description et ajouter ou supprimer des adresses IP.

   >[!NOTE]
   >
   >Le nom du pool d’adresses IP n’est pas modifiable. Si vous souhaitez le modifier, vous devez supprimer le pool d’adresses IP et en créer un autre avec le nom de votre choix.

   ![](assets/ip-pool-edit.png)

   >[!CAUTION]
   >
   >Procédez avec attention lorsque vous envisagez de supprimer une adresse IP, car cela entraîne une charge supplémentaire pour les autres adresses IP, ce qui peut avoir de graves répercussions sur votre délivrabilité. En cas de doute, contactez un expert en délivrabilité.

1. Enregistrez vos modifications.

La mise à jour est effective immédiatement ou de manière asynchrone, selon que le groupe d’adresses IP est associé ou non à une [configuration de canal](channel-surfaces.md) :

* Si le groupe d’adresses IP **n’est pas** associé à une quelconque configuration de canal, la mise à jour est instantanée (statut **[!UICONTROL Succès]**).
* Si le groupe d’adresses IP **est** associé à une configuration de canal, la mise à jour peut prendre jusqu’à 3 heures (statut **[!UICONTROL En cours de traitement]**).

>[!NOTE]
>
>Lors de la [création d’une configuration de canal](channel-surfaces.md#create-channel-surface), si vous sélectionnez un groupe d’adresses IP en cours d’édition (statut **[!UICONTROL En cours de traitement]**) et qui n’a jamais été associé au sous-domaine sélectionné pour cette configuration, vous ne pouvez pas poursuivre la création de la configuration. [En savoir plus](channel-surfaces.md#create-channel-surface)

Pour vérifier l’état de mise à jour du pool d’adresses IP, cliquez sur le bouton **[!UICONTROL Autres actions]** et sélectionnez **[!UICONTROL Mises à jour récentes]**.

![](assets/ip-pool-recent-update.png)

>[!NOTE]
>
>Une fois qu’un pool d’adresses IP a été mis à jour, vous devrez peut-être attendre :
>
>* quelques minutes avant qu&#39;il soit consommé par les messages unitaires ;
>* jusqu’au lot suivant pour que le pool d’adresses IP soit effectif dans les messages par lots ;

Vous pouvez également utiliser le bouton **[!UICONTROL Supprimer]** pour supprimer un pool d’adresses IP. Sachez que vous ne pouvez pas supprimer un groupe d’adresses IP associé à une configuration de canal.

