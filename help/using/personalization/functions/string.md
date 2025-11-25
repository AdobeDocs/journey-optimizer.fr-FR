---
title: Bibliothèque de fonctions de chaîne
description: Bibliothèque de fonctions de chaîne
feature: Personalization
topic: Personalization
role: Developer
level: Experienced
exl-id: 8674ef9e-261b-49d9-800e-367f9f7ef979
source-git-commit: 6f7b9bfb65617ee1ace3a2faaebdb24fa068d74f
workflow-type: ht
source-wordcount: '1859'
ht-degree: 100%

---

# Fonctions de chaîne {#string}

Découvrez comment utiliser les fonctions de chaîne dans l’éditeur de personnalisation.

## Casse mixte {#camelCase}

La fonction `camelCase` met en majuscule la première lettre de chaque mot d&#39;une chaîne.

**Syntaxe**

```sql
{%= camelCase(string)%}
```

**Exemple**

La fonction suivante met en majuscule la première lettre du mot de l&#39;adresse postale du profil.

```sql
{%= camelCase(profile.homeAddress.street) %}
```

## Char code at {#char-code-at}

La fonction `charCodeAt` renvoie la valeur ASCII d’un caractère, comme la fonction charCodeAt dans JavaScript. Elle prend une chaîne et un entier (qui définissent la position du caractère) comme arguments d’entrée et renvoie sa valeur ASCII correspondante.

**Syntaxe**

```sql
{%= charCodeAt(string,int) %}: int
```

**Exemple**

La fonction suivante renvoie la valeur ASCII de o, c’est-à-dire 111.

```sql
{%= charCodeAt("some", 1)%}
```

## Concat {#concate}

La fonction `concat` combine deux chaînes en une seule.

**Syntaxe**

```sql
{%= concat(string,string) %}
```

**Exemple**

La fonction suivante combine la ville et le pays du profil dans une seule chaîne.

```sql
{%= concat(profile.homeAddress.city,profile.homeAddress.country) %}
```

## Contient {#contains}

La fonction `contains` permet de déterminer si une chaîne contient une sous-chaîne donnée.

**Syntaxe**

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

## Ne contient pas{#doesNotContain}

La fonction `doesNotContain` permet de déterminer si une chaîne ne contient pas une sous-chaîne donnée.

**Syntaxe**

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


## Ne se termine pas par{#doesNotEndWith}

La fonction `doesNotEndWith` permet de déterminer si une chaîne ne se termine pas par une sous-chaîne donnée.

**Syntaxe**

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

## Ne commence pas par{#doesNotStartWith}

La fonction `doesNotStartWith` permet de déterminer si une chaîne ne commence pas par une sous-chaîne donnée.

**Syntaxe**

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

**Syntaxe**

```sql
{%= encode64(string) %}
```

## Se termine par{#endsWith}

La fonction `endsWith` permet de déterminer si une chaîne se termine par une sous-chaîne donnée.

**Syntaxe**

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


## Égal à{#equals}

La fonction `equals` permet de déterminer si une chaîne est égale à une chaîne donnée, en respectant la casse.

**Syntaxe**

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

## Égal à ignorer la casse{#equalsIgnoreCase}

La fonction `equalsIgnoreCase` permet de déterminer si une chaîne est égale à la chaîne donnée, en respectant la casse.

**Syntaxe**

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

## Extraire le domaine e-mail {#extractEmailDomain}

La fonction `extractEmailDomain` permet d&#39;extraire le domaine d&#39;une adresse e-mail.

**Syntaxe**

```sql
{%= extractEmailDomain(string) %}
```

**Exemple**

La requête suivante extrait le domaine de l&#39;adresse e-mail personnelle.

```sql
{%= extractEmailDomain(profile.personalEmail.address) %}
```

## Format currency {#format-currency}

La fonction `formatCurrency` est utilisée pour convertir n’importe quel nombre en sa représentation monétaire sensible à la langue correspondante en fonction des paramètres régionaux transmis sous forme de chaîne dans le deuxième argument.

**Syntaxe**

```sql
{%= formatCurrency(number/double,string) %}: string
```

**Exemple**

Cette requête renvoie 56.00 £.

```sql
{%= formatCurrency(56L,"en_GB") %}
```

## Obtenir l’hôte d’URL {#get-url-host}

La fonction `getUrlHost` sert à récupérer le nom d’hôte d’une URL.

**Syntaxe**

```sql
{%= getUrlHost(string) %}: string
```

**Exemple**

```sql
{%= getUrlHost("https://www.myurl.com/contact") %}
```

Renvoie « www.myurl.com »

## Obtenir le chemin d’accès à l’URL {#get-url-path}

La fonction `getUrlPath` sert à récupérer le chemin d’accès d’après le nom de domaine d’une URL.

**Syntaxe**

```sql
{%= getUrlPath(string) %}: string
```

**Exemple**

```sql
{%= getUrlPath("https://www.myurl.com/contact.html") %}
```

Renvoie « /contact.html »

## Obtenir le protocole d’URL {#get-url-protocol}

La fonction `getUrlProtocol` est utilisée pour récupérer le protocole d’une URL.

