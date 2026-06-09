---
solution: Journey Optimizer
product: journey optimizer
title: Fragments personnalisables
description: Découvrez comment personnaliser des fragments en rendant certains de leurs champs modifiables.
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
exl-id: cd47ca1d-f707-4425-b865-14f3fbbe5fd1
TQID: https://experienceleague.adobe.com/cwg-nGPftYg6UgVSKXZPdW6DZr4-m5UM5Wqzfx3w028
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: dc22c819-3f29-4e91-8b7d-5c6719831141
  - id: fe338112-e2ce-4876-8989-fc4d497613f1
subfeature_v2:
  - id: c6e980f5-2d4f-494f-beef-186b9ecf1513
  - id: ee5bb250-0884-4d71-86eb-d8489e8bcadd
  - id: fb9a80eb-bebc-492f-a0e9-584595621ebb
role_v2:
  - id: b69b2659-1057-424e-8fc5-ed9e016dc554
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
  - id: e8ccd51f-da0d-4e3b-939b-e30d5ebb1ea5
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: a4e4f5ca5c3eb9dbfb5691cb5de420009ed7e5a5
workflow-type: tm+mt
source-wordcount: 1735
ht-degree: 86%

---

# Fragments personnalisables {#customizable-fragments}

Lorsque des fragments sont utilisés dans une action de campagne ou de parcours, ils sont verrouillés par défaut en raison de l’héritage. Cela signifie que toutes les modifications apportées à un fragment sont automatiquement propagées à tous les parcours et à toutes les campagnes où le fragment est utilisé.

Avec les **fragments personnalisables**, des champs spécifiques d’un fragment peuvent être définis comme modifiables lorsque le fragment est ajouté à une action de campagne ou de parcours. Supposons, par exemple, que vous ayez un fragment avec une bannière, du texte et un bouton. Vous pouvez désigner comme modifiables certains champs, tels que l’image ou l’URL cible du bouton. Cela permet aux utilisateurs et utilisatrices de modifier ces éléments lorsqu’ils incorporent le fragment dans leur campagne ou leur parcours, ce qui offre une expérience personnalisée sans affecter le fragment d’origine.

Grâce aux fragments personnalisables, il n’est plus nécessaire de rompre l’héritage des fragments, ce qui arrêtait auparavant la propagation des changements centralisés au niveau des fragments vers les campagnes et les parcours. Cette approche permet d’ajuster les portions de contenu au moment de l’utilisation, ce qui offre la possibilité de remplacer les valeurs par défaut par des détails spécifiques au contexte.

En exploitant des fragments personnalisables, vous pouvez gérer et personnaliser efficacement votre contenu sans créer de blocs de contenu entièrement nouveaux ni interrompre l’héritage du fragment d’origine. Cela garantit que les modifications apportées au niveau du fragment sont toujours propagées, tout en permettant une personnalisation nécessaire au niveau de la campagne ou du parcours.

Les fragments visuels et d’expression peuvent être marqués comme personnalisables. Pour obtenir des instructions détaillées sur la manière de procéder pour chaque type de fragment, reportez-vous aux sections ci-dessous.

![](../content-management/assets/do-not-localize/gif-fragments.gif)

## Ajouter des champs modifiables à des fragments visuels {#visual}

Pour rendre des parties d’un fragment visuel modifiables, procédez comme suit :

