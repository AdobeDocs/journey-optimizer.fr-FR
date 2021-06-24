---
title: Gestion des environnements de test
description: Découvrir comment gérer les environnements de test
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
exl-id: null
feature: Populations témoins
topic: Administration
role: Administrator
level: Intermediate
source-git-commit: 4be1d6f4034a0bb0a24fe5e4f634253dc1ca798e
workflow-type: tm+mt
source-wordcount: '350'
ht-degree: 100%

---

# Gestion des environnements de test {#sandboxes}

## Utilisation des environnements de test {#using-sandbox}

[!DNL Journey Optimizer] vous permet de partitionner votre instance en environnements virtuels séparés appelés Sandbox.
Les environnements Sandbox sont affectés par le biais des profils de produit dans Admin console. [Découvrez comment affecter des environnements Sandbox](permissions.md#create-product-profile).

[!DNL Journey Optimizer] reflète les environnements Sandbox Adobe Experience Platform qui ont été créés pour une organisation donnée.
Vous pouvez créer ou réinitialiser des environnements Sandbox Adobe Experience Platform à partir de votre instance Adobe Experience Platform. [Pour en savoir plus, consultez le guide d&#39;utilisation des environnements Sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=fr).

La commande de sélecteur des environnements Sandbox se trouve dans la partie supérieure gauche de votre écran. Pour passer d&#39;un environnement Sandbox à un autre, cliquez sur l&#39;environnement Sandbox actif dans le sélecteur et sélectionnez-en un autre dans la liste déroulante.

## Affectation d&#39;environnements Sandbox {#assign-sandboxes}

>[!IMPORTANT]
>
> La gestion des environnements Sandbox peut uniquement être effectuée par un administrateur **[!UICONTROL Produit]** ou **[!UICONTROL Système]**. Pour plus d&#39;informations à ce sujet, consultez la [documentation relative à Admin Console](https://helpx.adobe.com/fr/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html).

Vous pouvez choisir d&#39;affecter différents environnements Sandbox aux **[!UICONTROL profils de produit]** prêts à l&#39;emploi ou personnalisés.

Pour affecter des environnements Sandbox :

1. Dans l&#39;onglet **[!UICONTROL Produits]** de [!DNL Admin Console], sélectionnez le produit **[!UICONTROL Adobe Experience Platform Apps]**.

1. Sélectionnez un **[!UICONTROL profil de produit]**.

   ![](../assets/sandbox_1.png)

1. Sélectionnez l&#39;onglet **[!UICONTROL Autorisations]**.

1. Sélectionnez la fonctionnalité **[!UICONTROL Environnements Sandbox]**.

   ![](../assets/sandbox_2.png)

1. Dans **[!UICONTROL Éléments d&#39;autorisations disponibles]**, cliquez sur l&#39;icône plus (+) pour affecter des environnements Sandbox à votre profil. [En savoir plus sur les environnements Sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=fr).

   ![](../assets/sandbox_3.png)

1. Si nécessaire, dans **[!UICONTROL Éléments d&#39;autorisations disponibles]**, cliquez sur l&#39;icône X pour supprimer l&#39;accès des environnements Sandbox à votre **[!UICONTROL profil de produit]**.

   ![](../assets/sandbox_4.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

## Accès au contenu {#content-access}

Pour configurer l&#39;accessibilité de votre contenu, vous devez affecter un dossier de contenu partagé à chacun de vos environnements Sandbox. Vous pouvez créer et configurer votre dossier partagé dans l&#39;onglet **[!UICONTROL Stockage]** affiché dans [!DNL Admin Console] pour les administrateurs. Si vous avez accès à [!DNL Admin Console] en tant qu&#39;administrateur système, vous pouvez créer des dossiers partagés et ajouter des délégués ayant un niveau d&#39;accès différent à ceux-ci.

![](../assets/do-not-localize/content_access.png)

Notez que pour que votre contenu soit synchronisé avec l&#39;environnement Sandbox correct, vous devez suivre la même syntaxe que cet environnement. Par exemple, si votre environnement Sandbox est appelé développement, votre dossier partagé doit porter le même nom.

[Découvrez comment gérer les dossiers partagés](https://helpx.adobe.com/fr/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html) .