**Syntaxe**

```sql
{%= getUrlProtocol(string) %}: string
```

**Exemple**

```sql
{%= getUrlProtocol("https://www.myurl.com/contact.html") %}
```

Renvoie « http »

## Index de {#index-of}

La fonction `indexOf` est utilisée pour renvoyer la position (dans le premier argument) de la première occurrence du deuxième paramètre. Renvoie -1 s’il n’existe aucune correspondance.

**Syntaxe**

```sql
{%= indexOf(STRING_1, STRING_2) %}: integer
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | Chaîne à rechercher dans le premier paramètre |

**Exemple**

```sql
{%= indexOf("hello world","world" ) %}
```

Renvoie 6.

## Est vide {#isEmpty}

La fonction `isEmpty` permet de déterminer si une chaîne contient une chaîne est vide.

**Syntaxe**

```sql
{%= isEmpty(string) %}
```

**Exemple**

La fonction suivante renvoie &quot;true&quot; si le numéro de téléphone mobile du profil est vide. Sinon, elle renverra &quot;false&quot;.

```sql
{%= isEmpty(profile.mobilePhone.number) %}
```

## N’est pas vide {#is-not-empty}

La fonction `isNotEmpty` sert à déterminer si une chaîne n’est pas vide.

**Syntaxe**

```sql
{= isNotEmpty(string) %}: boolean
```

**Exemple**

La fonction suivante renvoie &quot;true&quot; si le numéro de téléphone mobile du profil n’est pas vide. Sinon, elle renverra &quot;false&quot;.

```sql
{%= isNotEmpty(profile.mobilePhone.number) %}
```

## Dernier index de {#last-index-of}

La fonction `lastIndexOf` est utilisée pour renvoyer la position (dans le premier argument) de la dernière occurrence du deuxième paramètre. Renvoie -1 s’il n’existe aucune correspondance.

**Syntaxe**

```sql
{= lastIndexOf(STRING_1, STRING_2) %}: integer
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | Chaîne à rechercher dans le premier paramètre |

**Exemple**

```sql
{%= lastIndexOf("hello world","o" ) %}
```

Renvoie 7.

## Supprimer à gauche {#leftTrim}

La fonction `leftTrim` est utilisée pour supprimer les espaces blancs au début d&#39;une chaîne.

**Syntaxe**

```sql
{%= leftTrim(string) %}
```

## Longueur {#length}

La fonction `length` est utilisée pour obtenir le nombre de caractères d&#39;une chaîne ou d&#39;une expression.

**Syntaxe**

```sql
{%= length(string) %}
```

**Exemple**

La fonction suivante renvoie la longueur du nom de ville du profil.

```sql
{%= length(profile.homeAddress.city) %}
```

## Comme{#like}

La fonction `like` permet de déterminer si une chaîne correspond à un modèle donné.

**Syntaxe**

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

## Minuscules{#lower}

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

## Correspond à{#matches}

La fonction `matches` permet de déterminer si une chaîne correspond à une expression régulière donnée. Reportez-vous à [ce document](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) pour plus d&#39;informations concernant les modèles correspondants dans les expressions régulières.

**Syntaxe**

```sql
{%= matches(STRING_1, STRING_2) %}
```

**Exemple**

La requête suivante détermine si le nom de la personne commence par « John » sans respect de la casse.

```sql
{%= matches(person.name.,"(?i)^John") %}
```

## Masque {#mask}

La fonction `Mask` est utilisée pour remplacer une partie d’une chaîne par des caractères « X ».

**Syntaxe**

```sql
{%= mask(string,integer,integer) %}
```

**Exemple**

La requête suivante remplace la chaîne « 123456789 » par des caractères « X », à l’exception des deux premiers et derniers caractères.

```sql
{%= mask("123456789",1,2) %}
```

La requête renvoie `1XXXXXX89`.

## MD5 {#md5}

La fonction `md5` est utilisée pour calculer et renvoyer le hachage md5 d’une chaîne.

**Syntaxe**

```sql
{%= md5(string) %}: string
```

**Exemple**

```sql
{%= md5("hello world") %}
```

Renvoie « 5eb63bbe01eeed093cb22bb8f5acdc3 »

## Différent de{#notEqualTo}

La fonction `notEqualTo` permet de déterminer si une chaîne est différente d&#39;une chaîne donnée.

**Syntaxe**

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

## Différent de Ignorer la casse {#not-equal-with-ignore-case}

La fonction `notEqualWithIgnoreCase` sert à comparer deux chaînes qui ne respectent pas la casse.

**Syntaxe**

```sql
{= notEqualWithIgnoreCase(STRING_1,STRING_2) %}: boolean
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à comparer à la première chaîne. |

**Exemple**

La requête suivante détermine si le nom de la personne n’est pas « john » sans respect de la casse.

```sql
{%= notEqualTo(profile.person.name,"john") %}
```

## Groupe d’expressions régulières{#regexGroup}

La fonction `Group` est utilisée pour extraire des informations spécifiques en fonction de l&#39;expression régulière fournie.

**Syntaxe**

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
{%= regexGroup(emailAddress,"@(\\w+)", 1) %}
```

