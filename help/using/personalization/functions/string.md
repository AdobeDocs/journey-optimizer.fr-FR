---
title: Bibliothèque de fonctions de chaîne
description: Bibliothèque de fonctions de chaîne
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: b9ebacf410f268e19bbaf1d43ee98f5376d0913f
workflow-type: tm+mt
source-wordcount: '1237'
ht-degree: 97%

---

# Fonctions de chaîne {#string}

Découvrez comment utiliser les fonctions de chaîne dans l&#39;éditeur d&#39;expression.

## Camel Case {#camelCase}

La fonction `camelCase` met en majuscule la première lettre de chaque mot d&#39;une chaîne.

**Format**

```sql
{%= camelCase(string)%}
```

**Exemple**

La fonction suivante met en majuscule la première lettre du mot de l&#39;adresse postale du profil.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## Concat {#concate}

La fonction `concat` combine deux chaînes en une seule.

**Format**

```sql
{%= concat(string,string) %}
```

**Exemple**

La fonction suivante combine la ville et le pays du profil dans une seule chaîne.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## Contains {#contains}

La fonction `contains` permet de déterminer si une chaîne contient une sous-chaîne donnée.

**Format**

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Description |
| --------- | ----------- |
| `STRING_1` | La chaîne à vérifier. |
| `STRING_2` | La chaîne à rechercher dans la première chaîne. |
| `CASE_SENSITIVE` | Un paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Valeurs possibles : true (par défaut)/false. |

**Exemples**

* La fonction suivante vérifie si le prénom du profil contient la lettre A (en majuscule ou en minuscule). Si c&#39;est le cas, elle renverra &quot;true&quot;, sinon elle renverra &quot;false&quot;.

   ```sql
   {%= contains(profile.person.name.firstName, "A", false) %}
   ```

* La requête suivante détermine si l&#39;adresse e-mail de la personne contient la chaîne « 2010@gm » en respectant la casse.

   ```sql
   {%= contains(profile.person.emailAddress,"2010@gm") %}
   ```

## Does not contain{#doesNotContain}

La fonction `doesNotContain` permet de déterminer si une chaîne ne contient pas une sous-chaîne donnée.

**Format**

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Description |
| --------- | ----------- |
| `STRING_1` | La chaîne à vérifier. |
| `STRING_2` | La chaîne à rechercher dans la première chaîne. |
| `CASE_SENSITIVE` | Un paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Valeurs possibles : true (par défaut)/false. |

**Exemple**

La requête suivante détermine si l&#39;adresse e-mail de la personne ne contient pas la chaîne « 2010@gm » en respectant la casse.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```


## Does not end with{#doesNotEndWith}

La fonction `doesNotEndWith` permet de déterminer si une chaîne ne se termine pas par une sous-chaîne donnée.

**Format**

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à rechercher dans la première chaîne. |
| `{CASE_SENSITIVE}` | Un paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Valeurs possibles : true (par défaut)/false. |

**Exemple**

La requête suivante détermine si l&#39;adresse e-mail de la personne ne se termine pas par « .com » en respectant la casse.

```sql
doesNotEndWith(person.emailAddress,".com")
```

## Does not start with{#doesNotStartWith}

La fonction `doesNotStartWith` permet de déterminer si une chaîne ne commence pas par une sous-chaîne donnée.

**Format**

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à rechercher dans la première chaîne. |
| `{CASE_SENSITIVE}` | Un paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Valeurs possibles : true (par défaut)/false. |

**Exemple**

La requête suivante détermine si le nom de la personne ne commence pas par « Joe » en respectant la casse.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

## Encode 64{#encode64}

La fonction `encode64` est utilisée pour coder une chaîne afin de conserver les informations personnelles (PI) si elles doivent être incluses, par exemple, dans une URL.

**Format**

```sql
{%= encode64(string) %}
```

## Ends with{#endsWith}

La fonction `endsWith` permet de déterminer si une chaîne se termine par une sous-chaîne donnée.

**Format**

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à rechercher dans la première chaîne. |
| `{CASE_SENSITIVE}` | Un paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Valeurs possibles : true (par défaut)/false. |

**Exemple**

La requête suivante détermine si l&#39;adresse e-mail de la personne se termine par « .com » en respectant la casse.

```sql
{%= endsWith(person.emailAddress,".com") %}
```


## Equals{#equals}

La fonction `equals` permet de déterminer si une chaîne est égale à une chaîne donnée, en respectant la casse.

**Format**

