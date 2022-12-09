---
title: Helpers
description: Helpers
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 44e87553b5a001414f28a972ec5c61947decdf55
workflow-type: tm+mt
source-wordcount: '372'
ht-degree: 0%

---

# Helpers {#gs-helpers}

## Valeur de secours par défaut{#default-value}

Le `Default Fallback Value` helper est utilisé pour renvoyer une valeur de secours par défaut si un attribut est vide ou nul. Ce mécanisme fonctionne pour les attributs de profil et les événements de parcours.

**Syntaxe**

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

Dans cet exemple, la valeur `there` s’affiche si la variable `firstName` de ce profil est vide ou nul.

## Conditions{#if-function}

Le `if` helper est utilisé pour définir un bloc conditionnel.
Si l’évaluation de l’expression renvoie true (vrai), le bloc est rendu, sinon il est ignoré.

**Syntaxe**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

En procédant comme suit : `if` aide, vous pouvez saisir une `else` pour spécifier un bloc de code à exécuter, si la même condition est fausse.
Le `elseif` spécifie une nouvelle condition à tester si la première instruction renvoie false (faux).


**Format**

```sql
{
    {
        {%#if condition1%} element_1 
        {%else if condition2%} element_2 
        {%else%} default_element 
        {%/if%}
    }
}
```

**Exemples**

1. **Rendu de différents liens de magasin en fonction d’expressions conditionnelles**

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
   {%/if%}
   ```

1. **Déterminer l’extension de l’adresse électronique**

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Ajout d’un lien conditionnel**

   L&#39;opération suivante ajoutera un lien vers le &#39;site web www.adobe.com/academia&#39; pour les profils ayant uniquement des adresses email &#39;.edu&#39;, vers le &#39;site web www.adobe.com/org&#39; pour les profils ayant des adresses email &#39;.org&#39;, et l&#39;URL par défaut &#39;www.adobe.com/users&#39; pour tous les autres profils :

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Contenu conditionnel basé sur l’appartenance à un segment**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

1. **Déterminer si un profil est déjà membre**

   ```sql
   {%#if profile.segmentMembership.get(segments.`123e4567-e89b-12d3-a456-426614174000`.id)%}
       You're a member!
   {%else%}
       You should be a member! Sign up now!
   {%/if%}
   ```

>[!NOTE]
>
>Pour en savoir plus sur le service de segmentation et de segmentation, reportez-vous à cette section [section](../../segment/about-segments.md).


## Sauf{#unless}

Le `unless` helper est utilisé pour définir un bloc conditionnel. Par opposition au `if`  assistance, si l’évaluation de l’expression renvoie false, le bloc est rendu.

**Syntaxe**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Exemple**

Rendre du contenu en fonction de l’extension de l’adresse électronique :

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

## Chaque{#each}

Le `each` helper est utilisé pour effectuer une itération sur un tableau.
La syntaxe de l’assistant est la suivante : ```{{#each ArrayName}}``` YourContent {{/each}}
Nous pouvons nous référer aux éléments individuels du tableau à l’aide du mot-clé . **this** à l&#39;intérieur du bloc. L’index de l’élément du tableau peut être rendu à l’aide de {{@index}}.

**Syntaxe**

```sql
{{#each profile.productsInCart}}
    <li>{{this.name}}</li>
    </br>
{{/each}}
```

**Exemple**

```sql
{{#each profile.homeAddress.city}}
  {{@index}} : {{this}}<br>
{{/each}}
```

**Exemple**

Rendre la liste des produits que cet utilisateur a dans son panier :

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

## Avec{#with}

Le `with` helper est utilisé pour modifier le jeton d’évaluation de template-part.

**Syntaxe**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

Le `with` Cette fonction est utile pour définir une variable de raccourci.

**Exemple**

Utilisez avec pour donner un alias aux noms de variables longs par rapport aux noms plus courts :

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Let{#let}

Le `let` permet à une expression d’être stockée en tant que variable et d’être utilisée ultérieurement dans une requête.

**Syntaxe**

```sql
{% let variable = expression %} {{variable}}
```

**Exemple**

L’exemple suivant permet d’utiliser toutes les sommes des totaux des produits pour la transaction en USD, pour laquelle la somme est supérieure à 100 USD et inférieure à 1 000 USD.

```sql
{% let variable = expression %} {{variable}}
```
