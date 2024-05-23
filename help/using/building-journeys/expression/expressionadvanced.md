---
solution: Journey Optimizer
product: journey optimizer
title: À propos de l’éditeur d’expression avancé
description: Découvrez comment créer des expressions avancées
feature: Journeys
role: Data Engineer, Architect
level: Experienced
keywords: éditeur d’expression, données, parcours
exl-id: 9ea6cc3a-6a1b-4e8f-82ff-f8b1812617d7
source-git-commit: 8a1ec5acef067e3e1d971deaa4b10cffa6294d75
workflow-type: tm+mt
source-wordcount: '668'
ht-degree: 28%

---

# À propos de l’éditeur d’expression avancé {#about-the-advanced-expression-editor}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_advanced"
>title="À propos de l’éditeur d’expression avancé"
>abstract="Utilisez l’éditeur d’expression avancé pour créer des expressions avancées dans divers écrans de l’interface. Par exemple, vous pouvez créer des expressions lors de la configuration et de l’utilisation de parcours, ainsi que lors de la définition d’une condition de source de données."

Utilisez l’éditeur d’expression avancé de Journey pour créer des expressions avancées dans divers écrans de l’interface. Par exemple, vous pouvez créer des expressions lors de la configuration et de l’utilisation de parcours, ainsi que lors de la définition d’une condition de source de données.

>[!NOTE]
>
>Les fonctions et fonctionnalités disponibles dans l’éditeur d’expression avancé de Parcours diffèrent de celles disponibles dans la variable [éditeur de personnalisation](../../personalization/functions/functions.md).

Il est également disponible chaque fois que vous devez définir des paramètres d’action qui nécessitent des manipulations de données spécifiques. Vous pouvez exploiter les données issues d’événements ou d’informations supplémentaires récupérées de la source de données.
Dans un parcours, la liste affichée des champs d’événement est contextuelle et varie selon le ou les événements ajoutés dans le parcours.

L’éditeur d’expression avancé propose un ensemble de fonctions et d’opérateurs intégrés qui vous permettent de manipuler des valeurs et de définir une expression qui répond spécifiquement à vos besoins. L’éditeur d’expression avancé vous permet également de définir les valeurs du paramètre de source de données externe, de manipuler les champs de mappage et les collections, comme les événements d’expérience.

![](../assets/journey65.png)

_Interface de l’éditeur d’expression avancé_

L’éditeur d’expression avancé peut être utilisé pour :

* create [conditions avancées](../condition-activity.md#about_condition) sur les sources de données et les informations sur les événements
* définir des [activités d’attente](../wait-activity.md#custom)
* définition du mapping des paramètres d’action

Lorsque cela est possible, vous pouvez basculer entre les deux modes à l’aide du **[!UICONTROL Mode avancé]** / **[!UICONTROL Mode simple]** bouton . Le mode simple est décrit [here](../condition-activity.md#about_condition).

>[!NOTE]
>
>Les conditions peuvent être définies dans l’éditeur d’expression simple ou avancé. Ils renvoient toujours un type booléen.
>
>Les paramètres d’action peuvent être définis en sélectionnant des champs ou à l’aide de l’éditeur d’expression avancé. Ils renvoient un type de données spécifique en fonction de leur expression.

## Accès à l’éditeur d’expression avancé {#accessing-the-advanced-expression-editor}

Vous pouvez accéder à l’éditeur d’expression avancé de différentes manières :

* Lorsque vous créez une condition de source de données, vous pouvez accéder à l’éditeur avancé en cliquant sur **[!UICONTROL Mode avancé]**.

  ![](../assets/journeyuc2_33.png)

* Lorsque vous créez un minuteur personnalisé, l’éditeur avancé s’affiche directement.
* Lorsque vous mappez le paramètre d’action, cliquez sur **[!UICONTROL Mode avancé]**.

## Découverte de l’interface{#discovering-the-interface}

Cet écran vous permet d’écrire manuellement votre expression.

![](../assets/journey70.png)

Dans la partie gauche de l’écran s’affichent les champs et fonctions disponibles :

* **[!UICONTROL Événements]**: choisissez l’un des champs reçus de l’événement entrant. La liste affichée des champs d’événement est contextuelle et varie selon le ou les événements ajoutés dans le parcours. [En savoir plus](../../event/about-events.md)
* **[!UICONTROL Audiences]** : si vous avez déposé un événement de **[!UICONTROL qualification d’audience]**, choisissez l’audience à utiliser dans votre expression. [En savoir plus](../condition-activity.md#using-a-segment)
* **[!UICONTROL Sources de données]**: effectuez votre choix dans la liste des champs disponibles des groupes de champs de vos sources de données. [En savoir plus](../../datasource/about-data-sources.md)
* **[!UICONTROL Propriétés du parcours]**: cette section regroupe les champs techniques liés au parcours pour un profil donné. [En savoir plus](journey-properties.md)
* **[!UICONTROL Fonctions]**: effectuez votre choix dans la liste des fonctions intégrées permettant d’effectuer un filtrage complexe. Les fonctions sont organisées par catégories. [En savoir plus](functions.md)

![](../assets/journey65.png)

Un mécanisme de saisie semi-automatique affiche des suggestions contextuelles.

![](../assets/journey68.png)

Un mécanisme de validation de syntaxe vérifie l’intégrité de votre code. Les erreurs s’affichent en haut de l’éditeur.

![](../assets/journey69.png)

**Nécessité de paramètres lors de la création de conditions avec l’éditeur d’expression avancé**

Si vous sélectionnez un champ d’une source de données externe qui nécessite l’appel d’un paramètre (voir [cette page](../../datasource/external-data-sources.md)), un nouvel onglet s’affiche à droite pour vous permettre de spécifier ce paramètre. La valeur du paramètre peut provenir des événements situés dans le parcours ou de la source de données Experience Platform (et non d’autres sources de données externes). Par exemple, dans une source de données météorologiques, un paramètre fréquemment utilisé est &quot;city&quot; (ville). Par conséquent, vous devez sélectionner l’emplacement où vous souhaitez obtenir ce paramètre de ville. Des fonctions peuvent également être appliquées aux paramètres pour effectuer des modifications de format ou des concaténations.

![](../assets/journeyuc2_19.png)

Dans les cas d’utilisation plus complexes, si vous souhaitez inclure les paramètres de la source de données dans l’expression principale, vous pouvez définir leurs valeurs à l’aide du mot-clé &quot;params&quot;. Consultez [cette page](../expression/field-references.md).
