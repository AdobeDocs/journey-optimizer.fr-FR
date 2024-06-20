---
solution: Journey Optimizer
product: journey optimizer
title: Fragments personnalisables
description: Découvrez comment personnaliser des fragments en rendant certains de leurs champs modifiables.
feature: Fragments
topic: Content Management
role: User
level: Beginner, Intermediate
source-git-commit: ca743774017e8f6cf5f385119d9c71de6020bb19
workflow-type: tm+mt
source-wordcount: '1185'
ht-degree: 0%

---


# Fragments personnalisables {#customizable-fragments}

Lorsque des fragments sont utilisés dans une opération ou une action de parcours, ils sont verrouillés par défaut en raison de l’héritage. Cela signifie que toutes les modifications apportées à un fragment sont automatiquement propagées à tous les parcours et campagnes où le fragment est utilisé. Avec les fragments personnalisables, des champs spécifiques d’un fragment peuvent être définis comme modifiables lorsque le fragment est ajouté à une opération ou à une action de parcours. Supposons, par exemple, que vous ayez un fragment avec une bannière, du texte et un bouton. Vous pouvez désigner comme modifiable certains champs, tels que l’image ou l’URL cible du bouton. Cela permet aux utilisateurs de modifier ces éléments lorsqu’ils incorporent le fragment dans leur campagne ou leur parcours, ce qui leur offre une expérience personnalisée sans affecter le fragment d’origine.

Les fragments personnalisables éliminent la nécessité de rompre l’héritage des fragments, ce qui empêchait auparavant la propagation des modifications centralisées au niveau des fragments vers les campagnes et les parcours. Cette approche permet d’ajuster les portions de contenu au moment de l’utilisation, ce qui offre la possibilité de remplacer les valeurs par défaut par des détails spécifiques au contexte.

En exploitant des fragments personnalisables, vous pouvez gérer et personnaliser efficacement votre contenu sans créer de blocs de contenu entièrement nouveaux ni interrompre l’héritage du fragment d’origine. Cela garantit que les modifications apportées au niveau du fragment sont toujours propagées, tout en permettant une personnalisation nécessaire au niveau de la campagne ou du parcours.

Les fragments visuels et d’expression peuvent être marqués comme personnalisables. Pour obtenir des instructions détaillées sur la manière de procéder pour chaque type de fragment, reportez-vous aux sections ci-dessous.

![](../content-management/assets/do-not-localize/gif-fragments.gif)

## Ajout de champs modifiables à des fragments visuels {#visual}

Pour rendre des parties d’un fragment visuel modifiables, procédez comme suit :

