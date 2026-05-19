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
TQID: https://experienceleague.adobe.com/NlC-JLidAL9r-1-8rX4hX-WxCkr-Nv1e6YKSisx1n28
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: a653cc2e-bc85-4353-a306-399e5b247978
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: c6e980f5-2d4f-494f-beef-186b9ecf1513
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: f8d2e9f0-69c9-40cd-890f-71336c8dfff7
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f9b8e1590f14cdcd00432295c653769f753b9b40
workflow-type: tm+mt
source-wordcount: 832
ht-degree: 94%

---

# Créer un fragment {#create-fragments}

>[!CONTEXTUALHELP]
>id="ajo_create_visual_fragment"
>title="Sélectionner le type Visuel"
>abstract="Créez un fragment visuel autonome pour rendre votre contenu réutilisable dans un e-mail au sein d’un parcours ou d’une campagne, ou dans un modèle de contenu."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/channels/email/design-email/add-content/use-visual-fragments" text="Ajouter des fragments visuels à vos e-mails"

>[!CONTEXTUALHELP]
>id="ajo_create_expression_fragment"
>title="Sélectionner le type Expression"
>abstract="Créez un fragment d’expression autonome à partir de zéro pour rendre votre contenu réutilisable sur plusieurs parcours et campagnes. Lorsque vous utilisez l’éditeur de personnalisation, vous pouvez utiliser tous les fragments d’expression qui ont été créés dans le sandbox actuel."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/content-management/personalization/personalization-build-expressions" text="Utiliser l’éditeur de personnalisation"

