---
title: Recettes de personnalisation
description: Modèles de personnalisation courants et exemples concrets pour Adobe Journey Optimizer
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
feature_v2:
  - id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2:
  - id: cb09dcb7-3367-4b63-b02c-8a1356eb876e
  - id: ac5d9310-7772-40fb-9d78-864562e1bfd6
source-git-commit: 18067b68e09b98e616126dd40b8ad729233c49fa
workflow-type: tm+mt
source-wordcount: 1530
ht-degree: 0%

---

# Recettes de personnalisation {#personalization-recipes}

>[!BEGINSHADEBOX]

**Sur cette page :** recherchez des recettes de personnalisation prêtes à l’emploi pour les dates, les tableaux, les chaînes, la logique conditionnelle et les cas Edge de PQL que vous pouvez copier directement dans votre contenu Adobe Journey Optimizer.

>[!ENDSHADEBOX]

Cette page fournit des modèles de personnalisation prêts à l’emploi pour les cas d’utilisation les plus courants dans Adobe Journey Optimizer. Tous les exemples utilisent la syntaxe de l’éditeur de personnalisation et peuvent être copiés directement dans un contenu d’e-mail, de SMS ou de notification push.

Pour obtenir une référence complète des fonctions disponibles, voir [Fonctions d’assistance](functions/helpers.md), [Fonctions date/heure](functions/dates.md), [Fonctions de chaîne](functions/string.md) et [Fonctions de tableau](functions/arrays-list.md).