## Remplacer {#replace}

La fonction `replace` permet de remplacer une sous-chaîne donnée dans une chaîne par une autre sous-chaîne.

**Syntaxe**

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

Renvoie « Bonjour Marc, voici votre newsletter mensuelle ! »

## Tout remplacer{#replaceAll}

La fonction `replaceAll` permet de remplacer toutes les sous-chaînes d’un texte correspondant à l’expression « RegEx » par la chaîne littérale de « remplacement » spécifiée. Les expressiones régulières (RegEx) ont une gestion spéciale de « \ » et « + », et toutes les expressions RegEx suivent la stratégie d’échappement PQL. Le remplacement s’effectue du début à la fin de la chaîne. Par exemple, le remplacement de « aa » par « b » dans la chaîne « aaa » donnera « ba » et non « ab ».

**Syntaxe**

```sql
{%= replaceAll(string,string,string) %}
```

>[!NOTE]
>
> Lorsque l’expression utilisée comme second argument est un caractère RegEx spécial, utilisez une double barre oblique inverse (`//`).  Les caractères RegEx spéciaux sont les suivants : [., +, *, ?, ^, $, (, ), [, ], {, }, |, \].
> 
> En savoir plus dans la [documentation Oracle](https://docs.oracle.com/javase/7/docs/api/java/util/regex/Pattern.html){_blank}.
>

## Supprimer à droite {#rightTrim}

La fonction `rightTrim` est utilisée pour supprimer les espaces blancs de la fin d’une chaîne.

**Syntaxe**

```sql
{%= rightTrim(string) %}
```

## SHA256 {#sha256}

La fonction `SHA256` calcule et renvoie le hachage sha256 d’une chaîne.

**Syntaxe**

```sql
{%= sha256(string) %} : string
```

**Exemple**

```sql
{%= sha256("Eliechxh")%}
```

renvoie : `0b0b207880b999adaad6231026abf87caa30760b6f326b21727b61139332257d`

## Fractionner {#split}

La fonction `split` est utilisée pour fractionner une chaîne selon un caractère donné.

**Syntaxe**

```sql
{%= split(string,string) %}
```

## Commence par{#startsWith}

La fonction `startsWith` permet de déterminer si une chaîne commence par une sous-chaîne donnée.

**Syntaxe**

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

## Chaîne en date {#string-to-date}

La fonction `stringToDate` convertit une valeur de chaîne en valeur date / heure. Elle comporte deux arguments : représentation sous forme de chaîne d’une date et d’une heure et sous forme de chaîne du formateur.

**Syntaxe**

```sql
{= stringToDate("date-time value","formatter" %}
```

**Exemple**

```sql
{= stringToDate("2023-01-10 23:13:26", "yyyy-MM-dd HH:mm:ss") %}
```

## Chaîne en entier {#string-to-integer}

La fonction `string_to_integer` est utilisée pour convertir une valeur de chaîne en valeur entière.

**Syntaxe**

```sql
{= string_to_integer(string) %}: int
```

## Chaîne en nombre {#string-to-number}

La fonction `stringToNumber` est utilisée pour convertir une chaîne en nombre. Elle renvoie la même chaîne que la sortie pour une entrée non valide.

**Syntaxe**

```sql
{%= stringToNumber(string) %}: double
```

## Sous-chaîne {#sub-string}

La fonction `Count string` est utilisée pour renvoyer la sous-chaîne de l’expression de chaîne entre l’index de début et l’index de fin.
**Syntaxe**

```sql
{= substr(string, integer, integer) %}: string
```

## Casse du titre{#titleCase}

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

## En valeur booléenne {#to-bool}

La fonction `toBool` est utilisée pour convertir une valeur d’argument en valeur booléenne, selon son type.

**Syntaxe**

```sql
{= toBool(string) %}: boolean
```

## En date/heure {#to-date-time}

La fonction `toDateTime` est utilisée pour convertir une chaîne en date. Elle renvoie la date de l’époque comme sortie pour une entrée non valide.

**Syntaxe**

```sql
{%= toDateTime(string, string) %}: date-time
```

## To Date Time Only {#to-date-time-only}

La fonction `toDateTimeOnly` est utilisée pour convertir une valeur d’argument en une valeur de date et d’heure uniquement. Elle renvoie la date de l’époque comme sortie pour une entrée non valide. Cette fonction accepte les types de champs chaîne, date, long et int.

**Syntaxe**

```sql
{%= toDateTimeOnly(string/date/long/int) %}: date-time
```

## Taille {#trim}

La fonction **trim** supprime tous les espaces blancs du début et de la fin d&#39;une chaîne.

**Syntaxe**

```sql
{%= trim(string) %}
```

## Majuscules{#upper}

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

## Décodage de l’URL {#url-decode}

La fonction `urlDecode` est utilisée pour décoder une chaîne codée en URL.

**Syntaxe**

```sql
{%= urlDecode(string) %}: string
```

## Encodage de l’URL {#url-encode}

La fonction `Count only null` est utilisée pour encoder une chaîne en URL.

**Syntaxe**

```sql
{%= urlEncode(string) %}: string
```
