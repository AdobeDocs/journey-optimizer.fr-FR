---
solution: Journey Optimizer
product: journey optimizer
title: Syntaxe de personnalisation
description: Découvrez comment utiliser la syntaxe de personnalisation.
feature: Personalization
topic: Personalization
role: Developer
level: Intermediate
keywords: expression, éditeur, syntaxe, personnalisation
exl-id: 5a562066-ece0-4a78-92a7-52bf3c3b2eea
TQID: https://experienceleague.adobe.com/kZEw2lITdt8SMWMe-UT2vPzdoiAjB2vbItmK9zt-WJo
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
level_v2:
  - id: b5a62a22-46f7-4f0d-b151-3fc640bef588
topic_v2:
  - id: e0eb8757-182f-49f3-94a4-1587d16f5094
subfeature_v2:
  - id: ac5d9310-7772-40fb-9d78-864562e1bfd6
  - id: e51e8901-97d9-4f7d-a835-503025a90e32
source-git-commit: f552e98f370f96e9a99d2f1d604f840ac6069d65
workflow-type: tm+mt
source-wordcount: 1979
ht-degree: 31%

---

# Syntaxe de personnalisation {#personalization-syntax}

>[!BEGINSHADEBOX]

**Sur cette page :** découvrez la syntaxe de personnalisation Handlebars et PQL dans Adobe Journey Optimizer, y compris les règles générales, les mots-clés réservés, la coercition de type, les espaces de noms disponibles et les bonnes pratiques.

>[!ENDSHADEBOX]

Dans [!DNL Journey Optimizer], Personalization utilise deux syntaxes complémentaires qui fonctionnent ensemble dans la même expression :

