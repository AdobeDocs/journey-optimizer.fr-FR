---
title: Prise en main de Journey Optimizer pour l’administrateur système
description: En tant qu’administrateur système, découvrez comment utiliser Journey Optimizer
level: Intermediate
exl-id: 24f85ced-aa45-493f-b2c4-7c7b58351b38
source-git-commit: f0c5b42984b76fee005fe0c0e10312d47f9d10e8
workflow-type: ht
source-wordcount: '693'
ht-degree: 100%

---

# Prise en main pour les administrateurs système

![administrateur](assets/do-not-localize/user-2.png)

Avant de commencer à utiliser [!DNL Adobe Journey Optimizer], plusieurs étapes sont nécessaires pour préparer votre environnement. Vous devez effectuer les étapes suivantes afin que l’[Ingénieur de données](data-engineer.md) et le [Praticien Parcours](marketer.md) puissent commencer à utiliser [!DNL Adobe Journey Optimizer]. 


En tant qu’**administrateur système**, vous devez **connaître les profils de produit et attribuer des autorisations** pour l’administration des sandbox et la configuration des canaux. Vous devez également configurer des sandbox et les gérer pour les profils de produit disponibles. Vous pourrez ensuite affecter des membres de l’équipe aux profils de produit. 

Ces fonctionnalités peuvent être gérées par les **[!UICONTROL administrateurs produits]** qui ont accès à Admin Console. [En savoir plus sur Adobe Admin Console](https://helpx.adobe.com/fr/enterprise/admin-guide.html){target=&quot;_blank&quot;}.

Découvrez la gestion des accès dans les pages suivantes :

1. **Créer des sandbox** pour partitionner vos instances en environnements virtuels distincts et isolés. Les **sandbox** sont créées dans [!DNL Journey Optimizer]. Pour en savoir plus, consultez la section [Sandbox](../administration/sandboxes.md). 

   >[!NOTE]
   >En tant qu’**administrateur système**, si le menu **[!UICONTROL Sandbox]** ne s’affiche pas dans [!DNL Journey Optimizer], mettez à jour vos autorisations dans l’[Admin Console](https://adminconsole.adobe.com/){_blank}. Découvrez comment mettre à jour votre profil de produit sur [cette page](../administration/permissions.md#edit-product-profile). 

1. **Présentation des profils de produit**. Les profils de produit sont un ensemble de droits unitaires qui permet aux utilisateurs d’accéder à certaines fonctionnalités ou à certains objets dans l’interface. Pour en savoir plus, consultez la section [Profils de produit d’usine](../administration/ootb-product-profiles.md). 

1. **Définissez les autorisations** pour les profils de produits, y compris les **Sandbox**, et donnez l’accès aux membres de votre équipe en les affectant à différents profils de produits. Cette étape est effectuée dans l’[Admin Console](https://adminconsole.adobe.com/){_blank}. Les autorisations sont des droits unitaires qui vous permettent de définir les autorisations attribuées au **[!UICONTROL Profil de produit]**. Chaque autorisation est regroupée sous des fonctionnalités, par exemple Parcours, Messages ou Offres, ce qui représente les différentes fonctionnalités ou objets dans [!DNL Journey Optimizer]. Pour en savoir plus, consultez la section [Niveaux d’autorisation](../administration/high-low-permissions.md). 


En outre, vous devez **déployer[!DNL Adobe Experience Manager Assets Essentials]** pour gérer les ressources et les images dans vos messages : les utilisateurs qui nécessitent l’accès à [!DNL Assets Essentials] doivent faire partie des profils de produit **Utilisateurs clients Assets Essentials** ou/et **Utilisateurs Assets Essentials**. [Pour en savoir plus, consultez la documentation sur Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html?lang=fr){target=&quot;_blank&quot;}. 

Lorsque vous accédez à [!DNL Journey Optimizer] pour la première fois, une sandbox de production vous est allouée ainsi qu’un certain nombre d’adresses IP en fonction de votre contrat. 

Pour pouvoir créer vos parcours et envoyer des messages, accédez au menu **ADMINISTRATION**. Parcourez le menu **[!UICONTROL Canaux]** pour configurer vos e-mails et vos préréglages.  

>[!NOTE]
>En tant qu’**administrateur système**, si le menu **[!UICONTROL Canaux]** ne s’affiche pas dans [!DNL Journey Optimizer], mettez à jour vos autorisations dans l’[Admin Console](https://adminconsole.adobe.com/){_blank}. Découvrez comment mettre à jour votre profil de produit sur [cette page](../administration/permissions.md#edit-product-profile). 

Suivez les étapes énumérées ci-dessous :

1. **Configurer les messages et les canaux** : définir des préréglages, adapter et personnaliser les paramètres des e-mails et des messages push.

   * Définissez **les paramètres des notifications push** dans [!DNL Adobe Experience Platform] et [!DNL Adobe Experience Platform Launch]. [En savoir plus](../push-gs.md)

   * Créez des **préréglages de messages** pour configurer tous les paramètres techniques requis pour les e-mails et les notifications push. [En savoir plus](../configuration/message-presets.md)

   * Gérez le nombre de jours pendant lesquels des **reprises** sont effectuées avant de transmettre des adresses e-mail à la liste de suppression. [En savoir plus](../configuration/manage-suppression-list.md)

1. **Déléguer des sous-domaines** : pour un nouveau sous-domaine à utiliser dans Journey Optimizer, la première étape consiste à le déléguer. [En savoir plus](../configuration/about-subdomain-delegation.md)

   ![](../assets/subdomain.png)

1. **Créer des pools d&#39;adresses IP** : améliorez la délivrabilité et la réputation de vos e-mails en regroupant les adresses IP configurées avec votre instance. [En savoir plus](../configuration/ip-pools.md)

   ![](../assets/ip-pool.png)

1. **Gérer les listes de suppression et d’autorisation** : améliorez votre délivrabilité grâce aux listes de suppression et d’autorisation. 

   * Une [liste de suppression](../suppression-list.md) est constituée d’adresses e-mail que vous souhaitez exclure de vos diffusions, car l’envoi d’e-mails à ces contacts pourrait nuire à votre réputation d’envoi et à vos taux de diffusion. Vous pouvez surveiller toutes les adresses e-mail qui sont automatiquement exclues de l’envoi d’un parcours, telles que les adresses non valides, les adresses qui entraînent constamment des soft bounces et qui pourraient nuire à la réputation de vos e-mails, ainsi que les destinataires qui demandent le classement de l’un de vos e-mails comme spam. Découvrez comment gérer la [liste de suppression](../configuration/manage-suppression-list.md) et les [reprises](../configuration/retries.md).
   ![](../assets/suppression-list-filtering-example.png)

   * La [liste autorisée](../allow-list.md) vous permet de spécifier des adresses e-mail ou des domaines individuels qui seront les seuls destinataires ou domaines autorisés à recevoir les e-mails que vous envoyez à partir d’un environnement Sandbox spécifique. Cela peut vous empêcher d’envoyer accidentellement des e-mails à des adresses client réelles lorsque vous vous trouvez dans un environnement de test. Découvrez comment [activer la liste autorisée](../allow-list.md).
   En savoir plus sur la gestion de la délivrabilité dans [!DNL Adobe Journey Optimizer] [sur cette page](../deliverability.md).
