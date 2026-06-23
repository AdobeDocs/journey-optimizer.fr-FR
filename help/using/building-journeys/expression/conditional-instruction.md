---
solution: Journey Optimizer
product: journey optimizer
title: Instruction conditionnelle (if, then, else/si, alors, sinon)
description: En savoir plus sur l’instruction conditionnelle
feature: Journeys
role: Developer
level: Experienced
keywords: avancé, condition, action, parcours
exl-id: 5a5b35a7-e3b5-4dc0-8a87-e985956b04a4
version: Journey Orchestration
TQID: https://experienceleague.adobe.com/SObpEvgu0D-pcoLVaKM7iRffLTSP1stp1zcg4Ygs-vQ
product_v2:
  - id: cb954087-f4fc-4456-afb9-e939cabcdc79
feature_v2:
  - id: b3538224-471e-4c63-a444-9b19d89ae29c
  - id: d998adac-2f81-400b-a669-d07bb196e4eb
subfeature_v2:
  - id: cce82f05-fc3c-4af7-85ff-8bba603861a7
  - id: d8353d85-5da7-453d-bd68-40ad33fa0ab7
role_v2:
  - id: ff6a42d2-313e-452e-93a6-792e4fad9ff8
source-git-commit: bf5866b0e7437f93936f573fd83ada8526fe004d
workflow-type: tm+mt
source-wordcount: 576
ht-degree: 29%

---

# Instruction conditionnelle (if, then, else/si, alors, sinon) {#conditional-instruction}

L’instruction conditionnelle (if, then, else) est prise en charge dans l’éditeur avancé. Elle permet de définir des expressions plus complexes. Elle se compose des éléments suivants :

* **[!UICONTROL If]** : condition à évaluer en premier.
* **[!UICONTROL then]** : expression à évaluer au cas où le résultat de l’évaluation de la condition serait vrai.
* **[!UICONTROL else]** : expression à évaluer au cas où le résultat de l’évaluation de la condition serait faux.

>[!NOTE]
>
>Toutes les expressions doivent être mises entre parenthèses.

```json
if  (<expression1>)
then
   (<expression2>)
else
   (<expression3>)
```

`<expression1>` doit renvoyer une valeur **booléenne**.

`<expression2>` et `<expression3>` doit avoir le même type ou des types compatibles. Les signatures prises en charge et les types renvoyés sont les suivants :

```json
boolean,boolean : boolean
dateTime,dateTime : dateTime
dateTimeOnly,dateTimeOnly : dateTimeOnly
decimal,integer : decimal
integer,decimal : integer
integer,decimal : decimal
duration,duration : duration
string,string : string
listBoolean,listBoolean : listBoolean
listDateTime,listDateTime : listDateTime
listDateTimeOnly,listDateTimeOnly : listDateTimeOnly
listDateOnly,listDateOnly : listDateOnly
listDecimal,listDecimal : listDecimal
listInteger,listInteger : listInteger
listString,listString : listString
```

**Utilisation**

L’instruction conditionnelle vous permet d’optimiser le workflow de parcours en réduisant le nombre d’activités de condition. Vous pouvez, par exemple, spécifier dans la même activité d’action, deux options pour une définition de champ en utilisant une seule expression de condition.

Exemple pour une activité d’action (pour un champ qui attend une chaîne comme résultat de l’instruction conditionnelle) :

```json
if (startWithIgnoreCase(@event{eventiOSPushPermissionAllowed.device.model}, 'iPad') or startWithIgnoreCase(@event{eventiOSPushPermissionAllowed.device.model}, 'iOS'))
then
   ('apns')
else
   ('fcm')
```

+++ Référence des connaissances sur l’IA

Cette section contient des connaissances structurées destinées à soutenir l’interprétation, la récupération et la réponse aux questions liées à ce sujet.

Pour une compréhension totale, ces informations doivent être combinées avec la documentation de cette page. Aucune des sources n’est conçue pour être autonome. La page décrit la fonctionnalité, tandis que cette section fournit un contexte supplémentaire qui permet de clarifier la terminologie, l’intention, l’applicabilité et les contraintes.

* **TL;DR:** Cette page explique l’instruction conditionnelle `if / then / else` disponible dans l’éditeur d’expression avancé par Parcours, y compris les règles de syntaxe, les combinaisons de types prises en charge et un exemple d’utilisation pratique.

**Intentions:**

* Écrivez une expression conditionnelle à l’aide de `if`, `then` et `else` pour renvoyer différentes valeurs en fonction d’une condition booléenne
* Réduisez le nombre d’activités de condition dans un parcours en incorporant une logique conditionnelle intégrée dans une seule activité d’action
* Déterminez quelles combinaisons de types de données sont valides pour les branches `then` et `else`
* Appliquez l’instruction conditionnelle pour acheminer les jetons de notification push vers APNS ou FCM en fonction du modèle de l’appareil

**Glossaire:**

* **Instruction conditionnelle** : construction d’expression `if / then / else` dans l’éditeur avancé qui évalue une valeur booléenne et renvoie l’une des deux expressions *(spécifique au produit)*
* **Éditeur d’expression avancé** : interface Journey Optimizer permettant d’écrire des expressions complexes utilisées dans des conditions, des activités d’attente et des *de mappage de paramètres d’action (spécifiques au produit)*

**Mécanismes de sécurisation :**

* Des parenthèses sont requises autour de toutes les expressions dans les clauses `if`, `then` et `else`
* La clause `if` (`<expression1>`) doit renvoyer un type booléen
* Les expressions `then` et `else` (`<expression2>` et `<expression3>`) doivent avoir le même type ou des types compatibles (par exemple, `decimal` et `integer` sont compatibles, `string` et `integer` ne le sont pas)
* Toutes les combinaisons de types ne sont pas prises en charge — seules les paires répertoriées dans le tableau des signatures prises en charge sont valides

**Terminologie:**

* Nom canonique : instruction conditionnelle — Acronyme : none — variantes : if/then/else, condition de style ternaire
* Synonymes : « instruction conditionnelle » = « condition intégrée » = « expression if-then-else »
* Ne les confondez pas : instruction conditionnelle (expression intégrée) ≠ activité Condition (nœud de zone de travail de parcours)

**FAQ:**

* **Q : La clause `if` doit-elle être placée entre parenthèses ?** — Oui, des parenthèses sont requises autour de toutes les expressions, y compris la condition dans la clause `if`.
* **Q : Puis-je utiliser `if / then / else` pour renvoyer un nombre d’une branche et une chaîne d’une autre ?** — Non ; `<expression2>` et `<expression3>` doivent avoir des types identiques ou compatibles.
* **Q : Comment l’instruction conditionnelle réduit-elle la complexité du parcours ?** — Il vous permet de spécifier deux alternatives de valeur de champ dans une seule activité d&#39;action à l&#39;aide d&#39;une seule expression, en évitant un nœud d&#39;activité Condition distinct sur la zone de travail.
* **Q : Quel type l&#39;instruction conditionnelle renvoie-t-elle si les deux branches sont des chaînes ?** — Renvoie un `string`.
* **Q : Peut-`if / then / else` être utilisé pour sélectionner un canal de notification push ?** — Oui ; par exemple, l’évaluation du modèle d’appareil pour renvoyer des `'apns'` pour les appareils Apple ou des `'fcm'` pour d’autres.

+++
