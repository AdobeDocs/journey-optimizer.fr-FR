---
solution: Journey Optimizer
product: journey optimizer
title: Syntaxe de la personnalisation
description: Découvrez comment utiliser la syntaxe de personnalisation.
feature: Personalization
topic: Personalization
role: Data Engineer
level: Intermediate
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
source-git-commit: 020c4fb18cbd0c10a6eb92865f7f0457e5db8bc0
workflow-type: tm+mt
source-wordcount: '719'
ht-degree: 0%

---

# Syntaxe de la personnalisation {#personalization-syntax}

Personnalisation dans [!DNL Journey Optimizer] est basé sur la syntaxe de modèle appelée Handlebars.
Pour une description complète de la syntaxe Handlebars, reportez-vous à la section [Documentation HandlebarsJS](https://handlebarsjs.com/).

Il utilise un modèle et un objet de saisie pour générer des formats HTML ou texte. Les modèles Handlebars ressemblent à du texte normal avec des expressions Handlebars incorporées.

Exemple d’expression simple :

`{{profile.person.name}}`

où :

* `profile` est un espace de noms.
* `person.name` est un jeton composé d’attributs. La structure des attributs est définie dans un schéma XDM Adobe Experience Platform. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.

## Règles générales de syntaxe {#general-rules}

Les identifiants peuvent être n’importe quel caractère unicode sauf ce qui suit :

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

La syntaxe est sensible à la casse.

Les mots **true**, **false**, **null** et **undefined** ne sont autorisées que dans la première partie d’une expression de chemin.

Dans les Guidons, les valeurs renvoyées par la variable {{expression}} are **Échappement HTML**. Si l’expression contient `&`, la sortie HTML échappée renvoyée est générée sous la forme `&amp;`. Si vous ne souhaitez pas que les Guidons échappent à une valeur, utilisez le &quot;triple-ensemble&quot;.

En ce qui concerne les arguments de fonctions littérales, l’analyseur de langue de modèle ne prend pas en charge la barre oblique inverse sans échappement unique (`\`). Ce caractère doit être échappé avec une barre oblique inverse supplémentaire (`\`). Exemple :

`{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

## Profil

Cet espace de noms vous permet de référencer tous les attributs définis dans le schéma de profil décrit dans [Documentation du modèle de données Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html){target=&quot;_blank&quot;}.

Les attributs doivent être définis dans le schéma avant d’être référencés dans une [!DNL Journey Optimizer] bloc de personnalisation.

>[!NOTE]
>
>Découvrez comment utiliser les attributs de profil dans des conditions dans [cette section](functions/helpers.md#if-function).

**Exemples de références :**

`{{profile.person.name.fullName}}`

`{{profile.person.name.firstName}}`

`{{profile.person.gender}}`

`{{profile.personalEmail.address}}`

`{{profile.mobilePhone.number}}`

`{{profile.homeAddress.city}}`

`{{profile.faxPhone.number}}`

## Segments{#perso-segments}

Découvrez comment utiliser les attributs de profil dans des conditions dans [cette section](functions/helpers.md#if-function).

>[!NOTE]
>Pour en savoir plus sur le service de segmentation et de segmentation, reportez-vous à la section [cette section](../segment/about-segments.md).

## Offres {#offers-syntax}

Cet espace de noms vous permet de référencer les décisions d’offres existantes.
Pour référencer une offre, vous devez déclarer un chemin avec les différentes informations qui définissent une offre.

Ce chemin possède la structure suivante :

`offers.Type.[Placement Id].[Activity Id].Attribute`

où :

* `offers` identifie l’expression de chemin appartenant à l’espace de noms de l’offre
* `Type`  détermine le type de représentation de l’offre. Les valeurs possibles sont les suivantes : `image`, `html` et `text`
* `Placement Id` et `Activity Id` sont des identifiants d’emplacement et d’activité ;
* `Attributes` sont des attributs spécifiques à l’offre qui dépendent du type d’offre. Exemple : `deliveryUrl` pour les images

Pour plus d’informations sur l’API Decisions et sur la représentation des offres, reportez-vous à la section [cette page](../offers/api-reference/offer-delivery-api/decisioning-api.md)

Toutes les références sont validées par rapport au schéma Offres avec un mécanisme de validation décrit dans [cette page](personalization-validation.md)

**Exemples de références :**

* Emplacement d’hébergement de l’image :

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

* URL cible lorsque vous cliquez sur l’image :

   `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

* Contenu textuel de l’offre provenant du moteur de prise de décision :

   `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

* Contenu HTML de l’offre provenant du moteur de prise de décision :

   `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`


## Helpers{#helpers-all}

Un assistant Handlebars est un identifiant simple qui peut être suivi de paramètres.
Chaque paramètre est une expression Handlebars. Ces assistants sont accessibles depuis n’importe quel contexte dans un modèle.

Ces assistants de bloc sont identifiés par un # précédant le nom de l’assistant et nécessitent une fermeture / correspondante du même nom.
Les blocs sont des expressions qui présentent une ouverture de bloc ({{# }}) and closing ({{/}}).


>[!NOTE]
>
>Les fonctions d’assistance sont présentées dans la section [cette section](functions/helpers.md).

## Types littéraux {#literal-types}

[!DNL Adobe Journey Optimizer] prend en charge les types littéraux suivants :

| Littéral | Définition |
| ------- | ---------- |
| Chaîne | Un type de données composé de caractères entourés de guillemets doubles. <br>Exemples : `"prospect"`, `"jobs"`, `"articles"` |
| Booléen | Type de données vrai ou faux. |
| Entier | Un type de données représentant un nombre entier. Il peut être positif, négatif ou nul. <br>Exemples : `-201`, `0`, `412` |
| Tableau | Type de données constitué d’un groupe d’autres valeurs littérales. Elle utilise des crochets pour regrouper et des virgules pour délimiter les différentes valeurs. <br> **Remarque :** Vous ne pouvez pas accéder directement aux propriétés des éléments d’un tableau. <br> Exemples : `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>L’utilisation de **xEvent** n’est pas disponible dans les expressions de personnalisation. Toute référence à xEvent entraîne des échecs de validation.

## Personnalisation des URL{#perso-urls}

Les URL personnalisées orientent les destinataires vers des pages spécifiques d&#39;un site web ou vers un microsite personnalisé, en fonction des attributs du profil. Dans Adobe Journey Optimizer, vous pouvez ajouter une personnalisation aux URL dans le contenu de votre message. La personnalisation de l&#39;URL peut être appliquée au texte et aux images, et utiliser les données de profil ou les données contextuelles.

Journey Optimizer vous permet de personnaliser une ou plusieurs URL dans votre message en leur ajoutant des champs de personnalisation. Pour personnaliser une URL, procédez comme suit :

1. Créez un lien dans le contenu de votre message. [En savoir plus](../email/message-tracking.md#insert-links)
1. Sélectionnez les attributs à partir de l’icône de personnalisation. L’icône de personnalisation n’est disponible que pour les types de liens suivants : **Lien externe**, **Lien de désabonnement** et **Exclusion**.

![](assets/perso-url.png)

>[!NOTE]
>
>Dans l’éditeur d’expression, lorsque vous modifiez une URL personnalisée, les fonctions d’assistance et l’appartenance aux segments sont désactivées pour des raisons de sécurité.

**Exemples d’URL personnalisées**

* `https://www.adobe.com/users/{{profile.person.name.lastName}}`
* `https://www.adobe.com/users?uid={{profile.person.name.firstName}}`
* `https://www.adobe.com/usera?uid={{context.journey.technicalProperties.journeyUID}}`
* `https://www.adobe.com/users?uid={{profile.person.crmid}}&token={{context.token}}`

>[!CAUTION]
>
>Les espaces ne sont pas pris en charge dans les jetons de personnalisation utilisés dans les URL.
