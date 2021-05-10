---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
translation-type: tm+mt
source-git-commit: 2cd1a6cfede96bd1afb0b3f784d20cda5ebc6cb7
workflow-type: tm+mt
source-wordcount: '747'
ht-degree: 7%

---

# Fonctions de chaîne {#string}

![](../../assets/do-not-localize/badge.png)


TBC CJM, fonctions de chaîne

## Comme{#like}

La fonction `like` est utilisée pour déterminer si une chaîne correspond à un modèle spécifié.

**Format**

```sql
like ({STRING_1},{STRING_2})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne sur laquelle effectuer la vérification. |
| `{STRING_2}` | Expression à comparer à la première chaîne. Deux caractères spéciaux sont pris en charge pour créer une expression : `%` et `_`. <ul><li>`%` est utilisée pour représenter zéro ou plusieurs caractères.</li><li>`_` est utilisé pour représenter exactement un caractère.</li></ul> |

**Exemple**

La requête suivante récupère toutes les villes contenant le modèle &quot;es&quot;.

```sql
like (city ,"%es%")
```

## Commence par{#startsWith}

La fonction `startsWith` est utilisée pour déterminer si une chaîne est début avec une sous-chaîne spécifiée.

**Format**

```sql
startsWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne sur laquelle effectuer la vérification. |
| `{STRING_2}` | Chaîne à rechercher dans la première chaîne. |
| `{BOOLEAN}` | Paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Par défaut, cette valeur est définie sur true. |

**Exemple**

La requête suivante détermine, en tenant compte de la casse, si le nom de la personne est début avec &quot;Joe&quot;.

```sql
startsWith(person.name,"Joe")
```

## Ne commence pas par{#doesNotStartWith}

La fonction `doesNotStartWith` est utilisée pour déterminer si une chaîne ne se début pas avec une sous-chaîne spécifiée.

**Format**

```sql
doesNotStartWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne sur laquelle effectuer la vérification. |
| `{STRING_2}` | Chaîne à rechercher dans la première chaîne. |
| `{BOOLEAN}` | Paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Par défaut, cette valeur est définie sur true. |

**Exemple**

La requête suivante détermine, en tenant compte de la casse, si le nom de la personne ne s’début pas avec &quot;Joe&quot;.

```sql
doesNotStartWith(person.name,"Joe")
```

## Se termine par {#endsWith}

La fonction `endsWith` permet de déterminer si une chaîne se termine par une sous-chaîne spécifiée.

**Format**

```sql
endsWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne sur laquelle effectuer la vérification. |
| `{STRING_2}` | Chaîne à rechercher dans la première chaîne. |
| `{BOOLEAN}` | Paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Par défaut, cette valeur est définie sur true. |

**Exemple**

La requête suivante détermine, en respectant la casse, si l’adresse électronique de la personne se termine par &quot;.com&quot;.

```sql
endsWith(person.emailAddress,".com")
```

## Ne se termine pas par {#doesNotEndWith}

La fonction `doesNotEndWith` permet de déterminer si une chaîne ne se termine pas par une sous-chaîne spécifiée.

**Format**

```sql
doesNotEndWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne sur laquelle effectuer la vérification. |
| `{STRING_2}` | Chaîne à rechercher dans la première chaîne. |
| `{BOOLEAN}` | Paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Par défaut, cette valeur est définie sur true. |

**Exemple**

La requête suivante détermine, en respectant la casse, si l’adresse électronique de la personne ne se termine pas par &quot;.com&quot;.

```sql
doesNotEndWith(person.emailAddress,".com")
```

## Contient{#contains}

La fonction `contains` est utilisée pour déterminer si une chaîne contient une sous-chaîne spécifiée.

**Format**

```sql
contains({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne sur laquelle effectuer la vérification. |
| `{STRING_2}` | Chaîne à rechercher dans la première chaîne. |
| `{BOOLEAN}` | Paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Par défaut, cette valeur est définie sur true. |

**Exemple**

La requête suivante détermine, en respectant la casse, si l’adresse électronique de la personne contient la chaîne &quot;2010@gm&quot;.

```sql
contains(person.emailAddress,"2010@gm")
```

## Ne contient pas{#doesNotContain}

La fonction `doesNotContain` permet de déterminer si une chaîne ne contient pas de sous-chaîne spécifiée.

**Format**

```sql
doesNotContain({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne sur laquelle effectuer la vérification. |
| `{STRING_2}` | Chaîne à rechercher dans la première chaîne. |
| `{BOOLEAN}` | Paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Par défaut, cette valeur est définie sur true. |

**Exemple**

La requête suivante détermine, en respectant la casse, si l’adresse électronique de la personne ne contient pas la chaîne &quot;2010@gm&quot;.

```sql
doesNotContain(person.emailAddress,"2010@gm")
```

## Est égal à{#equals}

La fonction `equals` est utilisée pour déterminer si une chaîne est égale à la chaîne spécifiée.

**Format**

```sql
equals({STRING_1},{STRING_2})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne sur laquelle effectuer la vérification. |
| `{STRING_2}` | Chaîne à comparer à la première chaîne. |

**Exemple**

La requête suivante détermine, en tenant compte de la casse, si le nom de la personne est &quot;John&quot;.

```sql
equals(person.name,"John")
```

## Différent de{#notEqualTo}

La fonction `notEqualTo` est utilisée pour déterminer si une chaîne n&#39;est pas égale à la chaîne spécifiée.

**Format**

```sql
notEqualTo({STRING_1},{STRING_2})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | Chaîne sur laquelle effectuer la vérification. |
| `{STRING_2}` | Chaîne à comparer à la première chaîne. |

**Exemple**

La requête suivante détermine, en tenant compte de la casse, si le nom de la personne n’est pas &quot;John&quot;.

```sql
notEqualTo(person.name,"John")
```

## Correspond à {#matches}

La fonction `matches` permet de déterminer si une chaîne correspond à une expression régulière spécifique. Consultez [ce document](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) pour plus d&#39;informations sur les modèles correspondants dans les expressions régulières.

**Format**

```sql
matches({STRING_1},STRING_2})
```

**Exemple**

La requête suivante détermine, sans tenir compte de la casse, si le nom de la personne début avec &quot;John&quot;.

```sql
matches(person.name.,"(?i)^John")
```

## Groupe d&#39;expressions régulières {#regexGroup}

La fonction `regexGroup` est utilisée pour extraire des informations spécifiques, en fonction de l&#39;expression régulière fournie.

**Format**

```sql
regexGroup({STRING},{EXPRESSION})
```

**Exemple**

La requête suivante est utilisée pour extraire le nom de domaine d’une adresse électronique.

```sql
regexGroup(emailAddress,"@(\w+)", 1)
```


## Fonctions

## Minuscule{#lower}

La fonction **lowerCase** convertit une chaîne en lettres minuscules.

Syntaxe :

```sql
{%=lowerCase(string)%}
```

Exemple :

Cette fonction convertit le prénom du profil en lettres minuscules.

```sql
{%=lowerCase(profile.person.name.firstName)%}
```

## majuscule{#upper}

La fonction **upper** convertit une chaîne en lettres minuscules.

Syntaxe :

```sql
{%=upperCase(string)%}
```

Exemple :

Cette fonction convertit le nom de profil en majuscules.

```sql
{%=upperCase(profile.person.name.lastName)%}
```
