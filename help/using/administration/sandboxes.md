---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser et attribuer des sandbox
description: Découvrir comment gérer les sandbox
feature: Sandboxes
topic: Administration
role: Admin, Architect, Developer
level: Experienced
keywords: sandbox, virtuels, environnements, organisation, platform
exl-id: 14f80d5d-0840-4b79-9922-6d557a7e1247
source-git-commit: 8093af8c3e7484f9ebed8dbc50065bcff0459581
workflow-type: tm+mt
source-wordcount: '321'
ht-degree: 52%

---

# Utiliser et attribuer des sandbox {#sandboxes}

## Utiliser des sandbox {#using-sandbox}

[!DNL Journey Optimizer] vous permet de partitionner votre instance en environnements virtuels distincts appelés sandbox. Les sandbox sont affectées par le biais de rôles dans les autorisations. [Découvrez comment affecter des sandbox](permissions.md#create-product-profile).

[!DNL Journey Optimizer] reflète les sandbox Adobe Experience Platform créés pour une organisation donnée. Vous pouvez créer ou réinitialiser des sandbox Adobe Experience Platform à partir de votre instance Adobe Experience Platform. [Pour en savoir plus, consultez le guide d’utilisation des sandbox](https://experienceleague.adobe.com/docs/experience-platform/sandbox/ui/user-guide.html?lang=fr){target="_blank"}.

Le sélecteur de sandbox se trouve dans le coin supérieur droit de l’écran, en regard du nom de votre organisation. Pour passer d’un sandbox à un autre, cliquez sur le sandbox actif dans le sélecteur et sélectionnez-en un autre dans la liste déroulante.

![](assets/sandbox_5.png)

➡️ [En savoir plus sur les sandbox dans cette vidéo](#video)

## Affectation de sandbox {#assign-sandboxes}

>[!IMPORTANT]
>
> La gestion des sandbox peut uniquement être effectuée par un administrateur **[!UICONTROL Produit]** ou **[!UICONTROL Système]**.

Vous pouvez choisir d’affecter différentes sandbox aux **[!UICONTROL Rôles]** prêts à l’emploi ou personnalisés.

Pour affecter des sandbox :

1. Dans [!DNL Permissions], dans l’onglet **[!UICONTROL Rôles]**, sélectionnez un **[!UICONTROL Rôle]**.

   ![](assets/sandbox_1.png)

1. Cliquez sur **[!UICONTROL Modifier]**.

1. Dans le menu déroulant des ressources **[!UICONTROL Sandbox]**, sélectionnez la sandbox qui sera affectée à votre rôle.

   ![](assets/sandbox_3.png)

1. Si nécessaire, cliquez sur l’icône X en regard de Supprimer l’accès des sandbox à votre **[!UICONTROL Rôle]**.

   ![](assets/sandbox_4.png)

1. Cliquez sur **[!UICONTROL Enregistrer]**.

## Accès au contenu {#content-access}

Pour configurer l’accessibilité du contenu, affectez un dossier de contenu partagé à chacun de vos sandbox. Vous pouvez créer et configurer des dossiers partagés dans l’onglet **[!UICONTROL Stockage]** affiché dans le [!DNL Admin Console] pour les administrateurs. Si vous avez accès au [!DNL Admin Console] en tant qu’administrateur système, vous pouvez créer des dossiers partagés et ajouter des délégués ayant différents niveaux d’accès à ces dossiers.

![](assets/do-not-localize/content_access.png)

Notez que pour que votre contenu soit synchronisé avec le sandbox correct, vous devez suivre la même syntaxe que ce dernier. Par exemple, si votre sandbox est appelé « développement », votre dossier partagé doit porter le même nom.

[Découvrez comment gérer les dossiers partagés](https://helpx.adobe.com/fr/enterprise/admin-guide.html/enterprise/using/manage-adobe-storage.ug.html){target="_blank"} .

## Vidéo pratique{#video}

Découvrez ce que sont les sandbox et comment faire la distinction entre les sandbox de développement et de production. Découvrez comment créer, réinitialiser et supprimer des sandbox.

>[!VIDEO](https://video.tv.adobe.com/v/334355?quality=12)