>[!NOTE]
>
>Des champs modifiables peuvent être ajoutés à **image**, **text** et **button** composants. Pour **HTML** composants, les champs modifiables sont ajoutés à l’aide de l’éditeur de personnalisation, comme pour les fragments d’expression. [Découvrez comment ajouter un champ modifiable dans les composants de HTML et les fragments d’expression](#expression)

1. Ouvrez l’écran d’édition du contenu du fragment.

1. Sélectionnez le composant de votre fragment dans lequel vous souhaitez configurer des champs modifiables.

1. Le volet des propriétés du composant s’ouvre sur le côté droit. Sélectionnez la variable **Champs modifiables** puis activez l’option **Activer l’édition** .

1. Tous les champs pouvant être modifiés pour le composant sélectionné sont répertoriés dans le volet. Les champs disponibles pour la modification dépendent du type de composant sélectionné.

   Dans l&#39;exemple ci-dessous, nous autorisons l&#39;édition de l&#39;URL du bouton &quot;Cliquez ici&quot;.

   ![](assets/fragment-param-enable.png)

1. Cliquez sur le bouton **Présentation** pour vérifier tous les champs modifiables et leurs valeurs par défaut.

   Dans cet exemple, le champ URL du bouton s’affiche avec la valeur par défaut définie dans le composant. Cette valeur sera personnalisable par les utilisateurs après avoir ajouté le fragment à leur contenu.

   ![](assets/fragment-param-preview.png)

1. Une fois prêt, enregistrez vos modifications pour mettre à jour le fragment.

1. Après avoir ajouté le fragment dans un email, les utilisateurs pourront personnaliser tous les champs modifiables configurés dans le fragment. [Découvrez comment personnaliser des champs modifiables dans un fragment visuel](../email/use-visual-fragments.md#customize-fields)

## Ajout de champs modifiables dans les composants de HTML et les fragments d’expression {#expression}

Pour rendre modifiables des parties d’un composant de HTML ou d’un fragment d’expression, vous devez utiliser une syntaxe spécifique dans l’éditeur d’expression. Cela implique de déclarer une **variable** avec une valeur par défaut que les utilisateurs peuvent remplacer après l’ajout du fragment à leur contenu.

Supposons, par exemple, que vous souhaitiez créer un fragment à ajouter à vos emails et permettre aux utilisateurs de personnaliser une couleur spécifique utilisée à différents emplacements, tels que les cadres ou les couleurs d’arrière-plan des boutons. Lors de la création de votre fragment, vous devez déclarer une variable avec une **ID unique**, par exemple &quot;color&quot;, et appelez-le aux emplacements souhaités dans le contenu du fragment où vous souhaitez appliquer cette couleur. Lors de l’ajout du fragment à leur contenu, les utilisateurs pourront personnaliser la couleur utilisée partout où la variable est référencée.

Pour les composants de HTML, seuls des éléments spécifiques peuvent devenir des champs modifiables. Pour plus d’informations, développez la section ci-dessous.

+++Éléments modifiables dans les composants de HTML :

Les éléments ci-dessous peuvent devenir des champs modifiables dans un composant de HTML :

* Une partie de texte
* Une URL complète pour le lien ou l’image (ne fonctionne pas avec une partie de l’URL)
* Propriété CSS entière (ne fonctionne pas avec la propriété partielle)

Par exemple, dans le code ci-dessous, chaque élément surligné en rouge peut devenir une propriété :

![](assets/fragment-html.png){width=&quot;70%}

+++

Pour déclarer une variable et l’utiliser dans votre fragment, procédez comme suit :

1. Ouvrez votre fragment d’expression, puis modifiez son contenu dans l’éditeur de personnalisation. Pour les composants de HTML, sélectionnez le composant dans le fragment et cliquez sur le bouton **Afficher le code source** bouton .

   ![](assets/fragment-html-edit.png)

1. Déclarez la variable que vous souhaitez que les utilisateurs modifient. Accédez au **Fonctions d’assistance** dans le volet de navigation de gauche et ajoutez le **inline** fonction d’assistance. La syntaxe à déclarer et à appeler la variable est automatiquement ajoutée à votre contenu.

   ![](assets/fragment-add-helper.png)

1. Remplacer `"name"` avec un identifiant unique pour identifier le champ modifiable.

   >[!NOTE]
   >
   >L’identifiant de champ doit être unique et ne doit pas comporter d’espaces. Cet identifiant doit être utilisé partout dans le contenu où vous souhaitez afficher la valeur de la variable.

1. Adaptez la syntaxe à vos besoins en ajoutant les paramètres présentés dans le tableau ci-dessous :

   | Action | Paramètre | Exemple |
   | ------- | ------- | ------- |
   | Déclarez un champ modifiable avec un **valeur par défaut**. Lorsque vous ajoutez le fragment à votre contenu, cette valeur par défaut est utilisée si vous ne le personnalisez pas. | Ajoutez la valeur par défaut entre les balises intégrées. | `{{#inline "editableFieldID"}}default_value{{/inline}}` |
   | Définition d’une **label** pour le champ modifiable. Ce libellé s’affiche dans le Designer email lors de l’édition des champs du fragment. | `name="title"` | `{{#inline "editableFieldID" name="title"}}default_value{{/inline}}` |
   | Déclarez un champ modifiable contenant une **Source de l’image** qui doit être publié. | `assetType="image"` | `{{#inline "editableFieldID" assetType="image"}}default_value{{/inline}}` |
   | Déclarez un champ modifiable contenant une **URL** qui doit faire l&#39;objet d&#39;un suivi.<br/>Notez que les blocs prédéfinis &quot;URL de page miroir&quot; et &quot;Lien de désabonnement&quot; prêts à l’emploi ne peuvent pas devenir des champs modifiables. | `assetType="url"` | `{{#inline "editableFieldID" assetType="url"}}default_value{{/inline}}` |

1. Utilisez la variable `{{{name}}}` dans votre code à tous les endroits où vous souhaitez afficher la valeur du champ modifiable. Remplacer `name` avec l’identifiant unique du champ défini précédemment.

   ![](assets/fragment-call-variable.png)

1. Enregistrez votre fragment.

Lors de l’ajout du fragment à leur contenu d’email, les utilisateurs peuvent désormais remplacer les valeurs par défaut des variables par les valeurs de leur choix :

* Pour les fragments d’expression, une syntaxe spécifique est utilisée pour remplacer les valeurs de variables. [Découvrez comment personnaliser des champs modifiables dans un fragment d’expression](../personalization/use-expression-fragments.md#customize-fields)

* Pour les composants de HTML, la variable s’affiche dans la liste des champs modifiables du Designer de messagerie. [Découvrez comment personnaliser des champs modifiables dans un fragment visuel](../email/use-visual-fragments.md#customize-fields)

## Exemple de fragment d’expression modifiable {#example}

Dans l’exemple ci-dessous, nous allons créer un fragment d’expression présentant de nouvelles collections sportives. Par défaut, le fragment affiche le contenu suivant : *Vous cherchez plus ? Ne manquez pas notre dernière collection de sports !*

Nous voulons permettre aux utilisateurs de remplacer &quot;sports&quot; dans ce contenu par le sport de leur choix. Par exemple : *Vous cherchez plus ? Ne manquez pas notre dernière collection de yoga !*

Pour ce faire :

1. Déclarez une variable &quot;sport&quot; avec l’identifiant &quot;sport&quot;.

   Par défaut, si les utilisateurs ne modifient pas la valeur de la variable après l’ajout du fragment dans leur contenu, la valeur définie entre la variable `{{#inline}}` et `{{/inline}}` balises, soit &quot;sports&quot;.

1. Ajoutez la variable ``{{{sport}}}`` dans le contenu du fragment où vous souhaitez afficher la valeur de la variable, c’est-à-dire &quot;sports&quot; par défaut, ou la valeur choisie par les utilisateurs.

   ![](assets/fragment-expression-custom.png)

1. Lors de l’ajout du fragment d’expression à leur contenu, les utilisateurs peuvent modifier la valeur de la variable avec leur choix directement dans l’éditeur d’expression. [Découvrez comment personnaliser des champs modifiables dans un fragment d’expression](../personalization/use-expression-fragments.md#customize-fields)

   ![](assets/fragment-expression-use.png)