>[!TIP]
>
>Avant de copier des exemples, passez en revue les [bonnes pratiques de &#x200B;](personalization-syntax.md#best-practices) afin d’éviter les erreurs de syntaxe les plus courantes.

## Recettes de date et d’heure {#date-time-recipes}

### Recette 1 — Afficher la date courante dans un format lisible {#recipe-current-date}

Utilisez `formatDate` avec `getCurrentZonedDateTime()` pour effectuer le rendu de la date d’aujourd’hui dans n’importe quel format :

```sql
{%= formatDate(getCurrentZonedDateTime(), "MMMM dd, yyyy") %}
```

Sortie (exemple) : `April 11, 2026`

**Modèles de format courants :**

| Motif | Exemple en sortie |
|---------|---------------|
| `"dd/MM/yyyy"` | `11/04/2026` |
| `"MM/dd/yyyy"` | `04/11/2026` |
| `"EEEE, MMMM dd"` | `Saturday, April 11` |
| `"yyyy-MM-dd"` | `2026-04-11` |

>[!NOTE]
>
>Utilisez des `y` minuscules (année civile) plutôt que des `Y` (année basée sur une semaine) pour éviter des résultats inattendus aux limites de l’année. Voir [caractères de motif](functions/dates.md#pattern-characters) pour une référence complète.

### Recette 2 — Compte à rebours jusqu&#39;à une date d&#39;expiration ou d&#39;événement {#recipe-countdown}

Utilisez `dateDiff` pour calculer le nombre de jours restants jusqu’à l’attribut de date de profil, puis effectuez son rendu dynamique :

```handlebars
{% let daysLeft = dateDiff(getCurrentZonedDateTime(), stringToDate(profile.loyalty.expiryDate)) %}
{%#if daysLeft > 0%}
Your reward points expire in {{daysLeft}} day{%#if daysLeft > 1%}s{%/if%}. Use them before they're gone!
{%else%}
Your reward points have expired.
{%/if%}
```

Sortie (exemple) : `Your reward points expire in 7 days. Use them before they're gone!`

### Recette 3 — X jours avant une date de fin dynamique {#recipe-days-before}

Pour calculer une date qui précède de X jours un attribut de profil (par exemple pour y faire référence dans le contenu ou les lignes d’objet), utilisez `addDays` avec un décalage négatif :

```sql
{%= formatDate(addDays(stringToDate(profile.subscription.endDate), -7), "MMMM dd, yyyy") %}
```

Sortie (exemple) : `April 04, 2026` *(7 jours avant le 11 avril)*

Pour également définir une heure fixe dans la journée (par exemple, 9 h), combinez avec `setHours` :

```sql
{%= formatDate(setHours(addDays(stringToDate(profile.subscription.endDate), -7), 9), "dd/MM/yyyy HH:mm") %}
```

### Recette 4 — Afficher l&#39;heure actuelle sous la forme HH:MM uniquement {#recipe-time-only}

Utilisez `extractHours` et `extractMinutes` pour n’afficher que la partie temporelle, avec une protection zéro au début pendant minutes :

```handlebars
{% let h = extractHours(getCurrentZonedDateTime()) %}
{% let m = extractMinutes(getCurrentZonedDateTime()) %}
Your appointment is at {{h}}:{%#if m < 10%}0{%/if%}{{m}}.
```

Sortie (exemple) : `Your appointment is at 14:05.`

### Recette 5 — Détecter le week-end par rapport au jour de la semaine {#recipe-weekend}

Utilisez `dayOfWeek` pour adapter le contenu en fonction de la journée. La fonction renvoie 1 (lundi) à 7 (dimanche). Utilisez l&#39;opérateur `=` unique (syntaxe PQL, non `==`) :

```handlebars
{%#if dayOfWeek(getCurrentZonedDateTime()) = 6 or dayOfWeek(getCurrentZonedDateTime()) = 7%}
We're closed on weekends — our team will follow up on the next business day.
{%else%}
Our team will get back to you within 24 hours.
{%/if%}
```

>[!NOTE]
>
>`dayOfWeek()` sert à adapter le **contenu** en fonction de la journée. Pour acheminer les profils différemment dans un parcours en fonction du jour de la semaine, utilisez l’option intégrée **Condition de temps → Jour de la semaine** dans l’activité Condition du parcours . [En savoir plus](../building-journeys/condition-activity.md#date_condition)

## Recettes de tableau et de boucle {#array-recipes}

### Recette 6 — Répertorier tous les éléments d&#39;un tableau de profils {#recipe-list-items}

Utilisez `{{#each}}` pour effectuer une itération sur un tableau de profils et effectuer le rendu de chaque élément. Cette option est disponible uniquement dans l’éditeur de personnalisation (e-mail, SMS, notification push) :

```handlebars
{{#each profile.purchases.recentItems}}
  - {{this.name}}: {{this.price}}&euro;
{{/each}}
```

Sortie (exemple) :

```
- Running shoes: 89&euro;
- Water bottle: 15&euro;
- Gym bag: 45&euro;
```

>[!NOTE]
>
>`{{#each}}` n’est pas pris en charge dans l’activité de condition de parcours. Pour le filtrage de tableau dans des conditions, utilisez [fonctions de gestion des collections](../building-journeys/expression/collection-management-functions.md).

### Recette 7 — Afficher les N premiers éléments d&#39;un tableau par prix {#recipe-first-n}

Utilisez `topN` pour trier et récupérer les N premiers éléments par un champ numérique. Comme `topN` est une fonction PQL, affectez-la d’abord à une variable avec `{% let %}`, puis bouclez avec `{{#each}}` :

```handlebars
{% let topOrders = topN(profile.orders, price, 3) %}
{{#each topOrders}}
  {{this.name}} — {{this.price}}&euro;
{{/each}}
```

>[!NOTE]
>
>`topN(profile.orders, price, 3)` trie les commandes par `price` dans l’ordre décroissant et renvoie les 3 premiers éléments ; il ne renvoie pas simplement les 3 premiers éléments dans l’ordre du tableau d’origine.

Ou utilisez `head` pour obtenir uniquement le premier élément :

```sql
{%= head(profile.purchases.recentItems).name %}
```

### Recette 8 — Effectuer un rendu conditionnel du contenu par élément de tableau {#recipe-conditional-loop}

Utilisez des `{%#if%}` à l’intérieur des `{{#each}}` pour effectuer le rendu de la sortie uniquement pour les éléments correspondants. Définissez un alias de boucle avec `as |order|` afin que l’évaluateur PQL puisse résoudre la référence d’attribut dans la condition :

```handlebars
{{#each profile.orders as |order|}}
  {%#if order.status = "pending"%}
  Order {{order.id}} is pending — we'll notify you when it ships.
  {%/if%}
{{/each}}
```

>[!NOTE]
>
>`this.status` fonctionne dans les expressions Handlebars mais n’est pas résolu par l’évaluateur PQL dans `{%#if%}`. L’utilisation d’un alias de boucle nommé (par exemple, `order`) rend l’attribut disponible pour les contextes Handlebars et PQL.

## Recettes de chaînes et de formatage {#string-recipes}

### Recette 9 — Nettoyer une chaîne avec replaceAll et la réutiliser {#recipe-replaceall-reuse}

`replaceAll` renvoie une nouvelle valeur — elle ne modifie pas l’original. Utilisez `{% let %}` pour stocker le résultat et le référencer plusieurs fois sans répéter l’appel de la fonction :

```handlebars
{% let cleanName = replaceAll(profile.person.name.firstName, "[^a-zA-Z]", "") %}
Hi {{cleanName}},
Your exclusive code is: WELCOME-{%= upperCase(cleanName) %}
```

Sortie (exemple) :

```
Hi John,
Your exclusive code is: WELCOME-JOHN
```

### Recette 10 — Guillemet double une valeur dans la sortie JSON {#recipe-json-quotes}

Pour inclure un guillemet double littéral dans une chaîne (par exemple, générer un fichier JSON pour une payload personnalisée), insérez une barre oblique inverse (`\"`) dans l’échappement :

```handlebars
{ "greeting": "Hello \"{{profile.person.name.firstName}}\"" }
```

Sortie : `{ "greeting": "Hello \"John\"" }`

### Recette 11 — Mettre en forme un composant de date en majuscules {#recipe-uppercase-date}

Combinez des `formatDate` avec des `upperCase` pour effectuer le rendu des noms des mois ou des jours en majuscules :

```sql
{%= upperCase(formatDate(getCurrentZonedDateTime(), "MMMM")) %}
```

Sortie (exemple) : `APRIL`

Pour une chaîne de date en majuscules complète :

```sql
{%= upperCase(formatDate(profile.person.birthDateTime, "EEEE MMMM dd yyyy")) %}
```

Sortie (exemple) : `WEDNESDAY JANUARY 01 2020`

## Recettes de logique conditionnelle {#conditional-recipes}

### Recette 12 — IF/ELSEIF/ELSE dans le contenu personnalisé {#recipe-if-elseif}

Utilisez `{%#if%}`, `{%else if%}` et `{%else%}` pour la logique conditionnelle à plusieurs branches. Ce modèle fonctionne dans le contenu et les fragments des e-mails :

```handlebars
{%#if profile.loyalty.tier = "gold"%}
As a Gold member, enjoy free shipping on all orders.
{%else if profile.loyalty.tier = "silver"%}
As a Silver member, enjoy free shipping on orders over &euro;50.
{%else%}
Join our loyalty program to unlock exclusive benefits.
{%/if%}
```

### Recette 13 — Affichage des attributs de sécurité NULL {#recipe-null-safe}

Utilisez une version de secours conditionnelle pour éviter de rendre des valeurs vides lorsqu’un attribut de profil peut être nul ou manquant :

```handlebars
{%#if profile.person.name.firstName%}
Hi {{profile.person.name.firstName}},
{%else%}
Hi there,
{%/if%}
```

Ou inséré avec un modèle de style ternaire à l’aide de `isEmpty` :

```handlebars
Hi {%#if isEmpty(profile.person.name.firstName)%}valued customer{%else%}{{profile.person.name.firstName}}{%/if%},
```

## Recettes de cas Edge de PQL {#pql-edge-cases}

### Recette 14 — Référencer une clé d&#39;attribut avec trait d&#39;union {#recipe-hyphenated-key}

Si le nom de votre champ de schéma XDM contient des traits d’union (par exemple, `order-total`, `event-type`), placez-le dans des accents graves dans une expression PQL pour empêcher que le trait d’union ne soit interprété comme un opérateur de soustraction :

```sql
{%= profile.events.`order-total` > 100 %}
```

>[!NOTE]
>
>Les accents graves ne sont pris en charge que dans les expressions PQL (`{%= ... %}`). Ils ne sont pas acceptés dans l&#39;interpolation simple Handlebars (`{{...}}`). Si vous devez effectuer directement le rendu d’une valeur de champ avec trait d’union, évaluez-la via une expression PQL ou stockez-la dans une variable à l’aide de `{% let %}`.

### Recette 15 — Référencer un identifiant d&#39;événement numérique dans un attribut de contexte {#recipe-numeric-event-id}

Lors de l’utilisation d’un événement de contexte de parcours dont l’ID est une chaîne numérique (par exemple, `1697323153`), placez l’ID entre majuscules et utilisez `{% let %}` avec `toDateTime()` et `formatDate()` :

```handlebars
{% let appointmentDate = formatDate(toDateTime(context.journey.events.`1697323153`.timestamp), "dd/MM/yyyy HH:mm") %}
Your appointment: {{appointmentDate}}
```

Sortie (exemple) : `Your appointment: 18/03/2026 14:30`

### Recette 16 — Type coercition : comparez un champ de chaîne à un nombre {#recipe-type-coercion}

PQL est fortement typé. Lorsqu’un champ de profil est stocké sous la forme d’une chaîne, mais que vous devez le comparer numériquement, convertissez-le d’abord avec `stringToNumber()` :

```sql
{%= stringToNumber(profile.loyalty.pointsBalance) > 500 %}
```

Pour les champs booléens stockés sous forme de chaînes :

```sql
{%= toBool(profile.consents.email.val) = true %}
```

## Référence rapide {#quick-reference}

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

>[!BEGINTABS]

>[!TAB Vue d’ensemble]

**TL;DR**

Cette page fournit 16 recettes de personnalisation de copier-coller prêtes à l’emploi, couvrant les dates, les tableaux, les chaînes, la logique conditionnelle et les cas Edge de PQL, à utiliser dans les e-mails, SMS et contenus push Journey Optimizer.

**Intentions**

* Copier des modèles de date et d’heure prêts à l’emploi (date actuelle, compte à rebours, dates décalées, affichage de l’heure, détection du week-end)
* Copier des modèles de tableau et de boucle (éléments de liste, N premiers éléments, rendu conditionnel par élément)
* Copier des modèles de formatage de chaîne (nettoyer et réutiliser des chaînes, guillemets JSON, composants de date en majuscules)
* Copier des modèles logiques conditionnels (affichage d’attributs multi-branches if/elseif/else, nuls et sécurisés)
* Gérer les cas Edge de PQL (clés avec tirets, identifiants d’événement numériques, coercition de type)

>[!TAB Glossaire]

* **Recette Personalization** : modèle de copier-coller prêt à l’emploi pour un cas d’utilisation de personnalisation courant, à l’aide de la syntaxe de l’éditeur de personnalisation. *(spécifique au produit)*
* **`formatDate`** : fonction qui convertit une date en chaîne à l’aide d’un modèle de format spécifié (par exemple, `"MMMM dd, yyyy"`).
* **`dateDiff`** : fonction qui calcule la différence numérique entre deux dates.
* **`getCurrentZonedDateTime()`** : fonction renvoyant la date et l’heure actuelles dans un format prenant en compte le fuseau horaire.
* **`topN`** : une fonction PQL qui trie un tableau en fonction d’un champ numérique spécifié dans l’ordre décroissant et renvoie les N premiers éléments. Doit être attribué via `{% let %}` avant utilisation dans une boucle Handlebars.
* **`{% let %}`** : syntaxe d’affectation de variable Handlebars pour le stockage des valeurs calculées ; cette syntaxe est requise lorsqu’un résultat de fonction PQL doit être référencé dans un contexte Handlebars suivant.
* **`replaceAll`** : fonction de chaîne qui remplace toutes les occurrences d’un modèle dans une chaîne ; renvoie une nouvelle chaîne sans modifier l’original.

>[!TAB  Terminologie ]

* **Nom canonique :** recette de personnalisation — variantes : motif, modèle, exemple, motif de copier-coller
* **Ne pas confondre :** `{%= ... %}` (syntaxe de l’expression PQL — évaluée, renvoie une valeur calculée) ≠ `{{...}}` (interpolation Handlebars — effectue le rendu d’une variable ou d’une expression de modèle)
* **Ne pas confondre :** `{%#if%}` / `{%/if%}` (syntaxe conditionnelle de Journey Optimizer, accolades en pourcentage) ≠ `{{#if}}` / `{{/if}}` (syntaxe conditionnelle de Handlebars standard)
* **Ne pas confondre :** `topN(array, field, n)` (trie par champ décroissant, renvoie N premiers) ≠ `head(array)` (renvoie uniquement le premier élément du tableau)
* **Ne pas confondre :** `dayOfWeek()` (utilisée dans le contenu du message pour adapter l’affichage en fonction du jour) ≠ l’option de condition d’heure du parcours « Jour de la semaine » (utilisée dans l’activité Condition de parcours pour acheminer différemment les profils)
* **À ne pas confondre :** modèle de format de date `y` (année civile — correct) ≠ `Y` (année basée sur la semaine — peut produire des résultats inattendus aux limites de l’année)

>[!TAB Mécanismes de sécurisation et limitations]

* `{{#each}}` n’est pas pris en charge dans l’activité de condition de parcours. Utilisez les fonctions de gestion de collections pour le filtrage de tableaux dans des conditions de parcours.
* L’échappement des accents graves pour les clés d’attribut avec trait d’union n’est pris en charge que dans les expressions PQL (`{%= ... %}`) ; les accents graves ne sont pas acceptés dans l’interpolation Handlebars simple (`{{...}}`).
* `topN` est une fonction PQL qui doit être affectée à une variable `{% let %}` avant d’être utilisée comme cible de boucle `{{#each}}`.
* Lors de l’utilisation d’une variable de boucle dans un bloc de `{%#if%}`, déclarez un alias de boucle nommé (par exemple, `as |order|`) ; `this.status` n’est pas résolu par l’évaluateur PQL dans `{%#if%}`.
* Utilisez des `y` en minuscules dans les modèles de `formatDate` pour l’année civile. `Y` (année basée sur la semaine) peut produire des valeurs inattendues aux limites de fin d’année.

>[!TAB FAQ]

**Q : Quelle est la différence entre `{%= ... %}` et `{{...}}` dans la personnalisation ?**

`{%= ... %}` est la syntaxe de l&#39;expression PQL — elle est évaluée et renvoie une valeur calculée (nombre, chaîne, booléen). `{{...}}` est l’interpolation Handlebars ; elle effectue le rendu d’une variable ou d’une expression de modèle. Les deux apparaissent dans le contenu de personnalisation, mais servent des objectifs différents.

**Q : Comment utiliser un résultat de fonction PQL dans une boucle de `{{#each}}` Handlebars ?**

Attribuez le résultat de la fonction PQL à une variable à l’aide de `{% let variableName = pqlFunction(...) %}`, puis utilisez `{{#each variableName}}` pour effectuer une itération sur celle-ci.

**Q : Peut-`{{#each}}` être utilisé dans une activité de condition de parcours ?**

Non. `{{#each}}` est disponible uniquement dans le contenu de personnalisation des messages (e-mail, SMS, notification push). Pour le filtrage de tableau dans des conditions de parcours, utilisez les fonctions de gestion des collections.

**Q : Comment référencer un champ dont le nom contient un trait d’union ?**

Encapsulez la clé avec trait d’union avec les accents graves dans une expression PQL : ``{%= profile.events.`order-total` > 100 %}``. Les accents graves ne sont pas pris en charge dans l’interpolation simple Handlebars. Utilisez une variable `{% let %}` comme étape intermédiaire si nécessaire.

**Q : Pourquoi `topN` a-t-il besoin de `{% let %}` avant une `{{#each}}` boucle ?**

`topN` est une fonction PQL qui renvoie une liste PQL. Son affectation à une variable `{% let %}` rend le résultat disponible dans le contexte Handlebars afin qu’il puisse être itéré avec `{{#each}}`.

>[!ENDTABS]

<!-- ai-section-version: 1 | source-hash: 20c7ee0f -->

