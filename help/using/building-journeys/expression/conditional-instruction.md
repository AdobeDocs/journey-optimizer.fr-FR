---
solution: Journey Optimizer
product: journey optimizer
title: Instruction conditionnelle (if, then, else / si, alors, sinon)
description: En savoir plus sur l’instruction conditionnelle
feature: Journeys
role: Developer
level: Experienced
keywords: avancé, condition, action, parcours
exl-id: 5a5b35a7-e3b5-4dc0-8a87-e985956b04a4
version: Journey Orchestration
source-git-commit: bdf857c010854b7f0f6ce4817012398e74a068d5
workflow-type: ht
source-wordcount: '168'
ht-degree: 100%

---

# Instruction conditionnelle (if, then, else / si, alors, sinon) {#conditional-instruction}

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
