---
solution: Journey Optimizer
product: journey optimizer
title: Prise en main de la configuration des emails
description: En savoir plus sur la configuration des emails dans [!DNL Journey Optimizer]
role: Admin
level: Intermediate
feature: Application Settings
topic: Administration
exl-id: 1fc9a4f6-6c34-4414-b400-aac6bda9ee25
source-git-commit: d1c11881654580247e8d7c92237cad130f11f749
workflow-type: tm+mt
source-wordcount: '202'
ht-degree: 0%

---

# Prise en main de la configuration des emails {#get-starte-email-config}

Pour envoyer des emails par le biais de parcours et de campagnes dans [!DNL Journey Optimizer], vous devez passer par plusieurs étapes de configuration.

1. Pour garantir une délivrabilité optimale et protéger votre réputation, commencez par déléguer à Adobe les sous-domaines que vous allez utiliser pour envoyer vos emails. [!DNL Journey Optimizer]. Ces sous-domaines déterminent des éléments tels que les pages web à suivre et les URL de page miroir. [En savoir plus](../configuration/about-subdomain-delegation.md)

   ![](../configuration/assets/subdomain-list.png)

1. Améliorez la délivrabilité et la réputation de vos emails en regroupant les adresses IP configurées avec votre instance. [En savoir plus](../configuration/ip-pools.md)

   ![](../configuration/assets/ip-pool-create.png)

1. Créez des surfaces de canal et sélectionnez **[!UICONTROL Email]** canal. [En savoir plus](../configuration/channel-surfaces.md)


   ![](../configuration/assets/preset-general.png)

1. Dans chaque surface de canal email, configurez tous les paramètres techniques requis pour diffuser les emails. [En savoir plus](email-settings.md)

   * C’est là que vous sélectionnez le sous-domaine à utiliser pour envoyer les emails et les pools d’adresses IP à associer à la surface. [En savoir plus](email-settings.md#subdomains-and-ip-pools)

   ![](assets/preset-subdomain-ip-pool.png)

   * Le **[!UICONTROL Sender email]** et **[!UICONTROL Error email]** Les adresses doivent utiliser le sous-domaine délégué sélectionné actuel. [En savoir plus](email-settings.md#email-header)

   ![](assets/preset-header.png)

1. Déterminez l’adresse électronique à utiliser en priorité pour vos destinataires lorsque plusieurs adresses sont disponibles dans Adobe Experience Platform. [En savoir plus](../configuration/primary-email-addresses.md)

   ![](../configuration/assets/primary-address-execution-fields.png)

1. Gérez le nombre de jours pendant lesquels des reprises sont effectuées avant d’envoyer des adresses électroniques à la liste de suppression. [En savoir plus](../configuration/manage-suppression-list.md)

   ![](../configuration/assets/suppression-list-edit-retries.png)