>[!NOTE]
>
>Des champs modifiables peuvent être ajoutés aux composants **image**, **texte** et **bouton**. Pour les composants **HTML**, les champs modifiables sont ajoutés à l’aide de l’éditeur de personnalisation, comme pour les fragments d’expression. [Découvrez comment ajouter un champ modifiable dans les composants HTML et les fragments d’expression.](#expression)

1. Ouvrez l’écran d’édition du contenu du fragment.

1. Sélectionnez le composant de votre fragment dans lequel vous souhaitez configurer des champs modifiables.

1. Le volet des propriétés du composant s’ouvre sur le côté droit. Sélectionnez l’onglet **Champs modifiables**, puis activez l’option **Activer l’édition**.

1. Tous les champs pouvant être modifiés pour le composant sélectionné sont répertoriés dans le volet. Les champs disponibles pour la modification dépendent du type de composant sélectionné.

   Dans l’exemple ci-dessous, nous autorisons la modification de l’URL du bouton « Cliquez ici ».

   ![](assets/fragment-param-enable.png)

1. Cliquez sur la **Vue d’ensemble** pour vérifier tous les champs modifiables et leurs valeurs par défaut.

   Dans cet exemple, le champ URL du bouton s’affiche avec la valeur par défaut définie dans le composant. Cette valeur sera personnalisable par les utilisateurs et utilisatrices après l’ajout du fragment à leur contenu.

   ![](assets/fragment-param-preview.png)

1. Une fois que tout est prêt, enregistrez vos modifications pour mettre à jour le fragment.

1. Après avoir ajouté le fragment dans un e-mail, les utilisateurs et utilisatrices peuvent personnaliser tous les champs modifiables configurés dans le fragment. [Découvrir comment personnaliser des champs modifiables dans un fragment visuel](../email/use-visual-fragments.md#customize-fields)

>[!CAUTION]
>
>Lorsque les **libellé** et **URL** d’un composant de bouton sont rendus modifiables dans un fragment, les rapports de suivi affichent l’URL au lieu du libellé du bouton. [En savoir plus sur le tracking](../email/message-tracking.md)

## Ajouter des champs modifiables dans les composants HTML et les fragments d’expression {#expression}

Pour rendre modifiables des parties d’un composant HTML ou d’un fragment d’expression, vous devez utiliser une syntaxe spécifique dans l’éditeur d’expression. Cela implique de déclarer une **variable** avec une valeur par défaut que les utilisateurs et utilisatrices peuvent remplacer après l’ajout du fragment à leur contenu.

Supposons, par exemple, que vous souhaitiez créer un fragment à ajouter à vos e-mails et permettre aux utilisateurs et utilisatrices de personnaliser une couleur spécifique utilisée à différents emplacements, tels que les cadres ou les couleurs d’arrière-plan des boutons. Lors de la création de votre fragment, vous devez déclarer une variable avec un **ID unique**, par exemple « couleur », puis l’appeler aux emplacements souhaités dans le contenu du fragment où vous souhaitez appliquer cette couleur. Lors de l’ajout du fragment à leur contenu, les utilisateurs et utilisatrices peuvent personnaliser la couleur utilisée partout où la variable est référencée.

Pour les composants HTML, seuls des éléments spécifiques peuvent devenir des champs modifiables. Pour plus d’informations, développez la section ci-dessous.

+++Éléments modifiables dans les composants HTML :

Les éléments ci-dessous peuvent devenir des champs modifiables dans un composant HTML :

* Partie de texte
* URL complète pour un lien ou une image (ne fonctionne pas avec une partie d’une URL)
* Propriété CSS entière (ne fonctionne pas avec une propriété partielle)

Par exemple, dans le code ci-dessous, chaque élément surligné en rouge peut devenir une propriété :

![](assets/fragment-html.png){width="70%"}

+++

Pour déclarer une variable et l’utiliser dans votre fragment, procédez comme suit :

1. Ouvrez votre fragment d’expression, puis modifiez son contenu dans l’éditeur de personnalisation.

   ![](assets/fragment-html-edit.png)

   Pour les composants HTML, sélectionnez le composant dans le fragment et cliquez sur le bouton **Afficher le code source**.

1. Déclarez la variable que vous souhaitez que les utilisateurs et utilisatrices modifient. Accédez au menu **Fonctions d’assistance** dans le volet de navigation de gauche, puis ajoutez la fonction **en ligne**. La syntaxe pour déclarer et appeler la variable est automatiquement ajoutée à votre contenu.

   ![](assets/fragment-add-helper.png)

1. Remplacez `"name"` par un ID unique pour identifier le champ modifiable.

   >[!NOTE]
   >
   >L’ID de champ doit être unique et ne doit pas comporter d’espaces. Cet ID doit être utilisé partout dans le contenu où vous souhaitez afficher la valeur de la variable.

1. Adaptez la syntaxe à vos besoins en ajoutant les paramètres présentés dans le tableau ci-dessous :

   | Action | Paramètre | Exemple |
   | ------- | ------- | ------- |
   | Déclarez un champ modifiable avec une **valeur par défaut**. Lorsque vous ajoutez le fragment à votre contenu, cette valeur par défaut est utilisée si vous ne la personnalisez pas. | Ajoutez la valeur par défaut entre les balises intégrées. | `{{#inline "editableFieldID"}}default_value{{/inline}}` |
   | Définissez un **libellé** pour le champ modifiable. Ce libellé s’affiche dans le concepteur d’e-mail lors de l’édition des champs du fragment. | `name="title"` | `{{#inline "editableFieldID" name="title"}}default_value{{/inline}}` |
   | Déclarez un champ modifiable contenant une **source d’image** qui doit être publiée. | `assetType="image"` | `{{#inline "editableFieldID" assetType="image"}}default_value{{/inline}}` |
   | Déclarez un champ modifiable contenant une **URL** qui doit faire l’objet d’un suivi.<br/>Notez que les blocs prédéfinis « URL de page miroir » et « Lien de désabonnement » prêts à l’emploi ne peuvent pas devenir des champs modifiables. | `assetType="url"` | `{{#inline "editableFieldID" assetType="url"}}default_value{{/inline}}` |

1. Utilisez la syntaxe `{{{name}}}` dans votre code à tous les endroits où vous souhaitez afficher la valeur du champ modifiable. Remplacez `name` par l’ID unique du champ défini précédemment.

   ![](assets/fragment-call-variable.png)

1. Enregistrez et publiez votre fragment.

Lors de l’ajout du fragment à leur contenu d’e-mail, les utilisateurs et utilisatrices peuvent désormais remplacer les valeurs par défaut des variables par les valeurs de leur choix :

* Pour les fragments d’expression, une syntaxe spécifique est utilisée pour remplacer les valeurs des variables. [Découvrir comment personnaliser des champs modifiables dans un fragment d’expression](../personalization/use-expression-fragments.md#customize-fields)

* Pour les composants HTML, la variable s’affiche dans la liste des champs modifiables du concepteur d’e-mail. [Découvrir comment personnaliser des champs modifiables dans un fragment visuel](../email/use-visual-fragments.md#customize-fields)

### Exemple : fragment d’expression personnalisable {#example}

Dans l’exemple ci-dessous, nous allons créer un fragment d’expression présentant de nouvelles collections sportives. Par défaut, le fragment affiche le contenu suivant : *Vous en voulez plus ? Ne manquez pas notre dernière collection sports !*

Nous voulons permettre aux utilisateurs et utilisatrices de remplacer « sports » dans ce contenu par le sport de leur choix. Par exemple : *Vous en voulez plus ? Ne manquez pas notre dernière collection yoga !*

Pour ce faire, procédez comme suit :

1. Déclarez une variable « sports » avec l’ID « sports ».

   Par défaut, si les utilisateurs et les utilisatrices ne modifient pas la valeur de la variable après avoir ajouté le fragment dans leur contenu, la valeur définie entre les balises `{{#inline}}` et `{{/inline}}` s’affiche, soit « sports ».

1. Ajoutez la syntaxe ``{{{sport}}}`` dans le contenu du fragment où vous souhaitez afficher la valeur de la variable, c’est-à-dire « sports » par défaut, ou la valeur choisie par les utilisateurs et utilisatrices.

   ![](assets/fragment-expression-custom.png)

1. Lors de l’ajout du fragment d’expression à leur contenu, les utilisateurs et utilisatrices peuvent remplacer la valeur de la variable par la valeur de leur choix directement dans l’éditeur d’expression. [Découvrir comment personnaliser des champs modifiables dans un fragment d’expression](../personalization/use-expression-fragments.md#customize-fields)

   ![](assets/fragment-expression-use.png)

## Ajouter du texte enrichi à un fragment personnalisable {#rich-text}

>[!CONTEXTUALHELP]
>id="ajo_editable_fragment_compatibility"
>title="Fragment hérité"
>abstract="Les champs modifiables de ce fragment sont en mode texte uniquement. Cela signifie que vous ne pouvez saisir que du texte brut lorsque vous modifiez ce fragment dans des e-mails. Le texte enrichi tel que le gras, l’italique, les liens hypertexte et les sauts de ligne n’est pas pris en charge. Cliquez sur <b>Basculer en mode HTML</b> pour activer le texte enrichi dans les champs modifiables lors de l’utilisation du fragment dans un e-mail."

>[!CONTEXTUALHELP]
>id="ajo_editable_field_compatibility"
>title="Fragment hérité"
>abstract="Ce champ modifiable est en mode texte uniquement. La mise en forme de texte enrichi (gras, italique, liens hypertexte, sauts de ligne, etc.) n’est pas disponible tant que le fragment n’a pas été mis à niveau vers le mode compatible avec HTML. Accédez aux paramètres du corps du fragment et cliquez sur <b>Basculer en mode HTML</b> pour activer la modification de texte enrichi."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/channels/email/design-email/add-content/use-visual-fragments#customize-fields" text="Personnaliser des champs modifiables dans un fragment"

>[!CONTEXTUALHELP]
>id="ac_editable_fragment_compatibility"
>title="Fragment hérité"
>abstract="Les champs modifiables de ce fragment sont en mode texte uniquement. La mise en forme de texte enrichi (gras, italique, liens hypertexte, sauts de ligne, etc.) n’est pas disponible tant que le fragment n’a pas été mis à niveau vers le mode compatible avec HTML. Pour ce faire, ouvrez l’éditeur de fragments et cliquez sur <b>Basculer en mode HTML</b>."
>additional-url="https://experienceleague.adobe.com/fr/docs/journey-optimizer/using/channels/email/design-email/add-content/use-visual-fragments#customize-fields" text="Personnaliser des champs modifiables dans un fragment"

Le texte enrichi tel que les sauts de ligne, le gras, l’italique, etc. peut être ajouté à un fragment personnalisable à l’aide des composants HTML. Pour ce faire, procédez comme suit.
<!--
➡️ [Learn how to add and use rich text in a customizable fragment in this video](#video)
-->

### Créer un fragment contenant du texte enrichi {#add-rich-text}

1. Créez un [fragment](create-fragments.md) visuel et commencez à ajouter des composants.

1. Ajoutez un [composant HTML](../email/content-components.md#HTML) et ouvrez l’éditeur HTML.

1. Accédez au menu **[!UICONTROL Fonctions d’assistance]** dans le volet de navigation de gauche, puis ajoutez la fonction **inline**.

1. Remplacez `"name"` par l’identifiant à utiliser pour votre contenu modifiable, par exemple &quot;EditableContent&quot;.

1. Remplacez `render_content` par le code HTML correspondant au contenu enrichi par défaut de votre choix. Vous pouvez ajouter un attribut gras ou italique, des sauts de ligne, des listes à puces, etc.

   ![](assets/fragment-rich-editable-content.png)

1. Dans le même composant HTML, ajoutez une autre fonction d’assistance **inline** pour vos éléments de style.

1. Remplacez `"name"` et `render_content` par l’identifiant et le code HTML correspondant au style par défaut de votre choix.

   ![](assets/fragment-rich-editable-styling.png)

1. Enregistrez votre contenu. Les champs modifiables sélectionnés s’affichent sur le côté droit.

   ![](assets/fragment-rich-editable-fields.png)

1. Enregistrez et [publiez](create-fragments.md#publish) le fragment.

### Utiliser du texte enrichi dans des fragments personnalisables {#use-rich-text}

Lors de l’ajout du fragment à votre e-mail, vous pouvez désormais modifier le contenu et le style de texte enrichi que vous avez créés. En tant que spécialiste marketing, procédez comme suit.

1. [Créez un e-mail](../email/create-email.md) dans une campagne ou un parcours, puis ajoutez le fragment avec le texte enrichi qui a été [créé](#add-rich-text).

   Vous pouvez voir les deux champs modifiables qui ont été créés sur le côté droit.

   ![](assets/fragment-use-rich-editable-fields.png)

1. Utilisez l’une ou l’autre des méthodes de simulation pour voir le rendu du contenu modifiable et du style : cliquez sur **[!UICONTROL Simuler du contenu]** pour tester les variations de contenu avec des exemples de données d’entrée ou la génération automatique de l’IA, ou cliquez sur **[!UICONTROL Simuler du contenu]**, puis sélectionnez **[!UICONTROL Simuler du contenu (profils AEP)]** dans la liste déroulante pour afficher l’aperçu avec les profils de test. [En savoir plus sur la prévisualisation de contenu](preview-test.md)

1. Sélectionnez l’icône **[!UICONTROL Ajouter une personnalisation]** à côté de l’un des champs modifiables.

1. Dans l’éditeur de personnalisation qui s’ouvre, mettez à jour le <!--CSS-->style et/ou le contenu selon vos besoins en ajoutant ou en supprimant des éléments du champ modifiable.

   ![](assets/fragment-rich-editable-fields-update-styling.png)

<!--
## How-to video {#video}

This video shows how to make HTML components within a fragment editable, allowing for dynamic updates to both content and styling.

>[!VIDEO](https://video.tv.adobe.com/v/3464363/?learn=on&#x26;enablevpops)
-->