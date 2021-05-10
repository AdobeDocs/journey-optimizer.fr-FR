---
title: Syntaxe de la personnalisation
description: Découvrez comment utiliser la syntaxe de personnalisation
translation-type: tm+mt
source-git-commit: 4f097636e059c5d0676b0129cdbdb125e5ad9415
workflow-type: tm+mt
source-wordcount: '718'
ht-degree: 1%

---

# Syntaxe de la personnalisation {#personalization-syntax}

![](../assets/do-not-localize/badge.png)

## Introduction

La personnalisation dans Journey Optimizer est basée sur la syntaxe de modèle appelée Handlebars.
Pour une description complète de la syntaxe des barres de contrôle, voir [HandlebarsJS](https://handlebarsjs.com/).

Il utilise un modèle et un objet d’entrée pour générer du code HTML ou d’autres formats de texte. Les modèles de barres de poignées ressemblent à du texte normal avec des expressions de barres de poignées incorporées.

Exemple d&#39;expression simple :

```sql
{{profile.person.name}}
```

where:

* **** profileest un espace de nommage.
* **person.** name est un jeton composé par attributs. La structure des attributs est définie dans un Schéma Adobe Experience Platform XDM. [En savoir plus](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html).

## Règles générales de syntaxe

Les identificateurs peuvent être n’importe quel caractère Unicode, à l’exception des caractères suivants :

```
Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
```

La syntaxe est sensible à la casse.

Les mots **true**, **false**, **null** et **undefined** ne sont autorisés que dans la première partie d&#39;une expression de chemin.

Dans les barres de contrôle, les valeurs renvoyées par {{expression}} sont **HTML-escape**. Si l’expression contient &amp;, la sortie HTML avec séquence d’échappement renvoyée est générée sous la forme &amp;. Si vous ne souhaitez pas que les barres de contrôle échappent à une valeur, utilisez le &quot;triple-stash&quot;.

## Profil

Cet espace de nommage vous permet de référencer tous les attributs définis dans le schéma de profil décrit dans la documentation [Modèle de données Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html).

Les attributs doivent être définis dans le schéma avant d’être référencés dans un bloc de personnalisation Journey Optimizer.

Toutes les références sont validées par rapport au Schéma de Profil avec un mécanisme de validation décrit [ici](personalization-validation.md).

**Exemples de références :**

* ```{{profile.person.name.fullName}}```
* ```{{profile.person.name.firstName}}```
* ```{{profile.person.gender}}```
* ```{{profile.personalEmail.address}}```
* ```{{profile.mobilePhone.number}}```
* ```{{profile.homeAddress.city}}```
* ```{{profile.faxPhone.number}}```

**Déterminez l&#39;extension** d&#39;adresse électronique :

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
{%else if contains(profile.personalEmail.address, ".org")%}
<a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
{%else%}
<a href="https://www.adobe.com/users">Checkout our page</a>
{%/if%}
```

## Segments

Pour en savoir plus sur le service de segmentation et de segmentation, consultez cette [section](../segment/about-segments.md).

**Générer un contenu différent en fonction de l’appartenance** au segment :

```sql
{%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
  Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
{%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
  Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
{%/if%}
```

**Déterminez si un profil est déjà membre** :

```sql
{%#if profile.segmentMembership.get(segments.`123e4567-e89b-12d3-a456-426614174000`.id)%}
    You're a member!
{%else%}
    You should be a member! Sign up now!
{%/if%}
```

## Offres

Cet espace de nommage vous permet de référencer les décisions d&#39;offre existantes.
Pour référencer une offre, vous devez déclarer un chemin avec les différentes informations qui définissent une offre.

Ce chemin possède la structure suivante :
0 - &quot;offres : identifie l&#39;expression de chemin appartenant à l&#39;espace de nommage d&#39;offre
1 - Type : détermine le type de rendu de l&#39;offre. Les valeurs valides sont &#39;image&#39;, &#39;html&#39; et &#39;text&#39;
2 - Id de placement
3 - ID d’Activité
4 - Attributs spécifiques à l&#39;Offre. Selon le type d’offre, les attributs pris en charge peuvent être utilisés. Par exemple, pour les images `deliveryUrl`.

Pour plus d&#39;informations sur l&#39;API Décisions, consultez cette [page](https://experienceleague.corp.adobe.com/docs/offer-decisioning/using/api-reference/offer-delivery/deliver-offers.html?lang=en#deliver-offers-using-the-decisions-api)

Pour plus d&#39;informations sur la représentation des Offres, consultez cette [page](https://experienceleague.corp.adobe.com/docs/offer-decisioning/using/api-reference/offer-delivery/deliver-offers.html?lang=en#accept-and-content-type-headers).

Toutes les références sont validées par rapport aux Offres Schéma avec un mécanisme de validation décrit [ici](personalization-validation.md).

**Exemples de références :**

* Emplacement d’hébergement de l’image :

```offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl```

* URL de la cible lorsque vous cliquez sur l’image :

```offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl```

* Contenu textuel de l&#39;offre provenant du moteur de décision :

```offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content```

* Contenu HTML de l’offre provenant du moteur de décision :

```offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content```


## Assistance

Un assistant Handlebars est un identifiant simple qui peut être suivi de paramètres.
Chaque paramètre est une expression Handlebars. Ces assistants sont accessibles depuis n’importe quel contexte dans un modèle.

Ces assistants de blocs sont identifiés par un # précédant le nom de l&#39;aide et nécessitent une fermeture /, correspondante du même nom.
Les blocs sont des expressions qui ont une ouverture de bloc ({{# }}) et une fermeture ({{/}}).

### If{#if}

L&#39;aide **if** est utilisée pour définir un bloc conditionnel.
Si l’évaluation de l’expression renvoie true, le bloc est rendu, sinon il est ignoré.

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

Après l&#39;aide **if**, vous pouvez entrer une instruction **else** pour spécifier un bloc de code à exécuter, si la même condition est false.
L&#39;instruction **else if** spécifie une nouvelle condition à tester si la première instruction renvoie false.

**Générer différents liens de magasin en fonction d’expressions** conditionnelles :

```sql
{%#if profile.homeAddress.countryCode = "FR"%}
  <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
{%else%}
  <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
{%/if%}
```

### Sauf si{#unless}

**#** unlesshelper est utilisé pour définir un bloc conditionnel. Par opposition à l&#39;assistance **#if**, si l&#39;évaluation de l&#39;expression renvoie false, le bloc est rendu.

**Générer du contenu en fonction de l’extension** d’adresse électronique :

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

### Chacun{#each}

L&#39;assistance **each** est utilisée pour effectuer une itération sur une baie.
La syntaxe de l&#39;assistance est ```{{#each ArrayName}}``` YourContent {{/each}.
Nous pouvons nous référer aux éléments individuels de la baie en utilisant le mot-clé **this** à l&#39;intérieur du bloc. L&#39;index de l&#39;élément du tableau peut être rendu à l&#39;aide de {{@index}}.

Exemple :

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
    </br>
{{/each}}
```

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Générer une liste de produits que cet utilisateur a dans son panier** :

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

### Avec {#with}

L&#39;aide **#with** permet de modifier le jeton d&#39;évaluation de template-part.

Exemple :

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

L&#39;aide **#with** est utile pour définir également une variable de raccourci.

**Utilisez l’option avec pour attribuer un alias aux noms de variables longs par rapport aux noms** plus courts :

```
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```


## Limites

* L’utilisation de la variable **xEvent** n’est pas disponible dans les expressions de personnalisation. Toute référence à xEvent entraîne des échecs de validation.
