---
solution: Journey Optimizer
product: journey optimizer
title: Gestion des sandbox
description: Découvrir comment gérer les sandbox
feature: Sandboxes
topic: Administration
role: Admin, Architect, Developer
level: Experienced
keywords: sandbox, virtuels, environnements, organisation, platform
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
source-git-commit: 16738786e4ebeef3417fd0f6e5be741b348c2744
workflow-type: tm+mt
source-wordcount: '387'
ht-degree: 100%

---

# Gestion des sandbox {#sandboxes}

## Utilisation des sandbox {#using-sandbox}

[!DNL Journey Optimizer] vous permet de partitionner votre instance en environnements virtuels séparés appelés Sandbox.
Les environnements Sandbox sont affectés par le biais des profils de produit dans Admin console. [Découvrez comment affecter des sandbox](permissions.md#create-product-profile).

[!DNL Journey Optimizer] reflète les sandbox Adobe Experience Platform qui ont été créés pour une organisation donnée.
Vous pouvez créer ou réinitialiser des sandbox Adobe Experience Platform à partir de votre instance Adobe Experience Platform. [Pour en savoir plus, consultez le guide d’utilisation des sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=fr){target="_blank"}.

Le sélecteur de sandbox se trouve dans le coin supérieur droit de votre écran, à côté du nom de votre organisation. Pour passer d’un sandbox à un autre, cliquez sur le sandbox actif dans le sélecteur et sélectionnez-en un autre dans la liste déroulante.

![](assets/sandbox_5.png)

➡️ [En savoir plus sur les sandbox dans cette vidéo](#video)

## Affectation de sandbox {#assign-sandboxes}

>[!IMPORTANT]
>
> La gestion des sandbox peut uniquement être effectuée par un administrateur **[!UICONTROL Produit]** ou **[!UICONTROL Système]**. Pour plus d’informations à ce sujet, consultez la [documentation relative à Admin Console](https://helpx.adobe.com/fr/enterprise/admin-guide.html/enterprise/using/admin-roles.ug.html){target="_blank"}.

Vous pouvez choisir d’affecter différents sandbox aux **[!UICONTROL profils de produit]** prêts à l’emploi ou personnalisés.

Pour affecter des sandbox :

1. Dans l&#39;onglet **[!UICONTROL Produits]** de [!DNL Admin Console], sélectionnez le produit **[!UICONTROL Adobe Experience Platform Apps]**.

1. Sélectionnez un **[!UICONTROL profil de produit]**.

   ![](assets/sandbox_1.png)

1. Sélectionnez l&#39;onglet **[!UICONTROL Autorisations]**.

1. Sélectionnez la fonctionnalité **[!UICONTROL Sandbox]**.

   ![](assets/sandbox_2.png)

1. Dans **[!UICONTROL Éléments d’autorisations disponibles]**, cliquez sur l’icône plus (+) pour affecter des sandbox à votre profil. [En savoir plus sur les sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/home.html?lang=fr){target="_blank"}.

   ![](assets/sandbox_3.png)

1. Si nécessaire, dans **[!UICONTROL Éléments d’autorisations disponibles]**, cliquez sur l’icône X pour supprimer l’accès des sandbox à votre **[!UICONTROL profil de produit]**.

   ![](assets/sandbox_4.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

## Accès au contenu {#content-access}

Pour configurer l’accessibilité de votre contenu, vous devez affecter un dossier de contenu partagé à chacun de vos sandbox. Vous pouvez créer et configurer votre dossier partagé dans l&#39;onglet **[!UICONTROL Stockage]** affiché dans [!DNL Admin Console] pour les administrateurs. Si vous avez accès à [!DNL Admin Console] en tant qu&#39;administrateur système, vous pouvez créer des dossiers partagés et ajouter des délégués ayant un niveau d&#39;accès différent à ceux-ci.

![](assets/do-not-localize/content_access.png)

Notez que pour que votre contenu soit synchronisé avec le sandbox correct, vous devez suivre la même syntaxe que cet environnement. Par exemple, si votre sandbox est appelé développement, votre dossier partagé doit porter le même nom.

[Découvrez comment gérer les dossiers partagés](https://helpx.adobe.com/fr/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target="_blank"}.

## Vidéo pratique{#video}

Découvrez ce que sont les sandbox et comment faire la distinction entre les sandbox de développement et de production. Découvrez comment créer, réinitialiser et supprimer des sandbox.

>[!VIDEO](https://video.tv.adobe.com/v/334355?quality=12)
