---
solution: Journey Optimizer
product: journey optimizer
title: Commencer la configuration du canal e-mail
description: En savoir plus sur la configuration du canal e-mail dans  [!DNL Journey Optimizer].
role: Admin
level: Experienced
feature: Channel Configuration, Email
topic: Administration
keywords: e-mail, configuration, surface, sous-domaines
exl-id: 1fc9a4f6-6c34-4414-b400-aac6bda9ee25
source-git-commit: 9274277872e34f47e05be1acfe248a3b3303cb13
workflow-type: tm+mt
source-wordcount: '229'
ht-degree: 84%

---

# Commencer la configuration du canal e-mail {#get-starte-email-config}

Pour envoyer des e-mails par le biais de parcours et de campagnes dans [!DNL Journey Optimizer], vous devez passer par plusieurs étapes de configuration.

1. Pour garantir une délivrabilité optimale et protéger votre réputation, commencez par **déléguer à Adobe les sous-domaines** que vous allez utiliser pour envoyer vos e-mails avec [!DNL Journey Optimizer]. Ces sous-domaines déterminent des éléments tels que les pages web à suivre et les URL de page miroir. [En savoir plus](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. Créez des groupes d’adresses IP pour **regrouper les adresses IP** approvisionnées avec votre instance. [En savoir plus](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. Créez des **configurations de canal** et sélectionnez le canal **[!UICONTROL E-mail]**. [En savoir plus](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. Dans chaque configuration de canal e-mail, configurez tous les **paramètres techniques** requis pour diffuser les e-mails. [En savoir plus](email-settings.md)

   * C’est là que vous sélectionnez le sous-domaine à utiliser pour envoyer les e-mails et les groupes d’adresses IP à associer à la configuration. [En savoir plus](email-settings.md#ip-pools)

   ![](assets/surface-subdomain-ip-pool.png)

   * Les champs **[!UICONTROL Préfixe d’e-mail de l’expéditeur]** et **[!UICONTROL Préfixe d’e-mail d’erreur]** utilisent le [sous-domaine délégué](../configuration/about-subdomain-delegation.md) actuellement sélectionné. Vous pouvez éventuellement identifier **[!UICONTROL Nom de l’expéditeur]** et **[!UICONTROL E-mail de l’expéditeur]** une autre partie émettrice (adresse **expéditeur** complète, non liée à ce suffixe de sous-domaine). [En savoir plus](header-parameters.md#sender-header)

   ![](assets/preset-header.png)

1. Déterminez les **champs d’exécution** à utiliser en priorité pour vos personnes destinataires lorsque plusieurs adresses sont disponibles dans Adobe Experience Platform. [En savoir plus](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. Gérez le nombre de jours pendant lesquels des **reprises** sont effectuées avant de transmettre des adresses e-mail à la liste de suppression. [En savoir plus](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