Les fragments peuvent être créés entièrement à partir du menu de gauche **[!UICONTROL Fragments]**. De plus, vous pouvez également enregistrer une partie du contenu existant en tant que fragment lorsque vous concevez du contenu. [Voici comment procéder](save-fragments.md#)

Une fois enregistré, votre fragment peut être utilisé dans un parcours, une campagne ou un modèle. Vous pouvez utiliser ce fragment pour créer du contenu dans le cadre des parcours et des campagnes. Voir [Ajouter des fragments visuels](../email/use-visual-fragments.md) et [Utiliser des fragments d’expression](../personalization/use-expression-fragments.md).

Pour créer un fragment, suivez les étapes présentées ci-dessous.

## Définir les propriétés du fragment {#properties}

1. Accédez à la liste des fragments via le menu de gauche **[!UICONTROL Gestion de contenu]** > **[!UICONTROL Fragments]**.

1. Sélectionnez **[!UICONTROL Créer un fragment]** et renseignez le nom et la description du fragment (si nécessaire).

   ![](assets/fragment-details.png)

1. Sélectionnez ou créez des balises Adobe Experience Platform à partir du champ **[!UICONTROL Balises]** pour classer votre fragment en vue d’une recherche améliorée. [Découvrir comment utiliser les balises unifiées](../start/search-filter-categorize.md#tags)

1. Sélectionnez le type de fragment : **Fragment visuel** ou **Fragment d’expression**. [En savoir plus](../content-management/fragments.md#visual-expression)

   >[!NOTE]
   >
   >Pour l’instant, les fragments visuels ne sont disponibles que pour le canal **E-mail**.

1. Si vous créez un fragment d’expression, sélectionnez le type de code que vous souhaitez utiliser : **[!UICONTROL HTML]**, **[!UICONTROL JSON]** ou **[!UICONTROL Texte]**.

   ![](assets/fragment-expression-type.png)

1. Pour attribuer des libellés d’utilisation des données personnalisés ou de base au fragment, cliquez sur le bouton **[!UICONTROL Gérer l’accès]** dans la partie supérieure de l’écran. [En savoir plus sur le contrôle d’accès au niveau de l’objet (OLAC)](../administration/object-based-access.md)

1. Cliquez sur le bouton **[!UICONTROL Créer]** pour concevoir le contenu de votre fragment.

## Concevoir le contenu du fragment {#content}

Après avoir configuré les propriétés du fragment, le concepteur d’e-mail ou l’éditeur de personnalisation s’ouvre, selon le type de fragment que vous créez.

>[!NOTE]
>
>Les [attributs contextuels](../personalization/personalization-build-expressions.md) ne sont pas pris en charge dans les fragments.
>
>Lorsque le suivi est activé dans un parcours ou une campagne, si vous ajoutez des liens à un fragment et que ce fragment est utilisé dans un message, ces liens font l’objet d’un suivi comme tous les autres liens inclus dans le message. [En savoir plus sur les liens et le suivi](../email/message-tracking.md)

* Pour les fragments visuels, modifiez votre contenu selon vos besoins, de la même manière que pour tout e-mail se trouvant dans un parcours ou une campagne. [En savoir plus](../email/get-started-email-design.md)

  ![](assets/fragment-designer.png)

  Pour appliquer rapidement un style spécifique adapté à votre marque et à votre conception, vous pouvez appliquer un [thème](../email/apply-email-themes.md) à votre fragment.

  ![](assets/fragment-themes.png)

  >[!CAUTION]
  >
  >Les fragments ne sont pas compatibles entre les modes Utiliser des thèmes et Style manuel. Lors de l’utilisation d’un fragment dans le contenu d’un e-mail, veillez à appliquer un thème que vous avez défini pour ce fragment. [En savoir plus](../email/apply-email-themes.md#leverage-themes-fragment)

* Pour les fragments d’expression, utilisez l’éditeur de personnalisation de [!DNL Journey Optimizer] et toutes ses fonctionnalités de personnalisation et de création pour créer le contenu de votre fragment. [En savoir plus](../personalization/personalization-build-expressions.md)

  ![](assets/fragment-expression-editor.png)

  >[!NOTE]
  >
  >Les fragments d’expression de type JSON sont validés syntaxiquement lors de l’enregistrement, les erreurs s’affichant sous forme d’alertes d’avertissement.

Lorsque votre contenu est prêt, cliquez sur le bouton **[!UICONTROL Enregistrer]**.

>[!NOTE]
>
>Les fragments visuels ne doivent pas dépasser 100 Ko. Les fragments d’expression ne doivent pas dépasser 200 Ko.

Le fragment est créé et ajouté à la liste de fragments avec le statut **[!UICONTROL Brouillon]**. Vous pouvez le prévisualiser et le publier pour le rendre disponible dans les parcours et les campagnes.

## Prévisualiser et publier le fragment {#publish}

>[!NOTE]
>
>Pour publier un fragment, vous devez disposer de l’autorisation utilisateur [Publier le fragment](../administration/ootb-product-profiles.md#content-library-manager).

Si votre fragment est prêt à être publié, vous pouvez le prévisualiser et le publier afin de le rendre disponible dans vos parcours et campagnes. Pour ce faire, procédez comme suit.

1. Revenez à l’écran de création de fragment après avoir conçu son contenu ou ouvrez-le depuis la liste des fragments.

1. Une prévisualisation du fragment est disponible sous le champ **[!UICONTROL Balises]**, permettant de vérifier son rendu. Si vous devez apporter des modifications, cliquez sur le bouton **[!UICONTROL Modifier]** dans la section supérieure de l’écran pour ouvrir le concepteur d’e-mail ou l’éditeur de personnalisation en fonction du type de fragment. [En savoir plus](manage-fragments.md#edit-fragments)

   ![](assets/fragment-preview.png)

1. Cliquez sur le bouton **[!UICONTROL Publier]** dans le coin supérieur droit pour publier le fragment.

1. Si le fragment est utilisé dans un parcours actif ou une campagne active, un message s’ouvre pour vous en informer. Cliquez sur le lien **[!UICONTROL En savoir plus]** pour accéder à la liste des parcours et/ou campagnes dans lesquels il est référencé. [Découvrir comment explorer les références d’un fragment](../content-management/manage-fragments.md#explore-references)

   ![](assets/fragment-publish.png){width="70%" align="center"}

   Cliquez sur **[!UICONTROL Confirmer]** pour publier le fragment et le mettre à jour dans les parcours actifs/campagnes actives qui l’utilisent.

Le fragment est maintenant **[!UICONTROL Actif]** et devient disponible lors de la création de tout contenu dans le concepteur d’e-mail ou l’éditeur de personnalisation de [!DNL Journey Optimizer] :

* [Découvrir comment utiliser des fragments visuels](../email/use-visual-fragments.md)
* [Découvrir comment utiliser des fragments d’expression](../personalization/use-expression-fragments.md)

>[!CAUTION]
>
>Une fois publié, vous ne pouvez pas ajouter de nouveaux attributs personnalisés à un fragment dynamique. Si vous souhaitez ajouter des attributs de personnalisation, vous devez dupliquer le fragment. [En savoir plus](manage-fragments.md#adding-new-attributes)