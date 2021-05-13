---
title: Bibliothèque de fonctions
description: Bibliothèque de fonctions
translation-type: tm+mt
source-git-commit: 55b9e5d8ed259ec6ed7746e835691d7d6261a8a4
workflow-type: tm+mt
source-wordcount: '696'
ht-degree: 98%

---

# Fonctions de chaîne {#string}

![](../../assets/do-not-localize/badge.png)


TBC CJM, fonctions de chaîne

## Like

La fonction `like` permet de déterminer si une chaîne correspond à un modèle donné.

**Format**

```sql
like ({STRING_1},{STRING_2})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | L’expression à laquelle comparer la première chaîne. Les deux caractères spéciaux pris en charge pour créer une expression sont `%` et `_`. <ul><li>`%` est utilisé pour représenter aucun ou plusieurs caractères.</li><li>`_` est utilisé pour représenter exactement un caractère.</li></ul> |

**Exemple**

La requête suivante récupère toutes les villes contenant le modèle « es ».

```sql
like (city ,"%es%")
```

## Starts with

La fonction `startsWith` permet de déterminer si une chaîne commence par une sous-chaîne donnée.

**Format**

```sql
startsWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à rechercher dans la première chaîne. |
| `{BOOLEAN}` | Un paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Par défaut, cette valeur est définie sur vraie. |

**Exemple**

La requête suivante détermine si le nom de la personne commence par « Joe » en respectant la casse.

```sql
startsWith(person.name,"Joe")
```

## Does not start with

La fonction `doesNotStartWith` permet de déterminer si une chaîne ne commence pas par une sous-chaîne donnée.

**Format**

```sql
doesNotStartWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à rechercher dans la première chaîne. |
| `{BOOLEAN}` | Un paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Par défaut, cette valeur est définie sur vraie. |

**Exemple**

La requête suivante détermine si le nom de la personne ne commence pas par « Joe » en respectant la casse.

```sql
doesNotStartWith(person.name,"Joe")
```

## Ends with

La fonction `endsWith` permet de déterminer si une chaîne se termine par une sous-chaîne donnée.

**Format**

```sql
endsWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à rechercher dans la première chaîne. |
| `{BOOLEAN}` | Un paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Par défaut, cette valeur est définie sur vraie. |

**Exemple**

La requête suivante détermine si l’adresse électronique de la personne se termine par « .com » en respectant la casse.

```sql
endsWith(person.emailAddress,".com")
```

## Does not end with

La fonction `doesNotEndWith` permet de déterminer si une chaîne ne se termine pas par une sous-chaîne donnée.

**Format**

```sql
doesNotEndWith({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à rechercher dans la première chaîne. |
| `{BOOLEAN}` | Un paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Par défaut, cette valeur est définie sur vraie. |

**Exemple**

La requête suivante détermine si l’adresse électronique de la personne ne se termine pas par « .com » en respectant la casse.

```sql
doesNotEndWith(person.emailAddress,".com")
```

## Contains

La fonction `contains` permet de déterminer si une chaîne contient une sous-chaîne donnée.

**Format**

```sql
contains({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à rechercher dans la première chaîne. |
| `{BOOLEAN}` | Un paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Par défaut, cette valeur est définie sur vraie. |

**Exemple**

La requête suivante détermine si l’adresse électronique de la personne contient la chaîne « 2010@gm » en respectant la casse.

```sql
contains(person.emailAddress,"2010@gm")
```

## Does not contain

La fonction `doesNotContain` permet de déterminer si une chaîne ne contient pas une sous-chaîne donnée.

**Format**

```sql
doesNotContain({STRING_1},{STRING_2}, {BOOLEAN})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à rechercher dans la première chaîne. |
| `{BOOLEAN}` | Un paramètre facultatif permettant de déterminer si la vérification est sensible à la casse. Par défaut, cette valeur est définie sur vraie. |

**Exemple**

La requête suivante détermine si l’adresse électronique de la personne ne contient pas la chaîne « 2010@gm » en respectant la casse.

```sql
doesNotContain(person.emailAddress,"2010@gm")
```

## Equals

La fonction `equals` permet de déterminer si une chaîne est égale à une sous-chaîne donnée.

**Format**

```sql
equals({STRING_1},{STRING_2})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à comparer à la première chaîne. |

**Exemple**

La requête suivante détermine si le nom de la personne est « John » en respectant la casse.

```sql
equals(person.name,"John")
```

## Not equal to

La fonction `notEqualTo` permet de déterminer si une chaîne est différente d’une chaîne donnée.

**Format**

```sql
notEqualTo({STRING_1},{STRING_2})
```

| Argument | Description |
| --------- | ----------- |
| `{STRING_1}` | La chaîne à vérifier. |
| `{STRING_2}` | La chaîne à comparer à la première chaîne. |

**Exemple**

La requête suivante détermine si le nom de la personne n’est pas « John » en respectant la casse.

```sql
notEqualTo(person.name,"John")
```

## Matches

La fonction `matches` permet de déterminer si une chaîne correspond à une expression régulière donnée. Reportez-vous à [ce document](https://docs.oracle.com/javase/8/docs/api/java/util/regex/Pattern.html) pour plus d’informations concernant les modèles correspondants dans les expressions régulières.

**Format**

```sql
matches({STRING_1},STRING_2})
```

**Exemple**

La requête suivante détermine si le nom de la personne commence par « John » sans tenir compte de la casse.

```sql
matches(person.name.,"(?i)^John")
```

## Regular expression group

La fonction `regexGroup` est utilisée pour extraire des informations spécifiques en fonction de l’expression régulière fournie.

**Format**

```sql
regexGroup({STRING},{EXPRESSION})
```

**Exemple**

La requête suivante est utilisée pour extraire le nom de domaine d’une adresse électronique.

```sql
regexGroup(emailAddress,"@(\w+)", 1)
```
