---
solution: Journey Optimizer
product: journey optimizer
title: Utiliser l’éditeur d’expression avancé
description: Découvrir comment créer des expressions avancées
feature: Journeys
role: Developer
level: Experienced
keywords: éditeur d’expression, données, parcours
exl-id: 9ea6cc3a-6a1b-4e8f-82ff-f8b1812617d7
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/8RsF-CRRrsLiCzwsaqfJQnWcyy6frmKkdSJBKnIhGgE
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2:
  - id: ac5d9310-7772-40fb-9d78-864562e1bfd6
  - id: e51e8901-97d9-4f7d-a835-503025a90e32
  - id: fa683eda-48de-4558-af32-2673edcd44fe
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
source-git-commit: f39bcb2f8b68315b082014b96801c51223ac8a54
workflow-type: tm+mt
source-wordcount: 738
ht-degree: 97%

---

# Utiliser l’éditeur d’expression avancé {#about-the-advanced-expression-editor}

>[!CONTEXTUALHELP]
>id="ajo_journey_expression_advanced"
>title="À propos de l’éditeur d’expression avancé"
>abstract="Utilisez l’éditeur d’expression avancé pour créer des expressions avancées dans divers écrans de l’interface. Par exemple, vous pouvez créer des expressions lors de la configuration et de l’utilisation de parcours, ainsi que lors de la définition d’une condition de source de données."

Utilisez l’éditeur d’expression avancé de Journey pour créer des expressions avancées dans divers écrans de l’interface. Par exemple, vous pouvez créer des expressions lors de la configuration et de l’utilisation de parcours, ainsi que lors de la définition d’une condition de source de données.

Il est également disponible chaque fois que vous devez définir des paramètres d’action qui nécessitent des manipulations de données spécifiques. Vous pouvez exploiter les données issues d’événements ou d’informations supplémentaires récupérées de la source de données. Dans un parcours, la liste des champs d’événements affichée est contextuelle et varie selon le ou les événements ajoutés dans le parcours.

![](../assets/journey65.png)


L’éditeur d’expression avancé propose un ensemble de fonctions et d’opérateurs intégrés qui vous permettent de manipuler des valeurs et de définir une expression qui répond spécifiquement à vos besoins. L’éditeur d’expression avancé vous permet également de définir les valeurs du paramètre de source de données externe et de manipuler les champs de mappage et les collections.

>[!NOTE]
>
>Les fonctions et les fonctionnalités disponibles dans l’éditeur d’expression avancé de Journey diffèrent de celles disponibles dans l’[éditeur de personnalisation](../../personalization/functions/functions.md).

## Accéder à l’éditeur d’expression avancé {#accessing-the-advanced-expression-editor}

L’éditeur d’expression avancé peut être utilisé pour effectuer ce qui suit :

* Créer des [conditions avancées](../conditions.md#data_source_condition) pour des sources de données et des informations d’événements.
* Définir des [activités Attente](../wait-activity.md#custom) personnalisées.
* Définir le mappage de paramètres d’actions.

Lorsque cela est possible, vous pouvez basculer entre les deux modes à l’aide du bouton **[!UICONTROL Mode avancé]**/**[!UICONTROL Mode simple]**. Le mode simple est décrit [ici](../conditions.md#about_condition).

>[!NOTE]
>
>* Les conditions peuvent être définies dans l’éditeur d’expression simple ou l’éditeur d’expression avancé. Elles renvoient toujours un type booléen.
>
>* Les paramètres d’actions peuvent être définis en sélectionnant des champs ou à l’aide de l’éditeur d’expression avancé. Ils renvoient un type de données spécifique en fonction de leur expression.

Vous pouvez accéder à l’éditeur d’expression avancé de différentes manières :

* Lorsque vous créez une condition de source de données, vous pouvez accéder à l’éditeur avancé en cliquant sur **[!UICONTROL Mode avancé]**.

  ![](../assets/journeyuc2_33.png)

* Lorsque vous créez un retardateur personnalisé, l’éditeur avancé s’affiche automatiquement.
* Lorsque vous mappez un paramètre d’action, cliquez sur **[!UICONTROL Mode avancé]**.

>[!NOTE]
>
>Pour générer des expressions de Parcours à l’aide d’invites en langage naturel, utilisez l’**[Assistant d’expression](expression-agent.md)** (**bêta publique**) via le contrôle de l’IA dans l’éditeur avancé.

## Découvrir l’interface {#discovering-the-interface}

Cet écran vous permet d’écrire manuellement votre expression.

![](../assets/journey70.png)

Dans la partie gauche de l’écran, les champs et les fonctions disponibles sont affichés :

* **[!UICONTROL Événements]** : choisissez l’un des champs reçus à partir de l’événement entrant. La liste des champs d’événements affichée est contextuelle et varie selon le ou les événements ajoutés dans le parcours. [En savoir plus](../../event/about-events.md)

  >[!CAUTION]
  >
  >La création d’expressions à l’aide d’événements d’expérience n’est pas prise en charge. Les autres approches et bonnes pratiques pour créer des expressions et des logiques avec des événements d’expérience sont référencées [ici](../../building-journeys/exp-event-lookup.md).

* **[!UICONTROL Audiences]** : si vous avez déposé un événement de **[!UICONTROL qualification d’audience]**, choisissez l’audience à utiliser dans votre expression. [En savoir plus](../conditions.md#using-a-segment)
* **[!UICONTROL Sources de données]** : choisissez dans la liste des champs disponibles issue des groupes de champs de vos sources de données. [En savoir plus](../../datasource/about-data-sources.md)
* **[!UICONTROL Propriétés du parcours]** : cette section regroupe les champs techniques liés au parcours pour un profil donné. [En savoir plus](journey-properties.md)
* **[!UICONTROL Fonctions]** : choisissez dans la liste des fonctions intégrées qui permettent d’effectuer un filtrage complexe. Les fonctions sont organisées par catégories. [En savoir plus](functions.md)

![](../assets/journey65.png)

Un mécanisme d’autocomplétion affiche des suggestions contextuelles.

![](../assets/journey68.png)

Un mécanisme de validation de la syntaxe vérifie l’intégrité de votre code. Les erreurs s’affichent en haut de l’éditeur.

![](../assets/journey69.png)


>[!TIP]
>
>Lors de la création de conditions dans l’éditeur d’expression avancé, assurez-vous que vos expressions ne contiennent pas de caractères masqués ou non imprimables. De plus, utilisez des expressions sur une seule ligne pour éviter les erreurs d’analyse.


**Des paramètres sont requis lors de la création de conditions avec l’éditeur d’expression avancé.**

Si vous sélectionnez un champ d’une source de données externe qui nécessite l’appel d’un paramètre (voir [cette page](../../datasource/external-data-sources.md)), un nouvel onglet s’affiche à droite pour vous permettre de spécifier ce paramètre. La valeur du paramètre peut provenir des événements situés dans le parcours ou de la source de données Experience Platform (et non d’autres sources de données externes). Par exemple, dans une source de données météorologique, un paramètre fréquemment utilisé est « ville ». Par conséquent, vous devez sélectionner l’emplacement où vous souhaitez avoir ce paramètre « ville ». Des fonctions peuvent également être appliquées aux paramètres pour effectuer des modifications de format ou des concaténations.

![](../assets/journeyuc2_19.png)

Dans les cas d’utilisation plus complexes, si vous souhaitez inclure les paramètres de la source de données dans l’expression principale, vous pouvez définir leurs valeurs à l’aide du mot-clé « params ». Consultez [cette page](../expression/field-references.md).
