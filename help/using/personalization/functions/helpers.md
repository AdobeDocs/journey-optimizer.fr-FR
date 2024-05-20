---
title: Assistants
description: Assistants
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: b08dc0f8-c85f-4aca-85eb-92dc76b0e588
source-git-commit: 7e7ff2f6451947d4d52efb2963d940ba3f50819f
workflow-type: ht
source-wordcount: '362'
ht-degree: 100%

---

# Assistants {#gs-helpers}

## Valeur de secours par défaut{#default-value}

L’helper `Default Fallback Value` est utilisé pour renvoyer une valeur de secours par défaut si un attribut est vide ou nul. Ce mécanisme fonctionne pour les attributs de profil et les événements de parcours.

**Syntaxe**

```sql
Hello {%=profile.personalEmail.name.firstName ?: "there" %}!
```

Dans cet exemple, la valeur `there` s&#39;affiche si l&#39;attribut `firstName` de ce profil est vide ou nul.

## Conditions{#if-function}

L&#39;helper `if` est utilisé pour définir un bloc conditionnel.
Si l&#39;évaluation de l&#39;expression renvoie true, le bloc est rendu, sinon il est ignoré.

**Syntaxe**

```sql
{%#if contains(profile.personalEmail.address, ".edu")%}
<a href="https://www.adobe.com/academia">Check out this link</a>
```

À la suite de l&#39;helper `if`, vous pouvez saisir une instruction `else` pour spécifier un bloc de code à exécuter, si la même condition est false.
L&#39;instruction `elseif` spécifie une nouvelle condition à tester si la première instruction renvoie false.


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

1. **Générer différents liens de boutique en fonction d&#39;expressions conditionnelles**

   ```sql
   {%#if profile.homeAddress.countryCode = "FR"%}
   <a href="https://www.somedomain.com/fr">Consultez notre catalogue</a>
   {%else%}
   <a href="https://www.somedomain.com/en">Checkout our catalogue</a>
   {%/if%}
   ```

1. **Déterminer l&#39;extension d&#39;adresse e-mail**

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Ajout d&#39;un lien conditionnel**

   L&#39;opération suivante ajoutera un lien vers le site Web &#39;www.adobe.com/academia&#39; pour les profils avec des adresses e-mail &#39;.edu&#39; uniquement, vers le site Web &#39;www.adobe.com/org&#39; pour les profils avec des adresses e-mail &#39;.org&#39;, et l&#39;URL par défaut &#39;www.adobe.com/users&#39; pour tous les autres profils :

   ```sql
   {%#if contains(profile.personalEmail.address, ".edu")%}
   <a href="https://www.adobe.com/academia">Checkout our page for Academia personals</a>
   {%else if contains(profile.personalEmail.address, ".org")%}
   <a href="https://www.adobe.com/orgs">Checkout our page for Non Profits</a>
   {%else%}
   <a href="https://www.adobe.com/users">Checkout our page</a>
   {%/if%}
   ```

1. **Contenu conditionnel basé sur l’appartenance à une audience**

   ```sql
   {%#if profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8b").status = "existing"%}
   Hi! Esteemed gold member. <a href="https://www.somedomain.com/gold">Checkout your exclusive perks </a>
   {%else%} if 'profile.segmentMembership.get("ups").get("5fd513d7-d6cf-4ea2-856a-585150041a8c").status = "existing"'%}
   Hi! Esteemed silver member. <a href="https://www.somedomain.com/silver">Checkout your exclusive perks </a>
   {%/if%}
   ```

>[!NOTE]
>
>Pour en savoir plus sur les audiences et le service de segmentation, consultez cette [section](../../audience/about-audiences.md).


## Unless{#unless}

L&#39;helper `unless` est utilisé pour définir un bloc conditionnel. Par opposition à l&#39;helper `if`, si l&#39;évaluation de l&#39;expression renvoie false, le bloc est rendu.

**Syntaxe**

```sql
{%#unless unlessCondition%} element_1 {%else%} default_element {%/unless%}
```

**Exemple**

Générer du contenu en fonction de l&#39;extension d&#39;adresse e-mail :

```sql
{%#unless endsWith(profile.personalEmail.address, ".edu")%}
Some Normal Content
{%else%}
Some edu specific content Content
{%/unless%}
```

## Each{#each}

L&#39;helper `each` est utilisé pour effectuer une itération sur un tableau.
La syntaxe de l’assistant est ```{{#each ArrayName}}``` YourContent {{/each}}
Il est possible de se référer aux éléments individuels du tableau en utilisant le mot-clé **this** à l’intérieur du bloc. L’index de l’élément du tableau peut être rendu à l’aide de {{@index}}.

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

Générer une liste de produits que cet utilisateur a dans son panier :

```sql
{{#each profile.products as |product|}}
    <li>{{product.productName}} {{product.productRating}}</li>
   </br>
{{/each}}
```

## Avec{#with}

L&#39;helper `with` permet de modifier le jeton d&#39;évaluation d&#39;une partie de modèle.

**Syntaxe**

```sql
{{#with profile.person.name}}
{{this.firstName}} {{this.lastName}}
{{/with}}
```

L&#39;helper `with` est utile pour définir également une variable de raccourci.

**Exemple**

Utiliser l&#39;option avec pour attribuer un alias aux noms de variables longs par rapport aux noms plus courts :

```sql
{{#with profile.person.name as |name|}}
 Hi {{name.firstName}} {{name.lastName}}!
 Checkout our trending products for today!
{{/with}}
```

## Let{#let}

La fonction `let` permet à une expression d&#39;être stockée en tant que variable et d&#39;être utilisé ultérieurement dans une requête.

**Syntaxe**

```sql
{% let variable = expression %} {{variable}}
```

**Exemple**

L&#39;exemple suivant permet de calculer la somme totale des prix des produits du panier dont les prix sont compris entre 100 et 1 000.

```sql
{% let sum = 0%}
    {{#each profile.productsInCart as |p|}}
        {%#if p.price>100 and p.price<1000%}
            {%let sum = sum + p.price %}
        {%/if%}
    {{/each}}
{{sum}}
```
