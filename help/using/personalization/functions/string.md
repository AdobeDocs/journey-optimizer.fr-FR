---
title: Bibliothèque de fonctions de chaîne
description: Bibliothèque de fonctions de chaîne
feature: Personalization
topic: Personalization
role: Data Engineer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: 1d9fc184bb67362aac608e9816fe3afe64eb055c
workflow-type: tm+mt
source-wordcount: '1678'
ht-degree: 0%

---

# Fonctions de chaîne {#string}

Découvrez comment utiliser les fonctions de chaîne dans l’éditeur d’expression.

## Camel Case {#camelCase}

Le `camelCase` met en majuscules la première lettre de chaque mot d’une chaîne.

**Format**

```sql
{%= camelCase(string)%}
```

**Exemple**

La fonction suivante met en majuscules la première lettre de mot de l’adresse postale du profil.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## Concat {#concate}

Le `concat` combine deux chaînes en une seule.

**Format**

```sql
{%= concat(string,string) %}
```

**Exemple**

La fonction suivante combine ville et pays du profil dans une seule chaîne.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## Contient {#contains}

Le `contains` permet de déterminer si une chaîne contient une sous-chaîne donnée.

**Format**

```sql
{%= contains(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Description |
| --------- | ----------- |
| `STRING_1` | Chaîne à vérifier. |
| `STRING_2` | Chaîne à rechercher dans la première chaîne. |
| `CASE_SENSITIVE` | Paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Valeurs possibles : true (par défaut) / false. |

**Exemples**

* La fonction suivante vérifie si le prénom du profil contient la lettre A (en majuscules ou en minuscules). Si c’est le cas, il renverra &quot;true&quot;, sinon il renverra &quot;false&quot;.

   ```sql
   {%= contains(profile.person.name.firstName, "A", false) %}
   ```

* La requête suivante détermine si l’adresse électronique de la personne contient la chaîne &quot;2010@gm&quot; en respectant la casse.

   ```sql
   {%= contains(profile.person.emailAddress,"2010@gm") %}
   ```

## Ne contient pas{#doesNotContain}

Le `doesNotContain` permet de déterminer si une chaîne ne contient pas de sous-chaîne donnée.

**Format**

```sql
{%= doesNotContain(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Description |
| --------- | ----------- |
| `STRING_1` | Chaîne à vérifier. |
| `STRING_2` | Chaîne à rechercher dans la première chaîne. |
| `CASE_SENSITIVE` | Paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Valeurs possibles : true (par défaut) / false. |

**Exemple**

La requête suivante détermine si l’adresse électronique de la personne ne contient pas la chaîne &quot;2010@gm&quot; en respectant la casse.

```sql
{%= doesNotContain(profile.person.emailAddress,"2010@gm")%}
```


## Ne se termine pas par{#doesNotEndWith}

Le `doesNotEndWith` permet de déterminer si une chaîne ne se termine pas par une sous-chaîne donnée.

**Format**

```sql
{%= doesNotEndWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne à vérifier. |
| `{STRING_2}` | Chaîne à rechercher dans la première chaîne. |
| `{CASE_SENSITIVE}` | Paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Valeurs possibles : true (par défaut) / false. |

**Exemple**

La requête suivante détermine si l’adresse électronique de la personne ne se termine pas par &quot;.com&quot; en respectant la casse.

```sql
doesNotEndWith(person.emailAddress,".com")
```

## Ne commence pas par{#doesNotStartWith}

Le `doesNotStartWith` permet de déterminer si une chaîne ne commence pas par une sous-chaîne donnée.

**Format**

```sql
{%= doesNotStartWith(STRING_1, STRING_2, CASE_SENSITIVE)%}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne à vérifier. |
| `{STRING_2}` | Chaîne à rechercher dans la première chaîne. |
| `{CASE_SENSITIVE}` | Paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Valeurs possibles : true (par défaut) / false. |

**Exemple**

La requête suivante détermine si le nom de la personne ne commence pas par &quot;Joe&quot; en respectant la casse.

```sql
{%= doesNotStartWith(person.name,"Joe")%}
```

## Encode 64{#encode64}

Le `encode64` sert à coder une chaîne afin de préserver les informations personnelles (PI) si elles doivent être incluses, par exemple dans une URL.

**Format**

```sql
{%= encode64(string) %}
```

## Se termine par{#endsWith}

Le `endsWith` permet de déterminer si une chaîne se termine par une sous-chaîne donnée.

**Format**

```sql
{%= endsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne à vérifier. |
| `{STRING_2}` | Chaîne à rechercher dans la première chaîne. |
| `{CASE_SENSITIVE}` | Paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Valeurs possibles : true (par défaut) / false. |

**Exemple**

La requête suivante détermine si l’adresse électronique de la personne se termine par &quot;.com&quot; en respectant la casse.

```sql
{%= endsWith(person.emailAddress,".com") %}
```


## Est égal à{#equals}

Le `equals` sert à déterminer si une chaîne est égale à la chaîne spécifiée, en respectant la casse.

**Format**

```sql
{%= equals(STRING_1, STRING_2) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne à vérifier. |
| `{STRING_2}` | Chaîne à comparer à la première chaîne. |

**Exemple**

La requête suivante détermine si le nom de la personne est &quot;John&quot; en respectant la casse.

```sql
{%=equals(profile.person.name,"John") %}
```

## Est égal à Ignorer la casse{#equalsIgnoreCase}

Le `equalsIgnoreCase` sert à déterminer si une chaîne est égale à la chaîne spécifiée, sans respect de la casse.

**Format**

```sql
{%= equalsIgnoreCase(STRING_1, STRING_2) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne à vérifier. |
| `{STRING_2}` | Chaîne à comparer à la première chaîne. |

**Exemple**

La requête suivante détermine si le nom de la personne est &quot;John&quot;, sans respect de la casse.

```sql
{%= equalsIgnoreCase(profile.person.name,"John") %}
```

## Extract Email Domain {#extractEmailDomain}

Le `extractEmailDomain` sert à extraire le domaine d’une adresse électronique.

**Format**

```sql
{%= extractEmailDomain(string) %}
```

**Exemple**

La requête suivante extrait le domaine de l’adresse électronique personnelle.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## Obtention de l’hôte d’URL {#get-url-host}

Le `getUrlHost` sert à récupérer le nom d’hôte d’une URL.

**Format**

```sql
{%= getUrlHost(string) %}: string
```

**Exemple**

```sql
{%= getUrlHost("http://www.myurl.com/contact") %}
```

Renvoie &quot;www.myurl.com&quot;

## Obtention du chemin d’URL {#get-url-path}

Le `getUrlPath` sert à récupérer le chemin d’accès après le nom de domaine d’une URL.

**Format**

```sql
{%= getUrlPath(string) %}: string
```

**Exemple**

```sql
{%= getUrlPath("http://www.myurl.com/contact.html") %}
```

Renvoie &quot;/contact.html&quot;

## Obtenir le protocole url {#get-url-protocol}

Le `getUrlProtocol` est utilisée pour récupérer le protocole d’une URL.

**Format**

```sql
{%= getUrlProtocol(string) %}: string
```

**Exemple**

```sql
{%= getUrlProtocol("http://www.myurl.com/contact.html") %}
```

Renvoie &quot;http&quot;

## Index de {#index-of}

Le `indexOf` est utilisée pour renvoyer la position (dans le premier argument) de la première occurrence du deuxième paramètre. Renvoie -1 s’il n’existe aucune correspondance.

**Format**

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne à vérifier. |
| `{STRING_2}` | Chaîne à rechercher dans le premier paramètre |

**Exemple**

```sql
{%= indexOf("hello world","world" ) %}
```

Renvoie 6.

## Est vide {#isEmpty}

Le `isEmpty` sert à déterminer si une chaîne est vide.

**Format**

```sql
{%= isEmpty(string) %}
```

**Exemple**

La fonction suivante renvoie &quot;true&quot; si le numéro de téléphone portable du profil est vide. Sinon, il renverra &quot;false&quot;.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## N’est pas vide {#is-not-empty}

Le `isNotEmpty` sert à déterminer si une chaîne n’est pas vide.

**Format**

```sql
{= isNotEmpty(string) %}: boolean
```

**Exemple**

La fonction suivante renvoie &quot;true&quot; si le numéro de téléphone portable du profil n’est pas vide. Sinon, il renverra &quot;false&quot;.

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

## Dernier index de {#last-index-of}

Le `lastIndexOf` est utilisée pour renvoyer la position (dans le premier argument) de la dernière occurrence du deuxième paramètre. Renvoie -1 s’il n’existe aucune correspondance.

**Format**

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne à vérifier. |
| `{STRING_2}` | Chaîne à rechercher dans le premier paramètre |

**Exemple**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

Renvoie 7.

## Rognage gauche {#leftTrim}

Le `leftTrim` sert à supprimer les espaces blancs au début d’une chaîne.

**Format**

```sql
{%= leftTrim(string) %}
```

## Longueur {#length}

Le `length` est utilisée pour obtenir le nombre de caractères d’une chaîne ou d’une expression.

**Format**

```sql
{%= length(string) %}
```

**Exemple**

La fonction suivante renvoie la longueur du nom de ville du profil.

```sql
{%= length(profile.homeAddress.city) %}
```

## Comme{#like}

Le `like` sert à déterminer si une chaîne correspond à un modèle spécifié.

**Format**

```sql
{%= like(STRING_1, STRING_2) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne à vérifier. |
| `{STRING_2}` | L’expression à faire correspondre à la première chaîne. Deux caractères spéciaux sont pris en charge pour créer une expression : `%` et `_`. <ul><li>`%` est utilisé pour représenter zéro ou plusieurs caractères.</li><li>`_` est utilisé pour représenter exactement un caractère.</li></ul> |

**Exemple**

La requête suivante récupère toutes les villes où résident les profils contenant le modèle &quot;es&quot;.

```sql
{%= like(profile.homeAddress.city, "%es%")%}
```

## Minuscule{#lower}

Le `lowerCase` convertit une chaîne en minuscules.

**Syntaxe**

```sql
{%= lowerCase(string) %}
```

**Exemple**

Cette fonction convertit le prénom du profil en minuscules.

```sql
{%= lowerCase(profile.person.name.firstName) %}
```

## Correspond à{#matches}

Le `matches` sert à déterminer si une chaîne correspond à une expression régulière spécifique. Reportez-vous à la section [ce document](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) pour plus d’informations sur les modèles correspondants dans les expressions régulières.

**Format**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Exemple**

La requête suivante détermine si le nom de la personne commence par &quot;John&quot; sans tenir compte de la casse.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## Masque {#mask}

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

## MD5 {#md5}

Le `md5` est utilisée pour calculer et renvoyer le hachage md5 d’une chaîne.

**Format**

```sql
{%= md5(string) %}: string
```

**Exemple**

```sql
{%= md5("hello world") %}
```

Renvoie &quot;5eb63bbe01eeed093cb22bb8f5acdc3&quot;

## Différent de{#notEqualTo}

Le `notEqualTo` sert à déterminer si une chaîne n’est pas égale à la chaîne spécifiée.

**Format**

```sql
{%= notEqualTo(STRING_1, STRING_2) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne à vérifier. |
| `{STRING_2}` | Chaîne à comparer à la première chaîne. |

**Exemple**

La requête suivante détermine si le nom de la personne n’est pas &quot;John&quot; en respectant la casse.

```sql
{%= notEqualTo(profile.person.name,"John") %}
```

## Différent De La Case Ignorer {#not-equal-with-ignore-case}

Le `notEqualWithIgnoreCase` sert à comparer deux chaînes qui ne respectent pas la casse.

**Format**

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne à vérifier. |
| `{STRING_2}` | Chaîne à comparer à la première chaîne. |

**Exemple**

La requête suivante détermine si le nom de la personne n’est pas &quot;jean&quot;, sans respect de la casse.

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

## Groupe d’expressions régulières{#regexGroup}

Le `Group` sert à extraire des informations spécifiques, en fonction de l’expression régulière fournie.

**Format**

```sql
{%= regexGroup(STRING, EXPRESSION, GROUP) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING}` | Chaîne à vérifier. |
| `{EXPRESSION}` | L’expression régulière à faire correspondre à la première chaîne. |
| `{GROUP}` | Groupe d’expressions à comparer. |

**Exemple**

La requête suivante est utilisée pour extraire le nom de domaine d’une adresse électronique.

```sql
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

## Remplacer {#replace}

Le `replace` sert à remplacer une sous-chaîne donnée d’une chaîne par une autre sous-chaîne.

**Format**

```sql
{%= replace(STRING_1,STRING_2,STRING_3) %}:string
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne dans laquelle la sous-chaîne doit être remplacée. |
| `{STRING_2}` | Sous-chaîne à remplacer. |
| `{STRING_3}` | Sous-chaîne de remplacement. |

**Exemple**

```sql
{%= replace("Hello John, here is your monthly newsletter!","John","Mark") %}
```

Renvoie &quot;Hello Mark, voici votre newsletter mensuelle !&quot;

## Tout remplacer{#replaceAll}

Le `replaceAll` sert à remplacer toutes les sous-chaînes d’un texte correspondant à &quot;target&quot; par la chaîne littérale &quot;remplacement&quot; spécifiée. Le remplacement s’effectue du début à la fin de la chaîne, par exemple, le remplacement de &quot;aa&quot; par &quot;b&quot; dans la chaîne &quot;aaa&quot; générera &quot;ba&quot; plutôt que &quot;ab&quot;.

**Format**

```sql
{%= replaceAll(string,string,string) %}
```

## Rognage droit {#rightTrim}

Le `rightTrim` est utilisée pour supprimer les espaces blancs de la fin d’une chaîne.

**Format**

```sql
{%= rightTrim(string) %}
```

## Partage {#split}

Le `split` sert à fractionner une chaîne selon un caractère donné.

**Format**

```sql
{%= split(string,string) %}
```

## Commence par{#startsWith}

Le `startsWith` permet de déterminer si une chaîne commence par une sous-chaîne donnée.

**Format**

```sql
{%= startsWith(STRING_1, STRING_2, CASE_SENSITIVE) %}
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne à vérifier. |
| `{STRING_2}` | Chaîne à rechercher dans la première chaîne. |
| `{CASE_SENSITIVE}` | Paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Par défaut, cette valeur est définie sur true. |

**Exemple**

La requête suivante détermine si le nom de la personne commence par &quot;Joe&quot; en respectant la casse.

```sql
{%= startsWith(person.name,"Joe") %}
```

## Chaîne à entier {#string-to-integer}

Le `string_to_integer` est utilisée pour convertir une valeur de chaîne en valeur entière.

**Format**

```sql
{= string_to_integer(string) %}: int
```

## Chaîne à nombre {#string-to-number}

Le `stringToNumber` est utilisée pour convertir une chaîne en nombre. Elle renvoie la même chaîne que la sortie pour une entrée non valide.

**Format**

```sql
{%= stringToNumber(string) %}: double
```

## Sous-chaîne {#sub-string}

Le `Count string` est utilisée pour renvoyer la sous-chaîne de l’expression de chaîne entre l’index de début et l’index de fin.
**Format**

```sql
{= substr(string, integer, integer) %}: string
```

## Cas de titre{#titleCase}

Le **titleCase** sert à mettre en majuscules les premières lettres de chaque mot d’une chaîne.

**Syntaxe**

```sql
{%= titleCase(string) %}
```

**Exemple**

Si la personne vit dans Washington high street, cette fonction renverra Washington High Street.

```sql
{%= titleCase(profile.person.location.Street) %}
```

## À Bool {#to-bool}

Le `toBool` est utilisée pour convertir une valeur d’argument en valeur booléenne, selon son type.

**Format**

```sql
{= toBool(string) %}: boolean
```

## Heure de la date {#to-date-time}

Le `toDateTime` est utilisée pour convertir une chaîne en date. Elle renvoie la date de l’époque comme sortie pour une entrée non valide.

**Format**

```sql
{%= toDateTime(string, string) %}: date-time
```

## À date seule {#to-date-time-only}

Le `toDateTimeOnly` est utilisée pour convertir une valeur d’argument en une valeur de date et d’heure uniquement. Elle renvoie la date de l’époque comme sortie pour une entrée non valide.

**Format**

```sql
{%= toDateTimeOnly(string) %}: date-time
```

## Rogner{#trim}

Le **trim** supprime tous les espaces blancs du début et de la fin d’une chaîne.

**Syntaxe**

```sql
{%= trim(string) %}
```

## majuscule{#upper}

Le **upperCase** convertit une chaîne en majuscules.

**Syntaxe**

```sql
{%= upperCase(string) %}
```

**Exemple**

Cette fonction convertit le nom du profil en majuscules.

```sql
{%= upperCase(profile.person.name.lastName) %}
```

## décodage de l’url {#url-decode}

Le `urlDecode` est utilisée pour décoder une chaîne codée en url.

**Format**

```sql
{%= urlDecode(string) %}: string
```

## Encode d&#39;URL {#url-encode}

Le `Count only null` est utilisée pour encoder une chaîne en URL.

**Format**

```sql
{%= urlEncode(string) %}: string
```
