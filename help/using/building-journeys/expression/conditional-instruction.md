---
solution: Journey Optimizer
product: journey optimizer
title: Instruction conditionnelle (if, then, else)
description: En savoir plus sur l’instruction conditionnelle
feature: Journeys
role: Data Engineer
level: Experienced
exl-id: 5a5b35a7-e3b5-4dc0-8a87-e985956b04a4
source-git-commit: d17e64e03d093a8a459caef2fb0197a5710dfb7d
workflow-type: tm+mt
source-wordcount: '161'
ht-degree: 0%

---

# Instruction conditionnelle (if, then, else) {#conditional-instruction}

L’instruction conditionnelle (if, then, else) est prise en charge dans l’éditeur avancé. Il permet de définir des expressions plus complexes. Il se compose des éléments suivants :

* **[!UICONTROL if]**: la condition à évaluer en premier.
* **[!UICONTROL then]**: l’expression à évaluer au cas où le résultat de l’évaluation de la condition serait vrai.
* **[!UICONTROL else]**: l’expression à évaluer au cas où le résultat de l’évaluation de la condition serait faux.

>[!NOTE]
>
>Des parenthèses sont requises autour de toutes les expressions.

```json
if  (<expression1>)
then
   (<expression2>)
else
   (<expression3>)
```

`<expression1>` doit renvoyer une valeur **boolean**.

`<expression2>` et `<expression3>` doivent avoir le même type ou des types compatibles. Les signatures prises en charge et les types renvoyés sont les suivants :

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

L’instruction conditionnelle vous permet d’optimiser le processus du parcours en réduisant le nombre d’activités de condition. Par exemple, dans la même activité d’action, vous pouvez spécifier deux alternatives pour une définition de champ en utilisant une seule expression de condition.

Exemple pour une activité d’action (pour un champ qui attend une chaîne comme résultat de l’instruction conditionnelle) :

```json
if (startWithIgnoreCase(@{eventiOSPushPermissionAllowed.device.model}, 'iPad') or startWithIgnoreCase(@{eventiOSPushPermissionAllowed.device.model}, 'iOS'))
then
   ('apns')
else
   ('fcm')
```