```sql
{%= equals(STRING_1, STRING_2) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à comparer à la première chaîne. |

**Exemple**

La requête suivante détermine si le nom de la personne est « John » en respectant la casse.

```sql
{%=equals(profile.person.name,"John") %}
```

## Equals Ignore Case{#equalsIgnoreCase}

La fonction `equalsIgnoreCase` permet de déterminer si une chaîne est égale à la chaîne donnée, en respectant la casse.

**Format**

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à comparer à la première chaîne. |

**Exemple**

La requête suivante détermine si le nom de la personne est « John » sans respect de la casse.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

## Extract Email Domain {#extractEmailDomain}

La fonction `extractEmailDomain` permet d&#39;extraire le domaine d&#39;une adresse e-mail.

**Format**

```sql
{%= extractEmailDomain(string) %}
```

**Exemple**

La requête suivante extrait le domaine de l&#39;adresse e-mail personnelle.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## Is empty {#isEmpty}

La fonction `isEmpty` est utilisée pour déterminer si une chaîne est vide.

**Format**

```sql
{%= isEmpty(string) %}
```

**Exemple**

La fonction suivante renvoie &quot;true&quot; si le numéro de téléphone mobile du profil est vide. Sinon, elle renverra &quot;false&quot;.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## Left trim {#leftTrim}

La fonction `leftTrim` est utilisée pour supprimer les espaces blancs au début d&#39;une chaîne.

**Format**

```sql
{%= leftTrim(string) %}
```

## Length {#length}

La fonction `length` est utilisée pour obtenir le nombre de caractères d&#39;une chaîne ou d&#39;une expression.

**Format**

```sql
{%= length(string) %}
```

**Exemple**

La fonction suivante renvoie la longueur du nom de ville du profil.

```sql
{%= length(profile.homeAddress.city) %}
```

## Like{#like}

La fonction `like` permet de déterminer si une chaîne correspond à un modèle donné.

**Format**

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | L&#39;expression à laquelle comparer la première chaîne. Les deux caractères spéciaux pris en charge pour créer une expression sont `%` et `_`. <ul><li>`%` est utilisé pour représenter aucun ou plusieurs caractères.</li><li>`_` est utilisé pour représenter exactement un caractère.</li></ul> |

**Exemple**

La requête suivante récupère toutes les villes où vivent les profils contenant le modèle &#39;&#39;es&#39;&#39;.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## Lower Case{#lower}

La fonction `lowerCase` convertit une chaîne en minuscules.

**Syntaxe**

```sql
{%= lowerCase(string) %}
```

**Exemple**

Cette fonction convertit le prénom du profil en minuscules.

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

## Matches{#matches}

La fonction `matches` permet de déterminer si une chaîne correspond à une expression régulière donnée. Reportez-vous à [ce document](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) pour plus d&#39;informations concernant les modèles correspondants dans les expressions régulières.

**Format**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Exemple**

La requête suivante détermine si le nom de la personne commence par « John » sans respect de la casse.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## Masque (#mask)

Le `Mask` est utilisée pour remplacer une partie d’une chaîne par des caractères &quot;X&quot;.

**Format**

```sql
{%= mask(string,integer,integer) %}
```

**Exemple**

La requête suivante remplace la chaîne &quot;123456789&quot; par des caractères &quot;X&quot;, à l’exception des deux premiers et derniers caractères.

```sql
{%= mask("123456789",1,2) %}
```

La requête renvoie `1XXXXXX89`.

## Not equal to{#notEqualTo}

La fonction `notEqualTo` permet de déterminer si une chaîne est différente d&#39;une chaîne donnée.

**Format**

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à comparer à la première chaîne. |

**Exemple**

La requête suivante détermine si le nom de la personne n&#39;est pas « John » en respectant la casse.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

## Regular expression group{#regexGroup}

La fonction `Group` est utilisée pour extraire des informations spécifiques en fonction de l&#39;expression régulière fournie.

**Format**

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING}` | La chaîne à vérifier. |
| `{EXPRESSION}` | L&#39;expression régulière avec laquelle comparer la première chaîne. |
| `{GROUP}` | Groupe d&#39;expressions à comparer. |

**Exemple**

La requête suivante est utilisée pour extraire le nom de domaine d&#39;une adresse e-mail.

```sql
{%= regexGroup(emailAddress,"@(\w+)", 1) %}
```

## Replace {#replace}

La fonction `replace` permet de remplacer une sous-chaîne donnée dans une chaîne par une autre sous-chaîne.

**Format**

```sql
{%= replace(string,string,string) %}
```

**Exemple**

La fonction suivante.

```sql

```


## Replace All{#replaceAll}

La fonction `replaceAll` permet de remplacer toutes les sous-chaînes d&#39;un texte correspondant à la &quot;cible&quot; par la chaîne littérale de &quot;remplacement&quot; spécifiée. Le remplacement s&#39;effectue du début à la fin de la chaîne. Par exemple, le remplacement de « aa » par « b » dans la chaîne « aaa » donnera « ba » et non « ab ».

**Format**

```sql
{%= replaceAll(string,string,string) %}
```


## Right trim {#rightTrim}

La fonction `rightTrim` est utilisée pour supprimer les espaces blancs de la fin d&#39;une chaîne.


**Format**

```sql
{%= rightTrim(string) %}
```

## Split {#split}

La fonction `split` est utilisée pour fractionner une chaîne selon un caractère donné.

**Format**

```sql
{%= split(string,string) %}
```

<!--
**Example**

The following function .

```sql

```

-->

## Starts with{#startsWith}

La fonction `startsWith` permet de déterminer si une chaîne commence par une sous-chaîne donnée.

**Format**

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à rechercher dans la première chaîne. |
| `{CASE_SENSITIVE}` | Un paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Par défaut, cette valeur est définie sur vraie. |

**Exemple**

La requête suivante détermine si le nom de la personne commence par « Joe » en respectant la casse.

```sql
{%= startsWith(person.name,"Joe") %}
```

## Title Case{#titleCase}

La fonction **titleCase** permet de mettre en majuscules les premières lettres de chaque mot d&#39;une chaîne.

**Syntaxe**

```sql
{%= titleCase(string) %}
```

**Exemple**

Si la personne vit dans Washington high street, cette fonction renverra Washington High Street.

```sql
{%= titleCase(profile.person.location.Street) %}
```

## Trim{#trim}

La fonction **trim** supprime tous les espaces blancs du début et de la fin d&#39;une chaîne.

**Syntaxe**

```sql
{%= trim(string) %}
```

## Upper Case{#upper}

La fonction **upperCase** convertit une chaîne en majuscules.

**Syntaxe**

```sql
{%= upperCase(string) %}
```

**Exemple**

Cette fonction convertit le nom du profil en majuscules.

```sql
{%= upperCase(profile.person.name.lastName) %}
```
