---
product: journey optimizer
title: replace
description: En savoir plus sur la fonction replace
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 3eb35fd6-2d11-4f24-b0d9-5334e7ed7872
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: ht
source-wordcount: '146'
ht-degree: 100%

---

# replace {#replace}

Remplace la première occurrence correspondant à la chaîne cible par la chaîne de remplacement dans la chaîne de base.

Le remplacement s’effectue du début à la fin de la chaîne. Par exemple, le remplacement de « aa » par « b » dans la chaîne « aaa » donnera « ba » et non « ab ».

## Catégorie

Chaîne

## Syntaxe de la fonction

`replace(<parameters>)`

## Paramètres

| Paramètre | Type |
|-----------|--------------|
| base | chaîne |
| cible | chaîne (RegExp) |
| remplacement | chaîne |

## Signature et type renvoyé

`replace(<base>,<target>,<replacement>)`

Renvoie une chaîne.

## Exemple 1

`replace("Hello World", "l", "x")`

Renvoie « Hexlo World ».

## Exemple 2 {#example_2}

Comme le paramètre cible est un RegExp, selon la chaîne que vous souhaitez remplacer, vous devrez peut-être ajouter une séquence d’échappement à certains caractères. Voici un exemple :

* chaîne à évaluer : `|OFFER_A|OFFER_B`
* fourni par un attribut de profil `#{ExperiencePlatform.myFieldGroup.profile.myOffers}`
* Chaîne à remplacer : `|OFFER_A`
* Chaîne remplacée par : `''`
* Vous devez ajouter `\\` avant le caractère `|`.

L’expression est la suivante :

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

La chaîne renvoyée est la suivante : `|OFFER_B`

Vous pouvez également créer la chaîne à remplacer à partir d’un attribut donné :

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`
