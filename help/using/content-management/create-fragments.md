---
solution: Journey Optimizer
product: journey optimizer
title: Créer un fragment
description: Découvrez comment créer des fragments pour réutiliser du contenu dans des campagnes et des parcours Journey Optimizer.
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: da3ffe9c-a244-4246-b4b5-a3a1d0508676
source-git-commit: ffeaa49cde2871b28c85598469e62f4d9acbf060
workflow-type: tm+mt
source-wordcount: '709'
ht-degree: 33%

---

# Créer un fragment {#create-fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="Sélectionner le type Visuel"
>abstract="Créez un fragment visuel autonome pour rendre votre contenu réutilisable dans un e-mail au sein d’un parcours ou d’une campagne, ou dans un modèle de contenu."
>additional-url="https://experienceleague.adobe.com/en/docs/journey-optimizer/using/email/design-email/add-content/use-visual-fragments" text="Ajouter des fragments visuels à vos e-mails"

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="Sélectionner le type Expression"
>abstract="Créez un fragment d’expression autonome à partir de zéro pour rendre votre contenu réutilisable sur plusieurs parcours et campagnes. Lorsque vous utilisez l’éditeur de personnalisation, vous pouvez utiliser tous les fragments d’expression qui ont été créés dans le sandbox actuel."
>additional-url="https://experienceleague.adobe.com/docs/journey-optimizer/using/content-management/personalization/expression-editor/use-expression-fragments.html?lang=fr" text="Utiliser des fragments d’expression"

Les fragments peuvent être créés entièrement à partir du **[!UICONTROL Fragments]** menu de gauche. De plus, vous pouvez également enregistrer une partie du contenu existant en tant que fragment lorsque vous concevez du contenu. [Voici comment procéder.](#save-as-fragment)

Une fois enregistré, votre fragment peut être utilisé dans un parcours, une campagne ou un modèle. Vous pouvez utiliser ce fragment lors de la création de contenu dans des parcours et des campagnes. Voir [Ajouter des fragments visuels](../email/use-visual-fragments.md) et [Utiliser des fragments d’expression](../personalization/use-expression-fragments.md)

Pour créer un fragment, procédez comme suit.

## Définition des propriétés du fragment {#properties}

1. Accédez à la liste des fragments via le menu de gauche **[!UICONTROL Gestion de contenu]** > **[!UICONTROL Fragments]**.

1. Sélectionner **[!UICONTROL Créer un fragment]** et renseignez le nom et la description du fragment (si nécessaire).

   ![](assets/fragment-details.png)

1. Sélectionnez ou créez des balises Adobe Experience Platform à partir du champ **[!UICONTROL Balises]** pour classer votre fragment en vue d’une recherche améliorée. [Découvrez comment utiliser les balises unifiées](../start/search-filter-categorize.md#tags)

1. Sélectionnez le type de fragment : **Fragment visuel** ou **Fragment d’expression**. [En savoir plus sur les fragments visuels et d’expression](../content-management/fragments.md#visual-expression)

   >[!NOTE]
   >
   >Pour l’instant, des fragments visuels sont disponibles pour le **Email** canal uniquement.

1. Si vous créez un fragment d’expression, sélectionnez le type de code que vous souhaitez utiliser : **[!UICONTROL HTML]**, **[!UICONTROL JSON]** ou **[!UICONTROL Texte]**.

   ![](assets/fragment-expression-type.png)

1. Pour attribuer des libellés d’utilisation de données personnalisés ou de base au fragment, cliquez sur le bouton **[!UICONTROL Gérer l’accès]** dans la section supérieure de l’écran. [En savoir plus sur le contrôle d’accès au niveau de l’objet (OLAC)](../administration/object-based-access.md).

1. Cliquez sur **[!UICONTROL Créer]** pour concevoir le contenu de votre fragment.

## Concevoir le contenu du fragment {#content}

Une fois les propriétés du fragment configurées, le Designer d’email ou l’éditeur de personnalisation s’ouvre, selon le type de fragment que vous créez.

* Pour les fragments visuels, modifiez votre contenu selon les besoins, de la même manière que pour tout email contenu dans un parcours ou une campagne. [En savoir plus](../email/get-started-email-design.md)

  ![](assets/fragment-designer.png)

* Pour les fragments d’expression, utilisez l’éditeur de personnalisation de [!DNL Journey Optimizer] et toutes ses fonctionnalités de personnalisation et de création pour créer le contenu de votre fragment. [En savoir plus](../personalization/personalization-build-expressions.md)

  ![](assets/fragment-expression-editor.png)

Lorsque votre contenu est prêt, cliquez sur l’icône **Enregistrer** bouton . Le fragment est créé et ajouté à la liste de fragments avec l’événement **Version préliminaire** statut. Vous pouvez le prévisualiser et le publier pour le rendre disponible dans les parcours et les campagnes.

>[!NOTE]
>
>La publication de fragments est progressivement déployée au cours des jours qui suivent la publication de la version de juin de Journey Optimizer. Bien que certains utilisateurs disposent d’un accès immédiat, d’autres peuvent rencontrer un délai avant qu’il ne soit disponible dans leur environnement. Si cette amélioration n’est pas encore disponible dans votre environnement, notez que la publication de fragments n’est pas nécessaire pour utiliser des fragments dans vos parcours et campagnes.

## Prévisualiser et publier le fragment {#publish}

>[!NOTE]
>
>Pour publier un fragment, vous devez disposer de la variable **Fragment Publish** autorisation associée. [En savoir plus sur les autorisations](../administration/ootb-permissions.md)

Si votre fragment est prêt à être publié, vous pouvez le prévisualiser et le publier afin de le rendre disponible dans vos parcours et campagnes. Pour ce faire, procédez comme suit :

1. Revenez à l’écran de création de fragment après avoir conçu son contenu ou ouvrez-le depuis la liste des fragments.

1. Un aperçu du fragment est disponible sous le **Balises** , permettant de vérifier son rendu. Si vous devez apporter des modifications, cliquez sur le bouton **Modifier** dans la section supérieure de l&#39;écran pour ouvrir le Designer email ou l&#39;éditeur de personnalisation en fonction du type de fragment.

   ![](assets/fragment-preview.png)

1. Cliquez sur le bouton **Publish** dans le coin supérieur droit pour publier le fragment.

   Si le fragment est utilisé dans un parcours ou une campagne actif, un message s’ouvre pour vous informer. Cliquez sur le bouton **En savoir plus** lien pour accéder à la liste des parcours et/ou campagnes dans lesquels il est référencé. [Découvrez comment explorer les références d’un fragment](../content-management/manage-fragments.md#explore-references)

   Cliquez sur **Confirmer** pour publier le fragment et le mettre à jour dans les parcours/campagnes actifs qui l’utilisent.

   ![](assets/fragment-publish.png){width="70%" align="center"}

Le fragment est maintenant **En direct**, et devient disponible lors de la création de tout contenu dans le [!DNL Journey Optimizer] Designer d’email ou éditeur de personnalisation :

* [Découvrir comment utiliser des fragments visuels](../email/use-visual-fragments.md)
* [Découvrir comment utiliser des fragments d’expression](../personalization/use-expression-fragments.md)
