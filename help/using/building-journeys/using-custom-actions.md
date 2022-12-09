---
solution: Journey Optimizer
product: journey optimizer
title: Utilisation d’actions personnalisées
description: Découvrez comment utiliser des actions personnalisées
feature: Actions
topic: Content Management
role: User
level: Intermediate
exl-id: 2b1b3613-3096-43ec-a860-600dda1d83b2
source-git-commit: 021cf48ab4b5ea8975135a20d5cef8846faa5991
workflow-type: tm+mt
source-wordcount: '395'
ht-degree: 0%

---

# Utilisation d’actions personnalisées {#use-custom-actions}

>[!CONTEXTUALHELP]
>id="ajo_journey_action_custom"
>title="Actions personnalisées"
>abstract="Les actions personnalisées vous permettent de configurer la connexion d’un système tiers pour envoyer des messages ou des appels d’API. Une action peut être configurée avec n’importe quel service de n’importe quel fournisseur pouvant être appelé via une API REST avec une payload au format JSON."

Les actions personnalisées vous permettent de configurer la connexion d’un système tiers pour envoyer des messages ou des appels d’API. Une action peut être configurée avec n’importe quel service de n’importe quel fournisseur pouvant être appelé via une API REST avec une payload au format JSON.

## Consentement et gouvernance des données {#privacy}

Dans Journey Optimizer, vous pouvez appliquer des stratégies de gouvernance des données et de consentement à vos actions personnalisées pour empêcher l’exportation de champs spécifiques vers des systèmes tiers ou exclure les clients qui n’ont pas consenti à recevoir des communications par courrier électronique, push ou SMS. Pour plus d&#39;informations, consultez les pages suivantes :

* [Gouvernance des données](../action/action-privacy.md).
* [Consentement](../action/consent.md).

## Configuration d’URL

Le volet de configuration de **Action personnalisée** affiche les paramètres de configuration de l’URL et les paramètres d’authentification configurés pour l’action personnalisée. Vous ne pouvez pas configurer la partie statique de l’URL dans le parcours, mais dans la configuration globale de l’action personnalisée. [En savoir plus](../action/about-custom-action-configuration.md).

### Chemin dynamique

Si l’URL comprend un chemin dynamique, spécifiez le chemin dans la variable **[!UICONTROL Path]** champ .

Pour concaténer des champs et des chaînes de texte brut, utilisez les fonctions String ou le signe plus (+) dans l’éditeur d’expression avancé. Placez les chaînes de texte brut entre guillemets simples (’) ou entre guillemets doubles (&quot;). [En savoir plus](expression/expressionadvanced.md).

Ce tableau présente un exemple de configuration :

| Champ | Valeur |
| --- | --- |
| URL | `https://xxx.yyy.com:8080/somethingstatic/` |
| Chemin | `The id of marketingCampaign + '/messages'` |

L’URL concaténée se présente comme suit :

`https://xxx.yyy.com:8080/somethingstatic/`\&lt;campaign id=&quot;&quot;>`/messages`

![](assets/journey-custom-action-url.png)

### En-têtes

Le **[!UICONTROL URL Configuration]** La section affiche les champs d’en-tête dynamiques, mais pas les champs d’en-tête constants. Les champs d’en-tête dynamique sont des champs d’en-tête HTTP dont la valeur est configurée comme variable. [En savoir plus](../action/about-custom-action-configuration.md).

Si nécessaire, spécifiez la valeur des champs d’en-tête dynamique :

1. Sélectionnez l’action personnalisée dans le parcours.
1. Dans le volet de configuration, cliquez sur l’icône en forme de crayon en regard du champ d’en-tête dans la **[!UICONTROL URL Configuration]** .

   ![](assets/journey-dynamicheaderfield.png)

1. Sélectionnez un champ et cliquez sur **[!UICONTROL OK]**.

## Paramètres d’action

Dans le **[!UICONTROL Action parameters]** , les paramètres de message définis comme _&quot;Variable&quot;_. Pour ces paramètres, vous pouvez définir où obtenir ces informations (par exemple : événements, sources de données), transmettez les valeurs manuellement ou utilisez l’éditeur d’expression avancé pour les cas d’utilisation avancés. Les cas d’utilisation avancés peuvent être la manipulation de données et d’autres utilisations de la fonction. Consultez cette section [page](expression/expressionadvanced.md).

**Rubriques connexes**

[Configuration d’une action](../action/about-custom-action-configuration.md)
