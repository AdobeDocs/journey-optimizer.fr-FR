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
source-git-commit: d3f0adab52ed8e44a6097c5079396d1e9c06e0a7
workflow-type: ht
source-wordcount: '668'
ht-degree: 100%

---

# À propos de l’éditeur d’expression avancé {#about-the-advanced-expression-editor}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_advanced"
>title="À propos de l’éditeur d’expression avancé"
>abstract="Utilisez l’éditeur d’expression avancé pour créer des expressions avancées dans divers écrans de l’interface. Par exemple, vous pouvez créer des expressions lors de la configuration et de l’utilisation de parcours, ainsi que lors de la définition d’une condition de source de données."

Utilisez l’éditeur d’expression avancé de Journey pour créer des expressions avancées dans divers écrans de l’interface. Par exemple, vous pouvez créer des expressions lors de la configuration et de l’utilisation de parcours, ainsi que lors de la définition d’une condition de source de données.

>[!NOTE]
>
>Les fonctions et fonctionnalités disponibles dans l’éditeur d’expression avancé de Journey diffèrent de celles disponibles dans l’[éditeur de personnalisation](../../personalization/functions/functions.md).

Il est également à votre disposition si vous avez besoin de définir des paramètres d’action qui nécessitent de manipuler des données spécifiques. Vous pouvez exploiter les données issues d’événements ou d’informations supplémentaires récupérées de la source de données.
Dans un parcours, la liste des champs d’événement affichée est contextuelle et varie selon les événements ajoutés.

L’éditeur d’expression avancé propose un ensemble de fonctions et d’opérateurs intégrés destinées à manipuler des valeurs et à définir une expression spécifiquement adaptée à vos besoins. L’éditeur permet également de définir les valeurs du paramètre de source de données externe, de gérer les champs de mapping et les collections, notamment les événements d’expérience.

![](../assets/journey65.png)

_Interface de l’éditeur d’expression avancé_

Vous pouvez utiliser l’éditeur d’expression avancé pour les opérations suivantes :

* créer des [conditions avancées](../condition-activity.md#about_condition) sur les sources de données et les informations relatives aux événements ;
* définir des activités [d’attente personnalisées](../wait-activity.md#custom) ;
* définir le mappage des paramètres d’action.

Lorsque cela est possible, vous pouvez basculer entre les deux modes à l’aide du bouton **** Mode avancé / Mode simple ****. Le mode simple est présenté [ici](../condition-activity.md#about_condition).

>[!NOTE]
>
>Vous pouvez définir des conditions dans l’éditeur d’expression simple ou avancé. Ces conditions renvoient toujours une valeur de type booléen.
>
>Vous pouvez définir des paramètres d’action en sélectionnant des champs ou à l’aide de l’éditeur d’expression avancé. Ces paramètres renvoient un type de données spécifique en fonction de leur expression.

## Accès à l’éditeur d’expression avancé {#accessing-the-advanced-expression-editor}

Il est possible d’accéder de différentes manières à l’éditeur d’expression avancé :

* Lorsque vous créez une condition de source de données, vous pouvez y accéder en cliquant sur **[!UICONTROL Mode avancé]**.

  ![](../assets/journeyuc2_33.png)

* Lorsque vous créez un retardateur personnalisé, l’éditeur avancé s’affiche directement.
* Lorsque vous mappez le paramètre d’action, cliquez sur le **[!UICONTROL Mode avancé]**.

## Découverte de l’interface{#discovering-the-interface}

Cet écran vous permet d’entrer manuellement votre expression.

![](../assets/journey70.png)

La partie gauche de l’écran contient les champs et les fonctions disponibles :

* **[!UICONTROL Événements]** : sélectionnez l’un des champs reçus de l’événement entrant. La liste des champs d’événement affichée est contextuelle et varie selon le(s) événement(s) ajouté(s) au parcours. [En savoir plus](../../event/about-events.md)
* **[!UICONTROL Audiences]** : si vous avez déposé un événement de **[!UICONTROL qualification d’audience]**, choisissez l’audience à utiliser dans votre expression. [En savoir plus](../condition-activity.md#using-a-segment)
* **[!UICONTROL Sources de données]** : effectuez votre choix parmi la liste de champs disponibles à partir des groupes de champs de vos sources de données. [En savoir plus](../../datasource/about-data-sources.md)
* **[!UICONTROL Propriétés du parcours]** : cette section regroupe les champs techniques liés au parcours pour un profil donné. [En savoir plus](journey-properties.md)
* **[!UICONTROL Fonctions]** : effectuez votre choix parmi la liste de fonctions intégrées permettant d’effectuer un filtrage complexe. Les fonctions sont classées par catégories. [En savoir plus](functions.md)

![](../assets/journey65.png)

Un mécanisme de saisie semi-automatique affiche des suggestions contextuelles.

![](../assets/journey68.png)

Un mécanisme de validation de syntaxe vérifie l’intégrité du code. Les erreurs s’affichent dans la partie supérieure de l’éditeur.

![](../assets/journey69.png)

**Nécessité de paramètres pour la création de conditions à l’aide de l’éditeur d’expression avancé**

Si vous sélectionnez un champ d’une source de données externe qui nécessite l’appel d’un paramètre (voir [cette page](../../datasource/external-data-sources.md)), un nouvel onglet s’affiche à droite pour vous permettre de spécifier ce paramètre. La valeur du paramètre peut provenir des événements situés dans le parcours ou de la source de données Experience Platform (et non d’autres sources de données externes). Le paramètre « ville », par exemple, est fréquemment utilisé dans une source de données météorologiques. Vous devez donc sélectionner l’emplacement où vous souhaitez obtenir ce paramètre. Il est également possible d’appliquer des fonctions aux paramètres pour effectuer des modifications de format ou des concaténations.

![](../assets/journeyuc2_19.png)

Dans les cas d’utilisation plus complexes, si vous souhaitez inclure les paramètres de la source de données dans l’expression principale, vous pouvez définir leurs valeurs à l’aide du mot-clé « params ». Consultez [cette page](../expression/field-references.md).
