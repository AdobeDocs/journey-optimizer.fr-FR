---
title: Recettes Personalization
description: Modèles de personnalisation courants et exemples concrets pour Adobe Journey Optimizer
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
feature_v2: id: fda7be7c-b81e-42c0-95a9-616e5b893c03
subfeature_v2: id: cb09dcb7-3367-4b63-b02c-8a1356eb876eid: ac5d9310-7772-40fb-9d78-864562e1bfd6
source-git-commit: 0ee10a0689d38c22b1180b197796b08a10c286cf
workflow-type: tm+mt
source-wordcount: 815
ht-degree: 0%

---

# Recettes Personalization {#personalization-recipes}

Cette page fournit des modèles de personnalisation prêts à l’emploi pour les cas d’utilisation les plus courants dans Adobe Journey Optimizer. Tous les exemples utilisent la syntaxe de l’éditeur de personnalisation et peuvent être copiés directement dans un contenu d’e-mail, de SMS ou de notification push.

Pour obtenir une référence complète des fonctions disponibles, voir [Fonctions d’assistance](functions/helpers.md), [Fonctions date/heure](functions/dates.md), [Fonctions de chaîne](functions/string.md) et [Fonctions de tableau](functions/arrays-list.md).

>[!TIP]
>
>Avant de copier des exemples, passez en revue les [bonnes pratiques de ](personalization-syntax.md#best-practices) afin d’éviter les erreurs de syntaxe les plus courantes.

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

