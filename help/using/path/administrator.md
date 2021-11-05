---
title: Prise en main de Journey Optimizer pour l’administrateur système
description: En tant qu’administrateur système, découvrez comment utiliser Journey Optimizer
level: Intermediate
source-git-commit: a27a6d7ab96bd08e7a2601c2e86d1d9f0fc4be0a
workflow-type: tm+mt
source-wordcount: '693'
ht-degree: 22%

---

# Prise en main pour les administrateurs système

![administrator](assets/do-not-localize/user-2.png)

Avant de commencer à utiliser [!DNL Adobe Journey Optimizer], plusieurs étapes sont nécessaires pour préparer votre environnement.  Vous devez effectuer les étapes suivantes afin que la variable [Ingénieur de données](data-engineer.md) et [Praticien parcours](marketer.md) peut commencer à utiliser [!DNL Adobe Journey Optimizer].


Comme **Administrateur système**, vous devez **comprendre les profils de produit et attribuer des autorisations** pour l’administration des environnements de test et la configuration des canaux. Vous devez également configurer des environnements sandbox et les gérer pour les profils de produit disponibles. Vous pourrez ensuite affecter des membres de l’équipe aux profils de produit.

Ces fonctionnalités peuvent être gérées par **[!UICONTROL Administrateurs de produits]** qui ont accès à Admin Console. [En savoir plus sur Adobe Admin Console](https://helpx.adobe.com/fr/enterprise/admin-guide.html){target=&quot;_blank&quot;}.

Découvrez la gestion des accès dans les pages suivantes :

1. **Création d’environnements de test** pour partitionner vos instances en environnements virtuels distincts et isolés. **Environnements de test** sont créées dans [!DNL Journey Optimizer]. En savoir plus dans la section [Environnements de test](../administration/sandboxes.md) .

   >[!NOTE]
   >Comme **Administrateur système**, si vous ne pouvez pas voir la variable **[!UICONTROL Environnements de test]** dans [!DNL Journey Optimizer], mettez à jour vos autorisations dans le [Admin Console](https://adminconsole.adobe.com/){_blank}. Découvrez comment mettre à jour votre profil de produit dans [cette page](../administration/permissions.md#edit-product-profile).

1. **Présentation des profils de produit**. Les profils de produit sont un ensemble de droits unitaires qui permet aux utilisateurs d’accéder à certaines fonctionnalités ou à certains objets dans l’interface. En savoir plus dans la section [Profils de produit d’usine](../administration/ootb-product-profiles.md) .

1. **Définition des autorisations** pour les profils de produit, y compris **Environnements de test** et donner accès aux membres de votre équipe en les affectant à différents profils de produit. Cette étape est effectuée dans la variable [Admin Console](https://adminconsole.adobe.com/){_blank}. Les autorisations sont des droits unitaires qui vous permettent de définir les autorisations attribuées à **[!UICONTROL Profil de produit]**. Chaque autorisation est regroupée sous des fonctionnalités, par exemple Parcours, Messages ou Offres, ce qui représente les différentes fonctionnalités ou objets dans [!DNL Journey Optimizer]. En savoir plus dans la section [Niveaux d’autorisation](../administration/high-low-permissions.md) .


En outre, vous devez **Déployer[!DNL Adobe Experience Manager Assets Essentials]** pour gérer les ressources et les images dans vos messages : utilisateurs qui doivent accéder à [!DNL Assets Essentials] doit faire partie de la variable **Utilisateurs clients Assets Essentials** ou/et **Utilisateurs d’Assets Essentials** Profils de produit. [En savoir plus dans la documentation Assets Essentials](https://experienceleague.adobe.com/docs/experience-manager-assets-essentials/help/deploy-administer.html?lang=fr){target=&quot;_blank&quot;}.

Lors de l&#39;accès à [!DNL Journey Optimizer] pour la première fois, vous recevez un environnement Sandbox de production et un certain nombre d&#39;adresses IP vous sont attribuées en fonction de votre contrat.

Pour pouvoir créer vos parcours et envoyer des messages, accédez à la **ADMINISTRATION** . Parcourez les **[!UICONTROL Canaux]** pour configurer vos emails et vos paramètres prédéfinis.

>[!NOTE]
>Comme **Administrateur système**, si vous ne pouvez pas voir la variable **[!UICONTROL Canaux]** dans [!DNL Journey Optimizer], mettez à jour vos autorisations dans le [Admin Console](https://adminconsole.adobe.com/){_blank}. Découvrez comment mettre à jour votre profil de produit dans [cette page](../administration/permissions.md#edit-product-profile).

Suivez les étapes répertoriées ci-dessous :

1. **Configuration des messages et des canaux**: définir des paramètres prédéfinis, adapter et personnaliser les paramètres des emails et des messages push ;

   * Définir **paramètres des notifications push** dans les deux [!DNL Adobe Experience Platform] et [!DNL Adobe Experience Platform Launch]. [En savoir plus](../push-gs.md)

   * Créer **paramètres prédéfinis de message** pour configurer tous les paramètres techniques requis pour les emails et les notifications push. [En savoir plus](../configuration/message-presets.md)

   * gérer le nombre de jours pendant lesquels **reprises** sont exécutés avant d’envoyer des adresses électroniques à la liste de suppression. [En savoir plus](../configuration/manage-suppression-list.md)

1. **Déléguer des sous-domaines** : pour un nouveau sous-domaine à utiliser dans Journey Optimizer, la première étape consiste à le déléguer. [En savoir plus](../configuration/about-subdomain-delegation.md)

   ![](../assets/subdomain.png)

1. **Créer des pools d&#39;adresses IP** : améliorez la délivrabilité et la réputation de vos e-mails en regroupant les adresses IP configurées avec votre instance. [En savoir plus](../configuration/ip-pools.md)

   ![](../assets/ip-pool.png)

1. **Gestion de la suppression et de la liste autorisée**: améliorer votre délivrabilité avec suppression et listes autorisées ;

   * A [liste de suppression](../suppression-list.md) se compose d’adresses email que vous souhaitez exclure de vos diffusions, car l’envoi à ces contacts peut nuire à votre réputation d’envoi et à vos taux de diffusion. Vous pouvez surveiller toutes les adresses électroniques qui sont automatiquement exclues de l’envoi d’un parcours, telles que les adresses non valides, les adresses qui rebondissent constamment et qui pourraient nuire à la réputation de votre email, ainsi que les destinataires qui envoient une plainte de spam d’une sorte contre l’un de vos emails. Découvrez comment gérer le [liste de suppression](../configuration/manage-suppression-list.md) et [reprises](../configuration/retries.md).

   ![](../assets/suppression-list-filtering-example.png)

   * Le [liste autorisée](../allow-list.md) vous permet de spécifier des adresses électroniques ou des domaines individuels qui seront les seuls destinataires ou domaines autorisés à recevoir les courriers électroniques que vous envoyez à partir d’un environnement de test spécifique. Cela peut vous empêcher d&#39;envoyer accidentellement des e-mails à des adresses client réelles lorsque vous vous trouvez dans un environnement de test. Découvrez comment [activer la liste autorisée](../allow-list.md).
   En savoir plus sur la gestion de la délivrabilité dans [!DNL Adobe Journey Optimizer] [dans cette page](../deliverability.md).