* **Handlebars** (`{{...}}`) : utilisé pour effectuer le rendu des attributs de profil, passer en boucle sur des tableaux et appeler des assistants de blocs. Reportez-vous à la documentation [HandlebarsJS](https://handlebarsjs.com/) pour une référence complète.
* **Profile Query Language (PQL)** (`{%= ... %}`) : utilisé pour appeler des fonctions intégrées (par exemple `upperCase()`, `formatDate()`, `dateDiff()`) et évaluer des expressions conditionnelles.

Comprendre dans quel contexte vous vous trouvez est essentiel pour éviter les erreurs d’exécution. Par exemple, un appel de fonction PQL placé dans `{{...}}` échouera, car Handlebars tente de le résoudre en tant qu’assistant plutôt que de l’évaluer en tant qu’expression PQL.

**Exemples :**

| Cas d’utilisation | Syntaxe |
|----------|--------|
| Rendu d’un attribut de profil | `{{profile.person.name.firstName}}` |
| Appeler une fonction PQL | `{%= upperCase(profile.person.name.firstName) %}` |
| Bloc conditionnel | `{%#if profile.loyalty.tier = "gold"%}...{%/if%}` |
| Boucle sur un tableau | `{{#each profile.orders}}...{{/each}}` |

La structure des attributs est définie dans un schéma XDM Adobe Experience Platform. [En savoir plus](https://experienceleague.adobe.com/fr/docs/experience-platform/xdm/home){target="_blank"}.

>[!TIP]
>
>Pour les expressions prêtes à l’emploi qui appliquent ces syntaxes à des scénarios réels (mise en forme des dates, comptes à rebours, basculements conditionnels, etc.), consultez la page **[recettes](personalization-recipes.md)**.

## Règles générales de syntaxe {#general-rules}

* Les identifiants peuvent être n’importe quel caractère Unicode, à l’exception des caractères spéciaux suivants, qui sont réservés à la syntaxe Handlebars :

  ```
  Whitespace ! " # % & ' ( ) * + , . / ; < = > @ [ \ ] ^ ` { | } ~
  ```

* La syntaxe est sensible à la casse.

* Les mots **true**, **false**, **null** et **undefined** ne sont autorisés que dans la première partie d&#39;une expression de chemin.

* Dans Handlebars, les valeurs renvoyées par {{expression}} se caractérisent par un **échappement HTML.** Si l’expression contient `&`, la sortie avec échappement HTML renvoyée est générée sous la forme `&amp;`. Si vous ne souhaitez pas que Handlebars effectue l’échappement d’une valeur, utilisez trois accolades au lieu de deux.

  Supposons que la valeur du champ `profile.person.name` soit « Mark &amp; Mary ». Le `{{profile.person.name}}` de syntaxe affiche `Mark &amp; Mary`, tandis que `{{{profile.person.name}}}` affiche `Mark & Mary`.

* En ce qui concerne les arguments de fonctions littérales, l’analyseur de langage de création de modèles ne prend pas en charge la barre oblique inverse sans échappement (`\`). Ce caractère doit avoir fait l’objet d’un échappement avec une barre oblique inverse supplémentaire (`\`). Exemple :

  `{%= regexGroup("abc@xyz.com","@(\\w+)", 1)%}`

* Pour inclure un **guillemet double littéral** dans une valeur de chaîne (par exemple lors de la génération d’une sortie JSON), insérez une barre oblique inverse (`\"`) dans l’échappement :

  ```handlebars
  { "message": "Hello \"{{profile.person.name.firstName}}\"" }
  ```

  Sortie : `{ "message": "Hello \"John\"" }`

  Vous pouvez également utiliser la `{{{ }}}` triple stash pour générer une valeur HTML sans échappement lorsque la valeur elle-même contient des caractères spéciaux que vous ne souhaitez pas encoder dans HTML.

## Mots-clés réservés {#reserved-keywords}

Certains mots-clés sont réservés dans PQL (Profile Query Language) et ne peuvent pas être utilisés directement comme noms de champ ou de variable dans les expressions de personnalisation. Si votre schéma XDM contient des champs dont les noms correspondent à des mots-clés réservés, vous devez leur appliquer une séquence d’échappement à l’aide d’accents graves (`` ` ``) pour les référencer dans vos expressions.

**Les mots-clés réservés sont les suivants :**

* `next`
* `last`
* `this`

**Exemple :**

Si votre schéma de profil comporte un champ nommé `next`, vous devez l’encadrer de guillemets inversés :

```
{{profile.person.`next`.name}}
```

Sans les guillemets inversés, l’éditeur de personnalisation échouera lors de la validation et vous obtiendrez une erreur.

>[!NOTE]
>
>L’échappement avec barre oblique inverse pour les mots-clés réservés s’applique à la fois aux chemins Handlebars `{{...}}` et aux expressions PQL `{%= ... %}`, car ces mots-clés sont réservés au niveau de résolution du chemin. Cette approche est différente des noms de champ avec trait d’union, où l’échappement par backtick n’est pris en charge que dans les expressions PQL. Voir [Clés d’attribut coupées](#hyphenated-keys).

## Règles de syntaxe PQL pour les clés d’attribut spéciales {#pql-special-keys}

Au-delà des mots-clés réservés, deux cas supplémentaires nécessitent une séquence d’échappement dans les expressions PQL.

### Clés d’attribut avec trait d’union {#hyphenated-keys}

Si votre schéma XDM contient des noms de champ avec des tirets (par exemple `my-field`, `event-type`) ou des noms commençant par ou contenant des chiffres, placez la clé avec des accents graves dans les expressions PQL :

```sql
{%= profile.events.`order-total` > 100 %}
```

>[!NOTE]
>
>L’échappement avec backtick est uniquement pris en charge dans les expressions PQL (`{%= ... %}`). Il n’est pas pris en charge dans l’interpolation Handlebars (`{{...}}`). Toutefois, les noms de champ avec trait d’union peuvent être référencés directement dans les blocs de `{{...}}` (par exemple, `{{profile.my-custom-field}}`) ; seule la syntaxe backtick échoue à cet endroit.

Sans backticks dans une expression PQL, le trait d&#39;union est interprété comme un opérateur de soustraction et provoque une erreur de syntaxe PQL.

### Identifiants d’événement numériques dans les attributs contextuels {#numeric-event-ids}

Lors du référencement d’attributs d’événement contextuels où l’identifiant d’événement est un nombre (par exemple, `1697323153`), placez-le entre accents graves. Cela s’applique également aux fonctions internes telles que `formatDate()` :

```handlebars
{% let ts = formatDate(toDateTime(context.journey.events.`1697323153`.timestamp), "dd/MM/yyyy") %}
{{ts}}
```

## Type coercition {#type-coercion}

PQL est fortement typé. Lors de la comparaison ou de la transmission de valeurs, les deux côtés doivent être du même type. Cas courants :

| Scénario | Solution |
|----------|----------|
| Valeur numérique stockée sous forme de chaîne | Utiliser `stringToNumber()` avant l&#39;arithmétique ou la comparaison : `{%= stringToNumber(profile.loyalty.pointsBalance) > 500 %}` |
| Entier stocké sous forme de chaîne | Utiliser `string_to_integer()` ou `stringToNumber()` avant l&#39;arithmétique |
| Booléen stocké sous forme de chaîne | Utilisez `toBool()` pour convertir : `{%= toBool(profile.consents.email.val) = true %}` |

## Espaces de noms disponibles {#namespaces}

* **Profile**

  Cet espace de noms vous permet de référencer tous les attributs définis dans le schéma de profil décrit dans la [documentation Modèle de données Adobe Experience Platform (XDM)](https://experienceleague.adobe.com/docs/experience-platform/xdm/home.html?lang=fr){target="_blank"}.

  Les attributs doivent être définis dans le schéma avant d&#39;être référencés dans un bloc de personnalisation [!DNL Journey Optimizer].

  Pour plus d’informations sur l’utilisation des attributs de profil dans des conditions, consultez [cette section](functions/helpers.md#if-function).

  +++Exemples de références

   * `{{profile.person.name.fullName}}`
   * `{{profile.person.name.firstName}}`
   * `{{profile.person.gender}}`
   * `{{profile.personalEmail.address}}`
   * `{{profile.mobilePhone.number}}`
   * `{{profile.homeAddress.city}}`
   * `{{profile.faxPhone.number}}`

  +++

* **Audience**

  Pour en savoir plus sur le service de segmentation, consultez [cette documentation](https://experienceleague.adobe.com/docs/experience-platform/segmentation/home.html?lang=fr){target="_blank"}.

* **Offres**

  Cet espace de noms vous permet de référencer les décisions d’offre existantes.

  Pour référencer une offre, vous devez déclarer un chemin avec les différentes informations qui définissent une offre. Ce chemin possède la structure suivante :

  `offers.Type.[Placement Id].[Activity Id].Attribute`

  où :

   * `offers` identifie l&#39;expression de chemin appartenant à l&#39;espace de noms de l&#39;offre.
   * `Type` détermine le type de représentation de l&#39;offre. Les valeurs possibles sont les suivantes : `image`, `html` et `text`.
   * `Placement Id` et `Activity Id` sont des identifiants d&#39;emplacement et d&#39;activité.
   * `Attributes` sont des attributs spécifiques à l&#39;offre qui dépendent du type d&#39;offre. Exemple : `deliveryUrl` pour les images

  Pour plus d’informations sur l’API Decisions et sur la représentation des offres, consultez [cette page](../offers/api-reference/offer-delivery-api/decisioning-api.md).

  Toutes les références sont validées par rapport au schéma d’offres avec un mécanisme de validation décrit sur [cette page](../personalization/personalization-build-expressions.md).

  +++Exemples de références

   * Emplacement où l&#39;image est hébergée :

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].deliveryUrl`

   * URL de la cible lorsque vous cliquez sur l&#39;image :

     `offers.image.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].linkUrl`

   * Contenu textuel de l&#39;offre provenant du moteur de décision :

     `offers.text.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

   * Contenu HTML de l&#39;offre provenant du moteur de décision :

     `offers.html.[offers:xcore:offer-placement:126f767d74b0da80].[xcore:offer-activity:125e2c6889798fd9].content`

  +++

## Assistants {#helpers-all}

Un assistant Handlebars est un identifiant simple qui peut être suivi de paramètres. Chaque paramètre est une expression Handlebars. Ces assistants sont accessibles depuis n&#39;importe quel contexte dans un modèle.

Ces assistants de bloc sont identifiés par un `#` placé devant le nom de l’assistant et une `/` correspondante doit être placée à la fin avec le même nom.

Les blocs sont des expressions qui ont une ouverture (`{{# }}`) et une fermeture (`{{/}}`) de bloc.

Pour plus d’informations sur les fonctions d’assistance, consultez [cette section](functions/helpers.md).

## Types littéraux {#literal-types}

[!DNL Adobe Journey Optimizer] prend en charge les types littéraux suivants :

| Littéral | Définition |
| ------- | ---------- |
| Chaîne | Un type de données composé de caractères entourés par des guillemets doubles. <br>Exemples : `"prospect"`, `"jobs"`, `"articles"` |
| Booléen | Un type de données qui est soit vrai soit faux. |
| Entier | Un type de données représentant un nombre entier. Ce nombre peut être positif, négatif ou nul. <br>Exemples : `-201`, `0`, `412` |
| Tableau | Un type de données composé d’un groupe d’autres valeurs littérales. Elle utilise des crochets pour regrouper et des virgules pour délimiter les différentes valeurs. <br> **Remarque :** vous ne pouvez pas accéder directement aux propriétés des éléments d’un tableau. <br> Exemples : `[1, 4, 7]`, `["US", "FR"]` |

>[!CAUTION]
>
>L&#39;utilisation de la variable **xEvent** n&#39;est pas disponible dans les expressions de personnalisation. Toute référence à xEvent entraîne des échecs de validation.

## Bonnes pratiques {#best-practices}

Consultez ces règles de syntaxe avant de créer des expressions de personnalisation. La plupart des erreurs d’exécution proviennent du mélange des contextes Handlebars et PQL.

**Utilisez la syntaxe correcte du bloc conditionnel**

Utilisez toujours `{%#if%}` / `{%else if%}` / `{%else%}` / `{%/if%}`. La syntaxe `{% if %}` / `{% elseif %}` / `{% endif %}` n’est pas prise en charge.

```handlebars
{%#if profile.loyalty.tier = "gold"%}
Gold member content
{%else if profile.loyalty.tier = "silver"%}
Silver member content
{%else%}
Default content
{%/if%}
```

**N’appelez pas les fonctions PQL dans `{{...}}` blocs Handlebars**

`{{...}}` résout uniquement les variables Handlebars et les assistants ; il n’évalue pas PQL. Encapsuler une fonction PQL comme `upperCase()` dans `{{...}}` provoque une erreur « impossible de trouver un helper ». Utilisez plutôt `{%= ... %}` :

| Incorrect | Correct |
|-----------|---------|
| `{{upperCase(cleanName)}}` | `{%= upperCase(cleanName) %}` |

**Utiliser un alias de boucle nommé lors de la combinaison de `{{#each}}` avec`{%#if%}`**

`this.field` est résolu par le rendu Handlebars, mais pas par l’évaluateur PQL dans une condition de `{%#if%}`. Définissez un alias nommé avec `as |item|` afin que les deux contextes puissent résoudre le champ :

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Order {{order.id}} is pending.
  {%/if%}
{{/each}}
```

**Attribuer les résultats de la fonction PQL à une variable avant la boucle**

Les champs définis par l’utilisateur PQL tels que `topN` ne peuvent pas être appelés directement dans `{{#each}}`. Évaluez-les d’abord avec `{% let %}`, puis effectuez une itération sur le résultat :

```handlebars
{% let topOrders = topN(profile.orders, price, 3) %}
{{#each topOrders}}
  {{this.name}} — {{this.price}}&euro;
{{/each}}
```

**Utilisez `{% let %}` pour éviter de répéter les appels de fonction**

Lorsqu’une valeur calculée est nécessaire plusieurs fois, stockez-la dans une variable. Cela améliore la lisibilité et évite les évaluations redondantes :

```handlebars
{% let cleanName = replaceAll(profile.person.name.firstName, "[^a-zA-Z]", "") %}
Hi {{cleanName}}, your code is: WELCOME-{%= upperCase(cleanName) %}
```

**Utiliser l’ordre d’argument correct pour`dateDiff`**

`dateDiff(start, end)` prend la date antérieure en premier. Pour calculer le nombre de jours restants jusqu’à une date ultérieure, transmettez la date actuelle comme premier argument :

```handlebars
{% let daysLeft = dateDiff(getCurrentZonedDateTime(), stringToDate(profile.loyalty.expiryDate)) %}
```

**Utilisez `=` pour les comparaisons d’égalité dans PQL, et non`==`**.

PQL utilise un seul opérateur `=` pour l’égalité. L’utilisation de `==` entraîne une erreur de syntaxe.

**Utilisez des accents graves pour les noms de champ avec trait d’union — dans les expressions PQL uniquement**

Si un nom de champ de schéma XDM contient un trait d’union (par exemple, `order-total`), placez-le dans des accents graves pour empêcher le trait d’union d’être analysé en tant qu’opérateur de soustraction. Elle est uniquement prise en charge dans les expressions `{%= ... %}` PQL, et non dans les blocs Handlebars `{{...}}` :

```sql
{%= profile.events.`order-total` > 100 %}
```

Pour les expressions prêtes à l’emploi que vous pouvez copier directement dans votre contenu, consultez [Recettes &#x200B;](personalization-recipes.md).

## Référence rapide {#quick-reference}

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

>[!BEGINTABS]

>[!TAB Vue d’ensemble]

**TL;DR**

Cette page explique les syntaxes de personnalisation Handlebars et PQL dans Journey Optimizer : leurs règles générales, mots-clés réservés, structure de l’espace de noms, système de type et bonnes pratiques pour éviter les erreurs d’exécution courantes.

**Intentions**

* Comprendre quand utiliser la syntaxe Handlebars (`{{...}}`) ou PQL (`{%= ... %}`)
* Application de règles de syntaxe générales : caractères réservés, respect de la casse, échappement HTML, barre oblique inverse
* Échapper correctement les mots-clés réservés et les clés d’attribut spéciales (noms avec traits d’union, identifiants d’événement numériques)
* Appliquer une coercition de type lors de la comparaison ou de la transmission de valeurs de types incompatibles
* Personnalisation de référence à partir des espaces de noms disponibles : profil, audience, offres
* Suivez les bonnes pratiques pour éviter les erreurs d’exécution et de validation les plus courantes

>[!TAB Glossaire]

* **Handlebars** : syntaxe de modèle `{{...}}` utilisée pour les attributs de rendu, la boucle sur des tableaux et l’appel d’assistants de bloc ; par défaut, la sortie HTML-escapes. *(spécifique au produit)*
* **Profile Query Language (PQL)** : syntaxe d&#39;expression `{%= ... %}` utilisée pour appeler les fonctions intégrées (par exemple `upperCase()`, `formatDate()`) et évaluer les expressions conditionnelles. *(spécifique au produit)*
* **Triple-stash (`{{{ }}}`)** : variante de syntaxe Handlebars qui génère des valeurs sans échappement HTML, utile lorsque la valeur elle-même contient des caractères HTML qui ne doivent pas être codés.
* **Mots-clés réservés** : identifiants de PQL (`next`, `last`, `this`) qui ne peuvent pas être utilisés directement comme noms de champ ou de variable ; ils doivent être entourés de marques d’apostrophe lorsqu’un champ de schéma utilise l’un de ces noms.
* **Type coercition** : conversion explicite d’une valeur d’un type de données à un autre (par exemple, chaîne → nombre) à l’aide de fonctions telles que `stringToNumber()` ou `toBool()`, requises avant la comparaison ou l’arithmétique dans PQL.
* **Espace de noms** : regroupement de niveau supérieur des données de personnalisation (Profil, Audience, Offres), chacune ayant sa propre structure de chemin d’accès et ses propres règles d’accès.
* **Assistant de bloc** : assistant Handlebars identifié par `#` avant le nom de l’assistant et une `/` de fermeture correspondante, utilisé pour les constructions de bloc telles que `{{#each}}`.

>[!TAB  Terminologie ]

* **Nom canonique :** Handlebars — pour la syntaxe `{{...}}` ; PQL — pour la syntaxe `{%= ... %}`
* **Ne pas confondre :** `{{...}}` (Handlebars — rend les variables et les assistants, avec échappement HTML) ≠ `{%= ... %}` (PQL — évalue les fonctions et les expressions) ≠ `{%#if%}`/`{%/if%}` (syntaxe de bloc conditionnelle, accolades en pourcentage)
* **Ne pas confondre :** `{{profile.person.name}}` (sortie avec échappement HTML) ≠ `{{{profile.person.name}}}` (sortie avec échappement triple - sortie sans échappement)
* **Ne les confondez pas :** clé réservée avec échappement (s’applique à la fois à `{{...}}` et `{%= ... %}`) ≠ clé avec trait d’union avec échappement (uniquement pris en charge dans `{%= ... %}` expressions PQL, et non dans `{{...}}`)
* **Ne pas confondre :** `=` (opérateur d’égalité PQL — correct) ≠ `==` (PQL non valide — provoque une erreur de syntaxe)

>[!TAB Mécanismes de sécurisation et limitations]

* La variable `xEvent` n’est pas disponible dans les expressions de personnalisation ; toute référence à `xEvent` entraîne des échecs de validation.
* Les appels de fonction PQL dans `{{...}}` blocs Handlebars échoueront ; utilisez `{%= ... %}` à la place.
* La syntaxe conditionnelle `{% if %}` / `{% elseif %}` / `{% endif %}` n’est pas prise en charge ; utilisez `{%#if%}` / `{%else if%}` / `{%/if%}`.
* L’échappement avec accents graves pour les noms de champ avec trait d’union est uniquement pris en charge dans les expressions PQL (`{%= ... %}`). Dans `{{...}}`’interpolation Handlebars, la syntaxe de la bascule inverse échoue, mais les noms de champ avec trait d’union peuvent toujours être référencés directement (par exemple, `{{profile.my-custom-field}}`).
* Les mots-clés réservés (`next`, `last`, `this`) doivent être placés entre accents graves lorsqu’ils sont utilisés comme noms de champ de schéma ; s’applique à la fois à `{{...}}` et à `{%= ... %}`.
* La `\` barre oblique inverse simple n’est pas prise en charge comme argument de fonction littérale ; utilisez une `\\` barre oblique inverse double.
* Le PQL est fortement typé ; les types incompatibles dans les comparaisons ou les opérations arithmétiques nécessitent une conversion explicite à l’aide de `stringToNumber()`, `toBool()` ou de fonctions de coercition similaires.

>[!TAB FAQ]

**Q : Quand dois-je utiliser `{{...}}` plutôt que `{%= ... %}` ?**

Utilisez `{{...}}` (Handlebars) pour effectuer le rendu des valeurs d’attribut, passer en boucle sur des tableaux et appeler des assistants de blocs. Utilisez `{%= ... %}` (PQL) pour appeler des fonctions intégrées telles que `upperCase()` et `formatDate()`, et pour évaluer des expressions conditionnelles.

**Q : Comment générer une valeur sans codage HTML ?**

Utilisez le `{{{ }}}` triple stash au lieu de `{{...}}`. La sortie d’HTML-escapes Handlebars à accolade simple (par exemple, `&` devient `&amp;`) ; le triple stash contourne l’échappement.

**Q : Quel est l’opérateur d’égalité correct dans PQL ?**

Utilisez un seul `=` pour les comparaisons d’égalité dans PQL. L’utilisation de `==` est une erreur de syntaxe.

**Q : Comment référencer un champ de schéma dont le nom est un mot-clé réservé (par exemple `next`, `last`, `this`) ?**

Encapsulez-le avec des accents graves : `{{profile.person.\`next\`.name&rbrace;’. Cela s’applique à la fois aux chemins Handlebars et aux expressions PQL.

**Q : Puis-je appeler des fonctions PQL dans `{{...}}` blocs Handlebars ?**

Non. `{{...}}` résout uniquement les variables Handlebars et les helpers. Une fonction PQL dans `{{...}}` entraîne l’erreur « impossible de trouver un helper ». Utilisez `{%= functionName(...) %}` à la place.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 7fa07aa5 -->
