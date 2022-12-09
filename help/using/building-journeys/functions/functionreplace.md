---
product: journey optimizer
title: replace
description: En savoir plus sur la fonction replace
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 3eb35fd6-2d11-4f24-b0d9-5334e7ed7872
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '148'
ht-degree: 0%

---

# replace {#replace}

Remplace la première occurrence correspondant à la chaîne cible par la chaîne de remplacement dans la chaîne de base.

Le remplacement s’effectue du début à la fin de la chaîne, par exemple, le remplacement de &quot;aa&quot; par &quot;b&quot; dans la chaîne &quot;aaa&quot; générera &quot;ba&quot; plutôt que &quot;ab&quot;.

## Catégorie

Chaîne

## Syntaxe de la fonction

`replace(<parameters>)`

## Paramètres

| Paramètre | Type |
|-----------|--------------|
| base | string |
| cible | string (RegExp) |
| remplacement | string |

## Signature et type renvoyé

`replace(<base>,<target>,<replacement>)`

Renvoie une chaîne.

## Exemple 1

`replace("Hello World", "l", "x")`

Renvoie &quot;Hexlo World&quot;.

## Exemple 2 {#example_2}

Comme le paramètre cible est un RegExp, selon la chaîne que vous souhaitez remplacer, vous devrez peut-être ajouter une séquence d’échappement à certains caractères. Voici un exemple :

* Chaîne à évaluer : `|OFFER_A|OFFER_B`
* fourni par un attribut de profil `#{ExperiencePlatform.myFieldGroup.profile.myOffers}`
* Chaîne à remplacer : `|OFFER_A`
* Chaîne remplacée par : `''`
* Vous devez ajouter `\\` avant l’événement `|` caractère.

L’expression est :

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|OFFER_A', '')`

La chaîne renvoyée est la suivante : `|OFFER_B`

Vous pouvez également créer la chaîne à remplacer à partir d’un attribut donné :

`replace(#{ExperiencePlatform.myFieldGroup.profile.myOffers}, '\\|' + #{ExperiencePlatform.myFieldGroup.profile.myOfferCode}, '')`
